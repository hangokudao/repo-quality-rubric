# Accessibility Overlay

Use this for web UI, documents, generated pages, and product experiences.

## WCAG-Oriented Checks

- Keyboard access: all core actions reachable and visible focus is present.
- Text alternatives: meaningful images, icons, and controls have accessible names or labels.
- Contrast: important text and controls meet contrast expectations.
- Structure: headings, landmarks, labels, tables, and form errors are semantically usable.
- Responsive/zoom: content remains usable at narrow widths and high zoom.
- Motion: animations do not block use and respect reduced-motion expectations when relevant.
- Errors: form errors identify the field and explain the fix.

## Evidence

- Automated tools are useful but not sufficient.
- Pair automated checks with manual keyboard and screen-size checks when the UI matters.
- When not checked, state it clearly under "Not verified" instead of giving accessibility credit.

## Deductions

- Core workflow cannot be completed by keyboard.
- Low contrast affects primary text or actions.
- Form fields lack labels or errors are only color-coded.
- Text overlaps or disappears at mobile widths or zoom.
