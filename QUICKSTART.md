# MDP Preflight Quick Start

Run an evidence-first audit of an AI-coded repository without changing its files.

## Option 1 — Run from GitHub

Paste this into a repository-aware coding agent:

```text
Read https://raw.githubusercontent.com/abed211/mdp-preflight/main/MDP-PREFLIGHT.md
and run MDP Preflight against this repository in AUDIT ONLY mode.
Do not change files. Support every score with repository or executable evidence.
Return the compact report defined by the audit.
```

## Option 2 — Run Locally

1. Download the [latest release](https://github.com/abed211/mdp-preflight/releases/latest).
2. Copy `MDP-PREFLIGHT.md` into the root of the project being audited.
3. Ask the coding agent to run it in `AUDIT ONLY` mode.
4. Review the evidence table, score, release blockers, and next three actions.

## What a Valid Run Must Do

- Remain read-only unless the user explicitly changes the mode.
- Search before opening files and expand context only when evidence requires it.
- Trace at least one critical user journey across every affected application or service.
- Separate `PASS`, `PARTIAL`, `FAIL`, and `NOT VERIFIED`.
- Treat confirmed critical security, authorization, secret-exposure, and data-loss risks as release blockers.
- Never invent test results or convert missing evidence into a pass.

## Expected Output

A compact report containing:

- repository and runtime facts;
- evidence-backed scores across ten engineering areas;
- confirmed release blockers;
- unverified checks;
- the next three highest-value actions.

Compare your result with [`SAMPLE-REPORT.md`](SAMPLE-REPORT.md).

## Need the Findings Fixed?

MDP Preflight diagnoses the project. Miracoulia Developer Protocol — Enterprise Edition governs discovery, connected implementation, durable memory, security repair, testing, and release evidence.

[Explore MDP Enterprise](https://miracoulia.lahza.store/products/miracoulia-developer-protocol?utm_source=github&utm_medium=quickstart&utm_campaign=mdp_preflight_v1)
