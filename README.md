# Agent Mag Docs

Generated first-party documentation context for Agent Mag agents.

This repository is a public mirror. The source of truth lives in the private Agent Mag site repository under `content/docs`.

## Install Context

```bash
npx agentmag add docs scrape
npx agentmag add docs index
```

Docs context is not a skill bundle and is not counted as a skill install. It is source-grounded content that agents can copy or install locally.

## Pages

| Page | CLI |
| --- | --- |
| [Documentation](docs/index.md) | `npx agentmag add docs index` |
| [Web Intelligence API](docs/web-intelligence-api.md) | `npx agentmag add docs web-intelligence-api` |
| [Scrape Endpoint](docs/scrape.md) | `npx agentmag add docs scrape` |
| [Credits and Billing](docs/credits-and-billing.md) | `npx agentmag add docs credits-and-billing` |
| [Dashboard](docs/dashboard.md) | `npx agentmag add docs dashboard` |
| [Open Source AI Agent Tools](docs/open-source-projects.md) | `npx agentmag add docs open-source-projects` |

## Files

- `docs/*.md` contains prompt-ready Markdown.
- `docs/*.json` contains structured context with title, URL, table of contents, content formats, and CLI metadata.

Generated from https://docs.theagentmag.com.
