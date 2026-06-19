# Documentation project instructions

## About this project

- This is the documentation site for **David**, a synthetic financial data API for building, training, and evaluating financial AI agents.
- The site is built on [Mintlify](https://mintlify.com). Pages are MDX files with YAML frontmatter.
- Configuration lives in `docs.json` (branding, theme, navigation tabs and groups).
- Content is modeled on the structure of the Financial Datasets documentation and describes the SynthFin API that powers David's synthetic data.

## Terminology

- The product is **David** (David Data Solutions). Refer to the API as "the David API".
- A **scenario** is a self-contained synthetic market world. Every data endpoint is scoped to a `scenario_id`. Never call it a "dataset" or "project".
- Scenarios are generated and curated by **David**, not by API consumers. The docs describe browsing and querying scenarios — never document user-facing scenario creation/generation endpoints.
- Data is **synthetic** and **scenario-scoped**. Ticker symbols and company display identity are real; prices, fundamentals, news, filings, ownership, and events are generated.
- Distinguish **operating companies** (full issuer surface) from **non-operating instruments** (ETFs, warrants, units — prices and market data only).

## Style preferences

- Use active voice and second person ("you").
- Keep sentences concise — one idea per sentence.
- Use sentence case for headings.
- Bold for UI elements; code formatting for endpoints, parameters, file names, and field names.
- Document HTTP endpoints with a fenced ` ```http ` block showing `METHOD /path`, a parameter table, and a `curl` example with a JSON response.
- Always include the `X-API-KEY` header in request examples. Use `https://api.davidhf.com` as the base URL.

## Content boundaries

- Document the public API surface. Admin endpoints are documented but clearly marked admin-only.
- Be honest about synthetic-data limitations: David is a research/evaluation tool, not a licensed feed of real market data.
- Don't document internal generator implementation details beyond what helps an API consumer reason about the data.
