
# Track-Record State — user_oleksii.md

Per-user state record (icm-specialist per-user convention). `userKey` matches the filename; identity from the Bensyne user bank. History carried over 2026-10-04 by explicit human instruction from the legacy shared `_meta/progress.md` (now removed); `change_history` events backfilled on stage output artifacts as same-user recovery proof.

## 2026-10-06 — LIVE: ADMITIDA A TRÁMITE + requerimiento de tasas (05_longterm)
- Comunicación de inicio del procedimiento expte. **450020260012292** (Oficina Extranjería Toledo, doc 05/10/2026, notified 06/10 09:43, CSV CNO-018e-8599-ee31-ee83-abbd-66c8-7eea-c65b). Stored: members/oleksii/stages/05_longterm/materials/2026-10-05_OFICINA-EXTRANJERIA-TOLEDO_comunicacion-inicio_REQUERIMIENTO-TASAS_expte-450020260012292_HONCHAR.pdf
- **URGENT: pay 790-052 €10,94 + 790-062 €81,54 within 10 DÍAS HÁBILES (deadline ≈ 20/10/2026), then remit justificantes via ADAE/Mercurio.** Non-payment = desistimiento/archivo (art. 68 Ley 39/2015).
- Resolution clock: 3 months from admisión ≈ 06/01/2027; silencio NEGATIVO if silent (appealable). timeline.md §1 updated.
- Note: state format migrated to journal.md + jsonl (legacy user_oleksii.md in _migrated/).

## 2026-10-04 — LIVE: 04_filing started, filing plan written
- Filing plan: members/oleksii/stages/04_filing/output/filing-plan.md (channel, docs, step order A–E, payment records, human-check gate).
- Channel RESOLVED (Hoja 55): Mercurio, Oficina Extranjería Toledo (45). Silence correction: NEGATIVO after 3m.
- HUMAN GATE: sign method decision (Cl@ve vs FNMT+AutoFirma), then Oleksii executes submission + payment personally; record resguardos here + _shared/procedures-tasas.md.

## 2026-10-04 — LIVE: EX-26 form filled + doc upload 4/9 (04_filing)
- Form filled & validated → Id formulario inicial I45202604965185. Rep/employer corrections applied (Miazzo Y3769091A, Payfit 08018, CNAE 6209).
- 4 docs attached server-side with HASH (pasaporte, recursos, contrato, nómina agosto). 5 remaining staged (upload/ + /tmp/ex26_upload/).
- Tooling blocker: CloakBrowser MCP upload bug (ENAMETOOLONG on base64) + native picker interception in driven browser → manual upload impossible there. Human check surfaced; manual-browser restart recommended (data sheet given). Lesson: in automation-driven browsers, file pickers are intercepted — never let the human click Examinar there; and never cancel stale pickers after a successful upload (resets plupload queue).

## 2026-09-16 — LIVE: solicitud certificado de convivencia (03_documents)
- SIA 3218824 wizard + RE-11414; resolved 2026-09-27 as paperless id 177 (certificado colectivo). Calendar reminder created.
