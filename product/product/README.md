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
- **Distinguish current from planned.** This folder is about *what is*, not *what will be*. Plans go in `/strategy` or `/execution`.

## Keeping it current

Review this folder monthly. Ask yourself: "If an AI read only this folder, would it understand our product correctly?"

## Related folders

- `/.ai/` — Point AI here to understand how to help you
- `/strategy/current/` — Where the product is headed (vision, goals)
- `/execution/shipped/` — Recently shipped features that should be reflected here
- `/discovery/ongoing/` — Research informing product direction
