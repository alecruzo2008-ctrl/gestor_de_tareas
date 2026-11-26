# Gestor de tareas

## Descripción

Aplicación web que permite registrar y consultar tareas utilizando Python, FastAPI, MySQL y React.

## Autor

Alejandro Cruz Orjuela

Aprendiz de Análisis y Desarrollo de Software — SENA.

## Tecnologías

- Python
- FastAPI
- MySQL
- PyMySQL
- React
- Vite
- Git y GitHub

## Configuración de MySQL

Ejecutar el archivo backend/schema.sql en MySQL Workbench.

Crear un usuario llamado gestor_app para el host 127.0.0.1, asignándole una contraseña propia y permisos SELECT e INSERT sobre gestor_tareas.tareas.

Crear el archivo backend/.env con las variables DB_HOST, DB_PORT, DB_NAME, DB_USER y DB_PASSWORD.

## Ejecutar el backend

Desde PowerShell:

```powershell
cd backend
python -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
python -m uvicorn app.main:app --reload --port 8000
```

API: http://127.0.0.1:8000/api/tareas

Documentación: http://127.0.0.1:8000/docs

## Ejecutar el frontend

Desde una segunda terminal ubicada en la raíz:

```powershell
cd frontend
npm install
npm run dev
```

Abrir la dirección indicada por Vite.

## Funcionalidades

- Consultar tareas.
- Registrar nuevas tareas.
- Validar títulos vacíos.
- Almacenar información en MySQL.
- Mostrar mensajes de confirmación y error.
- Contar las tareas registradas.

## Persistencia

Los registros se almacenan en MySQL, lo que permite conservar las tareas después de reiniciar FastAPI.

## Repositorio

https://github.com/alecruzo2008-ctrl/gestor_de_tareas