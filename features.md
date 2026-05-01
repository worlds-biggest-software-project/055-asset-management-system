# Asset Management System — Feature & Functionality Survey

> Candidate #55 · Researched: 2026-05-01

## Solutions Analysed

| Tool | Type | Licence / Model | URL |
|------|------|-----------------|-----|
| IBM Maximo Application Suite | Commercial | Proprietary; $200K–$2M+/yr | https://www.ibm.com/products/maximo |
| SAP PM / IAM (S/4HANA) | Commercial | Proprietary; bundled with SAP S/4HANA | https://www.sap.com |
| Fiix (Rockwell Automation) | Commercial SaaS | Proprietary; from $45/user/mo | https://www.fiixsoftware.com |
| UpKeep | Commercial SaaS | Proprietary; from $20/user/mo | https://www.upkeep.com |
| Limble CMMS | Commercial SaaS | Proprietary; from $28/user/mo | https://limblecmms.com |
| Asset Panda | Commercial SaaS | Proprietary; from ~$3K/yr | https://www.assetpanda.com |
| Cheqroom | Commercial SaaS | Proprietary; from ~$99/mo | https://www.cheqroom.com |
| Snipe-IT | Open Source | AGPLv3 (self-hosted); hosted from $39.99/mo | https://snipeitapp.com |
| openMAINT | Open Source | AGPLv3 (self-hosted) | https://www.openmaint.org |
| Atlas CMMS | Open Source | GPLv3 (self-hosted) | https://atlascmms.com |

## Feature Analysis by Solution

### IBM Maximo Application Suite

**Core features**
- Unified asset lifecycle management (ALM) combining Enterprise Asset Management, Asset Performance Management (APM), and Asset Investment Planning (AIP) in a single platform
- Equipment hierarchy with parent-child asset relationships, location tracking, and linear asset management (pipelines, roads, rail)
- Work order management: creation, scheduling, labour assignment, parts reservation, and completion recording
- Preventive maintenance (PM) scheduling by calendar interval, meter reading, or condition trigger
- Regulatory inspection and certification tracking with evidence attachment
- Inventory management for spare parts, tools, and consumables with reorder point automation

**Differentiating features**
- Maximo Mobile enables field technicians to access work orders, asset records, and manuals on iOS/Android with offline capability
- AI-powered predictive maintenance via IBM Watson integration: anomaly detection from IoT sensor data, remaining useful life (RUL) estimation
- Asset Investment Planning module prioritises capital expenditure across a fleet of assets using risk and condition scoring
- Unbeatable depth for linear asset management (utility pipelines, rail infrastructure, road networks)
- Maximo Health Safety and Environment add-on covers regulatory compliance and incident management for industrial operators

**UX patterns**
- Configurable role-based dashboards; historically complex but improved significantly with the Application Suite (cloud-native)
- Mobile-first field interface with camera-based work order creation and barcode/QR asset lookup
- Implementation typically requires 6–24 months; extensive configuration investment

**Integration points**
- SAP, Oracle, and major ERP connectors; SCADA and IoT platform integration (OSIsoft PI, Azure IoT Hub); GIS integration (Esri ArcGIS)
- Open API; REST and SOAP interfaces for custom integration

**Known gaps**
- Prohibitively expensive for any organization outside large enterprise or critical infrastructure ($200K–$2M+/yr)
- Requires weeks of training for maintenance staff; adoption remains a chronic implementation risk
- Overkill for non-industrial asset types (IT assets, office equipment, general facilities)
- Implementation and customization costs frequently exceed licence fees

**Licence / IP notes**
- Fully proprietary; IBM Application Suite subscription model; no open-source components exposed

---

### SAP PM / IAM (S/4HANA)

**Core features**
- Plant Maintenance module integrated directly into SAP S/4HANA: functional locations, equipment master, maintenance orders, and work centres
- Maintenance planning and scheduling with task lists, PM plans, and maintenance strategy definition
- Integration with SAP Materials Management for spare parts procurement triggered by maintenance orders
- Integration with SAP Controlling for maintenance cost allocation and asset accounting
- Inspection management with digital inspection rounds and characteristic recording

**Differentiating features**
- Unrivalled financial integration: maintenance orders post actual costs directly to asset cost centres; depreciation and impairment fully linked to asset master
- SAP Asset Intelligence Network (AIN) enables OEM-to-operator data sharing for asset documentation, service history, and IoT telemetry
- Predictive Maintenance with SAP BTP (Business Technology Platform): sensor data ingestion, ML-based failure prediction, and work order auto-generation

**UX patterns**
- Traditional SAP GUI for power users; Fiori-based mobile apps for field technicians in newer implementations
- Steep learning curve; SAP transaction codes remain the fastest route for experienced users

**Integration points**
- Native integration with all SAP modules (MM, FI, CO, PP, QM); IDoc/API for third-party systems; SAP BTP for cloud extensions

**Known gaps**
- Not sold as a standalone product; only viable for existing SAP S/4HANA customers
- Implementation complexity rivals Maximo for cost and duration
- Predictive maintenance capabilities require additional BTP licencing and data science resources
- No competitive market presence outside SAP ERP ecosystem

**Licence / IP notes**
- Proprietary; bundled with SAP S/4HANA licences; no standalone pricing

---

### Fiix (Rockwell Automation)

**Core features**
- Cloud-based CMMS with work order management, preventive maintenance scheduling, asset hierarchy, and parts inventory
- Multi-site asset management with location-based dashboards and cross-site reporting
- AI-powered analytics module called Fiix Foresight: identifies asset failure patterns and recommends PM schedule adjustments
- IoT integration framework for condition-based maintenance triggers from sensor data
- Mobile app for technician work order management with parts lookup and time tracking

**Differentiating features**
- Fiix Foresight applies machine learning to historical work order and failure data to surface maintenance optimisation recommendations without requiring IoT hardware investment
- Strong integration with Rockwell Automation Allen-Bradley hardware and FactoryTalk MES since the 2021 acquisition
- Reliability reporting with MTBF, MTTR, and failure mode analysis out of the box
- Robust API enabling integration with ERP, EAM, and IoT platforms

**UX patterns**
- Clean, modern cloud interface; technician-friendly work order forms with photo attachment and signature capture
- Configurable dashboards for maintenance managers with KPI tiles and PM compliance tracking

**Integration points**
- REST API; pre-built connectors for Oracle, SAP, and Microsoft Dynamics ERPs; Rockwell FactoryTalk integration; IoT platform connectors

**Known gaps**
- Increasingly complex and expensive as it moves up-market post-Rockwell acquisition; original SMB simplicity eroding
- Asset depreciation and financial accounting not a core capability; requires ERP integration
- Limited built-in GIS or linear asset management for utilities/infrastructure
- No IT asset management (ITAM) module

**Licence / IP notes**
- Proprietary SaaS; Basic free (limited); Professional from $45/user/mo; Enterprise custom

---

### UpKeep

**Core features**
- Mobile-first CMMS with work order creation, preventive maintenance scheduling, asset tracking, and inventory management
- Asset hierarchy with equipment records, warranty information, and attached manuals and photos
- Technician mobile app with push notification work order assignments, parts lookup, and completion workflow
- Meter-based and calendar-based PM trigger scheduling
- Downtime tracking and basic MTBF/MTTR reporting

**Differentiating features**
- Fastest deployment in the market; typical SMB and mid-market implementations complete in days to weeks
- Technician UX consistently rated highest in class; minimal training required for field staff adoption
- IoT sensor integration for condition-based PM triggers from vibration, temperature, and pressure sensors
- Strong use case for facilities management (HVAC, lighting, plumbing) and hospitality maintenance teams

**UX patterns**
- Consumer-grade mobile interface designed to be adopted by tradespeople who resist enterprise software
- Manager dashboard with real-time work order status, PM compliance, and technician utilisation

**Integration points**
- REST API; Zapier connector for no-code ERP integration; Slack and Teams notifications; QuickBooks integration

**Known gaps**
- Not a full EAM; lacks asset lifecycle modelling, depreciation tracking, capital planning, and complex hierarchy capabilities
- Limited multi-site reporting depth for organizations with 50+ locations
- No financial asset register or depreciation schedule integration
- Predictive maintenance analytics are basic compared to Fiix Foresight or IBM Maximo APM

**Licence / IP notes**
- Proprietary SaaS; Essential $20/user/mo; Premium $55/user/mo; Business+ custom

---

### Limble CMMS

**Core features**
- Cloud-based CMMS with work orders, PM scheduling, asset tracking, parts inventory, and vendor management
- Customizable PM templates with checklist steps, required photos, and signature capture
- QR code and barcode asset labelling with mobile scan-to-work-order creation
- Parts inventory with minimum quantity alerts and purchase order generation
- Multi-site dashboard aggregating work order and PM compliance metrics across locations

**Differentiating features**
- Consistently highest ease-of-use ratings in category (G2 Leader); rapid onboarding without IT support
- Customizable report builder producing maintenance KPI reports without SQL or BI tool knowledge
- Lowest total cost of ownership in the mid-market CMMS segment
- Guest technician access enabling contractors to submit and update work orders without requiring full user licences

**UX patterns**
- Drag-and-drop work order board; technician interface optimised for minimal taps to complete common tasks
- Guided setup wizard enables non-technical administrators to configure the system without professional services

**Integration points**
- REST API; Zapier and Make connectors; QuickBooks and Xero for parts cost posting

**Known gaps**
- No depreciation accounting or financial asset register
- No predictive maintenance or AI layer
- ERP integration requires third-party middleware or custom API work
- Limited for complex hierarchical asset structures (large industrial plant)

**Licence / IP notes**
- Proprietary SaaS; Basic $28/user/mo; Standard $69/user/mo; Enterprise custom

---

### Snipe-IT

**Core features**
- Open-source IT asset management (ITAM) platform tracking hardware assets (laptops, servers, networking gear), software licences, accessories, and consumables
- User assignment and check-in/check-out workflow with email notifications
- Asset history: every assignment, check-out, check-in, maintenance, and audit event recorded with timestamps
- Barcode and QR code label generation for physical asset tagging
- Software licence seat tracking with compliance reporting (seats assigned vs seats purchased)
- LDAP/Active Directory integration for user synchronisation

**Differentiating features**
- The de facto open-source standard for IT asset management; large and active community
- Custom fields on any asset category without schema changes; highly extensible data model
- REST API enabling integration with ITSM tools (Jira Service Management, Freshservice, Zendesk)
- Self-hostable on any Linux server or Docker environment; no per-user licence cost

**UX patterns**
- Clean, functional web interface; accessible to IT help desk staff without training
- Bulk import via CSV; bulk actions for mass check-in, check-out, and audit

**Integration points**
- REST API; LDAP/AD sync; Slack notifications; third-party ITSM integrations via API

**Known gaps**
- No physical plant or equipment maintenance; no work orders, PM scheduling, or maintenance history
- No depreciation accounting or financial fixed asset register
- No predictive maintenance or IoT integration
- No mobile native app (mobile-responsive browser only)
- IT assets only; not designed for vehicles, plant equipment, buildings, or infrastructure

**Licence / IP notes**
- AGPLv3; self-hosted free; hosted plans from $39.99/mo. AGPLv3 requires that modifications to the source code be made available if the application is run as a network service.

---

### openMAINT

**Core features**
- Open-source enterprise asset and maintenance management built on the CMDBuild framework (Java/PostgreSQL)
- Supports building assets, plant and equipment, infrastructure, and vehicles across their full lifecycle
- Work order management, PM scheduling, contractor management, and maintenance cost tracking
- Spatial data management: GIS integration for location-aware asset management of buildings and infrastructure
- Document management for asset manuals, certificates, and compliance records

**Differentiating features**
- Only open-source platform covering both physical infrastructure assets (buildings, roads) and plant equipment within a single system
- GIS integration enables map-based asset location and inspection route management
- Configurable class hierarchy: any custom asset type, attribute, and relationship can be defined without code
- Full maintenance history with costs, labour, and parts consumption linked to each asset record

**UX patterns**
- Java-based web interface that is functional but visually dated compared to modern SaaS CMMS tools
- Configuration via the CMDBuild admin console; requires technical expertise for customisation

**Integration points**
- REST API; BIM (Building Information Modelling) import for construction asset data; GIS (Esri, OpenLayers) integration; CSV import/export

**Known gaps**
- UI is dated and requires modernisation to achieve enterprise adoption
- No predictive maintenance, IoT integration, or AI capabilities
- Limited mobile technician experience
- Small community; limited commercial support options
- No depreciation accounting or integration with financial systems

**Licence / IP notes**
- AGPLv3; free self-hosted; commercial support available from the CMDBuild community. AGPLv3 copyleft applies to modifications distributed as network services.

---

### Atlas CMMS

**Core features**
- Open-source cloud CMMS with work orders, PM scheduling, asset hierarchy, parts inventory, and basic reporting
- Multi-site support with location-based asset organisation
- Mobile-responsive web interface for technician work order completion
- Community-supported with GitHub-based issue tracking and contribution model

**Differentiating features**
- Hosted cloud option alongside self-hosted, lowering the technical barrier for small organizations wanting open-source with managed infrastructure
- Lightweight and fast to deploy; minimal configuration required for basic CMMS functionality

**UX patterns**
- Modern flat-design web interface; simpler and more approachable than openMAINT

**Integration points**
- REST API (basic); limited pre-built integrations; primarily standalone

**Known gaps**
- Small and less active community than Snipe-IT; long-term sustainability uncertain
- No depreciation, financial integration, or fixed asset register
- No predictive maintenance, IoT, or AI capabilities
- No mobile native app; mobile browser performance inconsistent

**Licence / IP notes**
- GPLv3; free self-hosted. GPLv3 requires derivative works to be distributed under the same licence.

---

## Cross-Cutting Feature Themes

### Table-Stakes Features
- Asset master record with unique ID, location, manufacturer, model, serial number, purchase date, and warranty information
- Work order creation, assignment, and completion tracking with labour and parts consumption recording
- Preventive maintenance scheduling (calendar-based and meter/usage-based)
- Asset hierarchy (parent equipment, sub-components, functional location)
- Barcode or QR code label generation and mobile scan-to-lookup
- Parts and spare parts inventory with minimum stock alerts
- Maintenance history audit trail for each asset

### Differentiating Features
- Predictive maintenance via IoT sensor data ingestion (vibration, temperature, pressure, cycle counts) with ML-based failure prediction and remaining useful life estimation
- Fixed asset financial register integration: depreciation schedules (straight-line, MACRS, units-of-production), impairment flagging, and disposal journal generation
- Computer vision asset identification: photograph an asset with a mobile camera and have the system identify it and open its record
- GIS/spatial asset management for location-aware infrastructure and utility assets
- Asset Investment Planning: risk-and-condition-based capital expenditure prioritisation across asset portfolios
- Contractor and third-party maintenance management with time and materials tracking

### Underserved Areas / Opportunities
- No open-source solution combines physical asset tracking, PM scheduling, depreciation accounting, and IoT-driven predictive maintenance in a modern cloud-native package
- openMAINT covers the domain breadth but has a dated UI and no AI/IoT layer; Snipe-IT covers IT assets only
- AI-assisted field identification (camera to asset record) does not exist in any open-source CMMS
- Natural language work order creation and procedure lookup from maintenance knowledge bases is absent in open-source tools
- Carbon footprint and energy consumption tracking per asset class is an emerging compliance requirement not served by current open-source options

### AI-Augmentation Candidates
- Predictive maintenance: ingest IoT sensor data and historical failure records to estimate remaining useful life and dynamically adjust PM schedules
- Computer vision identification: identify equipment from a photo and retrieve its maintenance record
- Automated depreciation method inference: classify new assets by type and jurisdiction and generate compliant depreciation schedules
- Knowledge extraction from technician notes and OEM manuals into searchable, structured maintenance procedures
- Anomaly detection in energy and resource consumption data to flag equipment operating outside normal parameters

---

## Legal & IP Summary

Enterprise commercial tools (IBM Maximo, SAP PM, Fiix, UpKeep, Limble, Asset Panda, Cheqroom) are all fully proprietary with no open-source licensing. Customers have no rights to source code, workflow logic, or data schemas.

Open-source options carry the following obligations:
- **Snipe-IT (AGPLv3):** Modifications must be published if the application is offered as a network service. Using Snipe-IT unmodified does not trigger copyleft; forking and running a modified version as a hosted service requires releasing the modified source.
- **openMAINT (AGPLv3):** Same AGPLv3 obligations as Snipe-IT. The underlying CMDBuild framework is also AGPLv3.
- **Atlas CMMS (GPLv3):** Derivative works must be GPLv3-licensed. GPLv3 is less onerous than AGPLv3 for SaaS use cases (network use does not automatically trigger copyleft under GPLv3 as it does under AGPLv3).

A new AI-native OSS EAM built on MIT or Apache 2.0 would avoid all incumbent copyleft entanglement, provided it is written from scratch without incorporating existing GPLv3/AGPLv3 code. Industry standards (ISO 55000, ISO 55001, ISO 13374, IAS 16) are open specifications with no software licensing implications.

---

## Recommended Feature Scope

**Must-have (MVP)**
- Asset master with hierarchy (functional location, equipment, sub-component), serial number, warranty, and document attachment
- Work order lifecycle: creation, technician assignment, parts and labour recording, and completion with photo evidence
- Preventive maintenance scheduling: calendar-based and meter/usage-based triggers with automatic work order generation
- Mobile technician interface with QR/barcode scan-to-asset-record and offline capability
- Parts inventory with minimum stock alerts and reorder workflow
- Maintenance history and cost reporting per asset and asset class

**Should-have (v1.1)**
- IT asset management module: hardware assignment tracking, software licence compliance, and user check-in/check-out (covering Snipe-IT use cases)
- Fixed asset financial register: depreciation schedule generation (straight-line, declining balance), net book value tracking, and disposal recording
- IoT sensor data ingestion and threshold-based condition maintenance triggers
- AI-assisted predictive maintenance: ML model on historical work order and sensor data to estimate failure probability and recommended maintenance date
- Contractor and external vendor work order assignment with time-and-materials tracking

**Nice-to-have (backlog)**
- Computer vision asset identification from mobile camera photograph
- Natural language procedure lookup: query the maintenance knowledge base in plain language
- GIS/spatial asset mapping for facilities and infrastructure operators
- Carbon and energy consumption tracking per asset with benchmark reporting
- Asset investment planning: risk-and-condition-based capital expenditure prioritisation dashboard
