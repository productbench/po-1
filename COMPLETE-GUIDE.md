# PO-1 Complete Guide
## The Complete Product Repository Structure

---

# Welcome to PO-1
## What is PO-1?

PO-1 is a product repository—a structure for product people to organize content. It's designed for use within an AI-powered code editor.

# What does the structure look like?

├── .ai/          → Skills and instructions for your AI
├── product/      → What you're building (current state)
├── research/     → What you're learning (discovery, insights)
├── strategy/     → Where you're going (vision, goals, roadmap)
├── ship/         → What you're shipping (PRDs, specs, releases)
├── team/         → How you work (processes, decisions)
├── workbench/    → Temporary workspace (ideas, experiments, all work in progress)
└── archive/      → Long-term storage for completed work

Each subfolder has its own readme.md for further information.

## Core Principles

**Keep it current.** This isn't documentation for its own sake—it's context for AI assistants. Outdated information actively hurts the quality of AI responses.

**Archive, don't delete.** When work is done, move it to the archive. Historical context is valuable for understanding why decisions were made.

**Minimal viable context.** Start small. Add documents when you find yourself repeatedly explaining the same context to AI assistants or you foresee repetitive use.

**Flexible, with orientation.** Add subfolders to suit your needs for structure.

## Using with AI Assistants

Claude Code / Cursor: Point the assistant to llms.txt at the start of a session, or reference specific folders when asking questions.

Example prompts:

"Read /product/overview.md and help me think through this feature"
"Based on our roadmap in /strategy/current/roadmap.md, prioritize these requests"
"Review our recent retros in /team/meetings/recent/retros and identify patterns"

## Getting Started

* Clone the project or download the repository via git:

>   $ git clone https://github.com/productbench/po-1.git

* Copy documents into the respective folders.
* Open the folder in your preferred IDE.

---

# product/

What you're building - the current state of your product. This is your single source of truth.

## What belongs here

Living documentation that describes the product *as it exists today*. When someone asks "what does this product do?" - point them here.

## Suggested structure

```
product/
├── overview.md           → The one-pager: what it is, who it's for, why it matters
├── architecture/         → How the system is built
├── features/             → Current feature documentation
├── metrics/              → KPIs, dashboards, success criteria
├── users/                → User segments, personas, jobs-to-be-done
└── integrations/         → Third-party connections and dependencies
```

## Example files

| File | Purpose |
|------|---------|
| `overview.md` | Product summary, value prop, key differentiators |
| `architecture/system-diagram.md` | High-level technical architecture |
| `architecture/data-model.md` | Core entities and relationships |
| `features/feature-catalog.md` | Index of current capabilities |
| `features/authentication.md` | How auth works today |
| `metrics/north-star.md` | Primary success metric and why |
| `metrics/dashboards.md` | Links to live dashboards with context |
| `users/personas.md` | Current user personas |
| `users/segments.md` | How you segment your user base |
| `users/jtbd.md` | Jobs-to-be-done framework |
| `integrations/api-partners.md` | External API dependencies |

## Tips

- **overview.md is essential.** This is often the first file an AI assistant should read. Keep it tight - one page max.
- **Update or archive.** If a feature changes significantly, update the doc. If it's removed, move to archive.
- **Link to live sources.** For metrics, link to dashboards rather than copying numbers that go stale.
- **Distinguish current from planned.** This folder is about *what is*, not *what will be*. Plans go in `/strategy` or `/ship`.

## Keeping it current

Review this folder monthly. Ask yourself: "If an AI read only this folder, would it understand our product correctly?"

## Related folders

- `/.ai/` — Point AI here to understand how to help you
- `/strategy/current/` — Where the product is headed (vision, goals)
- `/ship/shipped/` — Recently shipped features that should be reflected here
- `/research/ongoing/` — Research informing product direction

---

# research/

What you're learning - research, insights, and evidence that inform product decisions.

## What belongs here

Research findings, user interviews, competitive analysis, and market insights. This is where learning lives before it becomes strategy or ship.

## Suggested structure

```
research/
├── ongoing/              → Evergreen research you continuously update
├── projects/             → Active, time-bound research initiatives
└── archive/              → Completed research (move here when done)
```

## Example files

| File | Purpose |
|------|---------|
| `ongoing/competitive-landscape.md` | Living doc tracking competitors |
| `ongoing/user-feedback-themes.md` | Patterns from support, reviews, interviews |
| `ongoing/market-trends.md` | Industry developments worth watching |
| `projects/2024-q4-churn-study/` | Folder for a specific research project |
| `projects/mobile-app-research/research-plan.md` | Scope and methodology |
| `projects/mobile-app-research/findings.md` | What you learned |
| `projects/mobile-app-research/recommendations.md` | What to do about it |
| `archive/2024-pricing-research/` | Completed research, preserved for reference |

## Folder alternatives

Depending on your style, you might prefer:

```
research/
├── users/                → User research (interviews, surveys, usability)
├── market/               → Market and competitive research
├── data/                 → Quantitative analysis and experiments
└── archive/
```

Or organize by method:

```
research/
├── interviews/           → User interview notes and synthesis
├── surveys/              → Survey results and analysis
├── analytics/            → Data deep-dives
├── competitive/          → Competitor analysis
└── archive/
```

## Tips

- **Separate raw data from synthesis.** Keep interview notes, but also write up the "so what."
- **Date your snapshots.** Competitive analysis from 6 months ago has different weight than last week's.
- **Link to sources.** Reference the Figma prototype tested, the survey tool used, the dashboard queried.
- **Move to archive promptly.** When a research project concludes, archive it. The `/ongoing` folder is for truly continuous work.

## From research to action

Research should flow somewhere. When findings inform a decision, reference them in `/strategy` or `/ship` docs: "Based on churn research (see /research/archive/2024-q4-churn-study), we're prioritizing..."

## Related folders

- `/strategy/` — Where research insights become strategic direction
- `/ship/` — Where validated ideas become PRDs and specs
- `/product/users/` — Stable user documentation (personas, segments)
- `/workbench/` — Early research ideas before they have a formal plan
- `/archive/research/` — Completed research for historical reference

---

# strategy/

Where you're going - vision, goals, and roadmap that guide product decisions.

## What belongs here

The "why" and "where" documents. Strategy provides direction; ship provides the details of getting there.

## Suggested structure

```
strategy/
├── current/              → Active strategy documents
├── planning/             → Strategy work-in-progress (next quarter, next year)
└── archive/              → Historical strategies and goals
```

## Example files

| File | Purpose |
|------|---------|
| `current/vision.md` | Long-term product vision (1-3 years) |
| `current/goals-okrs.md` | Current quarter/year objectives |
| `current/roadmap.md` | What's planned and roughly when |
| `current/bets.md` | Strategic bets you're making and why |
| `current/principles.md` | Product principles guiding decisions |
| `planning/2025-strategy-draft.md` | Next year's strategy in development |
| `planning/q2-okr-candidates.md` | Goals being considered |
| `archive/2024-q4-okrs.md` | Last quarter's goals (with outcomes) |
| `archive/2024-roadmap.md` | Last year's roadmap |
| `archive/2023-vision.md` | Previous vision doc |

## Folder alternatives

For complex products or portfolios:

```
strategy/
├── company/              → Company-level strategy you operate within
├── product/              → Your product strategy
│   ├── vision.md
│   ├── roadmap.md
│   └── goals/
├── themes/               → Strategic themes or initiatives
└── archive/
```

Or time-oriented:

```
strategy/
├── long-term/            → Vision, north star, multi-year bets
├── annual/               → Yearly goals and roadmap
├── quarterly/            → Current quarter OKRs
└── archive/
```

## Tips

- **vision.md should be stable.** If you're rewriting it every quarter, it's not a vision.
- **Roadmap ≠ commitment.** Be clear about confidence levels. "Now / Next / Later" often works better than specific dates.
- **Goals need outcomes.** When archiving OKRs, note what actually happened. Did you hit them? What did you learn?
- **Link to research.** Strategy should reference the research that informed it: "Based on churn research (see /research/archive/2024-q4-churn-study), we're prioritizing retention."

## Strategy vs. ship

| Strategy | Ship |
|----------|------|
| *What* we're trying to achieve | *How* we'll achieve it |
| Goals and success metrics | PRDs and specs |
| Roadmap themes | Specific features |
| "Improve retention by 20%" | "Build re-engagement email flow" |

## Keeping it current

- **Vision:** Review annually. Update only when direction fundamentally changes.
- **Goals/OKRs:** Update quarterly. Archive previous quarter with outcomes.
- **Roadmap:** Review monthly. Move completed items, adjust timelines, add new items.
- **Planning:** Clean out after decisions are made—drafts become current docs or get discarded.

## Related folders

- `/research/` — Research that informs strategy decisions
- `/ship/` — Where strategy becomes shippable work
- `/product/` — Current state strategy aims to improve
- `/team/decisions/` — ADRs and RFCs that implement strategic choices
- `/archive/strategy/` — Historical goals and roadmaps

---

# ship/

What you're shipping - PRDs, specs, and release documentation for features in flight.

## What belongs here

The detailed "how" documents. Ship takes strategy and turns it into shippable work. This is where PRDs live, specs get refined, and shipped features are documented.

## Suggested structure

```
ship/
├── active/               → Work currently in progress
├── shipped/              → Recently released (last ~6 months)
└── archive/              → Older completed work
```

## Example files

| File | Purpose |
|------|---------|
| `active/prds/search-redesign.md` | PRD for feature in development |
| `active/specs/search-api-spec.md` | Technical specification |
| `active/user-stories/search-stories.md` | Detailed user stories |
| `shipped/release-notes/2024-11-release.md` | What went out and when |
| `shipped/search-redesign/` | Completed PRD + learnings |
| `archive/2024/onboarding-v2/` | Older shipped work |

## Folder alternatives

Organize by artifact type:

```
ship/
├── prds/
│   ├── active/
│   └── shipped/
├── specs/
│   ├── active/
│   └── shipped/
├── user-stories/
└── release-notes/
```

Or by initiative/epic:

```
ship/
├── active/
│   ├── search-redesign/
│   │   ├── prd.md
│   │   ├── spec.md
│   │   └── stories.md
│   └── mobile-notifications/
├── shipped/
└── archive/
```

Or by team/squad:

```
ship/
├── platform/
│   ├── active/
│   └── shipped/
├── growth/
│   ├── active/
│   └── shipped/
└── archive/
```

## Tips

- **PRDs should reference strategy.** "This supports Q4 goal X (see /strategy/current/goals-okrs.md)" keeps work connected to purpose.
- **Update status, don't duplicate.** One PRD per feature. Update its status rather than creating "PRD-v2."
- **Ship → Shipped → Archive.** Move docs to `/shipped` when released. After 6 months, move to `/archive`.
- **Capture learnings.** Before archiving, add a "Retrospective" or "Learnings" section. What worked? What didn't?

## From ship to product

When a feature ships and stabilizes, update `/product` to reflect the new reality. The PRD described what you planned to build; `/product` describes what you actually built.

## Keeping it current

Active folder should only contain work that's actually in progress. If something stalls for months, move it to `/workbench/ideas` or archive it with a note explaining why it paused.

## Related folders

- `/strategy/current/` — Goals and roadmap that ship implements
- `/product/` — Update here when shipped features become stable
- `/research/` — Research that informed the PRD
- `/team/processes/` — How PRDs get reviewed and approved
- `/workbench/drafts/` — PRDs still being written
- `/archive/ship/` — Shipped work older than 6 months

---

# team/

How you work - team structure, processes, meetings, and decisions.

## What belongs here

The "operating system" of your product team. How decisions get made, how meetings run, who does what, and the processes that keep things moving.

## Suggested structure

```
team/
├── about/                → Stable team documentation
├── processes/            → How you do things
├── meetings/             → Meeting notes and agendas
│   ├── recent/           → Last 2-3 months (active reference)
│   └── archive/          → Older notes
└── decisions/            → Decision records (ADRs, RFCs)
```

## Example files

| File | Purpose |
|------|---------|
| `about/team-charter.md` | Team mission, scope, and working agreements |
| `about/role-definitions.md` | Who does what (PM, Design, Eng, etc.) |
| `about/stakeholders.md` | Key stakeholders and how to work with them |
| `processes/sprint-workflow.md` | How sprints run |
| `processes/prd-process.md` | How PRDs get written and approved |
| `processes/on-call-rotation.md` | Support and incident handling |
| `meetings/recent/retros/2024-11-sprint-retro.md` | Recent retrospective |
| `meetings/recent/sprint-planning/2024-w48.md` | This week's planning |
| `decisions/adr-001-api-versioning.md` | Architecture decision record |
| `decisions/rfc-pricing-model.md` | Request for comments |

## Folder alternatives

Flatten if you have fewer docs:

```
team/
├── charter.md
├── processes.md
├── decisions/
└── meetings/
```

Or expand for larger teams:

```
team/
├── about/
│   ├── charter.md
│   ├── roles/
│   │   ├── product-manager.md
│   │   └── tech-lead.md
│   ├── onboarding/
│   └── stakeholders/
├── processes/
│   ├── planning/
│   ├── shipping/
│   └── support/
├── meetings/
│   ├── recent/
│   │   ├── standups/
│   │   ├── sprint-planning/
│   │   ├── retros/
│   │   ├── stakeholder-reviews/
│   │   └── 1-on-1s/
│   └── archive/
├── decisions/
│   ├── adrs/              → Architecture Decision Records
│   └── rfcs/              → Requests for Comments
└── incidents/             → Postmortems and incident reports
```

## Tips

- **Keep meeting notes lightweight.** Date, attendees, decisions, action items. AI can help synthesize patterns across retros without exhaustive notes.
- **Archive aggressively.** Meeting notes older than 2-3 months rarely get referenced. Move them to `/meetings/archive` monthly.
- **Decisions are permanent.** Unlike meeting notes, ADRs and RFCs stay in `/decisions` (not archived) because understanding *why* something was decided remains valuable.
- **Processes should be prescriptive.** Write them so a new team member could follow them. If you find yourself constantly explaining "how we actually do it," update the doc.

## Decision record format

A simple ADR template:

```markdown
# ADR-001: [Title]

## Status
Accepted | Proposed | Deprecated | Superseded by ADR-XXX

## Context
What's the situation? What forces are at play?

## Decision
What did we decide?

## Consequences
What are the implications? Trade-offs accepted?
```

## From team to action

Reference process docs in other folders: "For PRD approval process, see /team/processes/prd-process.md" keeps things DRY and up to date.

## Related folders

- `/ship/` — Where processes like PRD review get applied
- `/strategy/` — Goals that shape team priorities and processes
- `/.ai/` — AI instructions might reference team context and terminology
- `/archive/team/` — Old meeting notes and deprecated processes

---

# workbench/

Temporary workspace - ideas, experiments, and work in progress that hasn't found its home yet.

## What belongs here

Anything that's not ready for prime time. Half-formed ideas, early drafts, experiments, research-in-progress, and things you're still figuring out. This is your scratch space.

## Suggested structure

```
workbench/
├── ideas/                → Concepts worth capturing but not yet validated
├── experiments/          → Tests you're running
└── drafts/               → Documents in progress
```

## Example files

| File | Purpose |
|------|---------|
| `ideas/ai-feature-brainstorm.md` | Raw ideas from a brainstorm |
| `ideas/pricing-thoughts.md` | Early thinking on pricing changes |
| `ideas/competitors-to-watch.md` | Companies you've noticed |
| `experiments/onboarding-test-plan.md` | Experiment you're designing |
| `experiments/feature-flag-results.md` | Data from a test in progress |
| `drafts/q1-roadmap-draft.md` | Roadmap you're still refining |
| `drafts/new-prd-wip.md` | PRD that's not ready for /ship |

## Folder alternatives

Keep it minimal:

```
workbench/
├── wip/                  → Everything in progress
└── ideas/                → Everything speculative
```

Or more structured:

```
workbench/
├── ideas/
│   ├── features/         → Feature ideas
│   ├── improvements/     → Small enhancements
│   └── moonshots/        → Big, speculative bets
├── experiments/
│   ├── active/           → Currently running
│   └── results/          → Completed, awaiting decision
├── drafts/
├── research/             → Research work not yet organized
└── resources/            → Useful references, templates, inspirations
```

## Tips

- **This folder should be messy.** That's the point. Don't over-organize it.
- **Date or delete.** If something sits here for months untouched, either delete it or move it to archive with a note.
- **Graduate your work.** When an idea becomes real, move it: ideas → research (for research) or ship (for building). When a draft is done, move it to its proper folder.
- **Don't let it grow forever.** Review monthly. Ask: "Is this still relevant? Should it move somewhere? Should it be deleted?"

## The graduation path

```
workbench/ideas/feature-x.md
    ↓ (idea validated)
research/projects/feature-x-research/
    ↓ (research complete, decision to build)
ship/active/prds/feature-x.md
    ↓ (shipped)
ship/shipped/feature-x/
    ↓ (6+ months later)
archive/ship/feature-x/
```

## When to use workbench vs. other folders

| If it's... | Put it in... |
|------------|--------------|
| A half-formed idea | `workbench/ideas/` |
| Active research with a plan | `research/projects/` |
| A draft PRD you're writing | `workbench/drafts/` |
| A PRD ready for review | `ship/active/prds/` |
| Something you're experimenting with | `workbench/experiments/` |
| A validated experiment informing strategy | `research/` then reference in `strategy/` |

## Related folders

- `/research/projects/` — Where ideas graduate when research begins
- `/ship/active/` — Where drafts graduate when ready for development
- `/strategy/planning/` — Strategy drafts in development
- `/archive/` — Where abandoned experiments and ideas can be preserved

---

# archive/

Long-term storage for completed work.

## What belongs here

Documents that are no longer active but worth preserving. Historical context helps explain *why* decisions were made and prevents repeating past mistakes.

## Suggested structure

```
archive/
├── research/             → Completed research
├── strategy/             → Past strategies and goals
├── ship/                 → Shipped features (6+ months old)
└── team/                 → Old meeting notes, deprecated processes
```

## Example files

| File | Purpose |
|------|---------|
| `research/2024-pricing-research/` | Pricing research from last year |
| `strategy/2024-okrs.md` | Last year's goals and outcomes |
| `strategy/2023-vision.md` | Previous vision doc |
| `ship/2024/onboarding-v2/` | Feature shipped and stable |
| `team/meetings/2024-q3/` | Meeting notes from Q3 |
| `team/deprecated-processes/` | Old ways of working |

## Folder alternatives

Organize by year:

```
archive/
├── 2024/
│   ├── research/
│   ├── strategy/
│   ├── ship/
│   └── team/
├── 2023/
└── 2022/
```

Or keep it flat:

```
archive/
├── 2024-q4-okrs.md
├── 2024-pricing-research/
├── 2024-onboarding-v2/
└── ...
```

## Tips

- **Add context when archiving.** Before you move something, add a brief note: "Archived 2024-12: Shipped, see /product for current state" or "Archived 2024-12: Deprioritized, revisit Q2 2025."
- **Preserve the structure.** When moving from `/research/projects/research-x/` to archive, keep the folder structure intact: `/archive/research/research-x/`.
- **Include outcomes.** For completed work, note what happened: Did the feature succeed? Did the strategy pay off? What did you learn?
- **Don't over-organize.** The archive is for reference, not active work. A simple year-based or folder-mirrored structure is usually enough.

## When to archive

| Folder | Archive when... |
|--------|-----------------|
| `research/` | Research project is complete and synthesized |
| `strategy/` | Quarter/year ends, new goals replace old |
| `ship/` | Feature shipped 6+ months ago, stable |
| `team/meetings/` | Notes are 2-3+ months old |
| `team/processes/` | Process is deprecated or significantly changed |
| `workbench/` | Idea abandoned, experiment concluded, draft completed or scrapped |

## Archive vs. delete

**Archive** when:
- The work was completed and might be referenced
- Understanding historical context could help future decisions
- You might revisit the idea later
- Compliance or legal requires retention

**Delete** when:
- The document was never finished and won't be
- It's a duplicate or outdated version
- It contains no unique information
- It's been superseded and adds no historical value

When in doubt, archive. Storage is cheap; lost context is expensive.

## Related folders

Content flows *into* archive from all active folders:

- `/research/archive/` → `/archive/research/` (after ~1 year)
- `/strategy/archive/` → `/archive/strategy/` (historical goals and roadmaps)
- `/ship/shipped/` → `/archive/ship/` (after ~6 months)
- `/team/meetings/archive/` → `/archive/team/` (older notes)
- `/workbench/` → `/archive/` (abandoned ideas worth preserving)

---

## Quick Reference: Content Flow

```
workbench/ideas/
    ↓
research/projects/
    ↓
strategy/current/ ← (informs) → ship/active/
    ↓                               ↓
strategy/archive/              ship/shipped/
    ↓                               ↓
archive/strategy/              product/ (update)
                                    ↓
                               ship/archive/
                                    ↓
                               archive/ship/
```

## Folder Decision Tree

**Where should I put this document?**

1. Is it about *what exists today*? → `/product/`
2. Is it research or learning? → `/research/`
3. Is it strategic direction? → `/strategy/`
4. Is it a PRD or spec? → `/ship/`
5. Is it about how the team works? → `/team/`
6. Is it half-baked or in progress? → `/workbench/`
7. Is it completed and historical? → `/archive/`
