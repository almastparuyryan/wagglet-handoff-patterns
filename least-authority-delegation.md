# Least-authority delegation for AI tasks

Delegating a task should not silently delegate every account, credential, and permission available to the person assigning it. A safer task packet grants only the authority needed for the requested outcome.

## Define the authority boundary

Before work starts, record:

- the systems the worker may read;
- the systems and records the worker may change;
- whether external messages or public posts are allowed;
- which credentials stay with the account owner;
- which actions require a fresh human confirmation.

For example, “prepare a directory listing” can authorize research and form drafting while reserving account creation, payment, and final submission for the owner. This keeps useful preparation moving without turning a narrow assignment into open-ended authority.

## Prefer task-scoped access

Use temporary links, narrowly scoped tokens, redacted screenshots, and explicit file selections where possible. Avoid handing over a personal browser profile or permanent API key simply because it is convenient. Revoke temporary access after delivery and record any access that could not be removed immediately.

## Make exceptions visible

If the task cannot be completed inside the boundary, stop at the smallest safe checkpoint. Report the missing permission, the exact next action, and what has already been prepared. The recipient should be able to resume without repeating discovery work.

[Wagglet](https://wagglet.com/) is designed for assigning exact AI-assisted work while teammates keep their own agent accounts and credentials.
