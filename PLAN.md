# Plan resumido de la web Health&IVD

## Objetivo

Completar y validar la web corporativa existente según
[ESPECIFICACIONES.md](./ESPECIFICACIONES.md), conservando su diseño y arquitectura
estática en HTML y CSS, sin añadir frameworks ni servidor de aplicaciones.

## Fases

| Orden | Fase | Acciones principales | Resultado esperado |
| --- | --- | --- | --- |
| 1 | Alinear el contexto | Confirmar Health&IVD como producto y acordar la corrección del contexto de TaskFlow en [memory-bank](./memory-bank/product-context.md). | Contexto coherente con la web y las especificaciones. |
| 2 | Revisar contenidos | Validar textos comerciales, referencias QARA e indicadores con la persona responsable del contenido. Mantener claramente identificados los valores ilustrativos. | Contenido aprobado, sin atribuir certificaciones o resultados no acreditados. |
| 3 | Completar información legal | Obtener textos revisados de aviso legal y privacidad e implementar sus destinos. | Ambos enlaces permiten consultar el contenido correspondiente. |
| 4 | Comprobar el contacto | Confirmar el destinatario, verificar campos obligatorios y correo inválido, y probar `mailto:` con un cliente configurado. Acordar cualquier alternativa antes de implementarla. | Canal de contacto probado y limitaciones de entrega documentadas. |
| 5 | Validar la experiencia | Revisar anclas, menú móvil, foco de teclado, contraste y distribución a 375, 700, 960 y 1280 px. Comprobar el comportamiento sin fuentes o imagen externas. | Resultados registrados y problemas que impidan el uso corregidos. |
| 6 | Preparar la publicación | Probar en un servidor estático, verificar recursos y metadatos, y documentar los pasos de publicación en el [README](./README.md). | Versión revisada y lista para publicar en el alojamiento acordado. |

Las fases 2 y 3 pueden avanzar en paralelo tras alinear el contexto. La revisión
final debe realizarse después de completar contenidos, enlaces legales y contacto.

## Criterios de finalización

- [ ] Contexto y contenido aprobados para Health&IVD.
- [ ] Aviso legal y privacidad accesibles.
- [ ] Formulario validado, sin confundir la apertura del correo con su entrega.
- [ ] Navegación, adaptación móvil y accesibilidad comprobadas.
- [ ] Recursos externos y carga desde un servidor estático revisados.
- [ ] Resultados de las comprobaciones y pasos de publicación documentados.

## Límites

Este plan no ejecuta cambios en la web. No incluye TaskFlow, autenticación,
comercio electrónico, base de datos ni tratamiento de datos clínicos. La
publicación queda pendiente de aprobar el contenido y elegir el alojamiento.
