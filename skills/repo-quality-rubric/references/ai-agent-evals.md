# AI Agent Workflow Overlay

Use this for repos that implement agents, prompt workflows, eval harnesses, tool orchestration, or generated task pipelines.

## Suggested Weights

| Criterion | Weight |
|---|---:|
| Goal completion | 25 |
| Tool choice and sequencing | 20 |
| Instruction adherence | 20 |
| Failure recovery | 15 |
| Trace/eval repeatability | 10 |
| Cost, latency, and scope control | 10 |

## Checks

- Prompts and instructions define success criteria, boundaries, and outputs.
- Tool calls are justified by state, not blind loops.
- The workflow preserves user constraints and refuses unsafe actions.
- Failures produce recoverable next steps instead of hallucinated success.
- Evals or fixtures cover representative tasks, regressions, and edge cases.
- Outputs include enough trace or evidence to debug why a run passed or failed.
- Costs, model choices, and retry loops are bounded for routine use.

## Deductions

- The agent reports success without checking the artifact or command result.
- The eval asserts generic text instead of task-relevant behavior.
- Tool permission boundaries are unclear.
- The system cannot reproduce or inspect a failing run.
