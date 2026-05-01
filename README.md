# Vulnerability Assessment Report – Task 01

## Internship
Future Interns – Cyber Security Internship

---

## Objective

To perform a read-only vulnerability assessment on authorized and public web assets using ethical security testing practices.

---

## Scope

### Primary Target
- samihzs.in *(Authorized personal asset)*

### Validation Targets
- testphp.vulnweb.com *(Security testing environment)*
- demo.testfire.net *(Security testing environment)*

---

## Tools Used

- Kali Linux
- Nmap
- Browser Developer Tools
- SecurityHeaders.com
- Curl

---

## Methodology

### 1. Network Reconnaissance
Identified exposed ports and services using Nmap.

### 2. Header Analysis
Inspected HTTP response headers using browser developer tools.

### 3. Security Header Validation
Checked missing security controls using SecurityHeaders.com.

### 4. Transport Security Validation
Verified HTTP to HTTPS behavior using Curl.

---

## Key Findings

| Finding | Risk |
|---------|------|
| Missing Content-Security-Policy | Medium |
| Missing X-Frame-Options | Medium |
| Missing X-Content-Type-Options | Medium |
| Missing Referrer Policy | Low |
| Missing Permissions Policy | Low |
| Missing HTTP → HTTPS Redirect | High |

---

## Repository Structure

```bash
evidence/
notes/
report/
```

---

## Ethical Scope

This assessment was conducted under:

✅ Passive analysis  
✅ Read-only testing  
✅ No exploitation  
✅ No service disruption  

Aligned with internship ethical guidelines.

---

## Disclaimer

This project was performed for educational and professional skill development under the Future Interns Cyber Security Internship Program.
