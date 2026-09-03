# Runrate — corporate budgeting tool

A single-file, self-contained budgeting tool. It is **not** Velo page code — the
Wix Editor's page elements aren't available to this repo, so this lives
alongside the site's code as a standalone HTML file you can:

- Open `index.html` directly in a browser.
- Host it anywhere static files are served.
- Embed it in a Wix page via an **HTML iframe / Embed a Widget** element,
  pointing at wherever you host `index.html`.

## What it does

- Log budget line items as **credits** (revenue) or **debits** (expenses),
  each entered at whatever cadence is natural — weekly, fortnightly, monthly,
  quarterly, yearly, or a custom number of days.
- Switch the whole dashboard's "View as" timeframe to see every line
  converted to that cadence, with a per-line breakdown table and summary
  tiles (credits, debits, net, and an annualized run-rate).
- **Extrapolate**: pick a horizon (number of periods) and a start date, add
  an optional annual growth rate per line, and see a projected net-per-period
  chart plus a cumulative balance chart, with a shortfall warning if the
  balance is projected to go negative.

Data is kept in the browser's `localStorage`, seeded with example figures for
a small SaaS company on first load. Day-count basis: 365.25 days/year,
fortnight = 14 days, month = 30.44 days, quarter = 91.31 days.

No build step, no dependencies beyond a Google Fonts stylesheet (IBM Plex
Serif/Sans/Mono) loaded over HTTPS.
