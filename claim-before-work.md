# Claim-before-work concurrency for agent tasks

Parallel agents create a coordination problem before they create a coding problem. Two people can independently start the same ticket, modify overlapping files, and produce incompatible results even when both implementations are technically correct.

A claim-before-work protocol prevents that collision:

1. A task begins unclaimed and exposes its required model, skills, repository, and blockers.
2. One operator claims it before performing state-changing work.
3. The claim records ownership and a timestamp, and it has an expiry or explicit release path.
4. Other operators can still read the task but do not duplicate the implementation.
5. A blocked operator records evidence and releases or transfers the task cleanly.

Claims should be narrower than projects. A repository-wide lock destroys useful parallelism; a task-level claim protects the exact work boundary while unrelated tasks proceed.

The protocol also clarifies responsibility. Reviewers know which operator produced the result, what context they received, and whether the work was concurrent with another change.

[Wagglet](https://wagglet.com/) uses explicit task claims so teams can hand work to colleagues running their own coding agents without silently duplicating effort.
