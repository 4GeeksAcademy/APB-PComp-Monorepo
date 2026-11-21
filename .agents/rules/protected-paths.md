# Rutas protegidas

No modifiques las rutas siguientes sin confirmación explícita del desarrollador para ese cambio. Una solicitud directa para cambiar una ruta concreta cuenta como autorización para ese alcance, pero no autoriza cambios adicionales relacionados.

## Fuentes de negocio y decisiones

- `BRIEFING.md`
- `company-choice.md`
- `CONTEXT.md`
- `CONTEXT.es.md`
- `memory-bank/projectBrief.md` cuando el cambio altere negocio, objetivos, prioridades o alcance
- `memory-bank/techContext.md` cuando el cambio establezca o altere decisiones técnicas o arquitectura

## Instrucciones y configuración de agentes

- `AGENTS.md`
- `.agents/**`
- `.github/**`

## Entorno, dependencias y despliegue

- `.devcontainer/**`
- `infra/**`
- Archivos `Dockerfile*` y `docker-compose*.yml`
- Manifests y lockfiles de dependencias

## Datos y secretos

- `data/raw/**`: no sobrescribas, transformes ni elimines datos fuente. Trabaja sobre una copia o en la ubicación de salida acordada.
- Archivos `.env*`, `secrets/**`, `*.pem` y `*.key`, si existen: no muestres ni incluyas sus contenidos en respuestas, logs o commits. No los modifiques sin autorización explícita.

## Memory Bank y estado

- `memory-bank/progress.md` puede actualizarse para registrar trabajo completado y verificable, sin inventar fechas, responsables ni porcentajes.
- Las rutas protegidas siguen sujetas al flujo de confirmación anterior; la skill de sincronización no amplía por sí sola el alcance autorizado.
