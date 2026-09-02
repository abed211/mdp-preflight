# MDP Preflight

![MDP Preflight — Prove your AI-coded project is ready](social-preview.jpg)

**Your AI finished the screens. Did it finish the system?**

[![Release](https://img.shields.io/github/v/release/abed211/mdp-preflight?style=flat-square&color=2457ff)](https://github.com/abed211/mdp-preflight/releases/latest)
[![Free audit](https://img.shields.io/badge/audit-free-12a594?style=flat-square)](MDP-PREFLIGHT.md)
[![Read only](https://img.shields.io/badge/default-read--only-6b7280?style=flat-square)](MDP-PREFLIGHT.md)

MDP Preflight is a free, evidence-first readiness audit for repositories built with Codex, Claude Code, Cursor, Copilot, Gemini CLI, Windsurf, and other coding agents. It exposes what polished interfaces often hide: disconnected flows, missing business rules, client-only authorization, fake persistence, unsafe data paths, untested integrations, and release claims without proof.

It does **not** rewrite your project, install dependencies, expose secrets, or confuse plausible-looking code with working software.

## Try It in 60 Seconds

Open your repository in a coding agent and paste this:

```text
Read https://raw.githubusercontent.com/abed211/mdp-preflight/main/MDP-PREFLIGHT.md
and run MDP Preflight against this repository in AUDIT ONLY mode.
Do not change files. Support every score with repository or executable evidence.
Return the compact report defined by the audit.
```

Prefer a local file? Download the [latest release](https://github.com/abed211/mdp-preflight/releases/latest), place `MDP-PREFLIGHT.md` at your repository root, and use the same request.

## What Changes After the Audit

| Before | After |
|---|---|
| “The project looks finished.” | Every readiness claim is tied to evidence. |
| Screens are reviewed in isolation. | One critical journey is traced across UI, API, data, and services. |
| Missing tests are treated as uncertainty. | Unverified claims are marked `NOT VERIFIED`, never silently passed. |
| A total score hides serious risks. | Confirmed security and data-integrity blockers override the score. |
| The next step is “keep coding.” | You receive release blockers and the next three engineering actions. |

See the [three-application delivery-platform report](SAMPLE-REPORT.md) for a realistic example.

## Run It Manually

1. Open your project in your coding agent.
2. Copy the complete contents of [`MDP-PREFLIGHT.md`](MDP-PREFLIGHT.md) into the agent, or place the file at the repository root and ask the agent to run it.
3. Keep the run in `AUDIT ONLY` mode.
4. Review the evidence, score, release blockers, and next three actions.

Recommended local request:

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

The audit is intentionally diagnostic: it shows what is proven, what is broken, and what remains unknown before more code is added.

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

[Explore Miracoulia Developer Protocol — Enterprise Edition](https://miracoulia.lahza.store/products/miracoulia-developer-protocol?utm_source=github&utm_medium=repository&utm_campaign=mdp_preflight_v1)

## Honest Limits

An AI audit is not a security certification, legal review, penetration test, or substitute for qualified engineering judgment. Findings depend on repository access, runtime availability, tool behavior, and the evidence that can actually be verified. Missing evidence must be reported as `NOT VERIFIED`, never silently converted into a pass.

## Free-Use Notice

Copyright © 2026 Miracoulia. You may use and share this free package unchanged with attribution to Miracoulia. You may not sell it, remove its attribution, represent it as your own, or use it to distribute a competing derivative protocol. This is a free diagnostic package, not an open-source license. See [`LICENSE.md`](LICENSE.md) for the complete terms. No warranty is provided.
