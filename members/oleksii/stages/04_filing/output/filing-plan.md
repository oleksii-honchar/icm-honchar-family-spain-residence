---
change_history:
  - at: "2026-10-04T11:25:00Z"
    by: "user_oleksii"
    action: "created"
    artifact: "members/oleksii/stages/04_filing/output/filing-plan.md"
    stage: "oleksii/04_filing"
    summary: "Filing plan written: Mercurio channel (Hoja 55), EX-26 doc set, step order A-E, payment records, human-check gate. Stage NOT completed (gate open)."
  - at: "2026-10-04T11:55:00Z"
    by: "user_oleksii"
    action: "updated"
    artifact: "members/oleksii/stages/04_filing/output/filing-plan.md"
    stage: "oleksii/04_filing"
    summary: "Sign method DECIDED: FNMT certificate + AutoFirma v1.9 (installed on macOS); Cl@ve as fallback. Phase A adjusted for macOS (keychain .pfx import, validity check, test-sign). workStatus: in-progress."
---

# Oleksii HONCHAR — Filing Plan (04_filing)

> Date: 2026-10-04 · Route: art. 191.3 RD 1155/2024 (≥1y residence + AUTORIZA A TRABAJAR under TP) → **4-year autorización de residencia y trabajo** · Form: **EX-26**
> Inputs: `03_documents/output/checklist.md` (all 13 items READY, 2026-09-27) · `_shared/rules.md` · `_shared/procedures-tasas.md` · Hoja 55 (official, inclusion.gob.es)
> Status: **PLAN READY — awaiting human execution + human check** (the actual submission is done by Oleksii: Cl@ve/certificate login + card payment)

## Channel — RESOLVED (was open todo from route stage)

Verified 2026-10-04 at **Hoja 55** (Ministerio, "Modificación desde autorizaciones de residencia temporal que habilitan a trabajar", art. 191.3 section):

- **Telemática: Mercurio** — sede electrónica del Ministerio de Política Territorial y Memoria Democrática → `https://sede.administracionespublicas.gob.es/mercurio/inicioMercurio.html`
- Presencial alternative: Oficina de Extranjería de **Toledo** (provincia 45, residencia Illescas).
- NOT extranjeria.interior.gob.es (old URL), NOT sede.inclusion.gob.es for this procedure.

## Documents to upload (from paperless, per checklist)

| Field | Document | Paperless id |
|---|---|---|
| Pasaporte completo (en vigor) | PP GO229656 | 166 |
| TIE / NIE | Z0166205N (AUTORIZA A TRABAJAR, válida a 04/03/2027) | 17 |
| EX-26 (cumplimentado + firmado) | editable PDF from inclusion.gob.es → Modelos generales | — |
| Contrato de trabajo en vigor | Payfit CDI 20/01/2025 | 167 |
| Últimas nóminas (3+) | Jun/Jul/Ago 2026 (full 2026 series available) | 160/165/163 |
| Vida laboral (alta + ≥3 meses/año) | TGSS 11/09/2026, 1.341 días, Payfit 600 d en alta | 168 |
| Certificado de empadronamiento colectivo | Illescas 17/09/2026 | 177 |
| Prueba de medios (Santander) | saldo 5.864,81 € + 4 abonos nómina | 178 |
| Empleador: NIF/CIF | Payfit Recursos Humanos SL **B67154237** (C.C.C. 08207178383) | — |

Art. 191.3 supuesto to assert in the form: **continuing work relationship / alta + ≥3 months worked per year** (vida laboral + contract + nóminas prove it). Antecedentes: NOT attached — recabado de oficio (art. 74.h).

## Exact step order

**Phase A — preparation (before submission day)** — sign method DECIDED 2026-10-04: **(b) FNMT certificado + AutoFirma v1.9 on macOS** (Cl@ve = fallback if cert fails on the day).
1. ✅ AutoFirma v1.9 installed (macOS). Remaining prep:
   - Verify FNMT cert **validity** (4-year expiry — Keychain Access: search "FNMT"/NIE, check expiry). If expired: re-download from sede.fnmt.gob.es (identity already accredited) or fall back to Cl@ve.
   - Ensure cert + private key is in the **login keychain** of the Mac doing the filing (import .pfx via double-click if needed — see `_shared/procedures-autofirma.md` macOS section).
   - **Test-sign** a dummy PDF with AutoFirma once (macOS gotchas: first-run security permission prompts; use the JRE bundled with the AutoFirma installer).
2. Fill EX-26 (editable model), sign with AutoFirma. Data: solicitante OLEKSII HONCHAR, NIE Z0166205N; empleador Payfit (CIF B67154237); notificaciones = electronic, adult applicant's data (tuiteraz@gmail.com / 671402580).
3. Export the 8 documents above as legible PDFs from paperless.

**Phase B — submission (Mercurio)**
4. Login at `sede.administracionespublicas.gob.es/mercurio` → procedimiento **modificación de autorización de residencia** (art. 191), **órgano instructor: Oficina de Extranjería de Toledo (provincia 45)**.
5. Complete the registry form + upload documents per field. Submit → **resguardo with número de registro de entrada**.

**Phase C — tasas (within 10 días hábiles of admisión a trámite — Hoja 55)**
6. System generates the **tasación**: 790-052 **ep. 2.5.2 €10,94** (solicitante) + 790-062 **€81,54** (empleador — Oleksii pays per 2026-09-27 decision; if the system does not emit it, generate manually per `_shared/procedures-tasas.md`, ep. numbering: current form says 2.2, Hoja 55 cites 3.2.2 — the tasación is authoritative).
7. Pay via AEAT card/bank. **Upload the paid resguardos to the expediente** + save copies to paperless.

**Phase D — tracking**
8. Watch notificaciones electrónicas (DEHú 10-day risk). Resolution clock: **3 months**.
9. ⚠️ **Silence correction**: Hoja 55 states **desestimación por silencio negativo** after 3 months (route.md §2.5 assumed positive silence — corrected here). If silence/negative resolution arrives, appealable (reposición contencioso) — consult ONG/lawyer before letting it lapse.

**Phase E — after grant**
10. **Alta en Seguridad Social within 1 month** of notification (efficacy of the authorization is conditioned on it — currently already alta at Payfit; keep it uninterrupted).
11. **TIE at comisaría within 1 month of alta**: cita previa via ICPP (`icp.administracionelectronica.gob.es/icpplus`, Toledo offices), EX-17 + **790-012 €16,40** (paid there, not at filing). Bring resguardos + resolution.
12. **Renuncia expresa de TP** when applying for the new TIE (art. 24.1.d RD 1325/2003). Keep ALL resguardos (continuity proof for larga duración at the 5y mark, Nov 2027).

## Payment records (fill at payment — mirror in `_shared/procedures-tasas.md`)

| Tasa | Importe | Fecha pago | Nº resguardo | Paperless id |
|---|---|---|---|---|
| 790-052 ep. 2.5.2 | €10,94 | ___ | ___ | ___ |
| 790-062 (empleador, lo abona Oleksii) | €81,54 | ___ | ___ | ___ |
| 790-012 TIE (post-concesión, comisaría) | €16,40 | ___ | ___ | ___ |

## Human check (contract gate)

- [ ] Verify amounts at the tasación (tasas update annually — re-verify at payment).
- [ ] Verify EX-26 fields (especially órgano instructor = Toledo, notificaciones channel) before submitting.
- [ ] Oleksii performs the submission + payment personally (Cl@ve/cert + card).
- [ ] After submission: record número de registro + resguardos here and in `_meta/progress.md`.
