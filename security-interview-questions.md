# Security Interview Questions

## Setting up the context

This document covers security interview questions organized by domain and OWASP categories.
Use this to assess your knowledge across Web Application Security, Mobile Security, DevSecOps, and general cross-domain topics.

---

## Step 1: Web Application Security

### A01: Broken Access Control (OWASP 2025)

1. What is IDOR (Insecure Direct Object Reference)?
2. What is privilege escalation?
3. What are the types of privilege escalation, and how do they differ from IDOR?
4. What is account takeover?
5. What is directory listing?
6. What is path traversal?
7. What is the difference between path traversal and LFI?
8. What is the difference between RFI (Remote File Inclusion) and LFI (Local File Inclusion)?
9. Are all RFI vulnerabilities also SSRF?
10. What is an open redirect vulnerability?
11. What is session puzzling?
12. What is unprotected read access in applications?
13. What actions can be performed after identifying an LFI (Local File Inclusion) vulnerability?
14. How can LFI (Local File Inclusion) lead to RCE (Remote Code Execution)?
15. What are the implications of path traversal vulnerabilities and exposed SSH ports?
16. What is SSRF (Server-Side Request Forgery)?
17. What is SSRF and how can it be exploited in AWS environments?


### A02: Security Misconfiguration

1. What is CSP (Content Security Policy)?
2. What is the CSP (Content Security Policy) header?
3. What CSP header values are used to mitigate clickjacking?
4. What are security headers?
5. What is clickjacking?
6. What is the effect of properly configured CORS on CSRF attacks?
7. What is a preflight request?
8. What is HTTP request smuggling?
9. What is web cache poisoning?
10. What is web cache deception?
11. What is the difference between web cache poisoning and web cache deception?
12. What is directory listing?
13. What are the reasons for conducting security assessments even when a WAF is in place?
14. What is the difference between a WAF and a Next-Gen WAF?


### A03: Software Supply Chain Failures

1. What is Software Composition Analysis (SCA)?
2. What is dependency confusion?
3. What is the difference between transitive dependency and direct dependency?
4. How do you report transitive dependencies in security assessments?
5. What are zero-day vulnerabilities and how can they be mitigated?
6. What are common false positives in Fortify scans?


### A04: Cryptographic Failures

1. How should data be handled securely at rest and in transit?
2. If a custom encryption mechanism is implemented, how can it be bypassed?
3. Is custom encryption sufficient compared to AES or DES?
4. What are JWT test cases?
5. What are SAML test cases?
6. What are OAuth test cases?
7. What is OpenID authentication, and what are its associated test cases?
8. What are cookie attributes?
9. What are SameSite cookies?
10. What are SameSite cookie attribute values (Strict, Lax, None)?
11. What is the role of SameSite attribute in preventing CSRF?


### A05: Injection

1. What is SQL Injection and how does it impact application security?
2. What are the different types of SQL injection and their mitigation techniques?
3. How can SQL Injection be performed or bypassed?
4. What is LDAP injection?
5. What is OGNL injection?
6. What is ORM injection?
7. What is OS command injection?
8. What is SSTI (Server-Side Template Injection) and how can it be exploited?
9. What is XXE (XML External Entity) attack?
10. How can XXE vulnerabilities occur in REST-based APIs using JSON format?
11. How do you handle XXE when no response is received from the server?
12. What is HTML injection?
13. What is host header injection?
14. What is dangling markup injection?
15. What are the different types of injection attacks?


### A06: Insecure Design

1. How do you design a secure login page, and what test cases should be considered?
2. What are common login test cases in application security?
3. What are the mitigation techniques for OTP bypass vulnerabilities?
4. What are the techniques used for OTP bypass?
5. What are trust boundaries in security?
6. What are the key API security recommendations?
7. What are common API security test cases?
8. How do you perform scanning when CSRF tokens are implemented?
9. How do you handle scanning if the session logs out after 30 minutes?
10. What is a race condition vulnerability?
11. What is response manipulation?


### A07: Authentication Failures

1. What are the mitigation techniques for CSRF?
2. What is CSRF (Cross-Site Request Forgery)?
3. What are the test cases for JWT?
4. What are the test cases for OAuth?
5. What are login test cases?
6. How is session handled securely?


### A08: Software & Data Integrity Failures

1. What is insecure deserialization?
2. What is PHP object injection?
3. If custom serialization is implemented, how can a deserialization attack be performed?
4. What is prototype pollution?
5. What exploits can prototype pollution lead to (client/server side)?


### A09: Security Logging & Alerting Failures

1. What are the challenges in detecting attacks without proper logging?


### A10: Mishandling of Exceptional Conditions

1. What are the options when output encoding cannot be implemented?
2. What happens when unexpected inputs are processed incorrectly?


---

## Step 2: Mobile Security (Android + iOS)

### A01: Broken Access Control

1. How can exported components in Android applications be exploited?
2. How do you check for read and write access in exported activities?
3. What is an Intent in Android, and why can it be dangerous as a communication channel between activities?
4. What is the difference between implicit and explicit intents in Android?
5. What is deeplink exploitation?
6. What are deep links and what security risks do they introduce?


### A02: Security Misconfiguration

1. How can `allowBackup="true"` be exploited?
2. How can `debuggable="true"` be exploited in Android applications?
3. How do you install the Burp Suite certificate on Android 10+ devices?


### A03: Software Supply Chain Failures

1. What are vulnerabilities specific to mobile applications?
2. What are common security concerns in Flutter-based Android apps?


### A04: Cryptographic Failures

1. Where are secrets stored in Android and iOS (Keystore system vs Keychain)?
2. What is SSL pinning and why is it implemented?
3. What are the reasons for implementing SSL pinning?
4. How can SSL pinning be bypassed in a Flutter application?
5. How can SSL pinning be bypassed?
6. If data is encrypted after being captured in Burp Suite, how do you decrypt the request data in browsers and mobile applications?


### A05: Injection

1. What is WebView and deep linking? Is XSS possible in Android applications?
2. How can SQL Injection occur via a Content Provider?


### A06: Insecure Design

1. What are the different approaches to mobile application security?
2. How do you perform security testing on Android apps and iOS apps?


### A07: Authentication Failures

1. What are OTP bypass techniques in mobile applications?


### A08: Software & Data Integrity Failures

1. Can an IPA file be recompiled and re-signed like an Android APK? If yes, what is the process? If not, why?


### A10: Mishandling of Exceptional Conditions

1. What happens when security checks fail in mobile apps (root/jailbreak detection bypass)?


### Mobile Tools / Practical (Important for Interviews)

1. How does Frida work?
2. Can you write a Frida script manually?
3. What is hooking in Android and how is it used in security testing?
4. What is SSL pinning, root detection, and jailbreak detection? How can they be bypassed?
5. What are various ways to install an IPA file?


---

## Step 3: DevSecOps / Network / Infrastructure

### A02: Security Misconfiguration

1. What is the difference between Nessus Essentials and other Nessus versions?
2. What is IP overlapping in Nessus scans?
3. What is a paranoid scan in Nmap? What are other unique scan types available?
4. How do you perform an IPv6 scan using Nmap?
5. What command is used for fragmentation-based scanning in Nmap (`-f`), and why is it used?
6. What is the default port scan behavior in Nmap?
7. What type of scan does Nmap perform by default when running `nmap <IP>`?
8. How does Nmap determine which ports to send TCP SYN packets to?
9. How does Nmap indicate filtered and closed ports during analysis?
10. What are the common uses of ports 21, 22, 25, 445, and 8009?


### A01: Broken Access Control (Infrastructure Level)

1. How does the LLMNR response obtained from the Responder tool work?


### A05: Injection / Exploitation

1. How does Mimikatz work?


### A06: Insecure Design

1. What are the differences between Linux and Windows in terms of attacks or commonly exposed ports?


### A03: Supply Chain

1. What is Software Composition Analysis (SCA)?


### A02 / A05: Mixed Infrastructure Vulnerabilities

1. What are critical vulnerabilities associated with SMB (Server Message Block)?
2. What are common vulnerabilities in Samba?


---

## Step 4: General / Cross-Domain

### A05: Injection

1. What are the various methods for achieving RCE (Remote Code Execution)?
2. What is RCE (Remote Code Execution) vs OS command injection?
3. What is Out-of-Band (OOB) SQL Injection?


### A02: Security Misconfiguration

1. Is HTTP stateful or stateless? How does it compare with TCP?
2. When does the TLS handshake occur in a connection lifecycle?
3. What is the difference between REST and SOAP APIs?
4. What are WebSockets?
5. What are web services?


### A06: Insecure Design

1. What is the secure code review process?
2. How do you perform security testing on web applications and thick client applications?
3. What is the difference between automated and manual security testing?
4. What would you do if a developer is unable to fix a vulnerability?


### A07: Authentication

1. What is the difference between cookies and JWT?
2. What are the different OAuth grant types?
3. What are `kid` and `jku` parameters in JWT, and how can they be abused?


### A08: Integrity Failures

1. How can you identify Java serialization/deserialization vulnerabilities?
2. Which common libraries are vulnerable to deserialization attacks?


### A01 / Concepts

1. What is the difference between CWE and CVE?
2. What is SOP (Same-Origin Policy)?
3. What is server-side validation?


---

## Scenario-Based Questions

1. If an application fails to connect to the database due to some internal issue, which HTTP status code should be returned to the client? Explain your reasoning.

2. When a user logs in to a web application using a username and password, how are cookies created, where are they stored, and what is the browser's role in generating and managing them?

3. If an OTP is disclosed in the HTTP response, what could be the root cause of this issue?

4. If a cookie has `SameSite=Strict`, is it shared across subdomains?

5. If we want to share resources from a cross-origin domain using CORS, how does the preflight request behave? Is it sent the first time only or on every request? Where does the preflight request happen?

6. Suppose an application is deployed on a container cluster. How would you perform a security assessment of it?


---

## Threat Modeling Checklist

- How should a DB store passwords?
- How to protect the DB?
- The web server is connecting with a DB server — where should the DB credentials be stored?
- How to define and enforce trust boundaries?
