# Teacher dashboard R3 handoff

Recorded 15 November 2026. Use branch `review/r3-pupil-code-sorting`.
Implementation commit c2800b5 sorts using the separate register_number field and
updates both quiz/no-quiz data paths. This code is local only: no teacher-page
publication, merge or push has occurred for R3.

The complete specifications, deployment state, tests and hosted fixture inventory
are in monob26/gcse-history-homework-hub on `review/r4-pupil-timers`, starting at
HANDOFF.md. Fetch that branch after the owner approves its push; main/R1 alone do
not contain the current review work. REVIEW.md remains the primary authority.

IMPORTANT: the R3 register_number migration is NOT hosted, so do not publish this
teacher page yet. Apply any backend/frontend rollout only after a concrete proposal
and explicit approval. Hosted R2 migrations and fictional access-test fixtures
already exist; do not recreate them or blindly db push the R1 baseline.

Saved local full companion T1–T12, both-page smoke/register sorting, R3 upgrade/rebuild
and R4 timer checks passed. Hosted external-access tests and T13/T14 have not run.
R2/R3/R4 remain incomplete. The owner declined Pro, leaving leaked-password protection
unresolved. The approved next test scope is R2/T1–T4 only, with fictional data and owner
presence. The original task lacks password variables; the new task reportedly has them.
Never put passwords/keys/session tokens in this repository or in chat.

This handoff commit changes documentation only. No new application tests or hosted
operations were run. Push/merge/publication still require separate explicit approval.
