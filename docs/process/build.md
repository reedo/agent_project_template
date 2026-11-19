# Tasks, building and closing

## Tasks

`tasks.md` lives beside the spec and the plan. It is an ordered checklist that turns the plan into steps.

- Each task is small enough to finish and check in one sitting.
- Each task names the acceptance criteria it satisfies.
- Each task leaves the project passing its applicable verification checks.
- Every acceptance criterion appears in at least one task.

The task list is a gate like the others. The owner approves it before implementation begins.

## Building

The agent does one task at a time.

1. Define the checks for the task's acceptance criteria and identify the criterion each check covers. Write automated
   tests when applicable and see them fail before implementation. For manual checks, record repeatable steps and the
   expected result. Run them against the baseline when the result can be observed there.
2. Implement the task.
3. Run the task's checks and the applicable project checks documented in the [overview](../specs/000-overview.md)
   and the feature plan. Complete all required checks before ticking the task.
4. Record which checks passed in `tasks.md` and tick the task.
5. Stop and report what was built, which acceptance criteria now pass, and anything unexpected. The owner then
   asks for the next task, or for several to be done in one go.

If a task cannot be done as written, or shows that the spec or the plan is wrong, the agent stops. The document is
changed first and approved, and then the work continues.

## Closing

A feature is finished when all of these are true.

- Every task is ticked.
- Every acceptance criterion has at least one passing check with a result recorded against that criterion.
- The spec's status is Implemented.
- Anything the cycle taught us about the process has been written into these docs.
