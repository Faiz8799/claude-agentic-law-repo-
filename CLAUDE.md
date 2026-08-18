# Claude Legal — Project Rules

Team of subagents and skills for legal work. Default jurisdiction: **Spain and the European Union**.

## Non-negotiable rules

1. **Zero invention.** No agent cites a statute, judgment, appeal number or ECLI that it cannot verify. If it cannot be located, write `NOT LOCATED`. A fabricated citation destroys the matter and the firm's credibility.
2. **Mandatory verification.** No document goes out without passing through `verificador-citas`. It has veto power and its verdict is not negotiable under deadline pressure.
3. **Conflicts first.** `conflict-check` runs before any substantive work on a new matter.
4. **Deadlines always.** As soon as a relevant date appears, `plazos-procesales` steps in. A missed deadline cannot be recovered.
5. **Protected data.** Nothing leaves the environment without passing through `anonimizador`. Professional secrecy and GDPR.
6. **Cut-off date.** Every deliverable states the date through which the applicable legislation has been verified.
7. **Human review.** All output is preparatory work. It requires review and adoption by a qualified lawyer. It is not legal advice.
8. **Facts, not assumptions.** Whatever you have not been told is marked `[PENDING: ...]`. Never filled in with what seems reasonable.

## Standard workflow

```
(incoming case) triaje-asuntos → conflict-check → legal-orchestrator → [specialists in parallel]
                                              → contradictor → verificador-citas → delivery
```

## Structure

- `agents/` — 45 subagents. Copy to `.claude/agents/` (project) or `~/.claude/agents/` (global).
- `skills/` — 10 skills. Copy to `.claude/skills/`.
- `commands/` — 8 slash commands with the complete workflows. Copy to `.claude/commands/`.

## Note on the number of active agents

The orchestrator decides who to delegate to by reading the `description` field. With 44 candidates loaded at once, routing degrades. Keep the core active and load the verticals as needed for each matter.

**Recommended core (13):** legal-orchestrator, triaje-asuntos, legal-researcher, verificador-citas, conflict-check, contract-drafter, contract-reviewer, redline-negotiator, contradictor, compliance-officer, plazos-procesales, anonimizador, plain-language.
