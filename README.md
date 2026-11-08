# No Three in Progression

This repo holds the checker and the context for the challenge.
See [What's left to build](#whats-left-to-build) for what remains to fine-tune.
The challenge page is built in the Yukon repo from PAGE.md with the create-challenge skill.

Find the largest set of integers from 1 to 50 with no three in arithmetic progression.

See [rules.md](rules.md) for the challenge rules.

## What's left to build

- The written plan is missing.
- The researcher needs to give the baseline: the best result known today and what a submission is compared against.
- The researcher needs to say how progress is measured.


<!-- llm-verifier:solver-guidance:begin -->
## Preparing a submission

Read the [solver guide](https://github.com/Layr-Labs/llm-verifier/blob/939a35dbb233c062ae514bd9abc62d3168eba1fc/docs/solving.md) and
[solver skill](https://github.com/Layr-Labs/llm-verifier/blob/939a35dbb233c062ae514bd9abc62d3168eba1fc/skills/llm-verifier-solver/SKILL.md)
from the same pinned verifier revision as this challenge.

- Use the challenge's verifier revision for `llm-verifier check --root .`.
- Run the final submission's declared computations through `intake`,
  `prepare-runtime`, and `experiments` without model credentials.
  `test-checkers` runs organizer fixtures, not your candidate's checks.
- Ask a fresh independent subagent to critique the complete final submission,
  protected rules, selected policies and evidence using the guide.
- Fix findings and rerun affected checks and review.
- Report results and omitted steps. Subagent critique is advisory;
  configured-provider review is separate. `simulate` does not judge correctness.
<!-- llm-verifier:solver-guidance:end -->
