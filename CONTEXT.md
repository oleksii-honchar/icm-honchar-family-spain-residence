# Honchar Family — Spain Residence: the pipeline

The flow in one line: profile each member, pick their route, gather their documents, file, then track to long-term residence.

Per-member pipeline (same shape for everyone — `_templates/member/`):

| Stage | Job | Input | Output | Human check |
|---|---|---|---|---|
| `01_profile` | establish identity + TP status | `_shared/membership.md`, paperless | `output/profile.md` | re-check NIE/TIE dates against cards |
| `02_route` | choose authorization route | profile + `_shared/rules.md` | `output/route.md` | decide route; confirm with ONG/lawyer |
| `03_documents` | build the doc checklist | route + paperless | `output/checklist.md` | gather missing docs (gaps flagged) |
| `04_filing` | tasas, forms, cita, file | checklist | `output/filing-plan.md` | book cita; verify tasas + forms |
| `05_longterm` | resolution, TIE, 5y mark | filing-plan + resolution | `output/timeline.md` | calendar the larga duración mark |

Roster + identity: `_shared/membership.md` (person facts, NIE, TIE chain, paperless ids — one home per fact).
Legal framework: `_shared/rules.md` (protección temporal, SEM 2/2026, art. 160 minors, larga duración requirements, fees, forms, sources).
Statuses: `_shared/statuses.md` (what COMPLETE means per stage; how to read output folders).

Factory (stable, every run): `_shared/{membership.md, rules.md, statuses.md}`
Product (new per run): each member's `stages/*/output/`

Status is whatever exists: a stage is COMPLETE when its `output/` holds files other than `.gitkeep`.

The family shares one timeline anchor: TP (protección temporal) since ~Nov–Dec 2022 → 5-year larga duración mark ≈ Nov–Dec 2027 (per SEM 2/2026, TP time counts). Artem's research (2026-08-22) is the precedent this workspace was built from — see `members/artem/`.