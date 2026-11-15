# Teacher dashboard deployment mirror

Edit the source in
[gcse-history-homework-hub](https://github.com/monob26/gcse-history-homework-hub/tree/refactor/r6-consolidate-pages/teacher).
This repository holds prepared static deployment files to preserve
<https://monob26.github.io/history-teacher-dashboard/> and the existing Auth redirect.

Generate `index.html`, `teacher/` and `shared/` with the source repository's
`scripts/prepare-pages.py teacher <staging-directory>`, then copy them into a reviewed
deployment branch here. Do not edit these generated page files directly. The source
repository's `docs/R6.md` records the deployment order and validation.
