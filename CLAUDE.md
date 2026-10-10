# Mirabae: design rules for Claude

Goal: real design aesthetics and uniqueness, never generic AI web design.

## Skill hierarchy

1. **Base, always:** `impeccable` (design quality, critique, polish) and `emil-design-eng` (UI details, motion feel).
2. **Motion work:** use the Emil skills (`animate`, `review-animations`, `find-animation-opportunities`, `apple-design`).
3. **Taste skills, only on purpose:** use `taste-skill` / `redesign-skill` only when we design something new or redo a page. Do not mix `soft-skill` and `minimalist-skill` in one design; pick one direction.
4. When skills conflict, the Mirabae brand wins over any skill default.

## Workflow

- The user describes what they want; Claude builds it exactly that way.
- With every change, suggest 2 to 3 concrete ideas to make it more aesthetic and more unique.
- Test with Playwright: screenshots at phone width (390px) and desktop before showing results.
- Ask before changing the brand direction (colors, fonts, logo).

## Brand (current)

- Colors: black `#0A0A0A`, gold `#B8986A`, cream `#F6F0E7`.
- Fonts: Cormorant Garamond (display), Montserrat (text).
- Known risk: this combo is common in beauty link pages; push uniqueness through imagery, layout and motion.

## Food Noise App page (`app.html`, chosen 2026-10-09: variant A2)

- Colors: raspberry `#C8216F` (white type on it), aubergine `#2A0B3B`, blush `#F9DCE9`, petal `#FFC3DD`; pink as text on light grounds uses `#B5115A`.
- Fonts: Bodoni Moda only at display sizes, Hanken Grotesk for everything else (16px minimum).
- Photos: grayscale duotone (raspberry highlights, aubergine shadows) via CSS blend modes.
- Audience (TikTok, Oct 2026): 87% women, ~85% under 35; the founder's target is 35 to 50, so the page must work for both.
- Tone: no shame, no counting, no medical promises; always point to professional help for real distress.
- Alternatives kept for reference: `app-a.html` (louder fuchsia), `app-b.html` (aubergine-led).

## Mirabae links and facts (do not ask the founder again)

- Food Noise App (web app, hosted on Vercel): https://app.mirabae.com ("Mirabae · Food Noise Coach")
  - Features: 20-second daily check-ins, Quiet Score, food-noise patterns (e.g. "The Stress Grazer"), "Quiet Now" emergency program, 7-Day Reset, Mira (in-app text coach), Pattern Map, lessons, journaling, Satiety Plate.
  - Plans via Whop, 7-day free trial, cancel anytime: Quiet Start $19/mo https://whop.com/checkout/plan_vwpPc8bgB1u1w · Mirabae Ritual $49/mo https://whop.com/checkout/plan_e5cn9Mu03t5Kg
  - Whop product page: https://whop.com/mirabae-0696/mirabae-app/
  - Landing page CTA should say "Start 7 days free".
- Link hub: https://links.mirabae.com (this repo, index.html)
- Shop: https://www.mirabae.com · Brainelle: https://www.mirabae.com/products/brainelle?variant=52952487330130
- Anima (kefir fibre powder): https://anima.mirabae.com (repo catterelle-hub/anima-landing)
- The Appetite Recode (ebook): https://whop.com/mirabae-0696/the-appetite-recode
- Founder: Anjelika. 1:1 coaching via app.mirabae.com/coaching-apply.
- Where things live: app code is NOT in this repo and not visible to the connected GitHub/Vercel accounts (as of 2026-10-10); Notion "Mirabae — Master Operating Hub" holds older ops notes; the "Mirabae Brain" notes live on the founder's Mac unless synced.
