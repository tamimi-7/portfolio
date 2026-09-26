# Osama Altamimi — Portfolio

**Live:** https://tamimi-7.github.io/portfolio/ · Arabic: https://tamimi-7.github.io/portfolio/?lang=ar

A bilingual (English / Arabic) editorial portfolio. One HTML file, no build step,
no framework, no dependencies.

```
index.html        page, styles, scripts and the Arabic dictionary
assets/           product screenshots, favicon, social share image (og.png)
```

## Preview locally

Double-click `index.html`, or run `python3 -m http.server` and open http://localhost:8000.

## Projects featured

| # | Project | Live | Source |
|---|---|---|---|
| 01 | Inglish — STEP prep & English learning platform (flagship) | https://step-english-lime.vercel.app | https://github.com/tamimi-7/step-english |
| 02 | Saudi E-Invoice — ZATCA compliant | https://saudi-e-invoice-system.vercel.app | — |
| 03 | High Pressure Cables Factory | https://hpcfactory.com/ | — |
| 04 | Three games — Tuwaiq Academy | on request | — |

## How it works

**Two languages.** English lives in the HTML. Every translatable element has a
`data-i18n="key"` attribute, and the Arabic for that key is in the `AR` object at the
bottom of `index.html`. Switching language swaps the text, flips `dir` to `rtl`, and
changes fonts (Amiri + IBM Plex Sans Arabic). The choice is remembered, and
`?lang=ar` opens the Arabic version directly (useful for sharing).

To change text: edit the English in the HTML **and** the same key in `AR`.
To add a new element: give it a new `data-i18n` key and add that key to `AR`.
Latin-only text inside Arabic (e.g. `C#`) should be wrapped in `<bdi>` so it doesn't flip.

**Light / dark.** Follows the system setting, with a toggle in the top bar. All colours are
tokens at the top of the `<style>` block.

**Layout.** Built with CSS logical properties (`margin-inline`, `inset-inline-start`…) so
the same CSS mirrors correctly in RTL.

## Updating screenshots

The Inglish screenshots in `assets/` were captured from the app running locally
(`node dev/server.js` in the step-english repo) with Playwright, at 1440×900 for desktop
and 390×844 @2x for phones. Replace a file with the same name to update it.

## Deploy

GitHub Pages deploys from `main` / root. Merging to `main` publishes the site.
