# Osama — Portfolio

Single-file portfolio site. No build step, no dependencies, no Node required.
Everything (HTML, CSS, JS) lives in `index.html`.

## Preview locally

Double-click `index.html`. That's it.

## Status

Complete and ready to publish. No placeholders left.

**Optional upgrade:** the three bootcamp games are presented as one card. To split
them into three individual project cards, find the `✏️ OPTIONAL` comment in
`index.html` and duplicate the `<article>` block — one per game, each with its real
name, core gameplay loop, and the hardest technical problem you solved in it.
Named games with specifics are always stronger than a summary.

## Deploy

**Vercel (easiest)** — go to [vercel.com/new](https://vercel.com/new), drag this folder onto the page. Live in ~20 seconds.

**Netlify** — drag the folder onto [app.netlify.com/drop](https://app.netlify.com/drop).

**GitHub Pages** — push this folder to a repo, then Settings → Pages → deploy from `main` / root.

```bash
git init && git add . && git commit -m "Portfolio"
```

## Notes

- Poppins loads from Google Fonts; offline it falls back to Segoe UI/system fonts.
- Respects `prefers-reduced-motion` and prints cleanly to PDF.
- Responsive down to mobile, with a hamburger menu under 768px.
