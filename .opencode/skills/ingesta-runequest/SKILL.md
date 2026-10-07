---
name: ingesta-runequest
description: Use ONLY when user provides a new RuneQuest book, OCR, scan or supplement to ingest into the Obsidian vault. Triggers on nuevo libro, nuevo documento, escaneo, OCR, ingesta, ampliar obsidian, TAREAS, QUESTIONS.
---

# Ingesta RuneQuest

Proceso usado con Dioses de Glorantha. Aplica AGENTS.md del vault sin excepciones.

## 0. Leer antes de tocar

1. Leer fuente completa aportada por usuario.
2. Leer 00-Indice.md, TAREAS.md, QUESTIONS.md e índices locales (Indice-Cultos, Indice-Magia, Indice-Glorantha, Indice-Bestiario, Indice-Equipo-y-Economia, Indice-Escenarios, Indice-Tablas) más Plantillas/Culto y Plantillas/Conjuro.
3. Localizar notas existentes por TEMA con índices + búsqueda, nunca por nombre de fichero.

## 1. Planificar en TAREAS.md primero

Antes de crear nada, escribir listado completo en TAREAS.md, una línea por tarea `- [ ] …`, con subtareas con sangría. Ejemplo real usado:

- Bloque DG-0 base e inventario 60 vs 15, criterios Prosopedia y Palabras, dudas Q53-Q57.
- Bloques DG-1 a DG-9 por panteones y carpetas temáticas.
- Bloque DG-10 un conjuro por nota según apéndice.
- Bloque DG-11 cierre con índices y verificación.

Si una tarea se subdivide, reflejarlo en TAREAS.md. Marcar `- [x]` al terminar cada una antes de pasar a la siguiente. Nunca terminar con tareas sin marcar.

## 2. Dudas en QUESTIONS.md al momento

Toda duda de fidelidad (OCR dudoso, contradicciones, valores a cotejar), decisión de alcance o interpretación se registra en cuanto aparece con formato en uso:

**Pregunta N — tema**, `¿Dónde?` manual capítulo tabla, `Duda` dato y valor provisional, petición concreta.

N continúa desde máximo existente aunque esté cerrada (tras Q45 y Q46-Q52, siguiente Q53). Al responderse: aplicar a su nota, retirar warning y eliminarla de QUESTIONS.md. Avisar siempre por chat cuando aparezcan preguntas nuevas.

Casos tipo ya resueltos: Q53 Goods→Gods confirmado, Q54 Yelmalio canónico con variantes, Q55 Pocharngo Wachaza Babeester Gor Lumavoxoran Saliligor por cabecera, Q56 tablas manuales pp. 31 47 184 y omitir pp. 175-184 por imágenes, Q57 omitir mapas pp. 20-21 por imágenes, Q24 cerrada al ingerir Glorantha.

## 3. Crear sin duplicar

- Coincide por tema → ampliar sin duplicar. No coincide → crear en su carpeta temática.
- Nombres estables sin numerar notas, solo carpetas llevan número.
- Mezcla multitema → repartir entre notas, nunca cajón-de-sastre.
- UN culto por fichero en 04-Cultos/Culto-Nombre.md con secciones Panteón y afinidades, Rangos y requisitos, Magia del culto por tipo, Habilidades y beneficios, Fuente. Panteones.md solo agrupa.
- UN conjuro por fichero en 03-Magia/Nombre.md con Tipo, Culto de origen, Otros cultos que lo enseñan o exclusivo, Restricciones o sin restricciones conocidas, Requisitos rango y PER, Estadísticas Coste Alcance Duración Acumulable Reutilizable, Efecto, Fuente. Cada conjuro enlaza a su culto y cada culto lista su magia: vínculo bidireccional verificable.
- No usar conceptos de otras ediciones como secciones propias.
- Actualizar índice local + 00-Indice.md, wikilinks Nombre-de-Nota sin rutas absolutas, tags jerárquicos runequest. Sin frontmatter YAML. No tocar .obsidian/json.
- Markdown Obsidian, UTF-8 LF, encabezados ##, reglas en tablas no prosa.
- Fidelidad: no inventar reglas, resumir fiel. Pie obligatorio `*Fuente: <manual>, p. <páginas>.*`. OCR dudoso o contradicción con `> [!warning]` en nota, nunca fusionar en silencio.

## 4. Comunicación

Al responder sobre la bóveda en el chat, nombres y enlaces como texto plano, sin corchetes Obsidian, sin warnings ni tags. Los ficheros sí llevan wikilinks.

## 5. Cierre

- Índices y 00-Indice actualizados, Tablas-Referencia solo resúmenes.
- Verificar bidireccional culto-conjuro en cada nota.
- TAREAS todo marcado, QUESTIONS sin las resueltas.
- Si el usuario dice pregunta N, mostrarla, proponer cierre con question tool y al confirmar aplicar a nota, eliminar de QUESTIONS y actualizar TAREAS. Si dice continua, seguir por siguiente bloque pendiente.
