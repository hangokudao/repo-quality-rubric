# Frontend And Product Design Overlay

Use this for websites, apps, product flows, dashboards, and design implementation reviews.

## Suggested Weights

| Criterion | Weight |
|---|---:|
| Task/workflow fit | 20 |
| Visual hierarchy and consistency | 20 |
| Interaction states and recoverability | 15 |
| Accessibility evidence | 15 |
| Responsive behavior | 10 |
| Content clarity | 10 |
| Implementation maintainability | 10 |

## Checks

- Verify the rendered UI, not just the source.
- Capture desktop and mobile screenshots when practical.
- Check primary workflow completion, empty/loading/error states, forms, navigation, and keyboard interaction.
- Check visual hierarchy, spacing, contrast, responsive layout, overflow, and text fitting.
- Match the design tone to the product domain: operational tools should be dense and calm; marketing pages can be more expressive.
- Avoid treating a pretty screenshot as proof that workflows, states, or accessibility work.

## Deductions

- Text overlaps, clips, or resizes layout unexpectedly.
- Buttons or controls use unfamiliar text where a standard icon/control pattern would be clearer.
- Mobile layout is visually present but core workflow is awkward or hidden.
- Accessibility is asserted but not checked.
