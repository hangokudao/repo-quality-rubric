# Repo Quality Rubric

[한국어](README.ko.md)

A Codex skill for evidence-backed repository quality reviews.

Use this skill when you want Codex to review a repository, CLI, package, frontend app, documentation set, public release, or AI-agent workflow and return a weighted 100-point score with concrete evidence.

The skill asks Codex to:

- classify the project type
- choose the right weighted rubric
- inspect live evidence before scoring
- report must-fix issues separately from polish
- list anything that was not verified

## What It Produces

Example output shape:

```md
# Repo Quality Review

Total Score: 86/100

## Score Breakdown

| Criterion | Weight | Score | Evidence |
|---|---:|---:|---|
| User-facing quality | 20 | 16 | Generated examples are clear, but one README link is stale |

## Must Fix

1. ...

## Not Verified

- ...
```

## Skill Path

The installable skill is here:

```text
skills/repo-quality-rubric/
```

## Included Rubrics

- Core repository readiness
- Code review quality
- CLI and package release quality
- Public repo readiness
- Frontend and product design review
- Accessibility
- Security
- AI-agent workflow evaluation

## Usage

After installing or copying the skill into Codex, invoke it with:

```text
Use $repo-quality-rubric to review this repository and report a weighted 100-point score with evidence.
```

You can also ask naturally:

```text
Review this repository's public release readiness. Return a 100-point score with criteria and evidence.
```

## Notes

- This repository contains a Codex skill, not a full Codex plugin.
- The skill intentionally does not edit `AGENTS.md` or project rules during review.
- No license has been selected yet.
