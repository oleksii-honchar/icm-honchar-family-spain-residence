# Membership Roster — one home per person fact

Single source for who the family is, their NIE/TIE chain, and their paperless document ids. Person-specific data belongs in the member's `01_profile/output/profile.md`; this file holds only the stable cross-referenced facts everyone reads.

## Family

| Member | Name (legal) | Role | DOB | NIE | TP/TIE chain | Workspace record |
|---|---|---|---|---|---|---|
| oleksii | HONCHAR, Oleksii | father / family head (user) | 02/10/1979 | Z0166205N | TP desplazados; TIE issued 11/04/2025 Toledo; AUTORIZA A TRABAJAR | `members/oleksii/` |
| yuliia | HONCHAR, Yuliia | spouse (mother) | 14/11/1989 | Z0255414G | Tarjeta de residencia (per padrón Jan 2025) | `members/yuliia/` |
| artem | PRYKHODCHENKO, Artem | son (minor) | 10/02/2016 | Z0255480R | TP desplazados; TIE chain Alicante 12/2022 → Toledo 11/04/2025; NO AUTORIZA A TRABAJAR; depends on Z0255414-G (Yuliia) | `members/artem/` |

Notes:
- Artem's surname differs from parents (Prykhodchenko vs Honchar) — this is the father's surname; Yuliia is the legal representative in Spain. Artem's biological father lives in Ukraine (second-parent consent needed for residence filings).
- All three empadronado Calle Oasis 63, 1ºA, 45200 Illescas (Toledo) since 15/01/2025; prior padrón Alicante (Av. Maestro José Garberí 11) from ~Dec 2022.
- SS number Oleksii: 031153181317.

## Paperless document index (paperless IDs)

| Doc | Oleksii | Yuliia | Artem |
|---|---|---|---|
| TIE (protección temporal) | id 17 (Z0166205N, valid until 04/03/2026, auto-ext.) | — | — (no TIE PDF in paperless; present per padrón) |
| Padrón (15/01/2025, Oasis 63) | id 18 | id 18 | id 18 |
| Vida laboral (SS days) | id 25 (2024-12-12, 694 d), id 79 (2025-05-07, 849 d), **id 168 (2026-09-11, 1.341 d** = 3y 8m 3d; CEA GLZ3Z-RRYM5, verif. ≤12/09/2028) | — | — |
| Modelo 100 filings (Hijo listed Artem) | ids 69/80/87 | ids 69/80/87 | ids 69/80/87 |
| Passport (foreign) | **id 166** (PP GO229656, exp 21/05/2036; added 2026-09-11) | — | — (scans exist in session only; migration todo) |
| Work history (payslips) | Taxfix 2023.05 payslip id 118; **Payfit series ids 99…88 (2025) + 164/159/161/162/160/165/163 (2026); last 3 = 163/165/160** | — | — |
| **Payfit employment contract** | **id 167** (PF RH - CDI 2024, 20/01/2025, indefinido, Senior Software; added 2026-09-11) | — | — |
| Other | Contrato Securitas id 38 (name OCR "Olek/Oleksii <span class=...>Honchar</span>"; linked to ZAD3977 524) | — | — |

**Sources:** Artem residence session (2026-08-22) data-artem-family.json + paperless search (2026-09-05, refreshed 2026-09-11 — passport id 166, Payfit payslip series, Payfit contract id 167, and current vida laboral id 168 verified live). Verify before relying: TIE card backs, padrón certs.

> ⚠️ Domicile watch (2026-09-11): vida laboral id 168 shows the domicile registered at TGSS as Av. Maestro José Garberí 11, 03540 ALICANTE — the pre-move (pre-01/2025) address, NOT Calle Oasis 63 Illescas. Not fatal for art. 191 (informe is used to accredit time in alta), but flag when domicile matters (e.g., future larga duración/notifications) — consider updating it in TGSS/Tu Seguridad Social.

## Status per member (for the routing table)

| Member | Stage | Status | Next action |
|---|---|---|---|
| oleksii | 02_route | in progress | decide route (art. 191 vs wait for larga duración Nov 2027) |
| artem | 03_documents | imported (research 2026-08-22) | obtain second-parent consent + school certificate |
| yuliia | — | stub | bootstrap (profile + route) when user says go |

### All members share the timeline anchor

- TP since ~Nov–Dec 2022 (Oleksii first SS alta 22/11/2022; Artem NIE ZAD5480 registers 12/2022).
- 5-year larga duración nacional mark (per SEM 2/2026 TP time counts): **≈ Nov–Dec 2027** (confirm each member's exact TIE/NIE start).
- TP regime ends 04/03/2028 (Decisión (UE) 2026/1912); TIE auto-valid to 04/03/2027 (Orden INT/96/2026).

> Note: earlier draft said "Olek Slivskii Honchar phone 671402580 email tuiteraz" — that is the Securitas contract holder, same Oleksii; keep in profile, not roster.