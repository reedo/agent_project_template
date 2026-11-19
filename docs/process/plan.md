# Writing a plan

A plan explains how to deliver an approved spec. It lives beside the spec as `plan.md`. Keep experimental work in
`.scratch/` and leave implementation for the Build stage.

## Steps

1. **Explore.** The agent works out a design and can try ideas in `.scratch/` inside the repo. Clean up the scratch
   work by the end of step 4 (Review).
2. **Interview.** The agent asks the owner about decisions that affect users or maintainers, such as interface design,
   new dependencies and trade-offs with no clear winner.
3. **Draft.** The agent writes the plan. Anything it still had to guess goes under Assumptions.
4. **Review.** As for a spec: answers, notes and revisions until both lists are empty.
5. **Gate.** The agent asks for approval. The owner approves, and the status changes to Approved.

## Sections

In this order. A section is left out only if it would be empty.

- **Overview.** The design in one paragraph.
- **Interfaces.** How users and other systems interact with the feature. Include signatures and examples where
  applicable.
- **Design.** How the feature works, including any data structures it needs.
- **Layout.** Where the implementation and deliverables go.
- **Verification.** How each acceptance criterion will be checked and what project-wide checks to run. Record any
  feature-specific commands or manual steps.
- **Dependencies.** Each one and why it is needed.
- **Trade-offs.** For each real choice: what was chosen, what the alternative was, and why.
- **Spec changes.** Anything the design showed to be wrong or unclear in the spec. The spec is changed first.
- **Assumptions.** Decisions the agent made without asking.
- **Open questions.** Questions that cannot be answered yet.

## Ready for approval when

- Every acceptance criterion has a stated way of being verified.
- Every proposed interface traces back to something in the spec.
- Nothing in the plan contradicts the spec.
- Assumptions is empty.
- Open questions is empty, or the owner has deferred each one that remains.
