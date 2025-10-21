## 📘 Tutorial Básico de Django (Linux & Windows)

Este tutorial te guía paso a paso para instalar Django, crear tu primer proyecto y conocer los comandos esenciales.

---

## 1. Instalación

### 🔹 Requisitos previos

* Tener instalado **Python 3.8+**
* Se recomienda usar un **entorno virtual (venv)**

### 🔹 En Linux / Windows (con terminal)

```bash
# Crear entorno virtual
python3 -m venv env

# Activar entorno (Linux)
source env/bin/activate

# Activar entorno (Windows)
.\env\Scripts\activate

# Instalar Django
pip install django
```

Verificar versión instalada:

```bash
django-admin --version
```

---

## 2. Crear un proyecto Django

```bash
django-admin startproject miweb
cd miweb
```

Estructura inicial:

```
miweb/
├── manage.py
└── miweb/
    ├── __init__.py
    ├── settings.py
    ├── urls.py
    └── wsgi.py
```

---

## 3. Ejecutar el servidor

```bash
python manage.py runserver
```

Abre tu navegador en:
👉 [http://127.0.0.1:8000/](http://127.0.0.1:8000/)

---

## 4. Crear una app

```bash
python manage.py startapp miapp
```

Agregar la app al archivo `settings.py`:

```python
INSTALLED_APPS = [
    ...,
    'miapp',
]
```

---

## 5. Comandos útiles de Django

| Comando                            | Descripción                             |
| ---------------------------------- | --------------------------------------- |
| `python manage.py runserver`       | Ejecutar el servidor                    |
| `python manage.py startapp nombre` | Crear una nueva aplicación              |
| `python manage.py makemigrations`  | Preparar cambios de modelo para migrar  |
| `python manage.py migrate`         | Aplicar migraciones a la base de datos  |
| `python manage.py createsuperuser` | Crear usuario administrador             |
| `python manage.py shell`           | Consola interactiva con acceso a Django |

---

## 6. Machete Resumido

```bash
python3 -m venv env
source env/bin/activate
pip install django
django-admin startproject miweb
cd miweb
python manage.py runserver
python manage.py startapp miapp
```

---

## 7. Conclusión

* Django permite crear aplicaciones web completas de forma rápida y estructurada.
* Usa el patrón **MTV** (Modelo - Template - Vista).
* Organiza tu proyecto en **apps reutilizables**.
* El entorno virtual te permite aislar dependencias.
* La consola de Django (`manage.py`) centraliza todos los comandos.

---

