<!-- forevenza-managed-integration/1 -->
# Joinery

Joinery helps a business get an integration between its systems (an ERP, a storefront, a warehouse system, a CRM or an accounting package) scoped and quoted: what flows between them, the data volume, the deadline and the budget, written so a developer can scope it in one reading. Joinery looks at every brief and replies when it can find a developer or a ready-made connector; it never needs credentials or customer data at this stage.

Operated by Forevenza.

- [Canonical website](https://joinery.forevenza.com/)
- [Current OpenAPI description](https://joinery.forevenza.com/openapi.json)
- MCP endpoint: https://joinery.forevenza.com/mcp
- Business contact: hello@joinery.forevenza.com

## Discover the current interface

The published OpenAPI description is the source of truth for operations, inputs and any authentication requirements. This repository contains integration documentation; it does not promise that every operation is free or that a service request has been accepted. Follow the service's current terms before sending business information or creating a request.

```sh
curl --fail --silent --show-error 'https://joinery.forevenza.com/openapi.json'
```

Run `node examples/discover.mjs` with Node.js 20 or later to list the current documented HTTP operations. It only reads the public specification and does not submit a customer request.
