# Notes App — Fullstack CRUD Application

A lightweight, full-stack Notes CRUD (Create, Read, Update, Delete) web application featuring a RESTful API built with **FastAPI (Python)** using in-memory state, and a reactive single-page frontend built with **React 18** via browser-native **JavaScript ES Modules**, deployed on **Render** and **Vercel**.

---

## 🌐 Live Deployments

* **Frontend (Vercel):** [https://notes-app-red-seven.vercel.app/](https://notes-app-red-seven.vercel.app/)
* **Backend API (Render):** [https://notes-backend-6tmv.onrender.com](https://notes-backend-6tmv.onrender.com)
* **Interactive API Docs (Swagger UI):** [https://notes-backend-6tmv.onrender.com/docs](https://notes-backend-6tmv.onrender.com/docs)

---

## 🛠 Tech Stack

* **Backend:** Python 3, FastAPI, Uvicorn, Pydantic (Data Validation)
* **Frontend:** React 18, Native JavaScript ES Modules (`<script type="module">`), HTML5, CSS3
* **Data Storage:** Fast in-memory Python data structures (ephemeral RAM storage)
* **Cloud & Hosting:** Render (Backend Web Service), Vercel (Edge Static Frontend), GitHub

---

## 📌 REST API Endpoints

| Method | Endpoint | Description | Status Code |
| :--- | :--- | :--- | :--- |
| `GET` | `/notes` | Retrieve all notes | `200 OK` |
| `GET` | `/notes/{id}` | Retrieve a single note by ID | `200 OK` / `404 Not Found` |
| `POST` | `/notes` | Create a new note | `201 Created` / `400 Bad Request` |
| `PUT` | `/notes/{id}` | Update an existing note | `200 OK` / `400 Bad Request` / `404 Not Found` |
| `DELETE` | `/notes/{id}` | Delete a note by ID | `204 No Content` / `404 Not Found` |

---

## 🚀 Local Development Setup

### 1. Prerequisites
* Python 3.10+ installed on your machine

### 2. Backend Setup
Clone the repository and install dependencies:
```bash
git clone [https://github.com/Aryxn-Patel/notes-app.git](https://github.com/Aryxn-Patel/notes-app.git)
cd notes-app
pip install -r requirements.txt
