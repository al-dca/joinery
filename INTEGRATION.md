<!-- forevenza-managed-integration/1 -->
# Joinery

Joinery helps a business get an integration between its systems (an ERP, a storefront, a warehouse system, a CRM or an accounting package) scoped and quoted: what flows between them, the data volume, the deadline and the budget, written so a developer can scope it in one reading. Joinery looks at every brief and replies when it can find a developer or a ready-made connector; it never needs credentials or customer data at this stage.

Operated by Forevenza.

- [Canonical website](https://joinery.forevenza.com/)
- [Current OpenAPI description](https://joinery.forevenza.com/openapi.json)
- MCP endpoint: https://joinery.forevenza.com/mcp
- Business contact: hello@joinery.forevenza.com

## Connect an MCP client

Use the remote Streamable HTTP endpoint in an MCP client that supports it. Clients that use a mcpServers configuration can start with:

```json
{
  "mcpServers": {
    "joinery": {
      "type": "http",
      "url": "https://joinery.forevenza.com/mcp"
    }
  }
}
```

Inspect the live tools before choosing an operation:

```sh
node examples/discover-mcp.mjs
```

This Node.js 20+ example initializes the connection and reads every page of tools/list. It prints each current tool's description, input schema and action annotations; it never invokes a tool or submits a customer request. If discovery fails, it reports an error rather than implying the operation is available. Review the operation's inputs and terms before calling it.

## Discover the current HTTP interface

The published OpenAPI description is the source of truth for HTTP operations, inputs and any authentication requirements. This repository contains integration documentation and client examples, not the server implementation. It does not promise that every operation is free or that a service request has been accepted. Follow the service's current terms before sending business information or creating a request.

```sh
curl --fail --silent --show-error 'https://joinery.forevenza.com/openapi.json'
```

Run `node examples/discover.mjs` with Node.js 20 or later to list the current documented HTTP operations. It only reads the public specification and does not submit a customer request.
