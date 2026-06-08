# 🌐 Week 02 — Network Scanning & Enumeration

**Intern:** Ali Ahsan | **Roll No:** CSI-B1-427
**Program:** Cyberstar Cybersecurity Red Teaming Internship
**Instructor:** Umar Niaz
**Date:** 11 March 2026
**Target Domain:** hackthissite.org

---

## 📌 Overview

This week focused on **active network scanning** using Nmap to identify open ports, running services, and software versions. Advanced techniques including NSE scripting and firewall evasion were also explored.

---

## 🧪 Tasks Covered

### Task 01 — Advanced Network Scanning with Nmap

| Scan Type | Command | Result |
|-----------|---------|--------|
| TCP Connect (-sT) | `nmap -sT -p 1-1000` | Ports 80, 443 open — Duration: 16.84s |
| SYN Stealth (-sS) | `sudo nmap -sS -p 1-1000` | Ports 22, 80, 443 — Duration: 22.92s |
| UDP Scan | `sudo nmap -sU --top-ports 100` | Duration: 5.72s |
| Timing T2 vs T4 | `-T2` slow/stealth vs `-T4` fast | T4: 3.49s — T2: 93.68s |

### Task 02 — Service Fingerprinting & Banner Grabbing
- **Nmap -sV** — service version detection
- **Aggressive Scan (-A)** — OS detection, scripts, traceroute
- **Manual Banner Grabbing** — Netcat and Telnet methods
- **Enum4linux** — SMB enumeration on Port 445

### Task 03 — Nmap Scripting Engine (NSE)
- `http-enum` — hidden web directories and admin panels
- `discovery` and `safe` script categories
- `ssl-cert` — SSL certificate details on Port 443
- `vuln` scripts — mapped results to CVE IDs via NVD and MITRE

### Task 04 — Stealth & Firewall Evasion
- **Packet Fragmentation (-f)** — splits packets to bypass simple filters
- **MTU Manipulation (--mtu 16)** — forces extremely small packet sizes
- **Decoy Scanning (-D RND:10)** — hides real scanner behind fake IPs
- **Source Port Manipulation (--source-port 53)** — mimics DNS traffic

---

## 📊 Timing Comparison

| Speed | Template | Time Taken | Open Ports Found |
|-------|----------|------------|-----------------|
| Slow | -T2 | 93.68 sec | 22, 80 |
| Normal | -T3 | 10.52 sec | 22, 80, 443 |
| Fast | -T4 | 3.49 sec | 80 |

---

## 🛠️ Tools Used

`Nmap` · `Netcat` · `Telnet` · `Enum4linux`

---

## ⚠️ Disclaimer

> Performed in an **authorized lab environment** for educational purposes only.
