# Enterprise RAG Q&A

Python FastAPI service for retrieval-augmented question answering over internal documents.

Upload handbook-style text, index passages with classical retrieval features, and answer questions with grounded LLM responses. Built for demos of enterprise knowledge search without a heavyweight vector platform.

## Stack

- **Backend:** Python 3.11+, FastAPI, Uvicorn
- **AI / ML:** OpenAI (`gpt-4o-mini`), scikit-learn retrieval helpers
- **Frontend (optional demo UI):** React + Vite

## Features

- Document ingest endpoint for sample or custom text
- Question answering with cited context
- Local sample employee handbook for a quick walkthrough
- Environment-based API key configuration

## Quick start

```bash
cd backend
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
cp .env.example .env   # set OPENAI_API_KEY
uvicorn main:app --reload --port 8007
```

API docs: http://localhost:8007/docs

```bash
cd frontend
npm install
npm run dev
```

## Configuration

Copy `backend/.env.example` to `backend/.env` and set:

```
OPENAI_API_KEY=your-key
PORT=8007
```

Do not commit real `.env` files.

## Author

Pooja Sharma — [Pooja101117](https://github.com/Pooja101117)
