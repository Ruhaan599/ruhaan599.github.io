# Ruhaan Gupta — 10m Air Pistol

Athlete profile site for Ruhaan Gupta, NRAI "Renowned Shot" and member of
The Doon School Shooting Team. Live at **https://ruhaan599.github.io/**.

It's a single static page with no build step and no frameworks. Everything
lives in `index.html` (HTML, CSS and vanilla JS), so GitHub Pages serves it
exactly as it is.

## What's on the page

| Section | What it does |
| --- | --- |
| **Hero** | A live ISSF 10m air pistol target. Visitors click (or tap) to fire, and each shot is scored in decimals from the real target geometry. The aim drifts slightly, like a real hold. |
| **01 Record** | Scroll-driven story. A sticky target plots each result (state → North Zone MQS → Renowned Shot → inter-school circuit) as a step toward the centre. |
| **02 Event** | The sport's fixed numbers (10 m, 4.5 mm pellet, 11.5 mm ten-ring, 60 shots, 75 min, 500 g trigger), animated as they come into view. |
| **03 Range** | A playable simulator. An open-sight view (front post in the rear notch, target soft in the distance) with a breath-hold mechanic: **press and hold** to settle, **release** to break the shot. An electronic-scoring monitor zooms to the group, marks the mean point of impact and totals a 10-shot series. Your best series is saved in the browser. Sound is optional. |
| **04 Discipline** | Trigger control, breath and pulse, and composure, each with a small animated graphic. |
| **05 Next** | What's done, what's next, and what comes eventually. |
| **06 Contact** | Email link plus a copy-to-clipboard button. |

The page also has a custom sight cursor on desktop, a scroll progress bar,
a full-screen mobile menu, scroll reveals and film grain. Everything respects
`prefers-reduced-motion`, works with a keyboard (Space or Enter fires in the
simulator) and fits screens down to 320 px wide.

## Files

```
index.html            the site
404.html              "0.0 — MISS" page for broken links (GitHub Pages serves it automatically)
favicon.svg           browser tab icon
apple-touch-icon.png  iPhone/iPad home-screen icon
og-image.png          1200×630 preview shown when the link is shared (WhatsApp, LinkedIn, X…)
robots.txt            lets search engines crawl the site
sitemap.xml           tells search engines which pages exist
```

## Editing

- **Results / text:** search `index.html` for the section (e.g. `RECORD`) and edit the copy inside each `<li class="step">`.
- **Email:** search for `ruhaan.g13@gmail.com` (it appears in the contact section and the copy button's `data-email`).
- **Colours:** the `:root { … }` block at the top of the `<style>` tag.
- **Simulator difficulty:** in the script, `AMP_MIN` (hold wobble in mm) and the `gauss() * 2` trigger error inside `release()`. Lower numbers make it easier.
- **Adding a photo:** a real range photo would sit well in the hero or the Discipline section. Drop it in the repo and add an `<img>`.

## Getting found by Google and AI search

- Structured data (a schema.org `Person` block with awards, team and school) is already in the page `<head>`.
- Submit `https://ruhaan599.github.io/sitemap.xml` in [Google Search Console](https://search.google.com/search-console). This is the biggest single lever for fast indexing.
- Get the link onto other real pages, such as a Doon School page, NRAI results, an Instagram bio or LinkedIn.
