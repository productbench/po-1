# execution/

What you're shipping - PRDs, specs, and release documentation for features in flight.

## What belongs here

The detailed "how" documents. Execution takes strategy and turns it into shippable work. This is where PRDs live, specs get refined, and shipped features are documented.

## Suggested structure

```
execution/
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
execution/
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
execution/
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
execution/
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

## From execution to product

When a feature ships and stabilizes, update `/product` to reflect the new reality. The PRD described what you planned to build; `/product` describes what you actually built.

## Keeping it current

Active folder should only contain work that's actually in progress. If something stalls for months, move it to `/workbench/ideas` or archive it with a note explaining why it paused.

## Related folders

- `/strategy/current/` — Goals and roadmap that execution implements
- `/product/` — Update here when shipped features become stable
- `/discovery/` — Research that informed the PRD
- `/operations/processes/` — How PRDs get reviewed and approved
- `/workbench/drafts/` — PRDs still being written
- `/archive/execution/` — Shipped work older than 6 months
