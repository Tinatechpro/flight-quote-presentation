# Flight Quote Presentation · Buenos Aires ✈ Vienna

> A polished, **single-file** web presentation of a flight quote for a travel agency:
> five itinerary alternatives ranked by **price and convenience**, detailed per-leg
> timelines, and direct booking links. Built as a product demo for the travel
> industry (Amadeus / GDS-style workflow).

**🌎 Localized for the Hispanic travel market** — the interface is in Spanish (`es-AR`),
built for travel agencies in Argentina / LATAM. Porting it to English or a multi-locale
version would be a straightforward next step.

![Vanilla JS](https://img.shields.io/badge/JavaScript-vanilla-F7DF1E?logo=javascript&logoColor=black)
![Dependencies](https://img.shields.io/badge/dependencies-0-brightgreen)
![Responsive](https://img.shields.io/badge/responsive-mobile%20%E2%86%92%20desktop-blue)
![Accessibility](https://img.shields.io/badge/WCAG-AA-success)
![Print](https://img.shields.io/badge/print-A4%20ready-informational)
![Themes](https://img.shields.io/badge/themes-light%20%2F%20dark-6f42c1)

**🔗 Live demo:** https://Tinatechpro.github.io/flight-quote-presentation/

![Flight proposal — light and dark themes](preview.png)

---

## Highlights

- **Decision-first UX.** A comparison table surfaces fare, nights, stops and convenience
  at a glance; the lowest fare is flagged as *recommended*, and the airline with the
  shortest connections is called out — so the client decides in seconds.
- **Boarding-pass itineraries.** Each option expands into a per-leg timeline: departure /
  arrival times, airports, terminals, flight numbers, aircraft and layovers.
- **Light & dark themes.** Token-based, with a manual toggle and `prefers-color-scheme`
  detection; contrast audited to **WCAG AA** in both themes.
- **Print / PDF as a first-class layout.** A dedicated `@media print` + `@page A4`
  stylesheet paginates cleanly — no clipped tables, no orphaned headings, each option
  kept whole — for a professional export.
- **Zero dependencies, fully self-contained.** One `index.html`; all CSS and JS inline,
  no external requests. Loads instantly and works offline.

## Engineering decisions

- **A design system, not ad-hoc styles.** CSS custom properties drive the palette, type
  scale and spacing. A theme is a *token swap*, not a second copy of the rules — which is
  why dark mode stays consistent and maintainable.
- **Accessibility by default.** Semantic landmarks, `scope`-ed table headers, visible
  focus states, `aria` only where it adds meaning, `prefers-reduced-motion`, and contrast
  ratios verified programmatically (AA) in light and dark.
- **Print treated as design, not an afterthought.** The screen layout *reflows* for A4
  (compact tickets, tabular figures, links rendered like the web) instead of dumping the
  desktop view onto paper.
- **Content integrity.** Every fare, date, flight number, terminal and link mirrors the
  source quote verbatim — no invented data.

## Tech stack

Vanilla **HTML5 · CSS3 · JavaScript** — no framework, no build step, no libraries.
Typography, layout (Flexbox/Grid), CSS custom properties, `@media` (responsive, dark,
print) and a tiny progressive-enhancement script for the theme toggle.

## Run locally

Open `index.html` directly, or serve the folder:

```bash
python -m http.server 8000    # then open http://localhost:8000
```

## Repository

| File | Purpose |
|---|---|
| `index.html` | The site — served live by GitHub Pages. |
| `preview.png` | Light / dark preview image. |

---

**Designed & developed by [Ernestina D'Amico](https://github.com/Tinatechpro) — Web Developer.**

_Sample quote data (July 2026), for demonstration purposes only._
