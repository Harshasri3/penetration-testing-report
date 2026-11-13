# 🛡️ Penetration Testing Report: Footprinting & Network Scanning

**W2-PM-FINAL | Cybersecurity | Networkwalks**

This repository documents my Week 2 project activities in footprinting, reconnaissance, OSINT and network scanning. It follows the reference repository's simple layout: a README, the formal report and a screenshots.

---

## 📋 Report Overview

| Field | Detail |
|---|---|
| Author | Pogula Harsha Sri |
| Program | Cybersecurity & Ethical Hacking – Networkwalks |
| Date | 12 November 2026 |
| Modules | W2-PM1, W2-PM2, W2-PM3, W2-PM4, W2-PM5 |
| Phases | Reconnaissance & Footprinting; Scanning & Network Discovery |

## 🎯 Scope of Activities

| Activity | Target / Scope | Tools / Method |
|---|---|---|
| W2-PM1 Footprinting | `networkwalks.com` | WHOIS, WhatWeb, Nslookup, cURL, WAFW00F, DNSRecon |
| W2-PM2 GHDB | GHDB / search-engine results | Google dorks and review of indexed information |
| W2-PM3 Maltego | `networkwalks.com` | Domain entity and authorized OSINT relationship mapping |
| W2-PM4 theHarvester | `microsoft.com` | Passive collection of public email addresses and subdomains |
| W2-PM5 Zenmap | Own LAN | Ping Scan and host discovery |

> **Authorization:** Public indexing does not authorize access to private camera feeds, credentials, accounts or sensitive systems. Perform all activities only within the approved lab scope. The local network scan below was performed on my own LAN.

## 🗺️ The 5 Phases of a Penetration Test

| # | Phase | Status |
|---|---|---|
| 1 | Reconnaissance & Footprinting | Covered in PM1–PM4 |
| 2 | Scanning & Enumeration | Covered in PM5 |
| 3 | Gaining Access | Not part of this project |
| 4 | Maintaining Access | Not part of this project |
| 5 | Covering Tracks & Reporting | Reporting/documentation practiced |

## 🧰 Tools Used

| Tool | Purpose |
|---|---|
| WHOIS | Domain registration and name-server information |
| WhatWeb | Web technology fingerprinting |
| Nslookup | DNS name resolution |
| cURL | HTTP response-header inspection |
| WAFW00F | WAF detection |
| DNSRecon | DNS record enumeration |
| GHDB / Google Dorks | Search-engine reconnaissance |
| Maltego | Visual OSINT and entity relationship mapping |
| theHarvester | Public email and subdomain collection |
| Zenmap / Nmap | Host discovery and network scanning |

---

# 🔍 Phase 1: Footprinting & Reconnaissance

## 1. W2-PM1 – Footprinting with Multiple Kali Linux Tools

**Target:** `networkwalks.com`

```bash
whois networkwalks.com
whatweb networkwalks.com
nslookup networkwalks.com
curl -I https://networkwalks.com
wafw00f networkwalks.com
dnsrecon -d networkwalks.com
```

The module uses six tools to inspect domain registration, web technologies, DNS resolution, HTTP headers, WAF presence and DNS records.

![WHOIS Output](screenshots/whois.png)
![alt text](screenshots/whatweb.png)
![alt text](screenshots/nslookup.png)
![alt text](screenshots/curl.png)
![alt text](screenshots/wafw00f.png)
![alt text](screenshots/dnsrecon.png)

## 2. W2-PM2 – GHDB-Based Footprinting

This module introduces the Google Hacking Database and search operators (Google dorks). The tasks cover search patterns related to indexed security-camera results and public mathematics e-book PDF listings.

**Responsible handling:** Do not access or publish private camera feeds, credentials or sensitive systems. Use instructor-provided training targets or safe, non-sensitive authorized examples.


## 3. W2-PM3 – Footprinting with Maltego

The module covers installing Maltego on Windows and using it to identify email addresses related to `networkwalks.com` within the lab's authorized scope.

**Findings:** 
![maltego](screenshots/maltego.png)

## 4. W2-PM4 – Footprinting with theHarvester

**Target:** `microsoft.com`

The module specifies two runs:

```bash
theHarvester -d microsoft.com -b baidu -l 1000
theHarvester -d microsoft.com -b all -l 50
```

Check `theHarvester -h` because source names and options may vary by installed version. Record the source, limit, emails, subdomains, counts and any errors. Remove API keys before publishing.

![theHarvester](screenshots/theHarvester.png)

---

# 📡 Phase 2: Scanning with Zenmap

## 5. W2-PM5 – Host Discovery with Zenmap

### Objective

To understand network scanning and identify active hosts on a network using Zenmap (Nmap GUI).

### What I Learned

- Learned how to identify network configuration details using the Windows `ipconfig` command.
- Understood IP addresses, subnet masks, LAN subnets, and default gateways.
- Learned how to use Zenmap's **Ping Scan** profile to discover active hosts on a network.
- Understood how Nmap identifies live hosts and displays scan results.
- Learned how to identify IP addresses, MAC addresses, and vendor information from scan results.
- Explored Zenmap's **Topology** feature to visualize discovered hosts and their relationships within a network.
- Learned how to save scan results and network topology for documentation and analysis.
- Understood the importance of network discovery in identifying devices connected to a network.

### Tools Used

- Zenmap (Nmap GUI)
- Nmap
- Windows Command Prompt (`ipconfig`)

### Key Takeaways

This practical helped me understand the basics of network discovery, host identification, and network topology visualization. I also learned how network scanning can assist security professionals in understanding network infrastructure and identifying active devices.


---

## ⚖️ Risk Analysis

| Finding | Evidence | Potential impact |
|---|---|---|
| Public web technology information | PM1 outputs | Helps build a target profile; versions require validation |
| Publicly indexed information | PM2 results | May reveal unintended exposure; verify only within authorized scope |
| Domain-related entities | PM3 graph | Helps organize public information |
| Public emails and subdomains | PM4 output | Expands an organization's public footprint |
| Multiple live LAN hosts | PM5 Ping Scan | Unknown devices should be identified by the network owner |

These are observations, not confirmed vulnerabilities. No exploitation or vulnerability validation is claimed.

## ✅ Recommendations

- Review public-facing technology information and keep software updated.
- Review DNS records and HTTP response headers periodically.
- Keep OSINT collection within the approved scope.
- Never access or publish private camera feeds, credentials or sensitive data.
- Verify devices discovered on the local network.
- Maintain an updated inventory of authorized devices.
- Save scan outputs and network topology evidence.
- Remove credentials, tokens and personal account details from screenshots.

## 💡 What I Learned

- Each footprinting tool reveals a different part of a domain's public information.
- Search operators can locate information indexed by search engines.
- Maltego helps visualize relationships between entities.
- theHarvester collects public email and subdomain information.
- Zenmap simplifies host discovery and scan-result review.
- A finding is not automatically a vulnerability; observations need validation.
- Authorization and scope are essential before reconnaissance or scanning.


## 👤 Author

**Harsha Sri**  
Cybersecurity & Ethical Hacking – Networkwalks

*Educational project documentation. Perform security testing only with appropriate authorization.*
