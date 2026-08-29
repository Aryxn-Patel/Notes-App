# Notes App — Fullstack CRUD Application

A fullstack Notes CRUD (Create, Read, Update, Delete) web application featuring a RESTful API built with **FastAPI (Python)** and a reactive single-page frontend built with **React**, deployed across **Render** and **Vercel**.

---

## 🌐 Live Deployments

* **Frontend (Vercel):** [https://notes-qkxbq0inu-aryan-a1a6.vercel.app](https://notes-qkxbq0inu-aryan-a1a6.vercel.app)
* **Backend API (Render):** [https://notes-backend-6tmv.onrender.com](https://notes-backend-6tmv.onrender.com)
* **Interactive API Docs (Swagger UI):** [https://notes-backend-6tmv.onrender.com/docs](https://notes-backend-6tmv.onrender.com/docs)

---

## 🛠 Tech Stack

* **Backend:** Python 3, FastAPI, Uvicorn, Pydantic
* **Frontend:** React 18, ES Modules, HTML5/CSS3
* **Hosting & DevOps:** Render (Web Service), Vercel (Edge Static Hosting), Git/GitHub

---

## 📌 REST API Endpoints

| Method | Endpoint | Description | Status Code |
| :--- | :--- | :--- | :--- |
| `GET` | `/notes` | Retrieve all notes | `200 OK` |
| `GET` | `/notes/{id}` | Retrieve a specific note by ID | `200 OK` / `404 Not Found` |
| `POST` | `/notes` | Create a new note | `201 Created` / `400 Bad Request` |
| `PUT` | `/notes/{id}` | Update an existing note | `200 OK` / `400 Bad Request` / `404 Not Found` |
| `DELETE` | `/notes/{id}` | Delete a note by ID | `204 No Content` / `404 Not Found` |

---

## 🚀 Local Development Setup

### 1. Prerequisites
* Python 3.10+ installed

### 2. Backend Setup
Clone the repository and install dependencies:
```bash
git clone [https://github.com/Aryxn-Patel/Notes-App.git](https://github.com/Aryxn-Patel/Notes-App.git)
cd Notes-App
pip install -r requirements.txt
