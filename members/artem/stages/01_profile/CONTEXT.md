# 01_profile — establish identity + TP status

**Inputs**
- `_shared/membership.md` — this member's roster row (NIE, TIE chain, paperless ids)
- Paperless (search by name/NIE; verify against the roster's doc ids)

**Process**
1. Gather identity facts: full legal name, DOB, NIE, NSS.
2. Reconstruct the TP/TIE chain: first card, renewals, validity, working authorization.
3. Work history (SS days, employers, dates) from vida laboral docs.
4. Padrón history (settlement dates, addresses).
5. List paperless doc ids for every fact; mark anything without a source as GAP.

**Outputs** → `output/profile.md` (identity, TP status, work/padrón history, doc table, GAPs)

**Human check** — verify NIE/TIE dates against physical cards; confirm GAPs before 02_route.