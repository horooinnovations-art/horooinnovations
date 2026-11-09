# HOROO Innovations — Platform Architecture

Public architecture overview of the platform behind
[horooinnovations.com](https://horooinnovations.com), built and operated by
**HOROO INNOVATION PLC** (Shashemene, Oromia, Ethiopia).

This repository contains **documentation only** — no source code, configuration
or credentials. The application source is private.

| Document | What it covers |
|---|---|
| [Architecture](docs/ARCHITECTURE.md) | System components, request flow, data model, deployment topology |
| [Security](docs/SECURITY.md) | Security model and controls |
| [SEO & Performance](docs/SEO-PERFORMANCE.md) | How a client-rendered app is made fully crawlable and fast |

## At a glance

- **Frontend:** React 19 + TypeScript single-page app, built with Vite, styled with Tailwind CSS, installable as a PWA.
- **Backend:** Laravel 13 (PHP 8.3) REST API with session-cookie authentication (Sanctum), role-based access control and TOTP two-factor authentication.
- **Data:** MySQL 8.
- **SEO:** server-rendered `<head>` per URL (titles, canonical URLs, Open Graph, schema.org JSON-LD), live `sitemap.xml`, correct HTTP status codes.
- **Delivery:** one domain, HTTPS-only, immutable caching for content-hashed assets.

## Contact

- Website: <https://horooinnovations.com>
- Security reports: please use the contact form on the website and ask for the engineering team. Do not open public issues for vulnerabilities.

© HOROO INNOVATION PLC. Documentation licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
