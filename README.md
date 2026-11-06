# Panda Leads Tools

**Public leads and enrichment: NPI providers, podcasts, local businesses, hiring signals, website enrichment, team pages, topic trends, trucking carriers.**

Focused MCP server (8 tools) from the [Panda Federation](https://github.com/pandadad0214/panda-federation-tools) public-data toolkit. Prefer this over the 23-tool mega-server for better Tool Definition Quality Score (TDQS) / Glama coherence.

[![Umbrella](https://img.shields.io/badge/index-panda--federation--tools-blue)](https://github.com/pandadad0214/panda-federation-tools)
[![Apify Store](https://img.shields.io/badge/Apify_Store-pandadad0214-00a3ff)](https://apify.com/pandadad0214)
[![License: MIT](https://img.shields.io/badge/license-MIT-green)](LICENSE)

## Install / Use

Needs a free [Apify API token](https://console.apify.com/settings/integrations) and [uv](https://docs.astral.sh/uv/).

```bash
uvx --from panda-federation-tools panda-leads-tools
```

Same entry point from this repo:

```bash
uvx --from git+https://github.com/pandadad0214/panda-leads-tools panda-leads-tools
```

Cursor / Claude / VS Code: command `uvx`, args `["--from", "panda-federation-tools", "panda-leads-tools"]`, env `APIFY_TOKEN`.

## Tools (8)

- `npi_provider_lists`
- `podcast_leads_finder`
- `local_business_leads`
- `company_hiring_signals`
- `company_website_enricher`
- `company_team_finder`
- `topic_trends_tracker`
- `trucking_company_leads`

Each tool runs one Apify Actor on your account. Empty runs are not charged per result; every call is capped by `run_max_charge_usd`. Full schemas and prices: [umbrella README](https://github.com/pandadad0214/panda-federation-tools#domain-tool-lists).

## Sibling domain servers

- [`panda-research-tools`](https://github.com/pandadad0214/panda-research-tools) — Scholarly integrity and papers: citation checks, literature and PubMed search, academic experts, PDF tables.
- [`panda-public-funding-tools`](https://github.com/pandadad0214/panda-public-funding-tools) — US federal money and filings: grants, contracts, SBIR/STTR topics, SEC financials, clinical trials.
- [`panda-web-security-tools`](https://github.com/pandadad0214/panda-web-security-tools) — Site, email and agent safety: SPF/DKIM/DMARC audits, AI/SEO readiness, website change monitoring, hidden AI instructions scanner.

Index / compatibility mega-server: [panda-federation-tools](https://github.com/pandadad0214/panda-federation-tools) (use only when you truly need every tool).

## TDQS standard

New tools join this domain only while the count stays in the 3–15 band. Descriptions follow the checklist in the umbrella repo. See [tdqs-standard](https://github.com/pandadad0214/panda-federation-tools) / project docs.

Built by Panda Federation. MIT licensed.
