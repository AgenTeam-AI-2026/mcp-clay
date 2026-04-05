# mcp-clay

> ⚠️ **Status: Blocked — Clay.com does not currently have a public API.**

This repository is a placeholder for a future MCP server for **[clay.com](https://clay.com)** — the B2B data enrichment and waterfall platform used by outbound sales teams.

Built and maintained by [AgenTeam](https://agenteamai.com). MIT licensed.

---

## Why this doesn't exist yet

Clay.com does not offer a public REST API. Their own documentation states:

> *"Does Clay have an API? The short answer: no."*

What currently exists is too limited to build on:
- An **Enterprise-only** API for basic people/company lookups — requires contacting their GTM team directly, no self-serve access
- Webhooks for sending data **into** Clay
- A Clay API key that only supports cross-table lookups within the Clay UI — not external programmatic access
- MCP support in Clay's AI features means Clay can **consume** MCP servers, not expose one

---

## Not clay.earth

This server is for **clay.com** — the B2B GTM and data enrichment platform.

It is **not** for [clay.earth](https://clay.earth) (the personal CRM), which already has an official MCP server at `https://mcp.clay.earth/mcp`.

---

## What this server will do (when Clay releases a public API)

Once a public API is available, `mcp-clay` will expose tools for:

| Tool | Description |
|---|---|
| `clay_list_tables` | List all Clay tables in the connected workspace |
| `clay_search_table` | Search records in a Clay table |
| `clay_add_to_table` | Add new records to a Clay table |
| `clay_export_table` | Export a Clay table as structured data |
| `clay_run_waterfall` | Trigger a Clay enrichment waterfall on a list of contacts |

---

## Stack (when built)

- **Language:** TypeScript
- **Runtime:** Cloudflare Workers
- **Transport:** Streamable HTTP
- **Auth:** Bearer token (user's own Clay API key)
- **Pattern:** Same as [`mcp-apollo`](https://github.com/AgenTeam-AI-2026/mcp-apollo) — self-hosted, user owns the infra

---

## Watching for API availability

Track progress on the blocking issue: [#1 — Blocked: Clay.com has no public API](../../issues/1)

If Clay releases a public API, please comment on that issue with the documentation link.

---

## Related

- [`mcp-apollo`](https://github.com/AgenTeam-AI-2026/mcp-apollo) — Apollo.io MCP server (live ✅)
- [clay.com](https://clay.com)
- [Clay API status](https://university.clay.com/docs/guide-find-clay-api-key)

---

## License

MIT © AgenTeam-AI-2026
