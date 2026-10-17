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

## The Mirabae Lab (built 2026-10-17, branch `claude/mirabae-lab`, live after merge)

- `lab.html` at `/lab`: public vote on which finished formula gets made first (Brainelle, Anima, Miralemon). Votes counted 31 January 2027. Bottom entry in the link tree ("The Mirabae Lab · What we're making next").
- Approved copy (founder, 2026-10-17): hero "Not on any shelf. Yet." / "Collagen and green tea energy in one morning drink. Fiber made for your kefir. A soda with saffron in it." (changed 2026-10-17: Brainelle is not a green tea drink; green tea is its caffeine source) / "No boardroom decides. You do." Why vote: decide what gets made first, first access, founding price on the first order. Hooks: Brainelle "Brain and beauty. One scoop. Green tea, not coffee."; Anima "Your kefir brings the bacteria. Anima feeds them."; Miralemon "Soda, rewritten." Never write "coffee" as if it were an ingredient (Brainelle has green tea caffeine).
- Prism: CSS glass prism, drawn at 2x and shown at 1x for sharpness; it pauses 3 s on each pack flat (2D, razor sharp), spins in on load, glow colour and giant outlined name per product, sparkle burst on each rest, scroll gives it a spin, flick inertia. A Three.js glass version existed (commit 5db2ce6) but the founder preferred the CSS glass.
- Packs: 4K upscaled (WaveSpeed image upscaler) and cut out locally with macOS Vision (`VNGenerateForegroundInstanceMaskRequest`), saved as WebP in `img/lab/cut/`. Miralemon shows Keanu, the founder's golden British Shorthair, smiling with open eyes.
- Klaviyo via the public form endpoint, one list per product: Brainelle `TCGeRD`, Anima `TGRgd4`, Miralemon `WdVJcj`. Properties: lab_first_choice, lab_also_curious, lab_would_order (yes/maybe/no), lab_voted_at, lab_feedback (max 300 chars), lab_feedback_product.
- Typography: Bodoni Moda with explicit optical size ('opsz') for running text and italic display lines; default optical sizing made hairlines vanish.
- Reel: Remotion project `~/Documents/MirabaeReels/lab-reel` (12 s, 9:16). Rendering needs the founder's own terminal (headless Chrome crashes inside Claude's sandbox): `cd ~/Documents/MirabaeReels/lab-reel && npx remotion render LabReel <output.mp4>`.
