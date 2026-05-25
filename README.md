# 1NCE (1nce)
1NCE is a Cologne-headquartered global IoT connectivity provider best known for the IoT Lifetime Flat — a single one-time fee that bundles a multi-network SIM with 500 MB of data and 250 SMS over a 10-year subscription. The 1NCE Management API on `api.1nce.com/management-api` exposes the same surface as the customer portal across six product areas — Authorization, SIM Management (v1 and v2), Order Management, Product Information, Support Management, and 1NCE OS — with OAuth 2.0 bearer-token security and a public api-catalog document. 1NCE OS layers integration, device locator, inspector, optimizer, and partner-plugin services on top of the connectivity bundle, while the company's GitHub organization publishes the 1NCE IoT C SDK, FreeRTOS / Zephyr / Arduino blueprints, AWS IoT onboarding tooling, CloudFormation templates, and an MCP server for AI agent integration.

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/1nce/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

 - IoT, Connectivity, SIM, Cellular, NB-IoT, LTE-M, eUICC, Edge, Embedded, Global Roaming

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## Pricing — IoT Lifetime Flat

| Form factor | Hardware price | Subscription | Included data | Included SMS | Validity |
|---|---|---|---|---|---|
| SIM Card Business (non-eUICC) | $1 | $14 one-time | 500 MB | 250 SMS | 10 years |
| SIM Card Industrial (eUICC) | $2 | $14 one-time | 500 MB | 250 SMS | 10 years |
| SIM Chip Industrial (eUICC, solderable) | $2.50 | $14 one-time | 500 MB | 250 SMS | 10 years |

Coverage: 170+ countries across 2G, 3G, 4G/LTE-M, and NB-IoT through Tier-1 partners including Deutsche Telekom, SoftBank, and China Telecom. High Data IoT, 1NCE Fixers, and 1NCE Premium Service are available as add-ons.

## APIs

### 1NCE Authorization API
OAuth 2.0 client-credentials flow that issues bearer tokens for all 1NCE Management API endpoints. `POST /oauth/token` (Basic Auth) returns a short-lived access token used to call SIM Management, Order Management, Product Information, Support Management, and 1NCE OS services.

**Human URL:** [https://help.1nce.com/dev-hub/reference/api-welcome](https://help.1nce.com/dev-hub/reference/api-welcome)

- [Documentation](https://help.1nce.com/api/authorization/)
- [OpenAPI (v1)](openapi/1nce-authorization-openapi.yml)
- [OpenAPI (v2)](openapi/1nce-authorization-v2-openapi.yml)
- [Naftiko Capability — OAuth](capabilities/authorization-oauth.yaml)

### 1NCE SIM Management API
Manage, control, and monitor 1NCE IoT SIM cards by ICCID across the lifecycle. v1 covers General SIMs, SMS (MT/MO), Connectivity, SIM Events, SIM Usage, Volume Limits, Volume Top Up, and SIM Extension; v2 covers SIMs, Connectivity, SMS, and SIM Events on the v2 API surface.

**Human URL:** [https://help.1nce.com/api/sim-management/](https://help.1nce.com/api/sim-management/)

- [Documentation](https://help.1nce.com/api/sim-management/)
- [OpenAPI (v1)](openapi/1nce-sim-management-openapi.yml)
- [OpenAPI (v2)](openapi/1nce-sim-management-v2-openapi.yml)
- [JSON Schema — SIM](json-schema/1nce-sim-schema.json)
- [JSON-LD](json-ld/1nce-context.jsonld)
- [Naftiko Capability — SIMs](capabilities/sim-management-sims.yaml)
- [Naftiko Capability — SMS](capabilities/sim-management-sms.yaml)
- [Naftiko Capability — Connectivity](capabilities/sim-management-connectivity.yaml)
- [Naftiko Capability — Events](capabilities/sim-management-events.yaml)
- [Naftiko Capability — Usage](capabilities/sim-management-usage.yaml)

### 1NCE OS API
1NCE OS APIs for the bundled IoT operating system services. Covers IoT Integrator (CoAP/UDP/LwM2M device endpoints, PSK provisioning, AWS IoT cloud integration), Device Locator (positions, geofences), Device Inspector (device stats and diagnostics), Optimizer (payload compression savings and message tests), Devices, Settings, Administration Logs, Agreements, and the Plugin system (Datacake, Memfault, Mender, Tartabit).

**Human URL:** [https://help.1nce.com/api/1nce-os/](https://help.1nce.com/api/1nce-os/)

- [Documentation](https://help.1nce.com/api/1nce-os/)
- [OpenAPI](openapi/1nce-os-openapi.yml)
- [JSON Schema — Device](json-schema/1nce-device-schema.json)
- [Naftiko Capability — IoT Integrator Devices](capabilities/os-integrate-devices.yaml)
- [Naftiko Capability — IoT Integrator Clouds](capabilities/os-integrate-clouds.yaml)
- [Naftiko Capability — Device Locator](capabilities/os-locate.yaml)
- [Naftiko Capability — Device Inspector](capabilities/os-inspect.yaml)
- [Naftiko Capability — Optimizer](capabilities/os-optimize.yaml)
- [Naftiko Capability — Plugin System](capabilities/os-plugins.yaml)
- [Naftiko Capability — Administration](capabilities/os-admin.yaml)

### 1NCE Order Management API
Programmatically create and inspect 1NCE orders. `/v1/orders` lists and submits orders for SIM cards or services; `/v1/orders/{order_number}` retrieves order detail, status, and line items.

**Human URL:** [https://help.1nce.com/api/order-management/](https://help.1nce.com/api/order-management/)

- [Documentation](https://help.1nce.com/api/order-management/)
- [OpenAPI](openapi/1nce-order-management-openapi.yml)
- [Naftiko Capability — Orders](capabilities/order-management-orders.yaml)

### 1NCE Product Information API
Query the 1NCE product catalog including the IoT Lifetime Flat, Industrial and Business SIM form factors, High Data IoT add-ons, and 1NCE OS service entitlements via `/v1/products`.

**Human URL:** [https://help.1nce.com/api/product-information/](https://help.1nce.com/api/product-information/)

- [Documentation](https://help.1nce.com/api/product-information/)
- [OpenAPI](openapi/1nce-product-information-openapi.yml)
- [Naftiko Capability — Products](capabilities/product-information-products.yaml)

### 1NCE Support Management API
Open and track 1NCE customer support tickets programmatically via `/v1/support` so device-fleet operators can escalate connectivity, billing, or 1NCE Fixers requests from inside their own systems.

**Human URL:** [https://help.1nce.com/api/support-management/](https://help.1nce.com/api/support-management/)

- [Documentation](https://help.1nce.com/api/support-management/)
- [OpenAPI](openapi/1nce-support-management-openapi.yml)
- [Naftiko Capability — Tickets](capabilities/support-management-tickets.yaml)

## Tooling and SDKs

- [1NCE IoT C SDK](https://github.com/1NCE-GmbH/1nce-iot-c-sdk) — MIT-licensed C SDK with CoAP authentication, DTLS PSK, and energy saver
- [FreeRTOS Blueprint](https://github.com/1NCE-GmbH/blueprint-freertos) — Reference application integrating 1NCE OS features with FreeRTOS
- [Zephyr Blueprint](https://github.com/1NCE-GmbH/blueprint-zephyr) — Reference application for Zephyr RTOS
- [Arduino Blueprint](https://github.com/1NCE-GmbH/blueprint-arduino) — 1NCE OS feature walkthrough on Arduino
- [AWS IoT Core Device Onboarding](https://github.com/1NCE-GmbH/1nce-iot-device-onboarding) — TypeScript helper for MQTT onboarding to AWS IoT Core
- [CloudFormation Templates](https://github.com/1NCE-GmbH/cfn-templates) — Public AWS templates for 1NCE customer integrations
- [1NCE MCP Server](https://github.com/1NCE-GmbH/1nce-mcp-server) — Python MCP server exposing the 1NCE Management API to LLM agents

## Commercial Surface

- [Plans & Pricing](plans/1nce-plans-pricing.yml) — API Commons Plans 0.1
- [Rate Limits & Quotas](rate-limits/1nce-rate-limits.yml) — API Commons Rate Limits 0.1
- [FinOps](finops/1nce-finops.yml) — FinOps Framework / FOCUS 1.3 alignment

## Discovery

- [Public API Catalog](https://help.1nce.com/.well-known/api-catalog) — RFC 9727 linkset published by 1NCE
- [API Explorer v2](https://help.1nce.com/api/v2/) — Interactive try-it console (requires customer account)
- [Developer Hub](https://help.1nce.com/docs/) — Recipes, starting guide, and best-practices

## Maintainers

- Kin Lane — [API Evangelist](https://apievangelist.com) — info@apievangelist.com
