# Health Statistics MCP Server

Life expectancy, causes of death, health spending, healthcare resources and population health from WHO, Eurostat, OECD and the World Bank.

Remote MCP server (Streamable HTTP), read-only, hosted by [Monitly](https://monit.ly).

```
https://monit.ly/api/mcp/health
```

## Tools

| Tool | What it does |
|---|---|
| `search_catalog` | Find health datasets by topic, country and source. |
| `inspect_dataset` | Check country coverage, dimensions and the latest values. |
| `get_dataset` | Dataset metadata and period range. |
| `get_series` | Time series for one country. |

## Example prompts

- What is life expectancy in Japan compared with the EU average?
- Show health expenditure as % of GDP in Germany over time.
- How many hospital beds per 1,000 people does Poland have?

## Authentication

No account or key is needed. A fair-use daily limit applies; for higher volumes use the keyed Monitly MCP at https://monit.ly/mcp-docs.

## Setup

**Claude (claude.ai, Desktop):** Settings → Connectors → Add custom connector → paste the URL above.

**Cursor / VS Code / Windsurf** (`mcp.json`):

```json
{
  "mcpServers": {
    "health-statistics": {
      "url": "https://monit.ly/api/mcp/health"
    }
  }
}
```

**ChatGPT:** Settings → Apps → Developer mode → Create → paste the URL.

## About

Part of the [Monitly](https://monit.ly/mcp-docs) MCP family. Full Monitly catalog (100,000+ datasets, all topics): https://monit.ly/api/mcp/public.

Questions: info@monit.ly

## Gemini CLI

```bash
gemini extensions install https://github.com/ContentWriterco/Health-Statistics-MCP
```

No account or key needed.

## Setup guides

Step-by-step setup guides for Claude, ChatGPT, Gemini, Grok, Le Chat, Perplexity, Cursor, VS Code and Claude Code: https://monit.ly/mcp/connect
