# Bounded context packets for coding-agent handoffs

An agent handoff should transfer enough context to complete one task, but not an entire account history. The useful unit is a bounded context packet.

A strong packet contains:

1. **Outcome** — the observable result, written so two reviewers would agree whether it happened.
2. **Working surface** — repository, branch, relevant files, environment, and exact external systems in scope.
3. **Constraints** — behavior that must remain unchanged, security limits, style requirements, and prohibited actions.
4. **Current evidence** — failing tests, screenshots, logs, discussion decisions, and links that explain the present state.
5. **Delivery contract** — the report, tests, artifacts, or review state required at completion.

The packet should omit unrelated private conversations, reusable credentials, and broad browsing history. When access is necessary, prefer a task-scoped credential with a narrow capability and expiry.

This structure makes a handoff portable between Codex, Claude Code, and other coding agents. The recipient can work through their own subscription and local safeguards while the requester retains a reviewable specification.

[Wagglet](https://wagglet.com/) applies this boundary directly: teammates exchange the task and its scoped context instead of exchanging AI accounts.
