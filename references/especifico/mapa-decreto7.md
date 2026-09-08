# Mapa de artículos — Decreto 7/2023 (Norma Técnica de Seguridad de la Información y Ciberseguridad del Estado)

> Verificado contra `sources/especifico/decreto-7-2023-norma-tecnica-ciberseguridad-estado.pdf` (Diario
> Oficial N°43.629, 17-ago-2023, 6/6 páginas íntegras, Ministerio Secretaría General de la Presidencia).
> Dictado en virtud de la Ley 21.180 de Transformación Digital del Estado. **Aplica directamente y sin
> calificación previa a TODO órgano de la Administración del Estado — incluido un SLEP** — a diferencia
> de la Ley 21.663 donde el régimen reforzado (OIV) requiere calificación expresa.

## Artículo 1 — Objeto
> **TEXTO LITERAL** "definir los estándares y establecer las directrices técnicas sobre seguridad de la
> información y ciberseguridad, que deberán cumplir los órganos de la Administración del Estado para
> resguardar la confidencialidad, integridad, disponibilidad de la información y la infraestructura
> informática, de las plataformas electrónicas que sustentan sus procedimientos administrativos."

**Razonamiento aplicado:** el objeto se limita textualmente a "plataformas electrónicas que sustentan
procedimientos administrativos" — no es un mandato de seguridad genérico sobre cualquier sistema del
organismo, sino específicamente sobre las plataformas que soportan trámites/procedimientos
administrativos (ej. sistema de matrícula, plataforma de licencias/permisos, tramitación documental). Un
SLEP debe identificar primero cuáles de sus sistemas caen en esa categoría antes de aplicar la norma
indiscriminadamente a toda su infraestructura.

## Artículo 4 — Diagnóstico inicial
> **TEXTO LITERAL** "Cada órgano de la Administración del Estado deberá realizar un diagnóstico inicial
> del estado de ciberseguridad de sus plataformas electrónicas [...] deberán incluir el diagnóstico
> [...] en el Catálogo de Plataformas de la Norma Técnica de Calidad y Funcionamiento [...] con el fin de
> mantener un registro íntegro de las plataformas electrónicas que administren."

**Razonamiento aplicado:** el primer paso operativo obligatorio es un inventario/diagnóstico — no se
puede saltar directo a implementar controles sin antes tener el catálogo completo de plataformas. Esto
es funcionalmente equivalente al RAT de `proteccion-datos-personales-cl` pero para infraestructura
técnica en vez de datos personales — ambos inventarios deberían idealmente construirse de forma
coordinada (mismas plataformas, dos ángulos de registro).

## Artículo 5 — Política de Seguridad de la Información y Ciberseguridad
> **TEXTO LITERAL** "Cada órgano [...] deberá elaborar una Política [...] aprobada a través de acto
> administrativo por el respectivo Jefe(a) Superior de Servicio [...] La Política deberá contener, a lo
> menos, lo siguiente: 1) Los objetivos generales específicos [...] 2) La identificación y determinación
> del alcance [...] 3) La legislación y normativa vigente aplicable al órgano. 4) Especificar los roles, y
> definir un(a) responsable institucional de seguridad de la información y ciberseguridad y un(a)
> responsable de los activos de información. [...] El desempeño de estas funciones **no podrá ser
> externalizado bajo ninguna forma**."

**Razonamiento aplicado:** dos roles obligatorios y distintos (responsable institucional de seguridad ≠
responsable de activos de información) que **no pueden externalizarse** — coincide con la regla ya vista
en `proteccion-datos-personales-cl` para el DPO de un órgano público (debe ser funcionario de dotación
vigente, Reglamento MPI Art. 7). Un SLEP no puede contratar un CISO externo como única figura responsable
de esta política; puede apoyarse en terceros técnicamente, pero la responsabilidad formal debe recaer en
personal propio. La Política debe aprobarse por acto administrativo del Jefe Superior de Servicio — para
un SLEP, la Dirección Ejecutiva.

## Artículo 6-11 — Las 5 funciones (estructura idéntica a NIST CSF 1.1)
> **TEXTO LITERAL** (Arts. 7-11, resumen de cada función)
> "Artículo 7.- Función de identificación. [...] identificación y adecuada administración de los riesgos
> [...] comprende [...] contexto o entorno [...] gobernanza; gestión de activos de información; gestión de
> riesgos; y contratación y gestión de la relación con proveedores de servicios en la nube. Artículo 8.-
> Función de protección. [...] gestión de servidores, redes, autenticación y control de acceso [...] la
> concienciación y formación de los funcionarios [...] la seguridad de los datos [...] el registro de
> eventos. Artículo 9.- Función de detección. [...] análisis de eventos [...] monitoreo continuo de la
> seguridad [...] protección contra código malicioso [...] Artículo 10.- Función de respuesta. [...]
> planificación de respuesta ante incidentes; comunicación de acciones de respuesta; análisis de
> incidentes; mitigación de incidentes; y mejoras [...] Artículo 11.- Función de recuperación. [...]
> planificación de la recuperación; mejoras [...]; y comunicación del estado de recuperación."

**Razonamiento aplicado — hallazgo estructural verificado, no interpretación libre**: las 5 funciones del
Decreto 7 (Identificación, Protección, Detección, Respuesta, Recuperación) son, en nombre y contenido,
**exactamente las 5 funciones originales del NIST Cybersecurity Framework** (Identify, Protect, Detect,
Respond, Recover — NIST CSF 1.1). Esto no es una analogía forzada: la propia norma reconoce en sus
considerandos que la mesa técnica trabajó "de acuerdo a estándares internacionales emitidos por organismos
reconocidos". Consecuencia práctica directa: **el marco NIST CSF (ver `references/complementario/`) es la
guía de implementación de facto del Decreto 7** — no reemplaza la norma chilena (que es la obligatoria),
pero da el detalle operativo que el decreto delega a "guías técnicas" (Art. 12) aún genéricas en el texto
mismo del decreto.

**Nota importante — NIST CSF 2.0 (2024) agregó una sexta función, GOVERN, que no está en el Decreto 7**
(dictado en 2023 bajo el marco de 5 funciones de CSF 1.1). El Art. 5 (Política de Seguridad) cubre
parcialmente lo que CSF 2.0 formaliza como GOVERN, pero no con esa etiqueta ni el mismo detalle — al usar
NIST CSF como complemento, usar CSF 2.0 para profundidad pero verificar que la función GOVERN no se
presente como si fuera un requisito explícito del Decreto 7, que no la nombra.

## Artículo 12 — Guías técnicas (nivel de detalle operativo, pendiente verificar vigencia)
> **TEXTO LITERAL** "la División de Gobierno Digital [...] dictará una o más guías técnicas que
> establezcan sus aspectos operativos y procesos."

**Razonamiento aplicado:** el decreto delibera delega el detalle operativo (cómo hacer cada función en la
práctica) a guías técnicas separadas de la Secretaría de Gobierno Digital — verificar activamente en
`wikiguias.digital.gob.cl` si ya existen y qué versión está vigente antes de asumir que el decreto por sí
solo basta para implementar.

## Artículo 13 — Gradualidad
> **TEXTO LITERAL** "La aplicación de esta norma será acorde a la gradualidad establecida en el decreto
> con fuerza de ley Nº 1, de 2020 [...] la División de Gobierno Digital definirá los lineamientos y
> formato en que los órganos obligados deberán llevarla a cabo."

**Razonamiento aplicado:** no toda la Administración del Estado quedó obligada desde el día 1 — hay un
cronograma de gradualidad por tipo de órgano. Verificar en qué tramo de gradualidad cae un SLEP
específico antes de fijar plazos de cumplimiento internos.

## Grafo
Se combina con `mapa-ley21663.md` (obligaciones generales de ciberseguridad) y con
`references/complementario/` (NIST CSF, traducción operativa de las 5 funciones). Ver `## Grafo` en
`SKILL.md`.
