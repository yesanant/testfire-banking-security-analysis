# Security Mitigations

## Critical Fixes

| Finding | Fix | Priority |
|---------|-----|----------|
| F1 | Store account context server-side; issue opaque session ID | Immediate |
| F2 | Set Secure; HttpOnly; SameSite=Lax on all cookies | Immediate |
| F6 | Enforce server-side authorization on every object reference | Immediate |

## Recommended Fixes

| Finding | Fix | Priority |
|---------|-----|----------|
| F4 | Enable HSTS, CSP, X-Frame-Options: DENY, nosniff | High |
| F5 | Suppress Server banner and HTML comments | Medium |
| F7 | Complete JSESSIONID entropy analysis; improve token randomness | Medium |

## General Best Practices

1. Redirect all HTTP → HTTPS
2. Implement Referrer-Policy header
3. Add Cache-Control: no-store on authenticated pages
4. Use random, unpredictable session tokens
5. Validate all client-supplied parameters server-side
