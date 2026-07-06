# 🚀 TechNova CI/CD Pipeline

## 📌 Project Overview

This project demonstrates a complete CI/CD pipeline using Jenkins, GitHub Webhooks, Docker, and Flask.

Whenever code is pushed to GitHub:

- GitHub automatically sends a webhook
- Jenkins triggers the pipeline
- Dependencies are installed
- Pytest executes automated tests
- Docker image is built
- Old container is removed
- New container is deployed automatically

---

## 🛠 Technologies Used

- Python
- Flask
- Git
- GitHub
- GitHub Webhooks
- Jenkins
- Docker
- Pytest
- Ubuntu (WSL)

---

## ⚙️ CI/CD Workflow

Developer
↓
Git Push
↓
GitHub
↓
Webhook
↓
Jenkins
↓
Checkout Code
↓
Install Dependencies
↓
Run Tests
↓
Build Docker Image
↓
Deploy Docker Container

---

## ▶️ Run Locally

```bash
pip install -r requirements.txt
python app.py
```

Application runs on:

```
http://localhost:5000
```

---

## ✅ Features

- Automated CI/CD
- Automatic Jenkins Build
- Automated Testing
- Docker Deployment
- GitHub Integration

---

## 👩‍💻 Author

Bhoomi Verma
