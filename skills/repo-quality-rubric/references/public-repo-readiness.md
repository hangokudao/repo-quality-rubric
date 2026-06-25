# Public Repo Readiness Overlay

Use this when the repo is public, intended to be shared, or being prepared for release.

## Checks

- README explains what the project is, who it is for, install/setup, basic usage, examples, and limitations.
- Examples use neutral placeholders such as `localhost`, `example.test`, or `<your-authorized-url>` instead of personal domains unless intentionally public.
- License exists when distribution is intended.
- Contribution, security, issue, and PR guidance exist when the repo expects outside users.
- `.gitignore` blocks local output, secrets, run artifacts, and private folders.
- No obvious secrets, personal paths, private domains, or accidental generated artifacts are present.
- CI or repeatable local verification commands are documented.
- Language links, badges, and docs navigation work and are not corrupted.

## Deductions

- First-viewport README text or links are broken.
- The public examples cannot be safely copied.
- Current files are clean but older history may contain sensitive material; mention separately and do not rewrite history unless asked.
- Repo claims support for a workflow that is not tested or documented.
