# Carpeta `services`

Esta carpeta contiene **todos los servicios backend** (APIs y workers en segundo plano) relacionados con la compañía para el proyecto transversal de AI Engineering.

Cada subcarpeta dentro de `services/` debe corresponder a **un servicio concreto** (por ejemplo `admin-api`, `data-processor-worker`) e incluir su propia documentación técnica y funcional.

Esta organización por carpetas no obliga a dividir el backend en microservicios. El README raíz recomienda inicialmente una API FastAPI centralizada, que podría vivir en `services/api/`, y workers separados cuando haya una necesidad concreta. Esta recomendación no es una decisión técnica aprobada para el proyecto; el diseño final sigue pendiente.

- **Propósito principal**: centralizar toda la lógica backend, APIs y consumidores de colas que dan soporte a los casos de uso de la compañía.
- **Recomendación**: documenta en este archivo (o en sub-READMEs) los servicios que vayas añadiendo, su objetivo, tecnología usada y cómo ejecutarlos.
