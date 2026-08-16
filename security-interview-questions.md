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
4. Rest API vs soap api vs Graphql

---

## Scenario-Based Questions

1. If an application fails to connect to the database due to some internal issue, which HTTP status code should be returned to the client? Explain your reasoning.

2. When a user logs in to a web application using a username and password, how are cookies created, where are they stored, and what is the browser's role in generating and managing them?

3. If an OTP is disclosed in the HTTP response, what could be the root cause of this issue?

4. If a cookie has `SameSite=Strict`, is it shared across subdomains?

5. If we want to share resources from a cross-origin domain using CORS, how does the preflight request behave? Is it sent the first time only or on every request? Where does the preflight request happen?

6. Suppose an application is deployed on a container cluster. How would you perform a security assessment of it?
7. If User1 and User2 are on the same network, and User2 wants to view the burpsuite requests and responses that User1 is analysing using burpsuite


---

## Threat Modeling Checklist

- How should a DB store passwords?
- How to protect the DB?
- The web server is connecting with a DB server — where should the DB credentials be stored?
- How to define and enforce trust boundaries?

## AD
1. How do you perform Kerberoasting in an Active Directory penetration test, and what makes an account vulnerable to it?
2. What is Active Directory, and explain the core components — domain, forest, OU, and domain controller — and how they relate to each other.
3. What is Kerberoasting. how it works
4. Describe the process of performing a DCSync attack and what privileges are required.
5. What is a Golden Ticket attack, and how does it differ from a Silver Ticket?
6. You've compromised a low-privilege domain user account on an internal network assessment. Walk through a realistic AD attack chain you'd attempt, from initial enumeration to Domain Admin, and explain your decision points along the way.
7. You compromise a low-privilege domain user and run BloodHound. It shows your user is a member of a group with GenericWrite over a GPO linked to an OU containing several Tier-0 servers. Walk through exactly how you'd weaponize this.
8. Explain the difference between ASREPRoasting and Kerberoasting, including exactly what makes an account vulnerable to each and how you'd identify candidates for both in an engagement.
9. You find that SMB signing is disabled on several servers, and Responder has captured NTLMv2 hashes from passing traffic. Rather than cracking the hashes, explain how you'd use NTLM relay to escalate privileges, including a specific relay-to-LDAP scenario.
10. What is the krbtgt account, why is its hash so critical, and walk through exactly what happens technically when you forge a Golden Ticket with it.
11. You've identified a certificate template in AD CS that's vulnerable to ESC1. Explain precisely what configuration makes it exploitable and walk through the full exploitation chain to obtain a Domain Admin's TGT.
12. A target environment has unconstrained delegation enabled on a non-DC application server. Explain how you'd realistically force a high-value account to authenticate to it, since passive waiting is unreliable, and what you do once you capture the ticket.
13. Explain the MachineAccountQuota attribute, why it's a default AD weakness, and how an attacker chains it into a privilege escalation path without ever having existing computer object control.
14.  You discover a non-admin user has WriteOwner rights over a security group that is itself nested into Domain Admins. Walk through the full ACL abuse chain to weaponize this.
15.  A domain has the "Protected Users" security group and credential guard partially deployed, but only for a subset of privileged accounts. How does this change your approach to credential theft and lateral movement, and what gaps would you specifically look for?
16.  Walk through how you would detect and abuse a misconfigured trust relationship between two domains or forests — specifically, how SID History abuse could let you escalate from a compromised child domain to Enterprise Admin in the forest root.
17.  You're running BloodHound on a mid-sized AD environment (around 2,000 users, 500 computers) and the graph is overwhelming — too many nodes and paths to review manually in the time you have. How do you approach narrowing this down to find the most meaningful attack paths efficiently?

## Privilege escalation
1. what is suid.
2. what is means sudo -l

==============================================================================================================================================================================================================================
# VAPT & Application Security Interview Question Bank

A structured interview question bank for **Web Application, API, Mobile/Android, Thick Client, Network, and AI/LLM Security** penetration testing.

Questions are divided into:

- **Direct Questions** — fundamentals, concepts, methodology, and technical knowledge.
- **Scenario-Based Questions** — practical situations used to evaluate troubleshooting, testing methodology, and security impact.

> This list has been reviewed for duplicate questions. Repeated questions with the same intent have been consolidated into a single question.

---

# Table of Contents

1. [Web Application Security](#1-web-application-security)
2. [API Security](#2-api-security)
3. [Mobile / Android Security](#3-mobile--android-security)
4. [Thick Client Security](#4-thick-client-security)
5. [Network Security](#5-network-security)
6. [Qualys / Vulnerability Management / Security Engineering](#6-qualys--vulnerability-management--security-engineering)
7. [AI / LLM Security](#7-ai--llm-security)
8. [Cross-Domain Authentication & Authorization Scenarios](#8-cross-domain-authentication--authorization-scenarios)
9. [Coverage Summary](#9-coverage-summary)

---

# 1. Web Application Security

## 1.1 Direct Questions

### Methodology & Fundamentals

1. Explain your methodology for testing a web application.
2. How do you perform black-box web application penetration testing?
3. What are the major phases of a web application penetration test?
4. How do you identify the attack surface of a web application?
5. What test cases do you perform before login?
6. What test cases do you perform after login?
7. What is the difference between authentication and authorization?
8. What is your approach to authentication testing?
9. What is your approach to authorization testing?
10. What is IDOR/BOLA?
11. What is BFLA?
12. What are the major types of access-control vulnerabilities?
13. Explain horizontal and vertical privilege escalation.
14. What is a business logic vulnerability?
15. What is a race-condition vulnerability?
16. What is mass assignment?
17. Why is HTTP considered a stateless protocol?
18. Explain DNS resolution from a browser to the destination server.

### SQL Injection

19. What is SQL Injection?
20. What are the major types of SQL Injection?
21. How would you manually test a search field for SQL Injection using a single quote?
22. What happens when a single quote is inserted into a vulnerable SQL parameter?
23. What happens with a classic authentication-bypass payload such as `' OR '1'='1`?
24. What happens when a condition such as `1=1` is injected into a SQL query?
25. What determines which user/account is returned after an authentication-bypass SQL Injection?
26. What is error-based SQL Injection?
27. What is union-based SQL Injection?
28. What is Boolean-based blind SQL Injection?
29. What is time-based blind SQL Injection?
30. What is out-of-band SQL Injection?
31. How can you identify the underlying database type through SQL Injection?
32. How can error-based SQL Injection reveal database information?
33. How can you enumerate database/table names through SQL Injection?
34. How can you enumerate columns through SQL Injection?
35. How can data be retrieved through SQL Injection?
36. What is second-order SQL Injection?
37. Can SQL Injection lead to Remote Code Execution?
38. Can time-based SQL Injection lead to Remote Code Execution?
39. Can SQL Injection provide access to other databases on the same database server?
40. Can a compromised database server be used to reach another database server?
41. Why are parameterized queries used to prevent SQL Injection?
42. What is SQLMap?
43. What important SQLMap options do you commonly use?
44. Can SQLMap be used for file read/write operations?
45. Can SQLMap lead to operating-system command execution?

### Cross-Site Scripting

46. What is Cross-Site Scripting (XSS)?
47. What are the three major types of XSS?
48. What is reflected XSS?
49. What is stored/persistent XSS?
50. What is DOM-based XSS?
51. How does DOM-based XSS work?
52. What is the difference between client-side and server-side XSS?
53. What is the maximum realistic impact of persistent XSS?
54. How do you determine the severity of an XSS vulnerability?
55. What is XSS sandboxing?
56. How can XSS be mitigated?
57. What is the difference between input validation and output encoding?
58. Can XSS still have significant impact when session cookies use HttpOnly?

### CSRF

59. What is CSRF?
60. How does CSRF work?
61. What is the difference between CSRF and SSRF?
62. Can CSRF affect GET requests?
63. Can CSRF affect POST requests?
64. How do you test for CSRF?
65. How do you test CSRF when an endpoint accepts JSON?
66. What is a CSRF token?
67. What weaknesses can allow CSRF protection to be bypassed?
68. How do you mitigate CSRF?

### SOP & CORS

69. What is the Same-Origin Policy (SOP)?
70. What constitutes an origin?
71. How do protocol, host, and port determine an origin?
72. What is CORS?
73. What is a CORS preflight request?
74. When does a browser send an OPTIONS preflight request?
75. What is the difference between a simple CORS request and a preflighted request?
76. What is a CORS misconfiguration?
77. What is the impact of allowing arbitrary origins?
78. Why is `Access-Control-Allow-Credentials: true` sensitive?
79. How do you test CORS?

### Cookies & Sessions

80. Explain the important session-cookie attributes.
81. What is the primary purpose of the HttpOnly flag?
82. What is the purpose of the Secure flag?
83. What is the SameSite attribute?
84. Explain SameSite Strict, Lax, and None.
85. How does SameSite help mitigate CSRF?
86. What is session fixation?
87. What is session hijacking?
88. What security issues can occur when a session cookie does not use HttpOnly?
89. How is session invalidation tested after logout?

### Security Headers

90. What are HTTP security headers?
91. What is Content-Security-Policy (CSP)?
92. What is HSTS?
93. What is X-Frame-Options?
94. What is X-Content-Type-Options?
95. What is Referrer-Policy?
96. What is Permissions-Policy?
97. How does CSP help mitigate XSS?
98. How does X-Frame-Options help prevent clickjacking?
99. What happens when HSTS is enabled?

### HTTP Security

100. Explain the structure of an HTTP request and response.
101. Explain important HTTP response headers.
102. What is HTTP/1.1?
103. What is HTTP/2?
104. What are important security differences between HTTP/1.1 and HTTP/2?
105. What is HTTP Request Smuggling?
106. Explain CL.TE, TE.CL, and TE.TE request-smuggling cases.
107. What is CRLF Injection?
108. What is HTTP Response Splitting?
109. What is Host Header Injection?
110. What are the potential impacts of Host Header Injection?
111. What dependencies or conditions are normally required to exploit Host Header Injection?
112. How do you mitigate Host Header Injection?

### File Inclusion & Log Poisoning

113. What is Local File Inclusion (LFI)?
114. What is Remote File Inclusion (RFI)?
115. What is the difference between LFI and RFI?
116. What types of parameters can indicate potential LFI?
117. How can LFI sometimes lead to RCE?
118. What is log poisoning?
119. How can log poisoning be combined with LFI?
120. Can LFI potentially lead to RCE without an upload feature?
121. What types of files or application resources might you inspect during LFI testing?

### XXE

122. What is XML External Entity (XXE)?
123. What are the major types of XXE?
124. What is in-band XXE?
125. What is blind/out-of-band XXE?
126. Can XXE lead to SSRF?
127. Can XXE lead to local file disclosure?
128. What does `%` represent in an XXE declaration?
129. What is an XML parameter entity?
130. How do you mitigate XXE?

### Authentication, Authorization & Business Logic

131. What are common login-page security test cases?
132. What are common registration-page security test cases?
133. What are common forgot-password security test cases?
134. What are common OTP-bypass techniques?
135. What is account enumeration?
136. What is password-reset poisoning?
137. What is MFA bypass?
138. What is rate-limit bypass?
139. What security issues can occur in checkout/payment functionality?
140. What is a business-logic flaw in a payment or checkout workflow?
141. What is a race condition and how is it tested?
142. What is session fixation and how is it tested?

### OAuth & SAML

143. What is OAuth?
144. Explain a typical OAuth authentication/authorization flow.
145. What are common OAuth security vulnerabilities?
146. What is OAuth redirect URI manipulation?
147. What is the purpose of the OAuth `state` parameter?
148. What is OAuth token leakage?
149. What is SAML?
150. Explain a basic SAML authentication flow.
151. What are common SAML security vulnerabilities?
152. What is SAML signature wrapping?
153. What SAML assertions, signatures, and validation controls should be tested?

---

## 1.2 Scenario-Based Questions

1. A login page appears vulnerable to SQL Injection. How would you verify it manually and safely before using automation?
2. You submit `' OR '1'='1` to a vulnerable login form. Explain what happens at the SQL-query level and why authentication may succeed.
3. You find a parameter where `1=1` changes application behavior. How would you determine the resulting SQL logic and security impact?
4. You discover error-based SQL Injection. How would you validate the finding and demonstrate impact without unnecessarily extracting sensitive production data?
5. You discover time-based blind SQL Injection. How would you determine whether further impact, including possible OS-level execution, is realistically possible?
6. SQL Injection exposes multiple databases on the same DB server. What security boundaries and access controls would you investigate?
7. A compromised database server can communicate with another database server. What trust relationships and network controls would you investigate?
8. A login page has reflected XSS and the session cookie is HttpOnly. How would you demonstrate meaningful impact without relying on cookie theft?
9. A stored XSS payload does not execute when submitted, but executes when an administrator later opens a page. How would you identify the vulnerable parameter and execution sink?
10. A stored XSS executes only for administrators. How would you assess and demonstrate the real-world impact?
11. An API reflects an attacker-controlled Origin and also allows credentials. How would you validate whether the CORS configuration is exploitable?
12. A password-change endpoint uses POST but has no obvious CSRF token. How would you determine whether it is actually vulnerable?
13. A sensitive endpoint accepts JSON with `Content-Type: application/json`. How would you assess its CSRF protection?
14. An application trusts the Host header when generating password-reset URLs. What attack scenario would you investigate?
15. A front-end proxy and backend server appear to parse HTTP requests differently. How would you safely test for HTTP Request Smuggling?
16. You discover LFI but there is no upload functionality. What additional avenues would you investigate for impact?
17. LFI is confirmed and application logs are accessible. Explain how log poisoning could potentially increase the impact.
18. `/admin` returns `403 Forbidden`. What categories of access-control and request-normalization tests would you investigate?
19. A password-reset endpoint has no effective rate limiting. How would you demonstrate the security impact safely?
20. An application allows a one-time coupon to be redeemed. How would you test whether concurrent requests can reuse it?
21. A profile-update API accepts arbitrary JSON fields. How would you test for mass assignment?
22. A checkout application calculates the final price on the client side. What security and business-logic tests would you perform?
23. An OAuth application accepts a user-controlled redirect URI. What security tests would you perform?
24. A SAML response is accepted by the application. How would you validate signature, issuer, audience, assertion, and authentication controls?
25. A user can access another user's resource by modifying an identifier in a request. How would you determine whether it is BOLA/IDOR and assess the impact?

---

# 2. API Security

## 2.1 Direct Questions

### Methodology

1. Describe your API penetration-testing methodology.
2. How do you identify API endpoints during reconnaissance?
3. How do you discover undocumented API endpoints?
4. What HTTP methods should be tested during API security assessments?
5. What authentication mechanisms are commonly used by APIs?
6. How do you test API authentication?
7. How do you test API authorization?
8. How do you test API input validation?
9. How do you test API parameter tampering?
10. How do you test API rate limiting?
11. How do you test API versioning?
12. What is the difference between REST, SOAP, and GraphQL APIs?

### API Vulnerabilities

13. What is BOLA?
14. What is BFLA?
15. What is API mass assignment?
16. What is excessive data exposure?
17. What is improper API asset management?
18. What is API authentication bypass?
19. What is API authorization bypass?
20. What is API rate-limit weakness?
21. What is API parameter pollution?
22. What API security issues can occur when XML input is accepted?
23. What API security issues can occur when a URL parameter is accepted?

### JWT

24. What is JWT?
25. What are the three components of a JWT?
26. What is the JWT header?
27. What is the JWT payload?
28. What is the JWT signature?
29. What JWT security test cases do you perform?
30. What is JWT algorithm confusion?
31. What is `alg:none`?
32. What is RS256?
33. What is HS256?
34. What is the difference between symmetric and asymmetric JWT signing?
35. How can RS256-to-HS256 algorithm confusion occur?
36. Where can an RS256 public key normally be obtained?
37. What information/components are present in an RSA public key?
38. What is the root cause of JWT algorithm confusion?
39. What is JWT key confusion?
40. What is JWT token replay?
41. How do you test JWT expiration?
42. How do you test JWT issuer and audience validation?
43. How do you test JWT privilege escalation?

### OAuth-Based APIs

44. What is OAuth-based API authentication?
45. What OAuth-related security issues should be tested in APIs?
46. How do you test token scope enforcement?
47. How do you test access-token expiration and revocation?

---

## 2.2 Scenario-Based Questions

1. An API allows you to modify another user's account by changing `userId`. How would you test and classify the issue?
2. A normal user changes `role=user` to `role=admin` in a JSON request. What vulnerability could this indicate and how would you validate it?
3. An API returns fields that are not displayed in the application. How would you determine whether this is excessive data exposure?
4. An application exposes `/v1/users` and `/v2/users`. What would you investigate?
5. A JWT uses RS256. You modify the token to use HS256. What would you investigate and why?
6. You have access to an RS256 public key but not the private key. Under what implementation weakness could algorithm confusion become exploitable?
7. An API accepts an expired JWT. What does this indicate and how would you validate the impact?
8. A JWT's role claim can be modified and the server still accepts the token. What would you investigate?
9. An OTP-verification API has no effective rate limit. How would you demonstrate the security impact safely?
10. An API accepts unexpected JSON parameters. How would you test for mass assignment?
11. An API accepts XML input. What additional security tests would you perform?
12. An API accepts a URL parameter. What SSRF-related tests would you consider?
13. An API returns different responses for valid and invalid usernames. What security issue could this create?
14. An API allows concurrent requests to redeem the same transaction. How would you test for a race condition?
15. An API exposes authenticated responses cross-origin. How would you assess CORS and credential handling?

---

# 3. Mobile / Android Security

## 3.1 Direct Questions

### Methodology & Tools

1. Explain your mobile application penetration-testing methodology.
2. Explain your Android application security-testing approach.
3. What do you check during static analysis?
4. What do you check during dynamic analysis?
5. Which tools do you commonly use for Android security testing?
6. What is MobSF?
7. What is JADX?
8. What is Apktool?
9. What is JEB?
10. What is Frida?
11. What is Objection?
12. What is ADB?

### Android Components

13. What are the major Android application components?
14. What is an Activity?
15. What is a Service?
16. What is a Broadcast Receiver?
17. What is a Content Provider?
18. What security issues can occur with exported components?
19. What is Intent Injection?
20. What is Intent Hijacking?
21. What is Deep Link exploitation?
22. What is Android WebView?
23. What WebView vulnerabilities do you test?
24. What is JavaScript bridge abuse?
25. What is insecure WebView configuration?

### SSL Pinning & Runtime Protection

26. What is SSL certificate pinning?
27. Why is SSL pinning implemented?
28. How do you test SSL pinning?
29. How can SSL pinning be assessed/bypassed in an authorized test environment using Frida?
30. How do you approach SSL-pinning testing on a non-rooted device?
31. What limitations exist when testing SSL pinning on a non-rooted device?
32. What is runtime application self-protection?
33. What is RASP?
34. How can RASP detect instrumentation?
35. How would you assess RASP controls during an authorized mobile test?
36. What is root detection?
37. How can root-detection controls be assessed?

### Reverse Engineering & Secure Storage

38. What are the risks of hardcoded secrets?
39. Which files and resources would you inspect for hardcoded strings and secrets?
40. Where would you look for API keys in an Android application?
41. What is `AndroidManifest.xml`?
42. What security information can be obtained from the manifest?
43. What is ProGuard/R8?
44. What is code obfuscation?
45. Why is obfuscation important?
46. What Android storage locations would you inspect for sensitive data?
47. What security risks can arise from sensitive information in application logs?

---

## 3.2 Scenario-Based Questions

1. An Android application refuses to work when a Burp CA certificate is installed. What would you investigate?
2. SSL pinning is implemented. How would you approach testing it on an authorized rooted test device?
3. SSL pinning exists and the test device cannot be rooted. What legitimate approaches could you investigate?
4. The application has root detection. How would you assess whether the control is effective?
5. The application detects Frida or other instrumentation. How would you approach the security assessment?
6. RASP blocks dynamic instrumentation. What would you investigate?
7. An exported Activity accepts attacker-controlled Intent extras. What would you test?
8. An exported Broadcast Receiver processes attacker-controlled data. What could go wrong?
9. A Content Provider is exported. What authorization and data-access checks would you perform?
10. A deep link opens a privileged Activity directly. What would you investigate?
11. A deep link accepts a URL and loads it inside a WebView. What vulnerabilities would you test?
12. WebView has JavaScript enabled. What additional attack surface does this create?
13. A JavaScript bridge exposes sensitive native functions. How would you assess the impact?
14. An APK contains hardcoded API credentials. How would you determine whether they are actually exploitable?
15. An APK is not obfuscated. What risks would you explain to the client?
16. The application communicates with its backend but Burp cannot intercept the traffic. How would you troubleshoot it?
17. The application uses certificate pinning and a custom networking library. What would you investigate?
18. A malicious application can receive another application's Intent. What security issue could exist?
19. An application stores authentication tokens locally. What locations and protections would you inspect?
20. An application exposes sensitive information through logs. How would you validate the issue?

---

# 4. Thick Client Security

## 4.1 Direct Questions

### Methodology

1. Explain your thick-client penetration-testing methodology.
2. What is a thick client?
3. What is the difference between a thick client and a thin client?
4. How do you perform reconnaissance on a thick client?
5. How do you identify application endpoints?
6. How do you proxy HTTP/HTTPS traffic from a thick client?
7. How do you intercept non-HTTP traffic?
8. Can Burp Suite directly intercept raw TCP/UDP traffic?
9. What tools can be used to analyze non-HTTP traffic?
10. How do you test authentication in a thick client?
11. How do you test authorization in a thick client?

### Binary & OS Security

12. What is DLL Hijacking?
13. What is DLL Search Order Hijacking?
14. What is DLL Side-Loading?
15. What is the risk of an unsigned application?
16. What is digital code signing?
17. What is ASLR?
18. How does ASLR protect applications?
19. What is DEP?
20. What is binary reverse engineering?
21. What sensitive information would you search for in a thick-client binary?
22. What is hardcoded credential exposure?
23. What is code obfuscation?
24. Why is client-side validation insufficient as a security control?
25. What local-storage vulnerabilities can exist in thick-client applications?

---

## 4.2 Scenario-Based Questions

1. A thick-client application communicates over HTTPS but does not work through Burp. How would you troubleshoot it?
2. The application communicates using raw TCP. How would you intercept and analyze the traffic?
3. You discover an unsigned executable. What security risks would you investigate?
4. The application loads DLLs from its working directory. What would you investigate?
5. You identify a potentially hijackable DLL. How would you safely validate the issue?
6. The application is not compiled with ASLR. What impact could this have?
7. Sensitive credentials are found inside the executable. How would you determine whether they are exploitable?
8. The client-side application validates the user's role locally. How would you determine whether server-side authorization can be bypassed?
9. The application stores credentials locally. What locations and protections would you investigate?
10. A thick client communicates with multiple backend servers. How would you map and test those interfaces?
11. The application uses proprietary TCP communication. How would you identify and analyze the protocol?
12. An executable contains sensitive strings while the application uses encryption. How would you investigate where cryptographic keys are stored?

---

# 5. Network Security

## 5.1 Direct Questions

### Methodology & Scanning

1. Explain your network penetration-testing methodology.
2. How do you perform network reconnaissance?
3. How do you perform port scanning?
4. How do you prioritize a large list of IP addresses?
5. How would you test 1,000 IP addresses within one week?
6. What tools do you use for network penetration testing?
7. What is Nmap?
8. What is Nessus?
9. What is Qualys?
10. What is the difference between vulnerability scanning and penetration testing?
11. How do you validate automated scanner findings?
12. How do you identify false positives?
13. What is service fingerprinting?
14. What is banner grabbing?
15. What is enumeration?

### Network Protocols & Services

16. What is the difference between TCP and UDP?
17. Explain the TCP three-way handshake.
18. How do you test FTP?
19. How do you test SSL/TLS?
20. How do you test SMB?
21. What SMB versions would you identify during an assessment?
22. What are common SMB security issues?
23. How do you test DNS?
24. How do you test SMTP?
25. How do you test SNMP?
26. What is LDAP?
27. What is Kerberos?
28. What is RDP?
29. What common ports are associated with major network services?
30. What is DNS zone transfer?
31. What security issues can arise from exposed SNMP services?

---

## 5.2 Scenario-Based Questions

1. You receive 1,000 IP addresses and have one week to assess them. Explain your complete approach, prioritization, tooling, validation, and reporting strategy.
2. An IP exposes TCP/25, UDP/161, and TCP/53. What would you test for each service?
3. An FTP service is exposed. What would you check before considering it vulnerable?
4. A server supports weak TLS protocols or ciphers. How would you validate and report the finding?
5. SMB is exposed to the network. What enumeration and security tests would you perform?
6. UDP/161 is open. What would you investigate?
7. DNS port 53 is open. What DNS security tests would you perform?
8. SMTP port 25 is exposed. What would you test?
9. A DNS server permits zone transfer. How would you validate the issue and assess its impact?
10. A VA scanner reports 5,000 vulnerabilities, but you believe many are false positives. How would you validate them efficiently?
11. You identify a recurring false positive in a scanner. What would you do so that it does not repeatedly appear in future assessments?
12. A production server exposes many services. How would you prioritize testing while minimizing business impact?
13. A scanner reports an OS vulnerability but patch status is unclear. How would you verify the finding?
14. A vulnerability is confirmed on one host and appears across hundreds of hosts. How would you validate it efficiently?

---

# 6. Qualys / Vulnerability Management / Security Engineering

## 6.1 Direct Questions

1. What is your favourite vulnerability to find and exploit?
2. Why is it your favourite vulnerability?
3. How do you identify your favourite vulnerability?
4. Tell me about critical vulnerabilities you have discovered.
5. How would you create detection logic for BOLA?
6. How would you create detection logic for BFLA?
7. Explain the major types of access-control issues.
8. What is the difference between vulnerability assessment and penetration testing?
9. What is the difference between SAST and DAST?
10. What is SBOM analysis?
11. What information does an SBOM contain?
12. How can SBOM analysis help identify security risks?
13. What is vulnerability detection/signature logic?
14. How do you reduce false positives in automated vulnerability scanning?
15. How do you validate a vulnerability reported by an automated scanner?

---

## 6.2 Scenario-Based Questions

1. A scanner reports a critical vulnerability on 5,000 hosts. How would you validate it efficiently?
2. A scanner repeatedly reports a vulnerability that manual testing proves is a false positive. How would you improve the detection logic?
3. You need to create a signature for BOLA. What request/response characteristics would you use?
4. You need to detect BFLA automatically. What logic would you design?
5. A vulnerability scanner identifies SQL Injection based only on an error message. How would you determine whether it is a true positive?
6. A scanner reports XSS, but the payload is encoded and never executes. How would you validate the finding?
7. A scanner reports an outdated library. How would you verify whether the vulnerable component is actually present and relevant?
8. A client challenges a critical vulnerability as a false positive. How would you reproduce and prove the finding?
9. You have thousands of findings with different severities. How would you prioritize manual validation?

---

# 7. AI / LLM Security

## 7.1 Direct Questions

1. What security vulnerabilities can exist in an AI/LLM application?
2. What is prompt injection?
3. What is indirect prompt injection?
4. What is jailbreak testing?
5. What is sensitive-information disclosure in LLM applications?
6. What is system-prompt leakage?
7. What is insecure output handling?
8. What is excessive agency?
9. What is improper access control in an AI application?
10. What is data poisoning?
11. What is model denial of service?
12. What is insecure plugin/tool usage?
13. What is SSRF in an AI application?
14. What is RAG security?
15. What is vector-database security?
16. What is data leakage through an LLM?
17. How would you test an AI application's input validation?

---

## 7.2 Scenario-Based Questions

### Scenario: AI Application With Only an Input Box

You are given an AI application with only an input box and the application's response. You have no source code or documentation.

What vulnerabilities would you test?

1. Prompt injection.
2. System-prompt disclosure.
3. Jailbreaks.
4. Sensitive-information disclosure.
5. Instruction-hierarchy bypass.
6. Context manipulation.
7. Indirect prompt injection.
8. Unauthorized tool/function invocation.
9. SSRF through available tool/function capabilities.
10. Excessive agency.
11. Unauthorized data extraction.
12. Cross-user data leakage.
13. RAG/vector-database access-control issues.
14. Insecure output handling.
15. XSS if AI output is rendered as HTML.
16. Markdown injection.
17. Code execution through unsafe generated/processed content.
18. Resource-exhaustion / denial-of-service conditions.
19. Exposure of secrets in responses.
20. Model-behavior manipulation.

---

# 8. Cross-Domain Authentication & Authorization Scenarios

## Login

1. Login accepts unlimited password attempts. What would you test?
2. Login returns different responses for valid and invalid usernames. What vulnerability may exist?
3. A login endpoint appears vulnerable to SQL Injection. How would you validate it safely?
4. A session remains valid after logout. How would you investigate?
5. A normal user can directly access an administrator endpoint. How would you classify and validate the issue?

## Registration

6. What security test cases would you perform on a registration workflow?
7. What would you test for duplicate-account creation?
8. How would you test registration rate limiting?
9. How would you test email/phone verification?
10. How would you test privilege-related parameters during registration?

## Forgot Password

11. A password-reset token never expires. What is the impact?
12. A password-reset token can be reused. How would you test it?
13. OTP requests are unlimited. What would you investigate?
14. OTP verification has no effective rate limiting. How would you demonstrate impact?
15. A password-reset link is generated using a manipulated Host header. What vulnerability could result?
16. How would you test password-reset token predictability and entropy?

## Checkout / Business Logic

17. The application calculates the final price on the client side. What would you test?
18. A discount coupon can be reused by sending multiple concurrent requests. What vulnerability could exist?
19. A user can change the price, quantity, product ID, or discount value in the request. What would you test?
20. A payment succeeds but the order status remains client-controlled. What would you investigate?

## OAuth

21. An OAuth redirect URI is partially user-controlled. What would you test?
22. The OAuth state parameter is missing or predictable. What could happen?
23. An access token is exposed in a URL or browser history. What would you investigate?
24. OAuth scopes are not correctly enforced. How would you validate the impact?

## SAML

25. A SAML response is accepted without proper signature validation. What would you investigate?
26. The SAML issuer or audience is not validated. What impact could this create?
27. A SAML assertion contains conflicting identity information. What validation logic would you test?

---

# 9. Coverage Summary

The consolidated question bank covers the original handwritten notes and the additional typed questions.

| Domain | Direct | Scenario | Covered |
|---|---:|---:|---|
| Web Application | 153 | 25 | Yes |
| API | 46 | 15 | Yes |
| Mobile / Android | 47 | 20 | Yes |
| Thick Client | 25 | 12 | Yes |
| Network | 31 | 14 | Yes |
| Qualys / VA / Security Engineering | 15 | 9 | Yes |
| AI / LLM | 17 | 20 | Yes |
| Authentication / Authorization | — | 27 | Yes |

## Original Topics Verified

- Web application methodology
- Black-box testing
- Pre-login scenarios
- IDOR / BOLA
- BFLA
- Access control
- SQL Injection
- Error-based SQLi
- Blind SQLi
- Time-based SQLi
- SQLi to RCE
- Database enumeration
- Second-order SQLi
- SQLMap
- XSS
- Reflected XSS
- Stored XSS
- DOM XSS
- XSS with HttpOnly
- CSRF
- SOP
- CORS
- CORS preflight
- Cookie attributes
- HttpOnly
- Secure
- SameSite
- Security headers
- HSTS
- CSP
- X-Frame-Options
- HTTP Request Smuggling
- CRLF Injection
- Host Header Injection
- LFI
- RFI
- Log poisoning
- XXE
- Business logic
- Race conditions
- Mass assignment
- Login testing
- Registration testing
- Forgot-password testing
- OTP bypass
- Checkout testing
- OAuth
- SAML
- API penetration-testing methodology
- JWT
- JWT algorithm confusion
- RS256 / HS256
- JWT public-key concepts
- BOLA / BFLA
- API rate limiting
- Android components
- Intent Injection
- Intent Hijacking
- Deep Linking
- WebView
- SSL pinning
- Frida
- RASP
- Root detection
- Hardcoded secrets
- Android static/dynamic analysis
- Thick-client methodology
- HTTP/HTTPS proxying
- TCP/UDP traffic
- DLL Hijacking
- DLL Side-Loading
- Code signing
- ASLR
- DEP
- Network penetration testing
- 1,000-IP assessment scenario
- FTP
- SSL/TLS
- SMB
- DNS
- SMTP
- SNMP
- Nessus
- Qualys
- False-positive validation
- Vulnerability detection logic
- SAST
- SBOM
- AI/LLM security
- Prompt injection
- Jailbreak
- System-prompt leakage
- RAG security
- Excessive agency
- AI tool/function abuse

---

## Suggested Repository Structure

```text
vapt-interview-questions/
├── README.md
├── web-application.md
├── api-security.md
├── mobile-android.md
├── thick-client.md
├── network-security.md
├── qualys-security-engineering.md
└── ai-llm-security.md
```

The consolidated question bank can be kept as `README.md`, with the individual domain files added later if you want to split the repository into separate study sections.

