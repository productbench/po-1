# discovery/

What you're learning - research, insights, and evidence that inform product decisions.

## What belongs here

Research findings, user interviews, competitive analysis, and market insights. This is where learning lives before it becomes strategy or execution.

## Suggested structure

```
discovery/
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
| `projects/mobile-app-discovery/research-plan.md` | Scope and methodology |
| `projects/mobile-app-discovery/findings.md` | What you learned |
| `projects/mobile-app-discovery/recommendations.md` | What to do about it |
| `archive/2024-pricing-research/` | Completed research, preserved for reference |

## Folder alternatives

Depending on your style, you might prefer:

```
discovery/
├── users/                → User research (interviews, surveys, usability)
├── market/               → Market and competitive research
├── data/                 → Quantitative analysis and experiments
└── archive/
```

Or organize by method:

```
discovery/
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

## From discovery to action

Research should flow somewhere. When findings inform a decision, reference them in `/strategy` or `/execution` docs: "Based on churn research (see /discovery/archive/2024-q4-churn-study), we're prioritizing..."

## Related folders

- `/strategy/` — Where research insights become strategic direction
- `/execution/` — Where validated ideas become PRDs and specs
- `/product/users/` — Stable user documentation (personas, segments)
- `/workbench/` — Early research ideas before they have a formal plan
- `/archive/discovery/` — Completed research for historical reference
