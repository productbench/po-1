# strategy/

Where you're going - vision, goals, and roadmap that guide product decisions.

## What belongs here

The "why" and "where" documents. Strategy provides direction; execution provides the details of getting there.

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
- **Link to discovery.** Strategy should reference the research that informed it: "Based on churn research (see /discovery/archive/2024-q4-churn-study), we're prioritizing retention."

## Strategy vs. execution

| Strategy | Execution |
|----------|-----------|
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

- `/discovery/` — Research that informs strategy decisions
- `/execution/` — Where strategy becomes shippable work
- `/product/` — Current state strategy aims to improve
- `/operations/decisions/` — ADRs and RFCs that implement strategic choices
- `/archive/strategy/` — Historical goals and roadmaps