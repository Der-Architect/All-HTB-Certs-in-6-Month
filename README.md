# All HTB Certs in Under One Year — A Complete Guide

> **Goal:** Earn all four primary Hack The Box (HTB) Academy certifications — CPTS, CBBH, CDSA, and CWEE — within 12 months (or as few as 6 months for full-time learners).

---

## Table of Contents

1. [Why This Guide](#why-this-guide)
2. [The Certifications at a Glance](#the-certifications-at-a-glance)
3. [Prerequisites](#prerequisites)
4. [Study Roadmap](#study-roadmap)
   - [6-Month Plan (Full-Time ~4 hrs/day)](#6-month-plan-full-time-4-hrsday)
   - [12-Month Plan (Part-Time ~2 hrs/day)](#12-month-plan-part-time-2-hrsday)
5. [Certification Deep-Dives](#certification-deep-dives)
   - [CBBH — Certified Bug Bounty Hunter](#1-cbbh--certified-bug-bounty-hunter)
   - [CDSA — Certified Defensive Security Analyst](#2-cdsa--certified-defensive-security-analyst)
   - [CPTS — Certified Penetration Testing Specialist](#3-cpts--certified-penetration-testing-specialist)
   - [CWEE — Certified Web Exploitation Expert](#4-cwee--certified-web-exploitation-expert)
6. [Study Tips & Best Practices](#study-tips--best-practices)
7. [Recommended Tools & Resources](#recommended-tools--resources)
8. [Exam Strategy](#exam-strategy)
9. [Frequently Asked Questions](#frequently-asked-questions)

---

## Why This Guide

Hack The Box Academy offers the most hands-on, practical certification track in offensive and defensive security today. Unlike multiple-choice based alternatives, every HTB exam is **100% practical** — no guessing, no memorisation tricks, just real-world skills. This guide gives you a clear, ordered, and time-boxed plan to earn all four certifications without wasting time or money.

---

## The Certifications at a Glance

| Cert | Full Name | Level | Focus | Modules | Est. Study Hours | Exam Duration |
|------|-----------|-------|-------|---------|-----------------|---------------|
| **CBBH** | Certified Bug Bounty Hunter | Intermediate | Web app security & bug bounty | 20 | ~144 hrs | 7 days |
| **CDSA** | Certified Defensive Security Analyst | Intermediate | SOC operations & incident response | 15 | ~184 hrs | 7 days |
| **CPTS** | Certified Penetration Testing Specialist | Intermediate | Full-scope enterprise pentesting | 28 | ~344 hrs | 10 days |
| **CWEE** | Certified Web Exploitation Expert | Advanced | Advanced & hard-to-find web vulnerabilities | 20+ | ~200 hrs | 7 days |

**Combined estimated study time: ~870 hours**
- At **4 hrs/day**: ~218 days (~7 months)
- At **2–3 hrs/day**: ~290–435 days, averaging to well under 12 months

---

## Prerequisites

Before starting the path, you should be comfortable with the following:

- **Networking basics** — TCP/IP, DNS, HTTP/S, ports and protocols
- **Linux command line** — file navigation, permissions, piping, scripting
- **Windows basics** — file system, PowerShell, Active Directory concepts
- **Basic programming / scripting** — Python or Bash for automation
- **Web fundamentals** — HTML, HTTP requests/responses, cookies, sessions

> No prior certifications are required. HTB Academy's paths start from fundamentals and build up organically.

---

## Study Roadmap

### 6-Month Plan (Full-Time ~4 hrs/day)

This plan is designed for learners who can dedicate at least 4 hours every day (e.g., students, career-changers, or those on a sabbatical).

| Month | Focus | Certification Target |
|-------|-------|---------------------|
| **Weeks 1–4** | Complete all CBBH modules (web requests, XSS, SQLi, SSRF, file uploads, API hacking) + **CBBH exam** | ✅ CBBH |
| **Weeks 5–8** | Complete all CDSA modules (SIEM, Splunk, incident handling, malware analysis, threat hunting) + **CDSA exam** | ✅ CDSA |
| **Weeks 9–16** | Work through CPTS path modules (recon, exploitation, AD attacks, lateral movement, post-exploitation) | — |
| **Weeks 17–20** | Complete CPTS capstone modules + take and pass the **CPTS exam** | ✅ CPTS |
| **Weeks 21–24** | Study advanced CWEE modules + take and pass the **CWEE exam** | ✅ CWEE |

---

### 12-Month Plan (Part-Time ~2 hrs/day)

This plan is designed for learners who are working or studying full-time alongside this certification track.

| Period | Focus | Certification Target |
|--------|-------|---------------------|
| **Months 1–2** | Complete all CBBH modules at a relaxed pace, revisiting weak areas | — |
| **Month 3** | CBBH exam prep + take the **CBBH exam** | ✅ CBBH |
| **Months 4–5** | Complete all CDSA modules (blue team, SOC, DFIR) | — |
| **Month 6** | CDSA exam prep + take the **CDSA exam** | ✅ CDSA |
| **Months 7–9** | Work through the large CPTS path (28 modules) | — |
| **Month 10** | CPTS exam prep (ProLabs, capstone) + take the **CPTS exam** | ✅ CPTS |
| **Months 11–12** | Complete CWEE advanced modules + take the **CWEE exam** | ✅ CWEE |

---

## Certification Deep-Dives

### 1. CBBH — Certified Bug Bounty Hunter

**Why start here?** CBBH covers foundational web application security that feeds directly into CWEE (advanced) and complements CPTS (web attacks module). Starting here builds the web mental model early.

**Key Topics Covered:**
- Web requests & proxies (Burp Suite)
- Information gathering & web reconnaissance
- Cross-Site Scripting (XSS)
- SQL injection (SQLi)
- Server-Side Request Forgery (SSRF)
- Command injection & file upload attacks
- Web services & API hacking
- Session security & authentication attacks

**Exam Format:**
- All modules must be 100% complete before the exam unlocks
- 7-day practical exam in a bug-bounty-style environment
- Must identify, exploit, and write a professional bug bounty report
- One free retake included

**Tips:**
- Use a notes tool like Obsidian or CherryTree to capture every technique per module
- Practice Burp Suite Community Edition daily — speed with the proxy is essential
- Write mini-reports after each module's skills assessment to build report writing habits early

---

### 2. CDSA — Certified Defensive Security Analyst

**Why second?** After learning how attackers operate (CBBH), pivoting to the blue-team perspective dramatically accelerates your understanding of detection and incident response.

**Key Topics Covered:**
- Security Monitoring & SIEM fundamentals
- Splunk and ELK stack (log ingestion, queries, dashboards)
- Incident handling process (PICERL framework)
- Windows & network forensics
- Threat hunting with YARA and Sigma
- Malware analysis (static and dynamic)
- Digital Forensics & Incident Response (DFIR)

**Exam Format:**
- Complete the SOC Analyst job-role path (100%)
- 7-day hands-on exam: investigate a simulated security incident
- Must produce a commercial-grade security incident report
- One free retake included

**Tips:**
- Invest time in understanding Splunk SPL query language — it appears throughout the exam
- Build a personal reference sheet for common log sources and IOC patterns
- Practice incident report writing using the HTB-provided templates throughout your study

---

### 3. CPTS — Certified Penetration Testing Specialist

**Why third?** CPTS is the largest and most demanding path (~344 hrs). Building web (CBBH) and defensive (CDSA) knowledge first gives you context that accelerates the 28-module journey.

**Key Topics Covered:**
- Networking fundamentals & service enumeration
- Footprinting and information gathering
- Vulnerability scanning (Nessus, Nmap NSE)
- Exploitation (Metasploit, manual exploitation)
- Password attacks & credential dumping
- Active Directory attacks (Kerberoasting, AS-REP Roasting, Pass-the-Hash, BloodHound)
- Lateral movement & pivoting
- Privilege escalation (Windows & Linux)
- Post-exploitation & persistence
- Professional pentest report writing

**Exam Format:**
- Complete the Penetration Tester job-role path (100%)
- **10-day** practical exam: compromise a simulated multi-host enterprise environment
- Must submit a full professional pentest report
- One free retake included

**Tips:**
- Use the "Attacking Enterprise Networks" capstone module as a full practice run
- Build a methodology checklist (recon → enum → exploit → post-exploit → report) and follow it on every practice machine
- Supplement with HTB Pro Labs: **Dante** (beginner) → **Zephyr** (intermediate) for realistic network practice
- Watch IppSec's HTB box walkthroughs for methodology insights, especially pivoting techniques
- Start your report template on Day 1 of the exam — don't wait until you have all flags

---

### 4. CWEE — Certified Web Exploitation Expert

**Why last?** CWEE is the most advanced certification and requires mastery of concepts introduced in CBBH. Attempting it last ensures you have the maturity and experience needed.

**Key Topics Covered:**
- Advanced SQL injection (second-order, OOB, time-based)
- Advanced XSS (DOM-based, mutation XSS, CSP bypasses)
- Server-side template injection (SSTI)
- HTTP request smuggling & desynchronisation
- OAuth 2.0 and JWT vulnerabilities
- GraphQL exploitation
- Advanced SSRF and XXE
- Source code review and white-box testing
- Prototype pollution and advanced JavaScript exploitation

**Exam Format:**
- Complete the Web Exploitation Expert path (100%)
- 7-day expert-level practical exam
- Both black-box and white-box exploitation required
- Must produce an expert-level vulnerability report

**Tips:**
- CWEE requires both offensive skills and secure code reading — spend time on every code snippet in the modules
- Keep a personal payload library organised by vulnerability class
- Revisit your CBBH notes before starting; they directly underpin CWEE content
- Budget extra time — advanced web bugs require patience and creativity

---

## Study Tips & Best Practices

### 1. Consistency Over Intensity
Study a little every day rather than cramming. Three focused 30-minute Pomodoro cycles (25 min work + 5 min break) add up to roughly 90 minutes of quality study — far more effective than sporadic multi-hour sessions.

### 2. Active Note-Taking
Use a structured notes tool like **Obsidian** or **CherryTree**:
- Create a vault per certification
- One note per technique/vulnerability
- Include: concept explanation, attack steps, payload examples, detection bypass notes

### 3. Lab First, Theory Second
Read each module section once to understand the concept, then immediately practice in the HTB lab. Return to the text when you get stuck. Do not just read — your hands must be on the keyboard.

### 4. Build a Personal Cheatsheet
After completing each module, summarise the key commands, payloads, and methodology steps into a personal cheatsheet. This becomes your exam companion.

### 5. Practise Report Writing Early
All HTB exams require a professional report. Start writing mini-reports during module skills assessments. Use the official HTB report templates and critique your own reports for clarity and completeness.

### 6. Leverage the Community
- Join the **HTB Discord** server — the `#academy` and `#certifications` channels have active discussion and hints
- Search the **HTB Forum** for hints on specific module sections when stuck (avoid full writeups)
- Follow HTB-focused content creators on YouTube and blogs for methodology insights

### 7. Track Your Progress
Use a simple spreadsheet or Notion board to track:
- Modules completed (%)
- Skills assessments passed/failed
- Weak areas to revisit
- Estimated exam readiness

---

## Recommended Tools & Resources

### Core Tools (install before starting)

| Tool | Purpose |
|------|---------|
| **Kali Linux / Parrot OS** | Primary attack operating system |
| **Burp Suite Community** | Web proxy and web testing |
| **Nmap** | Port scanning and service enumeration |
| **Metasploit Framework** | Exploitation framework |
| **BloodHound + SharpHound** | Active Directory attack graphing |
| **Impacket** | Python tools for network protocols |
| **Obsidian / CherryTree** | Note-taking |
| **tmux** | Terminal multiplexer for efficient workflow |

### External Learning Resources

| Resource | Use Case |
|----------|---------|
| [IppSec YouTube Channel](https://www.youtube.com/c/ippsec) | HTB box walkthroughs, methodology insight |
| [PortSwigger Web Security Academy](https://portswigger.net/web-security) | Free supplement for CBBH/CWEE web topics |
| [TryHackMe](https://tryhackme.com) | Guided beginner rooms if prerequisites feel shaky |
| [HackTricks](https://book.hacktricks.xyz) | Technique reference wiki |
| [PayloadsAllTheThings](https://github.com/swisskyrepo/PayloadsAllTheThings) | Payload and bypass cheatsheets |
| [LOLBAS / GTFOBins](https://lolbas-project.github.io) | Living-off-the-land binaries for post-exploitation |
| [VulnHub / HTB Free Tier](https://www.vulnhub.com) | Extra practice machines |

---

## Exam Strategy

### Before the Exam
- [ ] Complete **100%** of all required path modules (mandatory unlock condition)
- [ ] Re-read your personal cheatsheets and notes
- [ ] Set up your attack environment and test your VPN connection
- [ ] Prepare your report template (title page, executive summary, findings table, appendix)
- [ ] Get a full night's sleep before Day 1

### During the Exam
- [ ] Start with full enumeration before attempting any exploits
- [ ] Document **everything** as you go — screenshots, commands, output — you will need them for the report
- [ ] Take breaks every 2–3 hours; fatigue causes missed details
- [ ] If stuck on one target for more than 2 hours, move on and return later with fresh eyes
- [ ] Maintain your methodology checklist; don't skip steps under time pressure

### Report Writing
- [ ] Use the official HTB report template
- [ ] Write findings in order of severity (Critical → High → Medium → Low → Informational)
- [ ] For each finding, include: Description, Severity, Affected Host/URL, Steps to Reproduce, Evidence (screenshots), Remediation Recommendation
- [ ] Proof-read for grammar and clarity — the report is as important as the technical findings
- [ ] Submit with time to spare; last-minute submissions risk technical issues

---

## Frequently Asked Questions

**Q: Do I need to do the certifications in this order?**
A: The order CBBH → CDSA → CPTS → CWEE is strongly recommended. CBBH builds the web foundation for CWEE, and CDSA gives you blue-team context that makes CPTS more meaningful. That said, CBBH and CDSA can be swapped if you prefer a blue-team start.

**Q: How much does it cost?**
A: HTB Academy uses a subscription model (Student, Individual, or Enterprise). Check [academy.hackthebox.com](https://academy.hackthebox.com) for current pricing. Each certification exam voucher is purchased separately. Budget approximately $300–$500 per certification (subscription + exam voucher), though student discounts and bundles are available.

**Q: What if I fail an exam?**
A: Every HTB certification includes **one free retake**. Use the retake strategically — review your weak areas thoroughly before attempting again. Additional retake vouchers can be purchased.

**Q: Is prior experience required?**
A: No formal experience is required, but comfort with Linux, networking, and basic scripting will significantly reduce your study time. Complete the prerequisites listed above before starting the first certification path.

**Q: How are the exams graded?**
A: Exams are graded on a combination of flags captured (proof of exploitation) and the quality of your submitted report. Both components matter — a technically sound report can compensate for a difficult flag, and vice versa.

**Q: Can I work on HTB machines on the main platform simultaneously?**
A: Yes, and it is encouraged! Practising on live HTB boxes (especially those tagged with skills relevant to your current path) builds the intuition and speed needed for exam conditions.

---

## Summary

| Step | Action |
|------|--------|
| 1 | Subscribe to HTB Academy and enrol in the Bug Bounty Hunter path |
| 2 | Complete all CBBH modules → earn **CBBH** |
| 3 | Enrol in SOC Analyst path → complete all modules → earn **CDSA** |
| 4 | Enrol in Penetration Tester path → complete all 28 modules → earn **CPTS** |
| 5 | Enrol in Web Exploitation Expert path → complete all modules → earn **CWEE** |
| 6 | 🎉 All four HTB certifications — in under one year |

---

*Good luck on your journey. The path is challenging by design — every struggle with a lab or exam scenario is building the real-world skill that makes these certifications worth having.*

*For the latest module lists, pricing, and exam requirements always refer to the official [HTB Academy Certifications page](https://academy.hackthebox.com/preview/certifications).*
