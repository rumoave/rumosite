# rumoave.com

The RumoAve website. A civic-technology company building software that makes legislation legible and representation accountable.

## Stack
Static HTML, no build step. Single `index.html` with embedded CSS, plus brand assets in `/assets`.

## Local preview
Open `index.html` in a browser. That's it.

## Deploy
Connected to Vercel. Every push to `main` deploys automatically.

```bash
git add .
git commit -m "your change"
git push
```

## Structure
```
.
├── index.html          # Full site
├── assets/
│   ├── rumoave-mark.png
│   └── civly-mark.png
├── vercel.json
├── .gitignore
└── README.md
```
