# Testing Methodology

## Environment Setup

- **Platform:** Kali Linux VM
- **Proxy Tool:** Burp Suite Community Edition
- **Browser:** Embedded Chromium/Firefox
- **Target:** testfire.net (deliberately vulnerable banking demo)

## Testing Process (11 Steps)

1. Configured Burp Suite proxy on 127.0.0.1:8080
2. Added testfire.net to Burp scope
3. Browsed anonymously, then authenticated with test credentials (jsmith)
4. Crawled all functional areas (Accounts, Transactions, Transfers, Search, Preferences, Logout)
5. Captured complete login request-response cycle
6. Decoded application cookie (AltoroAccounts) using Base64
7. Audited cookies for Secure, HttpOnly, SameSite flags
8. Catalogued response headers on authenticated pages
9. Mapped full data flow and client-controlled inputs
10. Ran Burp Sequencer on captured cookies
11. Compared authenticated vs anonymous responses using Burp Comparer

## Tools Used

| Tool | Purpose |
|------|---------|
| Burp Suite Community | Proxy, Repeater, Sequencer, Decoder, Comparer |
| Firefox DevTools | Client-side cookie verification |
| Kali Linux | Testing platform |
