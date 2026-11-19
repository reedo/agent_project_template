Use the project overview for the repository layout, constraints and verification steps.

## Start a session

1. Read the [development process](docs/process/README.md) and the [project overview](docs/specs/000-overview.md).
   The process defines how features are approved. The overview gives the project constraints and indexes the specs.
2. For feature work, follow the index to the feature the owner asked about. Read its `spec.md` and any sibling
   `plan.md` and `tasks.md`. Check their status lines, assumptions, open questions, `[[[review notes]]]` and task
   checkboxes. Use these records to resume the requested work.
3. Read the guide for the current stage below. A request to review a draft stays in that stage. Planning requires
   an approved spec, task breakdown requires an approved plan, and implementation requires an approved task list.

## Choose the stage guide

- **Spec** — Use [Writing a spec](docs/process/spec.md). For a new feature, restate the brief in one paragraph
  and get the owner's confirmation before the interview. For an existing draft, resume review in its feature folder.
- **Plan** — Use [Writing a plan](docs/process/plan.md). Write `plan.md` beside the spec. Discuss interface choices,
  new dependencies and trade-offs with the owner. Confine experiments to `.scratch/` and clean them up by the end of
  plan review.
- **Tasks, build and close** — Use [Tasks, building and closing](docs/process/build.md). Map every acceptance
  criterion to a task in `tasks.md`. During build, work one task at a time. Define the checks for its criteria, run
  them against the baseline where applicable, then implement and run the project's verification steps. Once clean,
  tick the task and report what was built, which criteria pass and anything unexpected. Stop unless the owner
  requested a batch. At close, verify all tasks and criteria, mark the spec Implemented and record any process lessons.

## Review and approval

- Ask in rounds of at most four questions, with options, costs and a recommendation. Record decisions made without
  asking under Assumptions. Move each answer into the document when the owner confirms or corrects it.
- Address every `[[[review note]]]`, remove its brackets and report what changed for each note.
- Check the stage guide's readiness criteria before requesting approval. Resolve every assumption and open question
  unless the owner explicitly defers a question. For each deferral, record a provisional answer and mark every
  dependent statement provisional.
- Name the document being approved and what the next stage will produce. Approval must explicitly identify the
  document (for example, “spec 001 approved”). Record its Approved status and announce the next stage and its
  deliverable before starting it.
- If a task cannot be completed as written or an approved document needs correction, stop and get the amended
  document approved before resuming. Keep approved acceptance criterion numbers stable. Append additions and mark
  removals withdrawn.
- Put a `Status:` line beneath each document title and wrap prose at 120 columns. Commit only when the owner asks.
