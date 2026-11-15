# History Teacher Dashboard

Plain HTML teacher page for the GCSE History Homework Hub. Uses Supabase Auth and
teacher-authorised database queries. Use fictional pupil data only.

## R1 backend source and contracts

The shared database baseline is maintained in the sibling `gcse-history-homework-hub`
repository under `supabase/migrations/`. Its README documents all 21 database functions,
local rebuild instructions, export provenance and verification scripts. Do not duplicate
or independently edit the schema in this repository. All database changes must be new
migration files, verified locally, with explicit approval before hosted application.

Teacher RPCs use the `public` schema:

| Function | Parameters | Return fields/type |
| --- | --- | --- |
| `is_history_teacher` | none | boolean: whether `auth.uid()` is an approved teacher |
| `get_history_class_results` | `requested_class text`, `requested_quiz uuid` | `pupil_code text`, `register_number integer`, `attempts bigint`, `highest_score integer`, `homework_status text` |

The results RPC checks teacher approval and class allocation, and includes pupils without
attempts for a published quiz of the matching year. The page also reads `history_classes`,
`history_quizzes` and `history_pupils` with the signed-in teacher's RLS permissions.
The R1 two-page smoke test lives in the sibling repository at `tests/r1/pages.cjs`.
No browser secret/service-role keys belong here; do not commit credentials.

## R3 local changes

The page now requests `register_number` separately from pupil codes and sorts by it.
Random pupil credentials no longer carry a class prefix or register suffix. The class
results RPC includes register_number too. These changes depend on the R3 migration in
the pupil/backend repository. Apply that migration only with owner approval, before
publishing this page. Nothing has been pushed or published for R3.
