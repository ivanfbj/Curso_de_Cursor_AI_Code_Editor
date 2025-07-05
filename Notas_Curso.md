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
