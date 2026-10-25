# Cybersecurity-CTF-Labs-Collection-File-Upload-Bypasses-Broken-Access-Control
A curated index of hands-on CTF labs covering file upload filter bypasses (MIME, Content-Type, Polyglots, Double Extensions) and Broken Access Control (BOLA, BFLA, Parameter Tampering) from Learn SecByte.
# File Upload Filter Bypasses & Broken Access Control CTF Labs Collection

A structured, searchable index of hands-on cybersecurity labs focusing on file upload filter evasion techniques (Content-Type header manipulation, MIME validation bypasses, double extensions, polyglot files, null byte truncation) and Broken Access Control vulnerabilities (API authorization bypass, function-level access control, parameter tampering, role manipulation) hosted on Learn SecByte.

This collection is designed for application security engineers, penetration testers, CTF competitors, security analysts, and software developers learning how to audit, exploit, and secure application upload handling and access enforcement logic.

---

## Table of Contents
- [Introduction](#introduction)
- [Lab Collection & Index](#lab-collection--index)
- [Categories](#categories)
  - [File Upload Filter Evasion & Bypass Techniques](#file-upload-filter-evasion--bypass-techniques)
  - [Broken Access Control & Authorization Flaws](#broken-access-control--authorization-flaws)
- [Learning Path](#learning-path)
- [How to Use the Labs](#how-to-use-the-labs)
- [Disclaimer](#disclaimer)

---

## Introduction

Insecure file upload mechanics and broken access controls consistently rank among the most critical application security risks. When servers trust client-side headers, rely solely on superficial extension checks, or fail to enforce robust server-side authorization checks on API endpoints, attackers can execute arbitrary code or gain unauthorized administrative access.

This repository organizes hands-on security labs from Learn SecByte into logical learning paths covering advanced file upload validation and access control auditing.

---

## Lab Collection & Index

| Lab Title | Primary Category | Vulnerability / Focus | Access Link |
| :--- | :--- | :--- | :--- |
| **Content-Type Bypass** | File Uploads | Header Trust & Filter Evasion | [Access Lab](https://learn.secbyte.org/ctf/content-type-bypass-from-header-trust-to-filter-evasion) |
| **MIME-Type Bypass** | File Uploads | Upload Filter Validation | [Access Lab](https://learn.secbyte.org/ctf/mime-type-bypass-upload-filters) |
| **Null Byte Upload** | File Uploads | Extension Truncation Bypass | [Access Lab](https://learn.secbyte.org/ctf/null-byte-upload-bypassing-file-extension-filters) |
| **Double Extension Upload** | File Uploads | Multi-Extension Handler Abuse | [Access Lab](https://learn.secbyte.org/ctf/double-extension-upload-from-filter-bypass-to-defensive-dete) |
| **Polyglot File Upload** | File Uploads | Dual-Format File Construction | [Access Lab](https://learn.secbyte.org/ctf/polyglot-file-upload) |
| **Unrestricted File Upload** | File Uploads | Core Validation Failures | [Access Lab](https://learn.secbyte.org/ctf/unrestricted-file-upload) |
| **Function-Level Authorization** | Access Control | Broken Access Control (BFLA) | [Access Lab](https://learn.secbyte.org/ctf/function-level-authorization-broken-access-control) |
| **API Authorization Bypass** | Access Control | API Enforcement Failure | [Access Lab](https://learn.secbyte.org/ctf/api-authorization-bypass) |
| **Access Control Bypass** | Access Control | Broken Authorization Mechanics | [Access Lab](https://learn.secbyte.org/ctf/access-control-bypass-broken-authorization-lab) |
| **Parameter Tampering** | Access Control | Hidden Input & State Tampering | [Access Lab](https://learn.secbyte.org/ctf/parameter-tampering-breaking-trust-in-hidden-inputs) |
| **Role Manipulation** | Access Control | Privilege Escalation | [Access Lab](https://learn.secbyte.org/ctf/role-manipulation) |

---

## Categories

### File Upload Filter Evasion & Bypass Techniques
Hands-on CTF labs exploring client-side header trust, file signature inspection, multi-extension execution logic, and polyglot payload construction:

* **Unrestricted File Upload:** Core concepts of unvalidated file uploads leading to web shell drop and execution.
  * Lab Link: https://learn.secbyte.org/ctf/unrestricted-file-upload
* **Content-Type Bypass:** Bypassing upload restrictions by tampering with the HTTP `Content-Type` header during request transmission.
  * Lab Link: https://learn.secbyte.org/ctf/content-type-bypass-from-header-trust-to-filter-evasion
* **MIME-Type Bypass:** Subverting MIME validation logic and magic byte verification in web applications.
  * Lab Link: https://learn.secbyte.org/ctf/mime-type-bypass-upload-filters
* **Null Byte Extension Truncation:** Utilizing null bytes (`%00`) to truncate string extensions in file upload handlers.
  * Lab Link: https://learn.secbyte.org/ctf/null-byte-upload-bypassing-file-extension-filters
* **Double Extension Abuse:** Exploiting misconfigured web server handlers (e.g., Apache `.php.jpeg`) to force executable script parsing.
  * Lab Link: https://learn.secbyte.org/ctf/double-extension-upload-from-filter-bypass-to-defensive-dete
* **Polyglot File Upload:** Crafting valid dual-format files (e.g., GIF/PHP or JPG/PHP polyglots) that pass binary header inspection while executing code.
  * Lab Link: https://learn.secbyte.org/ctf/polyglot-file-upload

### Broken Access Control & Authorization Flaws
Practical security labs demonstrating privilege escalation, parameter tampering, and administrative restriction bypasses:

* **Access Control Bypass:** Fundamentals of broken access controls and unauthorized state modification.
  * Lab Link: https://learn.secbyte.org/ctf/access-control-bypass-broken-authorization-lab
* **Function-Level Authorization (BFLA):** Bypassing administrative access checks to invoke restricted administrative functionality.
  * Lab Link: https://learn.secbyte.org/ctf/function-level-authorization-broken-access-control
* **API Authorization Bypass:** Circumventing authorization logic on REST/JSON API endpoints to query or modify protected resources.
  * Lab Link: https://learn.secbyte.org/ctf/api-authorization-bypass
* **Parameter Tampering:** Modifying client-side hidden fields, request parameters, and cookies to alter transaction ownership.
  * Lab Link: https://learn.secbyte.org/ctf/parameter-tampering-breaking-trust-in-hidden-inputs
* **Role Manipulation:** Altering user identity parameters, role arrays, or claims to escalate privileges from low-tier user to administrator.
  * Lab Link: https://learn.secbyte.org/ctf/role-manipulation

---

## Learning Path

Follow this structured roadmap to master file handling security and authorization testing:

1. **Upload Validation & Extension Handling**
   - Practice basic unrestricted file uploads and test Content-Type/MIME header modification.
   - Master advanced bypasses using double extensions, null bytes, and polyglot files.
2. **Access Control Fundamentals**
   - Identify parameter tampering vulnerabilities in hidden forms and cookies.
   - Practice role manipulation and user state escalation.
3. **API Security & Function-Level Authorization**
   - Test RESTful APIs for missing object and function-level access control checks.
   - Implement centralized server-side authorization matrices and strict file storage policies.

---

## How to Use the Labs

1. Select a practice environment from the index table or category sections above.
2. Access the target lab directly on Learn SecByte.
3. Utilize web proxies (e.g., Burp Suite) to intercept HTTP traffic, modify request headers, alter parameter values, and craft custom file payloads.
4. Review defensive controls to learn how strict extension allowlists, randomized filename generation, and role-based access control (RBAC) protect applications.

---

## Disclaimer

This repository is strictly intended for educational research, authorized security testing, and defensive engineering training. All concepts, techniques, and lab environments are provided to help cybersecurity practitioners identify vulnerabilities and harden systems. Unsanctioned testing or attacks against external infrastructure without prior written authorization are strictly illegal.
