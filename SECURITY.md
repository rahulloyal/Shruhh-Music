# Security Policy

## Reporting a Vulnerability

If you discover a security vulnerability within Shruhh Music, please report it responsibly.

**Do NOT open a public issue for security vulnerabilities.**

Instead, please reach out privately via:

- **LinkedIn**: [Rahul Loyal Dalmas](https://www.linkedin.com/in/rahul-loyal-dalmas-5baa4532b/)
- **Instagram**: [@rahul_.loyal](https://www.instagram.com/rahul_.loyal/)

## Security Measures

Shruhh Music implements the following security measures:

- **Content Security Policy (CSP)** — Strict CSP headers to prevent XSS and injection attacks
- **X-Frame-Options: DENY** — Prevents clickjacking
- **X-Content-Type-Options: nosniff** — Prevents MIME-type sniffing
- **Referrer Policy** — `strict-origin-when-cross-origin`
- **Permissions Policy** — Camera, microphone, and geolocation disabled by default
- **Local-First Data** — User data (playlists, history, preferences) is stored locally on-device
- **HTTPS Enforcement** — All network requests use HTTPS with upgrade-insecure-requests

## Supported Versions

| Version | Supported |
|:---:|:---:|
| 1.0.x | ✅ |
| < 1.0 | ❌ |

---

*Powered by Shruhh.Inc*
