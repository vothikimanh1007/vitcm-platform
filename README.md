# 🌿 Vi-TCM AI Assistant: Topological Clinical Decision Support System

[![Hugging Face Space](https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-Backend%20AI-yellow)](https://huggingface.co/spaces/YOUR_USERNAME/vitcm-ai-engine)
[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Live%20Demo-blue)](https://vothikimanh1007.github.io/vitcm-platform/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)

**Vi-TCM AI Assistant** is an advanced Clinical Decision Support System (CDSS) that applies Topological Data Analysis (TDA) to mathematically quantify the macroscopic synergy of herbal formulations in Vietnamese Traditional Medicine (TM).

This repository is the practical software implementation of the research paper: *"Knowledge-Driven Topological Data Analysis in Traditional Medicine: A Macroscopic Synergy Approach"*.

---

## 🚀 Key Features for Practitioners & Researchers

- **Digitized Pharmacopoeia:** Access a curated database of over 700 medicinal herbs from the Vietnamese Pharmacopoeia, standardized by Nature/Flavor (Tính Vị) and Meridian Tropism (Quy Kinh).
- **Topological Synergy Scoring:** Utilizes real-time AI to calculate a synergy score based on the geometric complexity of the formulated pharmacological network.
- **Betti Curve Visualization:** Provides scientific visualization of "Synergistic Loops" ($H_1$), offering doctors mathematical evidence of multi-target mechanisms in complex prescriptions.
- **Interactive Formulation:** A drag-and-drop "Digital Prescription Bowl" allowing practitioners to test herb combinations and receive instant structural feedback.

---

## 🧠 System Architecture

The platform is designed using a modern, serverless microservices architecture:

1.  **AI Backend (Hugging Face Spaces):** - Built on **FastAPI** for high-performance API routing.
    - Utilizes **Giotto-TDA** to compute Persistent Homology over Euclidean manifolds in real-time.
2.  **Frontend Dashboard (GitHub Pages):**
    - A lightweight, responsive Single Page Application (SPA).
    - Data visualization powered by **Chart.js** and styled with **Tailwind CSS**.
    - Securely fetches computation payloads from the AI Backend.

---

## 🛠 Deployment & Usage Guide

### 1. Backend Setup (Hugging Face Spaces)
- Ensure the `curated_tm_features.pkl` dataset is uploaded to your Space.
- Install the required dependencies:
  ```bash
  pip install fastapi uvicorn giotto-tda pandas scikit-learn
