# Core Rubric

Use this as the baseline when no domain-specific rubric is a better fit.

## Baseline Weights

| Criterion | Weight | What To Look For |
|---|---:|---|
| User-facing quality | 20 | First-run experience, generated output, messages, encoding, examples, errors, clarity |
| Functional correctness | 20 | Core flows work, tests cover important behavior, invalid inputs behave predictably |
| Safety boundaries | 15 | Destructive actions gated, secrets protected, external targets authorized, mutation limits clear |
| Packaging and operations | 15 | Build/package/install/run flow works, artifacts are clean, CI or repeatable commands exist |
| Maintainability | 15 | Small coherent modules, simple design, readable names, no speculative abstraction |
| Documentation/readiness | 10 | README, usage examples, public hygiene, release notes or contribution/security files when relevant |
| Verification quality | 5 | Evidence is fresh, commands are cited, unknowns are listed separately |

## Severity Guidance

- Critical: breaks core use, leaks secrets, enables unsafe external action, corrupts user-facing output, or makes the package unusable.
- High: makes common workflows fail, blocks release, or creates misleading documentation.
- Medium: hurts maintainability, confidence, or important edge cases.
- Low: polish, style, minor docs, or small packaging cleanup.

## Evidence Rules

- Prefer exact file paths, line numbers, command names, and observed outputs.
- If a generated file is part of the user experience, inspect the generated file, not only the template source.
- Passing tests do not prove user-facing quality; still inspect docs, samples, and generated output.
- A clean git tree is useful evidence, but not a quality score by itself.
- Do not count "not checked" as "passed."
