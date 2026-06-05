# Evaluación de seguridad mediante herramientas automáticas

## 1. Introducción

En esta actividad realizamos una evaluación de seguridad sobre la aplicación Secure To-Do Application utilizando diferentes herramientas y técnicas de análisis automatizado.

El objetivo fue identificar posibles vulnerabilidades, errores de configuración y riesgos de seguridad que pudieran afectar tanto a la aplicación como a su entorno de ejecución.

Para ello desplegamos la aplicación mediante Docker y analizamos la imagen generada utilizando herramientas de seguridad orientadas a entornos DevSecOps.

## 2. Despliegue de la aplicación

Antes de realizar las pruebas de seguridad desplegamos la aplicación utilizando Docker para verificar su correcto funcionamiento.

La aplicación fue construida mediante una imagen Docker basada en Nginx y posteriormente ejecutada en un contenedor local.

Durante la validación comprobamos que la aplicación era accesible desde el navegador a través de la dirección:

```text
http://localhost:8080
```

También verificamos que el contenedor se encontraba en ejecución mediante el comando:

```bash
sudo docker ps
```

Las capturas obtenidas durante este proceso se incluyen como evidencias de funcionamiento.

## 3. Herramientas de seguridad evaluadas

### 3.1 Trivy

Trivy es una herramienta de análisis de seguridad utilizada para detectar vulnerabilidades en imágenes Docker, dependencias y configuraciones.

Su principal objetivo es identificar componentes vulnerables antes de desplegar una aplicación en producción.

### 3.2 Docker Scout

Docker Scout permite analizar imágenes Docker para detectar vulnerabilidades conocidas y obtener recomendaciones de mejora relacionadas con las imágenes utilizadas.

### 3.3 GitHub Dependabot

GitHub Dependabot permite detectar dependencias vulnerables y proponer actualizaciones automáticas cuando se identifican problemas de seguridad conocidos.

### 3.4 OWASP Dependency-Check

OWASP Dependency-Check analiza componentes y librerías utilizadas por una aplicación para identificar vulnerabilidades registradas en bases de datos públicas.

### 3.5 SonarQube

SonarQube es una plataforma de análisis estático de código que permite detectar errores de programación, problemas de calidad y posibles vulnerabilidades de seguridad.

## 4. Análisis práctico realizado con Trivy

Para realizar una evaluación real de seguridad sobre la aplicación utilizamos Trivy para analizar la imagen Docker generada.

El comando ejecutado fue:

```bash
sudo trivy image secure-todo
```

La herramienta analizó la imagen Docker y los componentes incluidos dentro del contenedor.

## 5. Resultados obtenidos

El análisis realizado sobre la imagen Docker produjo los siguientes resultados:

* Imagen analizada: secure-todo
* Sistema operativo detectado: Alpine Linux 3.23.4
* Vulnerabilidades detectadas: 1
* Secretos expuestos detectados: 0

El análisis permitió comprobar que no existían credenciales, contraseñas ni secretos expuestos dentro de la imagen analizada.

Sin embargo, se detectó una vulnerabilidad de severidad alta asociada a una librería incluida en la imagen.

### Vulnerabilidad detectada

* Vulnerabilidad: CVE-2026-6732
* Severidad: HIGH
* Biblioteca afectada: libxml2
* Versión instalada: 2.13.9-r0
* Versión corregida: 2.13.9-r1

Descripción:

La vulnerabilidad identificada afecta a la librería libxml2 y puede permitir ataques de denegación de servicio (DoS) mediante el procesamiento de documentos XML especialmente manipulados.

Aunque la aplicación desarrollada no procesa directamente documentos XML, la presencia de esta vulnerabilidad demuestra la importancia de revisar periódicamente las imágenes Docker utilizadas en los despliegues.

## 6. Medidas de mitigación

Para reducir los riesgos identificados se proponen las siguientes medidas:

* Mantener actualizadas las imágenes Docker utilizadas.
* Actualizar la librería libxml2 a la versión corregida.
* Realizar análisis periódicos mediante Trivy.
* Utilizar herramientas de análisis de dependencias como Dependabot y OWASP Dependency-Check.
* Incorporar controles automáticos de seguridad dentro del flujo DevSecOps.
* Revisar periódicamente las configuraciones de despliegue.

## 7. Evidencias obtenidas

Durante la actividad se generaron las siguientes evidencias:

* Captura de la aplicación ejecutándose correctamente en el navegador.
* Captura del contenedor Docker en ejecución mediante el comando docker ps.
* Resultado del análisis de seguridad realizado con Trivy.
* Identificación de una vulnerabilidad real dentro de la imagen Docker utilizada.

Estas evidencias demuestran que la aplicación fue desplegada correctamente y que se realizó una evaluación de seguridad real sobre el entorno de ejecución.

## 8. Conclusión

La evaluación realizada demuestra la utilidad de incorporar herramientas automáticas de seguridad dentro del ciclo de vida del software.

El uso de Trivy permitió detectar una vulnerabilidad real de severidad alta presente en una dependencia incluida dentro de la imagen Docker utilizada por la aplicación.

Además, el estudio de herramientas como Docker Scout, GitHub Dependabot, OWASP Dependency-Check y SonarQube permite establecer una base sólida para futuras estrategias DevSecOps.

La incorporación de este tipo de herramientas facilita la detección temprana de vulnerabilidades, mejora la seguridad del proyecto y contribuye a reducir los riesgos antes de que la aplicación sea desplegada en entornos de producción.
