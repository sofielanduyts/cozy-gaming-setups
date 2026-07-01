# Shop the Look — New Setup Guide Builder

Create a new setup guide page for cozygamingsetups.com that exactly matches the layout and structure of the canonical template (`pink-cozy-gaming-setup/index.html`).

## What you receive as input

The user provides:
- A guide name / theme (e.g. "purple kawaii gaming setup")
- A list of Amazon product URLs or ASINs with product names
- Optionally: a hero image filename and a slug for the folder

## Step 1 — Gather info

If any of the following are missing, ask before proceeding:

1. **Guide title** — the full H1 name (e.g. "Purple kawaii gaming setup")
2. **Slug** — the folder name / URL path (e.g. `purple-kawaii-gaming-setup`)
3. **Aesthetic tag** — the `page-tag` sub-label (e.g. "Setup guide · Purple kawaii gaming")
4. **Hero image filename** — must already exist in `images/` (e.g. `images/purple-kawaii-setup.png`)
5. **Product images folder** — must already exist in `images/[slug]/` with renamed descriptive filenames
6. **Products** — list of: product name, category, ASIN, image filename

If the user provides Amazon URLs, extract the ASIN from the URL path (`/dp/XXXXXXXXXX/`).

## Step 2 — Verify product images

Before writing HTML, check that the product image folder exists:
- Path: `images/[slug]/`
- Each image must have a descriptive kebab-case filename (e.g. `hyperx-cloud-iii-headset-pink.jpg`)
- If filenames are still the raw Amazon format (`51TDQd19y5L._AC_SL1500_.jpg`), rename them first using descriptive names matching the product

## Step 3 — Write the guide page

Create `[slug]/index.html` following this **exact structure**. Do not deviate from it.

### Head section
```html
<title>[Guide title] — [N] cozy Amazon finds | Cozy Gaming Setups</title>
<meta name="description" content="[2-sentence description with top product names and Amazon mention]">
<meta name="p:domain_verify" content="3ff8e9c5c183b2a7218e1bc20133f83a"/>
<meta property="og:type" content="article">
<meta property="og:title" content="[Guide title] — [N] cozy Amazon finds ✨">
<meta property="og:description" content="[Longer OG description with all key product names, keywords for Pinterest]">
<meta property="og:url" content="https://cozygamingsetups.com/[slug]/">
<meta property="og:image" content="https://cozygamingsetups.com/images/[hero-image]">
```

Always include the Pinterest verify tag. Never omit it.

### Nav (identical on every page)
```html
<nav class="site-nav">
  <div class="nav-inner">
    <a class="nav-logo" href="../">
      <img src="../images/logo.png" width="28" height="28" alt="Cozy Gaming Setups logo">
      Cozy Gaming Setups
    </a>
    <ul class="nav-links">
      <li class="nav-home"><a href="../">Cozy Gaming Setups</a></li>
      <li><a href="../about/">About</a></li>
      <li class="nav-cta"><a href="https://nl.pinterest.com/cozygamingsetups/" target="_blank">Pinterest ↗</a></li>
    </ul>
  </div>
</nav>
```

### Main wrapper — MUST use these exact classes
```html
<div class="wrap narrow article-wrap">
```

### Breadcrumb — always present
```html
<nav class="breadcrumb"><a href="../">Home</a><span class="breadcrumb-sep">›</span><span>[Short guide name]</span></nav>
```

### Article header
```html
<header class="article-header">
  <span class="page-tag">Setup guide · [Aesthetic tag]</span>
  <h1>[Full guide title]</h1>
  <p class="sub-lead">[One sentence: what this is, how many products, Amazon mention]</p>
</header>
<p class="article-date">Updated [Month Year] &nbsp;·&nbsp; [N] pieces to shop</p>
```

### Hero image
```html
<div class="setup-hero-img">
  <img src="../images/[hero-image]" alt="[Descriptive alt text with key product names]">
</div>
```

### Intro paragraph
```html
<p class="intro">[2-3 sentences in brand voice. What makes this setup special, what the anchor piece is, what the mood feels like. End by mentioning everything is on Amazon.]</p>
```

### Quick picks list
```html
<div class="quick-picks">
  <p class="quick-picks-title">Everything in this setup</p>
  <ul class="picks-list">
    <li><span class="pick-num">01</span><span class="pick-cat">[Category]</span><span class="pick-name">[Product name]</span></li>
    <!-- one li per product, numbered 01–NN with leading zero -->
  </ul>
</div>
```

### Products section
```html
<div class="products-section">
  <!-- one .product block per item -->
</div>
```

### Each product block — exact structure
```html
<div class="product">
  <div class="product-img"><img src="../images/[slug]/[image-filename]" alt="[Product name — brief descriptor]" loading="lazy"></div>
  <div class="product-body">
  <div class="product-meta"><span class="product-idx">[01]</span><span class="cat">[Category]</span></div>
  <h3>[Product name]</h3>
  <p class="desc">[2-4 sentences: what it is, key specs, what makes it fit this aesthetic. Brand voice — warm, direct, not spec-sheet dry.]</p>
  <p class="why">[1-3 sentences starting with the real reason to choose this specific product: a hidden detail, a practical advantage, what makes it better than alternatives. This is the "why this one" paragraph.]</p>
  <a class="btn" href="https://www.amazon.com/dp/[ASIN]/?tag=cozygamingset-20" rel="nofollow sponsored" target="_blank">Check price on Amazon ↗</a>
  </div>
</div>
```

**Rules for product copy:**
- `desc` — sell the product: specs + aesthetic fit. 2-4 sentences.
- `why` — the honest reason to pick THIS one. Hidden detail, durability note, what it does better than alternatives. Never repeat the same info as `desc`.
- Button text is always exactly: `Check price on Amazon ↗`
- Button class is always exactly: `btn`
- Every affiliate link MUST contain `?tag=cozygamingset-20`
- Every `<a>` gets `rel="nofollow sponsored" target="_blank"`

### Page footer (prev/next nav)
```html
<footer class="page-footer">
  <a href="../">&larr; All setups</a>
  <a href="../[next-guide-slug]/">[Next guide name] →</a>
  <a href="../privacy/">Privacy</a>
</footer>
```

Check the current homepage card order to determine the correct next guide.

### Site footer (identical on every page)
```html
<footer class="site-footer">
  <div class="footer-inner">
    <a class="footer-logo" href="../">
      <img src="../images/logo.png" width="24" height="24" alt="Cozy Gaming Setups logo">
      Cozy Gaming Setups
    </a>
    <p class="footer-tagline">Curated shop-the-look guides for the cozy gaming aesthetic. Every piece linked, every choice considered.</p>
    <ul class="footer-links">
      <li class="nav-home"><a href="../">Cozy Gaming Setups</a></li>
      <li><a href="../about/">About</a></li>
      <li><a href="../privacy/">Privacy</a></li>
      <li><a href="https://nl.pinterest.com/cozygamingsetups/" target="_blank">Pinterest ↗</a></li>
    </ul>
    <p class="footer-copy">As an Amazon Associate we earn from qualifying purchases - at no extra cost to you.<br>&copy; Cozy Gaming Setups — made with 💜 for the community</p>
  </div>
</footer>
```

Note: the footer `<ul>` first `<li>` MUST have `class="nav-home"`.

## Step 4 — Update the homepage

Add a new card to `index.html` inside `<div class="grid">`.

Card structure:
```html
<a class="card [color-class]" href="[slug]/">
  <div class="card-img-wrap">
    <img src="images/[hero-image]" alt="[Alt text]">
  </div>
  <span class="card-label">[Short aesthetic label]</span>
  <h2>[Guide title]</h2>
  <p>[2 sentences: key products + mood. No spoilers — tease the look.]</p>
  <div class="card-foot">
    <span class="pill">Shop the look &rarr;</span>
    <span class="card-count">[N] pieces</span>
  </div>
</a>
```

Color class options: `pink` (pink/floral/pastel), `minimalist` (white/neutral), `pastel` (soft multi-color).

Position the card in the correct order — ask the user where in the grid it should appear if not obvious.

## Step 5 — Commit and push

```bash
git add [slug]/ images/[slug]/ images/[hero-image] index.html
git commit -m "Add [guide title] guide — [N] products"
git push
```

## Hard rules — never break these

1. Affiliate link format: `https://www.amazon.com/dp/[ASIN]/?tag=cozygamingset-20` — tag MUST be present
2. Every affiliate `<a>` gets `rel="nofollow sponsored" target="_blank"`
3. Amazon disclosure is in the site footer on every page — never remove it
4. Pinterest verify tag in every `<head>`: `<meta name="p:domain_verify" content="3ff8e9c5c183b2a7218e1bc20133f83a"/>`
5. Never invent an ASIN — if unknown, write `REPLACE_ASIN` as a placeholder
6. CSS is always `../style.css` for subfolder pages
7. All image paths use `../images/` for subfolder pages
8. `loading="lazy"` on all product images
9. Wrapper class is always `wrap narrow article-wrap` — never just `wrap`
10. Button class is always `btn` — never `btn-shop` or any other variant
