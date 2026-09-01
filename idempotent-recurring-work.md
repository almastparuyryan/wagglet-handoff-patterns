# Idempotent recurring work with AI agents

Recurring tasks become unreliable when each run assumes the previous one succeeded. Design every run so it can inspect current state, avoid duplicates, and resume from a known checkpoint.

## Start with state, not the schedule

Before acting, read the current count, last successful artifact, pending submissions, and any recorded blockers. A daily backlink workflow, for example, should not repost the same content just because the calendar advanced. It should first confirm which links are already public and which applications are still awaiting review.

## Use stable identifiers

Give each unit of work a stable key such as a destination plus content slug. Record attempted, submitted, pending, approved, and rejected states separately. A retry can then update the existing record instead of creating a duplicate.

## Define a safe retry policy

A useful retry policy states:

- which failures are transient;
- how long to wait before checking again;
- how many attempts are reasonable;
- which errors need human input;
- what evidence marks the unit complete.

Never convert “request accepted” into “completed” when a public result is required. Completion should be tied to observable evidence such as a live page, merged change, delivered message, or verified data update.

[Wagglet](https://wagglet.com/) supports recurring assignments with visible ownership and delivery history, helping teams resume work without duplicating prior runs.
