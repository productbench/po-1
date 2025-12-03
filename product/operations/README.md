# operations/

How you work - team structure, processes, meetings, and decisions.

## What belongs here

The "operating system" of your product team. How decisions get made, how meetings run, who does what, and the processes that keep things moving.

## Suggested structure

```
operations/
├── team/                 → Stable team documentation
├── processes/            → How you do things
├── meetings/             → Meeting notes and agendas
│   ├── recent/           → Last 2-3 months (active reference)
│   └── archive/          → Older notes
└── decisions/            → Decision records (ADRs, RFCs)
```

## Example files

| File | Purpose |
|------|---------|
| `team/team-charter.md` | Team mission, scope, and working agreements |
| `team/role-definitions.md` | Who does what (PM, Design, Eng, etc.) |
| `team/stakeholders.md` | Key stakeholders and how to work with them |
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
operations/
├── team-charter.md
├── processes.md
├── decisions/
└── meetings/
```

Or expand for larger teams:

```
operations/
├── team/
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

## From operations to action

Reference process docs in other folders: "For PRD approval process, see /operations/processes/prd-process.md" keeps things DRY and up to date.

## Related folders

- `/execution/` — Where processes like PRD review get applied
- `/strategy/` — Goals that shape team priorities and processes
- `/.ai/` — AI instructions might reference team context and terminology
- `/archive/operations/` — Old meeting notes and deprecated processes
