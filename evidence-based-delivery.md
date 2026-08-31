# Evidence-based delivery for AI coding work

“Done” is not useful unless the recipient can verify it. Agent work should end with a delivery packet tied to the acceptance criteria.

A compact delivery packet includes:

- **Outcome:** what changed and which requested result now holds.
- **Surface:** branch, commit, pull request, document, or public artifact containing the work.
- **Verification:** tests run, screenshots inspected, links checked, or manual flows exercised.
- **Exceptions:** known warnings, skipped checks, pending reviews, and assumptions.
- **Recovery:** how to reproduce, continue, or roll back the work safely.

Evidence should match risk. A copy edit may need a rendered-page check; an authentication change needs targeted tests and a permissions review; a public submission needs a live URL and confirmation that the backlink remains visible.

Avoid reporting attempted actions as completed outcomes. “Submitted for moderation” is different from “publicly visible,” and “the command ran” is different from “the behavior is correct.”

[Wagglet](https://wagglet.com/) structures task delivery around the outcome and supporting evidence, keeping the handoff reviewable across people and coding-agent subscriptions.
