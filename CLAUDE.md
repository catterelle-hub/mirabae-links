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
