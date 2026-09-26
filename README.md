# ☎️ DialIQ AI
https://dialiq-taupe.vercel.app/
https://sih-nine-kappa.vercel.app/


### One Citizen → One Interface → Multiple Government Services

**DialIQ AI** is a multilingual, voice-first AI platform that enables citizens to access digital government services through a simple phone conversation.

No app.
No complex portal navigation.
No need to know which department handles the service.

**Just call. Speak. Get the information you need.**

<p align="center">

<a href="#-demo">🎥 Demo</a> • <a href="#-how-it-works">⚙️ How It Works</a> • <a href="#-architecture">🏗️ Architecture</a> • <a href="#-getting-started">🚀 Get Started</a>

</p>

---

## 🚀 What is DialIQ AI?

Government services are becoming digital, but **digital availability does not always mean digital accessibility**.

A citizen may know:

> "I need to check my pension."

But they may not know:

* Which government portal to use
* Which department provides the service
* Which documents are required
* Whether they are eligible
* Where to check their application
* How to navigate the portal

DialIQ AI removes that complexity.

The citizen simply speaks naturally.

```text
Citizen
   │
   │ "I want to check my pension application"
   ▼
☎️ DialIQ AI
   │
   ├── Understands the request
   ├── Identifies the service
   ├── Retrieves relevant information
   └── Explains the result
   │
   ▼
🔊 Voice Response
```

---

# 🎥 Demo

> **Experience the complete flow:**

```text
☎️ Call
   ↓
🎙️ Speak naturally
   ↓
🧠 AI understands intent
   ↓
🏛️ Government service lookup
   ↓
📄 Information / status
   ↓
🔊 Natural voice response
```

### Example Conversation

**Citizen**

> "Naku pension application status telusukovali."

**DialIQ AI**

> "Sure. I can help you check your pension application status. Please provide the required identification details."

**Citizen**

> "..."

**DialIQ AI**

> "Your application is currently under verification."

The goal is to make the interaction feel like **talking to an intelligent service assistant rather than navigating a government portal**.

---

# ✨ Core Features

| Feature                    | Description                                            |
| -------------------------- | ------------------------------------------------------ |
| ☎️ Voice-First             | Access services through a phone call                   |
| 🌐 Multilingual            | Designed for Indian-language interaction               |
| 🧠 AI Understanding        | Understands natural-language requests                  |
| 🔎 Service Discovery       | Identifies the appropriate government service          |
| 🏛️ API Integration        | Connects with external government systems              |
| 📋 Eligibility Guidance    | Explains eligibility requirements                      |
| 📄 Document Guidance       | Explains required documents                            |
| 📊 Status Tracking         | Retrieves application/service status where supported   |
| 🔊 Conversational Response | Converts technical results into simple language        |
| 🔐 Secure Architecture     | Designed for authentication, authorization and consent |

---

# 🧠 How It Works

```text
                    CITIZEN
                       │
                       │ Phone Call
                       ▼
              ┌─────────────────┐
              │  Cloud Telephony │
              └────────┬────────┘
                       │
                       ▼
              ┌─────────────────┐
              │ Speech-to-Text  │
              └────────┬────────┘
                       │
                       ▼
          ┌──────────────────────────┐
          │    AI ORCHESTRATION      │
          │                          │
          │ • Intent Detection       │
          │ • Service Identification│
          │ • Context Management     │
          │ • Reasoning              │
          │ • Tool Selection         │
          └────────────┬─────────────┘
                       │
             ┌─────────┴─────────┐
             │                   │
             ▼                   ▼
      ┌──────────────┐    ┌──────────────┐
      │ Government   │    │ Knowledge /  │
      │ APIs         │    │ RAG          │
      └──────┬───────┘    └──────┬───────┘
             │                   │
             └─────────┬─────────┘
                       ▼
              ┌─────────────────┐
              │ Response Engine │
              └────────┬────────┘
                       │
                       ▼
              ┌─────────────────┐
              │ Text-to-Speech  │
              └────────┬────────┘
                       │
                       ▼
                    🔊 VOICE
                    RESPONSE
```

---

# 🏗️ Architecture

DialIQ AI follows a modular architecture where the AI layer is separated from telephony, speech processing, databases, and external government integrations.

```text
┌─────────────────────────────────────────────────────┐
│                    CITIZEN LAYER                    │
│                                                     │
│              Phone / Voice Interface                │
└──────────────────────────┬──────────────────────────┘
                           │
                           ▼
┌─────────────────────────────────────────────────────┐
│                 COMMUNICATION LAYER                 │
│                                                     │
│              Cloud Telephony / Voice               │
└──────────────────────────┬──────────────────────────┘
                           │
                           ▼
┌─────────────────────────────────────────────────────┐
│                   AI LAYER                          │
│                                                     │
│  STT → Intent → Agent → Tool Selection → LLM       │
│                                                     │
└──────────────────────────┬──────────────────────────┘
                           │
                           ▼
┌─────────────────────────────────────────────────────┐
│                INTEGRATION LAYER                    │
│                                                     │
│  API Gateway / Connectors / Authentication          │
└───────────────┬──────────────────┬──────────────────┘
                │                  │
                ▼                  ▼
       ┌────────────────┐   ┌─────────────────┐
       │ Government     │   │ Knowledge Base │
       │ APIs / Systems │   │ / RAG           │
       └────────────────┘   └─────────────────┘
                │                  │
                └────────┬─────────┘
                         ▼
                ┌─────────────────┐
                │ PostgreSQL      │
                │ / Data Layer    │
                └─────────────────┘
```

---

# 🔄 Example: Pension Status

### Step 1 — Citizen speaks

```text
"I want to know my pension application status."
```

### Step 2 — Speech Recognition

```text
Voice
  ↓
Speech-to-Text
  ↓
"I want to know my pension application status."
```

### Step 3 — Intent Detection

```json
{
  "intent": "APPLICATION_STATUS",
  "service": "PENSION",
  "language": "en"
}
```

### Step 4 — Service Selection

The AI determines which service connector should handle the request.

```text
PENSION
   ↓
Pension Service Connector
   ↓
Government API
```

### Step 5 — Retrieve Information

The connector retrieves the relevant service information.

### Step 6 — Response Generation

The raw API response is converted into a simple conversational response.

```text
API:
STATUS = VERIFICATION_PENDING

        ↓

AI:

"Your pension application is currently
under verification."
```

### Step 7 — Voice Response

```text
Text
 ↓
TTS
 ↓
🔊 Citizen hears the response
```

---

# 🧩 Service Connector Architecture

One of the important design principles of DialIQ AI is **service independence**.

Instead of hard-coding every service into the AI layer:

```text
                 AI ORCHESTRATOR
                       │
                       ▼
                SERVICE ROUTER
                       │
        ┌──────────────┼──────────────┐
        ▼              ▼              ▼
     Pension         Farmer         Education
     Connector       Connector      Connector
        │              │              │
        ▼              ▼              ▼
   Government       Government     Government
      API              API            API
```

This makes it possible to add new services without rewriting the entire platform.

---

# 🛠️ Technology Stack

### Backend

* Java
* Spring Boot
* REST APIs
* PostgreSQL

### AI

* Large Language Models
* Intent Detection
* AI Orchestration
* Retrieval-Augmented Generation
* Prompt-based reasoning

### Voice

* Speech-to-Text
* Text-to-Speech
* Cloud Telephony
* Real-time voice communication

### Frontend

* React
* JavaScript
* HTML
* CSS

### Security

* JWT
* OAuth 2.0
* RBAC
* Consent Management

### Deployment

* Docker
* Cloud Infrastructure
* Environment-based configuration

---

# 📁 Project Structure

```text
dialiq-ai/
│
├── backend/
│   ├── src/
│   │   ├── controller/
│   │   ├── service/
│   │   ├── repository/
│   │   ├── model/
│   │   ├── integration/
│   │   ├── security/
│   │   └── config/
│   │
│   └── pom.xml
│
├── frontend/
│   ├── src/
│   ├── public/
│   └── package.json
│
├── ai/
│   ├── orchestration/
│   ├── prompts/
│   ├── rag/
│   └── services/
│
├── docs/
│   ├── architecture/
│   └── api/
│
├── docker/
│
├── .env.example
├── docker-compose.yml
└── README.md
```

---

# 🚀 Getting Started

## Prerequisites

```text
Java 17+
Maven
Node.js
PostgreSQL
Docker
Git
```

Optional:

```text
LLM API
Speech-to-Text API
Text-to-Speech API
Cloud Telephony
```

---

## Clone

```bash
git clone https://github.com/<your-username>/dialiq-ai.git

cd dialiq-ai
```

---

## Backend

```bash
cd backend

mvn clean install

mvn spring-boot:run
```

---

## Frontend

```bash
cd frontend

npm install

npm run dev
```

---

# 🔐 Environment Variables

Create your environment configuration from `.env.example`.

```env
DATABASE_URL=
DATABASE_USERNAME=
DATABASE_PASSWORD=

LLM_API_KEY=

STT_API_KEY=
TTS_API_KEY=

TELEPHONY_API_KEY=
TELEPHONY_NUMBER=

JWT_SECRET=
```

**Never commit API keys or production credentials to the repository.**

---

# 🔌 API Design

DialIQ AI uses REST-based services for communication between the application components.

Example:

```http
POST /api/v1/query
```

Request:

```json
{
  "language": "en",
  "message": "I want to check my pension status"
}
```

Response:

```json
{
  "intent": "APPLICATION_STATUS",
  "service": "PENSION",
  "response": "Your application is currently under verification."
}
```

---

# 🔐 Security

The system is designed with security as a first-class architectural concern.

Key areas include:

* Authentication
* Authorization
* JWT-based access
* Role-based access control
* Consent management
* Secure API communication
* Input validation
* Secret management
* Minimal data collection
* Audit logging

Sensitive citizen information should only be accessed through authorized and secured workflows.

---

# 📈 Roadmap

### Phase 1 — Prototype

* [x] Voice interaction concept
* [x] AI service identification
* [x] Conversational response
* [x] Initial architecture
* [x] Prototype demonstration

### Phase 2 — Integration

* [ ] Government API connectors
* [ ] RAG knowledge layer
* [ ] Authentication
* [ ] Consent management
* [ ] More Indian languages
* [ ] Application status integration

### Phase 3 — Production

* [ ] Scalable cloud deployment
* [ ] Monitoring
* [ ] Human-agent escalation
* [ ] SMS notifications
* [ ] Conversation history
* [ ] Additional government services

---

# 🎯 Design Philosophy

DialIQ AI is built around a simple idea:

> **The citizen should not need to understand the digital infrastructure behind a service.**

The user should only need to explain:

> **"I need this."**

DialIQ handles the complexity behind the interface.

```text
                    COMPLEXITY
                        ↓
       ┌────────────────────────────────┐
       │ Government Portals             │
       │ APIs                           │
       │ Departments                    │
       │ Eligibility Rules              │
       │ Documents                      │
       │ Application Systems            │
       └───────────────┬────────────────┘
                       │
                       ▼
                  🧠 DialIQ AI
                       │
                       ▼
                Simple Conversation
                       │
                       ▼
                    👤 Citizen
```

---

# 🌐 Vision

Digital government should be accessible to everyone—not only to people who are comfortable with apps, websites, forms, and portals.

DialIQ AI explores a **voice-first interoperability layer** that can connect citizens with multiple digital services through a single conversational interface.

### One Citizen

### One Interface

### Multiple Services

---

# 🏆 Hackathon

Developed by **Team Empower** for the **Smart India Hackathon 2026** ecosystem.

**Problem Statement:**
`SIH26129 — System Integration & Interoperability among Government Digital Platforms`

---

# 👨‍💻 Team

**Team Empower**

Building technology around:

```text
AI × Voice × Interoperability × Accessibility
```

---

# 📜 License

This project is currently developed as a prototype.

Add an appropriate open-source license before distributing the project for external use.

---

<p align="center">

### ☎️ DialIQ AI

**Making digital government services conversational.**

`AI • Voice • APIs • Accessibility`

</p>
