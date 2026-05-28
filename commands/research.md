---
name: research
description: Ask Kai Rivers any M&E research question — competitive analysis, earnings, deal impact, market trends, and more.
---

Ask the user what they'd like to research, then call `ask_kai` with their query.

If the user provides a topic directly (e.g., `/studio-signal:research Netflix Q2 earnings`), pass it straight to `ask_kai`.

If no topic is provided, prompt: "What M&E topic would you like Kai to research? Examples: company analysis, earnings breakdown, competitive landscape, deal impact, market trends."

Present the research results with full formatting — headers, data points, source citations, and strategic analysis.

After presenting, offer follow-up options:
- Deeper analysis on a sub-topic
- Comparative analysis against a competitor
- Generate a LinkedIn post from the research (`generate_linkedin`)
