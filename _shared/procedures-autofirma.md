# Procedure — AutoFirma (instalación Windows 11) para firma digital de trámites

> Needed for the digital signature step of the art. 191/EX-03 filing (and any other
> sede electrónica trámite that asks to "firmar con certificado"). AutoFirma is the
> official AGE signing tool — it must come ONLY from the official source below.

## Descarga (oficial, 2026-09-11 verificado)

Página oficial: **https://firmaelectronica.gob.es/descargas** → pestaña **AutoFirma**

| Sistema | Enlace directo oficial |
|---|---|
| **Windows 64 bits** (la mayoría de Windows 11) | https://firmaelectronica.gob.es/content/dam/firmaelectronica/descargas-software/autofirma19/Autofirma64.zip |
| Windows 32 bits | https://firmaelectronica.gob.es/content/dam/firmaelectronica/descargas-software/autofirma19/Autofirma32.zip |
| Versión anterior 1.8.3 (64 bits) | https://firmaelectronica.gob.es/content/dam/firmaelectronica/ciudadanos/descargas/windows/AutoFirma64_1_8_3_64.zip |
| Manual de instalación (1.9) | https://firmaelectronica.gob.es/content/dam/firmaelectronica/ciudadanos/descargas/pdf/AF-manual-instalacion-usuarios-ES%20v1-9.pdf |

> ⚠️ No descargar de sitios de terceros (autofirma.net, info-autofirma.es, etc.) —
> redirigen a veces a versiones alteradas. Usar SOLO firmaelectronica.gob.es.
> Los accesos directos `/descargas` son estables; los enlaces `/content/dam/...`
> pueden cambiar de versión — si fallan, volver a la página de descargas.

## Instalación (Windows 11, paso a paso)

1. **Verificar arquitectura**: Win 11 casi siempre es 64 bits (Ajustes → Sistema → Información).
2. Descargar **Autofirma64.zip** y **descomprimir** (clic derecho → Extraer todo).
3. Ejecutar el instalador **.exe** que hay dentro (Autofirma64_…exe).
   - Si SmartScreen avisa "Windows protegió su equipo" → **Más información → Ejecutar de todas formas**.
4. En el asistente, instalar el componente **"Java Runtime Environment"** (JRE de OpenJDK que el
   instalador copia junto a AutoFirma). **Dejar marcado** — así NO hace falta instalar Java aparte
   en Windows/macOS (el manual oficial: en Windows no es necesario un entorno Java separado;
   en Linux sí se requiere Java 8+ completo, recomendado OpenJDK 17).
5. Terminar el asistente. Comprobar que AutoFirma aparece en el menú Inicio.

## Uso (cuando una sede pida "firmar")

- Al iniciar un trámite que requiera firma con **certificado**, el navegador abre AutoFirma
  automáticamente; eliges el certificado (p. ej. certificado FNMT o DNIe) y la contraseña.
- Si el trámite usa solo **Cl@ve (PIN/Clave Permanente)**, NO se necesita AutoFirma.
- Plugin de Huella Digital (hash): solo si una sede lo pide expresamente; requiere AutoFirma v1.8+.
- AutoFirma lee los certificados del **almacén de Windows del usuario actual**
  (Certificados – Usuario actual → Personal) — no tienes que "importar" nada dentro de
  AutoFirma; solo hace falta que el certificado + clave privada estén en el almacén de Windows.

## Instalar el certificado (clave privada) en Windows 11

Para firmar con AutoFirma necesitas un **certificado digital con clave privada** instalado en
**Certificados — Usuario actual → Personal** (el almacén que consultan Windows, Chrome, Edge y
AutoFirma). Dos caminos:

### Camino A — Obtener el Certificado de Ciudadano de la FNMT (gratuito, con NIE)

Válido para españoles o **extranjeros con NIE** (caso Oleksii: NIE + pasaporte).
Fuente oficial: https://www.sede.fnmt.gob.es/certificados/persona-fisica

1. **Preparación (una sola vez)**: usa **Chrome o Edge** (usan el almacén de Windows);
   ten a mano **NIE + pasaporte** y un correo activo.
2. **Solicitar**: sede.fnmt.gob.es → Certificados → Persona Física → **Certificado de Ciudadano**
   → "Solicitar certificado" → introduce NIE, primer apellido (tal como consta), correo y país.
   El trámite genera un **código de solicitud** y te pide elegir contraseña de descarga.
3. **Acreditación de identidad** (elegir una):
   - **Vídeo identificación** — videollamada con un agente FNMT (100% online; disponible desde 2023).
   - **Acreditación telemática con Cl@ve** — si ya tienes Cl@ve, permite verificar sin desplazarte.
   - **Presencial en Oficina de Registro** — pedir cita (p. ej. oficinas de la Agencia Tributaria
     / INSS / FNMT); llevar NIE + pasaporte.
   Tras la acreditación recibes por correo el **código** para la descarga.
4. **Descargar e instalar** (en el MISMO equipo y MISMO usuario de Windows donde se solicitó):
   - Vuelve a la página de FNMT → "Descargar certificado".
   - Introduce NIF/NIE + primer apellido + código recibido por correo.
   - Acepta condiciones → pide la contraseña que indicaste en la solicitud → **marca "hacer copia
     de seguridad" (recomendado)**: guarda el archivo **.pfx** + contraseña en sitio seguro.
   - El sistema **instala el certificado automáticamente** en el almacén de Windows.
5. **Comprobar**: Chrome → Ajustes → Privacidad → Seguridad → Certificados, o `certmgr.msc` →
   Personal → Certificados → debe aparecer con icono de llave (clave privada asociada).
   Luego ya aparece en AutoFirma al firmar.

### Camino B — Importar una copia .pfx / .p12 existente (por ejemplo la "copia de seguridad")

1. Ten el archivo **.pfx/.p12** + su contraseña.
2. **Doble clic** en el archivo → Asistente de importación de certificados:
   - "Usuario actual" → Siguiente.
   - Introduce la contraseña → marca "Marcar esta clave como exportable" SOLO si vas a moverla
     otra vez a otro equipo (por defecto mejor dejarlo sin marcar).
   - "Seleccionar automáticamente el almacén de certificados" (quedará en **Personal**) → Finalizar.
3. Alternativa manual: `Win + R` → `certmgr.msc` → **Personal → Certificados** → clic derecho →
   Todas las tareas → Importar → mismo asistente.
4. **Verificar**: en `certmgr.msc` → Personal, el certificado debe mostrar la llave (clave privada);
   haz clic derecho → Todas las tareas → Administrar claves privadas si hiciera falta.

### Notas y trampas

- **Chrome y Edge usan el almacén de Windows**: si instalaste el certificado ahí, ya vale para ambos.
- **Firefox usa su propio almacén**: si descargaste con Firefox y no ves el certificado en AutoFirma,
  o repite la descarga con Chrome/Edge, o expórtalo desde Firefox (pestaña Certificados) e impórtalo
  como .pfx (Camino B).
- Instala el certificado **en el usuario de Windows que hará el trámite** (los almacenes de usuario
  no se comparten entre perfiles).
- **Nunca** subas el .pfx a conversores/webs de terceros; no guardes .pfx y contraseña juntos en el
  mismo sitio. Si olvidaste la contraseña de la copia, no hay recuperación — exporta de nuevo o pide
  un certificado nuevo.
- **DNIe no aplica** a Oleksii (es DNI español); para firmar con DNIe haría falta el lector + middleware.
- Si la sede de extranjería (EX-03) ofrece firma con **Cl@ve**, no necesitas certificado ninguno.

## Problemas conocidos (manual oficial 1.9)

- **No se muestran certificados de curva elíptica del almacén de Windows**: versiones antiguas de
  Java 8 y primeras de Java 11 no cargan certificados EC → ejecutar **Java 17+** (o al menos una
  versión reciente de Java 8/11).
- **"No se puede iniciar el gestor de citas/firma" / archivos bloqueados**: cerrar AutoFirma,
  reiniciar el equipo e intentar de nuevo; si la descarga quedó bloqueada por una ejecución previa,
  reinstalar.
- **SmartScreen/firewall**: permitir la ejecución la primera vez (ver paso 3).

## Registro (rellenar tras la instalación)

- Fecha instalación: ___
- Versión: 1.9 / 1.8.3 / ___
- Máquina: ___
- Prueba de firma sobre un PDF de prueba: hecha / pendiente

---
*Redactado 2026-09-11. Fuentes: firmaelectronica.gob.es/descargas (página oficial vigente) +
Manual de instalación AutoFirma 1.9.0 (PDF oficial, agost-2025).*