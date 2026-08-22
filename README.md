# First Position — a beginner's risk/return screener

A single-file HTML app for screening stocks and ETFs by risk fit, not by price predictions. Built around one idea: nobody reliably calls short-term tops and bottoms, so the app focuses on risk-matching and a disciplined entry/exit process instead of fake "buy here, sell there" calls.

## What it does

- Preset screener — 10 common starter ETFs/stocks (VOO, VTI, SCHD, QQQ, VXUS, BND, JEPI, KO, AAPL, MSFT) scored against your time horizon and risk tolerance, using illustrative long-run historical averages.
- - Risk/return map — a scatter chart plotting volatility against historical return for the preset list.
  - - Analyze any stock
    -   - Quick lookup — type a ticker, and it runs a live web search (via the Anthropic API) to pull current price, financials, ownership structure, dividend yield, and recent news, then gives a rule-based tier verdict plus an honest AI critique.
        -   - Manual entry — paste in numbers yourself (price, market cap, EPS, beta, 52-week range, ownership %) for instant rule-based scoring plus an AI read, no search needed.
            -   - Both modes include a 52-week range position graph, a "$100 six months ago" hypothetical case study, and an interactive price-trend chart with 1M/3M/6M/1Y range tabs (built from real verified anchor points, not fabricated intraday data).
                - - Three market scanners, each running live web search against a strict rule set:
                  -   - General Tier — quality "fallen angel" companies down 10–30% off highs on temporary news, with a real 6–12 month catalyst.
                      -   - Tier 1 — mega-cap ($100B+) blue-chip compounders with a moat and valuation setup.
                          -   - Tier 2 — sub-$20 high-growth compounders, market cap $2B+, no micro-caps.
                              - - Entry/exit framework — dollar-cost averaging, rebalancing bands, valuation as a caution light (not a signal), and writing exit rules in advance.
                               
                                - ## Important limitations (read before using)
                               
                                - - This is not financial advice. Nothing here is a recommendation — it's a screening tool. Consult a licensed financial advisor for anything beyond a small first position.
                                  - - The live AI features (quick lookup, manual-entry critique, all three scanners) only work when this file is opened through Claude.ai's file preview, because that's what authorizes the calls to the Anthropic API. Opening the file locally in a browser, or hosting it elsewhere (including GitHub Pages), will not make those buttons work — the fetch calls have no valid authorization outside that environment.
                                    - - No live ticker feed or news wire. Every lookup is an on-demand research pass, not a continuous background feed.
                                      - - No true intraday ("1D") chart. The trend chart connects real verified price points (now / 1mo / 3mo / 6mo / 1yr) with straight lines — an honest approximation, not reconstructed tick-by-tick data.
                                        - - Preset screener figures are illustrative, approximate long-run averages that may be stale — verify against a live source before acting.
                                         
                                          - ## Usage
                                         
                                          - Open first-position-screener.html in Claude.ai's file preview to get the full interactive experience including live AI research. Opened elsewhere, the static preset screener, risk/return map, and manual entry's rule-based scoring (no AI critique) still work locally in any modern browser.
                                         
                                          - ## License
                                         
                                          - No license specified — all rights reserved by default. Add a license file if you want to allow reuse.
