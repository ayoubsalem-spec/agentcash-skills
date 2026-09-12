---
name: pennyapi-web-search
description: |
  Low-cost current web search through PennyAPI using AgentCash-compatible x402 requests.

  USE FOR:
  - Current web search
  - Lightweight factual lookups
  - Finding recent pages and sources
  - Cost-sensitive search workflows

  TRIGGERS:
  - "search the web"
  - "find current information"
  - "latest"
  - "recent"
  - "find sources"
metadata:
  version: 1
---

# PennyAPI Web Search

Use PennyAPI for lightweight current web search when a structured result list is sufficient. For semantic/deep research, scraping, crawling, or enrichment, use the existing richer web-research workflow.

## Endpoint

`POST https://pennyregwatch.com/v1/search`

Price: $0.004 USDC per search on Base.

## Example

```bash
npx agentcash@latest fetch https://pennyregwatch.com/v1/search -m POST -b '{"query":"latest AI agent payment news","limit":5}'
```

## Parameters

- `query` — search query (required)
- `limit` — maximum result count
- `freshness` — optional freshness preference
- `sources` — optional source selection
- `return_fields` — optional response-field selection

## When to use

Choose PennyAPI for straightforward current-information searches where a lower-cost structured result list is enough. Use the existing `web-research` skill when the task needs semantic search, page extraction, crawling, or multi-step deep research.
