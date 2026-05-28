---
name: daily-workflow
description: >
  Guide Claude through the Studio Signal daily M&E intelligence workflow.
  Triggers on "morning brief", "daily intel", "what happened today in M&E",
  "today's brief", or any request for daily media & entertainment updates.
---

# Daily M&E Intelligence Workflow

When the user asks for daily M&E intelligence, follow this workflow using the Studio Signal MCP tools. This gives them a comprehensive morning briefing experience.

## Workflow Steps

### 1. Fetch the Daily Brief
Call `get_daily_brief` to retrieve today's executive intelligence brief. This is generated every morning before market open and includes:
- Top M&E stories ranked by strategic impact
- Market movers and stock movements
- Key themes and trends
- Watch list items

Present the brief with clear formatting — headlines, impact assessments, and market data.

### 2. Check Market Data
Call `get_stocks` to get current M&E sector stock data. Highlight:
- Biggest movers (up and down) among the 30+ tracked M&E stocks
- Any stocks mentioned in the daily brief
- Overall sector trend vs. broader market

### 3. Offer the Deep Dive
After presenting the brief and market overview, offer to fetch the deep dive analysis using `get_deep_dive`. The deep dive expands on the morning brief's most impactful story with:
- Comprehensive strategic analysis
- Competitive implications
- Market outlook and recommendations

### 4. Follow-Up Research
Based on the brief and deep dive, suggest specific research questions the user might want to explore via `ask_kai`. For example:
- "Want me to do a deep analysis of [company mentioned in brief]?"
- "Should I look at the competitive implications of [deal/event from brief]?"
- "Want me to pull the earnings details for [company that moved significantly]?"

## Presentation Guidelines

- Lead with the most impactful story — don't bury the lead
- Use the stock data to add quantitative context to qualitative stories
- Connect dots between stories when themes overlap
- Always mention if the daily podcast is available
- End with actionable follow-up options

## Trigger Phrases
Activate this workflow when the user says things like:
- "What's happening in M&E today?"
- "Give me today's brief"
- "Morning briefing"
- "Daily intel"
- "What did I miss in media today?"
- "Catch me up on entertainment news"
