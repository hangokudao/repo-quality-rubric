# CLI And Package Release Overlay

Use this for command-line tools, npm packages, libraries with publishable artifacts, and public release readiness.

## Suggested Weights

| Criterion | Weight |
|---|---:|
| First-run and user-facing output quality | 20 |
| Functional correctness and tests | 20 |
| Safety and permissions | 15 |
| Package artifact hygiene | 15 |
| Documentation and examples | 15 |
| Maintainability | 10 |
| Verification evidence | 5 |

## Checks

- Inspect `package.json`, bin entries, exports, files, scripts, dependencies, and version/license fields.
- Run tests and build commands when available.
- Run the CLI against a small safe fixture when feasible.
- Run dry-run packaging when available, such as `pnpm pack --dry-run` or `npm pack --dry-run`.
- Inspect the packed file list for tests, fixtures, private files, generated junk, source maps, or missing dist files.
- Check `.gitignore`, `.npmignore`, or package `files` behavior.
- Check generated templates, runbooks, config examples, and starter output for encoding issues and stale placeholders.

## High-Signal Deductions

- Broken text or mojibake in generated files: heavy deduction under user-facing quality.
- Published package includes `dist/test`, private fixtures, or large irrelevant files: packaging deduction.
- README examples do not match the actual CLI behavior: docs and user-facing deduction.
- Safety options exist but are not tested: safety and verification deduction.
- Package installs but the bin cannot run from a clean install: critical release deduction.
