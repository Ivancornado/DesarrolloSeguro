# Incorporación de S-SDLC y DevSecOps en el proyecto

## 1. Introducción

En esta actividad incorporamos la metodología S-SDLC y el enfoque DevSecOps al proyecto Secure To-Do Application.

El objetivo es integrar la seguridad durante todo el ciclo de vida de la aplicación, desde la planificación inicial hasta el despliegue y mantenimiento. De esta forma, la seguridad no se revisa únicamente al final, sino que forma parte de cada fase del desarrollo.

## 2. Aplicación seleccionada

La aplicación utilizada es Secure To-Do Application, una aplicación web sencilla para la gestión de tareas.

Sus funcionalidades principales son:

* Visualizar tareas.
* Crear tareas.
* Editar tareas.
* Eliminar tareas.
* Marcar tareas como completadas.

Esta aplicación sirve como proyecto tipo para aplicar medidas de desarrollo seguro y prácticas DevSecOps.

## 3. Aplicación del S-SDLC

Aplicamos el Secure Software Development Life Cycle siguiendo varias fases:

### Requisitos

Identificamos los requisitos funcionales de la aplicación y también los requisitos de seguridad.
Entre los requisitos de seguridad se incluyen la validación de entradas, la protección frente a XSS, la prevención de inyecciones SQL y la gestión segura de errores.

### Diseño

Durante el diseño analizamos las amenazas principales que pueden afectar a la aplicación.

Las amenazas más relevantes son:

* Cross-Site Scripting (XSS).
* Inyección SQL.
* Acceso no autorizado.
* Dependencias vulnerables.
* Denegación de servicio.

### Desarrollo

Durante el desarrollo aplicamos buenas prácticas de programación segura.
Entre ellas se incluyen mantener una estructura clara del proyecto, separar el código de la documentación, evitar mostrar información sensible y preparar la aplicación para futuras validaciones de entrada.

### Pruebas

Definimos pruebas de seguridad para comprobar posibles vulnerabilidades.

Algunas pruebas previstas son:

* Pruebas frente a XSS.
* Pruebas frente a inyección SQL.
* Revisión de dependencias.
* Comprobación de errores.
* Validación del correcto despliegue en Docker.

### Despliegue

La aplicación se despliega mediante Docker utilizando una imagen basada en Nginx.
Esto permite ejecutar la aplicación en un entorno controlado, aislado y reproducible.

### Mantenimiento

Durante el mantenimiento revisaremos posibles vulnerabilidades, actualizaremos dependencias y documentaremos los cambios realizados en el proyecto.

## 4. Incorporación de DevSecOps

DevSecOps consiste en integrar la seguridad dentro del proceso de desarrollo, operación y despliegue de software.
En nuestro proyecto aplicamos DevSecOps incorporando controles de seguridad en cada fase del ciclo de vida.

### Planificación

En esta fase identificamos requisitos de seguridad y posibles riesgos desde el inicio del proyecto.

### Desarrollo

Durante el desarrollo seguimos buenas prácticas de programación segura y mantenemos el código organizado.

### Integración

En una evolución del proyecto, el repositorio podría incluir análisis automáticos de seguridad mediante GitHub Actions.

### Pruebas de seguridad

Se podrían utilizar herramientas automáticas para revisar vulnerabilidades, dependencias y configuración del contenedor.

Ejemplos de herramientas:

* Trivy.
* Docker Scout.
* GitHub Dependabot.
* OWASP Dependency-Check.
* SonarQube.

### Despliegue

El uso de Docker permite desplegar la aplicación de forma controlada y repetir el mismo entorno en diferentes equipos.

### Monitorización

Después del despliegue se revisarían alertas de seguridad, actualizaciones de dependencias y posibles errores detectados.

## 5. Diagrama del proceso

El flujo propuesto para aplicar S-SDLC y DevSecOps es el siguiente:

```text
Planificación segura
        ↓
Diseño seguro
        ↓
Desarrollo seguro
        ↓
Análisis automático de seguridad
        ↓
Pruebas de seguridad
        ↓
Despliegue con Docker
        ↓
Monitorización y mantenimiento
        ↺
```

## 6. Beneficios de aplicar DevSecOps

La incorporación de DevSecOps en el proyecto nos permite:

* Detectar vulnerabilidades antes.
* Reducir riesgos de seguridad.
* Automatizar revisiones de seguridad.
* Mejorar la calidad del código.
* Facilitar el mantenimiento.
* Tener un despliegue más controlado y reproducible.

## 7. Conclusión

Con la aplicación de S-SDLC y DevSecOps conseguimos integrar la seguridad desde las primeras fases del proyecto. Esto permite que la aplicación no solo funcione correctamente, sino que también tenga una base más segura, mantenible y preparada para futuras mejoras.
