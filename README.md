# FUTURE_CS_01
Cyber Security Internship – Task 1: Vulnerability Assessment Report using Nmap, OWASP ZAP, and Browser Dev Tools.”

# Cyber Security Task 1 (2026) - Vulnerability Assessment Report

## 🔍 Website Tested
- Target: http://demo.testfire.net
- Scope: Public-facing pages only (read-only analysis)

## 🛠 Tools Used
- **Nmap** → Port & service exposure
- **OWASP ZAP (Passive Scan)** → Header & cookie analysis
- **Browser DevTools** → Manual inspection

## 📂 Evidence
- Nmap Scan Output → [`nmap_results.txt`](nmap_results.txt)
- ZAP Passive Scan Report → [`zap_report.html`](zap_report.html)

### Screenshots
- ![Nmap Scan](screenshots/nmap_scan.png)
- ![ZAP Alerts](screenshots/zap_alerts.png)
- ![ZAP Sites Tree](screenshots/zap_sites_tree.png)
- ![ZAP History](screenshots/zap_history.png)

## 📑 Reports
- Final Vulnerability Assessment Report → `Vulnerability_Assessment_Report.pdf`

## ✅ Summary
This assessment identified:
- Open ports and outdated Apache Tomcat services
- Missing security headers (CSP, HSTS, X-Frame-Options)
- Insecure cookies (missing HttpOnly/Secure flags)
- Exposed Swagger API documentation

### Risk Classification
- **High:** Outdated components, missing CSP, insecure cookies  
- **Medium:** Missing HSTS, clickjacking risk, server banner disclosure, exposed API docs  
- **Low:** HTML comments, hidden form fields  
- **Informational:** Mixed content  

### Recommendations
- Upgrade Tomcat and hide server banners  
- Implement CSP, HSTS, and X-Frame-Options headers  
- Secure cookies with HttpOnly and Secure flags  
- Restrict access to API documentation  
- Remove unnecessary comments and validate hidden fields
