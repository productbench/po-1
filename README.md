# Welcome to PO-1
## What is PO-1?

PO-1 is a product repository—a structure for product people to organize content. It's designed for use within an AI-powered code editor.

# What does the structure look like?

├── .ai/          → Skills and instructions for your AI
├── product/      → What you're building (current state)
├── discovery/    → What you're learning (research)
├── strategy/     → Where you're going (vision, goals, roadmap)
├── execution/    → What you're shipping (PRDs, specs, releases)
├── operations/   → How you work (team, processes, decisions)
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
"Review our recent retros in /operations/meetings/recent/retros and identify patterns"

## Getting Started

* Clone the project or download the repository via git:

>   $ git clone https://github.com/productbench/po-1.git

* Copy documents into the respective folders.
* Open the folder in your preferred IDE.