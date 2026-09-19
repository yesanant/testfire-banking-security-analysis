# Secure vs Insecure Pattern Comparison

| Aspect | ✅ Best Practice | ❌ Observed on testfire.net |
|--------|-----------------|----------------------------|
| Transport | HTTPS + HSTS header | HTTPS only, no HSTS |
| Session cookies | Secure; HttpOnly; SameSite=Lax | No security flags |
| Session data storage | Server-side opaque ID | Account number in cookie |
| Sensitive payload | Encrypted or never sent | Account number Base64-decodable |
| Security headers | HSTS, CSP, X-Frame-Options, nosniff | All absent |
| Server identity | Generic/no banner | Apache-Coyote/1.1 disclosed |
| Authorization | Server validates every object ref | Client controls account IDs |
| Failed login | Generic response | Distinguishable redirect pattern |
