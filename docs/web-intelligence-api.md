# Web Intelligence API

Scraping, crawling, extraction, and search context for AI agents.

The Web Intelligence API turns public web pages into structured context that agents can use immediately. It starts with scraping and expands into crawl jobs, schema extraction, and search-backed context bundles.

> **TL;DR:** The Web Intelligence API is Agent Mag's planned hosted web data API for scraping, crawling, extraction, and search-backed context for AI agents.

## API Family

| Endpoint | Stage | Use case | Credit model |
| --- | --- | --- | --- |
| `POST /v1/scrape` | Preview | Fetch one URL and return clean markdown, text, HTML, links, metadata, and screenshots when enabled. | `1+ credit/page` |
| `POST /v1/crawl` | Planned | Traverse docs sites, sitemaps, blogs, and product sites with depth and limit controls. | `1 credit/page` |
| `POST /v1/extract` | Planned | Apply a schema or instruction to scraped pages and return typed JSON objects. | `5+ credits/page` |
| `POST /v1/search` | Planned | Find relevant web results, scrape selected pages, and return ranked context. | `2-5 credits/result` |

## Request Shape

```http
POST https://api.theagentmag.com/v1/scrape
Authorization: Bearer $AGENTMAG_API_KEY
Content-Type: application/json
```

```json
{
  "url": "https://docs.example.com",
  "formats": ["markdown", "links"],
  "agentContext": true
}
```

## Response Shape

```json
{
  "id": "scrape_01h",
  "url": "https://docs.example.com",
  "status": "completed",
  "credits": 3,
  "data": {
    "markdown": "# Docs example...",
    "links": ["https://docs.example.com/api"],
    "metadata": {
      "title": "Docs example"
    }
  }
}
```

## Why It Lives Under Agent Mag

The API belongs under Agent Mag because the platform already targets agent builders. The docs, CLI, dashboard, free tools, newsletter, and hosted APIs can all reinforce the same audience instead of splitting attention across separate brands.
