# dynamo-codebase-patterns

This folder is owned and maintained by the **Dynamo Codebase Patterns** agent (`agents/dynamo-codebase-patterns.agent.md`).

Do not edit pattern files manually without also updating the agent, and do not add patterns here that have not passed the agent's four-question filter.

## Status vocabulary

| Status | Meaning |
|---|---|
| `candidate` | Proposed pattern, not yet validated against 3+ real examples |
| `confirmed` | Validated and actively enforced in PR review |
| `legacy` | Still exists in the codebase but do not add new uses |
| `retired` | No longer present; kept for historical reference only |

## Catalog limit

The total number of `candidate` + `confirmed` patterns should stay under 40. Propose retiring a pattern before adding a new one if the catalog is at capacity.
