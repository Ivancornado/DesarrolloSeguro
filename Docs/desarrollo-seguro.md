# Aplicación de la metodología Secure Software Development Life Cycle (S-SDLC)

## 1. Selección de la aplicación

Para el desarrollo de esta actividad seleccionamos una aplicación web de gestión de tareas denominada Secure To-Do Application. Esta aplicación permite gestionar tareas de forma sencilla y nos sirve como proyecto base para aplicar principios de desarrollo seguro.

## 2. Identificación de requisitos

Antes de comenzar el desarrollo identificamos tanto los requisitos funcionales como los requisitos de seguridad necesarios para la aplicación.

### Requisitos funcionales

* Visualizar tareas.
* Crear tareas.
* Editar tareas.
* Eliminar tareas.
* Marcar tareas como completadas.

### Requisitos de seguridad

* Validar las entradas proporcionadas por los usuarios.
* Evitar ataques Cross-Site Scripting (XSS).
* Proteger la aplicación frente a posibles inyecciones SQL.
* Evitar la exposición de información sensible mediante mensajes de error.
* Mantener actualizadas las dependencias utilizadas por la aplicación.

## 3. Diseño seguro

Durante la fase de diseño analizamos las posibles amenazas que podrían afectar a la aplicación y estudiamos las medidas necesarias para reducir los riesgos identificados.

Las principales amenazas detectadas fueron:

* Cross-Site Scripting (XSS).
* Inyección SQL.
* Acceso no autorizado.
* Dependencias vulnerables.
* Denegación de servicio.

A partir de este análisis definimos diferentes controles de seguridad para minimizar el impacto de estas amenazas.

## 4. Desarrollo

Durante el desarrollo seguimos buenas prácticas de programación segura con el objetivo de reducir posibles vulnerabilidades.

Entre las medidas consideradas destacan:

* Validación de entradas de usuario.
* Organización clara de la estructura del proyecto.
* Separación entre código y documentación.
* Aplicación del principio de mínimo privilegio.
* Uso de Docker para aislar el entorno de ejecución.

## 5. Pruebas de seguridad

Una vez desarrollada la aplicación definimos diferentes pruebas de seguridad para comprobar su correcto funcionamiento.

Entre ellas se incluyen:

* Pruebas de validación de entradas.
* Pruebas frente a ataques XSS.
* Pruebas frente a inyecciones SQL.
* Revisión de dependencias.
* Comprobación de errores y excepciones.

Estas pruebas nos permiten detectar posibles vulnerabilidades antes del despliegue de la aplicación.

## 6. Despliegue

Para el despliegue utilizamos Docker junto con una imagen basada en Nginx. Esto nos permite ejecutar la aplicación en un entorno controlado, reproducible y fácil de mantener.

Además, el uso de contenedores facilita futuras actualizaciones y simplifica la gestión del proyecto.

## 7. Mantenimiento

Como parte del ciclo de vida seguro del software, realizaremos revisiones periódicas del código, actualizaciones de dependencias y análisis de nuevas vulnerabilidades que puedan aparecer con el tiempo.

También documentaremos los cambios realizados para mantener una adecuada trazabilidad del proyecto.

## Conclusión

Mediante esta actividad aplicamos los principios del Secure Software Development Life Cycle (S-SDLC), incorporando la seguridad desde las primeras fases del desarrollo hasta el despliegue y mantenimiento de la aplicación. De este modo conseguimos una base sólida para desarrollar software de forma más segura y reducir los riesgos asociados a posibles vulnerabilidades.
