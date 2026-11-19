# Writing a spec

A spec describes what the feature does and why in terms its intended users would recognise. Describe observable
behaviour and outcomes, and capture implementation decisions in the plan. The spec lives in
`docs/specs/NNN-short-name/spec.md`.

## Steps

1. **Brief.** The owner describes the feature in a few sentences. The agent restates it in one paragraph, and the
   owner confirms or corrects that paragraph.
2. **Interview.** The agent asks questions in rounds until it could write every section below without guessing. The
   interview covers at least: who will use the feature and for what, the smallest slice that is useful on its own,
   what is deliberately left out, what happens in normal use, what happens when something goes wrong, and the edge
   cases and limits.
3. **Draft.** The agent writes the spec. Anything it still had to guess goes under Assumptions.
4. **Review.** The owner reads the draft, answers the assumptions and open questions, and leaves notes. The agent
   revises. This repeats until both lists are empty.
5. **Gate.** The agent asks for approval. The owner approves, and the status changes to Approved.

## Sections

In this order. A section is left out only if it would be empty.

- **Summary.** Two or three sentences.
- **Why.** The reason this slice exists and why it is this size.
- **Terms.** Every word the spec uses in a special sense.
- **Behaviour.** What the feature does, as plain statements grouped by topic.
- **Invariants.** Things that are always true.
- **Non-goals.** Everything deliberately left out.
- **Acceptance criteria.** Numbered `AC-1`, `AC-2` and so on. Each is written as given, when, then, with concrete
  values. Each one breaks at most one rule, so the outcome never depends on the order rules are checked in.
- **Assumptions.** Decisions the agent made without asking.
- **Open questions.** Questions that cannot be answered yet.

## Ready for approval when

- Every statement under Behaviour is covered by at least one acceptance criterion.
- Every acceptance criterion can be verified with a repeatable check.
- Non-goals names everything a reader might otherwise expect to find.
- Assumptions is empty.
- Open questions is empty, or the owner has deferred each one that remains.
- The spec is as small as it can be and still be useful on its own.
