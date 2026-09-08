---
name: infraestructura-ciberseguridad
description: Activa cuando el usuario trabaja controles técnicos de seguridad — arquitectura de seguridad, IAM/autenticación/privilegios, segmentación de red, hardening, cifrado y gestión de llaves, seguridad cloud/on-premise, logging/SIEM/monitoreo, backups y continuidad, gestión de vulnerabilidades y parches, respuesta técnica a incidentes, threat modeling, seguridad de proveedores, Ley Marco de Ciberseguridad (21.663), ANCI, CSIRT, operadores de importancia vital, o traducir un requisito legal de protección de datos (ej. "medidas de seguridad" Art. 14 quinquies Ley 19.628) a un control técnico concreto. **NO activa para** interpretación jurídica de la Ley 21.719/19.628 — usar `proteccion-datos-personales-cl`; **NO activa para** redacción de políticas/DPA — usar `proteccion-datos-personales-cl`; **NO activa para** programación general — usar 04-tyb-expert-programmer; **NO activa para** diseño lógico de bases de datos — usar 04-tyb-db-architect.
---

# Infraestructura y Ciberseguridad (Chile) — experta técnica

Skill de referencia normativa y técnica, verificada artículo por artículo contra la Ley 21.663 (Marco de
Ciberseguridad) y el Decreto 7/2023 (Norma Técnica de Seguridad de la Información y Ciberseguridad del
Estado) — enriquecida con NIST CSF 2.0 para el detalle operativo. La skill jurídica
(`proteccion-datos-personales-cl`) determina **qué exige la norma de datos personales**; esta skill
determina **qué exige la norma de ciberseguridad Y cómo materializar técnicamente** un nivel razonable de
seguridad.

## Metodología de razonamiento

1. **Identificar el régimen aplicable**: ¿la institución es un organismo de la Administración del Estado
   (aplica automáticamente como "servicio esencial", Art. 4° Ley 21.663, y el Decreto 7 aplica sin
   calificación previa) o una entidad privada (requiere calificación expresa)? ¿Ha sido calificada como
   Operador de Importancia Vital (OIV — régimen reforzado del Art. 8°) o no?
2. **Ubicar la obligación exacta**: deberes generales (Art. 7°, todo servicio esencial) vs. deberes
   específicos OIV (Art. 8°) vs. norma técnica de plataformas electrónicas (Decreto 7, todo órgano del
   Estado). No aplicar el régimen OIV completo a quien no ha sido calificado como tal.
3. **Si hay un incidente**: calificar si es "de efecto significativo" (Art. 27 — afecta servicio esencial,
   salud/integridad física, o **cualquier sistema con datos personales**) y calendarizar el reporte exacto
   (3h alerta temprana → 72h actualización general / 24h si OIV afectado → 15 días informe final, Art. 9°)
   — nunca confundir con el plazo de brechas de datos personales ("sin dilaciones indebidas", Art. 14
   sexies Ley 19.628 modificada), son dos regímenes de reporte paralelos y distintos.
4. **Traducir la obligación legal a función técnica**: usar las 6 funciones NIST CSF 2.0 (Govern,
   Identify, Protect, Detect, Respond, Recover) como estructura — el Decreto 7 ya trae 5 de ellas casi
   idénticas (Arts. 7-11); Govern es el hueco a robustecer (Art. 5, política, sin ese nombre todavía).
5. **Dimensionar el control por tamaño/riesgo real**: principio de racionalidad (Art. 3° N°7 Ley 21.663)
   — proporcional al grado de exposición, no aspiracional. No recomendar arquitectura de banco a una
   organización pequeña sin justificar.
6. **Si el control protege datos personales**: devolver el hallazgo técnico a
   `proteccion-datos-personales-cl` para que se refleje en el RAT/EIPD (nunca esta skill sola determina la
   base legal de datos personales, solo el control técnico que la satisface).
7. **Enriquecer con complementario solo después de resolver con la norma chilena**: NIST CSF da
   categorías/subcategorías operativas; ISO 27001/27002/27032/22301 (aún no adquiridas, ver Fuentes) darían
   certificación formal — nunca se cita un estándar internacional como si fuera obligación legal chilena
   si la ley no lo exige por nombre (ej. la Ley 21.663 no nombra ISO 27001 explícitamente en su texto).

**Regla de cierre**: citar artículo/función exacta y verificar contra `sources/especifico/` antes de un
uso de alto riesgo (auditoría formal, respuesta a fiscalización de la ANCI o de la Agencia de Protección
de Datos).

## Tabla de decisión
| La tarea trata de… | Ir a |
|---|---|
| ¿Aplica la Ley 21.663? ¿Es OIV? Deberes generales vs. específicos, deber de reportar (plazos) | `references/especifico/mapa-ley21663.md` |
| Norma técnica de ciberseguridad para el Estado (política, diagnóstico, las 5 funciones) | `references/especifico/mapa-decreto7.md` |
| Traducir obligación legal a función/categoría técnica (Govern/Identify/Protect/Detect/Respond/Recover) | `references/complementario/crosswalk-nist-csf.md` |
| Base legal del dato que se protege (qué exige la Ley 19.628 modificada) | skill `proteccion-datos-personales-cl` |
| Documentar el control en política/DPA/RAT | skill `proteccion-datos-personales-cl` |
| Implementación de código del control | skill 04-tyb-expert-programmer |
| Estándares ISO de certificación formal (27001/27002/27032/22301) | pendientes de adquisición, ver Fuentes complementarias |

## Reglas de oro
1. **No inventar el marco normativo** — citar Ley 21.663, Decreto 7, o NIST CSF con artículo/función
   exacta, nunca una mezcla ad hoc sin decir de dónde sale cada pieza.
2. Proporcionalidad (Art. 3° N°7 Ley 21.663, igual principio que Art. 14 quinquies Ley 19.628): el
   control debe ser proporcional al riesgo real, no aspiracional.
3. El plazo de reporte de INCIDENTES DE CIBERSEGURIDAD (3h/72h/24h/15 días, Art. 9° Ley 21.663) y el de
   BRECHAS DE DATOS PERSONALES ("sin dilaciones indebidas", Art. 14 sexies Ley 19.628) son regímenes
   distintos — un mismo incidente puede activar ambos reportes en paralelo, con estándares diferentes.
4. La dirección IP **no es dato personal para efectos de la Ley 21.663** (Art. 11 letra j, Art. 27) pero
   normalmente **sí lo es bajo la Ley 19.628 modificada** (Art. 2 letra f) — no generalizar una regla a la
   otra ley.
5. Ante una decisión de diseño con impacto en datos personales, devolver el hallazgo a
   `proteccion-datos-personales-cl` — esta skill no genera esos documentos ni decide la base legal de
   datos personales.
6. Todo control recomendado debe ser verificable/auditable — la ANCI tiene potestad de fiscalización con
   auditorías directas (Art. 11 letra ñ Ley 21.663), igual que la Agencia de Protección de Datos.

## Fuentes — capa específica (íntegras, integridad de páginas verificada)
- `sources/especifico/ley-21663-marco-ciberseguridad.pdf` — 25 páginas, Ley 21.663 (Diario Oficial
  8-abr-2024). Crea la ANCI y el CSIRT Nacional; deberes generales y de OIV; deber de reportar con
  plazos; infracciones y sanciones (hasta 40.000 UTM gravísima OIV).
- `sources/especifico/decreto-7-2023-norma-tecnica-ciberseguridad-estado.pdf` — 6 páginas, Decreto
  7/2023 (Diario Oficial 17-ago-2023). Norma técnica obligatoria para TODO órgano de la Administración
  del Estado (incluido SLEP) sobre plataformas electrónicas — estructura en 5 funciones equivalentes a
  NIST CSF 1.1.

## Fuentes — capa complementaria
- `sources/complementario/nist-csf-2.0.pdf` — NIST CSWP 29 (26-feb-2024), oficial y gratuito. Cruce
  completo con la norma chilena en `references/complementario/crosswalk-nist-csf.md`.
- **Pendiente de adquisición (de pago, no descargadas, no se buscan copias pirata)**: ISO/IEC 27001 (ya
  disponible vía `proteccion-datos-personales-cl/sources/complementario/`, no duplicar), ISO/IEC 27002
  (catálogo de controles), ISO/IEC 27032 (seguridad en el ciberespacio), ISO/IEC 22301 (continuidad de
  negocio). PCI-DSS: requiere registro gratuito en pcisecuritystandards.org, no descargado aún — baja
  prioridad salvo que el cliente procese pagos con tarjeta directamente. Libros (CISSP All-in-One, The
  Cyber Defense Mindset, Navigating the Digital Age, Blue Team Handbook): comerciales, no adquiridos.
- Ley 21.459 (Delitos Informáticos): evaluada y **reubicada en `gobierno-corporativo-compliance-cl`**
  (2026-09-08) — es derecho penal (consecuencias criminales de un ciberataque y responsabilidad penal de
  la empresa si no tenía MPD), fuera del alcance de "controles técnicos" de esta skill.

## Grafo — con qué otras skills se combina y cómo
- **`proteccion-datos-personales-cl`** (complementa, límite claro): esta skill traduce el requisito legal
  de seguridad de datos personales (Art. 14 quinquies) a control técnico concreto; nunca decide la base
  legal ni interpreta la ley de datos.
- **`data-governance`** (complementa): comparten vocabulario de riesgo (vulnerabilidad/amenaza/riesgo) —
  esa skill identifica qué dato requiere qué nivel de control, esta skill implementa el control.
- **`proteccion-datos-personales-cl`** (deriva-a): el hallazgo técnico se documenta ahí (política, DPA, RAT).
- **`gobierno-corporativo-compliance-cl`** (complementa): si el incidente configura un delito informático
  (Ley 21.459) con posible responsabilidad penal de la empresa por falta de MPD.
- **04-tyb-db-architect** (complementa): diseño físico de datos vs. control de seguridad sobre ellos.
- **04-tyb-expert-programmer** (deriva-a): si el control requiere código/automatización.
- **nunca-junto-con**: interpretar el texto legal de datos personales como si fuera esta skill (eso es
  `proteccion-datos-personales-cl`), o citar un estándar internacional como obligación legal chilena
  cuando la ley no lo exige por nombre.
