# PROJECT LEDGER — The Homestead Toolshed

Single source of truth. Read fully at session start. Update before session end.

---

## Current status

**Phase:** 1 (foundation) — both Phase-1 tools LIVE; first post pending (human)
**Live site:** https://jbourgogne.github.io/homestead-toolshed/
**Repo:** https://github.com/JBourgogne/homestead-toolshed (Pages: main + /docs)
**Tools shipped:** 2 live (egg cost, coop size)

---

## Next Actions (queue — do from the top)

1. **Waiting on human:** Reddit account is aging (~2026-08-02 earliest post
   date). When the first post goes up, gather every piece of feedback into the
   ledger and act on the actionable ones.
2. **Verify tool #2 on the live site** (pushed at end of session 2 — confirm
   Pages rebuilt, spot-check both tools).
3. After tools 1–2 are live and posted: revisit the candidate list against any
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
| 1 | What do your eggs really cost? | `/docs/egg-cost/` | **Live** — https://jbourgogne.github.io/homestead-toolshed/egg-cost/ |
| 2 | How big should your coop be? | `/docs/coop-size/` | **Live** — https://jbourgogne.github.io/homestead-toolshed/coop-size/ |

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

### Task 2 — Read the three post drafts in `/outreach`, then post the first (~10 min)

The live URL is already in the drafts. Steps:

1. Read `outreach/README.md` (ground rules) and the three drafts. Note any
   objections — especially to the AI-disclosure line (see standing decisions).
2. Check r/homestead's rules on self-promotion (sidebar/wiki). If unclear,
   modmail first using the one-liner in the draft's header note.
3. Post `post-r-homestead.md` (adapt the words to your own voice freely —
   authenticity beats polish).
4. Over the following days: reply to every comment, and paste anything
   interesting (praise, complaints, feature requests, "this is wrong") into
   the ledger's parking lot — or just tell Claude next session.
5. Stagger the other two posts per the README (BYC forum needs an account with
   a bit of genuine participation first — start that whenever).

## Human Tasks (completed)

- 2026-07-26 — Handed project off from claude.ai session 0 into Claude Code.
- 2026-07-26 — **Task 1 done (deploy):** human created the GitHub repo and
  authenticated `gh` for the personal account (JBourgogne) alongside the work
  account; Claude pushed, enabled Pages via API, and verified the live site.

## Open questions / parking lot

- Domain name: GitHub Pages default is fine to start; a custom domain (~$10/yr)
  is a later, optional human decision once tools exist.
- Analytics: propose a privacy-respecting option to the human only after launch.
- Monetization: revisit only after evidence of real usage (Phase 3).
- Egg tool possible future enhancements (only if feedback asks): break-even
  selling price; breed presets for lay rate; metric units. Shipped > perfect.
- Machine note: `gh`'s credential helper only serves the *active* account's
  token, so pushing this repo requires:
  `gh auth switch -u JBourgogne` → `git push` → `gh auth switch -u jacobbourgogneRSC`
  (keep the work account active at rest).

## Roadmap

- **Phase 1 — Foundation:** validate ✅, build tools 1–2 (1 of 2 ✅), deploy,
  first posts.
- **Phase 2 — Portfolio:** grow to 5–8 tools, iterate on whichever gets shared,
  keep the index/branding consistent.
- **Phase 3 — Compounding:** double down on winners, consider affiliate links or
  a paid planner, custom domain, light analytics.

---

## Session Log

### Session 2 — 2026-07-26 (Claude Code, same day)
- **Human progress:** Reddit account created, r/homestead + r/BackYardChickens
  joined. Account aging + light genuine participation for ~3–7 days before the
  first post (≈2026-08-02). Claude declined to create the account for the
  human — accounts/credentials are the human's alone, and a manufactured
  account would undercut the transparency principle anyway.
- **Visual pass done:** live site checked in light mode (via injected token
  override) and at simulated phone width — hero, verdict, collapsed stat tiles
  all render cleanly. Dark + light both confirmed good.
- **Built tool #2: "How big should your coop be?"** (`/docs/coop-size/`).
  Two modes: plan (birds → coop/run sq ft with suggested buildable dimensions,
  roost length, nest boxes) and check (existing coop/run dimensions → honest
  bird capacity with the bottleneck named). Bird-size classes
  (bantam/standard/heavy), cold-winter bump (+1 sq ft/bird coop), free-range
  note. Explainer cites poultry extension space-allowance guidance and is
  honest that extension minima are lower than the community 4/10 standard we
  default to. Verified locally: all six test scenarios correct (24 sq ft for
  6 standard, cold bump, heavy sizes, capacity checks, too-small warning).
  Fixed a truncated select by moving it to a full-width field.
- Index updated with the new tool card; r/homestead draft updated to mention
  tool #2; segmented-control + select styles added to the shared stylesheet.
- **Next:** confirm Pages rebuild; then it's feedback-gathering once the human
  posts. Tool #3 decision deliberately waits for real-world feedback.

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
- **Deployed live, same day.** Human created the repo and added personal-account
  auth (a work account was the default and blocked the first push); Claude
  pushed, enabled Pages via the API (main + /docs), verified the live site in
  the browser, put the live URL into the outreach drafts (pointing straight at
  the tool page) and into the copy-my-result text.
  **Site: https://jbourgogne.github.io/homestead-toolshed/**
- **Next session:** check whether the first post happened and log any feedback;
  light-mode + phone-width visual pass; start tool #2 (coop/run size).

### Session 0 — 2026-07-26 (claude.ai)
- Founded the experiment. Agreed on operating model: human provides ~10 min/week
  of real-world hands; Claude directs and builds autonomously via this ledger.
- Ran market research (see RESEARCH_NOTES.md). Concluded generic calculator SEO
  is unwinnable; community-distribution strategy adopted.
- Selected homesteading niche (backup: RV/vanlife power). Chose static-site,
  free-hosting architecture. Wrote CLAUDE.md protocol and this ledger.
- Next: Session 1 in Claude Code — validation pass, then first build.
