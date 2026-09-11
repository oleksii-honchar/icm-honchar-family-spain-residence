# Statuses — how to read a member's pipeline

The filesystem is the state machine. A stage is COMPLETE when its `output/` holds files other than `.gitkeep`. Status is derived by scanning output folders — never hand-edited indexes.

| Stage | Output artifact | What COMPLETE means | What a human must check |
|---|---|---|---|
| `01_profile` | `output/profile.md` | profile has identity, TP/TIE chain, work/padrón history, paperless refs | re-check NIE/TIE dates against cards |
| `02_route` | `output/route.md` | one route chosen with rationale + open questions | decide route; confirm with ONG/lawyer |
| `03_documents` | `output/checklist.md` | full doc checklist with per-doc status (✓ / GAP / TODO) | gather missing docs (gaps flagged) |
| `04_filing` | `output/filing-plan.md` | tasas, forms, cita, filing steps, notificaciones | book cita; verify tasas + forms |
| `05_longterm` | `output/timeline.md` | resolution, TIE, 5y larga duración mark | calendar the larga duración mark |

## Status prefixes per member

- `members/<name>/` exists but no `stages/01_profile/output/profile.md` → **stub** (Yuliia).
- `01_profile` output exists, no later stage → **profiled**; current = `02_route`.
- Any stage's output folder holds files → that stage is COMPLETE → operator moves to next numbered stage.
- A stage's `output/` holds only `.gitkeep` → that stage is **not started**.

## Privacy statuses

- `_shared/membership.md` holds only roster-level facts (NIE/TIE/padrón/paperless ids) — no certificates.
- Certificates and sensitive scans belong in the member's own `stages/*/output/` (or outside the repo); never in `_shared/`.

Reconstruction logic (if `_meta/progress.md` lost): re-derive `completed[]` from what's in output folders, in numbered order; set `current` to the first stage without a complete output; rewrite `_meta/progress.md`; proceed.