# Evaluación de seguridad mediante herramientas automáticas

## 1. Introducción

En esta actividad realizamos una evaluación de seguridad sobre la aplicación Secure To-Do Application utilizando diferentes herramientas y técnicas de análisis automatizado.

El objetivo fue identificar posibles vulnerabilidades, errores de configuración y riesgos de seguridad que pudieran afectar a la aplicación o a su entorno de ejecución.

## 2. Despliegue de la aplicación

Antes de realizar las pruebas, desplegamos la aplicación utilizando Docker para verificar su correcto funcionamiento.

La aplicación fue construida mediante una imagen Docker basada en Nginx y posteriormente ejecutada en un contenedor local.

Durante la validación comprobamos que la aplicación era accesible desde el navegador y que el contenedor se encontraba en ejecución.

Las evidencias de este proceso se incluyen mediante capturas de pantalla de la aplicación funcionando y del estado del contenedor Docker.

## 3. Herramientas de seguridad evaluadas

### 3.1 Trivy

Trivy es una herramienta de análisis de seguridad utilizada para detectar vulnerabilidades en imágenes Docker, dependencias y configuraciones.

Su función principal es identificar componentes vulnerables antes de desplegar una aplicación en producción.

### 3.2 Docker Scout

Docker Scout permite analizar imágenes Docker para detectar vulnerabilidades conocidas y obtener recomendaciones de mejora.

Esta herramienta ayuda a mantener actualizadas las imágenes utilizadas durante el despliegue.

### 3.3 GitHub Dependabot

GitHub Dependabot permite detectar dependencias vulnerables y proponer actualizaciones automáticas cuando se encuentran problemas de seguridad conocidos.

Su integración con GitHub facilita el mantenimiento continuo del proyecto.

### 3.4 OWASP Dependency-Check

OWASP Dependency-Check analiza librerías y componentes utilizados por una aplicación para identificar vulnerabilidades conocidas registradas en bases de datos públicas.

Esta herramienta ayuda a reducir riesgos asociados al uso de software de terceros.

### 3.5 SonarQube

SonarQube es una plataforma de análisis estático de código que permite detectar errores, problemas de calidad y posibles vulnerabilidades de seguridad.

Su utilización facilita la identificación temprana de problemas durante el desarrollo.

## 4. Resultados obtenidos

Debido a la simplicidad de la aplicación desarrollada, no se detectaron vulnerabilidades funcionales significativas durante la evaluación.

La aplicación está compuesta por una página HTML sencilla servida mediante Nginx dentro de un contenedor Docker, por lo que la superficie de ataque es reducida.

No obstante, las herramientas seleccionadas permiten evaluar aspectos importantes relacionados con:

* Vulnerabilidades en imágenes Docker.
* Dependencias vulnerables.
* Errores de configuración.
* Calidad y seguridad del código.
* Actualizaciones de componentes.

## 5. Riesgos identificados

Durante el análisis se identificaron los siguientes riesgos potenciales:

* Uso de imágenes Docker desactualizadas.
* Dependencias con vulnerabilidades conocidas.
* Configuraciones inseguras en futuros despliegues.
* Falta de validación de entradas si la aplicación evoluciona e incorpora formularios.

Aunque estos riesgos no afectan actualmente a la aplicación desarrollada, deben considerarse en futuras versiones del proyecto.

## 6. Medidas de mitigación

Para reducir los riesgos identificados proponemos las siguientes medidas:

* Mantener actualizadas las imágenes Docker utilizadas.
* Revisar periódicamente las dependencias del proyecto.
* Automatizar análisis de seguridad mediante herramientas DevSecOps.
* Aplicar validación de entradas en futuras funcionalidades.
* Realizar pruebas de seguridad de forma periódica.

## 7. Evidencias

Como parte de la evaluación se generaron evidencias que demuestran:

* La correcta construcción de la imagen Docker.
* La ejecución del contenedor.
* El funcionamiento de la aplicación desde el navegador.

Estas evidencias permiten verificar que la aplicación puede desplegarse correctamente y servir como base para futuros análisis de seguridad.

## 8. Conclusión

La evaluación realizada demuestra la importancia de incorporar herramientas automáticas de seguridad dentro del ciclo de desarrollo de software.

Aunque la aplicación desarrollada es sencilla, el uso de herramientas como Trivy, Docker Scout, GitHub Dependabot, OWASP Dependency-Check y SonarQube permite establecer una base sólida para detectar vulnerabilidades y mejorar la seguridad de futuras versiones del proyecto.

La incorporación de estas herramientas contribuye a reforzar la estrategia DevSecOps y facilita la identificación temprana de riesgos durante el ciclo de vida del software.
