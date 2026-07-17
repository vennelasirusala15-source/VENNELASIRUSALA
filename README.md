# Vennela Sirusala — Portfolio Site

A single-page, editorial-style personal portfolio built as static HTML/CSS (no build step, no dependencies to install).

## What's inside

```
site/
├── index.html          ← the whole site (structure + styling in one file)
├── assets/              ← all photos, certificate images, and project thumbnails used on the page
└── README.md            ← this file
```

The design concept is a "field journal" — it ties your agriculture background and sustainability values to your supply chain career through an editorial layout: dated entries, captions, pull quotes, and a zigzag travel narrative.

## Sections on the page

| Section | Content |
|---|---|
| Hero | Headshot, headline, positioning toward corporate analytics (supply chain, marketing, SCM, OSCM) |
| Story | Agriculture-to-supply-chain narrative with fieldwork photos |
| Work (Live projects) | Your 4 GitHub repos, each with a custom-designed PNG thumbnail and a link to the repo |
| Mission | Motto — "Dream Big. Build Boldly. Lead with Purpose." — plus your Vision and Mission statements |
| Experience | ALSO Group, Temper, Aashman Foundation, Just Agriculture |
| Academic projects | Achal Cashews, Baker Hilvers, FMCG Fruit Juice, Van Balen |
| Field notes | Chronological timeline from B.Sc. Agriculture through TIAS graduation |
| The journey, in seven countries | Zigzag photo-story: India, Netherlands, Germany, Italy, Bahrain, Doha, Belgium — each with a 5-line story |
| Certifications | Six Sigma, Guest Speaker, Strategic Management + skills & languages |
| Contact | Email, phone, LinkedIn, GitHub |

## The 4 live projects

Each card has a custom PNG thumbnail (`assets/thumb-kpi.png`, `thumb-sql.png`, `thumb-rfm.png`, `thumb-sap.png`) designed in the site's palette, and links to:

1. [Supply Chain KPI Dashboard](https://github.com/vennelasirusala15-source/Power-BI-Supply-Chain-Dashboard) — Power BI
2. [Order Fulfilment Analysis](https://github.com/vennelasirusala15-source/-SQL-Order-Fulfilment-Analysis-) — SQL
3. [Customer Segmentation & RFM](https://github.com/vennelasirusala15-source/marketing-rfm-powerbidashboard) — Power BI
4. [Order-to-Cash Case Study](https://github.com/vennelasirusala15-source/e-SAP-Order-to-Cash-Case-Study) — SAP SD

If you get real dashboard screenshots later, just swap the `src="assets/thumb-*.png"` path on that project's `<img>` tag to your new file.

## The seven-country section

A zigzag layout — photo on one side, a 5-line story on the other, alternating left/right down the page — covering India, Netherlands, Germany, Italy, Bahrain, Doha, and Belgium. Bahrain and Doha are shown as flight-icon "stopover" entries since they were layovers rather than photographed stays; swap in a real photo any time by replacing the `.zphoto-icon` div with `<div class="zphoto"><img src="assets/your-photo.jpg"></div>`.

## Positioning

Copy across the site was written to target **corporate analytics roles in supply chain, marketing, SCM, and OSCM** — warehouse/logistics-floor language has been minimized in favor of analytics, strategy, and process-improvement framing.

## How to view it locally

Just double-click `index.html` — it opens directly in any browser. No server needed.

## How to make quick edits

Everything is in `index.html`. To change text, search for the words you want to change and edit them directly — it's plain HTML, no templating.

To swap a photo: replace the file in `assets/` **with the same filename**, or change the `src="assets/…"` path in `index.html` to point at a new filename.

Remaining placeholder still to fill in:
- A certificate image for **Basics of Strategic Management** in the **Certifications** section

## How to deploy (Netlify)

1. Go to [app.netlify.com](https://app.netlify.com) and log in
2. On your site's overview page, find **Production deploys**
3. Drag the whole `site` folder onto the "Drag and drop your project folder here" area
4. Netlify redeploys automatically — check the live URL once it finishes

**Important:** always drag the whole `site` folder together (not just `index.html` on its own), or the photos and thumbnails won't load since they're linked as relative paths inside `assets/`.

## Notes

- Fonts (Fraunces, Inter, IBM Plex Mono) load from Google Fonts via CDN — an internet connection is needed for them to render with the correct typefaces; without it, the browser falls back to system fonts.
- The layout is responsive down to mobile (zigzag rows stack vertically, nav collapses at 880px width).
