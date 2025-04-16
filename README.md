# Flask User API

API REST desarrollada con **Flask** y **PostgreSQL**, con operaciones CRUD para gestión de usuarios, validaciones personalizadas y autenticación con tokens JWT. Compatible con despliegue local y en contenedores Docker.

---

## 📦 Tecnologías utilizadas

- Python 3.9
- Flask
- PostgreSQL
- JWT
- Docker + Docker Compose

---

## 🚀 Endpoints principales

(Resumen aquí, puedes expandir cada uno si quieres. Ya lo hicimos antes.)

- `POST /login`: Inicio de sesión
- `POST /login/register`: Registro de usuario
- `GET /login/users`: Obtener todos los usuarios
- `POST /login/edituser`: Editar un usuario
- `POST /login/deleteuser`: Eliminar un usuario

---

## 🐳 Despliegue con Docker

### ✅ Requisitos

- [Docker](https://www.docker.com/)

### 📂 Estructura del proyecto esperada
. ├── app.py ├── Dockerfile ├── docker-compose.yml ├── requirements.txt ├── .env └── README.md


### ⚙️ Variables de entorno (`.env`)

```env
DATABASE_URL=postgresql://usuario:password@db:5432/tu_basedatos
SECRET_KEY=tu_clave_secreta

FROM python:3.9-slim

WORKDIR /app

COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

COPY . .

CMD ["flask", "run", "--host=0.0.0.0"]

▶️ Levantar el proyecto
La API estará disponible en:
👉 http://localhost:5000

✨ Extras
Validaciones robustas a nivel de API

Gestión segura de tokens JWT

Control de errores detallado

Preparado para entornos productivos
🧑‍💻 Autor
Daniel Armando Novoa Zambrano
Backend Developer con +8 años de experiencia
📍 CDMX, México
