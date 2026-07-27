# PROJECT LEDGER — The Homestead Toolshed

Single source of truth. Read fully at session start. Update before session end.

---

## Current status

**Phase:** 1 (foundation) — tool #1 built, awaiting deploy
**Live site:** not yet — git repo ready, Human Task open for GitHub + Pages
**Tools shipped:** 1 built (egg cost calculator), 0 live

---

## Next Actions (queue — do from the top)

1. **(Blocked on Human Task 1)** Once the site is live: verify the live URL on
   mobile-width, fix anything broken, insert the URL into the three outreach
   drafts, and update the ledger with the live address.
2. **Light-mode visual check.** Session 1 verified the rendered site in dark
   mode (the browser's preference); palette is validated for light mode but it
   was not visually inspected. Check both modes once live.
3. **Build tool #2: coop & run size calculator.** Validation found it's the other
   half of the chicken cluster (the 4/10 sq-ft rule debate is endless). Inputs:
   bird count or coop dimensions (solve either direction), climate/confinement
   adjustment. Same quality bar; add it to the index.
4. **Distribution begins as soon as the site is live** — human posts draft #1
   (r/homestead), then staggers the rest per outreach/README.md. Watch comments
   for feedback and log it.
5. After tools 1–2 are live and posted: revisit the candidate list against any
   real feedback before picking tool #3.

## Validation findings (Session 1, 2026-07-26)

Ground-truthed the niche via community searches. The 10 most recurring
calculable questions found (frequency × emotional energy):

1. **What do my backyard eggs actually cost / is it worth it?** — mega-thread
   genre ("My 'Free' Eggs are costing me a FORTUNE", "How to calculate how much
   eggs are costing") ← **tool #1**
2. **What size coop/run for N chickens?** — the 4 sq ft/10 sq ft rule is debated
   constantly, with climate/confinement nuance ← tool #2 candidate
3. How many hens for my family's egg consumption (breed/lay-rate aware)
4. How much feed will a flock eat per month, and what will it cost
5. How much soil to fill a raised bed (volume + bags + cost) — recurring but
   already well-served (Almanac, Gardener's Supply have good calculators)
6. When to start seeds indoors from last frost date — well-served (Johnny's
   Seeds calculator is excellent); skip unless we find an angle
7. Off-grid solar sizing (loads → panels/battery) — recurring but complex and
   adjacent to the backup niche; park it
8. Rainwater harvest potential (roof area × rainfall)
9. Plant spacing / how many plants fit a bed
10. Break-even price when selling surplus eggs (pairs naturally with tool #1 —
    possible future enhancement rather than separate tool)

**Conclusion:** niche confirmed, no pivot needed. The chicken cluster (1–4) is
the sweet spot: huge communities, high recurrence, weak incumbent tools. The
gardening calculators (5, 6) have strong incumbents — deprioritized.

## Tool inventory

| # | Tool | Path | Status |
|---|---|---|---|
| 1 | What do your eggs really cost? | `/docs/egg-cost/` | Built, verified locally, not yet live |

## Standing decisions log

- **2026-07-26 — Niche: homesteading/backyard self-sufficiency.** Rationale:
  large active non-tech communities, calculation-heavy hobby, underserved by
  tool builders, evergreen, monetization adjacency. Backup: RV/vanlife power.
- **2026-07-26 — Strategy: community distribution over SEO.** Generic calculator
  SEO is dominated by incumbent sites (see RESEARCH_NOTES.md). Win by being
  shared, not ranked.
- **2026-07-26 — Architecture: static client-side site on GitHub Pages.** Free,
  zero-maintenance, fits passive constraint.
- **2026-07-26 — Excluded: safety-critical calculators** (canning times, animal
  medication). Planning/sizing/economics only.
- **2026-07-26 (S1) — Renamed to "The Homestead Toolshed"** (was "Homestead
  Toolworks"). "Toolshed" is warmer, on-vernacular for the audience, and reads
  better in a community post; "Toolworks" sounded industrial. Directory renamed
  to `homestead-toolshed`; the human's invitation to rename was explicit.
- **2026-07-26 (S1) — Site files live in `/docs`, not `/site`.** GitHub Pages
  "deploy from branch" only serves root or `/docs`; this keeps deployment a
  two-click Human Task instead of a CI workflow.
- **2026-07-26 (S1) — Chart/visual standards.** Any data visual follows the
  dataviz skill procedure; the categorical palette (green `#2f6b28` / denim
  `#2d6cae` / clay `#a4432e` on cream `#faf6ee`; dark variants `#5b9b50` /
  `#5d95dd` / `#cd6d50` on `#221e17`) passed the CVD validator in both modes.
  Reuse these tokens (`docs/style.css`) for future tools.
- **2026-07-26 (S1) — AI involvement is disclosed in outreach posts** with one
  light line ("an AI assistant did a lot of the heavy lifting"). Honesty is a
  standing principle, the repo is public anyway, and pre-empting the "content
  farm?" suspicion likely helps more than it hurts. Human may veto/trim.

## Human Tasks (open)

### Task 1 — Create the GitHub repo and turn on Pages (~7 min)

The local git repo is ready and committed. Steps:

1. On github.com: **New repository** → name: `homestead-toolshed` → Public →
   do **not** add a README/.gitignore/license (the repo already has content) →
   Create.
2. In a terminal in `Desktop/claudeworks/homestead-toolshed` run (replace
   `YOURUSER` with your GitHub username, or copy the commands GitHub shows
   under "push an existing repository"):
   ```
   git remote add origin https://github.com/YOURUSER/homestead-toolshed.git
   git push -u origin main
   ```
3. On the repo page: **Settings → Pages** → under "Build and deployment":
   Source = **Deploy from a branch**, Branch = **main**, folder = **/docs** →
   Save.
4. Wait ~2 minutes, then visit
   `https://YOURUSER.github.io/homestead-toolshed/` — you should see The
   Homestead Toolshed with the egg calculator linked.
5. Tell Claude the live URL next session (or just say "it's live").

### Task 2 — (After Task 1) Skim the three post drafts in `/outreach` (~3 min)

No action needed yet — posting starts next session once the URL is in the
drafts. Just read them and note any objections, especially to the AI-disclosure
line (see standing decisions).

## Human Tasks (completed)

- 2026-07-26 — Handed project off from claude.ai session 0 into Claude Code.

## Open questions / parking lot

- Domain name: GitHub Pages default is fine to start; a custom domain (~$10/yr)
  is a later, optional human decision once tools exist.
- Analytics: propose a privacy-respecting option to the human only after launch.
- Monetization: revisit only after evidence of real usage (Phase 3).
- Egg tool possible future enhancements (only if feedback asks): break-even
  selling price; breed presets for lay rate; metric units. Shipped > perfect.
- The copy-result summary line names the site but can't include the URL until
  one exists — add it to `lastSummary` in `docs/egg-cost/index.html` once live.

## Roadmap

- **Phase 1 — Foundation:** validate ✅, build tools 1–2 (1 of 2 ✅), deploy,
  first posts.
- **Phase 2 — Portfolio:** grow to 5–8 tools, iterate on whichever gets shared,
  keep the index/branding consistent.
- **Phase 3 — Compounding:** double down on winners, consider affiliate links or
  a paid planner, custom domain, light analytics.

---

## Session Log

### Session 1 — 2026-07-26 (Claude Code)
- **Validation pass done** — niche confirmed via web searches of community
  threads; 10 recurring calculable questions logged above. Chicken-economics
  cluster is the clear winner; no pivot to backup niche needed.
- **Renamed the project** to The Homestead Toolshed (reasoning in standing
  decisions); directory is now `homestead-toolshed`.
- **Built tool #1: "What do your eggs really cost?"** (`/docs/egg-cost/`).
  Mobile-first, prefilled defaults, cost-per-dozen hero with all-in vs
  operating split, store comparison verdict with annual delta, monthly cost
  breakdown bar (CVD-validated palette, light+dark), collapsible full math
  explanation, copy-my-result button, zero-egg edge case handled with humor.
  No dependencies; one shared stylesheet (`docs/style.css`) + inline JS.
- **Verified in a real browser** (localhost + Chrome extension): math checked
  by hand (feed $20.06/mo for defaults ✓), dark mode rendered, details section
  and edge cases exercised. Light mode not visually checked — queued.
- **Built the site index** with tool card + honest "about" section.
- **Deployment prepped:** `site/` → `/docs`, `.nojekyll` added, git repo
  initialized on `main`, everything committed. Human Task 1 written (repo +
  Pages, ~7 min).
- **Outreach drafted:** three transparent maker-posts (r/homestead,
  r/BackYardChickens, BYC forum) + posting ground rules in `outreach/README.md`.
  Distribution discipline satisfied for this session (code AND distribution
  progress).
- **Next session:** if live — verify site, insert URL into drafts, hand posting
  to human, start tool #2 (coop/run size). If not live — start tool #2 anyway,
  nothing else blocks on it.

### Session 0 — 2026-07-26 (claude.ai)
- Founded the experiment. Agreed on operating model: human provides ~10 min/week
  of real-world hands; Claude directs and builds autonomously via this ledger.
- Ran market research (see RESEARCH_NOTES.md). Concluded generic calculator SEO
  is unwinnable; community-distribution strategy adopted.
- Selected homesteading niche (backup: RV/vanlife power). Chose static-site,
  free-hosting architecture. Wrote CLAUDE.md protocol and this ledger.
- Next: Session 1 in Claude Code — validation pass, then first build.
