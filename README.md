# MDP Preflight

**A free, evidence-first readiness audit for AI-coded projects.**

Before asking an AI coding agent to add another feature, make it prove that it understands the product it is changing.

MDP Preflight is a compact, read-only audit for repositories being built or maintained with Codex, Claude Code, Cursor, Copilot, Gemini CLI, Windsurf, or another coding agent. It finds the gaps that polished screens often hide: disconnected flows, missing business rules, weak authorization, fake persistence, unsafe data paths, untested integrations, and release claims without evidence.

It does **not** rewrite your project, install dependencies, expose secrets, or claim that a repository is safe because it looks complete.

## Run It in Minutes

1. Open your project in your coding agent.
2. Copy the complete contents of [`MDP-PREFLIGHT.md`](MDP-PREFLIGHT.md) into the agent, or place the file at the repository root and ask the agent to run it.
3. Keep the run in `AUDIT ONLY` mode.
4. Review the evidence, score, release blockers, and next three actions.

Recommended request:

```text
Run MDP Preflight against this repository in AUDIT ONLY mode.
Do not change files. Support every score with repository or executable evidence.
Return the compact report defined in MDP-PREFLIGHT.md.
```

## What It Checks

MDP Preflight scores ten areas from 0 to 5:

1. project and execution clarity;
2. requirements and business rules;
3. feature completeness;
4. data integrity and persistence;
5. authentication and authorization;
6. multi-system contracts and shared journeys;
7. executable testing;
8. security and privacy controls;
9. release and operational readiness;
10. context and project-memory discipline.

The result is a score out of 50, but the number is not the decision. A confirmed critical security issue, client-only authorization, exposed secret, fake test result, disconnected production flow, or unrecoverable data risk remains a blocker regardless of the total.

See [`SAMPLE-REPORT.md`](SAMPLE-REPORT.md) for an example based on a three-application delivery platform.

## Why the Audit Is Deliberately Small

More instructions do not automatically produce better engineering. A 2026 study of repository-level context files found that they did not generally improve task success and increased inference cost by more than 20% on average. The authors recommend evaluating instruction value instead of assuming that larger context helps.

MDP Preflight follows the same principle: search first, open a small evidence set, expand only when a finding requires it, and never treat a repository summary as proof.

Research: [Evaluating AGENTS.md: Are Repository-Level Context Files Helpful for Coding Agents?](https://arxiv.org/abs/2602.11988)

## Free Audit vs. MDP Enterprise

| MDP Preflight — Free | MDP Enterprise — Commercial |
|---|---|
| Diagnoses visible engineering gaps | Governs work from discovery through release |
| Produces a one-time readiness report | Maintains durable project memory across sessions |
| Read-only by default | Guides implementation, integration, testing, repair, and release evidence |
| Uses one compact audit workflow | Routes ten specialist protocols only when triggered |
| Does not fix findings | Converts findings into connected, verified implementation waves |

MDP Enterprise is a buyer-specific repository protocol for teams that want a coding agent to build complete features—not isolated screens—and preserve requirements, contracts, design decisions, security findings, tests, and release state without loading the complete protocol on every task.

**Get Miracoulia Developer Protocol — Enterprise Edition:**

https://miracoulia.lahza.store/products/miracoulia-developer-protocol

## Honest Limits

An AI audit is not a security certification, legal review, penetration test, or substitute for qualified engineering judgment. Findings depend on repository access, runtime availability, tool behavior, and the evidence that can actually be verified. Missing evidence must be reported as `NOT VERIFIED`, never silently converted into a pass.

## Free-Use Notice

Copyright © 2026 Miracoulia. You may use and share this free package unchanged with attribution to Miracoulia. You may not sell it, remove its attribution, represent it as your own, or use it to distribute a competing derivative protocol. This is a free diagnostic package, not an open-source license. See [`LICENSE.md`](LICENSE.md) for the complete terms. No warranty is provided.
