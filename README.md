# GitHub Dev Card Generator

An interactive full-stack application that dynamically generates beautiful, shareable developer profile cards based on GitHub user data. Built with a static frontend and a Python-powered serverless backend deployed seamlessly on Vercel.

---

## 🚀 Live Demo

Check out the live deployment here:  
👉 **[Live Demo Link](https://github-card-frontend-290964486654.us-central1.run.app/)**

---

## 📁 Project Structure

The project is structured as a monorepo, housing both the user interface and the API under one roof:

* **`github-card-generator/frontend`**: A fast, responsive frontend built with static web technologies (HTML, CSS, JavaScript).
* **`github-card-generator/backend`**: A Python-based API (`main.py`) that handles fetching, processing, and formatting data from the GitHub API.

---

## ⚙️ Architecture & Deployment

This project uses a unified monorepo configuration managed by **Vercel Serverless Functions**. 

* **Routing**: Standard web traffic routes directly to the static frontend asset folder.
* **API Execution**: Requests hitting `/api/*` are instantly directed to the Python backend application.
* **Configuration**: Orchestrated entirely via the root `vercel.json` file.

---

## 💻 Local Setup

If you want to run this project locally, follow these steps:

### Prerequisites
* Python 3.x installed
* A modern web browser

### 1. Clone the repository
```bash
git clone [https://github.com/Sai-Sri-Krishna/Github-Dev-Card.git](https://github.com/Sai-Sri-Krishna/Github-Dev-Card.git)
cd Github-Dev-Card
### 2. Run the Backend
```bash
cd github-card-generator/backend
pip install -r requirements.txt
python main.py
### 3. Run the Frontend
Simply open the index.html file inside the github-card-generator/frontend folder using any local browser or a live-server extension.

