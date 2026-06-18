# Vulnerability Assessment Report
### Task 1 – Reconnaissance & Vulnerability Scanning
**Author**: Arathi Shekhar Munavalli
**Internship:** Alfido Tech
**Date:** 02 April 2026

## Overview
As part of this task, a reconnaissance and vulnerability scanning activity was carried out on a publicly available test server. The aim was to understand how real-world systems are analyzed for security weaknesses using standard tools.

The target used for this assessment is officially provided for safe practice.

- **Target:** scanme.nmap.org
- **IP Address:** 45.33.32.156
- **Platform:** Ubuntu Linux

---

## Tools Utilized
The following tools were used during the assessment:

- **Nmap** – for identifying open ports and services
- **Nikto** – for detecting web server vulnerabilities

---

## Approach Followed
The task was completed in three stages:

1. **Service Discovery**
   Nmap was used to scan the target and detect active ports along with running services.

2. **Web Server Analysis**
   Nikto was used to check for possible misconfigurations and known issues in the web server.

3. **Result Analysis**
   The findings were reviewed and categorized based on severity.

---

## Key Findings

### Open Ports & Services
- Port 22 – SSH service detected
- Port 80 – Web server (Apache) running
- Additional ports (9929, 31337) were also open but less critical

---

### Identified Issues
The scan revealed several security concerns:

- The Apache web server version is outdated
- Important security headers are not configured
- Directory listing is enabled, exposing internal files
- Some default server files are accessible
- Unnecessary HTTP methods are allowed

---

## Risk Evaluation
- **High Risk:** Outdated Apache version
- **Medium Risk:** Missing headers and configuration issues
- **Low Risk:** Minor exposure and default settings

---

## Recommendations
Based on the findings, the following steps are suggested:

- Update Apache to the latest stable version
- Configure essential security headers
- Disable directory indexing
- Remove default or unnecessary files
- Restrict HTTP methods to only required ones
- Update older services like SSH

---

## Files in this Repository

| File | Description |
|------|-------------|
| `Task1_Explanation.pdf` | Full vulnerability assessment report |
| `nmap_results.txt` | Raw Nmap scan output |
| `nikto_results.txt` | Raw Nikto scan output |
| `Final_report.txt` | Summary of all findings |

---

## Conclusion
This exercise highlights how even a basic scan can reveal multiple vulnerabilities in a system. While the target used here is meant for testing, similar issues in real environments could lead to serious security risks.

Regular scanning and proper configuration are essential to maintain system security.

---

## Disclaimer
This assessment was performed only on an authorized test server (scanme.nmap.org) for learning purposes as part of the Alfido Tech Cybersecurity Internship program.
