# AI Tutor Agent

An intelligent, personalized learning assistant built using **Google Vertex AI Agents**, **RAG (Retrieval-Augmented Generation)**, **Firebase**, and **Cloud Run**. This project helps students learn faster by providing:

* Step-by-step explanations grounded in uploaded study materials
* Personalized quizzes and automatic grading
* Summaries, flashcards, and study plans
* A teacher dashboard for monitoring progress

---

## 🚀 Project Overview

Traditional learning can be slow and inefficient because students lack access to personalized support. Our AI Tutor Agent solves this by acting as a 24/7 intelligent tutor capable of:

* Understanding natural language questions
* Retrieving answers from textbooks/slides
* Explaining concepts at any difficulty level
* Generating quizzes and grading them automatically

---

## 🎯 Problem Statement

Students struggle with:

* Large, complex study materials
* Limited access to personal tutors
* Lack of customized learning paths
* Hard-to-generate practice questions

The AI Tutor Agent addresses all of these problems by combining advanced retrieval, reasoning, and personalized learning.

---

## 🤖 Why Agents?

Agents are the perfect solution because they:

* Combine retrieval + reasoning + tool use
* Maintain conversation context
* Provide personalized, interactive tutoring
* Allow modular tools (quiz generator, grader, summarizer)
* Enable multi-step task completion (RAG → explanation → quiz → evaluation)

---

## 🧱 Architecture

```
[Student UI] ----> [Frontend] ----> [Backend API]
                                      |
                                      v
                              [Vertex AI Agent]
                                      |
                ------------------------------------------------
                |             |                 |              |
             [RAG]     [Quiz Generator]   [Grader]      [Study Plan]
                |
                v
      [Vector DB / Semantic Search]
                |
                v
          [PDFs / Notes in GCS]
```

---

## 🛠️ Tech Stack

### **AI & Backend**

* Google Vertex AI Agents
* Gemini models (1.5 Pro / Flash)
* Vertex AI Embeddings
* Vertex Semantic Search (vector store)
* Cloud Run
* Node.js / Python (for APIs and ingestion)

### **Frontend**

* React.js
* Firebase Hosting (optional)

### **Database & Storage**

* Firebase Firestore (students, quizzes, progress)
* GCS (PDFs, slides, transcripts)

---

## 🌟 Features

### Student Features

* Ask any question from uploaded materials
* Step-by-step explanations with citations
* Personalized quizzes
* Instant grading
* Progress tracking

### Teacher/Admin Features

* Upload PDFs/notes for students
* Auto-ingestion into RAG index
* View student analytics

---

## 📥 How to Clone This Repository

```bash
git clone https://github.com/lavanyalakshman75-hue/ai-tutor-agent.git
cd ai-tutor-agent
```

---

## ⚙️ Setup Instructions

### 1️⃣ Install Dependencies

Backend:

```bash
cd backend
npm install
```

Frontend:

```bash
cd frontend
npm install
```

---

### 2️⃣ Create Environment Files

Create `.env` files in both backend and frontend:

Example for backend:

```
PROJECT_ID=your_project_id
REGION=us-central1
```

Frontend:

```
REACT_APP_API_URL=https://your-cloud-run-url
```

---

## ▶️ Running the App Locally

Backend:

```bash
cd backend
npm start
```

Frontend:

```bash
cd fronte
```
