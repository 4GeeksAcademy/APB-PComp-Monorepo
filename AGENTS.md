# Instrucciones del repositorio

## Idioma de la documentación

- Redacta en español toda documentación nueva o modificada para este repositorio, incluida la documentación del Memory Bank.
- El idioma del contenido no depende del nombre convencional del archivo: `README.md`, `CONTEXT.md`, `projectBrief.md` y otros nombres técnicos pueden conservarse aunque su contenido esté en español.
- Conserva nombres propios, identificadores de código, nombres de API, paquetes, herramientas y términos técnicos cuando corresponda; explica su significado en español si hace falta.
- Mantén sin cambios las versiones inglesas de documentación ya existente, salvo que se solicite expresamente traducirlas. No crees versiones en inglés de documentación nueva a menos que se pidan.

## Inicio del trabajo y reglas del agente

- Al iniciar cada nueva sesión de trabajo, lee las reglas de `.agents/rules/` y los tres documentos actuales del Memory Bank: `memory-bank/projectBrief.md`, `memory-bank/techContext.md` y `memory-bank/progress.md`. Lee también cualquier archivo Markdown nuevo que se añada a `memory-bank/`.
- Para VS Code Copilot Chat, `AGENTS.md` es el punto de entrada de instrucciones del repositorio. La carga automática de `.agents/rules/` no está garantizada; abre y sigue explícitamente esas reglas cuando trabajes en este repositorio.
- Usa la skill `.agents/skills/sincronizar-memory-bank/SKILL.md` cuando la tarea requiera sincronizar el Memory Bank con cambios confirmados del repositorio.
- Sigue las instrucciones específicas de estas reglas:
  - `.agents/rules/memory-bank.md`
  - `.agents/rules/commit-workflow.md`
  - `.agents/rules/protected-paths.md`

## Ubicación del código de producto

- El sitio web público de la empresa vive en `uis/website/` y usa `/` como ruta de entrada de esa aplicación.
- La aplicación interna vive en `uis/backoffice/`, separada del sitio público, con su propio layout y ruta de entrada `/` dentro de esa aplicación.
- Las APIs y servicios backend viven bajo `services/`.
- Antes de crear un componente, lee el README de la carpeta correspondiente. No crees un segundo árbol de aplicaciones, frontend o API fuera de estas rutas.
- Estas rutas indican dónde debe vivir el código cuando se creen las aplicaciones; no implican que las aplicaciones ya existan ni definen hostnames o despliegue.

## Revisión documental después de implementar

- Después de cada implementación, identifica qué documentación existente quedó afectada o podría haber quedado desactualizada y propone al desarrollador actualizar las rutas concretas con el motivo.
- Considera solo documentación relacionada con el cambio: README del componente, contratos o guías de API, arquitectura, contexto empresarial/técnico, Memory Bank, reglas o skills.
- En implementaciones grandes, revisa la coherencia entre los componentes afectados, sus pruebas y toda la documentación relacionada antes de informar que el trabajo está terminado.
- No amplíes silenciosamente el alcance ni edites rutas protegidas. Si una actualización propuesta excede la autorización recibida, enumera los archivos y espera confirmación.
- No afirmes que todo el repositorio está libre de inconsistencias si solo revisaste una parte; especifica el alcance de la revisión y cualquier limitación.
