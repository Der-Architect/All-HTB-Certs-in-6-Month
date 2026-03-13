# VM and VPN setup for HTB (Kali & Parrot) — Step‑by‑step with screenshots

Last updated: 2026-03-13

## Summary

This guide shows how to set up Kali Linux and Parrot Security OS in VirtualBox or VMware, install guest tools, and configure a VPN client to connect to Hack The Box (HTB). It includes step-by-step commands, configuration tips, and troubleshooting. Screenshots are referenced and named under `docs/images/` so you can add the actual captures later.

---

## Legal & ethical notice

Only connect to systems you have explicit permission to test. Use HTB and similar platforms according to their terms of service. Do not attempt to access or attack machines outside authorized labs.

---

## Requirements

- Host OS: Windows, macOS, or Linux
- Virtualization: VirtualBox (recommended) or VMware Workstation/Player
- HTB account with VPN access (Export `.ovpn` from HTB VPN page)
- Internet access for the VM
- Basic familiarity with terminal commands

---

## Minimum recommended VM specs

| Setting | Minimum | Recommended |
|---------|---------|-------------|
| CPU | 2 vCPUs | 4 vCPUs |
| RAM | 2 GB (light tasks) | 4–8 GB |
| Disk | 30 GB (thin-provisioned) | 50 GB |
| Network | NAT | NAT or Bridged |
| Display | 1024×768 | 1920×1080 |

- **Network — NAT** (default): easiest, works for HTB VPN.
- **Network — Bridged**: VM appears on your LAN with its own IP. Use when you want other LAN devices to reach the VM.

---

## Recommended HTB access

HTB has free and paid tiers. For active labs, retired boxes, and certificate tracks, a paid tier (Pro/VIP) gives broader access. Check [HTB](https://www.hackthebox.com) for current plans and what each includes.

---

## Download OS images and verify

1. **Kali Linux**
   - Website: <https://www.kali.org/get-kali/>
   - Choose the appropriate image (VirtualBox `.ova` or ISO).

2. **Parrot Security OS**
   - Website: <https://parrotsec.org/download/>
   - Choose `Home` or `Security` edition as needed.

3. **Verify checksum** (replace filenames as appropriate):

   ```bash
   sha256sum kali-*.iso
   sha256sum parrot-*.iso
   ```

   Download the `.sha256` or `.sha512` file from the distro site and confirm the computed checksum matches the published value before proceeding.

**Screenshot:** `docs/images/01-download-and-verify.png`
> Shows download page for Kali/Parrot and terminal output of `sha256sum`.

---

## VirtualBox — import/create VM (recommended)

### Option A — Import OVA (easiest)

1. Open VirtualBox → **File** → **Import Appliance** → select the downloaded `.ova`.
2. Review and adjust settings before importing:
   - **System → Base Memory**: 4096 MB (or as recommended by the distro).
   - **Processor**: 2 or more CPUs.
   - **Storage**: Ensure disk size meets your needs.
   - **Network → Adapter 1 → Attached to**: `NAT` (or `Bridged Adapter` if preferred).
3. Click **Import**, then start the VM and complete first-boot steps.

### Option B — Create VM from ISO

1. VirtualBox → **New** → Name: `kali` or `parrot`.
2. Type: **Linux**; Version: **Debian (64-bit)**.
3. Memory: **4096 MB**.
4. Create virtual hard disk (VDI), **30 GB**, dynamically allocated.
5. **Settings → Storage** → mount the ISO under **Controller: IDE**.
6. Start the VM and run the normal installer.

**Screenshot:** `docs/images/02-vbox-import-or-create.png`
> Shows Import Appliance dialog and VM Settings → System / Network tabs.

---

## VirtualBox — Guest Additions (Linux)

Installing Guest Additions enables clipboard sharing, drag-and-drop, and automatic screen resizing.

In the running VM terminal:

```bash
# 1. Update and install build dependencies
sudo apt update && sudo apt upgrade -y
sudo apt install -y build-essential dkms linux-headers-$(uname -r)
```

2. In the VirtualBox menu: **Devices → Insert Guest Additions CD image…**

```bash
# 3. Mount and run the installer
sudo mkdir -p /mnt/cdrom
sudo mount /dev/cdrom /mnt/cdrom
sudo sh /mnt/cdrom/VBoxLinuxAdditions.run
```

4. Reboot the VM:

```bash
sudo reboot
```

**Screenshot:** `docs/images/03-guest-additions-install.png`
> Shows "Insert Guest Additions" menu item and terminal running the installer.

---

## VMware — import/create and Tools

### Import or create

- **Import OVA/OVF**: **File → Open** → select the downloaded `.ova`.
- **New VM from ISO**: use the New Virtual Machine wizard, select the ISO, and follow the prompts.

### Install VMware Tools (open-vm-tools)

```bash
sudo apt update
sudo apt install -y open-vm-tools-desktop fuse
sudo reboot
```

**Screenshot:** `docs/images/04-vmware-import-vmtools.png`
> Shows VMware import dialog and terminal installing `open-vm-tools`.

---

## Network modes explained

| Mode | Description | Suitable for HTB? |
|------|-------------|------------------|
| **NAT** | VM uses host IP for outbound connections. Easiest setup. | ✅ Yes |
| **Bridged** | VM gets its own IP on your LAN. | ✅ Yes (if needed) |
| **Host-only** | Isolated network between host and VM only. | ❌ No internet access |

For most HTB use cases **NAT** is sufficient.

---

## HTB VPN overview

- HTB provides a `.ovpn` file from your HTB profile (VPN tab).
- You must only use the HTB VPN for HTB labs and must abide by their rules.
- The `.ovpn` file contains keys and routes to the HTB lab network. **Keep it private — do not share it.**

---

## Install OpenVPN (CLI) and NetworkManager plugin (GUI)

On Kali / Parrot (Debian-based):

```bash
# CLI client
sudo apt update
sudo apt install -y openvpn

# GUI + NetworkManager integration (optional)
sudo apt install -y network-manager-openvpn network-manager-openvpn-gnome
```

**Screenshot:** `docs/images/05-install-openvpn-nm.png`
> Shows terminal installing packages.

---

## Connect using CLI (recommended for HTB)

1. Place your HTB `.ovpn` file in `~/Downloads/` (or `~/htb/`).

2. Start the VPN tunnel (replace `<file>` with your actual filename):

   ```bash
   sudo openvpn --config ~/Downloads/<file>.ovpn
   ```

3. Keep the terminal open. You should see output ending with:

   ```
   Initialization Sequence Completed
   ```

4. Verify the tunnel interface is up (in a second terminal):

   ```bash
   ip a show tun0
   ping -c 3 10.10.10.10    # HTB gateway — adjust IP as needed
   ```

**Screenshot:** `docs/images/06-cli-vpn-connect.png`
> Shows terminal with `openvpn` running and `Initialization Sequence Completed` message.

---

## Connect using NetworkManager / GUI (optional)

If you installed `network-manager-openvpn-gnome`:

1. Open **Settings → Network** (or click the network icon in the taskbar).
2. Click **+** next to VPN.
3. Select **Import from file…** and choose your `.ovpn` file.
4. The connection is created automatically. Click the toggle to connect.

Alternatively, use `nmcli` from a terminal:

```bash
# Import the .ovpn as a NetworkManager connection
sudo nmcli connection import type openvpn file ~/Downloads/<file>.ovpn

# Bring the connection up (connection name matches the filename without extension)
nmcli connection up "<file>"
```

**Screenshot:** `docs/images/07-nm-vpn-import.png`
> Shows GNOME NetworkManager VPN import dialog with the `.ovpn` file selected.

---

## Verify connectivity to HTB

After connecting (CLI or GUI), confirm you can reach the HTB network:

```bash
# Check assigned tunnel IP
ip a show tun0

# Ping the HTB VPN gateway (IP may vary — check your .ovpn or HTB profile)
ping -c 4 10.10.10.1

# DNS check (optional)
nslookup hackthebox.eu
```

A successful ping confirms the VPN is routing traffic correctly.

**Screenshot:** `docs/images/08-verify-htb-connectivity.png`
> Shows `ip a show tun0` and successful ping output.

---

## Troubleshooting

### VPN fails to start

| Symptom | Likely cause | Fix |
|---------|-------------|-----|
| `Error opening configuration file` | Wrong path to `.ovpn` | Check the path: `ls ~/Downloads/*.ovpn` |
| `Cannot open TUN/TAP dev /dev/net/tun` | TUN device not available | Run `sudo modprobe tun` |
| `AUTH_FAILED` | Expired or invalid certificate | Download a fresh `.ovpn` from your HTB profile |
| Connection drops repeatedly | MTU mismatch | Add `--mssfix 1400` or set `mssfix 1400` in the `.ovpn` |

### NetworkManager import issues

- If the import silently fails, try the CLI method instead.
- Ensure `network-manager-openvpn` is installed and the `NetworkManager` service is running:

  ```bash
  sudo systemctl status NetworkManager
  sudo systemctl restart NetworkManager
  ```

### No internet in VM after VPN connects

- The VPN may be routing all traffic through the tunnel. This is expected behaviour for HTB's split-tunnel config. If you need internet and VPN simultaneously, check the **Use this connection only for resources on its network** option in NetworkManager, or add `route-nopull` to your `.ovpn` (note: this may affect HTB routing).

### Guest clipboard / screen resize not working

- Confirm Guest Additions / VMware Tools are installed and the VM was rebooted after installation.
- In VirtualBox: **Devices → Shared Clipboard → Bidirectional**.

**Screenshot:** `docs/images/09-troubleshooting-examples.png`
> Shows common error messages and their resolutions in a terminal.

---

## Security notes

- **Keep your `.ovpn` private.** It contains your unique key material. Do not commit it to version control or share it publicly.
- **Use a dedicated VM** for HTB work. Avoid mixing personal data with your attack environment.
- **Snapshot before each session.** VirtualBox and VMware both support snapshots. Taking one before connecting to a new HTB machine lets you roll back if something goes wrong.
- **Update your OS regularly** to stay current with tool versions and security patches:

  ```bash
  sudo apt update && sudo apt full-upgrade -y
  ```

- **Do not attack machines outside HTB.** The VPN gives access only to HTB's lab network. Any scanning or exploitation attempts on external hosts are illegal and violate HTB's terms of service.

---

## Quick-reference command cheatsheet

```bash
# Update system
sudo apt update && sudo apt full-upgrade -y

# Install OpenVPN
sudo apt install -y openvpn

# Connect to HTB VPN (CLI)
sudo openvpn --config ~/htb/<your-file>.ovpn

# Check VPN interface
ip a show tun0

# Ping HTB gateway
ping -c 4 10.10.10.1

# Import .ovpn into NetworkManager
sudo nmcli connection import type openvpn file ~/htb/<your-file>.ovpn

# Bring VPN up via nmcli
nmcli connection up "<your-file>"

# Bring VPN down via nmcli
nmcli connection down "<your-file>"

# Install VirtualBox Guest Additions deps
sudo apt install -y build-essential dkms linux-headers-$(uname -r)

# Mount Guest Additions CD and run installer
sudo mkdir -p /mnt/cdrom && sudo mount /dev/cdrom /mnt/cdrom
sudo sh /mnt/cdrom/VBoxLinuxAdditions.run

# Install VMware Tools
sudo apt install -y open-vm-tools-desktop fuse
```

---

## Screenshot index

| File | Description |
|------|-------------|
| `docs/images/01-download-and-verify.png` | Kali/Parrot download page and `sha256sum` terminal output |
| `docs/images/02-vbox-import-or-create.png` | VirtualBox Import Appliance dialog and VM Settings |
| `docs/images/03-guest-additions-install.png` | Insert Guest Additions menu and installer terminal output |
| `docs/images/04-vmware-import-vmtools.png` | VMware import dialog and `open-vm-tools` install |
| `docs/images/05-install-openvpn-nm.png` | Terminal installing OpenVPN and NetworkManager plugin |
| `docs/images/06-cli-vpn-connect.png` | `openvpn` terminal output with `Initialization Sequence Completed` |
| `docs/images/07-nm-vpn-import.png` | GNOME NetworkManager VPN import dialog |
| `docs/images/08-verify-htb-connectivity.png` | `ip a show tun0` and ping output |
| `docs/images/09-troubleshooting-examples.png` | Common error messages and resolutions |

> **Note:** The `docs/images/` directory is a placeholder. Add your own screenshots named as listed above to illustrate each step.

---

*For the latest VPN configuration and lab network details, always refer to the [HTB VPN page](https://www.hackthebox.com/home/htb/access) in your HTB profile.*
