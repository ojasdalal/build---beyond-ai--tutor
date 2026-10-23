
# 🚀 MindGraph AI: Adaptive AI Tutoring & Knowledge Mastery Agent

> **Built for the "Build Beyond AI" Competition**  
> An autonomous, agentic learning system that evaluates user understanding in real time, generates remedial micro-lessons, tracks cognitive retention, and constructs personalized mastery pathways.

---

## 📌 Problem Statement

Traditional quiz apps rely on static, generic question banks. They test knowledge, but fail to *teach*. When a learner answers incorrectly, passive platforms merely provide answer keys without diagnosing **why** the mistake occurred—leaving critical conceptual gaps unaddressed.

## 💡 The Solution

**MindGraph AI** moves beyond basic chatbots and static quizzes. It acts as an **Autonomous AI Learning Agent** that:
1. **Diagnoses Misconceptions:** Evaluates *why* a user got a question wrong (e.g., conceptual gap vs. calculation error).
2. **Generates Targeted Micro-Lessons:** Dynamically creates remedial flashcards and targeted follow-up questions focused on weak areas.
3. **Precision Media Retrieval:** Recommends specific YouTube resources mapped precisely to topic gaps using semantic transcript analysis.
4. **Adaptive Spaced Repetition:** Schedules review sessions using spaced-repetition algorithms to ensure long-term retention.

---

## 🛠️ Tech Stack & Google Technologies Used

| Layer | Technology | Role in System |
| :--- | :--- | :--- |
| **AI Layer** | **Google Gemini 1.5 Pro / Flash** | Natural language reasoning, diagnostic evaluation, JSON schema generation |
| **Database** | **Firebase Firestore** | Real-time user progress state, card scheduling, user profiles |
| **Auth** | **Firebase Auth** | Secure user authentication and session management |
| **Analytics** | **Google BigQuery** | Learning velocity tracking and performance reporting |
| **Frontend** | React / Next.js / Tailwind CSS | Interactive user interface and adaptive quiz loop |
| **Backend** | Python (FastAPI) / Node.js | Agentic loop orchestration and API integration |

---

## 🏗️ System Architecture & Agentic Workflow

```text
[ User Interface ]
       │
       ▼
[ Adaptive Quiz Agent ] ──► [ Gemini API ] ──► Evaluates Answer & Misconception
       │
       ├─► Correct? ──► Increment Mastery Rating ──► Next Dynamic Topic
       │
       └─► Incorrect? ──► [ Remedial Agent ] ──► Generates Micro-Lesson + Flashcard
                                 │
                                 ▼
                      [ Semantic Search ] ──► Fetches Precise YouTube Micro-Lesson
