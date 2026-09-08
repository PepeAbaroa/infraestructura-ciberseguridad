# Cruce NIST CSF 2.0 ↔ Decreto 7 ↔ Ley 21.663 — la norma chilena manda, NIST aterriza la implementación

> **Jerarquía (contrato v3, igual que en `proteccion-datos-personales-cl`):** el Decreto 7 y la Ley 21.663
> son la obligación legal en Chile — NIST CSF 2.0 no es ley chilena, no crea obligación nueva. Su función
> aquí es dar el detalle operativo (categorías, subcategorías, buenas prácticas) que la norma chilena
> delega a "guías técnicas" todavía genéricas. Fuente: `sources/complementario/nist-csf-2.0.pdf`
> (NIST CSWP 29, 26-feb-2024, oficial y gratuito).

## Las 6 funciones de NIST CSF 2.0

> **TEXTO LITERAL** (`sources/complementario/nist-csf-2.0.pdf.extracto/chunk_007.md`-`chunk_008.md`)
> "GOVERN (GV) — The organization's cybersecurity risk management strategy, expectations, and policy are
> established, communicated, and monitored. [...] GOVERN is in the center of the wheel because it informs
> how an organization will implement the other five Functions. IDENTIFY (ID) — The organization's current
> cybersecurity risks are understood. [...] PROTECT (PR) — Safeguards to manage the organization's
> cybersecurity risks are used. [...] identity management, authentication, and access control; awareness
> and training; data security; platform security [...] DETECT (DE) — Possible cybersecurity attacks and
> compromises are found and analyzed. [...] RESPOND (RS) — Actions regarding a detected cybersecurity
> incident are taken. [...] incident management, analysis, mitigation, reporting, and communication.
> RECOVER (RC) — Assets and operations affected by a cybersecurity incident are restored."

## Tabla de cruce — dónde vive cada función en la norma chilena

| Función NIST CSF 2.0 | Decreto 7 (norma técnica Estado) | Ley 21.663 |
|---|---|---|
| **GOVERN** — estrategia, roles, políticas | Art. 5 (Política de Seguridad, roles obligatorios: responsable institucional + responsable de activos) — **cobertura parcial, sin la etiqueta "Govern"** (el decreto es de 2023, pre-CSF 2.0 de 2024) | Art. 3 (principio de racionalidad/proporcionalidad), Art. 8 letra i) (delegado de ciberseguridad, solo OIV) |
| **IDENTIFY** | Art. 4 (diagnóstico inicial, catálogo de plataformas) + Art. 7 (función de identificación: contexto, gobernanza, activos, riesgos, proveedores cloud) | Art. 8 letra a) (SGSI continuo — determinar riesgos, solo OIV) |
| **PROTECT** | Art. 8 (servidores, redes, autenticación, control de acceso, concienciación, seguridad de datos, registro de eventos) | Art. 3 N°8 (seguridad y privacidad desde el diseño) |
| **DETECT** | Art. 9 (análisis de eventos, monitoreo continuo, código malicioso) | Art. 8 letra d) (revisión/ejercicios/simulacros, solo OIV) |
| **RESPOND** | Art. 10 (planificación de respuesta, comunicación, análisis y mitigación de incidentes) | Art. 9 (deber de reportar: 3h/72h/24h/15 días) + Art. 8 letra e) (medidas para reducir impacto, solo OIV) |
| **RECOVER** | Art. 11 (planificación de recuperación, comunicación del estado) | Art. 8 letra c) (planes de continuidad operacional, solo OIV) |

**Razonamiento aplicado:** el Decreto 7 ya trae 5 de las 6 funciones estructuradas casi idénticamente a
NIST CSF (verificado en `mapa-decreto7.md`) — el trabajo real de esta skill para un SLEP no es "inventar"
un marco, es llenar cada función del Decreto 7 con el detalle de categorías/subcategorías que NIST CSF sí
desarrolla y que las guías técnicas chilenas (Art. 12 Decreto 7) aún no han publicado con ese nivel de
detalle. La función GOVERN es el hueco real: el Decreto 7 (2023) no la nombra como función propia — el
Art. 5 cubre roles y política, pero sin el desarrollo de categorías (contexto organizacional, estrategia
de gestión de riesgo de la cadena de suministro, supervisión) que sí trae NIST CSF 2.0 (2024). Para un
SLEP que quiera adelantarse, usar GOVERN de NIST CSF para robustecer el Art. 5 antes de que una futura
actualización del Decreto 7 lo exija.

## Categorías de GOVERN (el hueco identificado) — detalle para robustecer el Art. 5

> **TEXTO LITERAL** (`chunk_007.md`) "GOVERN addresses an understanding of organizational context; the
> establishment of cybersecurity strategy and cybersecurity supply chain risk management; roles,
> responsibilities, and authorities; policy; and the oversight of cybersecurity strategy."

**Razonamiento aplicado:** 5 elementos que la Política de Seguridad (Decreto 7 Art. 5) de un SLEP debería
incorporar aunque el decreto no los exija por nombre todavía: (1) contexto organizacional (qué tipo de
entidad es, qué datos/activos maneja), (2) estrategia de riesgo de **cadena de suministro** —
particularmente relevante para contratos con proveedores cloud (Microsoft, Google) ya identificados como
pendientes en `proteccion-datos-personales-cl`, (3) roles/responsabilidades/autoridades (ya exigido, Art.
5 N°4), (4) política (ya exigida), (5) supervisión activa de la estrategia — el elemento que más
frecuentemente falta en la práctica (se escribe la política, no se supervisa su cumplimiento).

## Vínculo con las obligaciones de reporte de la Ley 21.663 (función RESPOND)

**Razonamiento aplicado:** NIST CSF define RESPOND como función continua de "incident management,
analysis, mitigation, reporting, and communication" — la Ley 21.663 la concreta con plazos exactos (Art.
9: 3h/72h u 24h/15 días, ver `mapa-ley21663.md`). Un plan de respuesta a incidentes construido sobre NIST
CSF sin calendarizar esos plazos exactos de la ley chilena estaría incompleto para efectos de
cumplimiento legal — NIST da la estructura, la ley da el cronograma obligatorio.

## Grafo
Se combina con `mapa-ley21663.md` y `mapa-decreto7.md` (ambos en `references/especifico/`). Ver
`## Grafo` en `SKILL.md` para la relación con otras skills.
