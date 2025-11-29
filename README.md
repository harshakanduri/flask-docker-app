# 🚀 Python Flask App Dockerized (GitHub Codespaces + Docker Hub)

This project is a **simple Python Flask web application** that is **containerized using Docker**,  
**built and tested in GitHub Codespaces**, and the **image is pushed to Docker Hub**.
<img width="1920" height="1080" alt="Screenshot (37)" src="https://github.com/user-attachments/assets/77f557a6-3906-4051-bdc2-64ed39abe9d9" />

You can use this project to show:
- You know **Python + Flask**
- You can write a **Dockerfile**
- You can build and run **Docker containers**
- You can use **GitHub Codespaces**
- You are able to **push Docker images to Docker Hub**
- You can **upload code to GitHub**

---

## 📁 Project Structure

```bash
flask-docker-app/
├── app.py
├─ requirements.txt
├─ Dockerfile
└── README.md
```

---

## 🧰 Tech Stack

- **Language**: Python 3.x  
- **Framework**: Flask  
- **Containerization**: Docker  
- **Dev Environment**: GitHub Codespaces  
- **Image Registry**: Docker Hub (Username: `harshakanduri`)  
- **Version Control**: Git + GitHub  

---

## 🐍 Step 1: Flask Application (`app.py`)

```python
from flask import Flask

app = Flask(__name__)

@app.route("/")
def home():
    return "Hello from Docker + Flask!"

if __name__ == "__main__":
    app.run(host="0.0.0.0", port=5000)
```

---

## 📦 Step 2: Python Dependencies (`requirements.txt`)

```text
flask
```

---

## 🧱 Step 3: Dockerfile

```dockerfile
FROM python:3.10
WORKDIR /app
COPY . .
RUN pip install -r requirements.txt
CMD ["python", "app.py"]
```

---

## 🧪 Step 4: Run the App Locally (Optional)

```bash
pip install -r requirements.txt
python app.py
```

Open in browser:

```
http://localhost:5000
```

Stop the app:  
```
Ctrl + C
```

---

## 🐳 Step 5: Build Docker Image

```bash
docker build -t flask-app .
```

---

## ▶️ Step 6: Run Docker Container

```bash
docker run -p 5000:5000 flask-app
```

Open:

```
http://localhost:5000
```

Stop container:  
```
Ctrl + C
```

---

## ☁️ Step 7: Push Image to Docker Hub

### Login:
```bash
docker login
```

### Tag Image:
```bash
docker tag flask-app harshakanduri/flask-app:latest
```

### Push Image:
```bash
docker push harshakanduri/flask-app:latest
```

### Docker Hub Image URL:
```
https://hub.docker.com/r/harshakanduri/flask-app
```

---

## 🧲 Step 8: Pull and Run Image from Docker Hub

```bash
docker pull harshakanduri/flask-app:latest
docker run -p 5000:5000 harshakanduri/flask-app:latest
```

---

## 💻 Step 9: Push Code to GitHub Repository

```bash
git init
git add .
git commit -m "Initial commit - Flask Docker project"
git branch -M main
git remote add origin https://github.com/harshakanduri/flask-docker-app.git
git push -u origin main
```

GitHub Repo:  
```
https://github.com/harshakanduri/flask-docker-app
```

---

