🛡️ AI-Powered Autonomous IDPS (Intrusion Detection & Prevention System)

An enterprise-grade, cloud-native security platform that detects and responds to cyber threats in real time using a hybrid approach of rule-based detection and AI-driven anomaly detection.

---

## 🚀 Overview

This project implements a full-stack Intrusion Detection and Prevention System (IDPS)capable of:

* Real-time log monitoring
* Rule-based threat detection
* Machine learning–based anomaly detection
* Automated response (IP blocking simulation)
* REST API for monitoring & control
* SIEM integration (ELK Stack)
* Persistent storage for audit & forensics
* Containerized deployment (Docker)

---

## 🧠 Key Features

### 🔍 Detection Engine

* Rule-Based Detection (e.g., failed login attempts)
* AI-Based Detection  using Isolation Forest
* Hybrid detection pipeline for higher accuracy

### ⚡ Real-Time Processing

* Asynchronous log processing (multi-threaded)
* High-throughput architecture with buffered ingestion

### 📊 Observability & Monitoring

* Structured **JSON logging**
* Real-time **metrics tracking**
* Health check system

### 🔐 Security & Stability

* Input sanitization
* Error handling & fault tolerance
* API authentication (X-API-KEY)
* Rate limiting

### 📡 Integrations

* **FastAPI REST API**
* **Webhook alerts**
* **ELK Stack (Elasticsearch + Kibana)**
* **SQLite database (SQLAlchemy ORM)**

### 🐳 Deployment

* Dockerized for cloud-native environments
* CI/CD ready (GitHub Actions)

---

## 🏗️ Architecture

```
            ┌───────────────┐
            │  Log Source   │
            └──────┬────────┘
                   │
                   ▼
          ┌──────────────────┐
          │ Log Collector    │
          └──────┬───────────┘
                 │
                 ▼
        ┌────────────────────┐
        │ Detection Engine   │
        │ (Rule + AI Model)  │
        └──────┬─────────────┘
               │
     ┌─────────┼───────────┐
     ▼         ▼           ▼
 Alerts   Database     ELK Stack
 (Console) (SQLite)   (SIEM)
     │
     ▼
 Webhooks / API
```

---

## 🧩 Tech Stack

| Category         | Technology                       |
| ---------------- | -------------------------------- |
| Language         | Python 3.12                      |
| ML Model         | scikit-learn (Isolation Forest)  |
| API Framework    | FastAPI                          |
| Database         | SQLite + SQLAlchemy              |
| Logging          | Python Logging (JSON structured) |
| Containerization | Docker                           |
| CI/CD            | GitHub Actions                   |
| SIEM             | Elasticsearch + Kibana           |

---

## ⚙️ Installation & Setup

### 1️⃣ Clone Repository

```bash
git clone https://github.com/your-username/AI-IDPS-System.git
cd AI-IDPS-System
```

---

### 2️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

---

### 3️⃣ Generate Sample Data

```bash
python generate_data.py
```

---

### 4️⃣ Train AI Model

```bash
python train_model.py
```

---

### 5️⃣ Run System

```bash
python src/main.py
```

---

### 6️⃣ Manual Testing

Open another terminal:

```bash
python manual_input.py
```

Example attack input:

```
Failed login attempt from 192.168.1.10
```

---

## 📡 API Endpoints (FastAPI)

| Endpoint   | Description     |
| ---------- | --------------- |
| `/status`  | System health   |
| `/metrics` | Real-time stats |
| `/alerts`  | Recent threats  |

---

## 📊 ELK Integration

* Elasticsearch index: `idps-alerts`
* Kibana dashboard:

  * Threat timeline
  * Severity distribution
  * Alert frequency

---

## 🧪 Testing

```bash
python tests/inject_logs.py
python tests/performance_test.py
python tests/validation_report.py
```

---

## 🐳 Docker Deployment

```bash
docker build -t ai-idps .
docker run -p 8000:8000 ai-idps
```

---

## 📁 Project Structure

```
.
├── src/
│   ├── main.py
│   ├── detector/
│   ├── responder/
│   └── api/
├── models/
├── data/
├── logs/
├── tests/
├── config.json
├── Dockerfile
├── requirements.txt
└── README.md
```

---

## 🎯 Use Cases

* SOC (Security Operations Center) monitoring
* Cloud infrastructure security
* Intrusion detection for enterprise networks
* Real-time anomaly detection systems

---

## 📌 Future Enhancements

* Frontend dashboard (React)
* Advanced ML models (Deep Learning)
* Real firewall integration
* Cloud deployment (AWS/GCP/Azure)

---

## 👨‍💻 Author

**Rohit Kumar**
GitHub: https://github.com/Rohit10606

---

## ⭐ If you like this project

Give it a ⭐ on GitHub and share it!

---
