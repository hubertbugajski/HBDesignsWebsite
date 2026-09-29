# hbdesigns.ca

Static site. No build step, no dependencies, no framework.

    index.html    all content
    styles.css    all styling (CSS vars at :root)
    script.js     scroll reveal only; site works fully with JS off
    favicon.svg   scope-trace mark
    og.png        1200x630 link-preview image
    brand/        HB logo: hb-logo.svg (full lockup), hb-monogram.svg (header),
                  hb-logo-1bit.png. SVGs use currentColor; header tints via CSS mask.
    robots.txt / sitemap.xml

## Before going live

1. `index.html` — replace `hello@hbdesigns.ca` (mailto link + JSON-LD) with your real address.
2. `index.html` — set the LinkedIn URL, or delete that button.

## Deploy

Any static host. Drag the folder into Netlify/Cloudflare Pages, or:

    # GitHub Pages
    git init && git add . && git commit -m "site"
    # push, then Settings > Pages > deploy from branch, add hbdesigns.ca as custom domain

DNS at your registrar: `A`/`ALIAS` per host instructions, plus `CNAME www -> hbdesigns.ca`.

Local check: `python3 -m http.server 8000`

## Adding a real contact form

The mailto link needs zero infrastructure. If you want a form instead, Formspree/Basin
take a plain POST — add a `<form action="https://formspree.io/f/XXXX" method="POST">`
block in the `#contact` section; no other changes needed.

## Design notes

- Palette in `:root`: `--paper` bench gray, `--panel` petrol ink, `--trace` phosphor
  teal, `--alert` instrument amber. Change those four and the whole site retones.
- Type: Archivo (display), Source Serif 4 (body), IBM Plex Mono (labels/specs).
- Hero waveform is hand-authored SVG paths; the amber CH2 pulse is the intermittent
  fault. Edit the `d` attributes directly if you want a different capture.
- Case-study results use a `before → after` delta row. Keep new entries in that shape.
