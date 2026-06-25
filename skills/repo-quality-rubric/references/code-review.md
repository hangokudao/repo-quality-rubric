# Code Review Overlay

Use this for implementation-heavy repos, libraries, CLIs, services, and apps.

## Criteria

- Correctness: the code implements the requested behavior and handles realistic invalid inputs.
- Tests: tests cover the bug/feature, important edge cases, and integration points with reasonable cost.
- Simplicity: the design solves the problem without speculative frameworks, configuration, or indirection.
- Maintainability: module boundaries, naming, data flow, and errors are easy to follow.
- Local style: the change matches existing patterns instead of imposing a new style.
- Documentation: public APIs, CLI behavior, and non-obvious decisions are documented where users will look.

## Common Deductions

- Tests assert broken or corrupted output.
- New abstractions have only one caller and do not remove real complexity.
- Adjacent refactors obscure the actual change.
- Error handling is either missing for plausible failures or bloated for impossible ones.
- Behavior is only verified by snapshot shape, not meaningful user-facing content.

## Evidence To Gather

- Key implementation files.
- Test files and test output.
- Build/lint/typecheck output where applicable.
- Generated artifacts or runtime output for user-facing flows.
