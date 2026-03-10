# 🎯 Alle Hack The Box Zertifikate in 6 Monaten

> **Maximaler Effizienz-Plan** – Von Null zum vollständig zertifizierten HTB-Experten in 6 Monaten.

---

## 📋 Inhaltsverzeichnis

1. [Übersicht der Zertifikate](#-übersicht-der-zertifikate)
2. [Voraussetzungen](#-voraussetzungen)
3. [Der 6-Monats-Plan](#-der-6-monats-plan)
4. [Tagesablauf & Zeitplanung](#-tagesablauf--zeitplanung)
5. [Lernressourcen & Tipps](#-lernressourcen--tipps)
6. [Karrieremöglichkeiten](#-karrieremöglichkeiten)
7. [Gehaltsaussichten](#-gehaltsaussichten)
8. [Häufige Fehler vermeiden](#-häufige-fehler-vermeiden)

---

## 🏆 Übersicht der Zertifikate

| Zertifikat | Kürzel | Schwierigkeit | Schwerpunkt | Geschätzte Lernzeit |
|---|---|---|---|---|
| HTB Certified Junior Cybersecurity Associate | **CJCA** | ⭐ Einsteiger | Grundlagen Cybersecurity | ~3–4 Wochen |
| HTB Certified Bug Bounty Hunter | **CBBH** | ⭐⭐ Fortgeschritten | Web-Hacking & Bug Bounty | ~4 Wochen |
| HTB Certified Defensive Security Analyst | **CDSA** | ⭐⭐ Fortgeschritten | SOC, SIEM, Incident Response | ~4 Wochen |
| HTB Certified Penetration Testing Specialist | **CPTS** | ⭐⭐⭐ Experte | Vollständiges Pentesting | ~5–6 Wochen |
| HTB Certified Active Directory Pentester | **CAP** | ⭐⭐⭐ Experte | Active Directory Angriffe | ~3–4 Wochen |
| HTB Certified Web Exploitation Expert | **CWEE** | ⭐⭐⭐⭐ Elite | Fortgeschrittenes Web-Hacking | ~4–5 Wochen |

---

## ✅ Voraussetzungen

### Technische Grundkenntnisse (vor dem Start)

- **Grundlegende Linux-Kenntnisse** (Kommandozeile, Dateisystem, Berechtigungen)
- **Netzwerkgrundlagen** (TCP/IP, DNS, HTTP/S, OSI-Modell)
- **Grundlagen der Programmierung** (Python oder Bash hilfreich, aber nicht zwingend erforderlich)
- **Virtualisierung** (VirtualBox oder VMware für lokale Labs)

### Zeitlicher Aufwand

> ⏱️ **Mindestens 4–5 Stunden täglich** (ca. 30–35 Stunden/Woche) sind erforderlich, um diesen Plan realistisch umzusetzen.

### Tools & Setup

```bash
# Empfohlenes Setup vor dem Start
- Kali Linux oder Parrot OS (als VM oder Dual-Boot)
- HTB Academy Subscription (Jährlich für maximale Kosteneffizienz)
- VPN-Client für HTB Labs
- Notizen-Tool: Obsidian, Notion oder CherryTree
- Burp Suite Community/Pro
```

---

## 📅 Der 6-Monats-Plan

### 📌 Monat 1 – Wochen 1–4: CJCA (Grundlagen)

**Ziel:** Solide Grundlage in Cybersecurity aufbauen und ersten Meilenstein erreichen.

| Woche | Fokus | HTB Academy Modules |
|---|---|---|
| Woche 1 | Linux & Netzwerk-Grundlagen | *Linux Fundamentals*, *Network Enumeration with Nmap* |
| Woche 2 | Web-Grundlagen & Einführung Pentesting | *Web Requests*, *Introduction to Web Applications* |
| Woche 3 | Erste Exploitation-Techniken | *Getting Started*, *Footprinting* |
| Woche 4 | Prüfungsvorbereitung & Exam | Wiederholung + **CJCA-Exam** |

**Wochenziele:**
- ✔ Verstehe das OSI-Modell und TCP/IP in der Praxis
- ✔ Kann grundlegende Nmap-Scans durchführen und interpretieren
- ✔ Kennt die gängigsten Angriffsvektoren auf Webanwendungen
- ✔ Hat erstes HTB Starting Point / EASY-Machines gelöst

---

### 📌 Monat 2 – Wochen 5–8: CBBH (Bug Bounty Hunter)

**Ziel:** Web-Hacking-Fähigkeiten auf Profi-Niveau bringen.

| Woche | Fokus | HTB Academy Modules |
|---|---|---|
| Woche 5 | SQL Injection & Authentication Bypasses | *SQL Injection Fundamentals*, *Login Brute Forcing* |
| Woche 6 | XSS, CSRF, SSRF | *Cross-Site Scripting (XSS)*, *Server-side Attacks* |
| Woche 7 | IDOR, API-Hacking, File Inclusion | *File Inclusion*, *Web Attacks* |
| Woche 8 | Bug Bounty Workflow & Exam | *Bug Bounty Hunting Process* + **CBBH-Exam** |

**Wochenziele:**
- ✔ Beherrscht alle OWASP Top 10 Schwachstellen
- ✔ Kann Burp Suite professionell einsetzen
- ✔ Hat mindestens 2 HTB Web-Challenge Machines gelöst
- ✔ Versteht den Bug-Bounty-Meldeprozess

---

### 📌 Monat 3 – Wochen 9–12: CDSA (Defensiv)

**Ziel:** Die andere Seite der Cybersecurity verstehen – Angriffe erkennen und abwehren.

| Woche | Fokus | HTB Academy Modules |
|---|---|---|
| Woche 9 | SOC Grundlagen & SIEM | *Security Monitoring & SIEM Fundamentals* |
| Woche 10 | Log-Analyse & Threat Hunting | *Intro to Threat Hunting & Hunting With Elastic* |
| Woche 11 | Incident Response & Malware-Analyse | *Introduction to Malware Analysis*, *DFIR* |
| Woche 12 | Prüfungsvorbereitung & Exam | Wiederholung + **CDSA-Exam** |

**Wochenziele:**
- ✔ Kann Splunk/Elastic-Logs analysieren und IOCs erkennen
- ✔ Versteht MITRE ATT&CK Framework
- ✔ Hat einen Incident-Response-Plan erstellt
- ✔ Kann verdächtigen Netzwerktraffic analysieren (Wireshark)

---

### 📌 Monat 4 – Wochen 13–18: CPTS (Penetration Testing Specialist)

**Ziel:** Das umfangreichste und anspruchsvollste Zertifikat – vollständiges Enterprise-Pentesting.

> ⚠️ **Hinweis:** Dem CPTS-Kurs liegt ein sehr umfangreicher Lernpfad zugrunde (~750h Lerninhalt lt. HTB). Deshalb werden hier 6 Wochen eingeplant (Wochen 13–18).

| Woche | Fokus | HTB Academy Modules |
|---|---|---|
| Woche 13 | Reconnaissance & Enumeration | *Information Gathering – Web Edition*, *Footprinting* |
| Woche 14 | Exploitation & Post-Exploitation | *Exploitation*, *Shells & Payloads*, *Using the Metasploit Framework* |
| Woche 15 | Privilege Escalation (Linux & Windows) | *Linux Privilege Escalation*, *Windows Privilege Escalation* |
| Woche 16 | Active Directory Grundlagen | *Active Directory Enumeration & Attacks* (Teil 1) |
| Woche 17 | Pivoting, Reporting | *Pivoting, Tunneling, and Port Forwarding*, *Documentation & Reporting* |
| Woche 18 | Prüfungsvorbereitung & Exam | Wiederholung + **CPTS-Exam** (10-tägiges Praxisexamen!) |

**Wochenziele:**
- ✔ Kann einen vollständigen Pentest-Report schreiben
- ✔ Beherrscht Pivoting und Tunneling-Techniken
- ✔ Hat mindestens 5 HTB Pro Labs / MEDIUM-Machines gelöst
- ✔ Versteht den kompletten Pentest-Lifecycle

---

### 📌 Monat 5 – Wochen 19–22: CAP (Active Directory Pentester)

**Ziel:** Spezialisierung auf Active Directory – das Herzstück moderner Unternehmensinfrastrukturen.

> 💡 **Vorteil:** Das AD-Wissen aus dem CPTS-Lernpfad ist direkte Vorbereitung für CAP!

| Woche | Fokus | HTB Academy Modules |
|---|---|---|
| Woche 19 | AD Enumeration & Kerberos | *Active Directory Enumeration & Attacks* (Teil 2), *Kerberoasting* |
| Woche 20 | AD Exploitation – Classic Attacks | *DCSync*, *Pass-the-Hash*, *Pass-the-Ticket*, *BloodHound* |
| Woche 21 | AD Exploitation – Moderne Angriffe | *ADCS*, *Delegation Attacks*, *Trust Attacks* |
| Woche 22 | Prüfungsvorbereitung & Exam | Wiederholung + **CAP-Exam** |

**Wochenziele:**
- ✔ Beherrscht BloodHound/SharpHound für AD-Recon
- ✔ Kann Golden/Silver Ticket Angriffe durchführen
- ✔ Versteht Kerberos-Protokoll tief
- ✔ Hat HTB Pro Lab (z. B. *Offshore* oder *RastaLabs*) begonnen

---

### 📌 Monat 6 – Wochen 23–26: CWEE (Web Exploitation Expert)

**Ziel:** Das Elite-Level im Web-Hacking – fortgeschrittene und komplexe Web-Exploits.

| Woche | Fokus | HTB Academy Modules |
|---|---|---|
| Woche 23 | Advanced SQL Injection & XXE | *Advanced SQL Injections*, *XML External Entity (XXE) Injection* |
| Woche 24 | Deserialization & Prototype Pollution | *Whitebox Pentesting 101: Command Injection*, *Advanced Deserialization* |
| Woche 25 | OAuth, JWT & moderne Auth-Schwachstellen | *Abusing HTTP Misconfigurations*, *Advanced XSS* |
| Woche 26 | Prüfungsvorbereitung & Exam | Wiederholung + **CWEE-Exam** |

**Wochenziele:**
- ✔ Kann Source-Code-Reviews für Sicherheitslücken durchführen
- ✔ Beherrscht fortgeschrittene Exploit-Techniken
- ✔ Hat mindestens 3 HTB HARD/INSANE-Level Web-Challenges gelöst
- ✔ Versteht Server-Side Template Injection, SSTI, SSRF-Chains

---

## ⏰ Tagesablauf & Zeitplanung

### Empfohlener Tagesplan (Wochentag)

```
06:30 – 07:00   Wiederholung Notizen vom Vortag (30 min)
07:00 – 09:00   Neue HTB Academy Module durcharbeiten (2h)
12:00 – 13:00   Übungen / Labs (1h – Mittagspause nutzen)
18:00 – 21:00   Praktische Übungen auf HTB / TryHackMe (3h)
21:00 – 21:30   Notizen zusammenfassen & Cheatsheet aktualisieren (30 min)
```
**Gesamt Wochentag: ~6,5 Stunden**

### Wochenende

```
Samstag:   8–10 Stunden intensives Lernen / CTF-Challenges
Sonntag:   4–6 Stunden Wiederholung + Schwachpunkte aufarbeiten
```
**Gesamt Wochenende: 12–16 Stunden**

### Wöchentliche Gesamtstunden: ~44–50 Stunden

---

## 📚 Lernressourcen & Tipps

### Primäre Ressourcen (Pflicht)

| Ressource | Zweck | Kosten |
|---|---|---|
| **HTB Academy** | Hauptlernplattform für alle Zertifikate | ~14€/Monat (Annual) |
| **Hack The Box** (Main Platform) | Praktische Machine-Übungen | Free / ~14€/Monat |
| **PortSwigger Web Academy** | Zusatz für CBBH & CWEE | Kostenlos |

### Sekundäre Ressourcen (Empfohlen)

| Ressource | Zweck | Kosten |
|---|---|---|
| **TryHackMe** | Anfänger-freundliche Labs | Free / 14$/Monat |
| **HackTricks** (https://book.hacktricks.xyz) | Referenz & Cheatsheets | Kostenlos |
| **GTFOBins / LOLBAS** | PrivEsc Referenz | Kostenlos |
| **PayloadsAllTheThings** (GitHub) | Exploit-Payloads Sammlung | Kostenlos |
| **0xdf.gitlab.io** | HTB Machine Writeups | Kostenlos |

### 🔑 Effizienz-Tipps

1. **Notizen-System aufbauen:** Nutze Obsidian mit einer strukturierten Vault. Erstelle für jedes Thema eine eigene Note mit Befehlen und Erkenntnissen.

2. **Cheatsheets erstellen:** Nach jedem Modul ein persönliches Cheatsheet anlegen. Das hilft enorm im Examen.

3. **HTB-Machines parallel zu Modulen lösen:** Sobald du ein Thema gelernt hast, löse sofort eine passende HTB-Machine dazu.

4. **Community nutzen:** HTB Discord, Reddit (r/hackthebox) und HTB Forum sind Gold wert bei Blockaden.

5. **Exam-Strategie:** Lies die Exam-Guides von HTB sorgfältig. Besonders beim CPTS hast du 10 Tage – nutze sie vollständig.

6. **Lücken dokumentieren:** Führe eine "Weakness List" – Themen, die du noch nicht sicher beherrschst.

---

## 💼 Karrieremöglichkeiten

Nach Abschluss aller 6 HTB-Zertifikate bist du einer der am besten ausgebildeten Cybersecurity-Praktiker auf dem Markt. Dir stehen folgende Karrierewege offen:

### 🔴 Offensive Security (Red Team)

| Position | Aufgaben |
|---|---|
| **Penetration Tester (Junior/Mid/Senior)** | Sicherheitstests für Unternehmen, Netzwerke, Web-Apps |
| **Red Team Operator** | Simulierte APT-Angriffe auf Unternehmensinfrastrukturen |
| **Bug Bounty Hunter (selbstständig)** | Schwachstellen auf Plattformen wie HackerOne, Bugcrowd melden |
| **Exploit Developer** | Entwicklung von Proof-of-Concept Exploits |
| **Offensive Security Engineer** | Aufbau von Red-Team-Infrastrukturen und Tools |

### 🔵 Defensive Security (Blue Team)

| Position | Aufgaben |
|---|---|
| **SOC Analyst (Tier 1–3)** | Monitoring, Alert-Triage, Incident Response |
| **Threat Hunter** | Proaktive Suche nach Bedrohungen im Netzwerk |
| **Incident Responder** | Reaktion auf Sicherheitsvorfälle & Forensik |
| **DFIR Analyst** | Digitale Forensik und Incident Response |
| **Security Engineer** | Aufbau & Betrieb von Sicherheitsinfrastrukturen |

### 🟣 Purple Team / Consulting

| Position | Aufgaben |
|---|---|
| **Security Consultant** | Beratung von Unternehmen zu Sicherheitsstrategien |
| **CISO / Security Manager** | Strategische Leitung der IT-Sicherheit |
| **Freelance Pentester** | Eigenständige Sicherheitsaudits für Kunden |
| **Security Trainer / Instructor** | Schulungen für Unternehmens- und Hochschulteams |

### 🌐 Selbstständigkeit

- **Freelance Penetration Testing** (Stundensätze: 120–250€/h in D-A-CH)
- **Bug Bounty** (Top-Hunter verdienen 100.000–500.000+ €/Jahr)
- **Security Consulting** für KMUs
- **YouTube/Blog** – Content zu Cybersecurity (Monetarisierung via Sponsoring, Kurse)

---

## 💰 Gehaltsaussichten

### Deutschland (D-A-CH Region)

| Position | Berufserfahrung | Jahresgehalt (brutto) |
|---|---|---|
| Junior Penetration Tester | 0–2 Jahre | 45.000 – 60.000 € |
| Mid-Level Penetration Tester | 2–5 Jahre | 65.000 – 85.000 € |
| Senior Penetration Tester | 5+ Jahre | 90.000 – 130.000 € |
| SOC Analyst (Tier 1) | 0–2 Jahre | 40.000 – 55.000 € |
| SOC Analyst (Tier 2–3) | 2–5 Jahre | 55.000 – 75.000 € |
| Red Team Operator | 3–7 Jahre | 80.000 – 120.000 € |
| Security Consultant | 3+ Jahre | 75.000 – 110.000 € |
| CISO | 8+ Jahre | 120.000 – 200.000 € |

### International (Remote/USA/UK)

| Position | Jahresgehalt (brutto) |
|---|---|
| Junior Pentester (USA) | $70,000 – $95,000 |
| Mid-Level Pentester (USA) | $100,000 – $140,000 |
| Senior Pentester (USA) | $150,000 – $200,000+ |
| Bug Bounty Top 1% | $100,000 – $500,000+ |

> 💡 **Tipp:** Mit allen 6 HTB-Zertifikaten + 1–2 Jahren Praxiserfahrung sind Remote-Jobs mit international wettbewerbsfähigen Gehältern realistisch erreichbar. Die tatsächlichen Gehaltsaussichten variieren je nach Marktlage, Arbeitgeber und individueller Erfahrung. LinkedIn und Toptal sind gute Einstiegsplattformen.

---

## ⚠️ Häufige Fehler vermeiden

### ❌ Fehler 1: Zu viel Theorie, zu wenig Praxis
**Lösung:** Für jede Stunde Theorie mindestens eine Stunde Praxis auf HTB-Machines einplanen.

### ❌ Fehler 2: Keine Notizen machen
**Lösung:** Jede neue Technik, jeden Befehl und jeden Exploit sofort dokumentieren. Im Exam wirst du froh sein.

### ❌ Fehler 3: Zu schnell zum Writeup schauen
**Lösung:** Mindestens 2–4 Stunden selbst an einer Machine arbeiten, bevor du dir Hilfe holst. Das Kämpfen ist der Lerneffekt.

### ❌ Fehler 4: Module überspringen
**Lösung:** Zertifikate bauen aufeinander auf. Besonders CPTS setzt CJCA und CBBH-Wissen voraus.

### ❌ Fehler 5: Exam unterschätzen
**Lösung:** Besonders der CPTS-Exam ist ein 10-tägiges Praxis-Examen. Voll ausgeruhst beginnen, Notizen nutzen.

### ❌ Fehler 6: Burnout durch Überarbeitung
**Lösung:** Mindestens 1 Tag/Woche komplett freinehmen. Marathon, kein Sprint.

---

## 📊 Fortschritts-Tracker

```
Monat 1: [ ] CJCA
Monat 2: [ ] CBBH
Monat 3: [ ] CDSA
Monat 4: [ ] CPTS
Monat 5: [ ] CAP
Monat 6: [ ] CWEE
```

---

## 🔗 Nützliche Links

- [HTB Academy](https://academy.hackthebox.com/) – Hauptlernplattform
- [Hack The Box](https://www.hackthebox.com/) – Labs & Machines
- [PortSwigger Web Academy](https://portswigger.net/web-security) – Kostenlose Web-Security Labs
- [HackTricks](https://book.hacktricks.xyz/) – Umfassende Referenz
- [PayloadsAllTheThings](https://github.com/swisskyrepo/PayloadsAllTheThings) – Payload-Sammlung
- [GTFOBins](https://gtfobins.github.io/) – Linux PrivEsc Referenz
- [LOLBAS](https://lolbas-project.github.io/) – Windows PrivEsc Referenz

---

## ⭐ Zertifizierungsreihenfolge (Zusammenfassung)

```
Monat 1  →  CJCA   (Grundlagen)
Monat 2  →  CBBH   (Web Hacking)
Monat 3  →  CDSA   (Defensiv / Blue Team)
Monat 4  →  CPTS   (Vollständiges Pentesting) ← 6 Wochen!
Monat 5  →  CAP    (Active Directory)
Monat 6  →  CWEE   (Advanced Web Exploitation)
```

> 🎓 **Nach 6 Monaten:** Du besitzt 6 anerkannte Industriezertifikate, hast hunderte Stunden Praxiserfahrung und bist bereit für den Einstieg oder Aufstieg in der Cybersecurity-Branche.

---

*Erstellt für den maximalen Effizienz-Lernpfad. Viel Erfolg auf deiner HTB-Reise! 🚀*