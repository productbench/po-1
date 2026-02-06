---
name: cleanup
description: Organize and clean up files within the PO-1 product repository structure. Use when a user wants to "clean up", "organize", "tidy", or "sort" files in a specific path or the current directory. Analyzes files and suggests moves to the correct PO-1 folder (product, research, strategy, ship, team, workbench, or archive) based on content and age. Works only within the specified scope—never touches files outside the given path.
---

# PO-1 Cleanup: File Organization Assistant

Organize files into the correct PO-1 repository structure based on content analysis and the folder decision tree.

## Required Reference

**Before classifying any files, read `/COMPLETE-GUIDE.md`** for detailed examples of common product files and their correct locations. The guide contains:

- Example files for each folder (overview.md, personas.md, prd.md, etc.)
- Subfolder structures (product/features/, research/projects/, ship/active/, etc.)
- File naming patterns and conventions
- When-to-archive guidance for each folder type

Use these examples to accurately match files to their destinations.

## Core Philosophy

**Scope-limited by design.** This skill only operates on the path or file explicitly provided. It never recursively cleans the entire repository unless specifically asked.

**Suggest, don't surprise.** Always show proposed changes and get confirmation before moving anything.

**Archive, don't delete.** When in doubt, move to archive rather than deleting. Historical context is valuable.

## PO-1 Structure Reference

```
├── product/      → What you're building (current state)
├── research/     → What you're learning (discovery, insights)
├── strategy/     → Where you're going (vision, goals, roadmap)
├── ship/         → What you're shipping (PRDs, specs, releases)
├── team/         → How you work (processes, decisions)
├── workbench/    → Temporary workspace (ideas, experiments, WIP)
└── archive/      → Long-term storage for completed work
```

## Workflow

### 1. Determine Scope

When invoked, identify the target:
- If a **specific file** is provided → analyze that file only
- If a **folder path** is provided → analyze files in that folder (non-recursive by default)
- If **no path** is provided → ask "Which folder or file would you like me to help organize?"

**Never** assume the entire repository. Always confirm scope.

### 2. Analyze Files

First, **read `/COMPLETE-GUIDE.md`** to understand the full PO-1 structure and file examples.

For each file in scope, determine:

1. **Current location** - Where is it now?
2. **Content type** - What kind of document is it? (Compare against examples in COMPLETE-GUIDE.md)
3. **Age/Status** - Is it active, stale, or completed?
4. **Recommended destination** - Where should it live? (Match to folder examples in COMPLETE-GUIDE.md)

Use this decision tree:

| Content Type | Destination |
|-------------|-------------|
| Product documentation (what exists today) | `product/` |
| Research findings, interviews, analysis | `research/` |
| Vision, goals, OKRs, roadmap | `strategy/` |
| PRDs, specs, user stories | `ship/active/` or `ship/shipped/` |
| Meeting notes, processes, decisions | `team/` |
| Half-formed ideas, drafts, experiments | `workbench/` |
| Completed work 6+ months old | `archive/` |
| Old meeting notes (2-3+ months) | `archive/team/` |

### 3. Check for Staleness

Flag files that may need attention:

- **Workbench items** untouched for 30+ days → suggest archive or delete
- **Ship/active items** with no updates for 60+ days → suggest review status
- **Meeting notes** older than 90 days → suggest move to archive
- **Draft documents** never completed → suggest archive with note

### 4. Present Recommendations

Create a clear summary table:

```markdown
## Cleanup Recommendations for `[path]`

| File | Current Location | Recommended Action | Reason |
|------|-----------------|-------------------|--------|
| feature-idea.md | workbench/ | → archive/ | Untouched 45 days |
| q3-okrs.md | strategy/current/ | → strategy/archive/ | Quarter ended |
| api-spec.md | workbench/drafts/ | → ship/active/specs/ | Ready for review |

### Summary
- 3 files to move
- 1 file to archive
- 0 files to delete (suggest archive instead)
```

### 5. Get Confirmation

Before any action, ask:

> I've identified [N] files that could be reorganized. Would you like me to:
> 1. **Execute all** - Move all files as recommended
> 2. **Review each** - Confirm each move individually
> 3. **Skip** - Cancel without changes

### 6. Execute Moves

When confirmed:
1. Create destination folders if they don't exist
2. Move files to recommended locations
3. Add archive notes where appropriate (e.g., "Archived [date]: [reason]")
4. Report results

```markdown
## Cleanup Complete

✓ Moved `feature-idea.md` → `archive/workbench/feature-idea.md`
✓ Moved `q3-okrs.md` → `strategy/archive/2024-q3-okrs.md`
✓ Moved `api-spec.md` → `ship/active/specs/api-spec.md`

3 files organized.
```

## Special Cases

### Cleaning workbench/

The workbench is meant to be messy, but not forever. When cleaning workbench:
- Ideas untouched 30+ days → archive or delete
- Drafts ready for use → graduate to proper folder
- Experiments with results → move results to research, archive the rest

### Cleaning archive/

Archive cleanup is rare but valid:
- Consolidate duplicate folders
- Add missing context notes
- Organize by year if structure is flat

### Unknown file types

If a file doesn't clearly fit the PO-1 structure:
1. Ask the user what it is
2. Suggest workbench/ as temporary home
3. Note it for future organization

## Triggers

This skill activates on:
- `/cleanup` or `/clean`
- "clean up [path]"
- "organize [folder]"
- "tidy up my files"
- "sort files in [path]"
- "what files need organizing?"
- "help me declutter"

## Safety Rules

1. **Never delete without explicit permission** - Always suggest archive first
2. **Never operate outside specified scope** - If given `workbench/`, don't touch `product/`
3. **Never move without confirmation** - Always show the plan first
4. **Preserve git history** - Use `git mv` when in a git repository
5. **Create backups for bulk operations** - For 10+ files, suggest a backup first
