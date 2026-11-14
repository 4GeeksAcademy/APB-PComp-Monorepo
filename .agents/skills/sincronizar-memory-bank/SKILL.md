---
name: sincronizar-memory-bank
description: "Usa esta skill cuando haya que sincronizar el Memory Bank después de cambios confirmados en el repositorio, decisiones del desarrollador o avances verificables del proyecto."
user-invocable: true
disable-model-invocation: false
---

# Sincronizar el Memory Bank

## Propósito

Mantener los documentos de `memory-bank/` alineados con el estado comprobable del repositorio y las decisiones explícitas del desarrollador, sin convertir propuestas en hechos.

## Cuándo usarla

- Después de completar un cambio que modifique el estado de implementación descrito en `progress.md`.
- Después de que el desarrollador confirme un cambio de objetivos, alcance o contexto empresarial.
- Después de que el desarrollador confirme una decisión técnica, un cambio de arquitectura o una nueva restricción.
- Cuando se solicite explícitamente revisar o sincronizar el Memory Bank.

No la uses para inventar un roadmap, validar objetivos sin fuente o registrar como decidido algo que solo aparece en una propuesta.

## Entradas

- Los archivos de Memory Bank existentes: `projectBrief.md`, `techContext.md`, `progress.md` y cualquier otro Markdown bajo `memory-bank/`.
- Los cambios del repositorio pertinentes, revisados mediante `git status` y `git diff` cuando estén disponibles.
- La solicitud o decisión explícita del desarrollador que autoriza cambios de negocio, alcance o arquitectura.
- Fuentes verificables del repositorio y resultados de las comprobaciones aplicables.

## Procedimiento

1. Lee los tres documentos actuales del Memory Bank y cualquier otro Markdown de esa carpeta.
2. Inspecciona `git status` y el diff relevante. Distingue cambios del usuario o preexistentes de los que forman parte de la tarea; no reviertas ni atribuyas cambios sin evidencia.
3. Clasifica cada hallazgo como hecho verificado, decisión explícita, propuesta o pregunta abierta. Si hay contradicciones entre fuentes, regístralas como pendientes y pide aclaración cuando impidan una actualización correcta.
4. Determina qué documento corresponde actualizar:
   - `progress.md`: estado de implementación y trabajo terminado verificable.
   - `projectBrief.md`: cambios confirmados de negocio, problema, objetivos o alcance.
   - `techContext.md`: cambios confirmados del stack, arquitectura o restricciones técnicas.
5. Edita solo los documentos de `memory-bank/` necesarios. Conserva el resto sin cambios y respeta las rutas protegidas.
6. Valida las rutas y referencias documentales, ejecuta las comprobaciones de formato o Markdown disponibles y resume los archivos tocados y cualquier tema pendiente.

## Resultados

- Los documentos afectados quedan alineados con las fuentes y decisiones verificadas; o
- el Memory Bank permanece sin cambios si no hay información nueva verificable.
- En ambos casos, informa qué se contrastó, qué documento se actualizó o se dejó intacto, las comprobaciones realizadas y las contradicciones que requieren confirmación.

## Criterios de aceptación

- Se leyeron los tres documentos actuales del Memory Bank y los Markdown adicionales que existan en esa carpeta.
- Cada afirmación nueva puede vincularse a una fuente del repositorio, un resultado de comprobación o una decisión explícita del desarrollador.
- Las propuestas, hipótesis y preguntas abiertas están identificadas como tales; no se inventan fechas, responsables, cifras, metas ni decisiones.
- Solo se modifican archivos dentro de `memory-bank/`, y únicamente los que necesitan actualizarse.
- Los cambios pasan las comprobaciones documentales disponibles; se informan las comprobaciones no disponibles o fallidas.
- El resultado final enumera las rutas modificadas y las cuestiones que siguen pendientes.
