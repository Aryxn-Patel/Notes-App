from fastapi import FastAPI, HTTPException
from fastapi.middleware.cors import CORSMiddleware
from pydantic import BaseModel

app = FastAPI(title="Notes API")

app.add_middleware(
    CORSMiddleware,
    allow_origins=["*"],
    allow_credentials=True,
    allow_methods=["*"],
    allow_headers=["*"],
)

notes_db = {}
next_id = 1

class NoteInput(BaseModel):
    title: str
    content: str = ""

@app.get("/")
def root():
    return {"message": "Notes API is running"}

@app.get("/notes")
def list_notes():
    return list(notes_db.values())

@app.get("/notes/{note_id}")
def get_note(note_id: int):
    note = notes_db.get(note_id)
    if note is None:
        raise HTTPException(status_code=404, detail="Note not found")
    return note

@app.post("/notes", status_code=201)
def create_note(payload: NoteInput):
    global next_id
    if not payload.title.strip():
        raise HTTPException(status_code=400, detail="Title is required")
    note = {"id": next_id, "title": payload.title, "content": payload.content}
    notes_db[next_id] = note
    next_id += 1
    return note

@app.put("/notes/{note_id}")
def update_note(note_id: int, payload: NoteInput):
    note = notes_db.get(note_id)
    if note is None:
        raise HTTPException(status_code=404, detail="Note not found")
    if not payload.title.strip():
        raise HTTPException(status_code=400, detail="Title is required")
    note["title"] = payload.title
    note["content"] = payload.content
    notes_db[note_id] = note
    return note

@app.delete("/notes/{note_id}", status_code=204)
def delete_note(note_id: int):
    if note_id not in notes_db:
        raise HTTPException(status_code=404, detail="Note not found")
    del notes_db[note_id]
    return None

    