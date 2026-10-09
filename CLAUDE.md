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
