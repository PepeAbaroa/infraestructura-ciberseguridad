# Mapa de artículos — Ley 21.663, Marco de Ciberseguridad

> Verificado contra `sources/especifico/ley-21663-marco-ciberseguridad.pdf` (Diario Oficial N°43.820,
> 8-abr-2024, 25/25 páginas íntegras, Ministerio del Interior y Seguridad Pública). Crea la Agencia
> Nacional de Ciberseguridad (ANCI) y el CSIRT Nacional; define Servicios Esenciales y Operadores de
> Importancia Vital (OIV); fija deberes de ciberseguridad, deber de reporte de incidentes con plazos
> concretos, y régimen de infracciones y sanciones.
>
> **Formato**: `TEXTO LITERAL` (cita exacta) + `Razonamiento aplicado` (interpretación, nunca mezclado).
> Tratamiento completo para los Títulos I, II, III (Párrafos 1-2 y 5), IV, VII — que son los operativos
> para un organismo público como un SLEP; tratamiento más liviano para el resto (estructura interna del
> Consejo de la Agencia, Red de Conectividad Segura del Estado, CSIRT de la Defensa Nacional).

## Título I — Disposiciones generales (Arts. 1-3)

### Artículo 1° — Objeto y ámbito subjetivo
> **TEXTO LITERAL** (Art. 1°, líneas 34-47)
> "La presente ley tiene por objeto establecer la institucionalidad, los principios y la normativa general
> que permitan estructurar, regular y coordinar las acciones de ciberseguridad de los organismos del
> Estado y entre éstos y los particulares [...] Para efectos de esta ley, la Administración del Estado
> estará constituida por los Ministerios, las Delegaciones Presidenciales Regionales y Provinciales, los
> Gobiernos Regionales, las Municipalidades, las Fuerzas Armadas, las Fuerzas de Orden y Seguridad
> Pública, las empresas públicas creadas por ley, y **los órganos y servicios públicos creados para el
> cumplimiento de la función administrativa**."

**Razonamiento aplicado:** un SLEP, como servicio público, encaja directamente en "órganos y servicios
públicos creados para el cumplimiento de la función administrativa" — la ley le aplica de pleno derecho
desde el Art. 1°, sin necesidad de calificación especial adicional (ver Art. 4° más abajo, que confirma
que los organismos de la Administración del Estado son "servicio esencial" por definición).

### Artículo 2° — Definiciones clave
> **TEXTO LITERAL** (Art. 2°, líneas 51-65 y página 2)
> "6. Ciberseguridad: preservación de la confidencialidad e integridad de la información y de la
> disponibilidad y resiliencia de las redes y sistemas informáticos [...] 9. Equipo de Respuesta a
> Incidentes de Seguridad Informática o CSIRT: centros multidisciplinarios que tienen por objeto
> prevenir, detectar, gestionar y responder a incidentes de ciberseguridad [...] 10. Incidente de
> ciberseguridad: todo evento que perjudique o comprometa la confidencialidad o integridad de la
> información, la disponibilidad o resiliencia de las redes y sistemas informáticos, o la autenticación de
> los procesos [...] 13. Resiliencia: capacidad de las redes y sistemas informáticos para seguir operando
> luego de un incidente de ciberseguridad, aunque sea en un estado degradado [...] 14. Riesgo: posibilidad
> de ocurrencia de un incidente de ciberseguridad; la magnitud de un riesgo es cuantificada en términos de
> la probabilidad de ocurrencia del incidente y del impacto de las consecuencias del mismo. 15.
> Vulnerabilidad: debilidad de un activo o control que puede ser explotado por una o más amenazas
> informáticas."

**Razonamiento aplicado:** vocabulario prácticamente idéntico al del DAMA-DMBOK Cap. 7 (`data-governance`)
— vulnerabilidad ≠ amenaza ≠ riesgo, y riesgo = función de probabilidad × impacto — confirma que las 3
skills (esta, `data-governance`, `proteccion-datos-personales-cl`) deberían auditar riesgo con el mismo
vocabulario y, cuando sea el mismo hecho, la misma matriz, no tres por separado.

### Artículo 3° — Principios rectores
> **TEXTO LITERAL** (Art. 3° N°7-8, página 3)
> "7. Principio de racionalidad: las medidas para la gestión de incidentes de ciberseguridad, las
> obligaciones de ciberseguridad y el ejercicio de las facultades de la Agencia deberán ser necesarias y
> proporcionales al grado de exposición a los riesgos, y al eventual impacto social y económico. 8.
> Principio de seguridad y privacidad por defecto y desde el diseño: los sistemas informáticos,
> aplicaciones y tecnologías de la información deben diseñarse, implementarse y gestionarse teniendo en
> cuenta la seguridad y la privacidad de los datos personales que procesan."

**Razonamiento aplicado:** el principio N°8 es el mismo "privacy/security by design" del Art. 14 quáter de
la Ley 19.628 modificada (ver `proteccion-datos-personales-cl/references/complementario/privacy-by-design-accountability.md`)
— confirmado ahora también como principio rector propio de la ley de ciberseguridad, no solo de la ley de
datos personales. El principio N°7 (racionalidad/proporcionalidad) es la misma regla de oro ya aplicada
en esta skill antes de esta reconstrucción: no recomendar controles de nivel banco a una organización
pequeña sin justificar por qué.

## Título II §1 — Servicios esenciales y Operadores de Importancia Vital (Arts. 4-6)

### Artículo 4° — Ámbito de aplicación / servicios esenciales
> **TEXTO LITERAL** (Art. 4°, página 3)
> "Son servicios esenciales aquellos provistos por **los organismos de la Administración del Estado** y
> por el Coordinador Eléctrico Nacional; los prestados bajo concesión de servicio público, y los
> proveídos por instituciones privadas que realicen las siguientes actividades: [...] telecomunicaciones;
> infraestructura digital; servicios digitales y servicios de tecnología de la información gestionados por
> terceros [...]"

**Razonamiento aplicado — confirma el punto más importante para SLEP**: un organismo de la Administración
del Estado es servicio esencial **por el solo hecho de serlo**, sin necesidad de una calificación especial
adicional — a diferencia de las instituciones privadas, que sí requieren un acto de calificación de la
Agencia. Un SLEP queda sujeto a las obligaciones del Art. 8° (ver abajo) desde la entrada en vigencia de
la ley, no desde que la Agencia dicte una resolución particular.

### Artículo 5° — Operadores de Importancia Vital (OIV)
> **TEXTO LITERAL** (Art. 5°, página 3)
> "La Agencia podrá calificar como operadores de importancia vital a quienes reúnan los siguientes
> requisitos: 1. Que la provisión de dicho servicio dependa de las redes y sistemas informáticos, y 2. Que
> la afectación, interceptación, interrupción o destrucción de sus servicios tenga un impacto significativo
> en la seguridad y el orden público, en la provisión continua y regular de servicios esenciales, en el
> efectivo cumplimiento de las funciones del Estado [...]"

**Razonamiento aplicado:** ser "servicio esencial" (automático para un SLEP) NO es lo mismo que ser "OIV"
(requiere calificación expresa de la Agencia, Art. 6°) — el régimen de obligaciones reforzadas del Art. 8°
solo aplica de lleno a quien sea calificado OIV. Un SLEP debe verificar activamente si ha sido calificado
como OIV (poco probable salvo que administre infraestructura crítica específica) antes de asumir que le
aplica el régimen más estricto — aunque igual le aplican los deberes generales del Art. 7°.

## Título II §2 — Obligaciones de ciberseguridad (Arts. 7-9)

### Artículo 7° — Deberes generales
> **TEXTO LITERAL** (Art. 7°, página 4)
> "Las instituciones obligadas por la presente ley deberán aplicar de manera permanente las medidas para
> prevenir, reportar y resolver incidentes de ciberseguridad. Estas medidas podrán ser de naturaleza
> tecnológica, organizacional, física o informativa [...] La Agencia deberá establecer medidas de
> seguridad diferenciadas según el tipo de organización de que se trate, teniendo especialmente en
> consideración las características y posibilidades de las pequeñas y medianas empresas [...]"

**Razonamiento aplicado:** deber general aplicable a TODO servicio esencial (incluido un SLEP no
calificado OIV) — el estándar es diferenciado por tamaño/tipo de organización, mismo principio de
proporcionalidad ya citado (Art. 3° N°7).

### Artículo 8° — Deberes específicos de los OIV
> **TEXTO LITERAL** (Art. 8°, página 5, letras clave)
> "a) Implementar un sistema de gestión de seguridad de la información continuo con el fin de determinar
> aquellos riesgos que puedan afectar la seguridad de las redes, sistemas informáticos y datos, y la
> continuidad operacional del servicio [...] c) Elaborar e implementar planes de continuidad operacional y
> ciberseguridad, los cuales deberán certificarse en conformidad al artículo 28, y someterse a revisiones
> periódicas [...] con una frecuencia mínima de dos años. [...] i) Designar un delegado de ciberseguridad,
> quien actuará como contraparte de la Agencia e informará a la autoridad o jefatura o jefe superior del
> órgano o servicio de la Administración del Estado [...]"

**Razonamiento aplicado:** letra (a) exige un "sistema de gestión de seguridad de la información continuo"
(SGSI) — **la ley NO nombra ISO/IEC 27001 explícitamente en el texto**; es el reglamento y la práctica de
la industria los que hacen de ISO 27001 el marco de facto para satisfacer esta obligación (tu
investigación tenía razón en el vínculo práctico, pero la cita textual de la ley es más genérica — no
sobre-citar ISO 27001 como si la ley la exigiera por nombre). La letra (i) crea la figura del **delegado
de ciberseguridad** — análogo funcional al DPO de `proteccion-datos-personales-cl`, pero de una materia
distinta; nada impide que sea la misma persona si el organismo lo decide, pero son designaciones legales
separadas.

### Artículo 9° — Deber de reportar (plazos operativos críticos)
> **TEXTO LITERAL** (Art. 9°, páginas 5-6)
> "a) Dentro del plazo máximo de **tres horas** contado desde que se tiene conocimiento de la ocurrencia
> del ciberataque o incidente [...] se deberá enviar una alerta temprana [...] b) Dentro del plazo máximo
> de **setenta y dos horas**, una actualización [...] Sin embargo, en caso de que la institución afectada
> fuera un operador de importancia vital y éste viera afectada la prestación de sus servicios esenciales a
> causa del incidente, la actualización [...] deberá entregarse [...] en el plazo máximo de **veinticuatro
> horas** [...] c) Dentro del plazo máximo de **quince días corridos** contado desde el envío de la alerta
> temprana [...] un informe final [...]"

**Razonamiento aplicado — cadena de plazos que todo protocolo de respuesta a incidentes de un SLEP debe
tener calendarizada**: 3 horas (alerta temprana) → 72 horas general / 24 horas si OIV afectado
(actualización) → 15 días corridos (informe final). Esto es lo que hace que "72 horas" SÍ sea el estándar
correcto a citar en materia de **ciberseguridad** (Ley 21.663) — a diferencia de brechas de **datos
personales** (Ley 19.628 modificada, Art. 14 sexies), donde el estándar es "sin dilaciones indebidas", sin
plazo fijo. **No confundir ambos regímenes**: un mismo incidente que compromete datos personales puede
activar AMBOS reportes en paralelo (a la Agencia de Protección de Datos y al CSIRT Nacional), con
estándares de plazo distintos.

## Título III — Agencia Nacional de Ciberseguridad y CSIRT Nacional (tratamiento operativo; estructura interna del Consejo Directivo se omite por ser de bajo interés práctico para un organismo regulado)

### Artículo 10-11 — Creación y atribuciones de la ANCI
> **TEXTO LITERAL** (Art. 10-11, páginas 6-7)
> "Créase la Agencia Nacional de Ciberseguridad como un servicio público funcionalmente descentralizado
> [...] cuyo objeto será asesorar al Presidente de la República en materias propias de ciberseguridad [...]
> y coordinar y supervisar la acción de los organismos de la Administración del Estado en materia de
> ciberseguridad. [...] Atribuciones: [...] f) Crear y administrar un Registro Nacional de Incidentes de
> Ciberseguridad. [...] ñ) Fiscalizar el cumplimiento de las disposiciones de esta ley [...] podrá realizar
> inspecciones, e instruir [...] auditorías por sí o mediante terceros autorizados [...]"

**Razonamiento aplicado:** la Agencia tiene potestad fiscalizadora directa con auditorías (letra ñ) —
mismo nivel de potestad que la Agencia de Protección de Datos bajo la Ley 19.628 modificada, confirmando
que un SLEP puede ser auditado por DOS agencias distintas (ciberseguridad y datos personales) con
potestades de acceso a sistemas/información similares pero regímenes procesales propios.

### Artículo 11 letra j) — Acceso a información y datos personales
> **TEXTO LITERAL** (Art. 11 letra j, página 7)
> "Cuando la información [...] incluya datos personales, éstos deberán ser anonimizados, siempre que ello
> sea posible sin entorpecer la gestión de incidentes. En cualquier caso, los datos personales sólo podrán
> ser tratados con estricto cumplimiento de lo dispuesto en la ley N° 19.628 [...] **no se considerará la
> dirección IP como un dato personal**."

**Razonamiento aplicado:** precisión importante y potencialmente contraintuitiva — la Ley 21.663
**excluye expresamente la IP del concepto de dato personal para sus propios efectos**, mientras que bajo
la Ley 19.628 modificada la IP normalmente calificaría como dato personal (identificador indirecto, Art.
2 letra f). Esta exclusión es **solo para efectos de la Ley 21.663** (reportes de incidentes al CSIRT), no
cambia el régimen general de la Ley 19.628 para otros usos de la IP.

### Artículo 24 — CSIRT Nacional
> **TEXTO LITERAL** (Art. 24, página 13)
> "Créase dentro de la Agencia Nacional de Ciberseguridad el Equipo Nacional de Respuesta a Incidentes de
> Seguridad Informática, en adelante 'CSIRT Nacional' [...] a) Responder ante ciberataques o incidentes de
> ciberseguridad, cuando éstos sean de efecto significativo. [...] i) Difundir alertas tempranas, avisos e
> información sobre riesgos e incidentes para la comunidad."

**Razonamiento aplicado:** el CSIRT Nacional es el destinatario operativo de los reportes del Art. 9° —
canal técnico, distinto del canal legal/administrativo hacia la Agencia de Protección de Datos.

## Artículo 27 — Incidente de "efecto significativo" (umbral que activa reporte reforzado)
> **TEXTO LITERAL** (Art. 27, página 15)
> "Se considerará que un incidente de ciberseguridad tiene efecto significativo si es capaz de interrumpir
> la continuidad de un servicio esencial o afectar la integridad física o la salud de las personas, así
> como **en el caso de afectar sistemas informáticos que contengan datos personales**. Para determinar la
> importancia de los efectos [...]: a) El número de personas afectadas. b) La duración del incidente. c)
> La extensión geográfica [...]"

**Razonamiento aplicado:** confirma que CUALQUIER incidente que afecte sistemas con datos personales se
califica automáticamente como "de efecto significativo" — no hace falta que además interrumpa el
servicio; esto dispara el plazo de 24h (si es OIV) en vez de 72h. Para un SLEP (que trata datos de
alumnos/funcionarios en prácticamente todos sus sistemas), casi cualquier incidente de seguridad relevante
va a calificar como "efecto significativo" por esta vía.

## Artículo 28 — Certificación
> **TEXTO LITERAL** (Art. 28, página 15)
> "Los operadores de importancia vital deberán obtener las certificaciones de ciberseguridad que señala
> esta ley y las que determine la Agencia mediante reglamento. [...] sólo los organismos que sean parte del
> registro de entidades certificadoras autorizadas a cargo de la Agencia estarán habilitadas para emitir
> certificaciones válidas [...] La Agencia podrá homologar certificaciones técnicas internacionales o
> extranjeras sobre ciberseguridad mediante resolución fundada."

**Razonamiento aplicado:** la certificación es exigible **solo a OIV**, no a todo servicio esencial —
y la homologación de certificaciones internacionales (ej. ISO 27001) queda sujeta a resolución fundada de
la Agencia, no es automática. Verificar activamente si la Agencia ya dictó esa homologación antes de
asumir que una certificación ISO 27001 basta por sí sola ante la ANCI.

## Título VII — Infracciones y sanciones (Arts. 37-46)

### Artículo 38 — Infracciones generales (leves/graves/gravísimas)
> **TEXTO LITERAL** (Art. 38, páginas 17-18)
> "Se considerarán infracciones leves las siguientes: [...] 2. Incumplir las instrucciones generales o
> particulares [...] Se considerarán infracciones graves las siguientes: 1. No haber implementado los
> protocolos y estándares establecidos por la Agencia [...] 5. Incumplir la obligación de reportar
> establecida en el artículo 9°. [...] Se considerarán infracciones gravísimas las siguientes: 1. Entregar
> a la Agencia información manifiestamente falsa o errónea, cuando ella sea necesaria para la gestión de
> un incidente [...]"

**Razonamiento aplicado:** no reportar dentro de los plazos del Art. 9° es, por sí solo, **infracción
grave** (no leve) — el incumplimiento del cronograma de 3h/72h/24h/15 días tiene consecuencia sancionatoria
directa, no es solo una buena práctica recomendada.

### Artículo 39 — Infracciones específicas de OIV (mapeadas 1:1 al Art. 8°)
> **TEXTO LITERAL** (Art. 39, página 18)
> "Se considerarán infracciones leves las siguientes: [...] 4. No designar un delegado de ciberseguridad,
> según dispone la letra i). [...] Se considerarán infracciones graves las siguientes: 1. No haber
> implementado el sistema de gestión de seguridad de la información continuo al que se refiere la letra
> a). 2. No haber elaborado o implementado los planes de continuidad operacional [...]"

**Razonamiento aplicado:** confirma que no tener SGSI implementado (Art. 8 letra a) es infracción
**grave** para un OIV — no designar delegado de ciberseguridad es solo **leve**. Jerarquía útil para
priorizar qué construir primero en una organización que parte de cero.

### Artículo 40 — Sanciones (montos, verificados contra el texto)
> **TEXTO LITERAL** (Art. 40, páginas 18-19)
> "1. Las infracciones leves serán sancionadas con multa de hasta 5.000 unidades tributarias mensuales, o
> hasta 10.000 unidades tributarias mensuales si se trata de un operador de importancia vital. 2. Las
> infracciones graves serán sancionadas con multa de hasta 10.000 unidades tributarias mensuales, o hasta
> 20.000 unidades tributarias mensuales si se trata de un operador de importancia vital. 3. Las
> infracciones gravísimas serán sancionadas con multa de hasta 20.000 unidades tributarias mensuales, o
> hasta 40.000 unidades tributarias mensuales si se trata de un operador de importancia vital."

**Razonamiento aplicado:** confirma exactamente el monto tope de tu investigación (40.000 UTM) — pero
precisa que ese monto máximo aplica **solo a OIV en infracción gravísima**; para un servicio esencial no
calificado OIV (la mayoría de los SLEP), el tope es la mitad (20.000 UTM). El monto se gradúa además por
las mismas variables ya vistas en otras leyes de esta arquitectura (diligencia, probabilidad, gravedad,
reincidencia en 3 años, tamaño/capacidad económica del infractor) — mismo patrón de determinación de multa
que la Ley 19.628 modificada (Art. 37) y el DAMA-DMBOK (factores de riesgo).

## Grafo de esta skill (relación con otras)
Ver `## Grafo` en `SKILL.md`. Este archivo es de contenido normativo — para el cruce con NIST CSF 2.0 y
la traducción a controles técnicos concretos, ver `references/complementario/`.
