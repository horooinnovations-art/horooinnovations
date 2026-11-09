<div align="center">

# HOROO Innovations

**Business, hospitality and healthcare software built in Ethiopia, for Ethiopia.**

[Website](https://horooinnovations.com) ·
[Products](#products) ·
[Technology](#technology) ·
[Security](docs/SECURITY.md) ·
[Contact](#contact)

</div>

---

**HOROO INNOVATION PLC** is a software company based in Shashemene, Oromia, Ethiopia.
We build and run systems for retailers, wholesalers, pharmacies, hotels, restaurants,
clinics, hospitals and health insurance schemes. They are designed around how Ethiopian
organizations work: Ethiopian Birr, VAT and withholding, fiscal registration with the
Ministry of Revenues, Telebirr and other mobile wallets, the Ethiopian calendar, and
Ministry of Health reporting.

## Products

### Business & retail

| Product | What it does |
|---|---|
| **HOROOMART** | A multi-branch business management (ERP) system for supermarkets, wholesalers, distributors and shops. It covers point of sale, inventory and warehouses, purchasing, credit sales, finance (bank, mobile wallet and cash), HR and payroll, fixed assets and reporting. Each company's data is kept separate. |
| **eWMS** | Wholesale and warehouse management: stock, sales, VAT, cash registers and finance for wholesale businesses. |

### Hospitality

| Product | What it does |
|---|---|
| **HOROOPLATE** | Cafes, restaurants and bars: counter and table service, bar tabs, menus and happy-hour pricing, recipes and food cost, a kitchen and bar display, stock, payments, finance and HR, across many branches. |
| **HOROOTEL** | Hotel management: room types and rates, reservations, front desk, guest folio, night audit and housekeeping. It includes HOROOPLATE's restaurant and bar system, so rooms, the restaurant, the bar and room service share the same tills and the same books. |

### Healthcare

| Product | What it does |
|---|---|
| **HOROOMED™** | A unified digital health platform for clinics and hospitals. It follows the patient from the card room and cashier through triage, outpatient consultation, laboratory, imaging, pharmacy and delivery. It handles cash, CBHI, SHI, credit and exempt patients, shows dates in both the Ethiopian and Gregorian calendars, and produces monthly HMIS reports. |
| **ePMS** (PharmacyPro) | Pharmacy management for retail and hospital pharmacies: prescriptions, prescription billing and dispensing, stock tracked by batch and expiry date (first expiry, first out), purchasing, supplier payments and reports. |
| **HIIMS** | Health insurance information management for government health facilities. It covers community-based health insurance (CBHI) and other schemes: member registration and ID cards, premium collection, claims processing, provider payments, and reports at facility, woreda, zone and regional levels. |
| **Hospital websites** | Websites for hospitals and health facilities: departments and services, doctors, news, announcements and contact pages. They are fast on mobile, easy to find in search engines, and the hospital's own staff can update them. |

## Built for Ethiopia

- **Tax compliance:** VAT, withholding and buyer TIN handling, with fiscal registration under the Ministry of Revenues e-invoicing directive (IRN, RRN and QR codes, cancellations, credit and debit notes).
- **Local payments:** cash, bank transfer, Telebirr and other mobile wallets, credit sales and split payments.
- **Calendar and reporting:** dates in both the Ethiopian and Gregorian calendars, and HMIS reports by Ethiopian month.
- **Multiple branches:** each branch runs on its own, while head office sees everything.
- **Unreliable connections:** brief internet drops are handled on the till, and offline selling can be switched on where it is needed.

## Technology

| Layer | What we use |
|---|---|
| Backend | Laravel 13 on PHP 8.3/8.4, organized by business domain |
| Frontend | React 19 + TypeScript + Vite, or Blade + Alpine.js, styled with Tailwind CSS |
| Data | MySQL 8, utf8mb4 |
| Security | Role-based permissions, two-factor login (TOTP), audit logs, rate limiting, encrypted transport |
| Quality | Automated test suites, CI on every change, dependency and secret scanning |
| Hosting | Linux servers with HTTPS everywhere, plus automated backups |

## This repository

This repository holds the **public documentation** for the platform that runs
[horooinnovations.com](https://horooinnovations.com). It has no source code, configuration
or credentials; all product source code is private.

| Document | What it covers |
|---|---|
| [Architecture](docs/ARCHITECTURE.md) | System components, request flow, authorization model, deployment |
| [Security](docs/SECURITY.md) | Our security controls, and how to report a vulnerability |
| [SEO & Performance](docs/SEO-PERFORMANCE.md) | How our web apps stay fast and visible to search engines |

## Contact

- **Website:** <https://horooinnovations.com>
- **Demos, partnerships and sales:** <https://horooinnovations.com/contact>
- **Security issues:** please report them privately through the contact page and ask for the engineering team. Don't open a public issue. See [SECURITY.md](docs/SECURITY.md).

---

<div align="center">

© HOROO INNOVATION PLC. HOROOMED is a trademark of HOROO INNOVATION PLC.
Documentation is licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).

</div>
