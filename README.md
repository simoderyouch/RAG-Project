# Stage-HCP Project

This project is a full-stack application for document analysis and retrieval, featuring:
- **Backend:** FastAPI, LangChain, MinIO, Qdrant, HuggingFace, OpenAI/DeepSeek, and more.
- **Frontend:** React (Create React App), with support for PDF, CSV, DOCX, and PPTX viewing and analysis.

---

## Table of Contents

- [Features](#features)
- [Project Structure](#project-structure)
- [Backend Setup](#backend-setup)
- [Frontend Setup](#frontend-setup)
- [Environment Variables](#environment-variables)
- [Usage](#usage)
- [Troubleshooting](#troubleshooting)
- [License](#license)

---

## Features

- Upload and analyze documents (PDF, DOCX, PPTX, CSV, TXT, XLS, XLSX)
- Store and retrieve documents using MinIO (S3-compatible object storage)
- Vector search and retrieval using Qdrant
- Embedding and LLM support via HuggingFace, OpenAI, DeepSeek, and Groq
- Custom prompt templates and summarization
- Modern React frontend for document viewing and interaction

---

## Project Structure

## Backend Setup

### 1. Prerequisites

- Python 3.10+
- [MinIO](https://min.io/) running locally (default: `localhost:9000`)
- [Qdrant](https://qdrant.tech/) running locally (default: `localhost:6333`)
- (Optional) PostgreSQL if using persistent DB DATA BASE NAE  IS hcp

### 2. Install Dependencies

Open a terminal in the `backend` directory and run:

```bash
pip install -r requirements
```


## Create a .env file in backend/app/ with the following (example):



OPENAI_API_KEY=your_openai_or_deepseek_api_key

FRONTEND_URL=http://localhost:3000
BACKEND_URL=http://127.0.0.1:8080

ADMIN_EMAIL=admin@example.com
ADMIN_PASSWORD=password

## Run the Backend
```bash
uvicorn app.main:app --reload
```

## Frontend Setup
### 1. Prerequisites
- Node.js (v16+ recommended)
- npm or yarn
### 2. Install Dependencies
Open a terminal in the frontend directory and run:

```bash
npm install
```

### 3. Environment Variables
Create a .env file in frontend/ with the following (example):
REACT_APP_BACKEND_URL=http://localhost:3000
REACT_APP_BACKEND_URL=URL_ADDRESS27.0.0.1:8080


### 4. Run the Frontend
```bash
npm start
```

The app will be available at http://localhost:3000

## Usage
1. Start MinIO and Qdrant services.
2. Start the backend server.
3. Start the frontend development server.
4. Access the frontend in your browser and upload/analyze documents.