# Standards & API Reference

> Project: Asset Management System · Generated: 2026-05-06

## Industry Standards & Specifications

### ISO Standards

**ISO 55000:2024 — Asset Management: Vocabulary, Overview and Principles**
- URL: https://www.iso.org/standard/83053.html
- The foundational standard defining the vocabulary, principles, and overview of asset management. Updated in 2024, this edition places a stronger focus on outcomes of asset management activities. Any EAM system targeting utilities, infrastructure, or regulated industries must align its terminology and lifecycle concepts with ISO 55000.

**ISO 55001:2024 — Asset Management System: Requirements**
- URL: https://www.iso.org/standard/83054.html
- Specifies requirements for establishing, implementing, maintaining, and improving an asset management system. ISO 55001 certification is increasingly mandated by public-sector infrastructure operators and utilities. An EAM platform that generates compliant audit trails, lifecycle records, and inspection evidence directly supports customer ISO 55001 certification programmes.

**ISO 55002:2018 — Asset Management: Guidelines for the Application of ISO 55001**
- URL: https://www.iso.org/standard/63198.html
- Provides guidance on interpreting and applying ISO 55001 requirements. EAM implementations for critical infrastructure regularly reference ISO 55002 to translate standard requirements into operational processes and software configuration decisions.

**ISO 55010:2019 — Asset Management: Guidance on the Alignment of Financial and Non-Financial Functions**
- URL: https://www.iso.org/standard/68150.html
- Guides alignment between financial reporting (depreciation, lifecycle cost) and operational asset management functions. Directly relevant to the dual-audience nature of an AI-native EAM that serves both maintenance engineers and finance controllers.

**ISO 55013:2024 — Asset Management: Guidance on Managing Data as an Asset**
- URL: https://www.iso.org/standard/80781.html
- Provides guidance on managing data as an organisational asset to support the broader asset management system. Directly informs the data model design, data quality, and governance requirements for an EAM platform.

**ISO 13374-1:2003 — Condition Monitoring and Diagnostics of Machines: Data Processing, Communication and Presentation (Part 1: General Guidelines)**
- URL: https://www.iso.org/standard/21832.html
- Establishes open software specifications for machine condition monitoring data exchange, allowing condition monitoring data to be communicated between different software packages without hardware-specific development. Defines the API interface description requirements (ISO/IEC 14750:1999) for condition monitoring processing blocks. Relevant to the predictive maintenance module.

**ISO 13374-3:2012 — Condition Monitoring: Part 3: Communication**
- URL: https://www.iso.org/standard/37611.html
- Specifies requirements for data communication in an open condition monitoring reference architecture. Informs the design of IoT sensor data ingestion APIs for the predictive maintenance layer.

**ISO 15686-1:2011 — Buildings and Constructed Assets: Service Life Planning (Part 1: General Principles and Framework)**
- URL: https://www.iso.org/standard/45798.html
- Establishes principles for service life planning across the full asset lifecycle (design through disposal). Relevant for facilities and real estate asset management modules, particularly remaining useful life estimation and capital replacement planning.

**ISO 15686-5:2017 — Buildings and Constructed Assets: Service Life Planning (Part 5: Life-Cycle Costing)**
- URL: https://www.iso.org/standard/61148.html
- Provides requirements for performing lifecycle cost (LCC) analyses of buildings and constructed assets. Directly applicable to the asset investment planning and depreciation modules in an EAM targeting facilities management customers.

**ISO 19650-1:2018 — Information Management Using BIM (Part 1: Concepts and Principles)**
- URL: https://www.iso.org/standard/68078.html
- International standard for Building Information Modelling (BIM) information management across the asset lifecycle. openMAINT already supports BIM data import; an AI-native EAM targeting construction and real estate verticals should support IFC/BIM data as an asset creation input.

**ISO/IEC 19987 — EPCIS (Electronic Product Code Information Services)**
- URL: https://www.gs1.org/standards/epcis
- GS1 EPCIS 2.0 is the ISO-standardised standard for capturing and sharing supply chain visibility events (what, when, where, why, how). EPCIS 2.0 adds REST API support and JSON-LD serialisation. Directly relevant to asset identification, transfer, and chain-of-custody tracking in asset management systems using barcode or RFID identification.

---

### Accounting & Financial Standards

**IAS 16 — Property, Plant and Equipment (IFRS)**
- URL: https://www.ifrs.org/issued-standards/list-of-standards/ias-16-property-plant-and-equipment/
- The primary IFRS accounting standard governing recognition, measurement, and depreciation of property, plant and equipment. Mandates component accounting (separate depreciation schedules for significant sub-components of a single asset), prohibits revenue-based depreciation methods, and requires depreciation to begin when the asset is available for use. All depreciation and fixed asset register features in the EAM must comply with IAS 16.

**IFRS 16 — Leases**
- URL: https://www.ifrs.org/issued-standards/list-of-standards/ifrs-16-leases/
- Requires lessees to recognise a right-of-use asset and a lease liability for all leases with a term greater than 12 months. Asset management systems used by large organisations with significant lease portfolios (real estate, fleet vehicles, equipment) must support IFRS 16 lease asset tracking and amortisation schedules.

**ASC 842 (US GAAP) — Leases**
- Standard governing lease accounting under US GAAP; the American counterpart to IFRS 16. EAM systems sold to US-headquartered companies need to support ASC 842 right-of-use asset schedules alongside IFRS 16 for multinational customers.

---

### W3C & IETF Standards

**W3C Web of Things (WoT) Thing Description 2.0**
- URL: https://www.w3.org/TR/wot-thing-description-2.0/
- W3C Recommendation providing a formal information model and JSON-LD serialisation for describing IoT device capabilities, interaction affordances, and metadata. An EAM that registers IoT sensor devices alongside physical assets should support WoT Thing Descriptions as the device metadata standard; the OPC Foundation is actively mapping WoT TDs to OPC UA asset models.

**RFC 7519 — JSON Web Tokens (JWT)**
- URL: https://www.rfc-editor.org/rfc/rfc7519
- Defines the JSON Web Token structure used for stateless authentication. JWT Bearer tokens are the standard authentication mechanism across all major EAM REST APIs (Snipe-IT, Limble, UpKeep, Asset Panda, Fiix) and must be supported by any EAM platform's API.

**RFC 6749 — OAuth 2.0 Authorization Framework**
- URL: https://www.rfc-editor.org/rfc/rfc6749
- The foundation for delegated authorisation used by all enterprise SaaS EAM platforms. OAuth 2.0 with PKCE (RFC 7636) is required for mobile client authentication (field technician apps). Enterprise customers require SAML 2.0 / OIDC SSO integration for identity federation.

---

### Data Model & API Specifications

**OpenAPI Specification (OAS) 3.1**
- URL: https://www.openapis.org/
- The industry-standard format for describing REST APIs. All major CMMS/EAM tools (Limble, UpKeep, Asset Panda, Snipe-IT) expose OpenAPI-described REST APIs. An AI-native EAM must publish a versioned OpenAPI 3.1 specification to support integration marketplaces, no-code connectors (Zapier, Make), and enterprise middleware.

**OPC Unified Architecture (OPC UA / IEC 62541)**
- URL: https://opcfoundation.org/about/opc-technologies/opc-ua/
- The dominant industrial IoT data exchange standard for manufacturing and process industries. OPC UA provides platform-neutral, vendor-independent data communication between PLCs, SCADA systems, and enterprise software, supporting both client-server and publish-subscribe patterns. An EAM targeting manufacturing customers must support OPC UA as a data ingestion source for condition-based maintenance triggers.

**MQTT v5 (ISO/IEC 20922)**
- URL: https://mqtt.org/
- The lightweight publish-subscribe messaging protocol that has become the standard for IoT sensor telemetry. MQTT brokers (e.g., HiveMQ, EMQX, Mosquitto) route sensor telemetry from field devices to EAM predictive maintenance processing pipelines. An AI-native EAM should natively subscribe to MQTT topics for condition data ingestion.

**GS1 EPCIS 2.0 REST API**
- URL: https://www.gs1.org/standards/epcis
- EPCIS 2.0 standardises a REST/JSON API for capturing and querying asset location and transfer events. An EAM that integrates with logistics and supply chain systems (for asset procurement and disposal) benefits from EPCIS-compliant event capture to record chain-of-custody transitions.

**IFC (Industry Foundation Classes) — buildingSMART**
- URL: https://www.buildingsmart.org/standards/bsi-standards/industry-foundation-classes/
- The open data standard for describing building and infrastructure asset data, used in BIM workflows. An EAM targeting facilities and construction asset management should support IFC file import as a source of asset hierarchy and equipment data for newly commissioned assets.

---

### Security & Authentication Standards

**OAuth 2.0 (RFC 6749) + PKCE (RFC 7636)**
- URL: https://oauth.net/2/
- The universal delegated authorisation framework for enterprise SaaS EAM APIs. PKCE extension is mandatory for mobile (public client) apps; relevant for technician mobile app authentication.

**OpenID Connect 1.0 (OIDC)**
- URL: https://openid.net/connect/
- Authentication layer built on OAuth 2.0; the standard for enterprise SSO integration (Azure AD / Entra ID, Okta, Google Workspace). All enterprise EAM deployments require OIDC-based SSO; Snipe-IT, Fiix, and Limble all support SAML/OIDC federation.

**SAML 2.0**
- URL: https://www.oasis-open.org/standards/saml/
- The XML-based standard for enterprise identity federation; still required by many corporate IT departments alongside or instead of OIDC. Enterprise EAM platforms support SAML 2.0 for SSO with corporate identity providers.

**OWASP API Security Top 10**
- URL: https://owasp.org/www-project-api-security/
- The authoritative guide to API security vulnerabilities. An EAM REST API must address Broken Object Level Authorization (BOLA), excessive data exposure, and lack of rate limiting — the top risks for multi-tenant asset management APIs where one customer must never access another's asset records.

---

### MCP Server Specifications

The Model Context Protocol (MCP) is relevant to an AI-native EAM as the standard interface by which AI assistant clients (Claude, Cursor, GitHub Copilot) connect to external tools and data sources.

**Model Context Protocol (MCP)**
- URL: https://modelcontextprotocol.io/
- An open protocol standardising how AI models connect to external data sources and tools. An AI-native EAM could expose an MCP server providing tools such as: `get_asset`, `create_work_order`, `query_maintenance_history`, `predict_failure_probability`. This would allow AI assistants embedded in enterprise workflows to query the asset management system in natural language without bespoke integration.

---

## Similar Products — Developer Documentation & APIs

### IBM Maximo Manage

- **Description:** IBM's enterprise EAM platform for asset-intensive industries. The most feature-complete EAM on the market, covering asset lifecycle, work management, inventory, and AI-powered predictive maintenance via Watson.
- **API Documentation:** https://ibm-maximo-dev.github.io/maximo-restapi-documentation/
- **IBM API Hub (Maximo APIs):** https://developer.ibm.com/apis/catalog/maximo--maximo-manage-rest-api/
- **Standards:** REST/JSON; OSLC (Open Services for Lifecycle Collaboration) for cross-tool integration; SOAP/XML legacy interfaces also supported
- **Authentication:** OAuth 2.0 Bearer tokens; LDAP/AD integration; API keys for system integrations
- **Notes:** The Maximo NextGen REST API (documented February 2026) supports querying, creating, updating, and invoking workflow actions on all Maximo business objects (assets, work orders, locations, inventory). Uses `oslc.where`, `oslc.select`, and `oslc.orderBy` query parameters. Supports bulk operations in a single transaction.

---

### Fiix CMMS (Rockwell Automation)

- **Description:** Cloud-based CMMS with work order management, preventive maintenance, asset hierarchy, and AI-powered maintenance analytics (Fiix Foresight). Strong Rockwell/Allen-Bradley hardware integration.
- **API Documentation:** https://fiixlabs.github.io/api-documentation/guide.html
- **API Reference:** https://fiixlabs.github.io/api-documentation/
- **SDKs:** Java SDK — https://github.com/fiixlabs/fiix-cmms-api-java-examples; JavaScript SDK — https://github.com/fiixlabs/fiix-cmms-api
- **Standards:** REST/JSON; CRUD operations; API key authentication; webhooks for event-driven integration
- **Authentication:** API key pair (Client Key + Client Secret) used to obtain session tokens
- **Notes:** The Fiix API supports full CRUD on assets, work orders, PM schedules, parts, locations, and custom fields. Both Java and JavaScript SDKs are maintained by Fiix Labs on GitHub. Integration with FactoryTalk Optix is documented in a separate Rockwell reference manual.

---

### UpKeep

- **Description:** Mobile-first CMMS/EAM for maintenance teams in facilities, manufacturing, and hospitality. Highest technician UX ratings in the category; fast time-to-value for SMB and mid-market deployments.
- **API Documentation:** https://developers.onupkeep.com/
- **Standards:** REST/JSON; webhook support for real-time event notifications; Zapier connector for no-code integration
- **Authentication:** Session token authentication (username/password exchange for bearer token); Business Plus plan required for API access
- **Notes:** The UpKeep REST API exposes Work Orders, Assets, Parts, Locations, Users, and PM Schedules as primary resources. Supports GET, POST, PUT, DELETE. Webhooks available for work order status changes, PM completions, and asset updates.

---

### Limble CMMS

- **Description:** Cloud CMMS with the highest ease-of-use ratings (G2 Leader). Work orders, PM scheduling, asset tracking, parts inventory, multi-site dashboards, and customizable reporting.
- **API Documentation:** https://apidocs.limblecmms.com/
- **Postman Workspace:** https://www.postman.com/limbleapiqa/limble-solutions-llc-s-public-workspace/documentation/zskh2o7/limble-api-v2
- **Standards:** REST/JSON (Limble API V2); BASIC authentication; regional endpoint support (US, Canada, Australia, Europe, 21CFR-compliant)
- **Authentication:** Basic HTTP authentication with API credentials
- **Notes:** Limble API V2 covers Assets, Locations, Parts, Tasks (Work Orders, PM, Work Requests), Users, Vendors, Roles, Teams, Purchase Orders, General Ledger, Budgets, Priorities, Tags, Statuses, Webhooks, and Units of Measure. Regional API endpoints support data residency requirements.

---

### Snipe-IT

- **Description:** The de facto open-source IT asset management (ITAM) platform. Tracks hardware, software licences, accessories, and consumables with user assignment workflows.
- **API Documentation:** https://snipe-it.readme.io/reference
- **Swagger/OpenAPI Spec:** Available via the Snipe-IT API documentation portal (linked from readme.io)
- **Developer Docs:** https://snipe-it.readme.io/docs/internally-parsing-the-api
- **Standards:** REST/JSON; Bearer token authentication; OpenAPI/Swagger specification published; API Explorer with live "Try It" calls in documentation
- **Authentication:** API token as a Bearer token in the Authorization header; token generated from user profile in the web interface
- **Notes:** Snipe-IT API base URL is `https://<your-domain>/api/v1`. Provides full CRUD for Assets, Models, Categories, Locations, Users, Licences, Accessories, Consumables, and Departments. AGPLv3 licensed; the Microsoft Snipe-IT API Cookbook on GitHub provides integration examples. A Python client is available via dltHub.

---

### Asset Panda

- **Description:** Flexible asset tracking platform bridging ITAM, CMMS, and fixed asset accounting. Highly configurable field structures and workflow automation across asset types.
- **API Documentation:** https://docs.api.assetpanda.app/docs/getting-started
- **API Reference:** https://team-asset-panda.readme.io/reference
- **Standards:** REST/JSON; OAuth 2.0 (Client ID + Client Secret → Bearer token); rate limit: 400 calls per 3-minute window per IP
- **Authentication:** OAuth 2.0 — exchange Client ID and Client Secret (from API Configuration page) for a Bearer token
- **Notes:** Asset Panda API is organised around Accounts, Collections (asset groups), and Records (individual assets). Supports full CRUD on asset records and collection schemas. Custom fields per asset type are fully accessible via the API.

---

### openMAINT

- **Description:** Open-source enterprise asset and maintenance management platform built on the CMDBuild framework (Java/PostgreSQL). Covers building, plant, infrastructure, and vehicle assets with GIS integration.
- **API Documentation:** https://www.openmaint.org/en/resources (REST API documentation linked from the official resources page; technical details discussed at https://forum.cmdbuild.org/t/restful-api-openmaint-2-and-cmdbuild-3-2/4025)
- **Integration Documentation:** https://rtn-087.lsst.io/ (OpenMAINT-Jira workflow and API integration example)
- **Standards:** REST/JSON webservices built on CMDBuild framework; BIM/IFC import; GIS integration (Esri, OpenLayers); SOA architecture
- **Authentication:** Session-based REST authentication via CMDBuild framework
- **Notes:** openMAINT exposes a REST API for all CMDBuild object types (assets, work orders, maintenance records, locations). The API supports custom class hierarchies defined in the CMDBuild schema. AGPLv3 licensed. Commercial support available from the CMDBuild community. Integration with external systems (Jira, LSST Observatory toolchain) is documented in community resources.

---

### ServiceNow IT Asset Management (HAM/ITAM)

- **Description:** Enterprise ITSM platform with a robust IT Asset Management module (Hardware Asset Management / HAM) tightly integrated with the CMDB. Widely deployed in large enterprises for hardware lifecycle, software licence compliance, and procurement workflows.
- **API Documentation:** https://www.servicenow.com/docs/bundle/zurich-api-reference/page/build/applications/concept/api-rest.html
- **CMDB Instance API:** https://www.servicenow.com/docs/bundle/zurich-api-reference/page/integrate/inbound-rest/concept/cmdb-instance-api.html
- **Standards:** REST/JSON Table API; CMDB Instance API; GraphQL (for complex queries); OAuth 2.0 + Basic Auth; OpenAPI specification available
- **Authentication:** Basic authentication or OAuth 2.0; session tokens for scripted integrations; service account credentials for system integrations
- **Notes:** ServiceNow's Table API endpoint `api/now/table/cmdb_ci_computer` is the primary asset record endpoint. The `alm_asset` table stores general asset records. The CMDB is organised in a hierarchy of `cmdb_ci_*` tables. ServiceNow ITAM developers use Glide API, REST, SOAP, and JDBC for asset data ingestion from external systems. Discovery module auto-populates CMDB from network-scanned devices.

---

### IFS Cloud (EAM Module)

- **Description:** Industrial ERP with a deep enterprise asset management module covering asset lifecycle, work orders, PM, condition-based maintenance, and predictive analytics. Positioned for asset-intensive industries after acquiring Ultimo and Clevest.
- **API Documentation:** https://docs.ifs.com/techdocs/foundation1/045_administration_aurena/240_integration/010_api_doc/
- **IFS Developer Portal:** https://developer.ifs.com/
- **Standards:** REST/OData APIs; OpenAPI specification; IFS Cloud uses an API-first architecture; OData query parameters for filtering and pagination
- **Authentication:** OAuth 2.0; integration user accounts; service-to-service authentication for ERP system integrations
- **Notes:** IFS Cloud exposes RESTful OData APIs for all business objects. The developer portal provides API documentation, SDKs, and extensibility guides. IFS Cloud EAM integrates natively with IoT platforms, GIS systems, and ERP finance modules.

---

## Notes

**Gaps and Emerging Areas:**

1. **No unified open standard for EAM data exchange:** Unlike ERP (SAP IDocs, EDIFACT) or ITSM (ITIL process standards), the EAM/CMMS space lacks a widely-adopted open data exchange standard for transferring asset records and maintenance history between platforms. Vendor lock-in via proprietary data schemas remains a significant pain point. An AI-native open-source EAM that defines and publishes an open asset data schema (using JSON Schema or OpenAPI) would have a structural advantage in customer migrations.

2. **MCP for EAM is an unexplored frontier:** No existing EAM/CMMS platform has published an MCP server. As enterprise AI assistants mature, the EAM system that first offers a well-designed MCP server (enabling natural-language work order creation, asset queries, and maintenance history retrieval from within AI coding tools and assistants) will capture significant developer-led adoption.

3. **OPC UA + MQTT convergence:** The industrial IoT space is converging on OPC UA for device data modelling and MQTT for transport (the "MQTT for OPC UA" Pub/Sub specification from OPC Foundation). An EAM predictive maintenance module should support both the OPC UA information model and MQTT as a transport to be compatible with the broadest range of industrial hardware.

4. **ISO 55013 (Data as an Asset):** The 2024 update of this standard is increasingly cited in enterprise EAM RFPs as a requirement for data governance and quality frameworks within asset management systems. AI-native EAM platforms should reference ISO 55013 in their data model and API governance documentation to differentiate in regulated industry procurement.
