# Detailed Vulnerability Findings

## Executive Summary

8 security weaknesses identified in testfire.net banking application. 3 classified as High risk, 2 as Medium, 1 as Low.

---

## Findings

### 🔴 High Severity

| Finding | Issue | Impact |
|---------|-------|--------|
| **F1** | Account number stored in Base64 cookie | Session fixation / XSS data theft |
| **F2/F3** | Missing Secure, HttpOnly, SameSite flags | Cookie hijacking over HTTP or XSS |
| **F6** | Client-controlled account references | IDOR vulnerability (unauthorized access) |

### 🟠 Medium Severity

| Finding | Issue | Impact |
|---------|-------|--------|
| **F4** | No security headers (HSTS, CSP, etc.) | Clickjacking, XSS, cache leaks |
| **F7** | Predictable session token structure | Token prediction attacks |

### 🟡 Low Severity

| Finding | Issue | Impact |
|---------|-------|--------|
| **F5** | Server banner reveals Tomcat version | Enables targeted exploitation |

---

## Risk Level Summary

| Finding | Risk Level |
|---------|------------|
| F6 (IDOR candidate) | High |
| F1 (Account data in cookie) | High |
| F2/F3 (Missing cookie flags) | High |
| F4 (Missing security headers) | Medium |
| F7 (Weak token structure) | Medium |
| F5 (Server disclosure) | Low |
