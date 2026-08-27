# Email Inactivity Survival Guide

A single-page, static reference site covering the free-account inactivity policies of 11 email providers (Tuta, Zoho, Proton, Autistici/Inventati, Mailfence, Disroot, Murena, Secria, Atomic Mail, Aster, and Gmail/Google Account), sourced from each provider's own official documentation.

This package takes your original HTML content **completely unchanged** — no facts, figures, quotes, or wording were altered — and wraps it in a more capable, interactive front end.

## What's inside

```
index.html   → the full site (open this file directly, or deploy it)
README.md    → this file
```

Everything lives in one self-contained HTML file. No build step, no dependencies, no server required.

## Features added on top of your original content

- **Live search & filter** — both the comparison table and the provider-by-provider cards can be filtered instantly by keyword and by risk level (Critical / High / Safe / Unspecified), with a live "X of 11 providers shown" counter.
- **Next check-in calculator** — pick a provider and your last login date, and it works out a safe check-in date with a built-in buffer, entirely client-side (nothing is sent anywhere). Flags overdue or soon-due dates in red/amber.
- **Dark mode** — toggle in the top nav, remembers your choice (via `localStorage`), and also respects your OS's light/dark preference on first visit.
- **Sticky navigation bar** — quick jump links to Compare, Providers, Calculator, Strategy, and Sources sections.
- **Print / Save as PDF button** — triggers the browser's print dialog with a print-friendly stylesheet (already present in your original CSS, now wired to a button).
- **Back-to-top button** — appears after scrolling, for easy navigation on a long page.
- **Responsive** — the original responsive breakpoints are preserved and extended to the new nav/search/calculator UI.

No original text, statistics, quotations, or source links were removed, reworded, or reordered. All additions are new UI chrome and interactive tooling layered around your existing content.

## How to open it locally

Just double-click `index.html`, or open it in any browser. No installation needed.

## How to publish it (GitHub Pages)

1. Create a new **public** repository on GitHub.
2. Upload `index.html` (keep the filename exactly as `index.html` — GitHub Pages uses it as the homepage).
3. Go to the repo's **Settings → Pages**.
4. Under **Build and deployment → Source**, choose **Deploy from a branch**.
5. Set **Branch** to `main` and folder to `/ (root)`, then **Save**.
6. Wait 1–2 minutes. Your site will be live at:
   `https://<your-username>.github.io/<repo-name>/`

### Optional: custom domain
In the same Pages settings screen, enter your domain under **Custom domain**, then create a `CNAME` (or `A`) DNS record with your domain provider pointing to GitHub's Pages servers.

## Updating the content later

Because everything is in one HTML file, you can open it in any text editor and edit the provider cards, table rows, or source links directly — no rebuild step needed. If you add a new provider, follow the existing pattern for:
- a `<tr class="datarow" data-risk="...">` row in the comparison table, and
- a matching `<article class="datacard card ...">` block in the "Provider evidence" section

so it's automatically picked up by the search and filter features.

## Disclaimer

This is a personal reference document, not legal or professional advice. Provider policies can change at any time — always verify current terms directly on the provider's official site before relying on any date in this guide.
