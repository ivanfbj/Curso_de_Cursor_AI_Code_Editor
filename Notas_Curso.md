# Curso de Cursor AI Code Editor

Configura contextos dinámicos, reglas personalizadas de automatización y arquitecturas limpias. Integra pruebas unitarias y E2E usando Jest, Pytest y Playwright con MCP (Model Context Protocol). Optimiza entornos profesionales en Docker, Xcode y Android Studio.

## Clase 1 - Desarrollo de aplicaciones multiplataforma en tiempos récord

**Resumen:**

Crear una aplicación móvil para Android e iOS en poco tiempo puede parecer complicado, especialmente cuando requiere backend, frontend y desarrollo nativo. Sin embargo, herramientas modernas como Cursor pueden facilitar su desarrollo considerablemente, siempre que exista una planificación estratégica adecuada para evitar errores comunes como datos incorrectos o vulnerabilidades.

**¿Qué necesitamos para desarrollar una aplicación multiplataforma rápido?**

Lo primero es establecer claramente cuál será el comportamiento de la aplicación, especificando:

- Qué acciones realizará cada una de sus funciones.
- Cuáles serán los endpoints necesarios.
- Cómo se manejará el "contrato" de comunicación entre los distintos componentes.

Esto permite que varios desarrolladores trabajen en paralelo sin conflictos en la integración final.

**¿Qué ventajas ofrece Cursor en el desarrollo ágil?**

La herramienta Cursor promete aumentar significativamente la rapidez y eficiencia del proceso de desarrollo de software, incluso en proyectos complejos y exigentes. Algunas ventajas mencionadas son:

- Mayor eficiencia y rapidez en la escritura de código.
- Posibilidad de avanzar velozmente por su estructura y funciones automatizadas.

No obstante, es necesario tener claro que cualquier código generado de manera automatizada debe ser revisado cuidadosamente por el equipo técnico.

**¿Cómo evitar riesgos en el desarrollo con automatización?**

Si bien herramientas como Cursor son eficientes, presentan riesgos como el ingreso de código basura o vulnerabilidades potenciales. Para enfrentar estos desafíos es crítico:

- Supervisar todo el código generado.
- Testear rigurosamente cada funcionalidad.
- Asegurar que se mantenga un alto estándar de calidad.
La colaboración del equipo y la verificación constante son fundamentales para que el proyecto resulte exitoso.

Te invitamos a compartir en los comentarios tus experiencias usando herramientas como Cursor, ¿qué estrategias empleas para asegurar la calidad de tu producto final?

**Anexo:**

Los “contratos” se refieren a las especificaciones técnicas y estructurales que regulan la comunicación y los intercambios de datos entre componentes del sistema.
Establecer estos contratos es clave para el desarrollo ágil, especialmente en entornos automatizados y colaborativos.

## Clase 2 - Stack tecnológico para plataforma educativa online

**Resumen:**

Para construir una aplicación web y móvil adecuada como Platziflix, debemos seleccionar cuidadosamente el stack tecnológico según las necesidades y objetivos del proyecto. En este caso concreto, utilizaremos TypeScript, CSS Modules y SaaS para frontend, Swift y Swift UI para nuestra aplicación móvil en iOS, y Kotlin y Jetpack para la app nativa Android. Finalmente, Python con FASTAPI y PostgreSQL serán la base para nuestro backend.

**¿Cuál es el stack tecnológico seleccionado para frontend y aplicaciones móviles?**

Al no existir restricciones para seleccionar tecnologías, definimos claramente el stack que mejor se adapta a las necesidades del proyecto:

- **Frontend:** TypeScript, CSS Modules y SaaS para una aplicación web organizada, escalable y fácil de mantener.
- **Aplicación móvil:**
iOS: Swift y Swift UI, aprovechando herramientas nativas optimizadas para Apple.
Android: Kotlin con Jetpack, manteniendo un desarrollo robusto y nativo.

**¿Qué stack es ideal para el backend y la base de datos?**

Para el backend proponemos:

- Python junto al framework FASTAPI.
- Base de datos PostgreSQL.

Esta combinación ofrece ventajas significativas en cuanto a rendimiento, facilidad de desarrollo y flexibilidad de estructura.

**¿Cuáles son las entidades principales y cómo se definen sus contratos JSON?**

Es fundamental definir claramente entidades y sus estructuras de datos. Las principales entidades identificadas fueron: curso, clase y profesor.

### ¿Qué detalles incluir en cada entidad?  

- **Curso:**
- ID numérico autoincremental.
- Nombre, descripción, thumbnail y slug.
- ID vinculado a docentes.
- Campos de auditoría: creación, edición y eliminación lógica (`deletedat`).  

- **Clase:**
- ID numérico.
- Pertenece a un curso específico (course ID).
- Nombre, descripción, URL del video, slug.
- Campos de auditoría similares a los del curso.  

- **Profesor:**
- ID numérico.
- Nombre y correo electrónico.
- Campos de auditoría, siguiendo el estándar definido en las otras entidades.  

**¿Qué endpoints son necesarios para la API?**

Para un consumo eficiente desde las aplicaciones, definimos un grupo claro de endpoints con respuestas explicadas para cada caso:

### **¿Cómo listar cursos adecuadamente?**

La lista de cursos contiene información esencial:

- ID numérico.
- Nombre del curso.
- Thumbnail.
- Slug único del curso.
- Descripción breve.

**¿Qué información requiere el endpoint del detalle del curso?**

Al solicitar detalles específicos de un curso, se incluirá:

- ID, nombre completo, descripción detallada.
- Slug del curso.
- Lista de IDs para profesores asociados.
- Listado de clases con información básica: ID, nombre, slug y descripción.

### **¿Qué retornar en el detalle específico de una clase?**

Los datos requeridos en el detalle de una clase son:

- ID numérico y slug único.
- Nombre y descripción clara.
- URL del video.
- Campos de auditoría (`createdat`, `updatedat`, `deletedat`).

Finalmente, consideramos importante utilizar slugs para las rutas de cursos, mientras que para las clases individuales usaremos IDs, asegurando así el manejo eficiente de información repetida.

Este criterio y planificación inicial es suficiente para establecer una base sólida y arrancar el proceso de desarrollo técnico.

**Anexo:**

Un slug es una cadena de texto amigable usada para identificar de forma única cursos o clases en URLs, generalmente derivada del nombre original, transformada a minúsculas, sin espacios ni caracteres especiales.

Por ejemplo el slug para "introduccion-a-la-programacion-con-python" podría ser "introduccion-a-la-programacion-con-python".

## Clase 3 - Configuración de contexto y reglas en Cursor para FastAPI

**Resumen:**

Configurar correctamente el contexto y las reglas de un proyecto es esencial al trabajar con inteligencia artificial para generar código efectivo. En este caso, aprenderás cómo establecer la estructura inicial del backend con FastAPI, Python y Postgres en la plataforma Cursor, asegurando un ambiente claro y simplificado.

**¿Por qué es importante el archivo README en markdown?**

El archivo README actúa como el contexto principal que explica el proyecto en un lenguaje accesible. Este documento no solo facilita que nuevos desarrolladores entiendan rápidamente el funcionamiento y propósito del proyecto, sino que también permite a la inteligencia artificial interpretar claramente la base sobre la cual generará el código.

### **¿Qué debe contener el README del backend?**

Para este proyecto específico, PlatziFlix, la descripción principal define que es una plataforma online de cursos sencilla y directa, enfocada en funcionalidades básicas. Además, especifica detalladamente el stack tecnológico:

- **Lenguaje principal**: Python.
- **Framework web**: FastAPI.
- **Base de datos relacional**: Postgres.
- **Contenedorización**: Docker.

La arquitectura del backend incluye el uso de FastAPI para exponer y consumir información almacenada en una base de datos Postgres hacia aplicaciones web y móviles.

**¿Qué rol juegan las reglas en Cursor para el proyecto?**

Definir reglas en Cursor ayuda a mantener un estándar claro durante el desarrollo, facilitando la generación precisa de código mediante inteligencia artificial. Las reglas pueden configurarse para ser:

- Siempre aplicables.
- Asociadas automáticamente a patrones específicos de archivo.
- Solicitadas manualmente por el desarrollador o el agente de Cursor.

### **¿Cómo crear y aplicar reglas de proyecto en Cursor?**

Para configurar reglas:

1. Ingresa a la sección project rules en los ajustes de Cursor.
2. Define el nombre que representará claramente el propósito de la regla, como "FastAPI".
3. Decide el tipo de regla, como aquellas que se auto-agregan por tipo de archivo.
4. Utiliza recursos disponibles como cursor.directory para encontrar reglas creadas por la comunidad que calcen con tus necesidades.

La ventaja principal es adaptar rápidamente reglas ya probadas por otros desarrolladores para diferentes contextos, acelerando el desarrollo y manteniendo calidad y simplicidad en el código generado.

**¿Cuáles son las recomendaciones principales antes de generar código con Cursor?**

- Crear un README claro y detallado en formato markdown que describa perfectamente la idea del proyecto con términos fácilmente comprensibles.
- Establecer reglas precisas en Cursor, preferiblemente utilizando o adaptando reglas ya diseñadas por la comunidad.
- Garantizar que estas reglas y contextos estén correctamente configurados antes de iniciar la generación de código.

Te animo a ajustar estas reglas según consideres necesario para optimizar aún más tu proceso de desarrollo con inteligencia artificial, y compártelas posteriormente para seguir enriqueciendo este aprendizaje en comunidad.

**Anexo:**

- [Documentación de reglas](https://docs.cursor.com/context/rules)
- [Reglas creadas por la comunidad](https://cursor.directory/rules/)
