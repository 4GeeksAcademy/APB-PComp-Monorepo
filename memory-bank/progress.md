# Estado del desarrollo

_Estado documentado a 14 de noviembre de 2026._

## Situación actual

El proyecto está en fase de definición y documentación. El repositorio es una plantilla de monorepo y todavía no contiene una aplicación funcional de TrackFlow.

### Documentación completada

- [`CONTEXT.md`](../CONTEXT.md) y [`CONTEXT.es.md`](../CONTEXT.es.md) describen el contexto empresarial y del dominio. Algunas discrepancias de las fuentes están señaladas como pendientes de confirmación.
- [`projectBrief.md`](projectBrief.md) resume el negocio, el problema, los objetivos descritos en el briefing, las áreas afectadas y las propuestas aún no aprobadas.
- [`techContext.md`](techContext.md) documenta el entorno técnico comprobable, el código existente y las decisiones técnicas que siguen abiertas.
- [`AGENTS.md`](../AGENTS.md) establece que la documentación nueva o modificada debe redactarse en español.
- `.agents/rules/` contiene reglas para el Memory Bank, el flujo previo al commit y las rutas protegidas.
- `.agents/skills/sincronizar-memory-bank/SKILL.md` documenta una skill para sincronizar el Memory Bank con cambios verificables.
- La ubicación prevista del sitio público es `uis/website/`, la de la aplicación interna es `uis/backoffice/` y las APIs/servicios backend viven bajo `services/`. Esas subcarpetas de producto aún no están creadas.

### Implementación visible

- El paquete `@repo/shared-types` contiene tipos TypeScript básicos de ejemplo.
- `skills/data-analysis/scripts/pandas_clean.py` es un ejemplo de limpieza exploratoria con pandas.
- `.devcontainer/devcontainer.json` configura el entorno de desarrollo.
- No se encontraron aplicaciones de interfaz, APIs, agentes de producto, servidores MCP, workflows ni infraestructura de despliegue implementados. La skill de mantenimiento en `.agents/` es configuración del agente, no un agente de producto.
- No se encontraron configuración de CI ni pruebas de producto.

## Próximos pasos pendientes de decisión

No se han acordado responsables ni fechas. Los siguientes elementos son temas de trabajo identificados, no compromisos aprobados:

1. Confirmar las discrepancias en las fuentes sobre los mercados de TrackFlow y los nombres de su dirección.
2. Verificar en VS Code Copilot Chat la carga efectiva de las reglas referenciadas desde `AGENTS.md` y la disponibilidad/invocación de la skill. La referencia local documenta las ubicaciones, pero esta verificación de ejecución no está registrada.
3. Decidir la arquitectura de backend y si se adoptará FastAPI; las rutas de las aplicaciones están documentadas, pero no hay implementación ni decisión de despliegue.
4. Acordar criterios de aceptación medibles para las primeras entregas, incluyendo fuentes de medición, líneas base y umbrales cuando corresponda.

## Criterio para actualizar este estado

Actualizar esta página cuando se confirme una decisión, se complete un entregable o cambie el estado de implementación. No registrar propuestas como decisiones, ni asignar fechas, responsables, porcentajes de avance o métricas que no se hayan confirmado.
