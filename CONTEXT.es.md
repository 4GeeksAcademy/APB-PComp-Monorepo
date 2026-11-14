# Contexto empresarial de TrackFlow

Este documento recoge el contexto compartido de la empresa y su dominio para el proyecto TrackFlow. Los hechos proceden de `BRIEFING.md`; las soluciones propuestas no se consideran alcance aprobado.

## Empresa y actividad

TrackFlow es una empresa de logística de terceros (3PL) que presta servicios a marcas de comercio electrónico. Almacena el inventario de sus clientes, prepara y empaqueta pedidos, coordina las entregas mediante redes de transportistas y gestiona las devoluciones.

El briefing detallado describe operaciones en Estados Unidos y España, con almacenes en Los Ángeles y Zaragoza. Indica aproximadamente 130 empleados, unos 9 millones de euros de facturación anual y ocho transportistas entre ambos mercados. Son cifras aproximadas procedentes del briefing.

TrackFlow atiende a dos grupos de clientes:

- **B2B:** marcas de comercio electrónico que contratan los servicios logísticos de TrackFlow.
- **B2C:** consumidores que reciben envíos gestionados por TrackFlow.

## Modelo operativo

El flujo descrito en el briefing es: una marca envía un pedido; TrackFlow almacena el inventario, prepara y empaqueta el pedido, lo entrega a un transportista y gestiona el seguimiento y cualquier devolución. Actualmente, los pedidos llegan por correo electrónico en formatos variados. Este documento no define el contrato de datos ni las interfaces de los sistemas.

La empresa opera en estas áreas: operaciones de almacén, última milla y gestión de transportistas, logística inversa, experiencia del cliente, comercial y relación con clientes, personas, tecnología y dirección ejecutiva.

## Situación operativa actual

- Los almacenes de Los Ángeles y Zaragoza utilizan sistemas de gestión distintos: uno usa software comercial y el otro una hoja de cálculo avanzada. No comparten visibilidad global del inventario.
- La recepción de pedidos, asignación y seguimiento de transportistas, revisión de devoluciones, atención de consultas e informes ejecutivos implican una cantidad importante de trabajo manual.
- TrackFlow trabaja con ocho transportistas. Según el briefing, los datos históricos de rendimiento no se mantienen de forma estructurada.
- Las devoluciones representan aproximadamente entre el 18 % y el 25 % del volumen, según el cliente y el país; actualmente las decisiones reciben revisión humana.
- Atención al cliente atiende tanto a marcas como a consumidores finales por correo electrónico, WhatsApp y teléfono. El briefing indica que los agentes consultan un documento de Word en Google Drive; no identifica un sistema unificado de tickets o de conocimiento.
- El entorno técnico incluye un ERP heredado de principios de la década de 2010, integraciones sin documentar, scripts de Python punto a punto y bases de datos en dos proveedores cloud. Son descripciones de sistemas existentes, no una arquitectura objetivo elegida.
- Los informes ejecutivos se preparan manualmente y pueden incluir datos con uno o dos días de antigüedad.

## Términos del dominio

- **Almacén / SGA:** almacén físico y sistema o proceso usado para gestionar inventario y preparación de pedidos.
- **SKU:** referencia usada para identificar un producto o artículo de inventario.
- **Transportista:** empresa que traslada un envío hasta su destino.
- **Seguimiento de envío:** información sobre el estado de un envío durante la entrega.
- **Logística inversa / devolución:** proceso de gestión de un producto después de que se devuelve.
- **B2B / B2C:** servicios para clientes empresariales / interacciones con consumidores finales.

## Pendientes y cautelas sobre las fuentes

- El briefing detallado sitúa los mercados en Estados Unidos y España. El antiguo placeholder en español decía México y España. Este documento sigue el briefing detallado; hay que confirmar los mercados antes de considerar resuelta la discrepancia.
- Los nombres de dirección discrepan entre las fuentes: el briefing nombra a Thomas Harry en la descripción de la empresa y a Thomas Espinoza en la sección ejecutiva; el `CONTEXT.md` anterior también mencionaba a Daniel Espinoza. También varía la atribución de la creación de TrackFlow Tech. No se debe asumir quién es el CEO o fundador de la unidad hasta confirmarlo.
- El briefing describe disponibilidad 24/7 como una característica deseada para algunos servicios, pero no define un acuerdo formal de nivel de servicio.
- El soporte en español e inglés se describe como opcional o recomendable para algunos departamentos. No se ha establecido el idioma base del proyecto.
- Este contexto empresarial no establece un stack tecnológico objetivo, contratos de API, un catálogo de reglas de negocio ni el alcance de implementación específico del proyecto.

_This document is also available in [English](./CONTEXT.md)._
