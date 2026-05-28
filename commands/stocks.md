---
name: stocks
description: Get live M&E sector stock data — prices, changes, sparklines, and analyst ratings for 30+ media & entertainment companies.
---

Fetch current M&E stock data using the `get_stocks` tool.

Present the results as a clean market overview:
1. Overall sector trend (how many up vs down)
2. Biggest movers (top 3 gainers and top 3 losers by % change)
3. Full table with ticker, price, change %, and analyst rating
4. Any notable analyst rating changes

If the user asks about specific stocks, filter with the `symbols` parameter (e.g., `symbols: "NFLX,DIS,WBD"`).

After presenting, offer to analyze any specific stock in depth via `ask_kai`.
