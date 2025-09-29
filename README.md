# Enhancing Digital Defence Using Federated Learning Security Sandbox

## 📌 Overview

This project is a **security sandbox platform** that combines **Docker-based isolation** with **Federated Learning (FL)** to detect malware and anomalies in a **privacy-preserving** manner.

* Suspicious files are uploaded via the frontend and executed safely inside **Docker containers**, which capture behavioral logs like system calls, file access, and network activity.
* Each sandbox trains a **local FL model** on its captured data. Instead of sharing raw logs, only model parameters are sent to the server for aggregation, ensuring **data privacy**.
* The **Flask backend** manages sandbox execution, federated training, and results delivery.
* The **frontend (HTML, CSS, JS)** lets users upload files and view real-time results.

---

## 🚀 Features

* **Docker Sandbox Isolation**: Safely executes potentially harmful files without risking the host system.
* **Federated Learning**: Collaborative anomaly detection model training without sharing sensitive data.
* **Privacy-Preserving Security**: Only model weights are shared, not raw logs.
* **Full-Stack Integration**: Frontend UI connected with Flask backend through REST APIs.
* **Database Support**: SQLite/MySQL stores logs, results, and training metadata.

---

## 🔄 Workflow

1. User uploads a suspicious file via the UI.
2. Flask backend executes the file inside a Docker sandbox.
3. Logs (system calls, file activity, network traces) are collected.
4. Local FL model trains on these logs.
5. Only model weights are aggregated into a global model.
6. Results and anomaly detection insights are displayed on the UI.

---

## 🛠️ Tech Stack

* **Frontend**: HTML, CSS, JavaScript
* **Backend**: Python (Flask)
* **Containerization**: Docker
* **Machine Learning**: Federated Learning (Logistic Regression)
* **Database**: SQLite / MySQL

---

## 👩‍💻 My Role

I contributed to three main parts of the project:

1. **Docker Sandbox Setup**: Configured isolated containers, captured system logs, and ensured secure execution of files.
2. **Federated Learning Training**: Implemented local model training and parameter aggregation for anomaly detection.
3. **Frontend-Backend Integration**: Connected the UI with Flask APIs for file uploads, real-time results, and smooth interaction.

---

## 📈 Future Scope

* Real-time **network packet analysis** (e.g., Wireshark integration).
* Lightweight **IoT-compatible sandboxes** for edge devices.
* **Live alert system** for immediate detection and response.

---

## ▶️ How to Run

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/security-sandbox-fl.git
   cd security-sandbox-fl
   ```
2. Start Docker service.
3. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```
4. Run Flask backend:

   ```bash
   python app.py
   ```
5. Open frontend in browser and upload a file for analysis.

---

## 📂 Project Structure

```
├── app.py              # Flask backend  
├── docker/             # Docker sandbox configs  
├── federated/          # FL model training code  
├── static/             # Frontend assets (CSS, JS)  
├── templates/          # Frontend HTML pages  
├── database/           # SQLite/MySQL schema and logs  
└── README.md
```

---

Would you like me to also **add GitHub-friendly visuals** (like badges for Docker, Flask, Python, etc. and an architecture diagram in markdown) to make the README stand out more?
