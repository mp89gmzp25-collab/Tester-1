# README — Vascular PDP section (`sections/vascular-pdp.liquid`)

The below-hero body of the Dova Nattokinase product page, as one reusable Shopify section. Every
image and every line of copy is editable in the theme editor. The hero / buy box / Kaching widget
are **out of scope** (handled by the existing product section + the app).

> ⚠️ **All product values are PROVISIONAL schema defaults.** Nothing ships until confirmed against
> the COA / spec sheet / finished label. See `CLAIMS-TO-SUBSTANTIATE.md`.

---

## 1. Install

1. **Online Store → Themes → ⋯ → Edit code.**
2. **Sections → Add a new section** → name it `vascular-pdp` → replace the generated contents with
   `sections/vascular-pdp.liquid` → **Save**.
3. In the **theme editor** (Customize), open the product template, **Add section → Vascular PDP**,
   and drag it below the hero/buy-box. The preset adds one of each block to start.
4. Fill copy and images per band. Toggle any band off with its **Show section** checkbox.

The section renders its own `<h2>` headings and does not include an `<h1>` — the product title
stays the page's single `<h1>`.

## 2. Bands & how they map to the brief

| Band | Setting group | Blocks used |
|---|---|---|
| 5.1 Trust bar | "5.1 Trust bar" | — |
| 5.2 Good numbers. Cold hands. | "5.2" | — |
| 5.3 Build and clear | "5.3" | — (5 fixed steps) |
| 5.4 Dose gate + dose scale | "5.4" | — |
| 5.5 Comparison | "5.5" | **comparison_row** (repeatable) |
| 5.6 Discovery story | "5.6" | — |
| 5.7 Ingredient grid | "5.7" | **ingredient** (repeatable) |
| 5.8 What to expect | "5.8" | — (3 horizons) |
| 5.9 Who should skip | "5.9" | — |
| 5.10 Reviews | "5.10" | **review** (repeatable, PLACEHOLDER) |
| 5.11 FAQ | "5.11" | **faq** (repeatable) |
| 5.12 Guarantee + CTA + disclaimer | "5.12" | — |

## 3. Image slots & recommended aspect ratios

All below-fold images are `loading="lazy"`, sized through `image_url`, with intrinsic width/height
to prevent layout shift. An empty picker renders nothing and never collapses the layout.

| Slot | Setting | Recommended | Direction |
|---|---|---|---|
| Gap lifestyle | `gap_img` | ~4:3, ≥1000px wide | Person 55–70 at home holding a lab printout. Not clinical, not a stock smile. |
| Discovery A | `disc_img_a` | ~4:3 | Lab / bench context. |
| Discovery B | `disc_img_b` | ~4:3 | Natto in cultural/heritage context — a bowl, a market, a breakfast table. **Not** a hero product shot. |
| Ingredient (per block) | `ingredient.image` | Square ~1:1, ≥600px | Optional. Clean product/ingredient shot. |

**Do not** put natto in the hero (that's the product-section team's shot). It is the single
most-cited disgust trigger in the comment corpus; it belongs only in the discovery band.

## 4. Correcting the Kaching selectors (no code edit)

The app's class names change between versions. Both selectors are **text settings**:

- **Settings → "Kaching selectors" → Kaching container selector** — default `.kaching-bundles__bar`
- **… → Kaching option selector** — default `.kaching-bundles__block`

To find the real ones: open the live PDP, right-click a bundle bar → Inspect, read the class on the
bar container (→ container selector) and on the individual clickable tier (→ option selector). Paste
them in. No redeploy needed.

**CTA behaviour (important):** every mid-page CTA **scrolls to the Kaching block and optionally
preselects a tier** — it never calls `/cart/add`. A direct add would strip the bundle discount.
If no target is found, the button's `#offer-block` href resolves normally; nothing throws. Give the
Kaching wrapper the id `offer-block`, or the CTA falls back to the container selector.

The **"Preselect bundle index"** setting (default `1`) picks which tier is auto-selected on click
(0 = first bar). Leave it blank to scroll only, no preselect.

## 5. What is PLACEHOLDER / pending substantiation

- **All product numbers** (10,000 FU, ingredient doses, guarantee, per-day cost, competitor tiers)
  are provisional defaults — verify against the COA/label. Full register: `CLAIMS-TO-SUBSTANTIATE.md`.
- **Reviews** — every `review` block is labelled *PLACEHOLDER — replace with verified reviews*.
  Replace all six before launch. Do not ship placeholder review text live.
- **Discovery pull-quote** — placeholder customer voice; replace with a real one.
- **Contact line** (`contact_line`) — currently `[COMPANY NAME] · [RETURNS ADDRESS] · …`. **Must be
  real** before launch (objection #8 depends on it).
- **`[CITATION NEEDED — …]` markers** appear inline in several bands; each is listed in
  `CLAIMS-TO-SUBSTANTIATE.md` with a source requirement and a fallback. Source them or soften the
  claim — do not delete the marker and ship the claim unsupported.
- **Soy-allergen line** (§5.9 + FAQ) carries a `[TODO]`; confirm against the COA allergen panel. If
  soy protein is detectable, the answer becomes a plain "no."

## 6. Design system (for anyone extending the section)

- **Palette:** 5 named CSS custom properties on `.vp-root` (paper, ink, accent-red, two greys). The
  oxygenated red is used **only** on verifiable numbers and the CTA — do not spread it.
- **Type:** display face = theme heading font (section heads); body = theme body font (≥16px,
  line-height ≥1.6); **monospace = every verifiable figure** (FU, mg, mcg, batch, review count,
  ages). The mono treatment is the signature — *anything in mono is something you can check.* Don't
  use mono for anything non-verifiable.
- **Numbering** appears only in §5.3 (a genuine sequence). Don't add numbered lists elsewhere.
- **Motion:** one scroll-fade on the dose scale, gated behind `prefers-reduced-motion`. Nothing else
  animates — animation density reads as "scam site" to this audience.
- **Scope:** all CSS is under `#shopify-section-{id} .vp-*`. No `!important`, no bare element
  selectors. Keep new styles inside that scope.
- Accessibility is a conversion requirement here (primary reader 50–75, on a phone): body ≥16px,
  contrast ≥4.5:1, visible keyboard focus, real `<details>` for the FAQ.
