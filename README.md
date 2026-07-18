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

<h1 style="color:#e74c3c; font-size: 36px;">
  <a href="https://github.com/Alex9989286/DataMiningAssignment1.git" style="color:#e74c3c; text-decoration: none;">
    🫀 Cardiovascular Disease Risk Prediction System
  </a>
</h1>

End-to-end agentic AI system for CVD risk prediction — Data Mining · FastAPI · n8n · Gemini AI

---

| Data Pipeline | ML Engine | Deployment & Automation |
|---------------|-----------|-------------------------|
| 280,985 patient records | Decision Tree classifier | FastAPI RESTful API on Render |
| Multi-source healthcare data | 87.94% accuracy · 82.56% F1-Score | n8n 4-node agentic workflow |
| 36 features from 24 user inputs | 95% recall for Abnormal cases | Google Gemini AI Agent |
| Automated feature engineering | Top: HbA1c (0.57), Triglycerides (0.22) | Streamlit frontend |

---

**Python** · **Scikit-learn** · **FastAPI** · **n8n** · **Gemini AI** · **Render** · **Streamlit**

---

### Architecture highlights:

- **End-to-end ML pipeline** — Data collection → preprocessing → model training (Decision Tree) → evaluation (87.94% accuracy, 95% recall for Abnormal cases)

- **36-feature engineering** — Automated generation from 24 user inputs; includes derived features (age_normalized, blood_pressure, bmi_level, high_blood_pressure_No/Yes, family_history_No/Yes, gender_Female/Male, low_HDL_cholesterol_No/Yes, high_ldl_cholesterol_No/Yes)

- **Agentic AI workflow (n8n)** — 4-node pipeline: Webhook → FastAPI prediction → Google Gemini AI Agent → Respond to Webhook

- **API deployment** — FastAPI with 4 endpoints (/, /health, /features, /predict) on Render.com with automatic HTTPS and CORS

- **Healthcare-focused optimization** — Balanced class weights for 62% Abnormal / 38% Normal imbalance; Decision Tree for interpretability

- **Real-time prediction** — Streamlit → n8n webhook → FastAPI → Gemini AI → risk tier, recommendation, and draft message
