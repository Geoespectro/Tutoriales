### 📘 Tutorial Básico de Git (Linux & Windows)

Este tutorial explica cómo instalar, configurar y usar Git tanto en **Linux (Ubuntu)** como en **Windows**, además de los conceptos básicos y los comandos esenciales.

---

## 1. Instalación de Git

### 🔹 En Linux (Ubuntu)

```bash
sudo apt update
sudo apt install git -y
```

Verificar instalación:

```bash
git --version
```

---

### 🔹 En Windows

1. Descargar **Git for Windows** desde 👉 [https://git-scm.com/download/win](https://git-scm.com/download/win)
2. Instalar con configuración por defecto.
3. Reiniciar si es necesario.
4. Verificar instalación en PowerShell o Git Bash:

```bash
git --version
```

---

## 2. Configuración Inicial

```bash
git config --global user.name "Tu Nombre"
git config --global user.email "tuemail@ejemplo.com"
```

Ver configuración actual:

```bash
git config --list
```

---

## 3. Conceptos Básicos

* **Repositorio:** espacio donde se guarda el historial de cambios de un proyecto.
* **Commit:** punto de guardado con mensaje descriptivo.
* **Branch:** rama paralela para trabajar sin afectar la principal.
* **Remoto:** repositorio en la nube (GitHub, GitLab).

---

## 4. Comandos Principales

### Inicializar repositorio local

```bash
git init
```

### Clonar repositorio remoto

```bash
git clone https://github.com/usuario/repositorio.git
```

### Ver estado

```bash
git status
```

### Agregar cambios

```bash
git add archivo.txt        # Agregar archivo específico
git add .                  # Agregar todos los archivos
```

### Confirmar cambios

```bash
git commit -m "Mensaje descriptivo"
```

### Ver historial

```bash
git log
```

---

### Trabajo con ramas

```bash
git branch                  # Ver ramas
git branch nueva-rama       # Crear nueva rama
git checkout nueva-rama     # Cambiar de rama
git merge otra-rama         # Fusionar ramas
```

---

### Conexión con remoto

```bash
git remote add origin https://github.com/usuario/repositorio.git
git push -u origin main       # Primer push
git push                      # Subir cambios
git pull                      # Traer cambios
```

---

## 5. Machete Resumido

| Comando               | Descripción                   |
| --------------------- | ----------------------------- |
| `git init`            | Crear repo local              |
| `git clone URL`       | Clonar repo remoto            |
| `git status`          | Ver cambios                   |
| `git add archivo`     | Preparar archivos para commit |
| `git commit -m "msg"` | Guardar cambios               |
| `git push`            | Subir al remoto               |
| `git pull`            | Bajar del remoto              |
| `git branch`          | Ver ramas                     |
| `git checkout rama`   | Cambiar de rama               |
| `git merge rama`      | Unir ramas                    |

---

## 6. Conclusión

* Git permite controlar versiones de tu código y colaborar con otros.
* GitHub es la plataforma más usada para alojar repos.
* Los comandos básicos te permiten crear, modificar y compartir tus proyectos.

