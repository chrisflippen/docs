# DealerOS Commerce Platform — Documentation project instructions

This is the engineering reference documentation for the DealerOS Google Commerce stack.
Pages are MDX files with YAML frontmatter. Configuration lives in `docs.json`.

- Use the Mintlify MCP server `https://mcp.mintlify.com` to edit content and settings via MCP.
- Use the Mintlify docs MCP server `https://www.mintlify.com/docs/mcp` to query Mintlify component/configuration reference.

## Terminology

Use these terms exactly as written to keep the docs consistent with the codebase.

| Term | Use | Avoid |
|------|-----|-------|
| dealer | the automotive retailer / customer | dealership (in prose), client |
| store_code | the canonical short identifier for a dealer's GBP location | storeCode, store code |
| feed | the Merchant Center product feed (TSV) for a dealer's inventory | data feed, product listing |
| Merchant Center / MC | Google Merchant Center | GMC (in prose) — GMC is acceptable in technical diagrams |
| feed registration | the act of creating and registering a feed in MC | "adding a feed" |
| inventory | vehicle listings sourced from the dealer DMS | stock, vehicles (in isolation) |
| onboarding | the full end-to-end process of activating a new dealer | setup (alone), provisioning |
| cockpit | the v2 Commerce Cockpit web app (apps/web-v2.0) | dashboard, console |
| GBP | Google Business Profile | GMB (deprecated Google name) |
| GSC | Google Search Console | Search Console (in headings) |
| Google Ads | the advertising platform | Ads (alone in prose) |
| DMS | Dealer Management System (inventory data source) | dealer system |
| TSV | Tab-Separated Values feed format | CSV (our feeds are TSV) |
| normalization | the pipeline step that maps raw DMS fields to GMC schema | transformation, mapping |

## Style preferences

- Use active voice and second person ("you").
- Keep sentences concise — one idea per sentence.
- Use sentence case for headings.
- Bold for UI elements: Click **Save**.
- Use code formatting for file names, commands, env vars, field names, and paths.
- Diagrams: D2 + ELK layout only — no Mermaid.

## Content boundaries

Document in this repo:

- Architecture decisions and system topology
- Feed ingestion pipeline mechanics
- Data model and schema reference
- Google integration wiring (MC, Ads, GBP, GSC)
- Dealer onboarding steps and prerequisites
- Engineering standards and conventions
- Domain glossary

Do not document in this repo:

- Internal account credentials or API keys
- Client-specific configuration or deal terms
- Ops / account-migration runbooks (those live in internal ops docs)
- Draft or experimental features behind feature flags (document only when shipped)
