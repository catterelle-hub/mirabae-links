# Handoff: Food Noise App landing page (for local Claude Code)

Read `CLAUDE.md` first. It has the design rules, the A2 palette, every Mirabae link and the real app facts.

## Done (on main after this PR is merged)

- `app.html`: pink A2 campaign landing page for the Mirabae app.
- All app buttons say "Start 7 days free" and link to the Whop Quiet Start checkout.
- Copy aligned with the real app: 20-second check-in + Quiet Score, Quiet Now, 7-Day Reset, Pattern Map.
- Mira (Text the Coach) is deliberately NOT promised: it is only in the $49 Mirabae Ritual plan, while the CTA sells Quiet Start ($19).

## Open, in this order

1. **Show the page on the link tree (links.mirabae.com)**
   - Add a featured link card to `index.html` pointing to `app.html` ("Quiet the food noise · Start 7 days free" or similar).
   - Confirm how links.mirabae.com is hosted (GitHub Pages, Vercel, other) and that `https://links.mirabae.com/app.html` loads after the merge. A nicer URL like `/app` may need a hosting rewrite or an `app/index.html`.
2. **Phone "camera pan" section with the real app**
   - The founder has a screen recording of the app (open app → home with Quiet Score → Quiet Now → 7-Day Reset). It was too large to attach in the cloud session.
   - Compress it with ffmpeg (H.264, about 720px wide, no audio, target under 8 MB), save as `img/app-demo.mp4` plus a poster frame `img/app-demo.jpg`.
   - Build a scroll-driven section: a phone tilts in 3D, the camera zooms in, the recording plays inside the phone. Respect `prefers-reduced-motion` (static poster). Pink campaign world outside the phone, the real cream/terracotta app inside.
3. **"60 seconds that read your noise" sequence** (replaces or extends the demo in the "Try it right now" block)
   - Three taps: when it gets loud (3 PM, after dinner, 11 PM, all day), what is under it (stress, boredom, tired, lonely, actually hungry), what happens after (regret, restrict next day, "Monday", nothing).
   - Reveal a pattern card using the app's real pattern names (founder to supply the list; "The Stress Grazer" is confirmed) plus one sentence that names the hidden reason.
   - Then a short Quiet Now style breath where the fridge notes fall away, then "Start 7 days free".
   - Label it as a preview, store nothing, no medical claims.
4. **Check with the founder**
   - Is "The app is the tool she wished she had at 23:14" (founder section) true to her story?
   - Whop shows "$23.75 crossed out → $19, Save 20%". If $23.75 was never charged, remove the strike price (EU reference-price rules, and the brand avoids discount culture).
   - Android: plan a PWA first (installable web app, free), then Google Play via a Trusted Web Activity. Check current Play fees, the closed-testing requirement for new accounts, and whether Whop billing is allowed for in-app subscriptions.
5. **Connect missing sources so future sessions see everything**
   - The app's code repo and its Vercel project are not visible to the connected GitHub/Vercel accounts. Install the Claude GitHub App on the app repo (https://claude.ai/connect-github) and connect the Vercel account that owns app.mirabae.com (https://claude.ai/customize/connectors).
   - Consider putting the "Mirabae Brain" notes in a private GitHub repo so cloud sessions can read them.

## Working rules

- Test every change with Playwright at 390px and desktop before showing it.
- Keep `app-a.html` / `app-b.html` as references; `app.html` is the live page.
- Higgsfield credits left: about 6 (as of 2026-10-11).
