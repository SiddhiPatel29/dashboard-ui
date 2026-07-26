# SaaS Admin Dashboard

A responsive admin dashboard UI built with plain HTML and CSS — no frameworks, no build step. Recreates a SaaS-style analytics dashboard with a sidebar, KPI cards, charts, an orders table, and a set of activity/status widgets.

![Dashboard preview](preview.png)

## Features

- **Sidebar navigation** with active-state highlighting and an "Active" badge
- **Stat cards** (Total Revenue, Orders, Customers, Conversion Rate) with inline sparkline trends
- **KPI Statistics card** with a live-style line chart and two toggle switches
- **Sales Analytics** area chart with gridlines, a tooltip marker, and a date-range switcher (1M / 3M / 6M / 1Y)
- **Revenue Breakdown** donut charts with a percentage legend
- **Recent Orders Table** with status badges (Completed / Pending / Processing / Cancelled)
- **Bottom widget row**: Project Progress, Team Members, Recent Activity Feed, Calendar, Notifications Panel, and a Storage Usage ring
- **Fully responsive** — reflows through desktop, tablet, and mobile breakpoints (see below)

## Tech stack

- **HTML5** — semantic structure, no templating
- **CSS3** — Flexbox + CSS Grid (including `fr`-unit proportional grids so the layout scales instead of clipping)
- **SVG** — hand-built charts, donuts, and the storage ring (no charting library)
- [Font Awesome](https://fontawesome.com/) — icons (via CDN)
- [Plus Jakarta Sans](https://fonts.google.com/specimen/Plus+Jakarta+Sans) — typeface (via Google Fonts CDN)

No JavaScript, no build tools, no dependencies to install.

## File structure

```
.
├── index.html   # Page markup
├── style.css    # All styling, including responsive breakpoints
└── README.md
```

## Getting started

This is a static site — just open it in a browser.

```bash
git clone https://github.com/<your-username>/<your-repo>.git
cd <your-repo>
open index.html        # macOS
# or double-click index.html in your file explorer
```

For live-reload while editing, you can use any static server, e.g.:

```bash
npx live-server
```

## Responsive behavior

| Breakpoint | What changes |
|---|---|
| `> 1650px` | Full fixed-width layout, everything in a single row per section |
| `≤ 1650px` | Top stat cards + KPI card wrap onto their own line |
| `≤ 1300px` | Stat cards go 2-column; Sales Analytics/Revenue Breakdown/Orders Table stack vertically; bottom widget row stacks to one column; KPI card's secondary controls wrap |
| `≤ 900px` | Sidebar collapses to a horizontal icon bar; header wraps; chart/donut pair stacks |
| `≤ 480px` | Stat cards go full single-column for small phones |

The Recent Orders Table also scrolls horizontally within its own card on narrow screens rather than forcing the page wider.

## Notes

- Avatar images are placeholders from [pravatar.cc](https://pravatar.cc/) — swap in real user photos for production use.
- Colors, spacing, and typography were matched by hand against a reference design rather than generated from design tokens.
- Requires an internet connection for the Google Fonts / Font Awesome CDN links; see comments in `index.html` if you'd rather self-host those assets.

## License

Feel free to use this as a starting point for your own dashboard projects.
