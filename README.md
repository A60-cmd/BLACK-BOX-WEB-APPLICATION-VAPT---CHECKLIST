# BLACK-BOX-WEB-APPLICATION-VAPT---CHECKLIST



-------------------------------------------------------------------------------------------------------------------
LARGER CHECKLIST FOR REFERENCE 

🔴 CRITICAL
SQL Injection (Authentication Bypass)

SQL Injection (UNION-Based Data Extraction)

SQL Injection (Error-Based)

SQL Injection (Blind Boolean)

SQL Injection (Blind Time-Based)

SQL Injection (Second-Order)

SQL Injection (Stacked Queries)

SQL Injection in ORDER BY / LIMIT clause

NoSQL Injection (Authentication Bypass)

NoSQL Injection (Operator Injection $ne, $gt, $regex, $where)

Command Injection (In-Band)

Command Injection (Blind / OOB)

Remote Code Execution (RCE)

Insecure Deserialization (Java)

Insecure Deserialization (PHP Object Injection)

Insecure Deserialization (.NET)

Insecure Deserialization (Python Pickle)

Insecure Deserialization (Ruby Marshal)

Insecure Deserialization (Node.js)

Authentication Bypass (Logic Flaw)

Authentication Bypass (JWT alg:none)

Authentication Bypass (JWT Algorithm Confusion RS256→HS256)

Authentication Bypass (JWT kid Injection — SQLi)

Authentication Bypass (JWT kid Injection — LFI)

Authentication Bypass (JWT jku/x5u Hijack)

JWT Weak Secret (Offline Crack)

JWT Claim Tampering (role, is_admin, sub, user_id)

JWT No Signature Verification

JWT No Expiration

JWT Not Invalidated After Logout

IDOR — Account Data

IDOR — Transaction Data

IDOR — Card Data (CVV/PAN)

IDOR — Statement / Document Download

IDOR — KYC Documents

IDOR — Beneficiary Data

IDOR — Loan Records

IDOR — Chat / Support Tickets

IDOR — Admin Functions

IDOR — File Uploads / Attachments

BOLA (Broken Object Level Authorization) — API

BFLA (Broken Function Level Authorization) — API

Mass Assignment — Role Escalation

Mass Assignment — Balance Manipulation

Mass Assignment — is_verified / kyc_status / is_admin

Privilege Escalation — Vertical (User → Admin)

Privilege Escalation — Horizontal (User A → User B)

Negative Amount Transfer

Zero Amount Transaction

Fractional / Decimal Rounding Abuse

Integer Overflow / Underflow in Amount

Transaction Replay (Missing Idempotency)

Race Condition — Double Spend

Race Condition — OTP Brute via Parallel

Race Condition — Coupon / Cashback

Race Condition — Limit Bypass

Workflow Bypass — Skip OTP Step

Workflow Bypass — Skip KYC Step

Workflow Bypass — Skip PIN / MPIN

Workflow Bypass — Direct API Call to Final Step

OTP Bypass — Null / Empty / $ne

OTP Bypass — Brute Force (No Rate Limit)

OTP Bypass — Reuse Same OTP

OTP Bypass — OTP Leaked in Response

OTP Bypass — OTP Sent to Attacker's Number (IDOR on mobile)

OTP Bypass — No OTP Verification on Server

MPIN / Transaction PIN Bypass

Password Reset — Host Header Poisoning

Password Reset — Token Predictable

Password Reset — Token Not Expiring

Password Reset — Token Leaked in Response / Referer

Password Reset — Token Reuse

Password Reset — User IDOR (Reset Other User's Password)

XXE — In-Band File Read

XXE — SSRF via XXE

XXE — Blind OOB

XXE — Error-Based

XXE — SVG Upload

XXE — DOCX / XLSX Upload

XXE — SAML Assertion

XXE — SOAP Endpoint

SSRF — Internal Service Access

SSRF — Cloud Metadata (AWS)

SSRF — Cloud Metadata (GCP)

SSRF — Cloud Metadata (Azure)

SSRF — Blind (Collaborator)

SSRF — Protocol Smuggling (gopher, dict, file)

SSRF — DNS Rebinding

SSTI — Jinja2 (RCE)

SSTI — Twig (RCE)

SSTI — Freemarker (RCE)

SSTI — Velocity (RCE)

SSTI — Smarty (RCE)

SSTI — ERB (RCE)

LFI → RCE via Log Poisoning

LFI → RCE via /proc/self/environ

LFI → RCE via PHP data:// Wrapper

LFI → RCE via PHP input:// Wrapper

LFI → RCE via PHP Session File

Unrestricted File Upload → Web Shell

File Upload — Extension Bypass

File Upload — MIME Bypass

File Upload — Magic Byte Bypass

File Upload — Filename Path Traversal

File Upload — Content-Type Bypass

File Upload — .htaccess Upload

File Upload — SVG Stored XSS

File Upload — Zip Slip

File Upload — Zip Bomb / DoS

LDAP Injection (Auth Bypass)

XPath Injection (Auth Bypass)

Expression Language Injection (Spring EL)

Server-Side JavaScript Injection (Node)

GraphQL — Introspection Enabled + Sensitive Schema

GraphQL — Batching Attack (Brute Force)

GraphQL — Deep Query / Nested Query DoS

GraphQL — Field Suggestion Leak

GraphQL — IDOR via Node ID

GraphQL — Mutation Authorization Bypass

Spring Boot Actuator — /env, /heapdump, /threaddump Exposed

Spring Boot Actuator — /jolokia RCE

Spring4Shell / Log4Shell / Specific Framework RCE

Struts2 RCE (S2-045, S2-057)

Java RMI / JMX Exposed

Docker API Exposed (:2375, :2376)

Kubernetes API Exposed

Redis Unauthenticated Access

MongoDB Unauthenticated Access

Elasticsearch Unauthenticated Access

Memcached Unauthenticated Access

Jenkins Unauthenticated RCE

Exposed .git → Source Code Recovery → Secrets

Exposed .env → DB Credentials / API Keys

Exposed wp-config.php / config.php

Exposed AWS / GCP / Azure Keys in JS

Hardcoded Credentials in Mobile APK / JS Bundle

Hardcoded JWT Secret

Default Credentials (admin/admin)

Weak Admin Credentials

Complete Account Takeover via Any Chain

🟠 HIGH
Stored XSS — Admin Panel

Stored XSS — Beneficiary Name

Stored XSS — Transaction Remarks

Stored XSS — Support Ticket

Stored XSS — Profile Fields

Stored XSS — File Name / Upload

Stored XSS — PDF / Statement Content

Reflected XSS — Authenticated

Reflected XSS — Unauthenticated

DOM XSS — innerHTML

DOM XSS — document.write

DOM XSS — eval / setTimeout

DOM XSS — location.hash

DOM XSS — window.name

DOM XSS — postMessage Handler

Blind XSS (OOB Callback)

XSS via Markdown / Rich Text Editor

XSS via SVG Upload

XSS via File Upload (HTML)

XSS Filter Bypass — Tag Blacklist

XSS Filter Bypass — Event Handler Blacklist

XSS Filter Bypass — Encoding

XSS → Cookie Theft

XSS → JWT Token Theft (localStorage)

XSS → Session Hijack

XSS → Force Transfer / CSRF Chain

XSS → Keylogger

XSS → Full Account Takeover

CSRF — Fund Transfer

CSRF — Email Change

CSRF — Password Change

CSRF — Add Beneficiary

CSRF — Card Block / Unblock

CSRF — Logout

CSRF — JSON Endpoint (Content-Type Bypass)

CSRF — Token Reuse / Static Token

CSRF — Token Not Tied to User

CSRF — Token Not Validated Server-Side

CSRF — SameSite=None Without Secure

SSRF — Basic (Any Form)

SSRF — Localhost Access

SSRF — Internal Port Scan

SSRF — Blacklist Bypass (Decimal/Hex/Octal IP)

SSRF — Redirect Chain Bypass

SSRF — Open Redirect Chain

SSTI — Non-RCE Confirmation ({{7*7}})

Command Injection — Confirmed (Blind)

SQLi — Detected but Not Exploited (Any Type)

NoSQLi — Confirmed

LDAP Injection — Confirmed

Path Traversal — /etc/passwd Read

Path Traversal — Windows win.ini Read

Path Traversal — Config File Read

LFI — Source Code Disclosure

LFI — Log File Read

Arbitrary File Read

Arbitrary File Write

Unrestricted File Upload — Any Executable

Insecure Deserialization — Confirmed (No RCE)

Broken Access Control — Vertical (Missing Auth on Admin Endpoint)

Broken Access Control — Horizontal (Any IDOR)

Forced Browsing — Admin Panel Access

Missing Function-Level Access Control on API

HTTP Method Bypass (POST on GET-only endpoint)

HTTP Method Override Header (X-HTTP-Method-Override)

Header Bypass — X-Original-URL / X-Rewrite-URL

Header Bypass — X-Forwarded-For: 127.0.0.1

Header Bypass — X-Custom-IP-Authorization

Host Header Injection

Host Header Injection — Cache Poisoning

Cache Poisoning — Web Cache Deception

Cache Poisoning — XSS via Header

Open Redirect — ?redirect=

Open Redirect — ?next= / ?return= / ?url=

Open Redirect — @ Trick / \\ Trick

Open Redirect — javascript: URI

Open Redirect — Chained to OAuth Token Theft

OAuth — redirect_uri Bypass

OAuth — CSRF (Missing state)

OAuth — Token Leakage in Referer

OAuth — Implicit Flow Token in Fragment

SAML — XML Signature Wrapping (XSW)

SAML — Comment Injection

SAML — XXE

SAML — No Signature Validation

SAML — Replay Attack

CORS Misconfiguration — Access-Control-Allow-Origin: * + Credentials

CORS — Origin Reflection

CORS — null Origin Allowed

CORS — Subdomain Wildcard Trust

CORS — Pre-Domain Bypass (bank.com.evil.com)

Sensitive Data in JWT Payload (PII, PAN)

Sensitive Data in URL Query String

Sensitive Data in Referer Header

Sensitive Data in Browser localStorage

Sensitive Data in Response Body (Password Hash, CVV, PAN)

Sensitive Data in API Over-Fetching

Excessive Data Exposure in API

PII Leakage via API Enumeration

Account Enumeration — Login

Account Enumeration — Registration

Account Enumeration — Password Reset

Account Enumeration — Timing-Based

No Rate Limiting on Login

No Rate Limiting on OTP

No Rate Limiting on Password Reset

No Rate Limiting on Transfer API

No Account Lockout

Weak Password Policy

Password in Plaintext Over HTTP

Credentials in URL

Credentials in Logs

Session Fixation

Session Not Rotated After Login

Session Not Invalidated on Logout

Session Not Invalidated on Password Change

Session Token in URL

Predictable Session Token

Concurrent Sessions Unlimited

Session Timeout Too Long / Missing

Cookie HttpOnly Missing on Session Cookie

Cookie Secure Missing on Session Cookie

Cookie SameSite Missing / None Without Secure

Cookie Scope Too Broad (Domain)

Cookie Path Too Broad

Cookie Prefix Missing (__Host-, __Secure-)

2FA Not Enforced on Admin

2FA Bypass via Response Manipulation

2FA Bypass via Endpoint Skip

2FA Bypass via Backup Code Brute

2FA Bypass via OTP Reuse

Weak OTP — 4 Digits, No Expiry

MFA Fatigue / Push Bombing

Password Reset Token Weak Entropy

Password Reset Token in URL (Leaks via Referer)

Password Change Without Current Password

Email Change Without Verification

Phone Number Change Without Verification

Security Question Weakness

Remember Me Token Predictable / No Expiry

API Key Exposed in Client-Side Code

API Key in JS Bundle

API Key in Mobile APK

API Key in HTML Comments

Exposed Swagger / OpenAPI (Detailed)

Exposed GraphQL Playground

Exposed Admin Panel (No Auth)

Exposed Debug Endpoint

Exposed Staging / Dev Environment

Exposed Test / Debug Backdoor

Verbose Error — Stack Trace (Full)

Verbose Error — SQL Error Message

Verbose Error — Internal Path Disclosure

Verbose Error — Framework Version

Verbose Error — DB Version

Source Code Disclosure via Backup (.zip, .tar.gz, .bak, .old, .swp)

Source Map Exposed (.map)

.git/ Directory Exposed

.svn/ Directory Exposed

.DS_Store Exposed

.env Exposed

.idea/ / .vscode/ Exposed

Unauthenticated Access to Sensitive API

WebSocket — No Auth

WebSocket — CSRF (Cross-Site WebSocket Hijacking)

WebSocket — Message Injection

WebSocket — Sensitive Data Leakage

HTTP Request Smuggling (CL.TE)

HTTP Request Smuggling (TE.CL)

HTTP Request Smuggling (TE.TE)

HTTP/2 Downgrade Smuggling

CRLF Injection → Header Injection

CRLF Injection → Response Splitting

CRLF Injection → XSS

Email Header Injection

SMTP Injection

XML Bomb (Billion Laughs)

XML Quadratic Blowup

Zip Slip

Zip Bomb

CSV Injection (Formula Injection)

Log Injection

Server-Side Prototype Pollution

Client-Side Prototype Pollution → DOM XSS

Insecure Randomness (Predictable Tokens)

Time-Based Token Prediction

IDOR via HTTP Parameter Pollution

Parameter Pollution — WAF Bypass

Parameter Pollution — Logic Bypass

HTTP Desync

Missing Authorization on Internal API

Mobile API — No Certificate Pinning

Mobile API — Hardcoded Secrets

Mobile API — Insecure Deep Link

Mobile API — Exported Components

Mobile API — Backup Enabled

Mobile API — Debug Mode Enabled

🟡 MEDIUM
Reflected XSS — Non-Authenticated, Low Impact

DOM XSS — Low-Impact Sink

Self-XSS (Requires User Action)

XSS — Content-Security-Policy Missing (Increases Impact)

CSRF — Low-Impact Action (Logout, Newsletter)

CSRF — Token Present but Not Validated

SSRF — DNS-Only Confirmation (No Response)

SSRF — No Cloud Metadata Access

Open Redirect — Confirmed, Not Chained

Open Redirect — 302 Only, No Auth Flow

Clickjacking — No X-Frame-Options

Clickjacking — No CSP frame-ancestors

Clickjacking — Confirmed on Sensitive Page

Tabnabbing (target="_blank" Without rel="noopener")

Reverse Tabnabbing

Missing X-Content-Type-Options: nosniff

Missing Strict-Transport-Security (HSTS)

HSTS — Short max-age

HSTS — Missing includeSubDomains

HSTS — Missing preload

Missing Content-Security-Policy

CSP — Weak Policy (unsafe-inline, unsafe-eval)

CSP — Wildcard *

CSP — Report-Only Mode

Missing Referrer-Policy

Referrer-Policy: unsafe-url

Missing Permissions-Policy

Missing X-Frame-Options

Missing X-XSS-Protection (legacy)

Missing X-Permitted-Cross-Domain-Policies

Missing Cross-Origin-Opener-Policy (COOP)

Missing Cross-Origin-Embedder-Policy (COEP)

Missing Cross-Origin-Resource-Policy (CORP)

Missing Cache-Control: no-store on Sensitive Pages

Missing Pragma: no-cache

Sensitive Page Cached by Browser

Sensitive Page Cached by CDN

Cache Deception (Appended Extension)

HTTP Server Banner Disclosure

Framework Version Disclosure

CMS Version Disclosure

Language Version Disclosure (PHP, ASP.NET)

X-Powered-By Disclosure

Server Header Verbose

X-AspNet-Version Disclosure

X-Generator Disclosure

HTML Comments Disclose Paths

HTML Comments Disclose Credentials / Tokens

HTML Comments Disclose TODO / FIXME / BUG

JS File Discloses Internal Endpoints

JS File Discloses API Keys

JS File Discloses Feature Flags

JS Source Map Exposed

Directory Listing Enabled

Directory Listing — Sensitive Files

Backup File Exposed — .bak

Backup File Exposed — .old

Backup File Exposed — .swp

Backup File Exposed — .zip / .tar.gz

Editor Config Exposed — .vscode/, .idea/

.git/config Exposed

.git/HEAD Exposed

robots.txt Discloses Sensitive Paths

sitemap.xml Discloses Admin Paths

security.txt Discloses Contacts (Info)

crossdomain.xml Overly Permissive

clientaccesspolicy.xml Overly Permissive

OPTIONS Method Enabled

TRACE Method Enabled

PUT / DELETE Method Enabled

WebDAV Enabled

HTTP Allowed (No HTTPS Redirect)

HTTP→HTTPS Redirect After Data Sent

Mixed Content (HTTP Resources on HTTPS)

Weak TLS — TLS 1.0 / 1.1 Enabled

Weak TLS — SSLv3 Enabled

Weak Cipher Suite — RC4, DES, 3DES, NULL

Certificate Expired

Certificate Self-Signed

Certificate Hostname Mismatch

Certificate Weak Signature (MD5, SHA1)

TLS Compression Enabled (CRIME)

Renegotiation Enabled

Heartbleed (CVE-2014-0160) — Rare

Weak SSH Algorithms (if exposed)

Insecure SMTP (No TLS)

No SPF Record

No DMARC Record

No DKIM

Weak SPF — +all

Weak DMARC — p=none

Email Spoofing Possible

Host Header Injection — Reflected Only (No Impact)

Host Header Used for Cache Key (Potential)

X-Forwarded-Host Trusted Without Validation

Missing Content-Type Validation

Missing Accept Header Validation

Missing Origin Validation

Origin Check Bypass — Null Origin

Origin Check Bypass — Subdomain Wildcard

Username Enumeration — Timing Only

Weak CAPTCHA Implementation

CAPTCHA Bypass — Reusable Token

CAPTCHA Bypass — Server-Side Not Enforced

CAPTCHA Bypass — Client-Side Only

CAPTCHA Bypass — OCR-Solvable

No CAPTCHA on Login

No CAPTCHA on Registration

No CAPTCHA on Password Reset

No CAPTCHA on Contact Form

Rate Limit — Bypass via X-Forwarded-For

Rate Limit — Bypass via Case Change

Rate Limit — Bypass via Whitespace

Rate Limit — Bypass via Parameter Pollution

Rate Limit — Bypass via Path Traversal

Rate Limit — IP-Based Only (VPN Bypass)

Rate Limit — Account-Based Only (Username Enum)

Password Autocomplete Enabled

Password Field in URL

Password Field Not Masked

Password Complexity Weak (< 8 chars)

No Password History Check

No Password Expiry (Debatable)

Password Change Without Current Password Verification

Email Change Without Re-Authentication

Sensitive Action Without Re-Authentication

Sensitive Action Without MFA Step-Up

Improper Error Message (Reveals Logic)

Improper Error Message (Reveals Internal State)

Insecure Direct File Reference (Low-Sensitivity)

Sequential Order Number in URL

Sequential Invoice / Transaction ID

Predictable Token — Numeric

Predictable Token — Timestamp-Based

Predictable Token — MD5 of Known Value

UUID v1 (Timestamp-Based) Predictable

Insecure Random Number Generator (Weak PRNG)

Logout — Not Available

Logout — Only Client-Side (Cookie Not Cleared)

Logout — GET Request (CSRF-able)

Unnecessary Redirect Chain

Redirect to HTTP from HTTPS

Redirect to External Domain (Non-Open-Redirect)

Parameter Pollution — Accepts Duplicate Params

HTTP 500 on Malformed Input

Missing Input Validation — Numeric Fields

Missing Input Validation — Email Format

Missing Input Validation — Phone Format

Missing Input Length Limit

No Maximum Length on Text Fields (DoS)

File Upload — No Size Limit

File Upload — No Type Restriction (Low-Impact)

File Upload — MIME Type Trust

File Upload — Publicly Accessible Directory

File Upload — Predictable Filename

File Upload — Same-Origin Uploads Served

Insecure External Resource Loading (HTTP)

Subresource Integrity (SRI) Missing

Third-Party Script Without Review

Third-Party Cookie Set Without Notice

Tracking Without Consent

Outdated jQuery

Outdated Bootstrap

Outdated Angular / React / Vue

Outdated PHP / ASP.NET / Tomcat

Outdated nginx / Apache / IIS

Vulnerable JS Library (Known CVE)

Vulnerable Server Component (Known CVE)

Vulnerable WordPress Plugin

Vulnerable Drupal Module

Unnecessary Service Exposed (FTP, Telnet)

Port 8080 / 8443 / 9090 Open (Non-Standard)

Debug Port Exposed (9229, 5005, 5858)

phpMyAdmin Exposed

Adminer Exposed

Server-Status / Server-Info Enabled

/actuator Exposed (Non-Critical Endpoints)

/health / /info Reveals Details

/metrics Prometheus Exposed

/swagger-ui Without Auth

/api-docs Without Auth

/graphql Playground Enabled in Prod

wp-json/wp/v2/users Exposed (WP User Enum)

xmlrpc.php Enabled (Brute Force)

admin-ajax.php Unauthenticated Action

setup.php / install.php Accessible

test.php / phpinfo.php Exposed

.htaccess Accessible

web.config Accessible

IIS Short Name (8.3) Disclosure

🟢 LOW
Cookie HttpOnly Missing (Non-Session)

Cookie Secure Missing (Non-Session)

Cookie SameSite Missing (Non-Session)

Cookie Prefix (__Host- / __Secure-) Missing on Session

Cookie Set Without Expires / Max-Age

Cookie Set With Very Long Max-Age

Cookie Set on Parent Domain (.bank.com)

Cookie Scope Broader Than Necessary

Cookie Flag — Path Too Broad

X-Content-Type-Options Missing

Referrer-Policy Missing / Weak

Permissions-Policy Missing

X-XSS-Protection Missing (Legacy)

Cross-Origin-Opener-Policy Missing

Cross-Origin-Embedder-Policy Missing

Cross-Origin-Resource-Policy Missing

X-Permitted-Cross-Domain-Policies Missing

Server Banner Disclosure

X-Powered-By Disclosure

Framework Version in Header

Server Header Verbose

X-AspNet-Version Disclosure

X-AspNetMvc-Version Disclosure

X-Generator Disclosure

X-Drupal-Cache Disclosure

X-Runtime Disclosure

Via Header Discloses Proxy

X-Cache / X-Served-By Discloses CDN

Verbose Date / Age Headers

HTTP OPTIONS Enabled (Low)

TRACE Method Enabled (Low, if no impact)

Unnecessary HTTP Methods Advertised

HTTP 200 on Non-Existent Pages (Soft 404)

Missing Custom 404 Page

Missing Custom 500 Page

Directory Listing (Non-Sensitive)

robots.txt Discloses Paths (Low)

sitemap.xml Discloses Paths (Low)

security.txt Exposed

HTML Comments Disclose Internal Notes

HTML Comments Disclose Test Notes

HTML Comments Disclose TODO / FIXME

JS File Discloses Non-Sensitive Endpoints

JS File Discloses Feature Flags

Source Map Exposed (Non-Sensitive)

.DS_Store Exposed

.editorconfig Exposed

.gitignore Exposed

README.md Exposed

CHANGELOG.md Discloses Versions

package.json Exposed

composer.json Exposed

composer.lock Exposed

HTTP Allowed (No Sensitive Data Sent)

Redirect to External Domain (Legitimate)

Unnecessary Redirect Chain

Autocomplete Enabled on Password (Low)

Password Field Not Masked (UI)

Password Complexity Guidance Missing in UI

No Client-Side Password Strength Meter

Username Enumeration — Very Low Signal

Rate Limiting — High Threshold (Effectively None)

CAPTCHA — Weak But Present

Session Timeout — Very Long

Concurrent Sessions — Unlimited (Low)

Remember Me — No Expiry

Remember Me — Predictable Token

Logout — Client-Side Only (Cookie Not Cleared)

Logout — GET Request (No CSRF Impact)

Email Change — No Confirmation Email

Phone Change — No Confirmation SMS

Sensitive Action — No Audit Log

Missing Audit Logging

Missing Security Monitoring

No WAF Detected

WAF Detected — Version Disclosure

CDN Detected — Version Disclosure

Technology Stack Disclosure (Low)

Framework Disclosure via Error Page

Language Disclosure via Cookie (PHPSESSID, JSESSIONID, ASP.NET_SessionId)

Session Cookie Name Reveals Tech

Error Page Reveals Framework

Verbose 404 Page

Verbose 403 Page

Verbose 500 Page

Missing Retry-After on 429

Missing Vary Header on Cached Content

Caching of Non-Sensitive Content

Cache-Control: public on Authenticated Page (Low if no PII)

Expires Header in the Past (Confusing)

Mixed Content — Passive (Image over HTTP)

Insecure External Link (target="_blank" Without rel="noopener")

Referrer-Policy Missing on External Links

Third-Party Script Without SRI

Outdated Library (No Known Exploit)

jQuery < 3.5 (Info)

Bootstrap < 4 (Info)

Unnecessary JS Library Loaded

Unnecessary CSS Framework

Unminified JS in Production

Unminified CSS in Production

Debug Console Statements in Prod JS

Source Code Comment in JS

/crossdomain.xml Exists

/clientaccesspolicy.xml Exists

web.config Accessible (No Sensitive Data)

.htaccess Accessible (No Sensitive Data)

phpinfo.php — Accessible but No Auth Needed (Info)

/server-status Accessible (Apache)

/server-info Accessible (Apache)

/nginx_status Accessible

/actuator/health Exposed (Info)

/actuator/info Exposed (Info)

/metrics Exposed (Info)

/env Exposed (No Secrets)

/trace Exposed

/loggers Exposed

/heapdump Exposed (No Access) — Escalate to High if accessible

/threaddump Exposed (Info)

/jolokia Exposed (No Auth) — Escalate to Critical if RCE possible

/swagger-ui.html Exposed (Info)

/api-docs Exposed (Info)

/graphql Playground in Prod (Info)

/graphiql Playground Exposed

/playground Exposed

/altair Exposed

/health Exposed

/ready Exposed

/live Exposed

/version Exposed

/status Exposed

/ping Exposed

/debug Exposed (No Impact)

/test Accessible (No Impact)

/dev Accessible

/staging Accessible (No Auth)

/demo Accessible

/sandbox Accessible

/beta Accessible

/preview Accessible

/internal Accessible (No Auth) — Escalate if sensitive

/private Accessible (No Auth) — Escalate if sensitive

HTTP 401 vs 403 — Info Disclosure

Different Error Message — Valid vs Invalid User (Timing)

Different Response Length — Enumeration Signal

Different Response Time — Enumeration Signal

Sequential IDs in URLs (Info Disclosure)

Sequential Invoice Numbers (Info)

Sequential Ticket Numbers (Info)

Predictable Filenames in Uploads

Public Directory Listing — Uploads

Public S3 Bucket Listing

Public Azure Blob

Public GCS Bucket

Public Firebase

Firebase Rules — Read Open

Firebase Rules — Write Open (Escalate to High)

MongoDB Atlas — IP Whitelist Missing (Info)

Port 22 Open to Public (Info)

Port 3306 Open to Public (Info)

Port 5432 Open to Public (Info)

Port 6379 Open to Public (Info)

Port 27017 Open to Public (Info)

Port 9200 Open to Public (Info)

FTP Open (Anonymous) (Escalate if writable)

SMTP Open Relay (Escalate to High)

DNS Zone Transfer Allowed (Info)

Missing SPF (Info)

Missing DMARC (Info)

SPF ~all (Soft Fail)

DMARC p=none

Email Spoofing (Info)

TLS 1.2 Only — Fine

Certificate Near Expiry (Info)

Certificate Wildcard (Info)

Certificate CT Logs Reveal Subdomains

Subdomain Enumeration via CT Logs

Subdomain Takeover (Escalate to High if confirmed)

Dangling CNAME

Dangling A Record

S3 Bucket Takeover

GitHub Repo Leak (Info)

Pastebin Leak (Info)

JS File — Non-Sensitive Comments

JS File — Non-Sensitive console.log

HTML — Non-Sensitive Comments

HTML — Non-Sensitive Hidden Field

HTML — Version Disclosure

HTML — Author Meta Tag

HTML — Generator Meta Tag

⚪ INFORMATIONAL / RECON
Server IP Disclosure

Real IP Behind CDN (Revealed)

Origin IP via DNS History

Subdomain Enumeration

Virtual Host Enumeration

Cloud Provider Identification

WAF Fingerprint

CDN Fingerprint

Framework Fingerprint

Language Fingerprint

CMS Fingerprint

JavaScript Library Fingerprint

Analytics ID Disclosure

Google Maps API Key (Client-Side)

reCAPTCHA Site Key

Stripe Publishable Key

PayPal Client ID

OAuth Client ID

Firebase Config Disclosure

Sentry DSN Disclosure

Segment Write Key

Mixpanel Token

Hotjar ID

Intercom App ID

Third-Party Integrations Listed

Email Provider Revealed

Password Manager Presence

Web Server Version

OS Fingerprint

TLS Certificate Fingerprint

DNS Records Disclosure

MX Records Disclosure

TXT Records — SPF / DMARC / DKIM

NS Records Disclosure

CAA Record Missing

DNSSEC Disabled

Reverse DNS Reveals Hosting

Favicon Hash (Fingerprint)

Response Header Order (Fingerprint)

HTTP/2 Support (Info)

📌 RAPID TRIAGE — What to Touch First When Time Is Short
If you only have 30 min on a new app, hit these 10 in order:

IDOR on any ?id= / ?account= (Critical)

Negative amount in transfer (Critical)

' in login / search (SQLi — Critical)

Transaction replay in Repeater (Critical)

<script>alert(1)</script> in every input (XSS — High)

Forced browse /admin, /api/admin (High)

Host header injection on password reset (High)

X-Forwarded-Host: COLLAB on any URL-accepting feature (SSRF — High)

Cookie flags + headers snapshot (Low-Medium — 5 min, guaranteed findings)

JWT alg:none if JWT present (High)

Legend for your workflow: 🔴 Critical = stop everything, confirm immediately · 🟠 High = prioritize this phase · 🟡 Medium = batch with others · 🟢 Low = fill gaps · ⚪ Info = passive observation only.

