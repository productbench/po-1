# archive/

Long-term storage for completed work.

## What belongs here

Documents that are no longer active but worth preserving. Historical context helps explain *why* decisions were made and prevents repeating past mistakes.

## Suggested structure

```
archive/
├── discovery/            → Completed research
├── strategy/             → Past strategies and goals
├── execution/            → Shipped features (6+ months old)
└── operations/           → Old meeting notes, deprecated processes
```

## Example files

| File | Purpose |
|------|---------|
| `discovery/2024-pricing-research/` | Pricing research from last year |
| `strategy/2024-okrs.md` | Last year's goals and outcomes |
| `strategy/2023-vision.md` | Previous vision doc |
| `execution/2024/onboarding-v2/` | Feature shipped and stable |
| `operations/meetings/2024-q3/` | Meeting notes from Q3 |
| `operations/deprecated-processes/` | Old ways of working |

## Folder alternatives

Organize by year:

```
archive/
├── 2024/
│   ├── discovery/
│   ├── strategy/
│   ├── execution/
│   └── operations/
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
- **Preserve the structure.** When moving from `/discovery/projects/research-x/` to archive, keep the folder structure intact: `/archive/discovery/research-x/`.
- **Include outcomes.** For completed work, note what happened: Did the feature succeed? Did the strategy pay off? What did you learn?
- **Don't over-organize.** The archive is for reference, not active work. A simple year-based or folder-mirrored structure is usually enough.

## When to archive

| Folder | Archive when... |
|--------|-----------------|
| `discovery/` | Research project is complete and synthesized |
| `strategy/` | Quarter/year ends, new goals replace old |
| `execution/` | Feature shipped 6+ months ago, stable |
| `operations/meetings/` | Notes are 2-3+ months old |
| `operations/processes/` | Process is deprecated or significantly changed |
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

- `/discovery/archive/` → `/archive/discovery/` (after ~1 year)
- `/strategy/archive/` → `/archive/strategy/` (historical goals and roadmaps)
- `/execution/shipped/` → `/archive/execution/` (after ~6 months)
- `/operations/meetings/archive/` → `/archive/operations/` (older notes)
- `/workbench/` → `/archive/` (abandoned ideas worth preserving)
