**Install** from [PyPI](https://pypi.org/project/panda-leads-tools/) (needs [uv](https://docs.astral.sh/uv/) and a free [Apify token](https://console.apify.com/settings/integrations)):

```bash
uvx panda-leads-tools@{{VERSION}}
```

- **Cursor / Claude / VS Code:** command `uvx`, args `["panda-leads-tools"]`, env `APIFY_TOKEN`.
- Official MCP Registry name: `io.github.pandadad0214/panda-leads-tools`.

### Changed
- Syncs the leads domain with panda-federation-tools 1.8.0 (40 tools across four focused servers). Still 15 tools after a rebalance: adds `colorado_new_business_leads` and `france_company_leads`; `topic_trends_tracker` moves to `panda-research-tools` and `eu_ted_tenders` moves to `panda-public-funding-tools`.
- Requires `panda-federation-tools>=1.8.0,<2`.

Full docs: [README](https://github.com/pandadad0214/panda-leads-tools#readme).
