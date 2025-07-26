# 🤖 Project Report: BoB Bot – Your AI-Powered Learning Assistant

## 📌 Project Title
**BoB Bot – AI Telegram Bot for Summarizing, Quizzing, and Finding Learning Resources**

---

## 📚 Objective

BoB Bot is a Telegram-based educational assistant designed to:
- 📑 Summarize lectures, PDFs, or custom topics
- ❓ Generate MCQs for revision and testing
- 🔎 Discover online resources (videos, notes, papers)

Built to support active learning with the help of local LLM inference (OpenHermes) and responsive user interaction.

---

## 🛠️ Tools & Technologies Used

| Tool / Tech              | Purpose                                |
|--------------------------|----------------------------------------|
| **Python**               | Core development language              |
| **TeleBot**              | Telegram bot framework                 |
| **OpenHermes via Ollama**| Local LLM for summarization & MCQs     |
| **LangChain**            | Prompt management, chat memory         |
| **PyMuPDF (fitz)**       | PDF text extraction                    |
| **Regular Expressions**  | Parsing answers & cleaning GPT output  |
| **YouTube API** (or scraping) | Finding relevant video content |
| **Google Search / SerpAPI** | Web-based learning material search  |

---

## ⚙️ Key Features

### 📄 1. Topic or PDF Input
- User can either **enter a topic** or **upload a PDF**.
- PDF contents are extracted and cleaned before processing.

### 🧠 2. Summarization
- The **OpenHermes** model generates a structured, clean summary of the content.
- Summaries are tailored to be short, informative, and beginner-friendly.

### ❓ 3. MCQ Generation and Quiz Mode
- BoB uses OpenHermes to generate **4-option MCQs** from any topic or document.
- Telegram inline buttons allow **interactive quiz mode** with:
  - Per-question feedback
  - Final evaluation/score after all answers
- Answers are validated with regex to ensure correctness extraction.

### 🌍 4. External Resource Discovery
- BoB finds **top relevant resources** for the user’s topic:
  - 📺 YouTube tutorials
  - 📖 Blog posts or academic notes
  - 📄 Research articles or books
- Each resource includes a title, short description, and link.

