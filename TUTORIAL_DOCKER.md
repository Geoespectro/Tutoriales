# 📘 Tutorial Básico de Docker (Linux & Windows)

Este tutorial explica cómo instalar, configurar y usar Docker tanto en **Linux (Ubuntu)** como en **Windows**, además de los conceptos básicos y los comandos esenciales.

---

## 1. Instalación de Docker

### 🔹 En Linux (Ubuntu)
```bash
sudo apt update
sudo apt install docker.io -y
````

Activar Docker al inicio y arrancar el servicio:

```bash
sudo systemctl enable docker
sudo systemctl start docker
```

Verificar instalación:

```bash
docker --version
```

---

### 🔹 En Windows

1. Descargar **Docker Desktop** desde 👉 [https://www.docker.com/products/docker-desktop](https://www.docker.com/products/docker-desktop).
2. Requisitos: Windows 10/11 con **WSL2 habilitado**.
3. Instalar y reiniciar el sistema.
4. Verificar instalación en PowerShell:

```powershell
docker --version
```

---

## 2. Docker Hub

* **Qué es:** repositorio oficial de imágenes (como GitHub, pero para contenedores).
* Crear una cuenta gratuita en 👉 [hub.docker.com](https://hub.docker.com).
* Iniciar sesión desde terminal:

```bash
docker login
```

---

## 3. Conceptos Básicos

* **Docker:** plataforma que permite ejecutar aplicaciones en contenedores, asegurando portabilidad.
* **Imagen:** plantilla que contiene un sistema + app (ej: `ubuntu`, `python:3.10`).
* **Contenedor:** instancia de una imagen en ejecución (como una mini-computadora).

### 🔹 ¿Por qué abrir una terminal dentro de un contenedor?

Abrir una terminal te permite:

* Inspeccionar archivos y carpetas dentro del contenedor.
* Ejecutar comandos para verificar dependencias.
* Depurar tu aplicación si algo falla.

Ejemplo:

```bash
docker exec -it NOMBRE_O_ID bash
```

---

## 4. Comandos Principales

### Imágenes

```bash
docker pull ubuntu        # Descargar imagen
docker images             # Listar imágenes
docker rmi ubuntu         # Eliminar imagen
```

### Contenedores

```bash
docker run -it ubuntu bash   # Crear y abrir contenedor interactivo
docker run -d ubuntu         # Ejecutar en segundo plano
docker ps                    # Ver contenedores activos
docker ps -a                 # Ver todos los contenedores
docker stop ID               # Parar contenedor
docker rm ID                 # Eliminar contenedor
```

### Acceso y logs

```bash
docker exec -it ID bash      # Abrir terminal dentro de contenedor
docker logs ID               # Ver logs
```

### Construcción de imágenes

```bash
docker build -t mi_imagen .
```

### Limpieza

```bash
docker container prune   # Eliminar contenedores detenidos
docker image prune       # Eliminar imágenes sin usar
docker system prune      # Limpiar todo
```

---

## 5. Machete Resumido

| Comando                    | Descripción                 |
| -------------------------- | --------------------------- |
| `docker pull nombre`       | Descargar imagen            |
| `docker run nombre`        | Crear y ejecutar contenedor |
| `docker ps`                | Ver contenedores activos    |
| `docker ps -a`             | Ver todos los contenedores  |
| `docker stop ID`           | Parar contenedor            |
| `docker rm ID`             | Eliminar contenedor         |
| `docker images`            | Ver imágenes                |
| `docker rmi nombre`        | Eliminar imagen             |
| `docker exec -it ID bash`  | Abrir terminal dentro       |
| `docker build -t nombre .` | Construir imagen            |
| `docker system prune`      | Limpiar recursos            |

---

## 6. Conclusión

* Docker es esencial para ejecutar apps en entornos aislados.
* Los contenedores garantizan que tu aplicación corra igual en cualquier máquina.
* Docker Hub es la “nube” de imágenes.
* Los comandos básicos te permiten descargar, ejecutar, inspeccionar y limpiar contenedores fácilmente.

---




