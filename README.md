# 🎧 SoundGuard: AI-Powered Sound Detection System

Real-time environmental sound classification for hearing-impaired users — from model training to mobile deployment

---

## 🏅 Featured Project

### SoundGuard

Real-time environmental sound classification for hearing-impaired users — CNN · Flutter · FastAPI · ONNX

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

### 📊 Testing & Evaluation

| Metric | Result |
|--------|--------|
| **Classification Accuracy** | 93% (lab) |
| **Test Cases** | 60+ (97% pass rate) |
| **SUS Score** | 72.75 (above average) |
| **Direction Detection** | 75% overall accuracy |
| **Participants** | 10 (UAT + SUS) |

---

### 🔗 Links

📄 [Project Report (FYP Thesis)](link-to-your-thesis)  
📱 [Demo Video](your-demo-link-here)  
🐙 [GitHub Repository](https://github.com/AlexNgJianSheng/SoundGuard)

---

### 📚 Tech Stack

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

⭐ *From model training to production deployment — SoundGuard brings AI-powered sound awareness to the hearing-impaired community.*
