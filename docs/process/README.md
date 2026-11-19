# Development process

Status: Draft

These docs describe how each feature is delivered. "The owner" makes decisions for the project. "The agent" is
the AI assistant that drafts the documents and carries out the work.

## The cycle

Each feature gets a numbered folder under `docs/specs/` and goes through five stages in order.

1. **Spec.** What we are building and why. Produces `spec.md`. See [spec.md](spec.md).
2. **Plan.** How we will build it. Produces `plan.md`. See [plan.md](plan.md).
3. **Tasks.** The order of the work. Produces `tasks.md`. See [build.md](build.md).
4. **Build.** Implement and verify one task at a time. See [build.md](build.md).
5. **Close.** Check every acceptance criterion and update the statuses. See [build.md](build.md).

## Gates

The spec, the plan and the task list each end at a gate. Nothing from the next stage starts until the owner has
approved the document.

- A document is ready for approval only when its Assumptions list is empty and its Open questions list is empty,
  or the owner has explicitly deferred each question that remains.
- The agent asks for approval only when the document is ready. The request says what is being approved and what the
  next stage will produce.
- Approval is explicit and names the document, for example "spec 001 approved". General encouragement, or
  agreement with one part of a document, is not approval.
- After an approval, the agent says which stage starts next before doing any of it.
- The overview, `docs/specs/000-overview.md`, is approved the same way, by name ("overview approved"), and is
  changed under Changing an approved document.

## Questions and assumptions

- The agent asks instead of assuming. Questions come in short rounds of at most four. Each question gives the
  options, what each one costs, and a recommendation.
- If the agent does decide something without asking, it goes in the document's Assumptions list. The owner answers
  each item with a yes or a change, and the item then moves into the body of the document.
- A question that cannot be answered yet goes in Open questions. Only the owner can defer one. A deferred question
  records a provisional answer, and every statement that depends on it is marked provisional.

## Review notes

- The owner can leave a note anywhere in a document inside triple square brackets, `[[[like this]]]`.
- The agent acts on every note, removes the brackets, and reports what changed for each one.

## Changing an approved document

- If a later stage shows that an approved document is wrong or unclear, that document is changed first and the
  owner approves the change. Then the work continues.
- Acceptance criteria keep their numbers once a spec is approved. New ones are added at the end. A removed one
  keeps its number and is marked withdrawn.

## Starting a session

- The documents are the record. The agent works out where a feature stands from its documents: the `Status:`
  lines, Assumptions, Open questions, review notes and the checkboxes in `tasks.md`. It does not rely on earlier
  chats or its own memory. An approval recorded in a `Status:` line holds in every later session.
- Before any work, the agent says which feature and stage it is in and what the next step is.
- A request for read-only work, such as a walkthrough or an audit, changes nothing. The agent does not edit files,
  act on review notes, ask for approval or move a feature to its next stage.

## Agent instructions

These docs apply to every agent. Agent-specific files such as `CLAUDE.md` and `AGENTS.md` only add guidance about
that agent's tools and never override these docs. If they disagree, these docs win and the agent-specific file is
corrected.

## Conventions

- Every document has a `Status:` line under its title: Draft, Ready for approval, Approved or Implemented. Ready for
  approval means the document meets its stage's readiness criteria and the agent has asked for approval.
- A document's `Status:` line is the only record of its status. No other file repeats it, including the spec index
  in the overview. A spec that has no folder yet has not been started.
- Prose is wrapped at 120 columns. Tables are exempt.
- Scope limits apply to project deliverables. Verification can use supporting fixtures and tools.
- The agent does not commit to git unless the owner asks. The owner commits whenever they like.
