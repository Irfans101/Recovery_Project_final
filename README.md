# Recovery Road

Recovery Road is an AI-powered MERN-based recovery support platform designed to help patients recovering from substance-use addiction through emotional monitoring, relapse-risk analysis, supervisor support, and intelligent conversational assistance.

The platform connects:

* Patients
* Supervisors
* Administrators
* NGO partners

through a centralized web-based healthcare support system.

Recovery Road combines:

* Machine Learning
* NLP-based emotional analysis
* Conversational AI
* Facial emotion recognition
* Real-time supervisor escalation
* Behavioral tracking

within a scalable microservice architecture.

---

# Project Objective

The main objective of Recovery Road is to provide continuous recovery assistance and emotional support for patients outside traditional rehabilitation environments.

The system helps:

* monitor emotional condition,
* detect relapse indicators,
* provide recovery-focused interaction,
* and notify supervisors during high-risk situations.

The platform is designed as a supportive healthcare-adjacent monitoring system and does not replace medical professionals or therapists.

---

# Core Features

## Patient Features

* AI-powered recovery support chatbot
* Mood logging and emotional tracking
* Relapse and craving tracking
* Daily goals and milestone management
* Educational recovery content
* Wellness activities and engagement modules
* Appointment scheduling
* Notifications and messaging
* Webcam-based AI mood scanning
* Real-time communication and video calls

---

## Supervisor Features

* Patient monitoring dashboard
* Real-time high-risk alerts
* Chat monitoring and escalation visibility
* AI-assisted emotional insights
* Goal and recovery progress management
* Activity and relapse visibility
* Communication and support tools

---

## Administrator & NGO Features

* User and role management
* Organization-scoped monitoring
* Dashboard analytics
* Platform management controls

---

# AI & Machine Learning Architecture

Recovery Road implements a multi-modal AI architecture combining:

| AI Component         | Purpose                           |
| -------------------- | --------------------------------- |
| NLP Text Analysis    | Emotional and risk classification |
| Behavioral ML        | Relapse-risk prediction           |
| Computer Vision AI   | Facial emotion recognition        |
| Conversational AI    | Supportive chatbot responses      |
| Real-Time Escalation | Supervisor alert system           |

---

# AI/ML Components

## 1. NLP Risk & Emotion Analysis

The platform analyzes patient messages using Machine Learning and NLP techniques.

### Features:

* Risk classification (HIGH / MED / LOW)
* Emotion detection
* Emotional intensity estimation
* Crisis keyword analysis

### ML Pipeline:

* Text preprocessing
* TF-IDF vectorization
* RandomForest classification
* SVM emotion classification

### Supported Emotions:

* Anxiety
* Sadness
* Anger
* Hope
* Neutral

---

## 2. Behavioral Relapse Prediction

The system predicts relapse risk using structured behavioral data.

### Inputs:

* Mood logs
* Cravings
* Trigger exposure
* Activities
* Recovery consistency

### ML Models:

* GradientBoostingClassifier
* StandardScaler preprocessing

---

## 3. Facial Emotion Recognition

Recovery Road includes webcam-based emotional analysis using DeepFace.

### Flow:

Frontend webcam capture
→ Express backend upload
→ Python FastAPI service
→ DeepFace analysis
→ Emotion prediction response

### Purpose:

* Detect emotional distress
* Support mood monitoring
* Enhance AI-assisted supervision

---

## 4. Conversational AI Chatbot

The platform uses Groq API with:

llama-3.3-70b-versatile

to generate empathetic and recovery-focused responses.

### Important Safety Architecture

The chatbot does NOT directly control crisis handling.

Instead:

Patient Message
→ ML Risk Analysis
→ Safety Rules
→ Supervisor Escalation
→ Then Conversational AI

### HIGH-Risk Messages:

* bypass chatbot AI,
* trigger supervisor alerts,
* use crisis-safe templates.

### LOW/MED Messages:

* use conversational AI responses.

This creates a safety-aware healthcare AI architecture.

---

# Real-Time Supervisor Escalation

The system automatically creates alerts when:

* overdose intent,
* self-harm indicators,
* severe emotional distress,
* or relapse planning

are detected.

### Technologies Used:

* Socket.IO
* Real-time event broadcasting
* MongoDB alert persistence

---

# Tech Stack

| Layer             | Technologies                               |
| ----------------- | ------------------------------------------ |
| Frontend          | React.js, Vite, Tailwind CSS, React Router |
| Backend           | Node.js, Express.js, JWT, Socket.IO        |
| Database          | MongoDB, Mongoose                          |
| AI/ML             | Python, scikit-learn, DeepFace             |
| Conversational AI | Groq API                                   |
| Visualization     | Recharts / Chart.js                        |
| Real-Time         | Socket.IO                                  |
| Video Calls       | WebRTC, simple-peer                        |

---

# System Architecture

```text
Frontend (React)
        ↓
Backend API (Node/Express)
        ↓
ML Microservices (Python)
        ↓
MongoDB Database
        ↓
Groq Conversational AI
```

The platform follows a microservice-based architecture for modularity and scalability.

---

# Repository Structure

```text
Recovery_Road/
├── frontend/                 # React frontend
├── backend/                  # Express backend
├── backend/ml_service/       # Python ML microservices
├── README.md
└── DEPLOYMENT.md
```

---

# Local Development Setup

# Prerequisites

* Node.js (LTS recommended)
* npm
* MongoDB
* Python 3
* pip

---

# Backend Setup

```bash
cd backend
npm install
npm run dev
```

---

# Frontend Setup

```bash
cd frontend
npm install
npm run dev
```

---

# Python ML Service Setup

```bash
pip install -r backend/ml_service/requirements.txt
python backend/ml_service/app.py
```

---

# Environment Variables

## Backend `.env`

```env
NODE_ENV=development
PORT=5000

MONGO_URI=your_mongodb_uri

JWT_SECRET=your_secret

FRONTEND_URL=http://localhost:5173

ML_SERVICE_URL=http://127.0.0.1:5001

CHAT_PROVIDER=GROQ
GROQ_API_KEY=your_groq_api_key
```

---

# Deployment Architecture

| Component         | Platform      |
| ----------------- | ------------- |
| Frontend          | Vercel        |
| Backend           | Render        |
| ML Service        | Render        |
| Database          | MongoDB Atlas |
| Conversational AI | Groq API      |

---

# Production Notes

* Keep API keys only on backend.
* Never expose secrets to frontend.
* Configure CORS properly.
* Use MongoDB Atlas in production.
* Deploy ML services separately from Node backend.

---

# Security

Recovery Road implements:

* JWT authentication
* Role-based authorization
* Protected API routes
* Supervisor escalation safeguards
* AI safety filtering
* Crisis-aware chatbot logic

---

# Future Improvements

Planned future enhancements include:

* Transformer-based NLP models
* BERT fine-tuning
* Voice emotion analysis
* Mobile application
* Multi-frame facial emotion detection
* Personalized AI recommendations
* Cloud GPU inference

---

# Final Summary

Recovery Road is a multi-modal AI-powered recovery support platform that combines:

* NLP,
* machine learning,
* computer vision,
* conversational AI,
* and real-time supervisor escalation

through a MERN microservice architecture to support addiction recovery in a safer and more scalable way.
