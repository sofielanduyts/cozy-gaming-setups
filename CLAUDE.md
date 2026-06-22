# Cozy Gaming Setups — project guide for Claude

This is a static affiliate website. Plain HTML + one shared CSS file. **No build
step, no framework, no Python.** You edit HTML files directly and `git push`;
GitHub Pages serves them.

## What this site does

It publishes "shop the look" guides for cozy / pastel / minimalist gaming desk
setups. Each guide is one page listing several products (keyboard, chair,
monitor, lighting, accessories), each with an Amazon affiliate link. Traffic
comes from Pinterest pins that link to these pages. The money is in the
*bundle* — one visitor buying several items from one page.

## Repo structure

```
index.html                              homepage — cards linking to each setup
style.css                               ALL styling lives here (edit design once)
pastel-coding-gaming-desk/index.html    a setup page
minimalist-white-battlestation/index.html  a setup page
about/index.html                        text page
privacy/index.html                      text page (has required disclosures)
.nojekyll                               makes GitHub Pages serve files as-is
```

Each setup lives in its own folder as `index.html` so the URL is clean
(`/pastel-coding-gaming-desk/`).

## Hard rules — never break these

1. **Affiliate link format is exact:**
   `https://www.amazon.com/dp/ASIN/?tag=cozygamingset-20`
   - `ASIN` is the 10-char product id (e.g. `B0821CDRXK`).
   - `tag=cozygamingset-20` MUST be present on every Amazon link, or we earn
     nothing. This is the US Associates tag. Never change or drop it.
   - Every affiliate `<a>` gets `rel="nofollow sponsored" target="_blank"`.

2. **The Amazon disclosure must stay** on the homepage and every setup page:
   "As an Amazon Associate we earn from qualifying purchases." It is an Amazon
   requirement; removing it risks the account.

3. **Only recommend genuine products.** Amazon policy requires links be real
   recommendations, not filler. If a product is a placeholder, mark its href
   `REPLACE_ASIN` so it's obviously unfinished — never invent an ASIN.

4. **Keep the Pinterest verify tag** in every page `<head>`:
   `<meta name="p:domain_verify" content="3ff8e9c5c183b2a7218e1bc20133f83a"/>`

5. **CSS path depends on depth.** Root pages link `style.css`; pages in a
   subfolder link `../style.css`.

## Brand

- Name: **Cozy Gaming Setups**
- Voice: warm, cozy, a little playful — like a friend who has great taste in
  desks. Aesthetic-first ("soft", "calm", "glow", "cozy", "dreamy"), never
  spec-sheet dry. Sentence case, not Title Case shouting.
- Palette (already in style.css as CSS vars): lavender `#7F77DD` (accent),
  pink `#D4537E`, cream `#FFF0DC`, amber `#FFD580`, soft blue `#DCEEFC`,
  background `#F3EEF8`.
- Logo: an inline SVG console-with-pixel-heart mark. It's embedded at the top
  of each page — copy the existing `<svg class="logomark">` block to reuse.

## Common tasks

- **Add a product to a setup:** duplicate a `.product` block in that setup's
  `index.html`, set the ASIN in the href, write a category + name + one cozy
  sentence.
- **Add a new setup:** see the `shop-the-look` skill — it does this end to end
  from a few Amazon links.
- **Change the design:** edit `style.css` only.
- **Update homepage:** after adding a setup, add a matching `.card` block in
  `index.html` and fix the "N pieces to shop" count.

## Deploy

`git add -A && git commit -m "..." && git push`. GitHub Pages redeploys in
~1 minute at https://sofielanduyts.github.io/cozy-gaming-setups/.
