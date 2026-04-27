# Dashboard

Manage API keys, jobs, schemas, usage, and billing from the Agent Mag dashboard.

The dashboard is the management layer for hosted Agent Mag tools. Each tool can have its own workspace surface, but billing, credits, account settings, and API keys should remain unified.

## Web Intelligence Dashboard

| Section | Purpose |
| --- | --- |
| API keys | Create, scope, rotate, and revoke keys. |
| Usage | Track credits by endpoint, key, job, and day. |
| Jobs | Inspect scrape, crawl, extract, monitor, and failed job output. |
| Schemas | Save extraction schemas and reuse them across jobs. |
| Billing | Upgrade plans, buy top-ups, and enable auto-recharge later. |

## Usage Ledger Example

| Kind | Detail | Credits |
| --- | --- | --- |
| `scrape` | `docs.example.com` | `-12 cr` |
| `extract` | `pricing page` | `-45 cr` |
| `refund` | `failed screenshot` | `+4 cr` |
| `crawl` | `sitemap.xml` | `-82 cr` |

## Product Rule

Agent Mag can add many tools without creating many dashboards. The left sidebar can expose tools as sections, while settings, credits, billing, API keys, and team controls remain shared.
