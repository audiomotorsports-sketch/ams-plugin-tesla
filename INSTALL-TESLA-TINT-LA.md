# Cursor / Grok Bot — Tesla Tint LA plugin

Copy everything below the line. **teslatintla.com only.** Folder **teslatintla/** at repo **ROOT** (not `sites/`). Vercel root **teslatintla**. Branch **v1**. Screenshot phone before production.

---

You are editing **teslatintla/** on github.com/audiomotorsports-sketch/audiomotorsport, branch **v1**. One pass. Do not open other network folders. Do not invent images. Do not rewrite the homepage.

This site canonicalises to the **bare host** — `https://teslatintla.com` — **no www**. Every other desk uses www. Do **not** “fix” that.

index.html is ~44,736 bytes. Trust the measured anchors in this file.

**This is a Los Angeles site.** Write for a driver in LA, Long Beach, or OC. Nobody travels for tint. Do not aim copy at California-as-a-state, Nevada, or anywhere out of metro. Tesla itself sells Model Y tint from the factory — this desk wins on the bay in Carson, not on statewide coverage.

## This site is WHITE

Do not copy pods / alarm / tint / hub CSS. Those are dark. This desk:

```
--bg:        #ffffff
--surface:   #f4f4f4
--text:      #171a20
--muted:     #5c5e62
--cta:       #171a20
--cta-text:  #ffffff
--border:    rgba(23, 26, 32, 0.12)
--hairline:  #e8e8e8
theme-color: #FFFFFF
```

There is no gold, no steel, no blue. Accent **is** near-black `#171a20`. Buttons are black-on-white. Thin hairlines. No glow.

Plugin CSS uses `var(--bg, #ffffff)` / `var(--text, #171a20)`. **Do not hardcode `#0a0a0a` anywhere.**

## Job

1. Insert the quote plugin **immediately under the existing banner**.
2. **MOVE** `<section class="offer-cards" id="offers">` to the **bottom** — after the last content section (`section-shop` / `#drive-in`), before the footer. Not deleted. Contents unedited. Keep `id="offers"`.
3. Leave the simulator (`#tesla-sim`, `sim-modelrow`, `sim-picker`, `sim-panel`) **untouched**.
4. **Do not** create or edit `/privacy/` or `/terms/`. They exist, they are linked on all 128 pages, they are in the sitemap. Skip.

Required homepage order:

```
hero-banner
[PLUGIN]
#tesla-sim / sim-modelrow / sim-picker / sim-panel
quote-top … content …
section-shop
offer-cards          ← LAST, before footer
```

The 3 cards (do not edit): SOLAR CERAMIC · Y FRONTS / SOLAR CERAMIC · MODEL 3 / SOLAR CERAMIC · CYBERTRUCK.

## Files
1. Save `ams-plugin-tesla.css` as `teslatintla/assets/css/ams-plugin-tesla.css`
2. In homepage `<head>`:
   `<link rel="stylesheet" href="/assets/css/ams-plugin-tesla.css">`
   (or `assets/css/ams-plugin-tesla.css` if this page uses relative CSS like the others — **match the existing pattern on this file**)
3. Paste `ams-plugin-tesla.html` using depth-count below.
4. **Strip any developer comment** from the top of the plugin HTML before it ships. The hub plugin shipped one and it showed in view-source. The file we gave you has **none** — keep it that way.
5. No new photos. Model cards use simulator images already on this site:
   - `/assets/sim/img/model-3.png`
   - `/assets/sim/img/model-y.png`
   - `/assets/sim/img/model-yl.png`
   - `/assets/sim/img/model-s.png`
   - `/assets/sim/img/model-x.png`
   - `/assets/sim/img/cybertruck.png`

## Insert — DEPTH COUNT. Not a literal next-sibling string.

Matching `</section>\n<section class="offer-cards"` broke the lacartint install.

1. Find `<section class="hero-banner">` in `teslatintla/index.html`.
2. Walk forward counting `<section` (+1) and `</section>` (−1) until depth returns to 0.
3. Insert `ams-plugin-tesla.html` **immediately after that closing tag**.

Do **not** touch `<section class="hero-banner">` or its images.

## Move offer-cards to the bottom

Cut the entire `<section class="offer-cards" id="offers"> … </section>` (79 lines, ~4,964 chars, 3 cards).

Paste it **after** `<section class="section section-shop" id="drive-in">` closes, **before** `<footer`.

Do not edit card contents. Keep `id="offers"`. Carry `offer-cards.css` — already in `<head>`.

## Plugin — Tesla only. No prices. Metro copy.

Proof bar, separate cells, never merge Google + Yelp:

Google 4.8 from 654 · Yelp 4.7 from 777 · Since 2003 · Bay Carson · Walk-in Mon–Sat 9:30–6

Year field. Model chips:

Model 3 · Model Y · Model Y L · Model S · Model X · Cybertruck

Film chips: Solar Ceramic · 3M IR Ceramic

Do **not** offer generic make/model. This desk is Tesla-only.

Lead copy is already metro: “LA, Long Beach, OC. Drive to Carson.” Do not expand it to statewide.

Text us / Call with year + model + film prefilled into SMS. Ask for Nick. Zack runs the floor.

Do **not** put `id="quote"` on the plugin. That id already exists on `section.quote-top`.

Shop: 22025 S Avalon Blvd Ste A, Carson, CA 90745  
Call `tel:+13105138800` · Text `sms:+12134291092` · Email audiomotorsports@gmail.com

Sticky: `right: 88px` so `#ams-chat` keeps the corner. **AND:**

```css
@media (min-width: 1024px) { .ams-plug-sticky { display: none; } }
```

Never `left: auto; right: auto` with a fixed width.

Plugin CSS hides `.mobile-cta-bar` only while `#ams-plug-tesla` is on the page. Do not delete the old bar HTML.

Cards are **buttons** that set the model chip. Do not invent `/model-3-window-tint/` URLs — those 404 today.

Plugin HTML has **zero** dollar amounts.

## Prices — plugin carries none

The model × film table on this site stays where it is. Do not print any of it in the plugin. Do not edit the table.

⚠️ **FLAG, DO NOT RESOLVE:** `.cursor/rules/pricing-and-email.mdc` lists “Tesla tint” as **TBD**. The live site publishes $189 / $249 / $269 / $349 / $369 / $399 / $499 / $549 / $569 / $599 / $699. Report the conflict. Do not pick a number.

Roof glass is a store visit. No public dollars. Never quote one.

No struck-through “was” prices.

## Do not
- Touch `<section class="hero-banner">` or its images
- Touch the simulator (`sim-modelrow` / `sim-picker` / `sim-panel` / `#tesla-sim`) at all
- Edit offer card contents — MOVE the section
- Touch chat (`ams-chat.js`, `#ams-chat`)
- Delete `.mobile-cta-bar` HTML
- Introduce dark-theme colours or hardcode `#0a0a0a`
- Use warranty / guaranteed / lifetime / financing
- Invent reviews or reviewer names
- Write new legal-tint copy. Reuse the site’s existing Legal & Compliance wording **verbatim** if you need any
- Write copy targeting other states or a multi-state service area
- **Touch `/privacy/` or `/terms/`** — they exist and are done
- Add `www.` to teslatintla.com
- **Touch `/tesla-tint-carson/`** — see P2

## SEO / legal — same pass

### P1 — privacy + terms. SKIP.

`/privacy/` and `/terms/` now exist, are linked from all 128 pages via the footer generator, and are in `sitemap.xml` (126 → 128). **Do not create, edit, or duplicate them.**

### P2 — THE CARSON PAGE. FLAG ONLY. DO NOT TOUCH IT.

**`/tesla-tint-carson/` is built as city “Avalon”.** Live title: “Tesla Window Tint Avalon | Tesla Tint LA”. Avalon CA is Catalina Island, ferry-only. The shop’s own home city has no working landing page.

This is **not** a generator bug. `teslatintla/scripts/city-flavor.mjs` has a hand-authored record: slug `"carson"`, name `"Avalon"`. Two guards **hard-fail the build** if “Carson” reappears:

- `teslatintla/scripts/assert-no-carson.mjs`
- `teslatintla/scripts/build-city-pages.mjs` (`console.error "Carson leaked on ..."` then `process.exit(1)`)

Someone kept Carson off this site and never wrote down why. **Owner decision. Not a fix.** Do not delete the guards. Do not rename the city. Do not `sed s/Avalon/Carson/g` — the street is Avalon Blvd and many “Avalon” hits are the real address.

**Raise it in the PR and stop.**

### P3 — review-attribution copy. FLAG. Do not mass-edit.

Only ~2 files carry “never call it anything else”.

**111 files** carry review-attribution copy (“borrowed from Los Angeles”, ` · borrowed` bylines from `quoteCard()` in `teslatintla/scripts/build-city-pages.mjs`).

Owner call: reword or leave. **Do not mass-edit 111 pages this pass.** If you see “never call it anything else” on the two files, fix **both** visible FAQ and JSON-LD identically:

- Payment Plan line → `We quote the work first. If a Payment Plan is the right fit, you can apply at the counter.`
- schema aggregate line → `Google shows 4.8 from 654 reviews for the shop overall, not for this page alone.`

### P4 — orphaned city pages. Do Orange only.

`/tesla-tint-carson/` and `/tesla-tint-orange/` have effectively zero inbound internal links. `onGrid: false` keeps them off `/locations/`.

- **Orange** is content-correct and just unlinked. Linking it is safe and worth doing: add **one** inbound link to `/tesla-tint-orange/` from `teslatintla/locations/` (or set Orange `onGrid: true` in `city-flavor.mjs` **only if** that does not rebuild 111 pages). Do not invent Orange copy.
- **Carson** is blocked by P2. Do not link it.

### P5 — 11 city pages on old .png banners. FLAG if it blows the diff.

anaheim, carson, gardena, hermosa-beach, long-beach, los-angeles, orange, rancho-palos-verdes, san-pedro, torrance, whittier.

`banner(slug)` already prefers jpg. Copying `assets/img/city/<slug>-desktop.jpg` + `-mobile.jpg` from the hub into `teslatintla/assets/img/city/` switches them. **Own pass if the diff is huge.** Do not start from carson.png.

### P6 — flag only
- Do not bulk-noindex 111 city pages
- Do not remove `aggregateRating` without an owner decision
- Do not carve a `/tint-law/` page this pass

## Done when
- Banner byte-identical
- Order: hero-banner → plugin → simulator → content → offer-cards LAST
- offer-cards byte-identical after the move, `id="offers"` kept
- Simulator still works (model → shade → price, no console errors)
- Plugin reads on WHITE. `grep -n "#0a0a0a" teslatintla/assets/css/ams-plugin-tesla.css` → 0
- Plugin has zero `$` amounts
- Plugin copy stays metro (LA / Long Beach / OC / Carson). No statewide pitch
- `/privacy/` and `/terms/` **untouched** and still linked from all 128 pages
- chat, `.mobile-cta-bar`, GTM intact
- Sticky hidden above 1024px
- **Carson page UNTOUCHED, guards UNTOUCHED, raised in the PR**
- Orange has at least one inbound internal link **or** is flagged with a reason
- No `www.teslatintla.com` invented
- No developer comment above the plugin in view-source
- Visible FAQ and FAQPage JSON-LD still match if you touched them
- JSON-LD still parses
- `git diff --shortstat`: report deletions and what went

## Post-deploy checks
```
curl -s https://teslatintla.com/ | grep -c 'id="ams-plug-tesla"'
curl -s https://teslatintla.com/ | grep -n 'offer-cards\|ams-plug-tesla\|sim-modelrow\|section-shop'
curl -sI https://teslatintla.com/privacy/ -o /dev/null -w '%{http_code}\n'
curl -sI https://teslatintla.com/terms/ -o /dev/null -w '%{http_code}\n'
curl -s https://teslatintla.com/ | grep -c 'id="ams-plug-tesla"'
curl -sI https://www.teslatintla.com/ -o /dev/null -w '%{http_code} %{redirect_url}\n'
```

Expect: plugin 1, plugin before simulator, offer-cards after section-shop, privacy 200, terms 200 (untouched), www still redirects to bare host (do not invert that).

Screenshot **phone** before production merge to branch `v1`.
