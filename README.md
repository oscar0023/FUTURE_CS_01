# 🔐 Vulnerability Assessment Report

**Target:** testphp.vulnweb.com
**Assessment Period:** February 16–21, 2026
**Author:** Oscar Alotchéwou ALIDJINOU

---

## 📌 Overview

This repository contains a **Vulnerability Assessment Report** conducted against the intentionally vulnerable web application:

🔗 [http://testphp.vulnweb.com](http://testphp.vulnweb.com)

The objective of this assessment was to identify security weaknesses, misconfigurations, and potential exposure points through **passive testing and configuration analysis only**.

No exploitation, brute force, DoS, or unauthorized access attempts were performed.

This assessment was conducted in a legal and ethical context, using a publicly available vulnerable test environment.

---

## 🎯 Scope of Assessment

The assessment focused on:

* Passive vulnerability scanning
* HTTP header analysis
* Service enumeration
* Configuration review
* Exposure of sensitive paths

---

## 🛠 Tools Used

* **Nmap** – Port scanning & service enumeration
* **OWASP ZAP** – Passive vulnerability scanning
* Browser DevTools – HTTP request & header analysis

---

## 📊 Risk Classification Summary

| Risk Level       | Count |
| ---------------- | ----- |
| 🔴 High          | 4     |
| 🟠 Medium        | 2     |
| 🟡 Low           | 4     |
| 🔵 Informational | 3     |

---

## 🚨 High Risk Findings

1. **HTTP Protocol Used Instead of HTTPS**
   Data transmitted in clear text, vulnerable to interception.

2. **Exposed Credentials**
   Credentials visible within the application.

3. **Very Weak Password Policy**
   Short and predictable password ("test").

4. **Sensitive Paths Exposed**

   * `/admin/`
   * `/CVS/`
     Direct access to sensitive resources without access control.

---

## ⚠️ Medium Risk Findings

5. **Content Security Policy (CSP) Header Not Set**
6. **Missing Anti-Clickjacking Header**

---

## 🟡 Low Risk Findings

7. Server Banner Information Disclosure
8. `X-Powered-By` Header Disclosure
9. `Server` Header Version Disclosure
10. Missing `X-Content-Type-Options` Header

---

## 🔵 Informational Findings

11. Authentication Request Identified
12. Charset Mismatch
13. Potential User-Controlled HTML Attribute (XSS Hotspot)

---

## 🧠 Key Security Issues Identified

* Lack of encryption (no HTTPS)
* Weak authentication controls
* Sensitive directory exposure
* Information leakage via HTTP headers
* Missing modern browser security protections

---

## 🛡 Recommended Remediation Actions

* Enforce HTTPS (TLS encryption)
* Remove exposed credentials from client-side code
* Implement strong password policy
* Restrict access to sensitive directories
* Configure secure HTTP headers:

  * Content-Security-Policy
  * X-Frame-Options
  * X-Content-Type-Options
* Suppress server version disclosure headers

---

## 📄 Report

The full vulnerability assessment report is available in this repository as a PDF document.

---

## ⚖️ Ethical Notice

This assessment was conducted:

* On an intentionally vulnerable public test application
* For educational and academic purposes
* Without exploitation of identified vulnerabilities

---

## 👤 Author

Oscar Alotchéwou ALIDJINOU
📧 [oscaralidjinou27@gmail.com](mailto:oscaralidjinou27@gmail.com)
