# Compr MCP Server

**Address in. Defendable offer out. 60 seconds.**

Compr is deal underwriting for acquisitions teams and wholesalers. This is the public listing for Compr's remote MCP server, so Claude, ChatGPT, Cursor and other MCP clients can underwrite a property on request.

Website: https://thecompr.ai
Docs: https://thecompr.ai/docs/mcp
Official MCP Registry: `ai.thecompr/compr`

## Endpoint

- URL: `https://thecompr.ai/api/mcp`
- Transport: Streamable HTTP (remote, hosted, nothing to install)
- Auth: OAuth for claude.ai, Claude Desktop and ChatGPT connectors (add the URL and sign in with your Compr account), or a Compr API key sent as `Authorization: Bearer <key>`

Start free: https://thecompr.ai/signup?src=github

## Tools

| Tool | What it does |
|---|---|
| `underwrite_address` | Give it an address and get back a Compr report: ARV, rehab, max offer and a shareable report link. |
| `search` | Find past Compr reports from your team by address or city. Read only. |
| `fetch` | Open one of those reports. Read only. |

## Connect

In claude.ai, Claude Desktop or ChatGPT, add `https://thecompr.ai/api/mcp` as a custom connector and sign in.

Cursor or any client that takes a JSON config with an API key:

```json
{
  "mcpServers": {
    "compr": {
      "url": "https://thecompr.ai/api/mcp",
      "headers": { "Authorization": "Bearer YOUR_COMPR_API_KEY" }
    }
  }
}
```

Then ask your assistant something like "Underwrite 4100 Carl St, Dallas TX 75210 and tell me if the numbers work at a $95k ask."

## About

Compr was founded by Trevor Rice, a San Antonio real estate investor with 11 years in the business and over 500 deals. Questions: support@thecompr.ai

This repository only documents the hosted server. The service itself runs at thecompr.ai.
