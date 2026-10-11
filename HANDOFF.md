# Handoff: Food Noise App landing page (for local Claude Code)

Read `CLAUDE.md` first. It has the design rules, the A2 palette, every Mirabae link and the real app facts.

## Done (on main after this PR is merged)

- `app.html`: pink A2 campaign landing page for the Mirabae app.
- All app buttons say "Start 7 days free" and link to the Whop Quiet Start checkout.
- Copy aligned with the real app: 20-second check-in + Quiet Score, Quiet Now, 7-Day Reset, Pattern Map.
- Mira (Text the Coach) is deliberately NOT promised: it is only in the $49 Mirabae Ritual plan, while the CTA sells Quiet Start ($19).

## Done on 2026-10-11 (local Claude Code, branch `claude/linktree-and-app-demo`)

- **Link tree (`index.html`)**: rebuilt from the July version that was never pushed. Order: Quiz, App (now `/app`, the landing page), Open Your App, Private Coaching (`app.mirabae.com/coaching-apply`), The Appetite Recode, Shop. Removed Brainelle (dead carrd link) and Anima (parked, DECISION-015 in the Brain).
- **Hosting confirmed**: Vercel project `mirabae-links`, Git connected; every merge to `main` deploys to production (links.mirabae.com). `vercel.json` with `cleanUrls` makes `/app` work.
- **Phone section** ("Inside the app", between "Imagine forgetting about food" and the offer): scroll driven 3D phone, the real screen recording plays inside, captions follow the video (Quiet Score, Quiet Now, 7-Day Reset). Reduced motion: no tilt, video with controls, no autoplay.
- `img/app-demo.mp4` (720px, 25.5 s, 2.5 MB, no audio) and `img/app-demo.jpg`, cut from `Screen_Recording_20261003_123049_Chrome.mp4` (Downloads on the founder's Mac). Segments used: 98.5 to 104.5 s, 14.5 to 27 s, 44 to 48.5 s, 54 to 56.5 s. **Never use 5 to 10 s (share sheet with contacts and a phone number) or 113 to 125 s (account screen with the founder's email).**
- Tested at 375px, 1280x720 and 1440x900: no horizontal scroll, no console errors.

## Open, in this order

1. **"60 seconds that read your noise" sequence** (replaces or extends the demo in the "Try it right now" block)
   - Three taps: when it gets loud (3 PM, after dinner, 11 PM, all day), what is under it (stress, boredom, tired, lonely, actually hungry), what happens after (regret, restrict next day, "Monday", nothing).
   - Reveal a pattern card using the app's real pattern names, seen in the recording on 2026-10-11: The Stress Grazer, The Evening Unraveler, The Reward Seeker, The Perfectionist Restrictor, The Emotional Soother (plus "Real Hunger"). Note: the quiz at quiz.mirabae.com uses a different set (Pressure Eater, Achiever's Trap, Night-Brain, Cycle Keeper, Feeling Feeder); the founder must decide which set is canonical plus one sentence that names the hidden reason.
   - Then a short Quiet Now style breath where the fridge notes fall away, then "Start 7 days free".
   - Label it as a preview, store nothing, no medical claims.
2. **Check with the founder**
   - Done 2026-10-11: the founder rejected "The app is the tool she wished she had at 23:14" (sounds like AI, too specific). Replaced with: "Today she eats full plates and her head stays quiet around food. It took her years to get there. The app is everything that helped, made small enough to fit into your day."
   - Settled 2026-10-11: the Whop strike price ($23.75 crossed out, $19) stays for now. The founder checked with Whop support; Whop offers no other way. Do not raise it again unless Whop changes this.
   - Android: plan a PWA first (installable web app, free), then Google Play via a Trusted Web Activity. Check current Play fees, the closed-testing requirement for new accounts, and whether Whop billing is allowed for in-app subscriptions.
3. **Connect missing sources so future sessions see everything**
   - The app's code repo and its Vercel project are not visible to the connected GitHub/Vercel accounts. Install the Claude GitHub App on the app repo (https://claude.ai/connect-github) and connect the Vercel account that owns app.mirabae.com (https://claude.ai/customize/connectors).
   - Done: the Mirabae Brain is a private GitHub repo (`catterelle-hub/Mirabae-Brain`) since 2026-10-10.

## Working rules

- Test every change with Playwright at 390px and desktop before showing it.
- Keep `app-a.html` / `app-b.html` as references; `app.html` is the live page.
- Higgsfield credits left: about 6 (as of 2026-10-11).

## The Mirabae Lab (in progress, branch `claude/mirabae-lab`, 2026-10-11)

Decided with the founder (Brain: DECISION-015 amendment, `20-products/miralemon.md`, `20-products/brainelle.md`):
- New page `lab.html` (first draft in this branch, not tested yet): pink campaign energy, three products (Brainelle, Anima, Miralemon) with prices and founding prices, multi-select waitlist posting to Klaviyo lists via the public form endpoint (same as anima.mirabae.com): Brainelle `TCGeRD`, Anima `TGRgd4`, Miralemon `WdVJcj`. Optional "Would you order it at launch?" (Yes / Maybe).
- One quiet link tree entry at the very bottom: "The Mirabae Lab · What we're making next" (not added yet).
- Fix in lab.html before shipping: "Kefir Fibre Powder" must be "Kefir Fiber Powder" (matches the Anima box, US market).
- Animation plan: Lenis smooth scroll (desktop only), GSAP (official GreenSock skills installed in ~/.claude/skills), SplitText hero, ScrollTrigger card reveals, a click spark on "I want this", and a slowly rotating three sided product prism with silver or gold edges that reacts to mouse and tilt. Inspiration: resend.com's Spline cube; take the technique, never copy the cube.
- Next step when the session resumes: founder approval of 4 packaging drafts (Brainelle powder tub x2, Miralemon can x2) on Nano Banana via WaveSpeed, about $0.16 total. Refs prepared in `~/Mirabae-Brain/generations/refs/` (anima_box_ref.png, mirabae_logo_gold.webp, miralemon_can_draft1_ref.jpg). Approved label copy is in the Brain product files and in the session; Brainelle is now a powder ("Brain & Beauty Morning Drink", "Collagen Powder Dietary Supplement").
