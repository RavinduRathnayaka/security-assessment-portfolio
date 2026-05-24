# Security Assessments & Penetration Testing Portfolio

This repository contains sanitized and redacted assessment reports detailing professional security audits, penetration testing engagements, and red teaming exercises. These documents highlight systematic approaches to vulnerability discovery, risk classification, and remediation strategy across diverse application architectures and infrastructures.

## Portfolio Directory

| Report Filename | Assessment Type | Focus Areas / Technical Scope | Key Vulnerabilities Identified |
| :--- | :--- | :--- | :--- |
| `Redacted Penetration testing and Red Teaming Assessment Report.pdf` | Red Teaming (Phase 1) | Social Engineering, Public-Facing Portals, Exposed Network Services, Unified Kill Chain | Phishing Execution, Insecure Password Management, WordPress Username Enumeration, ADSS Portal Info Leakage |
| `Redacted Vulnerability Assessment Report.pdf` | Web Application & API Penetration Test | Frontend Prototype Exploitation, Server-side Dependency Analysis, API Security Auditing | Prototype Pollution, Lodash Command Injection, Stored/Reflected XSS, Excessive API Request Rate |
| `Redacted Basic Vulnerability Assessment Report.pdf` | Web Application Security Review | Transport Security, Session Management, Basic Web Flaws | Cross-Site Request Forgery (CSRF), Missing Security Headers, Active Mixed Content over HTTPS, Insecure Cookie Attributes |

---

## Technical Overview & Methodology

### 1. Full-Scope Red Teaming Engagement (Phase 1)
* **Objective:** Achieve initial infrastructure foothold ("IN" phase) adhering to a test-halt authorization model.
* **Methodology:** Guided by the **Unified Kill Chain (UKC)** and an intelligence-led approach tracking real-world Tactics, Techniques, and Procedures (TTPs).
* **Execution:**
  * Simulated targeted phishing campaigns targeting personnel to capture administrative and domain credentials.
  * Audited external attack surfaces, identifying exposed services and evaluating email security resilience (e.g., assessing perimeter controls like Abnormal Email Security).
  * Discovered high-severity exposure vectors including WordPress enumeration flaws and unencrypted communication pipelines.

### 2. Advanced Web Application & API Security Review
* **Objective:** Evaluate deep-tier logical flaws within application layers and backend Application Programming Interfaces (APIs).
* **Execution:**
  * Analyzed client-side and server-side package dependencies to map out supply chain vulnerabilities.
  * Simulated exploitation vectors on modern data parsing pipelines, discovering critical ecosystem risks like **Prototype Pollution** and **Command Injection** within outdated third-party utility engines (e.g., historical Lodash distributions).
  * Evaluated API endpoints for common architectural flaws such as lack of strict rate-limiting, missing HTTP protection headers (`X-XSS-Protection`), and session flaws like persistent authentication tokens lacking absolute expiration times.
  * Discovered high-severity web application attack surfaces, executing proof-of-concept vectors for Stored and Reflected Cross-Site Scripting (XSS).

### 3. Transport Layer & Session Integrity Auditing
* **Objective:** Assure structural adherence to modern defensive web standards and encryption constraints.
* **Execution:**
  * Audited implementation state of essential transport policies including HTTP Strict Transport Security (HSTS) and Content Security Policies (CSP).
  * Evaluated application states regarding session token resilience, highlighting vectors vulnerable to session hijacking due to missing `HttpOnly`, `Secure`, and `SameSite` flags.
  * Drafted defensive configuration matrices to resolve Cross-Site Request Forgery (CSRF) and active mixed-content rendering defects.

---

## Sanitization and Compliance Statement
*Note: All artifacts housed within this repository have been fully processed to omit client names, specific system endpoints, internal IP schemas, and corporate personnel identifiers. These files are published strictly under defensive education and professional portfolio presentation boundaries.*
