# Evidence Collection

## Overview

Sanitized screenshots from the testfire.net web application security assessment.

**All IP addresses, credentials, account numbers, and sensitive data have been redacted.**

---

## File Inventory

| File | Description | Related Finding |
|------|-------------|-----------------|
| 01_sitemap.png | Burp Suite site map with scoped target and filtered history | Methodology |
| 02_login_success.png | POST /doLogin success — 302 redirect + Set-Cookie | F1, F2, F8 |
| 03_login_failure.png | POST /doLogin failure — 302 redirect to /login.jsp | F8 |
| 04_cookie_decoder.png | Burp Decoder output — Base64 cookie reveals account number | F1, F3 |
| 05_console_cookie.png | Firefox DevTools console showing document.cookie readability | F3 |
| 06_set_cookie_flags.png | Raw Set-Cookie header showing missing security flags | F2 |
| 07_response_headers.png | main.jsp raw response headers showing absent security headers | F4, F5 |
| 08_parameter_inspection.png | listAccounts=800028 client-controlled parameter | F6 |
| 09_comparer_diff.png | Burp Comparer word-level diff — 59 differences | F8 |

---
*See [methodology.md](../methodology.md) for testing process.*  
*See [findings.md](../findings.md) for detailed analysis.*  
*See [mitigations.md](../mitigations.md) for fix recommendations.*
