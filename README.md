# Networkwalks-WK2-Footprinting-Scanning

Hands-on domain footprinting, DNS enumeration, subnet scanning, ARP inspection, and network topology mapping for the Networkwalks Week 2 cybersecurity internship.

# PENETRATION TESTING & NETWORK SCANNING REPORT

## Description & Overview

This report documents the practical security analysis completed during Week 2 (`W2-PM1` and `W2-PM5`) under the Networkwalks Cybersecurity Internship Program.

The primary objective was to perform domain reconnaissance, gather publicly available infrastructure information, discover active hosts on an authorized local network, analyze network information, and visualize network topology.

All activities were performed within the authorized testing scope for educational and cybersecurity training purposes.

---

## 1. Document Metadata & Scope

- **Pentester Name:** Tanvi Gavatre
- **Program:** Networkwalks Cybersecurity Internship
- **Date:** November 11, 2026
- **Modules Completed:** `W2-PM1` (Multiple Kali Tools), `W2-PM5` (Zenmap Subnet Scanning)
- **Target Environments:**
  1. `networkwalks.com`(Secured written permission)
  2. Local Subnet
- **Permission Status:** Authorized Educational Testing
- **Phases Covered:** Phase 1 (Reconnaissance & Footprinting), Phase 2 (Scanning & Network Discovery)

---

## 2. Executive Summary & Liability Disclaimer

This report covers the execution of Week 2 tasks (`W2-PM1` and `W2-PM5`) under the Networkwalks Cybersecurity Internship Program.

The activities focused on domain reconnaissance, DNS enumeration, web technology identification, Web Application Firewall detection, local network host discovery, ARP inspection, and network topology visualization.

All activities were conducted within the authorized testing boundaries. The findings are documented for educational and cybersecurity learning purposes.

---

## 3. Technical Activities & Findings

### 3.1 Domain Reconnaissance & Footprinting (Task W2-PM1)

**Target Domain:** `networkwalks.com` / `www.networkwalks.com`

- **WHOIS & DNSRecon Enumeration:** Collected domain registration information and identified 16 DNS records, including A, NS, MX, TXT, and SRV records.
- **WhatWeb Fingerprinting:** Identified web technologies, including Apache, WordPress `7.1.4`, Bootstrap `7.1.4`, and jQuery `3.7.1`.
- **WAF Inspection (`wafw00f`):** Detected ModSecurity (SpiderLabs), indicating the presence of a Web Application Firewall.
- **DNS Resolution (`nslookup`):** Successfully resolved the target domain through DNS lookup.
- **HTTP Header Analysis (`curl -I`):** Observed HTTP-to-HTTPS redirection and a successful HTTP/2 `200 OK` response. Examined server and response headers.

### 3.2 Subnet Discovery & Topology Mapping (Task W2-PM5)

**Target Network:** Authorized Local Lab Network

- Executed Nmap host discovery (`-sn`) across the authorized lab subnet.
- Scanned 256 addresses and identified two active hosts.
- Used Zenmap GUI to perform network discovery and examine scan results.
- Examined the local ARP table using `arp -a`.
- Visualized discovered hosts using Zenmap's interactive topology graph.
- Captured screenshots of network discovery results and topology visualization as practical evidence.

---

## 4. Risk Analysis & Threat Impact

- **Domain Information Exposure:** Publicly available domain registration and DNS information can help attackers understand an organization's external infrastructure.
- **Technology Fingerprinting:** Identifying web technologies and software versions may help attackers search for known vulnerabilities.
- **WAF Identification:** Identifying security technologies can provide information about the target's defensive mechanisms.
- **Network Host Discovery:** Identifying active devices can help an attacker understand the structure of a network after gaining authorized network visibility.

These observations represent potential security risks and do not confirm that any vulnerability was successfully exploited.

---

## 5. Security Recommendations

1. Regularly review domain registration information and DNS configurations.
2. Keep web server software, CMS platforms, and associated libraries updated.
3. Maintain and properly configure Web Application Firewall protection.
4. Enforce HTTPS and review HTTP security headers.
5. Regularly monitor active devices within local networks.
6. Disable unnecessary network services and restrict unauthorized access.

---

## 6. Conclusion

The Week 2 practical activities provided hands-on experience in domain reconnaissance, DNS enumeration, web technology fingerprinting, WAF detection, HTTP header analysis, and network scanning.

WHOIS, DNSRecon, WhatWeb, Nslookup, cURL, and WAFW00F helped gather information about the target domain, while Nmap and Zenmap were used for local network discovery and topology visualization.

These exercises strengthened practical knowledge of cybersecurity reconnaissance, network discovery, security analysis, and technical documentation.

---

## 7. Tools & Command Reference

The following tools and commands were used during the security assessment:

| Command / Tool | Technical Purpose |
|---|---|
| `whois networkwalks.com` | Retrieves domain registration information and registrar details. |
| `dnsrecon -d networkwalks.com` | Enumerates DNS records and domain infrastructure information. |
| `nslookup networkwalks.com` | Performs DNS resolution for the target domain. |
| `whatweb https://networkwalks.com` | Identifies web server technologies and application frameworks. |
| `wafw00f https://networkwalks.com` | Detects Web Application Firewall technologies. |
| `curl -I https://networkwalks.com` | Examines HTTP response headers and server information. |
| `ipconfig /all` | Displays local network configuration on Windows. |
| `nmap -sn <authorized-lab-subnet>` | Performs host discovery across an authorized network range. |
| `arp -a` | Displays locally available ARP table entries. |
| **Zenmap** | Provides a graphical interface for network scanning and topology visualization. |

---

## 8. Evidences Collected

The following screenshots were captured during the practical activities:

- WHOIS domain lookup results.
- DNSRecon enumeration results.
- WhatWeb technology fingerprinting results.
- WAFW00F detection results.
- Nslookup DNS resolution results.
- cURL HTTP response header analysis.
- Nmap host discovery results.
- Zenmap network scanning results.
- Zenmap network topology visualization.

Sensitive network identifiers and confidential technical details have been excluded from the publicly shared evidence.

---

### Author & Reference Information

- **Author:** Tanvi Gavatre
- **Program:** Networkwalks Cybersecurity Internship
- **LinkedIn Profile:** [(https://www.linkedin.com/in/tanvi-gawatre/)]




