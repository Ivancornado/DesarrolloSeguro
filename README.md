# Secure To-Do Application

## Descripción

Secure To-Do Application es una aplicación web sencilla para la gestión de tareas. Permite visualizar una lista de tareas y sirve como proyecto de referencia para aplicar principios de desarrollo seguro mediante la metodología Secure Software Development Life Cycle (S-SDLC).

## Tecnologías utilizadas

* HTML
* Docker
* Nginx

## Ejecución de la aplicación

1. Acceder a la carpeta de la aplicación:

```bash
cd app
```

2. Construir la imagen Docker:

```bash
docker build -t secure-todo .
```

3. Ejecutar el contenedor:

```bash
docker run -d -p 8080:80 secure-todo
```

4. Abrir un navegador y acceder a:

```text
http://localhost:8080
```

La aplicación nos muestra una página web sencilla con las funcionalidades básicas de una aplicación de gestión de tareas.
