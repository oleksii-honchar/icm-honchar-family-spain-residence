# Track-Record State — progress.md
# ------------------------------------------------------------------
# CONVENTION (read before editing):
# - one minimal state file per workspace (this file)
# - READ on entry: answers "where are we, what's done, what's next"
# - UPDATE after every step before the human check
# - if MISSING or CORRUPTED: run Reconstruction Logic — re-derive
#   completed[]/current from outputs on disk, write, then proceed.
# ------------------------------------------------------------------

current: "oleksii/03_documents"

completed:
  - stage: "_bootstrap"
    at: "2026-09-05"
    artifacts: ["README.md", "AGENTS.md", "CONTEXT.md", "_shared/membership.md", "_shared/rules.md", "_shared/statuses.md", "_shared/sources.md", "_templates/member/**", "members/{oleksii,artem,yuliia}/**"]
    result: "pass — umbrella pipeline scaffolded; 3 member records instantiated from template (invariant 10)"
  - stage: "oleksii/01_profile"
    at: "2026-09-05"
    artifacts: ["members/oleksii/stages/01_profile/output/profile.md"]
    result: "pass — identity, TP/TIE chain, work history, padrón, doc table, GAPs; sources: prior research + paperless ids (TIE card not re-read → human check mandatory)"
  - stage: "oleksii/02_route"
    at: "2026-09-05"
    artifacts: ["members/oleksii/stages/02_route/output/route.md"]
    result: "pass (draft) — legal justification + citations: current SSL framework (RD 1155/2024 DA 19ª + RD 316/2026 + SEM 2/2026 + INT/96/2026 + (UE) 2026/1912), larga duración arts. 175-189 + art. 32 LOEX, route A (wait EX-11 2027) vs B (art. 191 now); recommendation B then A; 4 open questions. A-typical artefact path mistake during write (fixed)"
  - stage: "oleksii/02_route:verify-4y"
    at: "2026-09-10"
    artifacts: ["members/oleksii/stages/02_route/output/route.md", "_shared/rules.md", "_meta/progress.md"]
    result: "pass (research update) — user asked whether he can get a 4y permit now: CAN — art. 191.3 RD 1155/2024 grants a 4-year residencia y trabajo autorización for TP holders with AUTORIZA A TRABAJAR + ≥1y in a situation of residence (verified via Kagi: reglamento text, intergroupabogados, infomigrante; SEM 1/2026 same rule for humanitarian route). Route B now yields a 4-year permit (2026–2030), covering past the larga-duración mark. Updated route.md/rules.md/progress.md accordingly."
  - stage: "oleksii/02_route:legal-strategy"
    at: "2026-09-10"
    artifacts: ["members/oleksii/stages/02_route/output/route.md"]
    result: "pass (legal assessment added) — lawyer-style evaluation of Oleksii's 4-year case (art. 191 route), strengths, risks, requirements checklist, and step-by-step submission procedure. Added §2.4 and §2.5 to route.md."
  - stage: "oleksii/02_route:human-decision"
    at: "2026-09-10"
    artifacts: ["_meta/progress.md"]
    result: "pass (human decision made) — Oleksii chose Route B: file art. 191 modification now for 4-year residencia y trabajo permit (art. 191.3). Stage 02_route complete; advancing to 03_documents."
  - stage: "artem/01_profile"
    at: "2026-09-05"
    artifacts: ["members/artem/stages/01_profile/output/profile.md"]
    result: "pass — imported from archived session 260822-1627-residence-permit-artem (data-artem-family.json + notes.md): identity, TIE chain 12/2022 Alicante→11/04/2025 Toledo, padrón 16/12/2022 Alicante→15/01/2025 Illescas, passport valid, 8 GAPs incl. critical second-parent consent"
  - stage: "oleksii/03_documents:padron-volante"
    at: "2026-09-11"
    artifacts: ["_shared/procedures-padron.md"]
    result: "pass — volante de empadronamiento (colectivo) solicitado y registrado en la multi-Sede <illescas>: 2026-E-RE-11411 (11/09/2026 10:40), CSV instancia 59ESQQMRNHRCDHKCXFKHMYEWZ / CSV recibo AP6DJJR4XPCXPMWA4HNSPEDCJ. Procedimiento documentado en _shared/procedures-padron.md."
  - stage: "oleksii/03_documents:certificado-convivencia"
    at: "2026-09-11"
    artifacts: ["_shared/procedures-padron.md"]
    result: "pass (solicitud) — Certificado de convivencia o colectivo solicitado y registrado: 2026-E-RE-11414 (11/09/2026 10:45), CSV instancia 3Z6C6TEMHJ96F4Y5TJXC5EY9W / CSV recibo A3PYD5YKCJJYHA6Z7XW9C3SZX. NO inmediato (requiere firma de autoridades); pendiente de resolución — revisar notificaciones/Mi carpeta."
  - stage: "oleksii/03_documents:paperless-check-passport"
    at: "2026-09-11"
    artifacts: ["_shared/membership.md", "_shared/sources.md", "members/oleksii/stages/01_profile/output/profile.md"]
    result: "pass — Oleksii foreign passport CONFIRMED in paperless (id 166 'Honchar Foreign Passport', added by user 2026-09-11 11:44): PP GO229656, HONCHAR/OLEKSII, DOB 02/10/1979 (MRZ 791002), issued 21/05/2026 authority 2123, expiry 21/05/2036 (MRZ 360521 consistent). OCR transcription artifacts (verbatim 'May 2, 1979'/'Female') overridden by MRZ lines. Passport GAP closed for art. 191 dossier."
  - stage: "oleksii/03_documents:paperless-check-payfit-payslips"
    at: "2026-09-11"
    artifacts: ["_shared/membership.md", "_shared/sources.md"]
    result: "pass — Payfit payslip series found in paperless by live search (CORRECTS earlier claim 'zero Payfit nóminas in index' — workspace index was stale, live store has them): full 2025 series ids 99…88 (Jan–Dec, no gaps), 2026 ids 164(01),159(02),161(03),162(05),160(06),165(07),163(08). Last 3 payslips = 163 (08/2026), 165 (07/2026), 160 (06/2026) — closes payslip GAP. NOTE: 2026-04 (April) not found in index — suspicious, verify."
  - stage: "oleksii/03_documents:calendar-reminder"
    at: "2026-09-11"
    artifacts: ["_meta/progress.md"]
    result: "pass — Google Calendar reminder created (tuiteraz@gmail.com) Mon 2026-09-14 09:00 'Check padrón certificado 2026-E-RE-11414 (Mi carpeta/notificaciones)'. Event: https://www.google.com/calendar/event?eid=amthN3RuZjdwbG5wYXVoZ3NvbzBzcG1xcQ0gdHVpdGVyYXpAbQ"
  - stage: "oleksii/03_documents:paperless-check-payfit-contract"
    at: "2026-09-11"
    artifacts: ["_shared/membership.md", "_shared/sources.md", "members/oleksii/stages/01_profile/output/profile.md"]
    result: "pass — Payfit employment contract CONFIRMED in paperless (id 167 'PF RH - CDI 2024 - Oleksii Honchar 20_01_2025', added by user 2026-09-11 11:49): 16-page PDF, created 20/01/2025 (matches alta date), OCR shows CONTRATO DE TRABAJO, INDEFINIDO, Empresa/Trabajador, Senior Software role, salario base/retribución. Contract GAP closed for art. 191 dossier."
  - stage: "oleksii/03_documents:paperless-check-vida-laboral"
    at: "2026-09-11"
    artifacts: ["_shared/membership.md", "_shared/sources.md", "members/oleksii/stages/01_profile/output/profile.md"]
    result: "pass — current informe de vida laboral GENERATED + downloaded + registered in paperless (id 168 'vida_laboral_2026-09-11', 4 pages, added 12:12). Retrieved via Seguridad Social portal (portal.seg-social.gob.es — NOT SEPE; SEPE only covers prestaciones/desempleo). Data (TGSS 11/09/2026): NSS 031153181317, NIE 0Z0166205N, total alta 1.341 días = 3y 8m 3d. Situations: PAYFIT RECURSOS HUMANOS S.L. 20.01.2025→actualidad 600 días (TP 150%, gr. cotización 01); VACACIONES RETRIBUIDAS Taxfix 30.11–03.12.2024 (4d); VAC. DISEÑO GLOBAL 18.02–25.02.2023 (8d); PRESTACION DESEMPLEO.EXTINCIÓN 04.12.2024–19.01.2025 (47d); TAXFIX SPAIN 16.04.2023–29.11.2024 (594d); DISEÑO GLOBAL MERIDIANO 22.11.2022–17.02.2023 (88d). CEA GLZ3Z-RRYM5-QYLWA-SC2M4-6DZEH-QH6X5, verif. until 12/09/2028. Vida laboral GAP closed. ⚠️ Domicilio en SSG records: Av. Maestro José Garberí 11, 03540 ALICANTE (NOT Illescas) — data discrepancy to flag in dossier/membership."
  - stage: "oleksii/03_documents:brave-debug"
    at: "2026-09-11"
    artifacts: ["_meta/progress.md"]
    result: "info — used chrome-devtools MCP via Brave debug port 9222 (PID 25888, IPv4-only) to drive the Seguridad Social portal. Found: SEPE search/pages do NOT host vida laboral (SEPE=prestaciones/desempleo); the service lives at Seguridad Social (portal.seg-social.gob.es → Informes y Certificados → Informe de tu vida laboral). Auth: user completed Cl@ve manually (never automated). Tab workflow: SEPE tab 6 → Seguridad Social tab 8."

todo:
  - "oleksii/03_documents: verify last 3 payslips content (ids 163/165/160, Aug/Jul/Jun 2026) show €salary + period; locate missing 2026-04 payslip"
  - "oleksii/03_documents: check Mi carpeta/notificaciones for resolution of certificado 2026-E-RE-11414 (calendar reminder Mon 09-14) — save PDF when available"
  - "oleksii: confirm with ONG/lawyer that SEM 2/2026 TP-counting holds for larga duración (still open from route stage)"
  - "oleksii/03_documents: obtain antecedentes penales España (Sede del Gobierno) — only remaining doc GAP (vida laboral 2026 done, id 168)"
  - "oleksii: verify exact 5-year mark from TIE card back / NIE resguardo"
  - "oleksii/04_filing: verify which form the art. 191 modification uses (EX-03 vs EX-99) + whether Mercurio-based"
  - "artem/02_route: write route analysis from @profile + @rules (art. 160 EX-25 now, EX-11 at ~16/12/2027); confirm exact NIE/TP start"
  - "yuliia/01_profile: stub awaiting bootstrap (not started)"
  - "artem: migrate the remaining 5 session artem scans (TIE 2022/2025, padrón 2022, birth cert, passport) into paperless — only Oleksii passport (id 166) confirmed added so far"

decisions:
  - what: "Workspace shape = umbrella pipeline; each family member = record with identical 5-stage pipeline"
    why: "3 members share one legal framework but independent timelines; invariants 5/10 (factory + copy)"
    at: "2026-09-05"
  - what: "Route framework from Artem research (2026-08-22): TP → ordinary residence (art. 160 EX-25 minor / work-route) now, larga duración nacional at 5y mark (TP time counts per SEM 2/2026)"
    why: "Precedent research; SEM 2/2026 counted toward larga duración nacional"
    at: "2026-09-05"
  - what: "Oleksii's route question deferred to human: he already AUTORIZA A TRABAJAR under TP and hits 5 years Nov-2027 — whether to file now (EX-25 work route) or wait for larga duración (EX-11)"
    why: "TP-holder transition strategy not settled; SEM 2/2026 is an instruction, not settled law → ONG/lawyer confirmation required"
    at: "2026-09-05"
  - what: "Oleksii Route Decision: B — file art. 191 modification now for 4-year residencia y trabajo permit"
    why: "Human (Oleksii) chose B after lawyer-style legal assessment presented; route updated with legal strategy, checklist, submission procedure"
    at: "2026-09-10"
  - what: "Ukrainian criminal record certificate NOT required for art. 191 modification"
    why: "Verified against consolidated BOE text (BOE-A-2024-24099): art. 74.h) requires only «inexistencia de antecedentes penales en España» — foreign certificates not required for art. 191 modifications. Ukrainian cert will be needed later for EX-11 larga duración (art. 177.3.f)."
    at: "2026-09-10"
  - what: "Paperless search is the source of truth for doc GAPs — re-verify via MCP before declaring missing"
    why: "Workspace roster index (generated 2026-09-05) missed user-added doc id 166 and the full Payfit series; declaring GAPs 'not in paperless' without a live search was wrong. Lesson recorded."
    at: "2026-09-11"
  - what: "Always persist progress into workspace project files as I go"
    why: "User instructed: 'always track progress in project' — state lives in files (progress.md + roster + profile + route), not in conversation"
    at: "2026-09-11"
  - what: "Google Calendar used for the 09-14 padrón recheck reminder (user requested)"
    why: "Authorized reminder channel; event created via google_workspace MCP — linked above"
    at: "2026-09-11"

notes: "Bootstrap 2026-09-05 (reconstruction pass: state file rewritten to match disk). Oleksii = pilot member; Artem/Yuliia = templates instantiated, profiles pending. Paperless ids sourced from prior session + search; current vida laboral + TIE scans not re-verified. 2026-09-11: passport (id 166), Payfit payslip series, and Payfit contract (id 167) confirmed in paperless via live search; padrón certificado RE-11414 pending resolution."