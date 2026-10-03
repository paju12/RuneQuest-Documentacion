# AGENTS.md — RuneQuest Documentación (RQ2 Classic)

Bóveda de Obsidian con la documentación de RuneQuest 2.ª ed. / Classic (Chaosium), en español. No es código: no hay build, tests, lint ni package manager.

Las fuentes llegan como markdown extraído de PDFs u ocasionalmente texto de OCR (puede traer errores de transcripción).

## Estructura (carpetas temáticas)

```text
00-Indice.md                      ← mapa general, enlaza a los índices locales
01-Creacion-de-Personaje/         ← características (FUE CON TAM INT POD DES APA), razas, profesiones
02-Sistema/                       ← habilidades, combate, daño/curación, fatiga, experiencia
03-Magia/                         ← batalla/espíritu, divina, hechicería + Indice-Magia.md
04-Cultos/                        ← UNA nota por culto + Panteones.md como agrupadora
05-Glorantha/                     ← mundo, historia, calendario, geografía
06-Bestiario/                     ← una nota por criatura o grupo afín
07-Equipo-y-Economia/             ← armas, armaduras, precios, botín
08-Escenarios/                    ← material propio de mesa (separado de las reglas oficiales)
Plantillas/                       ← Conjuro, Culto, Criatura, Hoja-Aventurero, Escenario
Tablas-Referencia/                ← resúmenes de consulta rápida (el detalle vive en la nota, no aquí)
TAREAS.md                         ← lista de tareas del trabajo en curso (ver sección Tareas)
```

- Cada carpeta tiene su `Indice-*.md` local con nombre único en toda la bóveda (evita colisiones de wikilinks).
- Nombres de nota descriptivos y estables, sin numerar notas (solo las carpetas llevan número).
- No usar conceptos de otras ediciones (Runas, Pasiones de RQG) como secciones propias.

## Flujo de ingesta (cada documento fuente)

1. Leer la fuente completa.
2. Localizar notas existentes por TEMA (índices + búsqueda), nunca por nombre de fichero.
3. Coincide → ampliar sin duplicar. No coincide → crear la nota en su carpeta temática.
4. Actualizar índice local + `00-Indice.md`; añadir wikilinks cruzados y tags.
5. Si una sección de la fuente mezcla temas de varias carpetas, repartirla entre las notas correspondientes en vez de crear una nota cajón-de-sastre.

## Tareas (TAREAS.md)

- Antes de empezar cualquier trabajo, escribir en `TAREAS.md` el listado completo de tareas previstas (una línea por tarea, `- [ ] …`).
- Si una tarea se divide en bloques más pequeños, reflejar la subdivisión en `TAREAS.md` (subtareas con sangría, `- [ ] …`) y marcar cada bloque al completarse.
- Al terminar cada tarea, marcarla como hecha en `TAREAS.md` (`- [x] …`) antes de pasar a la siguiente.
- No dar el trabajo por terminado con tareas sin marcar.

## Fidelidad a la fuente

- No inventar reglas. Resumir con fidelidad al documento fuente.
- Pie de nota obligatorio: `*Fuente: <manual>, p. <páginas>.*`
- Dudas de OCR o contradicciones entre fuentes: marcarlas en la nota (`> [!warning] ...`) en vez de fusionarlas en silencio.

## Preguntas pendientes (QUESTIONS.md)

- Toda duda de fidelidad a la fuente (OCR dudoso, contradicciones, valores a cotejar con el manual) o cualquier otra duda en la que sea necesaria la intervención de una persona para resolverla (decisiones de alcance, fuentes a usar, interpretaciones) se registra en `QUESTIONS.md` en cuanto aparece, con el formato en uso: **Pregunta N — tema**, `¿Dónde?` (manual, capítulo, tabla; o ámbito de la decisión), `Duda` (dato afectado y valor provisional), petición concreta del dato o de la decisión.
- Al responderse una pregunta: aplicar el valor o la decisión a su nota, retirar su marca/warning y eliminarla de `QUESTIONS.md`.
- Avisar siempre por el chat cuando aparezcan preguntas nuevas.

## Notas de magia

- UNA nota por conjuro en `03-Magia/` con la plantilla `Plantillas/Conjuro`.
- Campos obligatorios: **Tipo** (batalla/divina/hechicería), **Culto de origen** (`[[Culto-…]]`), **Otros cultos que lo enseñan** (lista explícita; si ninguno: "exclusivo de…"), **Restricciones** (quién NO puede aprenderlo/usarlo: cultos, rangos o personajes vetados; si no hay: "sin restricciones conocidas"), **Requisitos** (rango, sacrificio de POD), **Estadísticas** (coste, alcance, duración, acumulable, reutilizable/un solo uso), **Efecto**, **Fuente**.
- Cada nota de conjuro enlaza a su culto de origen y a los que lo enseñan; cada nota de culto lista su magia. Vínculo bidireccional verificable.

## Notas de cultos

- UN documento independiente por culto/religión en `04-Cultos/` (`Culto-Nombre.md`) con la plantilla `Plantillas/Culto`. Prohibido agrupar varios cultos en un fichero.
- Secciones fijas: panteón y afinidades, rangos y requisitos, magia del culto (wikilinks a cada conjuro, separada por tipo), habilidades y beneficios, fuente.
- `Panteones.md` es solo agrupadora: enlaza a sus cultos, no duplica su contenido.

## Enlaces y tags

- Wikilinks `[[Nombre-de-Nota]]`, nunca rutas absolutas. Al renombrar, actualizar a mano los apuntadores (Obsidian no lo hace solo si se edita fuera de la app).
- Tags jerárquicos: `#runequest/reglas`, `#runequest/magia`, `#runequest/cultos`, `#runequest/glorantha`, `#runequest/bestiario`, `#runequest/escenarios`, `#runequest/tablas`.

## No tocar

- `.obsidian/*.json`: config del vault. No editar a mano salvo petición explícita.
- `properties` está desactivado: no usar frontmatter YAML como fuente de verdad; la estructura va en cuerpo Markdown, enlaces y etiquetas.

## Edición

- Markdown estándar compatible con Obsidian (tablas GitHub OK para tablas de referencia).
- UTF-8, saltos de línea LF. Encabezados `##` por sección; reglas en tablas, no en prosa.
