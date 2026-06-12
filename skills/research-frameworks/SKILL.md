---
name: research-frameworks
description: >
  MBA-level analytical frameworks for media & entertainment analysis. Use when the user
  requests strategic analysis, competitive assessments, financial modeling, or industry
  deep dives. Includes 30+ frameworks from competitive battlecards to IP Valuation.
---

# M&E Research Frameworks

Studio Signal auto-selects the best framework server-side when you call `ask_kai`. Your job is to **phrase queries clearly** so the right framework activates. Prefer `ask_kai` for grounded analysis — do not substitute your own unsourced framework write-ups.

## Query phrasing guide (critical)

| User intent | Example query to pass to `ask_kai` | Framework activated |
|-------------|-----------------------------------|---------------------|
| Head-to-head vendor/product comparison | "Competitor research: Signiant vs IBM Aspera vs Media Shuttle" | **competitive** (NOT SWOT) |
| Single-company positioning | "Analyze Frame.io's market positioning and ideal buyer profile" | **competitive** |
| Explicit SWOT/TOWS | "SWOT analysis of Warner Bros Discovery" | **swot** |
| Moats / durable advantage | "Does Spotify have a durable competitive advantage?" | **sevenpowers** |
| Industry structure | "Porter's Five Forces in the FAST channel market" | **porters** |
| Earnings / stock | "Disney Q2 earnings breakdown with key metrics" | **financial** |
| FAST / AVOD / CTV ads | "FAST and CTV ad economics — CPM and fill rate trends" | **adeconomics** |
| Creator M&A | "Creator economy M&A — recent MCN and creator-studio deals" | **creatorma** |
| AI disruption | "How is AI affecting localization vendors?" | **aiimpact** |

**Do NOT** say "SWOT" or "TOWS" for competitor bake-offs — say "competitor research" or "head-to-head comparison" instead.

## Framework catalog (30+)

### Comparison & strategy
- **competitive** — Battlecard / head-to-head product & vendor comparisons (B2B media-tech, workflow tools)
- **swot** — SWOT/TOWS (only when user explicitly requests SWOT)
- **porters** — Five Forces (industry structure, not product bake-offs)
- **sevenpowers** — Hamilton Helmer 7 Powers (single-company moats)
- **bcg** — Growth-Share Matrix
- **pestle** — Macro factor scan
- **disruption** — Christensen disruption theory
- **scenario** — Bull/base/bear futures
- **blueocean** — Value innovation (explicit request)
- **growth** — Ansoff matrix (explicit request)

### Financial & unit economics
- **financial** — Earnings, valuation, margins, solvency
- **revenue** — Revenue model decomposition (SVOD/AVOD/licensing/etc.)
- **adeconomics** — FAST/AVOD/CTV ad market economics
- **tam** — TAM/SAM/SOM sizing
- **saas** — SaaS KPIs for streaming/platforms
- **subscriberlifecycle** — Cohorts, churn, LTV

### M&E-specific
- **ipvaluation** — Content library & franchise valuation
- **windowing** — Release window economics
- **sportsrights** — Sports media rights deals
- **production** — Production economics (ATL/BTL, tax credits, guilds)
- **talentdeals** — Talent deal structures & residuals
- **creatorma** — Creator economy M&A and roll-ups
- **greenlight** — Theatrical greenlight / comp analysis
- **aiimpact** — AI across the M&E value chain
- **networkeffects** — Network effects + flywheel dynamics

### Explicit-request only (server will not auto-select)
vrio, mckinsey7s, wardley, jtbd, canvas, flywheel — user must name these in the query.

## Output expectations

Kai returns markdown reports. For matrix-style frameworks (SWOT, Porter's, 7 Powers):
- Expect **subsection headers + bullets**, not wide tables
- Competitive research uses **### per competitor**, not TOWS grids

## Data accuracy

- Cite deal values and metrics only from Kai's sourced report — not from this skill's examples
- Historical comps in training data (MGM/Amazon, NFL rights deals, etc.) may be stale; always use live `ask_kai` output

## How to apply

1. **Prefer `ask_kai`** — pass a clear, framework-aligned query string
2. **One framework per query** unless user asks for comprehensive multi-framework review
3. **Competitor research ≠ SWOT** — use competitive battlecard phrasing
4. **Layer context** — combine with `get_daily_brief` or `get_stocks` when relevant, then call `ask_kai` with that context in the query
