# Full Stack Docker Template

A Dockerized Full Stack setup with Django REST Framework (DRF) for the backend and a Vite-based frontend.

---

🛠️ Version Information
- Docker: 27.4.0
- Python: 3.13.1
- Node.js: 20.17.0
- Django: 4.0 or higher
- Vite: 6.0.11

## 🚀 Getting Started

### Prerequisites
- Install [Docker Desktop](https://www.docker.com/products/docker-desktop).
- Python: Version 3.13.1 or higher (required for the Django backend)
- Node.js: Version 20.17.0 or higher (required for the Vite frontend)
---

## 🔧 Setup

1. Clone the repository:
   git clone https://github.com/ChimentiMatt/fullstack-docker-template.git
   cd fullstack-docker-template

2. Create a `.env` file based on `.env.example`:
   SECRET_KEY=your-secret-key
   DB_NAME=postgres
   DB_USER=postgres
   DB_PASSWORD=postgres
   DB_HOST=db
   DB_PORT=5432

---

## ▶️ Running the Project

1. **Start Docker Desktop** and ensure the Docker Engine is running.

2. Start the Docker containers:
   docker-compose up -d

3. Access the app:
   - **Frontend**: http://localhost:3000/
   - **Backend API**: http://localhost:8000/
   - **Admin Panel**: http://localhost:8000/admin/

---

## 🔧 Common Commands

- **Apply Migrations**:
   docker-compose exec backend python manage.py migrate

- **Create a Superuser**:
   docker-compose exec backend python manage.py createsuperuser

- **View Backend Logs**:
   docker-compose logs backend

- **View Frontend Logs**:
   docker-compose logs frontend

- **Stop Containers**:
   docker-compose down

---

## 🛠️ Development Notes

- Ensure `.env` is **not tracked** in version control. Use `.gitignore` to exclude it.
- Use `docker-compose.override.yml` for local development configurations if needed.
- The frontend is built using **Vite**, and the backend is powered by **Django REST Framework**.

---

## 📂 Project Structure
```
fullstack-docker-template/
├── backend/        # Django backend (formerly movieproject)
│   ├── backend/    # Django project files
│   ├── manage.py   # Django CLI
│   ├── requirements.txt
│   ├── Dockerfile  # Backend Docker setup
│   └── ...
├── frontend/       # Frontend (Vite + React or Vue)
│   ├── src/
│   ├── public/
│   ├── package.json
│   ├── Dockerfile  # Frontend Docker setup
│   └── ...
├── docker-compose.yml  # Docker configuration
├── .env.example   # Environment variables template
└── README.md      # Project documentation
```
---
