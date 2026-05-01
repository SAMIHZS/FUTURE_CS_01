# Analyst Notes – Vulnerability Assessment

## Target
samihzs.in

## Environment
Authorized personal asset hosted on GitHub Pages.

---

## Observation 1 – Open Web Ports

### Evidence
Nmap scan identified:

- Port 80 (HTTP)
- Port 443 (HTTPS)

### Risk
Low

### Analysis
The website exposes standard web ports. HTTPS is enabled, which is positive.

---

## Observation 2 – Missing Security Headers

### Evidence
SecurityHeaders.com scan returned grade: F

Missing headers:

- Content-Security-Policy
- X-Frame-Options
- X-Content-Type-Options
- Referrer-Policy
- Permissions-Policy

### Risk
Medium

### Analysis
Missing browser security headers may increase exposure to browser-based attacks such as XSS, clickjacking, and content sniffing.

---

## Observation 3 – HTTP Not Redirecting to HTTPS

### Evidence
Curl validation returned:

HTTP/1.1 200 OK

### Risk
High

### Analysis
Users accessing the HTTP version are not automatically redirected to HTTPS, potentially exposing traffic to interception risks.

---

## Hosting Consideration

The website appears to be hosted on GitHub Pages. Some security header configurations may be restricted by hosting architecture.
