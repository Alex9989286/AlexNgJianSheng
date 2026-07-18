# 👋 Hi, I'm Alex Ng Jian Sheng

Software Engineering student · QA enthusiast · Building things that work


---


## 🏅 Featured Project

# 🎧 SoundGuard: AI-Powered Sound Detection System

Real-time environmental sound classification for hearing-impaired users — from model training to mobile deployment (CNN · Flutter · FastAPI · ONNX)

---

### Data Pipeline
- ESC-50 + UrbanSound8K datasets
- 7,194 audio samples · 7 sound categories
- MFCC (40) + delta + delta-delta
- 128-band Mel-spectrogram
- 248-dim feature tensor · Data augmentation

### ML Engine
- CNN architecture (3 conv layers)
- 93% classification accuracy
- ONNX optimization
- Cross-platform compatibility
- 7 sound categories (siren, dog, footsteps, clapping, children, thunderstorm, street music)

### Mobile Client
- Flutter cross-platform (Android/iOS)
- Real-time audio capture
- Silence detection & queue management
- Multimodal feedback (visual + vibration)
- Direction detection (Left/Centre/Right)

---

**Python** · **TensorFlow** · **FastAPI** · **Flutter** · **ONNX** · **CNN**

---

### Architecture highlights:

- **End-to-end ML pipeline** — Data collection → feature extraction (MFCC + Mel-spectrogram) → CNN training (93% accuracy) → ONNX optimization → FastAPI deployment; optimized for real-time inference on CPU-based servers

- **Cross-platform mobile application** — Flutter with real-time audio capture, silence detection (peak amplitude), task queue management (max 5 tasks), timeout/retry mechanisms, and multimodal feedback (visual + vibration)

- **Comprehensive testing & validation** — 60+ test cases across unit, integration, system, and UAT levels with 97% pass rate; formal SUS evaluation with 10 participants achieving a score of 72.75 (above average)

- **Sound direction detection** — Stereo volume-based left/centre/right detection using device microphones with compass UI feedback and confidence-based classification display (75%+ direct label, 50-75% "Possible" prefix, <50% "Unclear")

- **ONNX model deployment** — Converted trained Keras model to ONNX format to resolve TensorFlow version compatibility issues, enabling cross-framework deployment with efficient CPU inference via ONNX Runtime

---

###  Testing & Evaluation

| Metric | Result |
|--------|--------|
| **Classification Accuracy** | 93% (lab) |
| **Test Cases** | 60+ (97% pass rate) |
| **SUS Score** | 72.75 (above average) |
| **Direction Detection** | 75% overall accuracy |
| **Participants** | 10 (UAT + SUS) |

---

### 🔗 Links

 [Demo Video](https://drive.google.com/file/d/1mhGucrVhfExfgl8w9kSFB2wlRM733QKD/view?usp=drive_link)

---

###  Tech Stack

| Category | Technologies |
|----------|--------------|
| **ML Framework** | TensorFlow, Keras, scikit-learn |
| **Model Optimization** | ONNX, ONNX Runtime |
| **Backend** | FastAPI, Python, Uvicorn |
| **Mobile** | Flutter, Dart |
| **Audio Processing** | Librosa, NumPy |
| **Testing** | Selenium, JMeter, Postman |
| **Tools** | VS Code, GitHub, Render |

---

*From model training to production deployment — SoundGuard brings AI-powered sound awareness to the hearing-impaired community.*


---

<h1 style="color:#6f42c1; font-size: 36px;">
  <a href="https://github.com/katherine101001/project-management-system.git" style="color:#6f42c1; text-decoration: none;">
    🏗️Project Management System
  </a>
</h1>

Full-stack enterprise platform — Clean Architecture · C# .NET · Containerized Microservices

---

| Clean Architecture | | | |
|--------|-------------|----------------|-----|
| **Domain** | **Application** | **Infrastructure** | **API** |
| Entities | Use Cases | EF Core | ASP.NET Core |
| Value Obj | DTOs | SQL Server | RESTful |
| Interfaces | AutoMapper | Repositories | Swagger |

| 3-Tier RBAC | | |
|-------|-----------------|--------|
| **Admin** | **Project Manager** | **Member** |
| Full access | Manage projects | View tasks |
| User management | Assign tasks | Update status |
| System config | Team management | Comments |

---

**C#** · **.NET 9** · **React 18** · **AWS EC2** · **Docker** · **SQL Server** · **Postman**

---

### Architecture highlights:

- **5-layer Clean Architecture** — Domain → Application → Infrastructure → API → Shared; inner layers have zero external dependencies

- **Role-Based Access Control (RBAC)** — 3 user tiers (Admin, Project Manager, Member) with secure permission segregation enforced at both frontend router and backend controller levels

- **Repository + Unit of Work pattern** — 6 repository implementations behind interfaces, enabling testability and future database swapping without touching business logic

- **SOLID throughout** — Dependency Injection for all services; AutoMapper for object mapping; interface-based design at every boundary

- **React + Redux Toolkit** — Centralized state management with 3 slices (user, projects, theme); role-based protected routes (ADMIN/LEADER/MEMBER) enforced at both frontend and backend

- **Real-time collaboration** — Comments with @mentions, Mailjet transactional emails, in-app notification system with read/unread tracking

- **Analytics engine** — Recharts bar/pie visualizations; task completion rate, priority distribution, overdue detection; computed on-the-fly from Redux state

---

<h2 style="color:#e74c3c; font-size: 36px;">
  <a href="https://github.com/AlexNgJianSheng/CVD-Risk-Prediction-System" style="color:#e74c3c; text-decoration: none;">
    🫀 Cardiovascular Disease Risk Prediction System
  </a>
</h2>

End-to-end agentic AI system for CVD risk prediction — Data Mining · FastAPI · n8n · Gemini AI

---

### Data Pipeline
- 280,985 patient records · 39 features
- Multi-source healthcare data (diabetes, heart disease, hypertension)
- 36 features extracted from 24 user inputs
- Automated feature engineering (age_normalized, blood_pressure, bmi_level, etc.)

### ML Engine
- Decision Tree classifier
- 87.94% accuracy · 82.56% F1-Score
- 95% recall for Abnormal cases (critical for healthcare)
- Feature importance: HbA1c_level (0.57), Triglycerides (0.22), Sleep Hours (0.10)

### Deployment & Automation
- FastAPI RESTful API deployed on Render
- n8n agentic workflow with 4-node pipeline (Webhook → Prediction → AI Agent → Response)
- Google Gemini AI Agent for risk tiering & personalized recommendations
- Streamlit frontend for user data input

---

**Python** · **Scikit-learn** · **FastAPI** · **n8n** · **Gemini AI** · **Render** · **Streamlit**

---

### Architecture highlights:

- **End-to-end ML pipeline** — Data collection → preprocessing (one-hot encoding, label encoding, feature scaling) → model training (Decision Tree with balanced class weights) → evaluation (87.94% accuracy, 95% recall for Abnormal cases)

- **36-feature engineering** — Automated generation from 24 user inputs; includes derived features (age_normalized, blood_pressure, bmi_level, high_blood_pressure_No/Yes, family_history_No/Yes, gender_Female/Male, low_HDL_cholesterol_No/Yes, high_ldl_cholesterol_No/Yes)

- **Agentic AI workflow (n8n)** — 4-node pipeline: Webhook trigger → HTTP Request (FastAPI prediction) → Google Gemini AI Agent (risk tiering + recommendations) → Respond to Webhook (merged JSON response)

- **API deployment** — FastAPI RESTful service with 4 endpoints (/ , /health, /features, /predict) deployed on Render.com with automatic HTTPS, CORS middleware, and pickle-based model serialization

- **Healthcare-focused optimization** — Balanced class weights to address 62% Abnormal / 38% Normal class imbalance; Decision Tree selected for interpretability (medical professionals need explainable decisions)

- **Real-time prediction** — Streamlit frontend → n8n webhook → FastAPI → Gemini AI → consolidated response with risk tier, health recommendation, and draft patient message

📄 [Project Report (PDF)](link-to-your-report)  
🔗 [n8n Workflow JSON](https://github.com/AlexNgJianSheng/CVD-Risk-Prediction-System/blob/main/SWE2304249_SWE402_n8n.json)  
🐙 [GitHub Repository](https://github.com/AlexNgJianSheng/CVD-Risk-Prediction-System)

---

### 📊 Model Performance

| Metric | Result |
|--------|--------|
| **Accuracy** | 87.94% |
| **F1-Score** | 82.56% |
| **Precision (Abnormal)** | 90.35% |
| **Recall (Abnormal)** | 95% |
| **Dataset Size** | 280,985 records |
| **Features** | 36 |

### 🔬 Top Features (Feature Importance)

| Feature | Importance |
|---------|------------|
| HbA1c_level | 0.568 |
| Triglycerides | 0.215 |
| Sleep Hours | 0.102 |
| Glucose | 0.019 |
| Cholesterol | 0.018 |
| Age_normalized | 0.017 |

### 🏗️ n8n Workflow Architecture

| Node | Function |
|------|----------|
| **Webhook** | Receives patient data from Streamlit (24 inputs → 36 features) |
| **HTTP Request** | Sends POST to FastAPI /predict endpoint on Render |
| **AI Agent (Gemini)** | Analyzes prediction, generates risk tier + recommendation + draft message |
| **Respond to Webhook** | Merges all data and returns JSON response to client |

---

⭐ *From data preprocessing to AI-powered recommendations — a complete agentic system for cardiovascular disease risk assessment.*

- **DevOps-ready** — Docker Compose multi-container (backend + frontend); GitHub Actions auto-deploy to AWS EC2 on push to main; Swagger auto-generated API docs

🔗 [GitHub Repository](https://github.com/katherine101001/project-management-system.git)
