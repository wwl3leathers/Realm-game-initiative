# Realm Game Initiative — Agent Rules

These instructions apply to the entire repository.

## Authority

- Butch owns all creative, mechanical, economic, lore, and scope decisions.
- Do not convert discussion, examples, implications, or suggestions into established design.
- Do not add or revise game mechanics without Butch's explicit approval.
- Do not change the README, established concept documents, repository structure, or these rules without explicit permission.
- When a requested implementation exposes a materially different player experience, economy, lore consequence, or Talvaren dependency, stop and ask.
- Ordinary technical implementation choices inside an approved design may proceed when they do not change that design.

## Player Experience

- Judge features by what players actually see, understand, decide, and enjoy.
- Prefer meaningful cooperation and readable consequences over mechanical complexity.
- Do not preserve a technically elegant feature that makes play tedious, confusing, punitive, or socially hostile.
- Realm Games must remain worthwhile experiences in their own right; Talvaren rewards may support them but must not be their sole reason to exist.

## Implementation Discipline

- Build the smallest complete implementation of the approved behavior.
- Reuse proven Talvaren systems and assets only after their dependencies and licenses are verified.
- Do not introduce adjacent systems, speculative abstractions, visual embellishments, simulations, or future-proofing without approval.
- Preserve authored prefabs, scenes, metadata, GUID relationships, and working asset references.
- Never replace an existing working asset merely because recreating it appears easier.
- Keep generated files, caches, recordings, screenshots, temporary comparisons, and disposable test evidence out of version control.

## Precision and Stopping Rules

- Use the tolerance approved for the task.
- If no tolerance is specified, choose a human-visible or gameplay-relevant tolerance appropriate to the feature and state it before prolonged refinement.
- Do not pursue microscopic numerical agreement when a result is already visually and functionally acceptable.
- Exact agreement is required only for invariants such as deterministic rules, network state, saved data, boundaries that prevent overlap or exploits, and explicitly exact requirements.
- Once approved acceptance criteria pass, stop adjusting the result.

## Git and Checkpoints

- Work locally through exploratory iterations.
- Do not commit or push every experimental adjustment.
- Commit coherent, reviewable checkpoints with concise messages describing the completed outcome.
- Before committing, inspect the diff and exclude unrelated changes, generated churn, secrets, local settings, and disposable evidence.
- Do not rewrite, squash, force-push, reset, or delete history without Butch's explicit permission.
- Do not add a large binary to ordinary Git. Use Git LFS when covered by `.gitattributes`, and inspect unusually large or frequently changing files before committing.
- Do not add all `.asset` files to LFS indiscriminately; many are mergeable Unity YAML.
- Preserve every authored Unity asset's matching `.meta` file.

## Validation

- Validate in proportion to risk.
- Prefer focused tests during implementation and a relevant broader pass at a checkpoint.
- Do not represent EditMode tests, scripted input, a rehearsal, or isolated prototype behavior as multiplayer or production validation.
- Report what was tested, what passed, and what remains unverified.
