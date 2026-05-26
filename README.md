# Todo_App_Intern
# Todo App

A fullstack Todo application built with Next.js (frontend) and FastAPI (backend), using SQLite as the database.

## Tech Stack

- **Frontend** — Next.js 14, TypeScript, Tailwind CSS, Axios
- **Backend** — FastAPI, SQLAlchemy, Pydantic, SQLite

## Project Structure

```
Intern_Todo app/
├── Backend/
│   ├── app/
│   │   ├── main.py        # API routes
│   │   ├── models.py      # Database models
│   │   ├── schemas.py     # Pydantic schemas
│   │   └── database.py    # Database connection
│   └── todo.db            # SQLite database (auto-generated)
└── Frontend/
    ├── app/
    │   ├── page.tsx       # Main Todo UI
    │   ├── layout.tsx     # Root layout
    │   └── globals.css    # Global styles
    └── services/
        └── api.ts         # Axios instance
```

## Features

- Add a new todo
- Mark todo as completed (checkbox with strikethrough)
- Delete a todo
- Data persisted in SQLite database

## Getting Started

### Backend

```bash
cd Backend
python -m venv venv
venv\Scripts\activate
pip install fastapi uvicorn sqlalchemy pydantic
uvicorn app.main:app --reload
```

API runs at: `http://localhost:8000`  
API docs at: `http://localhost:8000/docs`

### Frontend

```bash
cd Frontend
npm install
npm run dev
```

App runs at: `http://localhost:3000`

## API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/` | Health check |
| GET | `/todos` | Get all todos |
| POST | `/todos` | Create a todo |
| PUT | `/todos/{id}` | Toggle completed |
| DELETE | `/todos/{id}` | Delete a todo |
