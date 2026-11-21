# Contexto técnico

## Alcance y estado

Este documento describe el entorno de desarrollo configurado, el código técnico visible en el repositorio y las orientaciones de arquitectura documentadas. No define un stack objetivo ni convierte recomendaciones de la plantilla en decisiones aprobadas.

## Entorno de desarrollo

La configuración de `.devcontainer/devcontainer.json` declara:

- Imagen base `mcr.microsoft.com/devcontainers/base:ubuntu-24.04`.
- Python 3.12, con instalación de JupyterLab.
- Node.js 22.
- Features para Docker fuera del contenedor, GitHub CLI y SSH.
- Extensiones de VS Code para Python, Pylance, Jupyter, Docker, Prettier, ESLint, Error Lens y GitLens, entre otras.
- Intérprete Python predeterminado en `${workspaceFolder}/.venv/bin/python`, terminal Bash y formato al guardar.
- Reenvío de los puertos 3000, 8000 y 5678.

Al crear el contenedor, la configuración habilita Corepack y prepara `pnpm@latest`. También instala o actualiza `uv` y `pip`. La instalación de dependencias del proyecto es condicional: ejecuta `pnpm install` si hay un `package.json` en la raíz y `uv sync` si hay un `pyproject.toml` en la raíz. Estos comandos no fijan versiones de `pnpm` o `uv` para el proyecto.

Lo anterior describe el entorno de desarrollo. No demuestra qué runtimes, dependencias o servicios se usan en producción.

## Código y tecnologías presentes

- `packages/shared/package.json` declara el paquete privado `@repo/shared-types`, versión `0.0.1`. No define scripts de ejecución, compilación o pruebas.
- `packages/shared/types/index.ts` contiene tipos TypeScript básicos de ejemplo: `Id` y `BaseEntity`.
- `skills/data-analysis/scripts/pandas_clean.py` es un ejemplo de limpieza exploratoria de CSV con pandas. El repositorio no incluye un manifest de dependencias para este script.

Estos componentes son mínimos y no constituyen una aplicación desplegable ni un stack integrado.

## Arquitectura documentada

La plantilla organiza el repositorio por responsabilidades: interfaces en `uis/`, servicios backend en `services/`, código reutilizable empaquetado en `packages/`, y áreas separadas para datos, agentes, skills, MCP, workflows, infraestructura y documentación.

La plantilla ofrece una recomendación de backend y una guía de organización por carpetas:

- El README raíz **recomienda** una API FastAPI centralizada y desaconseja empezar con muchos microservicios.
- `services/README.es.md` describe una subcarpeta por servicio, como `admin-api` o `data-processor-worker`.

Estas orientaciones pueden coexistir: una API central podría ubicarse en `services/api/` y los workers que necesiten ejecución independiente en otras subcarpetas. La documentación no obliga a crear microservicios por dominio. FastAPI centralizado sigue siendo una recomendación de la plantilla, no una tecnología implementada ni una decisión aprobada para el producto; la estructura final está pendiente de acordarse.

### Ubicación del código de producto

Según la estructura acordada para este proyecto:

- El sitio web público va en `uis/website/`; su ruta de entrada es `/` dentro de esa aplicación y su marca y contenido deben alinearse con `BRIEFING.md`.
- La aplicación interna va en `uis/backoffice/`, separada del sitio público, con layout propio y ruta de entrada `/` dentro de esa aplicación.
- Las APIs y los servicios backend van bajo `services/`, siguiendo el README de esa carpeta.
- No se debe crear un árbol paralelo de apps, frontend o API en otra ubicación. Antes de implementar, hay que revisar el README de la carpeta correspondiente.

Estas rutas son convenciones de ubicación, no evidencia de que las aplicaciones ya estén creadas. En el estado actual, `uis/` y `services/` contienen sus README, pero no esas subcarpetas de producto. Tampoco se define aquí el enrutamiento entre dominios/hostnames ni el despliegue de las aplicaciones.

## Sistemas existentes de TrackFlow

El briefing empresarial y los archivos `CONTEXT.md` y `CONTEXT.es.md` describen un entorno heredado que incluye dos sistemas de almacén distintos, un ERP de principios de la década de 2010, scripts de Python punto a punto, integraciones sin documentar y bases de datos en dos proveedores cloud.

Esta descripción corresponde a los sistemas actuales de la empresa; no indica qué tecnologías se adoptarán para las aplicaciones nuevas de este repositorio.

## Ausencias verificadas en el repositorio

En la revisión de la estructura actual no se encontraron:

- Un `package.json` o `pyproject.toml` en la raíz, ni un `pnpm-workspace.yaml`.
- Archivos `requirements*.txt` o configuración `tsconfig*.json`.
- Un `Dockerfile` o `docker-compose.yml`.
- Workflows de CI bajo `.github/workflows/`.
- Configuración compartida de lint, formato, compilación o pruebas para todo el monorepo.
- Un framework de frontend, API implementada, base de datos objetivo o estrategia de despliegue para el producto.

La ausencia significa que no se encontró esa configuración en el repositorio revisado; no implica que la tecnología sea incompatible o que no pueda añadirse posteriormente.

## Restricciones y decisiones pendientes

- Las versiones de Python y Node.js indicadas arriba pertenecen al dev container. No se documentan versiones de producción.
- No está definido si las aplicaciones compartirán dependencias y scripts desde la raíz o si cada proyecto mantendrá su propia configuración.
- No se ha elegido framework de frontend, framework de backend, base de datos, mecanismo de despliegue ni proceso de CI.
- El briefing indica que algunos servicios deben estar disponibles continuamente (24/7), pero no define un SLA ni un objetivo técnico cuantificado de disponibilidad.
- No hay contratos de API, límites de rendimiento, requisitos de capacidad ni requisitos de seguridad específicos del producto establecidos en los archivos revisados.

## Propuestas no aprobadas

No se añaden propuestas de stack o arquitectura a este contexto. Las recomendaciones futuras deberán aparecer identificadas explícitamente como propuestas hasta que sean aceptadas.

## Fuentes

- [`.devcontainer/devcontainer.json`](../.devcontainer/devcontainer.json): entorno de desarrollo.
- [`README.es.md`](../README.es.md): estructura del monorepo y recomendación de backend.
- [`services/README.es.md`](../services/README.es.md): organización sugerida para servicios.
- [`packages/shared/package.json`](../packages/shared/package.json) y [`packages/shared/types/index.ts`](../packages/shared/types/index.ts): paquete y tipos compartidos existentes.
- [`skills/data-analysis/scripts/pandas_clean.py`](../skills/data-analysis/scripts/pandas_clean.py): ejemplo de limpieza con pandas.
- [`CONTEXT.md`](../CONTEXT.md), [`CONTEXT.es.md`](../CONTEXT.es.md) y [`BRIEFING.md`](../BRIEFING.md): contexto de sistemas heredados de TrackFlow.
