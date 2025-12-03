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
| `drafts/new-prd-wip.md` | PRD that's not ready for /execution |

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
├── research/             → Discovery work not yet organized
└── resources/            → Useful references, templates, inspirations
```

## Tips

- **This folder should be messy.** That's the point. Don't over-organize it.
- **Date or delete.** If something sits here for months untouched, either delete it or move it to archive with a note.
- **Graduate your work.** When an idea becomes real, move it: ideas → discovery (for research) or execution (for building). When a draft is done, move it to its proper folder.
- **Don't let it grow forever.** Review monthly. Ask: "Is this still relevant? Should it move somewhere? Should it be deleted?"

## The graduation path

```
workbench/ideas/feature-x.md
    ↓ (idea validated)
discovery/projects/feature-x-research/
    ↓ (research complete, decision to build)
execution/active/prds/feature-x.md
    ↓ (shipped)
execution/shipped/feature-x/
    ↓ (6+ months later)
archive/execution/feature-x/
```

## When to use workbench vs. other folders

| If it's... | Put it in... |
|------------|--------------|
| A half-formed idea | `workbench/ideas/` |
| Active research with a plan | `discovery/projects/` |
| A draft PRD you're writing | `workbench/drafts/` |
| A PRD ready for review | `execution/active/prds/` |
| Something you're experimenting with | `workbench/experiments/` |
| A validated experiment informing strategy | `discovery/` then reference in `strategy/` |

## Related folders

- `/discovery/projects/` — Where ideas graduate when research begins
- `/execution/active/` — Where drafts graduate when ready for development
- `/strategy/planning/` — Strategy drafts in development
- `/archive/` — Where abandoned experiments and ideas can be preserved
