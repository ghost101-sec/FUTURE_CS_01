# FUTURE_CS_01: Vulnerability Assessment Report

**Internship:** Future Interns, Cyber Security Track
**Task:** 1, Vulnerability Assessment Report for a Live Website
**Author:** Edwin Baiju

## Overview
This project is a vulnerability assessment of a web application. It identifies common web weaknesses, classifies each as Low, Medium or High risk, explains them in simple business language, and gives clear fixes.

## Target
OWASP Juice Shop, a deliberately vulnerable practice application, running locally on my own machine (`http://localhost:3000`). No third-party system was tested.

## What's Inside
- `Vulnerability_Assessment_Report.pdf`: the full designed report (made in Canva)
- `zap_report.html`: the OWASP ZAP scan report
- `nmap_scan.txt`: Nmap scan output
- `zap_alerts.png`, `zap_alert_detail.png`, `nmap_scan.png`, `curl_headers.png`: evidence screenshots

## Summary of Findings
| Risk | Count |
|---|---|
| High | 0 |
| Medium | 4 |
| Low | 3 |
| Informational | 3 |

**Overall risk rating: Medium**

## Key Findings
- Content Security Policy (CSP) header not set
- Cross-domain misconfiguration (`Access-Control-Allow-Origin: *`)
- Missing anti-clickjacking header
- Session ID in URL
- Application served over plain HTTP, with no HSTS header

## Tools Used
Nmap, OWASP ZAP (passive scan), curl, browser DevTools, Kali Linux, Canva (report design)

## Method
1. Scanned the target with Nmap to find open ports and services
2. Checked security headers using curl
3. Explored the application through ZAP and reviewed the alerts
4. Classified each finding by risk and wrote plain-language fixes

## Limitations
Only passive checks were used and no attacks were launched, so deeper flaws may exist that this review did not find.

## Key Learning
Most web weaknesses found were missing security headers and information leaks, which can be fixed quickly with server configuration.
