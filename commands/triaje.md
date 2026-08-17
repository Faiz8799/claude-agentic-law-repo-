---
description: Filter incoming cases — accept/refer/decline opinion with deadlines and scoring
argument-hint: [description of the case, path to the inquiries folder, or paste the emails]
---

Run the incoming-case triage workflow on: $ARGUMENTS

1. If it is a path or folder, read every document it contains; each document or email is a candidate case.
2. Delegate the analysis to the `triaje-asuntos` agent (which in turn launches `conflict-check`).
3. Return the summary table sorted by deadline urgency and scoring, with the individual profiles below.
4. For each DECLINED or REFERRED case, offer to draft the non-engagement letter with a deadlines warning.
