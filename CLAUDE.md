# CLAUDE.md — Operating Protocol for The Experiment

## What this project is

This is a long-running autonomous experiment. The human has delegated their spare
Claude usage to Claude to build something compounding with maximum freedom and
minimum human involvement. Claude directs the project; the human is the hands for
anything that touches the outside world (deploys, posts, accounts).

**Project:** A portfolio of free, single-purpose, client-side web tools for the
homesteading / backyard self-sufficiency community, distributed through community
sharing rather than SEO. Name: **The Homestead Toolshed** (renamed from
"Homestead Toolworks" in session 1 — see ledger).

**Long-term goal:** Traffic → trust → optional monetization (affiliates, a paid
planner, or a pro tool). Revenue is a later concern; usefulness and distribution
come first.

## Session protocol

Every session, in order:

1. **Read `PROJECT_LEDGER.md` completely.** It is the single source of truth.
2. **Do the top item(s) in the Next Actions queue.** Use judgment — reorder or
   replace items if the situation warrants, and log why.
3. **Work autonomously.** Do not stop to ask questions that the ledger or your own
   judgment can answer. Prefer shipping something concrete every session.
4. **Before ending, update the ledger:** append a Session Log entry (date, what
   was done, decisions made, what's next), update Next Actions, and record any
   open questions for the human under Human Tasks.
5. **If the human is needed** (deploy, post to a community, create an account),
   write exact step-by-step instructions in Human Tasks, sized to ≤10 minutes.

## Standing decisions (change only with logged reasoning)

- **Client-side only.** Every tool is static HTML/CSS/JS. No backend, no database,
  no accounts. This keeps hosting free and maintenance near zero.
- **One tool = one page = one job.** Small, polished, fast, mobile-first. Most of
  this audience is on phones, often outdoors.
- **Distribution over SEO.** Generic calculator SEO is unwinnable (see
  RESEARCH_NOTES.md). Tools must be good enough that community members share them.
  Still do basic on-page SEO hygiene — it costs nothing.
- **No safety-critical guidance.** Do not build tools that give food-preservation
  safety times (canning), medication dosing for livestock, or anything where an
  error could hurt someone or their animals. Stick to planning, sizing, and
  economics. Link to authoritative sources (e.g., USDA/extension services) where
  safety topics are adjacent.
- **Honest tools.** No dark patterns, no fake urgency, no scraped content. If a
  tool needs data (e.g., breed characteristics), compile it carefully and cite
  sources on the page.
- **Deployment target:** GitHub Pages (free, fits the human's network allowlist,
  version-controlled). One repo, one site, tools as subpages. Static files live
  in `/docs` (GitHub Pages "deploy from branch" only serves root or `/docs`).

## Quality bar per tool

- Works instantly, no load spinner, no dependencies beyond a single CSS/JS file.
- Sensible defaults prefilled so the first impression is a working result.
- Explains its own math in a collapsible "How this is calculated" section — this
  builds trust and is what makes people share it.
- Looks intentionally designed, not templated. (In Claude Code, consult the
  frontend-design skill if available.)

## Ethics & guardrails

- When the human posts tools to communities, instructions must be transparent
  about being the maker ("I built this free tool") — no astroturfing, no fake
  accounts, respect each community's self-promotion rules.
- No tracking beyond privacy-respecting page analytics if the human opts in.
- If a monetization step ever conflicts with usefulness or honesty, usefulness
  and honesty win.

## Anti-drift discipline

Autonomous projects fail by busywork, not laziness. Therefore:

- **Every 5 sessions, run a drift check:** re-read the roadmap and ask whether
  recent work actually served "useful tools + distribution." Log the answer
  honestly, including "we drifted" if true, and correct course.
- **Prefer finishing over starting.** Never have more than one unshipped tool in
  progress. Polish and distribution of an existing tool beat starting tool n+1.
- **Distribution is not optional.** If two consecutive sessions produced code but
  no distribution progress (posts drafted, communities researched, feedback
  gathered), the next session must prioritize distribution.
- **Recognize sunk costs.** If real-world feedback says a tool or the niche isn't
  landing after a fair test (Phase 1 complete + 3–4 genuine distribution
  attempts), say so in the ledger and pivot to the backup rather than polishing
  in the dark.

## What "success" means for the experiment

Logged in order of priority:
1. A live site with genuinely useful tools (shipped > perfect).
2. Evidence real people use and share them (traffic, comments, backlinks).
3. Learnings honestly recorded — including failures — in the ledger.
4. Only then: revenue experiments.
