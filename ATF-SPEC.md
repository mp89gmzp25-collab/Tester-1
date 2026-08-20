# ATF-SPEC.md — Above-the-Fold Specification (Dova Nattokinase "Vascular" PDP)

> This file is Section 4 of the build brief, reproduced verbatim for the hero/product-section team.
> It is **not** built inside `sections/vascular-pdp.liquid` — it is the spec for the existing Shopify
> product section and the hero image commission. Treat it as the highest-leverage part of the job.
>
> Reference competitor benchmark: Luma Nutrition runs 120K monthly visits at **82% bounce** on a
> 4,000 FU page. The dose is visible on their bottle. That is what a lost ATF looks like in this category.

The visitor arrives from a creator video with roughly four seconds of patience and one question in mind: *is this the 10,000 FU one, or the useless one?*

Everything above the fold answers that question and one other: *do I have to eat the beans?*

## Required elements, in priority order

**1. The dose, as the largest number on the screen.**
Not a bullet. Not a badge. The hero number. `10,000 FU per serving` set in the display face at a size that reads on a 380px viewport without scrolling. This is the entire reason they clicked.

**2. The disqualifier, immediately beneath it.**
One line, no more: *"Most nattokinase sells at 2,000–5,000 FU. The research they're quoting was run at 10,000."*
This does the competitor-killing and the null-study rebuttal simultaneously, in fourteen words.

**3. The food escape hatch, in the subhead.**
Because it is the top-liked product comment in the dataset. Something in the register of: *"The dose from a bowl of natto. Without the bowl of natto."*
Do not be cute about the smell. One dry acknowledgement is enough; more reads as insecure.

**4. Three functional outcomes — felt, not measured.**
Cold hands and feet. Numbness in the legs. Stamina through the afternoon.
Not: longevity, plaque, arterial age, life expectancy. Not lab values as the primary promise — the audience's line is *"good numbers, cold hands."* They have been told their numbers are fine and they still feel bad.

**5. Trust strip — four items maximum, icons + two-word labels.**
Third-party tested · cGMP facility · Non-GMO · No proprietary blends.
If a batch-level COA or a scannable batch QR exists, **it goes here and it outranks everything else in the strip.** NF Supplements runs a QR on the bottle that scans to the actual batch test — it is the sharpest answer in the category to "mysterious pill filled with crap," and it converts a claim into a verifiable action.

**6. Rating + review count.** Star row, numeral, "verified buyers." One line.

**7. The Kaching offer block.** Not built here. Must sit within the first scroll on mobile.

**8. Risk reversal, directly under the buy button.** Guarantee length, shipping speed, cancel-anytime if subscription. Single line, small type.

**9. A quiet safety link.** `Not right for everyone — who should skip this →` anchoring to the safety section.
Counter-intuitive but correct: putting this above the fold *raises* trust with an audience whose loudest objection is bleeding risk. Every competitor buries it. Being the one brand that leads with it is a positioning asset, not a leak.

## Hero image direction (for later commission)

The hero image can carry claims and objection-handling directly, in the manner of the competitor ad creative already reviewed. Recommended payload, in order:

- The FU number, large, unmissable
- Side-by-side bottle comparison: a generic 4,000 FU bottle vs Dova, with a checkmark/cross on FU verification and strain naming
- Three outcome callouts in boxes (the functional three above)
- Certification bar along the bottom edge

Do **not** put natto in the hero photograph. It is the most-cited disgust trigger in the entire comment corpus — "looks like cat food," "gerbil poop," "dog food," "snot." Natto belongs in the story section further down, where it is context rather than product.

## Explicit ATF bans

- Any longevity or lifespan language
- The word "miracle," "breakthrough," "secret"
- Japan-vs-America political framing (it buys reach in the ad; on the page it starts an argument instead of a sale)
- A wall of ingredient text before the dose number
- Autoplay video

---

## Implementation notes for the product-section team (not part of the verbatim spec)

- The hero FU number must be set in the **monospace utility face** defined in the section's design system (see `README-vascular-pdp.md` §Design). Anything verifiable is mono; the FU number is the first instance of that system.
- Confirm the real product FU before shipping. If the product is **not** ≥10,000 FU, escalate — the entire page argument assumes the dose clears the market's installed threshold. Do not paper over a lower number.
- The safety anchor link (#9) should point at the section's `#vp-safety` id.
- The mid-page CTAs in the built section scroll to `#offer-block`; make sure the Kaching block (or its wrapper) carries that id, or update the selector settings.
