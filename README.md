# privyscribeAi

PrivyscribeAi is a local-first, privacy-focused audio transcription web app built with React, FastAPI, Celery, Redis, and self-hosted faster-whisper.

## Repo layout

- `/frontend` – React + TypeScript web UI
- `/backend`  – FastAPI API + Celery worker (transcription jobs)
- `/infra`    – Docker Compose for local-first runtime
- `/docs`     – Architecture notes + decisions

---

## Local run (dev)

### Backend API (FastAPI)
From `/backend`:

```bash
# example (once backend is implemented)
python -m venv .venv
# activate venv, then:
pip install -r requirements.txt
uvicorn app.main:app --host 0.0.0.0 --port 8000 --reload
