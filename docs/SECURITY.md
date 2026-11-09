# Security

How the platform protects its users and data. Implementation specifics that would
help an attacker are intentionally omitted.

## Authentication

- Staff and customers sign in with email and password; passwords are hashed with a modern adaptive algorithm.
- **Two-factor authentication** (TOTP, RFC 6238) with one-time recovery codes for staff accounts.
- **Brute-force protection:** rate limiting per client and per account, plus temporary account lockout after repeated failures.
- Sessions use HTTP-only, `Secure`, `SameSite` cookies; session IDs rotate on login.
- Password reset tokens are single-use, short-lived and stored hashed.

## Authorization

- Role-based access control with fine-grained permissions on every admin endpoint; deny by default.
- Customer and staff areas use separate authentication guards.

## Input, output and files

- All database access uses parameterized queries / ORM bindings.
- Request validation at the API edge; rich text is sanitized with an allow-list before rendering.
- Server-rendered metadata is HTML-escaped; structured data is encoded so content cannot break out of its script element.
- Uploads are validated by their real content type and size, renamed server-side, and stored where scripts cannot execute. Personal documents (e.g. CVs) are only available to authorized staff through audited downloads.

## Transport and browser hardening

- HTTPS everywhere with HSTS.
- `X-Content-Type-Options`, `X-Frame-Options` / `frame-ancestors`, `Referrer-Policy`, `Permissions-Policy` on every response; strict Content Security Policy on the API.
- The offline cache (service worker) stores only public content — never authenticated or paid content.

## Operations

- Production never exposes debug output or stack traces.
- Secrets live only in server environment files; none in the repository or the browser bundle.
- Automated CI: tests, dependency vulnerability audits and secret scanning on every change.
- Audit log of administrative actions, logins and data exports.
- Regular backups, restricted to the highest privilege level.

## Reporting a vulnerability

Please contact us privately through <https://horooinnovations.com/contact> and ask for the
engineering team. We will acknowledge your report and keep you informed. Please don't
publicly disclose an issue before it is fixed.
