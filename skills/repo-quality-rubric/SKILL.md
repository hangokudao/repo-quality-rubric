---
name: repo-quality-rubric
description: "Assess repository or project quality/readiness with a weighted 100-point rubric and concrete evidence. Use only when the user asks for a quality/readiness score, release-readiness check, 100-point rubric, weighted criteria, evidence table, or comparable benchmark for a repo, CLI, package, library, frontend app, documentation set, public release, or AI-agent workflow. Do not use for ordinary code review, PR review, bug fixing, implementation, or general review requests unless the user also asks for scoring, rubric, readiness, or evidence-backed criteria. Also use for Korean-language requests about repository quality checks, public release readiness, 100-point criteria, evidence, or weighted score breakdowns."
---

# Repo Quality Rubric

Use this skill to produce evidence-backed quality/readiness reviews. The goal is not a generic code review; the goal is a visible score breakdown with concrete evidence for each score.

## Core Rules

- Do not edit files during a review unless the user explicitly asks for fixes.
- Do not put rubric rules into `AGENTS.md` or other instruction files unless the user explicitly asks.
- Treat memory, prior summaries, and README claims as hints, not evidence.
- Prefer live evidence: files, generated output, tests, package contents, screenshots, logs, git state, and command output.
- Keep scope narrow. Score what was inspected, and list what was not verified.
- If a command would be expensive, risky, destructive, or externally consequential, skip it and list it under "Not verified" unless the user approved it.

## Workflow

1. Classify the artifact.
   - CLI/package, library/API, frontend/product UI, documentation/public repo, AI-agent workflow, security-sensitive system, or mixed.
   - If mixed, choose one primary rubric and add only the relevant overlays.

2. Load the minimum references needed.
   - Always read `references/core-rubric.md`.
   - For implementation quality, read `references/code-review.md`.
   - For CLI/npm/package release quality, read `references/cli-package-release.md`.
   - For public repo readiness, read `references/public-repo-readiness.md`.
   - For frontend/product UI, read `references/frontend-design.md` and `references/accessibility.md`.
   - For security-sensitive projects, read `references/security.md`.
   - For agent/eval workflows, read `references/ai-agent-evals.md`.

3. Gather evidence before scoring.
   - Inspect the repo structure and key manifests.
   - Read the smallest set of files needed to understand user-facing behavior.
   - Run existing tests, build, lint, package, or smoke commands when safe and relevant.
   - For generated artifacts, run the generator or inspect a fresh sample when feasible.
   - For UI/design work, capture screenshots or otherwise verify actual rendered output.

4. Score with weights.
   - Use a 100-point total.
   - Start from a reference weight set, then adjust only when the repo type justifies it.
   - Penalize user-facing broken output, failing core flows, unsafe defaults, missing tests for critical behavior, packaging mistakes, and unverifiable claims.
   - Do not hide uncertainty inside the score. Put unknown areas in "Not verified."

5. Report results in this shape:

```md
# Repo Quality Review

Total Score: NN/100

## Score Breakdown

| Criterion | Weight | Score | Evidence |
|---|---:|---:|---|
| ... | ... | ... | ... |

## Must Fix

1. ...

## Should Improve

1. ...

## Evidence Checked

| Evidence | Result |
|---|---|
| ... | ... |

## Not Verified

- ...

## Next Best Checks

- ...
```

## Scoring Calibration

- 90-100: Release-ready or near release-ready. Issues are polish, narrow edge cases, or low-risk improvements.
- 80-89: Strong, usable work with a few visible or operational gaps.
- 70-79: Directionally good but not yet public/release quality. One or more first-run, packaging, safety, or output-quality issues are material.
- 60-69: Useful prototype with significant correctness, verification, or readiness gaps.
- Below 60: High risk for real use; core behavior, safety, or maintainability needs substantial work.

When in doubt, make the score slightly conservative and explain the evidence gap.
