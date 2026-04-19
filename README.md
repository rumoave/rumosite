# RumoAve

> Democratizing democracy. Building CivTech to enhance engagement and foster transparency between government and constituents.

This is the source for [rumoave.com](https://rumoave.com), the one-page marketing site for RumoAve, a civic-technology company based in New York City.

## Stack

This is intentionally simple: a single static HTML file with no build step, no bundler, and no framework dependencies. Fonts are loaded from Google Fonts, the logo is inlined as base64, and the site works as-is when you double-click `index.html` locally.

- **HTML / CSS** — single file, ~45KB total
- **Typography** — SF Pro Display / New York on Apple devices, with Source Serif 4 and Inter Tight as fallbacks
- **Live data** — U.S. Treasury Fiscal Data API (Debt to the Penny) for the real-time national debt ticker, fetched client-side
- **Hosting** — Vercel
- **DNS** — Namecheap

## Structure

```
rumoave/
├── index.html      # The entire site
└── README.md       # This file
```

That's it. One file. If it ever grows beyond that, split things out; until then, resist the urge.

## Local development

No build step. Just open the file:

```bash
# macOS
open index.html

# Linux
xdg-open index.html

# Or serve it locally if you want to test real fetch calls
python3 -m http.server 8000
# then visit http://localhost:8000
```

Any text editor works for edits. VS Code with the Live Server extension is the smoothest dev loop.

## Deployment

Deploys happen automatically on push to `main` via Vercel's GitHub integration. Manual deploy from the CLI:

```bash
vercel --prod
```

## Data sources

The stats on the site are all drawn from public government and nonprofit data:

- **National debt ticker** — [U.S. Treasury Fiscal Data](https://fiscaldata.treasury.gov/datasets/debt-to-the-penny/), refreshed hourly, extrapolated between updates from the 30-day trailing average growth rate
- **Dark money** — [Brennan Center for Justice](https://www.brennancenter.org/our-work/research-reports/dark-money-hit-record-high-19-billion-2024-federal-races) and [OpenSecrets](https://www.opensecrets.org/)
- **Pentagon audits** — [Department of Defense Office of Inspector General](https://www.dodig.mil/) FY2024 audit report
- **FISA court** — [Stanford Law Review](https://www.stanfordlawreview.org/online/is-the-foreign-intelligence-surveillance-court-really-a-rubber-stamp/) and [EPIC FISA statistics](https://epic.org/foreign-intelligence-surveillance-court-fisc/fisa-stats/)
- **Federal lobbying** — [OpenSecrets federal lobbying dataset](https://www.opensecrets.org/federal-lobbying/)

If you find an error or a better source, open an issue.

## Contact

Carlos — [carlos@rumoave.com](mailto:carlos@rumoave.com)

## License

All rights reserved. The code, design, and content of this site are the property of RumoAve, Inc. Not currently licensed for reuse. If you want to build something civic-tech adjacent and think we can help, reach out.
