# Reglas del Memory Bank

## Lectura al inicio

Al comienzo de cada nueva sesión de trabajo, antes de responder sobre el proyecto, planificar o editar, lee en este orden:

1. `memory-bank/projectBrief.md` para conocer el negocio, el problema y los objetivos vigentes.
2. `memory-bank/techContext.md` para conocer el entorno técnico, la arquitectura documentada y las restricciones conocidas.
3. `memory-bank/progress.md` para conocer el estado actual y los asuntos pendientes.
4. Cualquier otro archivo Markdown que se añada a `memory-bank/`.

Si falta un archivo, indícalo. No inventes su contenido ni presentes propuestas como decisiones.

## Actualización

- Actualiza `progress.md` cuando se complete trabajo verificable, cambie el estado de implementación o se confirme una decisión relevante.
- Actualiza `projectBrief.md` solo cuando se confirme un cambio del negocio, del problema, de los objetivos o del alcance del proyecto.
- Actualiza `techContext.md` solo cuando se confirme o cambie una decisión técnica, una restricción o el entorno documentado.
- Basa cada cambio en archivos, resultados de comandos o decisiones explícitas del desarrollador. Señala contradicciones en vez de resolverlas por inferencia.
- No inventes fechas, responsables, porcentajes de avance, líneas base, metas ni criterios de aceptación.
- Mantén la documentación en español y no modifiques archivos fuera de `memory-bank/` como parte de una sincronización, salvo autorización explícita.
- Si no hay cambios verificables que registrar, deja el Memory Bank sin cambios e informa que sigue vigente.

## Revisión documental después de implementar

- Después de cada implementación, revisa qué documentación relacionada puede haber quedado desactualizada. Según el cambio, considera README del componente, contratos de API, arquitectura, `CONTEXT.md`, los archivos del Memory Bank, reglas y skills.
- Propón al desarrollador las actualizaciones necesarias con la ruta de cada archivo y el motivo; no propongas cambios en documentos no relacionados.
- En implementaciones grandes, haz una revisión cruzada de los componentes afectados y sus documentos para encontrar diferencias entre el comportamiento, las pruebas y la documentación.
- Si la actualización excede el alcance autorizado o afecta una ruta protegida, no la hagas todavía: presenta la propuesta y solicita confirmación.
- Al informar el resultado, indica qué documentación revisaste y qué quedó pendiente; no declares consistencia global sin haberla verificado.
