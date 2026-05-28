# 📡 Studio Signal — Claude Plugin

[![npm](https://img.shields.io/npm/v/@studiosignal/mcp-server)](https://www.npmjs.com/package/@studiosignal/mcp-server)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)

**Give Claude native M&E intelligence.** This plugin connects Studio Signal's AI-powered media & entertainment research platform directly into Claude Code and Claude Cowork — making Claude an expert M&E analyst out of the box.

> **Studio Signal** is the M&E intelligence platform used by media executives, analysts, and investors.
> This plugin gives Claude the same tools and domain expertise, powered by live ground truth.

## ⚡ Quick Install

### Claude Code
```bash
/plugin marketplace add vfxprojoe/studiosignal-plugin
```

### Manual Install
```bash
/plugin install --dir /path/to/studiosignal-plugin
```

## 🔑 Setup

You'll need a Studio Signal API key (free at [developer.studiosignal.app](https://developer.studiosignal.app)):

```bash
export STUDIO_SIGNAL_API_KEY=ss_live_your_key_here
```

## 📦 What's Included

### MCP Tools (6)

| Tool | What it does |
|------|-------------|
| `ask_kai` | Ask Kai Rivers any M&E research question — sourced, citation-backed analysis |
| `get_daily_brief` | Today's executive intelligence brief — top stories, market movers |
| `get_deep_dive` | In-depth analysis of the day's most significant M&E story |
| `get_stocks` | Live stock data for 30+ M&E companies |
| `generate_linkedin` | Transform research into a LinkedIn post |
| `get_usage` | Check API usage stats |

### Skills (4)

| Skill | What it adds |
|-------|-------------|
| `me-domain` | Core M&E industry domain knowledge — streaming, film, music, gaming, VFX, creator economy |
| `research-frameworks` | 20+ MBA-level analytical frameworks adapted for M&E (SWOT, Porter's, DCF, IP Valuation, etc.) |
| `daily-workflow` | Morning intelligence workflow — brief → market data → deep dive → research |
| `market-analysis` | M&E sector stock analysis — 30+ tracked tickers, sector groupings, catalyst mapping |

### Slash Commands (4)

| Command | Action |
|---------|--------|
| `/studio-signal:brief` | Fetch today's executive intelligence brief |
| `/studio-signal:stocks` | Get M&E sector market overview |
| `/studio-signal:research` | Research any M&E topic via Kai |
| `/studio-signal:deep-dive` | Fetch today's deep dive analysis |

### Agent (1)

| Agent | What it does |
|-------|-------------|
| `kai-analyst` | Multi-step research agent — gathers context, checks markets, runs deep research, synthesizes findings |

## 💡 Example Usage

Once installed, just ask naturally:

- *"What's happening in M&E today?"* — triggers the daily workflow
- *"Analyze Netflix's competitive position"* — calls ask_kai with frameworks
- *"Show me M&E stocks"* — fetches live market data
- *"Do a full analysis of the Disney-ESPN situation"* — invokes the kai-analyst agent

## 🏗 Plugin Structure

```
claude-plugin/
├── .claude-plugin/
│   ├── plugin.json          # Plugin manifest
│   └── marketplace.json     # Marketplace catalog
├── .mcp.json                # MCP server bundle
├── skills/
│   ├── me-domain/           # M&E industry domain knowledge
│   ├── research-frameworks/ # 20+ analytical frameworks
│   ├── daily-workflow/      # Daily intel workflow
│   └── market-analysis/     # Stock/market analysis
├── commands/
│   ├── brief.md             # /studio-signal:brief
│   ├── stocks.md            # /studio-signal:stocks
│   ├── research.md          # /studio-signal:research
│   └── deep-dive.md         # /studio-signal:deep-dive
├── agents/
│   └── kai-analyst.md       # Multi-step research agent
├── README.md
└── LICENSE
```

## 📊 API Pricing

### Free Trial (No credit card required)
- **50 API calls** across all tools
- **7-day trial window**

### Pay-as-you-go
| Volume | Rate per call |
|--------|---------------|
| First 1,000 | $0.15 |
| 1,001 – 10,000 | $0.10 |
| 10,001+ | $0.07 |

Track usage anytime with the `get_usage` tool or `/studio-signal:usage`.

## 🔗 Links

- **Platform**: [studiosignal.app](https://studiosignal.app)
- **Developer Portal**: [developer.studiosignal.app](https://developer.studiosignal.app)
- **npm (MCP Server)**: [@studiosignal/mcp-server](https://www.npmjs.com/package/@studiosignal/mcp-server)

## 🔒 Privacy

- Queries are processed by Google's Gemini AI — Google does not retain prompt data beyond the request
- API keys and usage logs stored in encrypted databases (Neon/AWS US-East)
- No query data sold or shared with third parties
- Full policy: [studiosignal.app/legal](https://studiosignal.app/legal)

## 📄 License

MIT — © [Harkins Capital, LLC](https://harkins.capital)
