# 1NCE (1nce)

1NCE is a Cologne-headquartered global IoT connectivity provider best known for the IoT Lifetime Flat — a single one-time fee that bundles a multi-network SIM with 500 MB of data and 250 SMS over a 10-year subscription. The 1NCE Management API on api.1nce.com/management-api exposes the same surface as the customer portal across six product areas — Authorization, SIM Management (v1 and v2), Order Management, Product Information, Support Management, and 1NCE OS — with OAuth 2.0 bearer-token security and a public api-catalog document. 1NCE OS layers integration, device locator, inspector, optimizer, and partner-plugin services on top of the connectivity bundle, while the company's GitHub organization publishes the 1NCE IoT C SDK, FreeRTOS / Zephyr / Arduino blueprints, AWS IoT onboarding tooling, CloudFormation templates, and an MCP server for AI agent integration.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/1nce/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/1nce/refs/heads/main/apis.yml)

## Scope

- **Position:** Consuming
- **Access:** 3rd-Party

## Tags

- IoT
- Connectivity
- SIM
- Cellular
- NB-IoT
- LTE-M
- eUICC
- Edge
- Embedded
- Global Roaming

## Timestamps

- **Created:** 2026-05-25T00:00:00.000Z
- **Modified:** 2026-05-25

## APIs

### 1NCE Authorization API

OAuth 2.0 client-credentials flow that issues bearer tokens for all 1NCE Management API endpoints. POST /oauth/token (Basic Auth) returns a short-lived access token used to call SIM Management, Order Management, Product Information, Support Management, and 1NCE OS services on api.1nce.com/management-api.

- **Human URL:** [https://help.1nce.com/dev-hub/reference/api-welcome](https://help.1nce.com/dev-hub/reference/api-welcome)

#### Tags

- Authorization
- OAuth
- IoT

#### Properties

- [Documentation](https://help.1nce.com/api/authorization/)
- [OpenAPI](openapi/1nce-authorization-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/1nce-authorization.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/1nce-authorization.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [OpenAPI](openapi/1nce-authorization-v2-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/1nce-authorization-v2.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/1nce-authorization-v2.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### 1NCE SIM Management API

Manage, control, and monitor 1NCE IoT SIM cards by ICCID across the lifecycle. v1 covers General SIMs, SMS (MT/MO), Connectivity, SIM Events, SIM Usage, Volume Limits, Volume Top Up, and SIM Extension; v2 (current) covers SIMs, Connectivity, SMS, and SIM Events on the v2 API surface. Includes data and SMS quotas, connectivity reset, status, top-ups, and event history.

- **Human URL:** [https://help.1nce.com/api/sim-management/](https://help.1nce.com/api/sim-management/)

#### Tags

- SIM
- Connectivity
- SMS
- Events
- Usage
- IoT

#### Properties

- [Documentation](https://help.1nce.com/api/sim-management/)
- [OpenAPI](openapi/1nce-sim-management-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/1nce-sim-management.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/1nce-sim-management.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [OpenAPI](openapi/1nce-sim-management-v2-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/1nce-sim-management-v2.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/1nce-sim-management-v2.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/1nce-sim-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON-LD](json-ld/1nce-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)

### 1NCE OS API

1NCE OS APIs for the bundled IoT operating system services. Covers IoT Integrator (CoAP/UDP/LwM2M device endpoints, PSK provisioning, AWS IoT cloud integration), Device Locator (positions, geofences), Device Inspector (device stats and diagnostics), Optimizer (payload compression savings and message tests), Devices, Settings, Administration Logs, Agreements, and the Plugin system (Datacake, Memfault, Mender, Tartabit).

- **Human URL:** [https://help.1nce.com/api/1nce-os/](https://help.1nce.com/api/1nce-os/)

#### Tags

- IoT
- Device Integration
- Device Locator
- Device Inspector
- Optimizer
- Plugins
- AWS IoT

#### Properties

- [Documentation](https://help.1nce.com/api/1nce-os/)
- [OpenAPI](openapi/1nce-os-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/1nce-os.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/1nce-os.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/1nce-device-schema.json) — [JSON Schema](https://json-schema.org/specification)

### 1NCE Order Management API

Programmatically create and inspect 1NCE orders. /v1/orders lists and submits new orders for SIM cards or services; /v1/orders/{order_number} retrieves order detail, status, and line items so customers can automate SIM provisioning flows.

- **Human URL:** [https://help.1nce.com/api/order-management/](https://help.1nce.com/api/order-management/)

#### Tags

- Orders
- Provisioning
- IoT

#### Properties

- [Documentation](https://help.1nce.com/api/order-management/)
- [OpenAPI](openapi/1nce-order-management-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/1nce-order-management.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/1nce-order-management.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### 1NCE Product Information API

Query the 1NCE product catalog including the IoT Lifetime Flat, Industrial and Business SIM form factors, High Data IoT add-ons, and 1NCE OS service entitlements via /v1/products.

- **Human URL:** [https://help.1nce.com/api/product-information/](https://help.1nce.com/api/product-information/)

#### Tags

- Catalog
- Products
- IoT

#### Properties

- [Documentation](https://help.1nce.com/api/product-information/)
- [OpenAPI](openapi/1nce-product-information-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/1nce-product-information.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/1nce-product-information.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### 1NCE Support Management API

Open and track 1NCE customer support tickets programmatically via /v1/support so device-fleet operators can escalate connectivity, billing, or 1NCE Fixers requests from inside their own systems.

- **Human URL:** [https://help.1nce.com/api/support-management/](https://help.1nce.com/api/support-management/)

#### Tags

- Support
- Tickets
- IoT

#### Properties

- [Documentation](https://help.1nce.com/api/support-management/)
- [OpenAPI](openapi/1nce-support-management-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/1nce-support-management.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/1nce-support-management.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Portal](https://www.1nce.com/en-us/)
- [Documentation](https://help.1nce.com/docs/)
- [Documentation](https://help.1nce.com/dev-hub/reference/api-welcome)
- [Documentation](https://help.1nce.com/dev-hub/reference/api-best-practices)
- [Getting Started](https://help.1nce.com/starting-guide/docs/api-general-information)
- [Sandbox](https://help.1nce.com/api/v2/)
- [Documentation](https://help.1nce.com/.well-known/api-catalog)
- [Portal](https://portal.1nce.com/)
- [Sign Up](https://portal.1nce.com/portal/customer/registration)
- [Documentation](https://www.1nce.com/en-us/1nce-connect/features/rest-api)
- [Portal](https://www.1nce.com/en-us/1nce-connect)
- [Portal](https://www.1nce.com/en-us/1nce-os)
- [Code Examples](https://www.1nce.com/en-us/resources/news/blog/iot-cookbook)
- [Blog](https://www.1nce.com/en-us/resources/news/blog)
- [GitHub Organization](https://github.com/1NCE-GmbH)
- [SDK](https://github.com/1NCE-GmbH/1nce-iot-c-sdk)
- [Code Examples](https://github.com/1NCE-GmbH/blueprint-freertos)
- [Code Examples](https://github.com/1NCE-GmbH/blueprint-zephyr)
- [Code Examples](https://github.com/1NCE-GmbH/blueprint-arduino)
- [Code Examples](https://github.com/1NCE-GmbH/1nce-iot-device-onboarding)
- [Code Examples](https://github.com/1NCE-GmbH/cfn-templates)
- [Tool](https://github.com/1NCE-GmbH/1nce-mcp-server)
- [LinkedIn](https://www.linkedin.com/company/1nce-gmbh)
- [Twitter](https://twitter.com/1nce_iot)
- [YouTube](https://www.youtube.com/@1nce_iot)
- [Terms of Service](https://www.1nce.com/en-us/legal/terms-and-conditions)
- [Privacy Policy](https://www.1nce.com/en-us/legal/privacy-policy)
- [Documentation](https://www.1nce.com/en-us/legal/imprint)
- [Contact Form](https://www.1nce.com/en-us/contact)
- [F A Q](https://www.1nce.com/en-us/support/faq)
- [Documentation](https://help.1nce.com/dev-hub/reference/api-best-practices)
- [Plans](plans/1nce-plans-pricing.yml)
- [Rate Limits](rate-limits/1nce-rate-limits.yml)
- [Fin Ops](finops/1nce-finops.yml)
- [Features](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** info@apievangelist.com
**URL:** https://apievangelist.com
