The project overview describes the project and its tools. The process docs define the workflow shared by every
agent. This file adds guidance for Claude Code and the Claude desktop app.

## Start every session

The files below are imported, so their full text is in context in every session and after every summary. Read them
before doing any work.

The process (the stages, the gates, and the rules for questions, assumptions and review notes) and the overview (what
the project is, its constraints and the index of specs):

@docs/process/README.md
@docs/specs/000-overview.md

The stage guides. Before any work at a stage, follow its guide: the spec guide for Spec, the plan guide for Plan, and
the build guide for Tasks, Build and Close.

@docs/process/spec.md
@docs/process/plan.md
@docs/process/build.md

The rules that matter most:

- Never start a stage until the owner has explicitly approved the previous stage's document by name.
- Ask instead of assuming. Anything decided without asking goes in that document's Assumptions list for the owner
  to confirm.
- When the stage changes, say which stage is starting and what it will produce before doing any of it.
- Do not commit unless asked.

## Claude Code and the desktop app

Where a tool's default conflicts with the process, the process wins.

- **Plan mode is not the Plan stage.** The process's plan is `plan.md`, approved at its gate. Do not use plan mode or
  accepting its plan as a stand-in for that stage or its approval.
- **Scratch work goes in `.scratch/`** inside the repo. Git ignores this directory. Clean it up as the stage guide
  says.
- **The documents are the record, not memory.** Do not save statuses, approvals, decisions or spec content to auto
  memory. Memory is only for how the owner likes to work.
- **One writer at a time.** Do not split build tasks or document edits across parallel sessions or subagents. The
  process builds one task at a time and the owner reviews each. Subagents may read and search.
- **Git.** Do not commit, push, open pull requests or offer to do any of these unless the owner asks.
