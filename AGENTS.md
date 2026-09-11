# Honchar Family — Spain Residence

One workspace for the whole family's immigration pipeline: each member is a record with its own 5-stage pipeline; the shared reference (legal framework, roster, statuses) lives once in `_shared/`. What leaves the workspace: a filed EX-25/EX-11 application per member and a resolucion/granted TIE tracked to the 5-year larga duración mark.

Built on ICM: folders carry sequencing, hierarchy carries context, files carry state. The structure is the documentation — if something needs explaining, the explanation goes in that folder's CONTEXT.md, not in your head.

## Where things live

| Folder | What it holds |
|---|---|
| `members/<name>/` | one record per family member (artem, oleksii, yuliia) |
| `members/<name>/stages/` | that member's pipeline: 01_profile → 02_route → 03_documents → 04_filing → 05_longterm |
| `_shared/` | factory: roster, legal framework, statuses — stable, every member reads these |
| `_templates/member/` | blank member record — new person = a copy, not a blank page |
| `_meta/progress.md` | the single state file: where we are, what's done, what's next |

## Route by what just happened

| If | Go to | Then stop at |
|---|---|---|
| starting a new member | `_templates/member/` → copy to `members/<name>/` | fill `01_profile/output/profile.md` from `_shared/membership.md` + paperless |
| a member's stage output is approved | that member's next numbered stage | human reads the next output |
| asked for family status | scan `members/*/stages/*/output/` | report what exists per member |
| asked "what's the law / what's the route" | `_shared/rules.md` + that member's `02_route/output/route.md` | flag open legal questions |
| asked about a person's identity/status | `_shared/membership.md` | verify against paperless before replying |

## The one rule

Nothing moves to the next stage until a person has read the output of the last one.

## Privacy

NIE numbers, TIE data and personal documents live in this repo. Do not push to a public remote and do not copy person-specific data into `_shared/` beyond the roster.