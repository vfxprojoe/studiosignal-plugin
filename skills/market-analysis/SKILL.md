---
name: market-analysis
description: >
  M&E sector stock and market analysis guidance. Triggers on stock questions,
  market data requests, or financial analysis of media & entertainment companies.
  Covers the 30+ tickers tracked by Studio Signal.
---

# M&E Market Analysis

When the user asks about M&E stocks, market data, or financial analysis, use the Studio Signal `get_stocks` tool and this domain knowledge to provide expert market intelligence.

## Tracked M&E Universe (30+ Tickers)

### Major Studios & Streamers
| Ticker | Company | Key Metrics to Watch |
|--------|---------|---------------------|
| NFLX | Netflix | Subscribers, ARPU, content spend, ad tier growth |
| DIS | Walt Disney Co | Parks revenue, D+ subs, ESPN strategy, Hulu integration |
| CMCSA | Comcast (NBCUniversal/Peacock) | Broadband subs, Peacock losses, theme parks |
| WBD | Warner Bros Discovery | Debt reduction, Max subs, theatrical performance |
| PARA | Paramount Global | Merger status, Paramount+ trajectory, linear decline |
| SONY | Sony Group | Pictures segment, gaming (PS5), music (catalog value) |

### Streaming & Digital
| Ticker | Company | Key Metrics |
|--------|---------|-------------|
| ROKU | Roku | Platform revenue, ARPU, active accounts, ad growth |
| SPOT | Spotify | MAU growth, podcast investment, gross margin trajectory |
| FUBO | fuboTV | Sports-first streaming, subscriber growth, path to profitability |

### Tech Platforms
| Ticker | Company | Key Metrics |
|--------|---------|-------------|
| GOOG | Alphabet (YouTube) | YouTube ad revenue, YouTube TV subs, AI integration |
| AAPL | Apple | Services revenue, Apple TV+ investment, Vision Pro |
| AMZN | Amazon | Prime Video, MGM integration, Thursday Night Football |
| META | Meta Platforms | Reels monetization, VR/AR investment, creator tools |

### Gaming
| Ticker | Company | Key Metrics |
|--------|---------|-------------|
| MSFT | Microsoft | Xbox/Game Pass, Activision integration, cloud gaming |
| EA | Electronic Arts | Live services, FIFA/EA Sports FC, mobile |
| TTWO | Take-Two | GTA franchise, NBA 2K, Zynga mobile |
| RBLX | Roblox | DAU growth, bookings, creator economy, aging up |

### Music & Live
| Ticker | Company | Key Metrics |
|--------|---------|-------------|
| LYV | Live Nation | Concert revenue, Ticketmaster, sponsorship |
| MSGS | MSG Sports | Venue revenue, team valuations |
| MSGE | MSG Entertainment | Sphere (Las Vegas), touring acts |

### Ad Tech & Infrastructure
| Ticker | Company | Key Metrics |
|--------|---------|-------------|
| TTD | The Trade Desk | CTV ad spend, programmatic growth, UID 2.0 |

### Market Index
| Ticker | Description |
|--------|-------------|
| ^GSPC | S&P 500 (benchmark for relative performance) |

## Analysis Framework

When analyzing M&E stocks, always consider:

1. **Sector-Specific Drivers**
   - Content calendar (tentpole releases, sports rights renewals)
   - Subscriber metrics (growth, churn, ARPU)
   - Ad market health (upfront commitments, CPM trends)
   - Regulatory environment (antitrust, AI regulation)

2. **Macro Attribution**
   - Interest rate sensitivity (highly leveraged media companies)
   - Consumer discretionary spending trends
   - Currency impact on international revenue
   - Tech sector rotation effects

3. **Comparative Analysis**
   - Always compare to S&P 500 benchmark
   - Group peers: Streamers (NFLX vs DIS vs WBD), Gaming (EA vs TTWO vs RBLX)
   - Track sector leadership rotation

4. **Catalyst Mapping**
   - Earnings dates and expectations
   - Content launches (major franchise releases)
   - Rights renewal cycles (NFL, NBA, etc.)
   - M&A activity and regulatory approvals

## Using the Tools

- Call `get_stocks` for current prices, changes, market caps, and analyst ratings
- Filter by specific symbols: `get_stocks` with `symbols: "NFLX,DIS,WBD"` for comparisons
- Combine with `ask_kai` for fundamental analysis beyond price data
- Use `get_daily_brief` for context on what's driving today's movements
