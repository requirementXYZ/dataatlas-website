# Handoff: DataAtlas Website — GitHub Publish

## Task

Publish the DataAtlas marketing website to a new public GitHub repository named **`dataatlas-website`** under the `requirementXYZ` organisation (or personal account as appropriate).

The files are complete, self-contained HTML pages — no build step required. They use vanilla HTML, CSS, and JavaScript only. The task is to:

1. Create the `dataatlas-website` GitHub repo (public)
2. Commit all files from this package into the repo root
3. Enable **GitHub Pages** on the repo (source: `main` branch, root folder `/`)
4. Confirm the live URL works

---

## About the Design Files

The files in this bundle are **production-ready static HTML pages** — not prototypes. They are fully functional, self-contained, and ready to be served as-is. No framework, no build pipeline, no dependencies beyond Google Fonts (loaded via CDN).

---

## Fidelity

**High-fidelity production output.** These are the final pages. Publish them exactly as provided — do not restyle, restructure, or convert to a framework.

---

## Files to Publish

| File | Purpose |
|------|---------|
| `DataAtlas Website.html` | Main marketing homepage — rename to `index.html` when publishing |
| `DataAtlas User Guide.html` | User documentation page |
| `DataAtlas Admin Guide.html` | Admin setup and configuration guide |
| `DataAtlas Brand.html` | Brand reference sheet (optional — can be included or omitted) |
| `screenshots/` | All product screenshot assets (light-app crops) |
| `screenshots/dark/` | Dark-mode screenshot variants |

> **Important:** Rename `DataAtlas Website.html` → `index.html` so it serves as the GitHub Pages root. Update the `href` links in the other HTML files accordingly (e.g. `href="index.html"` instead of `href="DataAtlas Website.html"`).

---

## Internal Links to Update

After renaming `DataAtlas Website.html` to `index.html`, update these references across all files:

### In `DataAtlas User Guide.html`
- `href="DataAtlas Website.html"` → `href="index.html"` (nav logo, back link, footer)

### In `DataAtlas Admin Guide.html`
- `href="DataAtlas Website.html"` → `href="index.html"` (nav logo, back link, footer)

### In `index.html` (was `DataAtlas Website.html`)
- Footer: `href="DataAtlas User Guide.html"` → keep as-is (filename unchanged)
- Footer: `href="DataAtlas Admin Guide.html"` → keep as-is (filename unchanged)

---

## Repository Structure

```
dataatlas-website/
├── index.html                        ← renamed from DataAtlas Website.html
├── DataAtlas User Guide.html
├── DataAtlas Admin Guide.html
├── DataAtlas Brand.html              ← optional
├── screenshots/
│   ├── 01-dashboard-governance-health.png
│   ├── 02-catalog-business-glossary.png
│   ├── 03-register-governed-assets.png
│   ├── 04-asset-detail-drawer.png
│   ├── 04b-asset-detail-data-shape.png
│   ├── 05-review-queue.png
│   ├── 06-requests-linked-intake.png
│   ├── 07-import-template-and-mapping.png
│   ├── 08-lineage-impact-graph.png
│   ├── 09-settings-governance-domains.png
│   ├── 10-service-portal-home.png
│   ├── 10-service-portal-home-full.png
│   ├── 10-import-step-1-upload.png
│   ├── 11-import-step-2-map.png
│   ├── 11-service-portal-measure-request.png
│   ├── 12-import-step-3-validate.png
│   ├── 13-import-step-4-duplicates.png
│   ├── 14-import-step-5-ready.png
│   └── dark/
│       ├── 01-dashboard-governance-health.png
│       ├── 02-catalog-business-glossary.png
│       ├── 03-register-governed-assets.png
│       ├── 04-asset-detail-drawer.png
│       ├── 04b-asset-detail-data-shape.png
│       ├── 05-review-queue.png
│       ├── 06-requests-linked-intake.png
│       ├── 07-import-template-and-mapping.png
│       ├── 08-lineage-impact-graph.png
│       ├── 09-settings-governance-domains.png
│       ├── 10-import-step-1-upload.png
│       ├── 11-import-step-2-map.png
│       ├── 12-import-step-3-validate.png
│       ├── 13-import-step-4-duplicates.png
│       └── 14-import-step-5-ready.png
```

---

## GitHub Pages Setup

After pushing:

1. Go to **Settings → Pages** in the repo
2. Set source to **Deploy from a branch**
3. Branch: `main`, folder: `/ (root)`
4. Save — the site will be live at `https://requirementxyz.github.io/dataatlas-website/`

---

## Design Tokens

| Token | Value |
|-------|-------|
| Primary (cyan) | `#22d3ee` |
| Pale (cyan-200) | `#a5f3fc` |
| Accent (sky-400) | `#38bdf8` |
| Violet | `#a78bfa` |
| Dark bg | `#080a0d` |
| Dark card | `#131820` |
| Light bg | `#f5f7fa` |
| Light card | `#ffffff` |
| Font | Inter Tight (Google Fonts) |

---

## Features

- **Dark / light mode** toggle with `localStorage` persistence and `prefers-color-scheme` support
- **Screenshot swap** — dark screenshots shown in dark mode, light screenshots in light mode
- **Sticky nav** with blur-on-scroll
- **FAQ accordion** (grouped by category)
- **Tabbed gallery** (stewardship section)
- **Lightbox** on all doc images (User Guide and Admin Guide) — click to enlarge, Escape to close
- **Sidebar nav** with IntersectionObserver active-link tracking (guide pages)
- **Responsive** — 3-col → 2-col → 1-col breakpoints at 900px and 600px
- **All CTAs** link to `https://marketplace.atlassian.com` (labelled "Coming Soon")

---

## Notes

- No build step. No package.json. No node_modules. Pure HTML/CSS/JS.
- Google Fonts (`Inter Tight`) loads from CDN — requires internet connection to render correctly.
- The `screenshots/` folder must be committed with the HTML files — all image `src` paths are relative.
- The site has no backend, no forms, no analytics — purely static.
