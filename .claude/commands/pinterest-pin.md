# Pinterest Pin Generator — Cozy Gaming Setups

Generate a fully optimised, ready-to-post Pinterest pin for any setup guide on cozygamingsetups.com.

## What you receive as input

The user may pass:
- A guide name (e.g. "pink flower setup", "minimalist white")
- A URL slug (e.g. "/pink-flower-gaming-setup/")
- A specific angle (e.g. "just the keyboard", "collage of all products")
- Nothing — in which case ask which guide

## Step 1 — Identify the guide

If the user specified a guide, confirm it. If not, list the available guides and ask:

Available guides:
- My ultimate pink cozy gaming setup → /pink-cozy-gaming-setup/
- Pink flower gaming setup inspiration → /pink-flower-gaming-setup/
- Minimalist white battlestation → /minimalist-white-battlestation/
- Pastel cozy coding & gaming desk setup → /pastel-coding-gaming-desk/

## Step 2 — Determine the pin angle

Every guide can produce multiple different pins. Ask the user which angle they want — or suggest the best one if they don't specify:

**Possible angles for any guide:**
1. **Hero shot** — the full setup image, sells the whole vibe
2. **Star product** — zoom in on the most Pinterestable single item (keyboard, chair, desk mat)
3. **Peripherals pair** — keyboard + mouse, or headset + stand
4. **Cozy detail** — accessories only (mug, pillow, clock, cable clips)
5. **Text-overlay graphic** — "X Amazon finds for [aesthetic] gaming" (requires a graphic tool, note this)
6. **Collage** — all product images tiled (requires a graphic tool, note this)

If the user didn't specify an angle, recommend the **Hero shot** for a new guide (most reach) and a **Star product** pin as a follow-up angle.

## Step 3 — Research trending keywords

Before writing copy, reason through which search terms have the most Pinterest traction for this specific aesthetic. Consider:

**Evergreen high-volume terms** (always search well):
- Pink gaming setup / pink gaming room
- Aesthetic gaming setup / aesthetic desk setup
- Cozy gaming setup / cozy desk setup
- Gaming room ideas / gaming room decor
- Amazon gaming finds / Amazon desk finds
- Cute gaming setup / cute desk accessories

**Trending aesthetic overlays** (layer these onto the above):
- Cottagecore → pairs with floral, wooden, nature-adjacent products
- Coquette → bows, pink, ultra-feminine, ballet-core adjacency
- Clean girl → white, minimal, functional beauty
- Soft life → warm tones, comfort items, tactile textures
- Dark academia → moody, bookish (not relevant here — skip)
- Y2K / retro → typewriter keyboards fit here too

**Niche-specific terms** (lower volume but higher intent — buyers, not browsers):
- Pink gaming chair Amazon
- Aesthetic keyboard pink
- Floral desk mat
- Cozy gaming accessories
- Pink monitor setup

Choose 3–5 terms that best match the guide and angle. Lead with the highest-volume term in the title.

## Step 4 — Generate the full Pinterest post

Output all five fields, clearly labelled and ready to copy-paste.

---

### Title
- Max 100 characters
- Lead with the #1 search term for this aesthetic
- Add a hook word: "ideas", "inspiration", "aesthetic", "finds", "guide"
- One emoji at the end is fine if it fits the vibe (🌸 for floral, 🤍 for white/minimal, 🎮 for gaming-forward)
- Do NOT use all-caps or clickbait

### Description
- 300–500 characters (count carefully)
- **First 2 lines**: name the most recognisable/searchable products in the guide — Pinterest indexes these for search
- **Middle**: one sentence of brand voice that sells the vibe, not the specs
- **End**: CTA + full URL on its own line
- Hashtags go at the very end of the description (not separate)
- Format: natural sentences, not bullet points

### Hashtags
- 2–5 max (Pinterest penalises more than 5)
- Mix: 1 broad (#PinkGamingSetup), 1 aesthetic (#CottageCore or #AestheticDeskSetup), 1 shopping (#AmazonFinds)
- Use PascalCase, no spaces
- Place these inside the description field, at the end

### Alt text
- 1–2 sentences describing the image literally
- Include the most searchable product names
- Describe colours and mood
- This is for accessibility AND Pinterest image search indexing

### Topics (up to 10)
- Select from: Gaming, Gaming Setup, Gaming Room, Aesthetic Gaming Room, Pink Gaming Setup, Desk Setup, Cottagecore, Amazon Finds, Desk Accessories, Pink Room Decor, Cute Desk Accessories, Room Decor, Gaming Accessories, Cozy Gaming, Cozy Room Ideas
- Pick the 8–10 most relevant for this specific guide and angle

---

## Step 5 — Posting time recommendation

The site targets the **US market**. User is in the **Netherlands (UTC+2 in summer)**.

US peak Pinterest hours: **Tuesday–Thursday, 8–11pm EST**

Always convert to Netherlands local time:
- 8pm EST = 2am NL (next day)
- 9pm EST = 3am NL (next day)
- 11pm EST = 5am NL (next day)

**Recommendation:** Use Pinterest's built-in scheduler. Create the pin now, schedule it for 3:00am NL time on the next Tuesday, Wednesday, or Thursday. This hits 9pm EST prime time with zero effort.

---

## Step 6 — Suggest follow-up angles

After delivering the pin, always suggest 2–3 alternative pin angles for the same guide that can be posted in the coming days (spaced at least 1–2 days apart to avoid Pinterest spam detection).

Format:
```
Follow-up pin ideas for [guide name]:
- [Angle]: [one-line description of what to post + suggested title hook]
- [Angle]: [one-line description of what to post + suggested title hook]
```

---

## Output format

Use this exact structure so the user can copy-paste each section into Pinterest:

```
TITLE
[title here]

DESCRIPTION
[description + hashtags here]

ALT TEXT
[alt text here]

TOPICS
[comma-separated list]

WHEN TO POST
[day + NL time + EST equivalent]

---
FOLLOW-UP PIN IDEAS
[2-3 alternative angles]
```

---

## Rules — never break these

- The URL in the description must always be the full canonical URL: `https://cozygamingsetups.com/[slug]/`
- Never recommend more than 5 hashtags
- Never invent product names — only use products that are actually in the guide
- The title must lead with a real Pinterest search term, not the brand name
- Always include the posting time in both NL local time and EST
- Never suggest posting the same URL to multiple boards within the same day
