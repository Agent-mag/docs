# Scrape Endpoint

Fetch a single URL and return clean web content for agent workflows.

`POST /v1/scrape` is the first hosted endpoint. It is designed for one-page capture, enrichment, and conversion into formats agents can consume.

Start with the [Web Intelligence API overview](/docs/web-intelligence-api) for the full endpoint family, then review [Credits and Billing](/docs/credits-and-billing) to understand how hosted usage is priced.

## Example

```bash
curl https://api.theagentmag.com/v1/scrape \
  -H "Authorization: Bearer $AGENTMAG_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "url": "https://docs.example.com",
    "formats": ["markdown", "links"],
    "agentContext": true
  }'
```

## Parameters

| Field | Type | Required | Notes |
| --- | --- | --- | --- |
| `url` | string | Yes | Public URL to fetch. |
| `formats` | string[] | No | Planned values include `markdown`, `html`, `text`, `links`, `screenshot`, and `metadata`. |
| `agentContext` | boolean | No | When true, return a compact summary and context hints for LLM workflows. |
| `waitFor` | number | No | Extra browser wait time for JavaScript-heavy pages. |

## Output Formats

| Format | Use case |
| --- | --- |
| `markdown` | RAG ingestion, summaries, doc indexing, and prompt context. |
| `links` | Crawl planning and discovery. |
| `metadata` | Titles, descriptions, canonical URLs, and page-level signals. |
| `screenshot` | Visual QA, design reference, and page state capture. |

## Operational Rules

- API keys are workspace-scoped.
- Credit estimates should be visible before long jobs run.
- Failed screenshot or browser jobs should refund the screenshot portion when no usable output is produced.
- Hosted scale uses credits; local open-source tools stay available where possible.
- Usage, API keys, and credit history should be manageable from the [Agent Mag dashboard](/docs/dashboard).
