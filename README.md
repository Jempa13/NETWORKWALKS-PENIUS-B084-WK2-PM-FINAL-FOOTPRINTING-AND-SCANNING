# NETWORKWALKS-PENIUS-B084-WK2-PM-FINAL-FOOTPRINTING-AND-SCANNING
# 🛡️ Penetration Testing Report: Footprinting & Network Scanning Phases
**W2-PM-FINAL | Cybersecurity & Ethical Hacking Internship | Networkwalks (Batch B084)**

![Program](https://img.shields.io/badge/Program-Networkwalks_Cybersecurity-blue)
![Batch](https://img.shields.io/badge/Batch-B084-informational)
![Module](https://img.shields.io/badge/Module-W2--PM--FINAL-success)
![Tools](https://img.shields.io/badge/Tools-Kali_Linux_|_Zenmap_|_Nmap-critical)

---

## 📋 Engagement & Project Metadata

| Field | Details |
| :--- | :--- |
| **Cybersecurity Professional** | Penius Jempa |
| **Program / Batch** | B084 — Networkwalks |
| **Date** | 12 November 2026 |
| **Modules Completed** | `W2-PM1` (Multiple Kali Tools) & `W2-PM5` (Zenmap Scanning) |
| **Client / Target Scope** | 1. `networkwalks.com` (Explicit written permission secured)<br>2. Local Area Network (`10.126.200.0/24` / Personal Lab LAN) |
| **Authorization Status** | ✅ Verified Written Permission Secured |
| **Phases Covered** | **Phase 1:** Reconnaissance & Footprinting<br>**Phase 2:** Scanning & Network Discovery<br>**Phases 3–5:** In Progress |

---

## ⚠️ 1. Liability & Legal Disclaimer

> **Strict Educational & Authorized Use Only:**  
> All reconnaissance and network scanning activities documented in this repository were performed strictly on systems where explicit written permission was obtained (`networkwalks.com`) or on personally owned local network hardware.  
> 
> These materials are published solely for educational and defensive research purposes. Unauthorized scanning, footprinting, or exploitation of systems without prior written consent is illegal in most jurisdictions and can result in criminal prosecution, fines, and permanent professional consequences. Neither the author nor Networkwalks assumes liability for misuse of this information.

---

## 📖 2. Overview & Objectives

This repository documents Week 2 of the **Networkwalks Cybersecurity & Ethical Hacking Internship**, bridging **Phase 1 (Footprinting & Reconnaissance)** and **Phase 2 (Scanning & Network Discovery)**:

1. **External Domain Footprinting (`W2-PM1`):** Gathering publicly exposed infrastructure, DNS, web stack, and WAF metadata for `networkwalks.com` using six command-line reconnaissance tools in **Kali Linux**.
2. **Internal Network Discovery (`W2-PM5`):** Identifying active hosts, IP/MAC mappings, and generating a visual network topology on a local LAN using **Zenmap (Nmap GUI)** and **Windows CMD**.

---

## 🛠️ 3. Tools & Environment

| Tool / Platform | Environment | Purpose |
| :--- | :--- | :--- |
| **Kali Linux & Windows** | OS / Lab | Host environments for external recon and internal scanning |
| **`whois`** | Kali Linux | Query domain registration records, registrar details, and name servers |
| **`whatweb`** | Kali Linux | Fingerprint web server software, CMS versions, plugins, and frameworks |
| **`nslookup`** | Kali Linux | Resolve target domain names to IPv4 addresses via DNS |
| **`curl -I`** | Kali Linux | Inspect raw HTTP response headers and exposed API endpoints |
| **`wafw00f`** | Kali Linux | Detect and fingerprint Web Application Firewalls (WAF) |
| **`dnsrecon`** | Kali Linux | Enumerate DNS records (`NS`, `MX`, `SPF`, `TXT`, `SRV`) |
| **Zenmap (Nmap GUI)** | Windows | Perform subnet ping sweeps, host discovery, and export network topology |
| **Windows CMD (`ipconfig`)** | Windows | Identify local interface IPv4 configuration, subnet mask, and MAC address |

---

## 🔍 4. Activities & Technical Findings

### 4.1 Phase 1: Footprinting & Reconnaissance (`networkwalks.com`)

Six passive and active reconnaissance utilities were executed from Kali Linux against `networkwalks.com`:

```bash
# 1. Domain Registration & Name Servers
whois networkwalks.com

# 2. Web Technology & CMS Fingerprinting
whatweb networkwalks.com

# 3. DNS Name-to-IP Resolution
nslookup networkwalks.com

# 4. HTTP Header & Endpoint Inspection
curl -I [https://networkwalks.com](https://networkwalks.com)

# 5. Web Application Firewall (WAF) Detection
wafw00f networkwalks.com

# 6. Comprehensive DNS Record Enumeration
dnsrecon -d networkwalks.com
