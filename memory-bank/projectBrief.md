# Resumen del proyecto: TrackFlow Tech

## Propósito y estado

Este documento resume el contexto empresarial, los problemas descritos en el briefing de la compañía y los resultados que el proyecto podría apoyar. No aprueba una implementación ni un alcance de entrega específicos. Las prioridades, entregables, fechas y metas de éxito de TrackFlow Tech no están confirmados en los documentos disponibles.

## Descripción del negocio

TrackFlow es una empresa de logística de terceros (3PL) que presta servicios a marcas de comercio electrónico. Almacena el inventario de sus clientes, prepara y empaqueta pedidos, coordina entregas mediante redes de transportistas y gestiona devoluciones. El briefing detallado describe operaciones en Estados Unidos y España, con almacenes en Los Ángeles y Zaragoza. Indica aproximadamente 130 empleados, unos 9 millones de euros de facturación anual, ocho transportistas y devoluciones equivalentes al 18-25 % del volumen según el cliente y el país. Estas cifras son aproximadas y proceden del briefing.

TrackFlow atiende tanto a clientes empresariales (marcas de comercio electrónico) como a consumidores finales que reciben envíos. El briefing describe una unidad interna llamada TrackFlow Tech, con el mandato de construir sistemas, integraciones y automatizaciones inteligentes para la empresa.

## Problema empresarial

La operación logística de TrackFlow abarca dos países y depende de sistemas de almacén separados, un ERP heredado, integraciones sin documentar y procesos manuales. Los almacenes no comparten visibilidad del inventario; los datos de pedidos que llegan en distintos formatos de correo electrónico se transcriben manualmente; la asignación y el seguimiento de transportistas requieren trabajo manual por separado; las devoluciones se revisan una a una; y los agentes atienden consultas consultando documentos, sin un sistema de soporte unificado. Los informes ejecutivos se preparan manualmente y, al usarse, pueden contener datos con uno o dos días de antigüedad.

Esta fragmentación dificulta coordinar la operación, detectar pronto errores e incidencias, medir el rendimiento y tomar decisiones con información actualizada y coherente. El briefing describe como consecuencia una empresa más lenta, más propensa a errores y menos rentable de lo que debería ser.

## Objetivos empresariales descritos en el briefing

El briefing identifica necesidades en varios departamentos. Como resultados empresariales, estas apuntan a los siguientes objetivos:

- Mejorar la visibilidad compartida del inventario y del estado de los pedidos entre ambos almacenes.
- Reducir el trabajo manual y la fragmentación en la recepción de pedidos, la gestión de transportistas, las devoluciones, la atención al cliente y los informes.
- Estructurar y facilitar el acceso a la información sobre envíos y rendimiento de transportistas.
- Mejorar la oportunidad y coherencia de la información operativa y ejecutiva.
- Dar soporte tanto a las marcas clientes como a los consumidores finales en Estados Unidos y España.

Son objetivos empresariales sintetizados a partir del briefing, no hitos de proyecto aprobados ni compromisos cuantificados.

## Áreas afectadas

- **Operaciones de almacén:** inventario, recepción de pedidos, picking, empaquetado y discrepancias de stock.
- **Última milla y gestión de transportistas:** asignación de transportista, seguimiento e incidencias de entrega.
- **Logística inversa:** revisión, inspección y gestión de devoluciones.
- **Experiencia del cliente:** consultas de marcas y consumidores finales.
- **Comercial y relación con clientes:** gestión de cuentas, informes y renovaciones.
- **Tecnología:** sistemas, integraciones, datos y soporte operativo.
- **Dirección ejecutiva:** informes entre países y decisiones empresariales.

El briefing detallado también describe Personas/RR. HH. como área de la empresa, pero no se ha establecido su prioridad dentro de este proyecto.

## Propuesta inicial, no aprobada como alcance

En `company-choice.md` se propone explorar un asistente integral que conecte la recepción de pedidos, las consultas de inventario, las recomendaciones de transportista sujetas a revisión humana y las consultas de clientes o la gestión de tickets. Es la idea inicial del estudiante, no un requisito confirmado de la empresa ni una decisión de implementación. Este documento no aprueba un agente, una API, un sitio web, un backoffice, un workflow ni un stack tecnológico concreto.

## Posibles medidas por definir

El briefing sugiere resultados que podrían medirse, pero no aporta líneas base ni metas acordadas. Algunas medidas candidatas para confirmar más adelante son las discrepancias y visibilidad del inventario, el esfuerzo o tiempo de recepción de pedidos, las entregas puntuales e incidencias de transportistas, el tiempo de procesamiento de devoluciones, la resolución de consultas y la antigüedad de los informes ejecutivos. Aquí no se establecen umbrales numéricos de aceptación.

## Preguntas abiertas y cautelas sobre las fuentes

- **Geografía:** el briefing detallado indica Estados Unidos y España; el placeholder anterior en español indicaba México y España. El contexto actualizado sigue el briefing detallado, pero la discrepancia debe confirmarse.
- **Dirección:** las fuentes dan nombres distintos para el CEO y discrepan sobre quién creó TrackFlow Tech. Consulta las cautelas de [`CONTEXT.es.md`](../CONTEXT.es.md); no infieras un nombre oficial.
- **Prioridades y alcance:** no se ha decidido qué departamentos, workflows e hitos abordará primero el proyecto.
- **Criterios de éxito:** hay que acordar líneas base, metas, fuentes de medición y umbrales de aceptación antes de poder verificar la entrega.
- **Expectativas de servicio:** el briefing indica que el agente de experiencia del cliente, el portal de seguimiento y el dashboard de operaciones deben estar disponibles de forma continua (24/7). No define un SLA ni una meta cuantificada de disponibilidad. El soporte en español e inglés es opcional o recomendable en algunas áreas; no se ha definido un idioma predeterminado para el proyecto.

## Fuentes

- [`BRIEFING.md`](../BRIEFING.md): descripción de la compañía, problemas actuales, necesidades por departamento y mandato de TrackFlow Tech.
- [`company-choice.md`](../company-choice.md): motivación del estudiante y propuesta inicial de solución.
- [`CONTEXT.md`](../CONTEXT.md) y [`CONTEXT.es.md`](../CONTEXT.es.md): contexto empresarial y del dominio, incluidas las discrepancias conocidas en las fuentes.
