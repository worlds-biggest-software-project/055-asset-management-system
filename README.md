# Asset Management System

> Part of the [worlds-biggest-software-project](https://github.com/worlds-biggest-software-project) initiative.
>
> An AI-native, open-source enterprise asset management platform that unifies physical asset tracking, preventive and predictive maintenance, depreciation accounting, and audit trails in a modern cloud-native package.

Asset Management System is a candidate project to build a modern open-source EAM/CMMS that combines what today is split across IBM Maximo, SAP PM, Snipe-IT, and openMAINT. It targets facilities managers, plant maintenance teams, IT directors, finance controllers, and compliance officers at organisations priced out of heavy enterprise suites but underserved by single-purpose tools.

---

## Why Asset Management System?

- IBM Maximo and SAP PM lead enterprise/industrial asset management but require $200K–$2M+/year and 6–24 month implementations, putting them out of reach for municipalities, educational institutions, and SMB manufacturers.
- Mid-market SaaS CMMS tools (Fiix, UpKeep, Limble) cover work orders well but lack depreciation accounting, fixed asset registers, and ERP-grade financial integration.
- Snipe-IT is the de facto open-source ITAM tool but does not handle physical plant equipment, work orders, preventive maintenance, or depreciation.
- openMAINT covers physical assets and infrastructure but ships a dated Java UI, has a small community, no IoT/AI layer, and no depreciation accounting.
- No open-source system today combines physical asset tracking, condition-based maintenance, depreciation accounting, and AI-assisted field workflows in a production-ready, cloud-native package.

---

## Key Features

### Asset Records & Hierarchy

- Asset master with unique ID, location, manufacturer, model, serial number, purchase date, and warranty information
- Parent-child asset hierarchy (functional location, equipment, sub-component)
- Document attachment for manuals, certificates, and compliance records
- Barcode and QR code label generation with mobile scan-to-asset-record lookup
- Custom fields and asset categories without schema changes

### Work Orders & Maintenance

- Work order lifecycle: creation, technician assignment, parts and labour recording, completion with photo evidence
- Preventive maintenance scheduling with calendar-based and meter/usage-based triggers and automatic work order generation
- Maintenance history audit trail per asset with costs, labour, and parts consumption
- Contractor and external vendor work order assignment with time-and-materials tracking
- MTBF, MTTR, and downtime reporting

### Mobile & Field Workflow

- Mobile technician interface with QR/barcode scan-to-asset lookup
- Offline capability for field work in disconnected environments
- Photo attachment, signature capture, and parts lookup during work order completion
- Push-notification work order assignments

### Inventory & Financial Register

- Parts and spare parts inventory with minimum stock alerts and reorder workflow
- Fixed asset financial register with depreciation schedule generation (straight-line, declining balance, MACRS, units-of-production)
- Net book value tracking, impairment flagging, and disposal recording
- Maintenance cost reporting per asset and asset class

### IT Asset Management

- Hardware assignment tracking (laptops, servers, networking gear)
- Software licence seat tracking with compliance reporting (seats assigned vs purchased)
- User check-in/check-out workflow with audit timestamps
- LDAP/Active Directory integration for user synchronisation

---

## AI-Native Advantage

Predictive maintenance models ingest IoT sensor data (vibration, temperature, pressure, cycle counts) alongside historical work orders and failure records to estimate remaining useful life and dynamically adjust PM schedules — reducing both unplanned downtime and over-maintenance. Computer vision asset identification lets a field technician photograph equipment and have the system identify it, retrieve its maintenance history, and create a work order. Automated depreciation method inference classifies new assets by type and jurisdiction and generates compliant depreciation schedules, eliminating manual fixed-asset accounting work. Natural-language knowledge extraction converts technician notes, repair logs, and OEM manuals into searchable, structured maintenance procedures, preserving institutional knowledge as experienced engineers retire.

---

## Tech Stack & Deployment

Cloud-native architecture with self-hosted and managed-cloud deployment options. Standards alignment includes ISO 55000 / ISO 55001 (asset management lifecycle), ISO 13374 (condition monitoring data communication), ISO 15686 (service life planning), IAS 16 / IFRS 16 / ASC 840 (depreciation and lease accounting), and GS1 / RFID / QR standards for asset identification. REST API for ERP, ITSM, IoT platform, and GIS integration. Mobile-first technician experience with offline support. Intended licence is permissive (MIT or Apache 2.0) to avoid AGPLv3/GPLv3 copyleft entanglement with incumbents (Snipe-IT, openMAINT, Atlas CMMS) — the codebase will be written from scratch without incorporating existing copyleft sources.

---

## Market Context

The global EAM market is valued at $7.29–$8.22 billion in 2026, projected to reach $12.07–$17.46 billion by 2031–2035 at a CAGR of 9.7–10.7% (Fortune Business Insights; Mordor Intelligence). The broader physical asset tracking market is expected to grow from $27 billion in 2025 to $71.1 billion by 2032, with manufacturing the largest vertical (~19.75%) and predictive maintenance the fastest-growing segment. Pricing spans $0 (open source) through $28–$85/user/month (mid-market SaaS) up to $200K–$2M+/year (IBM Maximo, SAP PM); primary buyers are facilities managers, plant maintenance managers, IT directors, CFOs/controllers, and compliance officers at utilities and infrastructure operators.

---

## Project Status

> This project is in the **research and specification phase**.  
> Contributions, feedback, and domain expertise are welcome.

---

## Contributing

We welcome contributions from developers, domain experts, and potential users.
See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

**Important:** All contributions must be your own original work or clearly attributed
open-source material with a compatible licence. Copyright infringement and licence
violations will not be tolerated and will result in immediate removal of the offending
contribution. If you are unsure whether a piece of code, text, or other material is
safe to contribute, open an issue and ask before submitting.

---

## Licence

Licence to be determined. See [discussion](#) for context.
