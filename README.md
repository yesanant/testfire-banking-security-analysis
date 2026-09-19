# TestFire Banking Application Security Analysis
Web application security assessment of testfire.net banking demo. Analyzed traffic, cookies, headers, identified 8 vulnerabilities with remediation roadmap. Educational purpose only.

![Security](https://img.shields.io/badge/Security-Web_Application_Assessment-blue)
![Status](https://img.shields.io/badge/Status-Complete-success)

## Overview

Traffic analysis and security assessment of testfire.net banking demo. Identified 8 security vulnerabilities with remediation recommendations.

## Tools

- Burp Suite Community Edition
- Kali Linux VM
- Firefox DevTools

## Key Findings

| Finding | Issue | Risk |
|---------|-------|------|
| F1 | Account data in Base64 cookie | High |
| F2 | Missing cookie security flags | High |
| F4 | No security headers | Medium |
| F6 | Client-controlled account refs | High |

## Documentation

- [Methodology](./methodology.md)
- [Findings](./findings.md)
- [Mitigations](./mitigations.md)
- [Evidence](./evidence/)
