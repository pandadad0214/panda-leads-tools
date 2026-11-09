# Panda Leads Tools

<!-- mcp-name: io.github.pandadad0214/panda-leads-tools -->

Give Claude, Cursor or any MCP client 15 public lead-generation tools: local businesses, healthcare providers, podcasts, hiring signals, company enrichment and team pages, new Florida, Texas and New York businesses, permits, carriers, nonprofits, H-1B sponsors and EU tenders. Each tool runs one public-data Apify Actor on your own Apify account and is priced per result. Part of the [Panda Federation](https://github.com/pandadad0214/panda-federation-tools) toolkit (36 tools in four focused servers).

[![PyPI](https://img.shields.io/pypi/v/panda-leads-tools)](https://pypi.org/project/panda-leads-tools/)
[![Latest Release](https://img.shields.io/github/v/release/pandadad0214/panda-leads-tools?label=latest%20release)](https://github.com/pandadad0214/panda-leads-tools/releases/latest)
[![Umbrella](https://img.shields.io/badge/index-panda--federation--tools-blue)](https://github.com/pandadad0214/panda-federation-tools)
[![Apify Store](https://img.shields.io/badge/Apify_Store-pandadad0214-00a3ff)](https://apify.com/pandadad0214)
[![License: MIT](https://img.shields.io/badge/license-MIT-green)](LICENSE)

## How to use this

```bash
uvx panda-leads-tools
```

1. **Get a free Apify token** at [console.apify.com/settings/integrations](https://console.apify.com/settings/integrations) (the free plan includes $5 of monthly credit) and install [uv](https://docs.astral.sh/uv/).
2. **Add the server to your MCP client:** command `uvx`, args `["panda-leads-tools"]`, env `APIFY_TOKEN` (Cursor JSON below).
3. **Ask in plain words**, e.g. "List dentists in Phoenix, AZ with a website and phone number, then enrich their domains." Start with one or two inputs and read the `summary` / `agentSummary` line before widening.

```json
{"mcpServers": {"panda-leads-tools": {"command": "uvx", "args": ["panda-leads-tools"], "env": {"APIFY_TOKEN": "apify_api_YOUR_TOKEN"}}}}
```

## For AI agents

| Field | Value |
| --- | --- |
| Purpose | Focused MCP server with 15 public lead-generation tools: local businesses, healthcare providers, podcasts, hiring signals, company enrichment and team pages, new Florida, Texas and New York businesses, permits, carriers, nonprofits, H-1B sponsors and EU tenders. |
| Use when | A task needs a prospect or account list built from official or open public data (registries, open maps, public job boards, company websites). |
| Do not use when | You need LinkedIn, logged-in or paywalled data, scholarly sources (use `panda-research-tools`), federal funding (`panda-public-funding-tools`) or security audits (`panda-web-security-tools`). |
| Install | `uvx panda-leads-tools` (stdio, Python 3.11+) |
| Auth | `APIFY_TOKEN` env var; runs bill to that Apify account. |
| Tools | 15, listed under [Tools](#tools-15) |
| Outputs | JSON rows plus a one-line `summary` / `agentSummary`; Excel/CSV files on the Apify run. |
| Side effects and cost | Starts Apify runs; pay per result; empty runs are not charged per result; `run_max_charge_usd` caps each call. Read-only toward third-party sites. |

## Other ways to install

From the umbrella package (same tools):

```bash
uvx --from panda-federation-tools panda-leads-tools
```

From this repo instead of PyPI:

```bash
uvx --from git+https://github.com/pandadad0214/panda-leads-tools panda-leads-tools
```

Docker (stdio):

```bash
docker build -t panda-leads-tools .
docker run -i --rm -e APIFY_TOKEN panda-leads-tools
```

Cursor / Claude / VS Code: command `uvx`, args `["panda-leads-tools"]`, env `APIFY_TOKEN`.

Official MCP Registry name for this stdio package: `io.github.pandadad0214/panda-leads-tools` ([server.json](server.json)). Registry clients install the PyPI package with `uvx panda-leads-tools`. The git command above stays the install path from this repo.

## Use with Gemini CLI

Install this repo as a [Gemini CLI extension](https://geminicli.com/docs/extensions/) (adds the MCP server plus a short `GEMINI.md` context file). Needs [Gemini CLI](https://geminicli.com/), [uv](https://docs.astral.sh/uv/), and a free [Apify token](https://console.apify.com/settings/integrations).

```bash
gemini extensions install https://github.com/pandadad0214/panda-leads-tools
```

The extension prompts for `APIFY_TOKEN` on install and launches the server with `uvx panda-leads-tools`. Gallery listing is automatic once this public repo carries the `gemini-cli-extension` topic and a root `gemini-extension.json` (crawled daily).

## Tools (15)

- `npi_provider_lists`
- `podcast_leads_finder`
- `local_business_leads`
- `company_hiring_signals`
- `company_website_enricher`
- `company_team_finder`
- `topic_trends_tracker`
- `trucking_company_leads`
- `nonprofit_leads_irs`
- `building_permit_leads`
- `florida_new_business_leads`
- `texas_new_business_leads`
- `new_york_new_business_leads`
- `h1b_lca_sponsor_leads`
- `eu_ted_tenders`

Each tool runs one Apify Actor on your account. Empty runs are not charged per result; every call is capped by `run_max_charge_usd`. Full schemas and prices: [umbrella README](https://github.com/pandadad0214/panda-federation-tools#domain-tool-lists).

## Sibling domain servers

- [`panda-research-tools`](https://github.com/pandadad0214/panda-research-tools) — Scholarly integrity and papers: citation checks, literature and PubMed search, academic experts, PDF tables, Wayback Machine snapshots.
- [`panda-public-funding-tools`](https://github.com/pandadad0214/panda-public-funding-tools) — US federal money, filings and safety monitors: grants, contracts, SBIR/STTR topics, SEC financials, clinical trials, Federal Register, recalls, VIN decode.
- [`panda-web-security-tools`](https://github.com/pandadad0214/panda-web-security-tools) — Site, email and agent safety: SPF/DKIM/DMARC audits, AI/SEO readiness, website change monitoring, hidden AI instructions scanner, bulk domain WHOIS/expiry, broken link checker.

Index / compatibility mega-server: [panda-federation-tools](https://github.com/pandadad0214/panda-federation-tools) (use only when you truly need every tool).

## TDQS standard

New tools join this domain only while the count stays in the 3–15 band. Descriptions follow the checklist in the umbrella repo. See [tdqs-standard](https://github.com/pandadad0214/panda-federation-tools) / project docs.

Built by Panda Federation. MIT licensed.
