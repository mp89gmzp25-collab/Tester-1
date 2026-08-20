# CLAIMS-TO-SUBSTANTIATE.md

> ## ⚠️ READ FIRST
>
> **Every product value referenced by this page is a target specification, not a verified product fact.**
> It exists so the copy could be written end-to-end without gaps. It is **not** a source of truth about
> what is in the bottle.
>
> **Nothing may ship to a live storefront until each line has been confirmed against the actual
> Certificate of Analysis, the manufacturer's spec sheet, and the finished label.**
>
> Every value below is a schema *default* that a human overwrites in the theme editor.

---

## A. Citation markers in the copy (claims needing a source)

| # | Claim (topic) | Location | What's needed | Fallback if unsupported |
|---|---|---|---|---|
| 1 | Fibrinolytic (clearing-side) activity declines with age | §5.3 step 3 | Citable source that fibrinolytic capacity decreases with age | Soften to "many people find…"; drop the age-specific mechanism |
| 2 | Nattokinase supports fibrinolytic activity (mechanism) | §5.3 close; §5.9 | Mechanism reference for nattokinase and fibrinolysis | Keep as structure/function support only, no mechanism detail |
| 3 | The widely-cited null RCT used ~2,000 FU | §5.4 (strongest argument) | ✅ **VERIFIED** — figure confirmed; written as a direct statement, marker removed | n/a |
| 4 | Nattokinase discovery attribution (found in a traditional food) | §5.6 | Discovery source/attribution | Keep "old food, looked at closely" framing, no name/date |
| 5 | Early functional timeline (weeks 1–4 onset) | §5.8; FAQ 5 | Onset/timeline evidence | Keep as "people commonly report," no clinical timeline |
| 6 | Long-term circulatory / cardiovascular support | §5.8 | Structure/function support reference | Permitted structure/function phrasing only |
| 7 | Fibrinolytic safety profile / mechanism specificity (plaque question) | §5.9 | Safety-profile reference for "supports a normal process, not a demolition" | Keep to "supports a normal process" + "see your doctor"; drop specificity |
| 8 | Dose threshold ("below a real dose the research doesn't apply") | §5.4; FAQ 1 | Support that studied benefits are dose-dependent above the low-FU range | Frame as "studies were run at meaningful FU," no implied hard cutoff |
| 9 | "CoQ10 is the nutrient statins deplete" | §5.7 ingredient 2 | Reference that statins lower CoQ10 | Soften to "a nutrient some people supplement alongside a statin" |
| 10 | Aged garlic studied for healthy blood pressure (already in range) | §5.7 ingredient 3 | Structure/function reference | Keep to "traditionally used," drop "studied" |

## B. Every provisional NUMERIC value (verify each against the COA / label)

| Value | Provisional | Where used | Verify against |
|---|---|---|---|
| Nattokinase potency | 10,000 FU per serving | ATF, trust bar, §5.4, §5.5, §5.7, FAQ | Finished-product COA, per serving |
| Strain | NSK-SD® | §5.5, §5.7, FAQ 7 | License to use on-pack |
| Capsules per serving | 2 | Directions, §5.7 | Label |
| Capsules per bottle | 60 | Trust bar / supply | Label |
| Supply | 30 days | Trust bar | Label |
| CoQ10 (ubiquinone) | 100 mg | §5.7 #2 | Label |
| Aged Garlic Extract | 600 mg | §5.7 #3 | Label |
| Vitamin K2 (MK-7) | 200 mcg | §5.7 #4 | Label |
| Pine Bark Extract (95% OPC) | 100 mg | §5.7 #5 | Label |
| Bromelain | 50 mg (500 GDU/g) | §5.7 #6 | Label |
| Null-study dose | ~2,000 FU | §5.4 | The actual cited trial's method |
| Competitor tiers on dose scale | 2,000 / 4,000 / 5,000 FU | §5.4 visual, §5.5 | Normalise per **serving**, not per capsule |
| Guarantee | 180 days, keep the bottle | §5.12, FAQ 10 | Fulfilment will honour |
| Shipping | Tracked, 3–5 days US (no free-shipping claim; cost TBD) | §5.12 | Ops |
| Cost per day | $1.33 / $1.17 / $1.00 | ATF risk-reversal, §5.12 | Kaching tier prices |
| Rating / review count | placeholder | ATF, §5.10 | Real review data |

## C. Product-fact TODOs (inputs / verifications, not citations)

- Soy-allergen status — **single most important line to verify** (§4 of spec). Confirm the COA allergen panel. If detectable soy protein, FAQ 9 becomes a plain "no."
- Batch COA + QR: must be live, or the QR line and "batch COA published" claim are removed and copy downgraded to "third-party tested."
- Third-party testing scope: per-lot vs per-product (copy currently says per lot).
- cGMP / FDA-registration status confirmed in writing.
- Country of manufacture (USA) + strain origin (Japan) confirmed.
- Contraindication list (§5.9) reviewed by a qualified person.
- Legal identity — MUST be real, no invented defaults: company legal name, returns address, support email, support phone, support hours.
- Kaching container + option selectors (from live PDP inspector).
- FU stated **per serving** everywhere; competitor comparisons normalised to a daily dose.
- Optional 7th active (turmeric): omitted by default per spec recommendation; add only if in the tablet.

## D. Regulatory note

US dietary-supplement context (DSHEA). Permitted verbs used: *supports healthy circulation, supports
normal fibrinolytic activity, supports healthy blood flow, supports cardiovascular function.* Banned and
confirmed absent: reverses plaque, unclogs arteries, removes %, treats/cures/prevents any disease,
replaces medication. The FDA structure/function disclaimer ("This statement has not been evaluated…")
ships via a schema `richtext` disclaimer setting and must appear near the claims.

## E. Pre-launch substantiation checklist (from the product spec §10)

- [ ] FU potency confirmed on a finished-product COA, per serving
- [ ] Strain name confirmed and licensed for on-pack use
- [ ] Every ingredient dose matches the finished label exactly
- [ ] Allergen panel reviewed; soy language corrected to match
- [ ] Third-party testing scope confirmed (per lot vs per product)
- [ ] Batch COA + QR either live, or removed from the copy
- [ ] cGMP / FDA-registration status confirmed in writing
- [ ] Country of manufacture and strain origin confirmed
- [ ] Contraindication list reviewed by a qualified person
- [ ] The open `[CITATION NEEDED]` items sourced or the claims dropped
- [ ] Guarantee terms match what fulfilment will honour
- [ ] Company name, address, phone, email are real
- [ ] Full page reviewed against DSHEA structure/function limits
