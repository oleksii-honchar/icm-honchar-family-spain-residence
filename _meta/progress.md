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
  - stage: "oleksii/03_documents:antecedentes-online-blocked"
    at: "2026-09-11"
    artifacts: ["_meta/progress.md", "members/oleksii/stages/01_profile/output/profile.md"]
    result: "BLOCKED — online antecedentes penales application via Justicia sede (sede.mjusticia.gob.es/tramites/certificado-antecedentes → Tramitación On-line con CL@VE) reached the application step, Cl@ve auth OK (OLEKSII HONCHAR), but the service REFUSED: «No es posible solicitar el certificado de manera telemática. El último TIE no está vigente. Le recomendamos acudir a una comisaría de la Dirección General de la Policía para subsanarlo.» Root cause hypothesis: Justicia system checks TIE validity against police registry; TIE card shows valid-until 04/03/2026 (auto-ext. to 04/03/2027 per Orden INT/96/2026 is NOT reflected in that registry). Online route terminal — human decision needed: (a) physical application at comisaría / Registro Central de Penados, (b) renew TIE first, (c) try again later if registry updated."
  - stage: "oleksii/03_documents:comisaria-route-investigation"
    at: "2026-09-11"
    artifacts: ["_meta/progress.md"]
    result: "RESEARCH — comisaría cita previa route fully mapped. citapreviadnie.es = DNI/pasaporte ONLY (no TIE/antecedentes trámites). Policía sede (sede.policia.gob.es) 'Antecedentes policiales' = PERPOL data-rights (acceso/supresión), NOT certificado de antecedentes penales. Extranjería trámites list + policia.es extranjería page: NO antecedentes penales service at comisaría. Official comisaría extranjería booking = ICPP (sede.administracionespublicas.gob.es/procedimientos/index/categoria/34 → icp.administracionelectronica.gob.es/icpplus). Toledo (p=45) offices: CNP Talavera (Carlos Barral 2), Jefatura Superior Toledo (Av. Portugal s/n), Oficina Extranjeros Toledo (Ronda Buenavista 57), Policía Toledo (Ronda Buenavista 57). Toledo Policía Nacional trámites: CERTIFICADOS CONCORDANCIA, RECOGIDA TIE, ASILO (expedición/solicitud), ASIGNACIÓN NIE, AUTORIZACIÓN REGRESO, CARTA INVITACIÓN, CERTIFICADO REGISTRO UE, CERTIFICADOS (residencia/no residencia/concordancia), TARJETA UCRANIA, TOMA DE HUELLAS (expedición TIE inicial/renovación/duplicado/Ley 14/2013). CONCLUSION: comisaría does NOT issue antecedentes penales — ministry's 'acudir a comisaría' = fix TIE registry (subsanación), then retry online Justicia. Relevant trámite: POLICÍA-TOMA DE HUELLAS (EXPEDICIÓN DE TARJETA) or CERTIFICADOS (residencia). Direct alternative: Registro Central de Penados (Madrid, C/ de la Mancha 2) in person / by mail."
  - stage: "oleksii/03_documents:justicia-presencial-route"
    at: "2026-09-11"
    artifacts: ["_meta/progress.md"]
    result: "RESEARCH — Justicia presencial channels for the certificado de antecedentes penales mapped (bypasses the TIE registry issue entirely; identity via NIE+passport, RCP search by NIE, no electronic TIE validation). Official cita previa systems: (1) Gerencias Territoriales → cita-previa.mjusticia.gob.es; (2) Oficina Central Atencion Ciudadano (C/ Bolsa 8, Madrid) → citaprevia.mjusticia.gob.es; (3) Registro Civil/Oficinas Judiciales → sedejudicial.justicia.es; (4) Registro Central de Penados (C/ de la Mancha 2, Madrid) in person / by mail (solicitud oficial + tasa 790 + NIE/passport copy). Certificate issued on the spot or within days. Phone 902 007 214 / 918 372 295 / 060. NOTE: mjusticia.gob.es info pages are JS-gated. CORRECTION: Gerencia de Justicia Castilla-La Mancha — DIR3 HQ = Av. Barber 42, 45005 Toledo; PUBLIC/cita office = C/ Periodista Campo Aguilar s/n, Albacete (tel 967 191 276, Mon-Fri 09:00-14:00 by cita only, gerencia.albacete@mjusticia.es). The online cita system lists only ‘TERRITORIAL ALBACETE’ for CLM (no Toledo option)."
  - stage: "oleksii/03_documents:justicia-cita-flow"
    at: "2026-09-11"
    artifacts: ["_meta/progress.md"]
    result: "IN PROGRESS — cita previa booking on cita-previa.mjusticia.gob.es via cloakbrowser (user-directed). Step 1: Centro = TERRITORIAL ALBACETE, Servicio = Certificado de Antecedentes Penales. Service info: tasa 790 = 3.86 €/certificate paid at any bank; identity doc in vigor = DNI/NIE/Passport/EU driving licence (Oleksii’s valid passport + NIE suffices — no valid TIE needed); if the certificate is for another public body they can consult data directly instead. Step 2 (fecha/hora): calendar shows Mon 14 — Fri 25 Sep 2026 (weekdays), hours 09:00-13:40; EARLIEST slot = Mon 14/09/2026. Checkbox ‘Dispongo de los documentos…’ ticked. BLOCKED awaiting human: (a) confirm location = ALBACETE (~237 km from Illescas by road, C/ Periodista Campo Aguilar s/n — the office, NOT Toledo), (b) chosen day+time, (c) phone number needed for the data step (NIE 0Z0166205N + name already on file). DISTANCE COMPARISON (road from Illescas, user-requested 2026-09-11): TERRITORIAL VALLADOLID is CLOSEST at 218.9 km ≈ 2h41m (Rome2Rio) — beats Albacete (236.9-237.7 km ≈ 2h54m) and Salamanca (~237.7 km); Zaragoza ~302 km (3h58). NOTE: 12:04 backend HTTP 500, 'No se pudo iniciar el gestor de citas previas' — Valladolid service-availability check pending retry."
  - stage: "oleksii/03_documents:antecedentes-rcp-route"
    at: "2026-09-11"
    artifacts: ["_shared/procedures-antecedentes-rcp.md", "_meta/progress.md"]
    result: "pass (decision + checklist) — HUMAN GATE: RCP Madrid presencial chosen as the route (Registro Central de Penados, C/ de la Mancha 2, 28045; solo 34.9-39.5 km / 35-40 min desde Illescas; identidad con pasaporte+NIE, sin TIE vigente; certificado el mismo día o en pocos días). Distancias rankeadas (carretera): Valladolid 218.9 km < Albacete ~237 ≈ Salamanca ~237.7 < Burgos 279 < Cáceres 282.2 < Zaragoza ~302. Checklist y procedimiento documentado en _shared/procedures-antecedentes-rcp.md."
  - stage: "oleksii/03_documents:antecedentes-verdict"
    at: "2026-09-11"
    artifacts: ["members/oleksii/stages/02_route/output/route.md", "_shared/procedures-antecedentes-rcp.md", "_meta/progress.md"]
    result: "RESEARCH (ES+UA sources) — is the SPANISH antecedentes certificate really needed? **NO** for the art. 191/EX-03 modification. RD 1155/2024 (BOE-A-2024-24099): «la oficina de extranjería recabará de oficio el informe del Registro Central de Penados para comprobar la inexistencia de antecedentes penales». Lawyer guide (Visal Immigration, 2026): for modifications you normally do NOT re-present the certificate — only if the office issues a requerimiento. UA resources (Instagram/dovidka.online): Ukrainian certificate needed mainly for arraigo/nacionalidad — NOT for art. 191 mod (consistent with prior art. 74.h finding). **RCP Madrid trip DOWNGRADED to CONTINGENCY** (only if SRU requerimiento, or for the future EX-11 larga duración dossier art. 177.3.f); do NOT print/pay the tasa for now."
  - stage: "oleksii/03_documents:autofirma-setup"
    at: "2026-09-11"
    artifacts: ["_shared/procedures-autofirma.md", "firmaelectronica.gob.es/descargas", "AF-manual-instalacion-usuarios-ES v1-9.pdf"]
    result: "pass (research) — AutoFirma for the EX-03 digital-signing step located and documented. Official source ONLY: firmaelectronica.gob.es/descargas → Autofirma64.zip (v1.9, Windows 64-bit = Win 11); installer bundles an OpenJDK JRE (leave 'Java Runtime Environment' checked — no separate Java needed on Windows; Linux-only requires Java 8+, OpenJDK 17 recommended). Manual PDF (oficial 1.9.0): EC-cert display on old Java 8/early 11 needs Java 17+ or recent 8/11; SmartScreen 'More info → Run anyway'. Cl@ve-only trámites do NOT need AutoFirma. Procedure doc written for the family (reusable)."

todo:
  - "oleksii/03_documents: verify last 3 payslips content (ids 163/165/160, Aug/Jul/Jun 2026) show €salary + period; locate missing 2026-04 payslip"
  - "oleksii/03_documents: check Mi carpeta/notificaciones for resolution of certificado 2026-E-RE-11414 (calendar reminder Mon 09-14) — save PDF when available"
  - "oleksii: confirm with ONG/lawyer that SEM 2/2026 TP-counting holds for larga duración (still open from route stage)"
  - "oleksii/03_documents: obtain antecedentes penales Espanya — ONLINE ROUTE BLOCKED 2026-09-11 (Justicia: «el último TIE no está vigente»; recommends comisaría de la DGP). Comisaría does NOT issue the certificate (ICPP Toledo cita = TIE subsanapolítica only). BEST route IN PROGRESS (now FALLBACK): cita previa online via cita-previa.mjusticia.gob.es (Centro = TERRITORIAL ALBACETE, Servicio = Certificado de Antecedentes Penales; office = C/ Periodista Campo Aguilar s/n, Albacete, ~237 km from Illescas; tasa 790 = 3,86 €; NIE/passport OK, no valid TIE needed). CLOSEST center check (12:00): TERRITORIAL VALLADOLID 218.8 km (~2h41) vs Albacete ~237 km (~2h54) — Salamanca ~237.7, Burgos 279, Cáceres 282.2, Zaragoza ~302. THEN SUPERSEDED (12:30): user chose RCP MADRID route instead — Madrid is only 34.9-39.5 km / ~35-41 min from Illescas (Himmera/ViaMichelin, 0 € tolls), far closer than any Gerencia. → 12:30 HUMAN GATE: user chose RCP MADRID PRESENCIAL (Registro Central de Penados, C/ de la Mancha 2, 28045 Madrid) — bring: solicitud (modelo oficial RCP) + tasa 790 modelo 006 = 3,86 € (paid at bank, stamped) + passport+NIE (originals + copies); certificate same visit or in a few days; call 060 / 902 007 214 / 918 372 295 to confirm horario before trip. → SUSPENDED 2026-09-11 (verdict: cert NOT required for the art. 191 mod — extranjería checks RCP de oficio; see route.md + procedures-antecedentes-rcp.md). RCP trip kept as CONTINGENCY: only if SRU requerimiento, or for the larga duración EX-11 dossier. Alternatives: RCP Madrid in person / by mail, Oficina Central (C/ Bolsa 8, Madrid), comisaría TIE subsanation → retry online — HUMAN DECISION REQUIRED"
  - "oleksii: verify exact 5-year mark from TIE card back / NIE resguardo"
  - "oleksii/04_filing: verify which form the art. 191 modification uses (EX-03 vs EX-99) + whether Mercurio-based"
  - "artem/02_route: write route analysis from @profile + @rules (art. 160 EX-25 now, EX-11 at ~16/12/2027); confirm exact NIE/TP start"
  - "yuliia/01_profile: stub awaiting bootstrap (not started)"
  - "artem: migrate the remaining 5 session artem scans (TIE 2022/2025, padrón 2022, birth cert, passport) into paperless — only Oleksii passport (id 166) confirmed added so far"
  - "oleksii/04_filing: download + install AutoFirma v1.9 on the Windows 11 machine (see _shared/procedures-autofirma.md) and test-sign a PDF before filing day — needed if the EX-03 sede asks 'firmar con certificado'; Cl@ve-only flow does NOT need it"
  - "oleksii/04_filing: DECIDE sign method for EX-03: (a) Cl@ve-only (no cert needed), or (b) FNMT Certificado de Ciudadano (free, needs NIE + passport, 100% online via vídeo-identificación or Cl@ve acreditación) — if (b), apply + install cert on Win 11 per _shared/procedures-autofirma.md (Camino A); import existing .pfx via Camino B"

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

notes: "Bootstrap 2026-09-05 (reconstruction pass: state file rewritten to match disk). Oleksii = pilot member; Artem/Yuliia = templates instantiated, profiles pending. Paperless ids sourced from prior session + search; current vida laboral + TIE scans not re-verified. 2026-09-11: passport (id 166), Payfit payslip series, Payfit contract (id 167), and current vida laboral (id 168, 1.341 días) confirmed in paperless via live search; padrón certificado RE-11414 pending resolution; TGSS domicile on file still Alicante (Garberí 11) — flagged in roster/profile."