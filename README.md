# 🚀 CodeMentor AI

> **An AI-powered Single-Agent Programming Mentor built with FastAPI and JavaScript**

CodeMentor AI is an intelligent coding assistant designed to help students and developers understand, write, debug, and optimize code. It follows a **single-agent architecture**, where one AI agent dynamically adapts its behavior based on the selected programming task.

---

## ✨ Features

- 📖 **Code Explainer**
  - Explains code in simple, beginner-friendly language.
  - Breaks down logic step-by-step.

- 🐞 **Error Finder**
  - Detects syntax and logical errors.
  - Suggests possible fixes and improvements.

- 💻 **Code Generator**
  - Generates code from natural language prompts.
  - Supports multiple programming languages.

- ⚡ **Code Optimizer**
  - Improves readability and performance.
  - Suggests best coding practices.

---

## 🏗️ Project Architecture

```text
                User
                  │
                  ▼
        Frontend (HTML/CSS/JS)
                  │
                  ▼
        FastAPI Backend (/mentor)
                  │
                  ▼
         CodeMentor Agent
                  │
                  ▼
         Prompt Selection Layer
                  │
                  ▼
        LLM Provider (OpenAI Compatible)
                  │
                  ▼
            AI Generated Response
```

The application uses a **single intelligent agent** that changes its behavior based on the selected mode instead of creating multiple specialized agents.

---

## 📂 Project Structure

```text
CodeMentor_AI/
│
├── backend/
│   ├── app.py
│   ├── mentor.py
│   ├── llm.py
│   ├── prompts.py
│   ├── tools.py
│   ├── requirements.txt
│   └── test_features.py
│
├── frontend/
│   ├── index.html
│   ├── style.css
│   └── script.js
│
├── .env.example
├── README.md
└── .gitignore
```

---

## 🛠️ Tech Stack

### Frontend
- HTML5
- CSS3
- JavaScript
- Marked.js

### Backend
- Python
- FastAPI
- Pydantic
- Requests
- Python-dotenv

### AI
- OpenAI Compatible API
- Groq / OpenAI (configurable)

---

## 🔄 Request Flow

```text
User
   │
   ▼
Frontend
   │
POST /mentor
   │
   ▼
FastAPI
   │
   ▼
CodeMentor Agent
   │
   ▼
Prompt Selection
   │
   ▼
LLM API
   │
   ▼
AI Response
   │
   ▼
Frontend
```

---

## ⚙️ Installation

### 1 Clone Repository

```bash
git clone https://github.com/Shrutiii01/CodeMentor_AI.git

cd CodeMentor_AI
```

---

### 2 Create Virtual Environment

Windows

```bash
python -m venv venv
venv\Scripts\activate
```

Linux / macOS

```bash
python3 -m venv venv

source venv/bin/activate
```

---

### 3 Install Dependencies

```bash
pip install -r backend/requirements.txt
```

---

### 4 Configure Environment Variables

Create a `.env` file.

Example:

```env
OPENAI_API_PROVIDER=groq

GROQ_API_KEY=YOUR_API_KEY

GROQ_API_BASE=https://api.groq.com/openai/v1

GROQ_MODEL=llama-3.3-70b-versatile
```

---

### 5 Run the Project

```bash
uvicorn backend.app:app --reload
```

Visit

```
http://127.0.0.1:8000
```

---

## 📌 API Endpoint

### POST `/mentor`

Request

```json
{
  "mode": "explain",
  "language": "python",
  "input_text": "print('Hello World')"
}
```

Response

```json
{
  "result": "The code prints Hello World to the console."
}
```

---

## 🎯 Supported Modes

| Mode | Description |
|------|-------------|
| Explain | Explains source code |
| Error Finder | Detects bugs and logic issues |
| Generate | Generates code from prompts |
| Optimize | Improves code quality |

---

## 📈 Future Improvements

- Multi-Agent Architecture
- Chat History
- Authentication
- Code Execution Sandbox
- File Upload Support
- GitHub Repository Analysis
- AI Conversation Memory
- Unit Test Generation

---

## 🎓 Educational Value

This project demonstrates:

- AI Integration with FastAPI
- Prompt Engineering
- REST API Development
- Frontend–Backend Communication
- Single-Agent AI Architecture
- Clean Software Design Principles

---

## 👩‍💻 Author

**Shruti Narsulwar**

- Computer Science Engineering Student
- Full Stack & AI Enthusiast
- Passionate about AI-powered Developer Tools

GitHub: https://github.com/Shrutiii01

---

## ⭐ If you found this project useful

Give the repository a ⭐ and feel free to contribute or share feedback!
