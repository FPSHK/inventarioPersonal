# Inventario Personal - Flask + MySQL

Proyecto final para COMP2052. La aplicacion permite a los usuarios registrar y manejar sus articulos personales. Hay tres roles: Admin, Usuario y Owner. Los Owners pueden crear y editar items, los Usuarios pueden verlos, y los Admins manejan los usuarios del sistema.

## Tecnologias

- Flask
- Flask-Login
- MySQL
- SQLAlchemy
- Bootstrap 5
- Jinja2

## Requisitos previos

- Python 3.8 o superior
- MySQL corriendo en localhost:3306
- Un entorno virtual (opcional pero recomendado)

## Como instalar y correr el proyecto

1. Clonar el repositorio

```
git clone https://github.com/TU_USUARIO/inventario_personal.git
cd inventario_personal
```

2. Crear entorno virtual (opcional)

```
python -m venv venv
venv\Scripts\activate.bat
source venv/bin/activate   # Solo en Linux/Mac requiere esto
```

3. Instalar dependencias

```
pip install -r requirements.txt
```

4. Crear la base de datos

```
mysql -u root -p < database_schema/05_inventario.sql
```

5. Crear usuarios de prueba

```
python create_demo_users.py
```

6. Correr la aplicacion

```
python run.py
```

Abrir en el navegador: http://127.0.0.1:5000

## Usuarios de prueba

| Rol     | Email                 | Contrasena |
|---------|-----------------------|------------|
| Admin   | admin@example.com     | admin123   |
| Owner   | owner@example.com     | owner123   |
| Usuario | user@example.com      | user123    |

## Archivos del proyecto

| Archivo                             | Descripcion                                      |
|-------------------------------------|--------------------------------------------------|
| run.py                              | Inicia el servidor Flask                         |
| config.py                           | Configuracion de la base de datos                |
| requirements.txt                    | Paquetes de Python necesarios                    |
| create_demo_users.py                | Crea los usuarios iniciales                      |
| app/models.py                       | Modelos de la base de datos (User, Role, Item)   |
| app/forms.py                        | Formularios del proyecto                         |
| app/routes.py                       | Rutas principales del CRUD                       |
| app/auth_routes.py                  | Rutas de login, registro y logout                |
| app/templates/layout.html           | Plantilla base con la barra de navegacion        |
| app/templates/index.html            | Pagina de bienvenida                             |
| app/templates/dashboard.html        | Panel del usuario despues de hacer login         |
| app/templates/item_form.html        | Formulario para crear o editar un item           |
| app/templates/items.html            | Tabla con todos los items                        |
| app/templates/usuarios.html         | Lista de usuarios, solo visible para Admin       |
| app/templates/cambiar_password.html | Formulario para cambiar la contrasena            |
| static/css/styles.css               | Estilos adicionales                              |
| database_schema/05_inventario.sql   | Esquema de la base de datos                      |
| test_routes.py                      | Rutas para pruebas del sistema                   |
| pruebas/                            | Scripts de prueba (REST Client)                  |
| .gitignore                          | Archivos excluidos del control de versiones      |

## Integrantes

| Nombre                            | GitHub                              |
|-----------------------------------|-------------------------------------|
| Janiel Valentin Nieves (Y00661894)| https://github.com/ALLTRIU   ------ |
| Jadriel (R000XXXXXX)              | https://github.com/USUARIO_COMPANERO|
