# Cozy Gaming Setups

Static affiliate site. Plain HTML — no build step.

## Structure
- `index.html` — homepage (setup cards)
- `style.css` — shared styling (edit design here once)
- `pastel-coding-gaming-desk/index.html` — a setup page
- `minimalist-white-battlestation/index.html` — a setup page
- `about/`, `privacy/` — text pages
- `.nojekyll` — tells GitHub Pages to serve files as-is

## Editing
- Change design: edit `style.css`.
- Add a product link: in a setup page, set the ASIN in the href —
  `https://www.amazon.com/dp/ASIN/?tag=cozygamingset-20`
- Add a setup: copy a setup folder, edit the HTML, add a card on the homepage.

## Deploy
Push to the repo; GitHub Pages serves it automatically.
