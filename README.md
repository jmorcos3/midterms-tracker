# Midterms 2026 Live Tracker

Live page: https://jmorcos3.github.io/midterms-tracker/

A single static page (`index.html`) that pulls prediction-market odds for the
2026 midterms: Senate and House control, balance-of-power combinations,
seat-count distributions, the contested Senate and governor races, and
state-level House seat markets.

- **Polymarket** prices are fetched live from the browser every 60 seconds
  (Gamma API; intraday lines from the CLOB price-history endpoint).
- **Kalshi** blocks browser requests, so `fetch_kalshi.py` runs on a GitHub
  Actions schedule every 10 minutes during election week and commits the
  result to `kalshi.json`, which the page reads.

Race ratings shown on the cards are the final pre-election Cook Political
Report ratings. Starting compositions: Senate 53 R / 47 D; House 218 R /
214 D / 1 I / 2 vacant; governors 26 R / 24 D.
