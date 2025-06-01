
#  Proyecto Flask: Lista de Tareas

Este proyecto es una aplicación web desarrollada con **Flask**, un microframework de Python, que permite gestionar una lista de tareas. Incluye funcionalidades para **crear**, **listar**, **editar** y **eliminar** tareas almacenadas en una base de datos **SQLite** mediante **SQLAlchemy**.

---

##  Objetivo

El objetivo del proyecto es demostrar el uso de Flask con SQLAlchemy para construir una aplicación CRUD básica. Esta aplicación puede ser utilizada como base para proyectos más complejos, y está diseñada con una estructura clara para facilitar su despliegue, por ejemplo, en plataformas como **Render**.

---

##  Tecnologías utilizadas

- Python 3.x
- Flask 3.1.1
- Flask-SQLAlchemy 3.1.0
- SQLite (como base de datos)
- HTML5 y CSS3 (para la interfaz de usuario)
- Gunicorn (para despliegue en producción)
- Render (opcional, para hosting en la nube)

---

##  Funcionalidades implementadas

-  Crear nuevas tareas con contenido personalizado.
-  Listar todas las tareas, ordenadas por fecha de creación.
-  Editar contenido de tareas existentes.
-  Eliminar tareas.
-  Guardado automático de fecha de creación.
-  Interfaz web sencilla y funcional.

---

##  Estructura del proyecto

```
/flaskpro/
│
├── app.py             # Código principal de la aplicación Flask
├── test.db            # Base de datos SQLite generada automáticamente
├── templates/
│   ├── index.html     # Página principal con lista de tareas
│   └── update.html    # Página para actualizar tareas
├── static/            # Carpeta para CSS (opcional)
│   └── style.css
├── requirements.txt   # Lista de dependencias del proyecto
├── Procfile           # Archivo necesario para despliegue en Render
└── README.md          # Documentación del proyecto
```

---

## Cómo ejecutar el proyecto localmente

1. **Clona el repositorio:**
   ```bash
   git clone
   cd flaskpro
   ```

2. **Crea un entorno virtual e instala las dependencias:**
   ```bash
   python -m venv venv
   source venv/bin/activate  # En Windows: venv\Scripts\activate
   pip install -r requirements.txt
   ```

3. **Inicializa la base de datos:**
   Puedes simplemente ejecutar `app.py`, o usar un script externo como `init_db.py`:
   ```python
   from app import app, db
   with app.app_context():
       db.create_all()
   ```

4. **Ejecuta la aplicación:**
   ```bash
   flask run  
   ```
    https://github.com/GIO239902/tarea-2.1
---

##  Despliegue en Render

Para desplegar en [Render](https://render.com/):

- Asegúrate de tener `Procfile` con el siguiente contenido:
  ```
  web: gunicorn app:app
  ```

- Sube tu proyecto a un repositorio de GitHub y conéctalo en Render.

---

##  Notas adicionales

- La base de datos `test.db` se crea automáticamente si no existe.
- Puedes personalizar los estilos HTML/CSS en la carpeta `static/`.

---

##  Licencia

Este proyecto está disponible para uso académico y personal bajo licencia MIT.

---

##  Contacto

Autor: giovani blanco flores 
Correo: giovaniblanco99@gmail.com  
link: https://tarea-2-1.onrender.com
