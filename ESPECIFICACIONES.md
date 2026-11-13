# Especificaciones de la web Health&IVD

## Alcance

Web corporativa en español sobre soluciones de diagnóstico in vitro, dirigida a
laboratorios y profesionales de la salud. Este documento describe el estado
observado en el código y los puntos pendientes; no certifica su funcionamiento
en navegadores ni la validez de las afirmaciones comerciales.

Fuentes: [página principal](./index.html), [estilos](./styles.css) y
[descripción del repositorio](./README.md).

## Tabla de especificaciones

| ID | Área | Especificación | Estado observado | Criterio de comprobación |
| --- | --- | --- | --- | --- |
| WEB-01 | Estructura | Sitio de una página con cabecera, contenido principal y pie corporativo. | Definido en HTML. | Comprobar que las secciones aparecen en ese orden. |
| WEB-02 | Identidad | Mostrar la marca Health&IVD y contenido en español. | Marca, título y atributo `lang="es"` presentes. | Revisar la marca visible y el título de la pestaña. |
| WEB-03 | Navegación | Acceder a Inicio, Soluciones, Tecnología, QARA y Contacto mediante anclas internas. | Enlaces y destinos presentes; la marca enlaza a Inicio. | Activar cada enlace y comprobar que su destino queda visible bajo la cabecera fija. |
| WEB-04 | Presentación | Incluir propuesta de valor, fotografía de laboratorio y accesos a soluciones y tecnología. | Contenido definido en la sección de inicio. | Comprobar imagen, texto alternativo y destinos de ambas llamadas a la acción. |
| WEB-05 | Soluciones | Presentar diagnóstico molecular, inmunoensayos, Point-of-Care y química clínica. | Cuatro tarjetas con descripción y enlace a Contacto. | Verificar las cuatro áreas y sus enlaces. |
| WEB-06 | Tecnología y QARA | Describir precisión analítica, flujos de trabajo y enfoque de calidad desde el diseño. | Contenido presente; QARA está dentro de Tecnología. | Revisar los textos y el acceso directo desde ambas navegaciones. |
| WEB-07 | Indicadores | Mostrar concordancia analítica y tiempo de respuesta como valores ilustrativos, no como resultados certificados. | Se muestran 99.8 % y menos de 15 minutos con una advertencia. | Comprobar que la advertencia permanece visible y vinculada visualmente a los indicadores. |
| WEB-08 | Contacto | Solicitar nombre, institución, correo electrónico, área de interés y mensaje. | Cinco campos obligatorios con etiquetas; correo de tipo `email`. | Intentar enviar con campos vacíos y con un correo inválido; el navegador debe impedirlo. |
| WEB-09 | Envío | Delegar el contacto en el cliente de correo mediante `mailto:`. | Formulario sin servidor de recepción ni confirmación de entrega. | Probar con un cliente de correo configurado; no interpretar su apertura como entrega confirmada. |
| WEB-10 | Navegación móvil | Usar un menú desplegable nativo sin JavaScript. | Elementos `details` y `summary`; menú móvil visible hasta 700 px. | Abrir y cerrar el menú con ratón, tacto y teclado en una ventana de 700 px o menos. |
| WEB-11 | Diseño adaptable | Adaptar distribución y espaciado a pantallas de escritorio y móviles. | Reglas CSS para anchos máximos de 960 y 700 px, entre otras adaptaciones. | Revisar a 375, 700, 960 y 1280 px que no haya contenido cortado ni desplazamiento horizontal inesperado. |
| WEB-12 | Accesibilidad | Proporcionar estructura semántica, etiquetas de formulario, texto alternativo y estilos de foco. | Recursos presentes en HTML y CSS; conformidad global no evaluada. | Recorrer enlaces, menú y formulario con teclado; revisar foco, nombres accesibles y contraste. |
| WEB-13 | Identidad visual | Utilizar azules, verdes y fondos claros; tipografías Inter y Plus Jakarta Sans. | Variables CSS y carga desde Google Fonts definidas, con alternativa `sans-serif`. | Revisar consistencia visual y legibilidad si las fuentes externas no cargan. |
| WEB-14 | Metadatos | Definir título, descripción, codificación UTF-8 y configuración de ventana adaptable. | Etiquetas presentes en la cabecera del documento. | Inspeccionar el documento servido y comprobar estos metadatos. |
| WEB-15 | Recursos externos | Cargar fuentes desde Google Fonts y la fotografía desde Unsplash. | La presentación completa depende de servicios externos. | Revisar carga con red y comportamiento si se bloquean dichos recursos. |
| WEB-16 | Información legal | Ofrecer aviso legal y política de privacidad con contenido consultable. | Pendiente: los enlaces actuales apuntan a sí mismos y no incluyen documentos legales. | Antes de publicar, comprobar que ambos enlaces muestran el contenido correspondiente. |
| WEB-17 | Arquitectura | Mantener una página estática basada en HTML y CSS. | Sin JavaScript, API, base de datos ni proceso de compilación en los archivos actuales. | Comprobar que un servidor estático permite cargar la página y sus estilos. |

## Pendientes antes de publicar

| Prioridad | Pendiente | Condición de cierre |
| --- | --- | --- |
| Alta | Completar aviso legal y política de privacidad. | Textos revisados y accesibles desde los enlaces correspondientes. |
| Alta | Validar afirmaciones comerciales, referencias regulatorias e indicadores. | Contenido aprobado para los productos y mercados reales, sin presentar ejemplos como evidencia clínica o certificaciones. |
| Alta | Confirmar destinatario de contacto y aceptar las limitaciones de `mailto:` o definir otro mecanismo. | Canal probado y comportamiento de envío documentado sin prometer una entrega no verificada. |
| Media | Ejecutar las comprobaciones visuales, de teclado y de formulario indicadas en la tabla. | Resultados registrados y problemas que impidan el uso resueltos. |
| Media | Corregir la discrepancia del contexto del proyecto. | [El contexto de producto](./memory-bank/product-context.md) describe actualmente TaskFlow; debe acordarse su actualización a Health&IVD antes de usarlo para futuros planes. |

## Fuera de alcance

No se especifican gestión de tareas TaskFlow, autenticación, comercio electrónico,
catálogo conectado a una base de datos ni tratamiento de datos clínicos. Este
documento tampoco añade funcionalidades ni cambia la implementación existente.
