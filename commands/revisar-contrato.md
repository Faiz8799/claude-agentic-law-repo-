---
description: Contract review with risk matrix and proposed redlines
argument-hint: [path to the contract] [which side we represent: client/supplier/buyer...]
---

Review the contract: $ARGUMENTS

1. Delegate to `contract-reviewer`, indicating which side we represent.
2. Apply the `matriz-riesgos` skill: table sorted by level, with quantified economic impact.
3. For each 🔴 and 🟠 risk, ask `redline-negotiator` for alternative wording and the fallback position.
4. Run the result through `verificador-citas` if legislation was cited.
5. Deliverable: executive summary (blocking risks first) + matrix + redlines ready to insert.
