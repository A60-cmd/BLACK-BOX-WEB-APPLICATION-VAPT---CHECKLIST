# BLACK-BOX-WEB-APPLICATION-VAPT---CHECKLIST

# 🔥 Web Application Penetration Testing — Vulnerability Checklist

A practical vulnerability checklist for Web Application VAPT engagements. This checklist covers commonly identified vulnerabilities, categorized by severity, along with real-world examples and testing priorities.

---

# 🔴 CRITICAL — Found in Almost Every Real Engagement

| # | Vulnerability | Example / Testing Scenario |
|---|---|---|
| 1 | **IDOR (Insecure Direct Object Reference)** | Change `?id=123` to `?id=124` |
| 2 | **Broken Access Control** | Access admin/user functions without permission |
| 3 | **SQL Injection** | Login bypass, data extraction |
| 4 | **Authentication Bypass** | Logic flaws, `JWT alg:none`, default credentials |
| 5 | **Business Logic Flaws** | Negative amount, price manipulation, replay |
| 6 | **Race Condition** | Double spend, coupon abuse |
| 7 | **Command Injection / RCE** | Any feature running system commands |
| 8 | **Insecure Deserialization** | Cookie/body containing a serialized object |
| 9 | **Hardcoded Secrets** | API keys, DB credentials, JWT secret in JS/APK/config |
| 10 | **Exposed `.git` / `.env` / Backup Files** | Full source code and credentials exposure |

---

# 🟠 HIGH — Found in Most Applications

| # | Vulnerability | Example / Testing Scenario |
|---|---|---|
| 1 | **Stored XSS** | Beneficiary name, ticket, profile, remarks |
| 2 | **Reflected XSS** | Search, error pages, redirects |
| 3 | **CSRF** | State-changing actions without a token |
| 4 | **SSRF** | URL-fetch features (webhook, image import) |
| 5 | **XXE** | XML endpoints, SVG/DOCX upload, SAML |
| 6 | **JWT Weak Secret / Claim Tampering** | Role escalation |
| 7 | **Mass Assignment** | Add `role:admin` to profile update |
| 8 | **Forced Browsing** | `/admin`, `/api/admin`, `/internal` |
| 9 | **Open Redirect** | `?redirect=`, `?next=`, `?return=` |
| 10 | **Host Header Injection** | Password reset poisoning |
| 11 | **CORS Misconfiguration** | `Access-Control-Allow-Origin: *` + credentials |
| 12 | **Sensitive Data Exposure** | Password hash, CVV, PAN in API response |
| 13 | **OTP / 2FA Bypass** | Null, reuse, brute force, endpoint skip |
| 14 | **Session Not Invalidated** | After logout / password change |
| 15 | **Account Enumeration** | Login / register / password reset |
| 16 | **Unrestricted File Upload** | Shell upload, extension bypass |
| 17 | **Path Traversal / LFI** | `../../../../etc/passwd` |
| 18 | **NoSQL Injection** | MongoDB `$ne`, `$gt` in login |
| 19 | **LDAP Injection** | AD-integrated login |
| 20 | **SSTI** | `{{7*7}}` → RCE in template fields |
| 21 | **API Key Exposed in Client JS** | API key disclosure in frontend JavaScript |
| 22 | **Verbose Error / Stack Trace** | Reveals internal application details |
| 23 | **Rate Limiting Missing** | On login, OTP, transfer |
| 24 | **Account Lockout Missing** | Brute force possible |
| 25 | **Weak Password Policy** | `123456` accepted |

---

# 🟡 MEDIUM — Very Common Findings

## 1. Cookie & Session Management

| # | Vulnerability | Description |
|---|---|---|
| 1 | **Missing HttpOnly on Session Cookie** | Session cookie accessible through JavaScript |
| 2 | **Missing Secure on Session Cookie** | Cookie may be transmitted over HTTP |
| 3 | **Missing SameSite on Session Cookie** | Cross-site cookie requests may be possible |
| 4 | **Session Not Rotated After Login** | Existing session ID remains unchanged after authentication |
| 5 | **Session Token in URL** | Session token exposed in URL |
| 6 | **Predictable Session Token** | Session token can be guessed or predicted |
| 7 | **Session Timeout Too Long** | Session remains active for an extended period |
| 8 | **Concurrent Sessions Unlimited** | Multiple sessions allowed without restrictions |
| 9 | **Password Autocomplete Enabled** | Browser can save or autocomplete credentials |
| 10 | **Cache-Control Missing on Authenticated Pages** | Sensitive authenticated content may be cached |

## 2. Security Headers

| # | Vulnerability | Description |
|---|---|---|
| 1 | **Missing Content-Security-Policy** | CSP header not implemented |
| 2 | **Missing Strict-Transport-Security (HSTS)** | HSTS header not implemented |
| 3 | **Missing X-Frame-Options / frame-ancestors** | Potential Clickjacking |
| 4 | **Missing X-Content-Type-Options: nosniff** | MIME-type sniffing may be possible |
| 5 | **Missing Referrer-Policy** | Referrer information may be exposed |
| 6 | **Missing Permissions-Policy** | Browser features are not restricted through this policy |

## 3. Authentication & Authorization

| # | Vulnerability | Description |
|---|---|---|
| 1 | **Credentials Over HTTP** | Credentials transmitted without HTTPS |
| 2 | **Password Reset Token Predictable / Not Expiring** | Weak or reusable password reset tokens |
| 3 | **Password Change Without Current Password** | Password can be changed without confirming the existing password |
| 4 | **Email Change Without Verification** | Email address can be changed without verification |
| 5 | **2FA Not Enforced** | Two-factor authentication is not mandatory |
| 6 | **Weak CAPTCHA / CAPTCHA Missing** | CAPTCHA can be bypassed or is not implemented |
| 7 | **Improper Input Validation** | Numeric, email, or length validation issues |

## 4. HTTP, TLS & Server Configuration

| # | Vulnerability | Description |
|---|---|---|
| 1 | **Application Accessible Over HTTP (No HTTPS Redirect)** | HTTP requests are not redirected to HTTPS |
| 2 | **Weak TLS** | TLS 1.0/1.1, weak ciphers |
| 3 | **Server / Framework Version Disclosure** | Server or framework version exposed |
| 4 | **X-Powered-By Disclosure** | Technology information exposed through headers |
| 5 | **Directory Listing Enabled** | Server exposes directory contents |
| 6 | **Backup Files Exposed** | `.bak`, `.old`, `.zip` |
| 7 | **Source Maps Exposed** | `.map` files exposed |
| 8 | **HTML Comments Disclose Paths / TODO** | Sensitive paths or development notes exposed |
| 9 | **JS File Discloses Internal Endpoints** | Internal API endpoints exposed in JavaScript |
| 10 | **Swagger / OpenAPI Exposed** | API documentation publicly accessible |
| 11 | **Exposed Debug Endpoint** | `/debug`, `/actuator` |

## 5. API Security & Information Disclosure

| # | Vulnerability | Description |
|---|---|---|
| 1 | **API Over-Fetching** | Returns more data than needed |
| 2 | **Sequential IDs in URLs (Leads to IDOR)** | Predictable object identifiers |
| 3 | **Verbose Error / Stack Trace** | Internal application information disclosed |
| 4 | **CSV Injection** | `=cmd|...` in export |
| 5 | **CRLF Injection** | Header injection |
| 6 | **Parameter Pollution** | Duplicate parameters |
| 7 | **Open Redirect — Low Impact** | Redirects users to an untrusted destination |
| 8 | **HTTP Method Allowed Unnecessarily** | PUT, DELETE, TRACE |
| 9 | **OPTIONS Reveals Methods** | HTTP methods disclosed through OPTIONS |
| 10 | **Improper Input Validation** | Numeric, email, length validation |

## 6. File Upload & Application Configuration

| # | Vulnerability | Description |
|---|---|---|
| 1 | **No File Upload Size Limit** | Large files can be uploaded |
| 2 | **Publicly Accessible Upload Directory** | Uploaded files accessible publicly |
| 3 | **Outdated Library** | jQuery, Bootstrap, etc. |
| 4 | **Backup Files Exposed** | `.bak`, `.old`, `.zip` |
| 5 | **Directory Listing Enabled** | Directory contents exposed |

---

# 🟢 LOW — Present Almost Always (Still Report)

| # | Vulnerability | Description |
|---|---|---|
| 1 | **X-Powered-By Header Present** | Technology information disclosed |
| 2 | **Server Header Verbose** | Detailed server information exposed |
| 3 | **Framework Version in Response** | Framework version disclosed |
| 4 | **robots.txt Discloses Paths** | Internal or sensitive paths listed |
| 5 | **sitemap.xml Discloses Paths** | Application paths exposed |
| 6 | **.gitignore / README.md Exposed** | Development information exposed |
| 7 | **package.json / composer.json Exposed** | Application dependencies and configuration information exposed |
| 8 | **phpinfo.php Accessible** | PHP configuration information exposed |
| 9 | **Soft 404** | Returns HTTP 200 for missing pages |
| 10 | **Custom 404 Page Missing** | Default or generic error page displayed |
| 11 | **X-XSS-Protection Missing (Legacy)** | Legacy browser security header missing |
| 12 | **X-Permitted-Cross-Domain-Policies Missing** | Cross-domain policy header missing |
| 13 | **COOP / COEP / CORP Missing** | Cross-origin isolation-related headers missing |
| 14 | **Retry-After Missing on 429** | Retry timing not provided after rate limiting |
| 15 | **Vary Header Missing on Cached Content** | Cache variation rules not specified |
| 16 | **Third-Party Script Without SRI** | External scripts loaded without Subresource Integrity |
| 17 | **target="_blank" Without rel="noopener"** | Potential opener access from the opened page |
| 18 | **Unminified JS / CSS in Production** | Unminified frontend files exposed |
| 19 | **console.log in Production JS** | Debug information left in production JavaScript |
| 20 | **Email Spoofing Possible** | SPF/DMARC misconfigured |

---

# 📌 THE "ALWAYS CHECK" TOP 20

> **If you remember nothing else, write these 20 in the front of your book. They cover 80% of real findings.**

| # | Vulnerability | What to Check |
|---|---|---|
| 1 | **IDOR** | Change IDs |
| 2 | **Broken Access Control** | Access admin functions as a normal user |
| 3 | **SQL Injection** | Quote in input |
| 4 | **Stored XSS** | Script in a saved field |
| 5 | **Reflected XSS** | Script in URL parameter |
| 6 | **CSRF** | Transfer without token |
| 7 | **JWT Tampering** | `role:admin`, `alg:none` |
| 8 | **Mass Assignment** | Add `role:admin` |
| 9 | **Business Logic** | Negative amount, replay |
| 10 | **Race Condition** | Parallel requests |
| 11 | **OTP Bypass** | Null, reuse, skip step |
| 12 | **Host Header Injection** | Password reset |
| 13 | **SSRF** | URL feature → Collaborator |
| 14 | **XXE** | XML/SAML/SVG upload |
| 15 | **Open Redirect** | `?redirect=evil.com` |
| 16 | **Account Enumeration** | Different error messages |
| 17 | **Rate Limit Missing** | Login/OTP brute force |
| 18 | **Sensitive Data Leak** | Hash/CVV in response |
| 19 | **File Upload RCE** | `shell.php` |
| 20 | **Cookie Flags + Headers** | 5-minute passive win |

---

# 🎯 THE "NEVER MISS" 5 — Banking / Finance Applications

> **If the application is banking or finance, these 5 checks should cover your entire first hour of testing.**

| # | Vulnerability | What to Check |
|---|---|---|
| 1 | **IDOR** | Account/transaction/card/statement IDs |
| 2 | **Business Logic Flaws** | Negative amount + transaction replay |
| 3 | **Race Condition** | Parallel transfer/withdrawal requests |
| 4 | **OTP Bypass** | Null, reuse, endpoint skip |
| 5 | **Host Header Injection** | Password reset |

**Important:** If you find even one of these five, investigate its actual impact and assign severity based on the demonstrated risk. A finding does not automatically qualify as Critical.

---

# 📊 REALITY CHECK — What Actually Shows Up

The following table represents approximate occurrence estimates from the original checklist. These are indicative figures, not independently verified industry-wide statistics.

| Category | % of Apps Affected |
|---|---:|
| Missing Security Headers / Cookie Flags | ~95% |
| Broken Access Control (IDOR/BFLA) | ~70% |
| XSS (Reflected or Stored) | ~60% |
| Business Logic Flaws | ~55% |
| Account Enumeration | ~50% |
| Rate Limiting Missing | ~45% |
| SQL Injection | ~30% |
| CSRF on Sensitive Action | ~30% |
| JWT Issues | ~25% |
| Open Redirect | ~20% |
| SSRF | ~15% |
| Command Injection / RCE | ~10% |
| XXE | ~10% |
| Deserialization | ~5% |

## ⏱️ Time Allocation During VAPT

**Read this table before every test.**

It tells you where to spend your time:

- **Top 5 rows:** 250 minutes of your 4:30-hour testing window.
- **Bottom 4 rows:** 20 minutes maximum, only if you spot the relevant feature.

Use these estimates as a prioritization guide, not as a fixed testing rule. Always adapt based on the application's functionality, attack surface, and findings.

---

# ✅ Final VAPT Testing Reminder

- [ ] Test authentication and authorization.
- [ ] Check IDOR and Broken Access Control.
- [ ] Test all user-controlled inputs for injection.
- [ ] Check business logic and transaction workflows.
- [ ] Test session management and cookie security.
- [ ] Check JWT implementation and token validation.
- [ ] Test file upload functionality.
- [ ] Review API endpoints and HTTP methods.
- [ ] Check security headers and TLS configuration.
- [ ] Look for sensitive information disclosure.
- [ ] Check rate limiting and account lockout.
- [ ] Review exposed files, directories, and debug endpoints.
- [ ] Test OTP and 2FA implementation.
- [ ] Check password reset and account recovery functionality.
- [ ] Document evidence, impact, severity, and remediation for every confirmed finding.

---

**Remember:** Don't just identify a vulnerability. Prove its impact, capture proper evidence, understand the root cause, and provide a practical remediation.

*Happy Hacking! 🔐*


