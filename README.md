# Akila Wasalathilaka 👋

[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](LICENSE)
[![GitHub Stars](https://img.shields.io/github/stars/akilaisadev?style=flat-square&logo=github)](https://github.com/akilaisadev)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=flat-square&logo=linkedin)](https://www.linkedin.com/in/akila-wasalathilaka)
[![Portfolio](https://img.shields.io/badge/Portfolio-akila.dev-red?style=flat-square)](https://akila.dev)

**Full-Stack AI Engineer & Security Researcher**

Crafting intelligent, secure, and high-performance solutions. Specialized in Deep Learning, Computer Vision, and proactive threat intelligence platforms.

---

## 📋 Table of Contents
- [🛠 Tech Stack](#-tech-stack)
- [🚀 Featured Projects](#-featured-projects)
  - [🛡️ PRISM (Threat Intelligence & Risk Assessment)](#-prism-threat-intelligence--risk-assessment)
  - [📱 Meduza (Censorship-Resistant News Reader)](#-meduza-censorship-resistant-news-reader)
  - [🌍 Slum Detection (Satellite Image AI Analyser)](#-slum-detection-satellite-image-ai-analyser)
- [📈 GitHub Stats](#-github-stats)
- [📬 Connect with Me](#-connect-with-me)

---

## 🛠 Tech Stack

- **Languages**: Python, TypeScript, JavaScript, C++, Kotlin, Go
- **AI / ML / CV**: PyTorch, TensorFlow, OpenCV, HuggingFace, Scikit-Learn
- **Backend & APIs**: FastAPI, Node.js, Express, Go-Fiber
- **Frontend / Mobile**: React, Next.js, Android (Kotlin/Java)
- **Infra & DevOps**: Docker, Kubernetes, AWS, PostgreSQL, Redis, GitHub Actions

---

## 🚀 Featured Projects

### 🛡️ PRISM (Threat Intelligence & Risk Assessment)
[![Live Demo](https://img.shields.io/badge/Live-Demo-brightgreen?style=for-the-badge&logo=vercel)](https://prism.akila.dev)
[![Documentation](https://img.shields.io/badge/Docs-View-blue?style=for-the-badge&logo=read-the-docs)](https://prism.akila.dev/docs)

PRISM is a proactive threat intelligence and security risk assessment platform designed to identify, analyze, and mitigate cyber threats before they impact your infrastructure.

#### ✨ Key Features
- **Proactive Threat Hunting**: Automated network anomaly detection and traffic classification.
- **Risk Scoring**: Real-time risk prioritization powered by machine learning classifiers.
- **Interactive Dashboard**: Rich telemetry visualization and incident response workflows.

#### ⚠️ Risk Examples & Incident Severity
PRISM categorizes risk into actionable, multi-tier threat vectors:
- **Critical (Score 9.0+)**: Potential active database exfiltration attempt / anomalous SSH traffic patterns.
- **High (Score 7.0-8.9)**: Multiple failed login attempts combined with suspicious geographic origin.
- **Medium (Score 4.0-6.9)**: Unauthorized internal port scanning or configuration drift detected.

#### ⚙️ Quick Self-Hosting
Start PRISM locally using the pre-configured `Makefile`:
```bash
git clone https://github.com/akilaisadev/prism.git
cd prism
make setup      # Install dependencies and setup environment
make up         # Spin up PostgreSQL, Redis, and FastAPI app
```

---

### 📱 Meduza (Censorship-Resistant News Reader)
[![Download APK](https://img.shields.io/badge/Download-APK-green?style=for-the-badge&logo=android)](https://github.com/akilaisadev/meduza/releases)
[![Build Status](https://img.shields.io/github/actions/workflow/status/akilaisadev/meduza/android.yml?style=flat-square)](https://github.com/akilaisadev/meduza/actions)

Meduza is a lightweight, decentralized, and censorship-resistant client application designed to deliver independent journalism to restricted regions.

#### 📸 Showcase & App Screenshots
<p align="center">
  <img src="https://raw.githubusercontent.com/akilaisadev/meduza/main/assets/screenshot_home.png" width="250" alt="Meduza Home Screen" style="border-radius: 10px; margin: 10px;" />
  <img src="https://raw.githubusercontent.com/akilaisadev/meduza/main/assets/screenshot_article.png" width="250" alt="Meduza Article Reader" style="border-radius: 10px; margin: 10px;" />
  <img src="https://raw.githubusercontent.com/akilaisadev/meduza/main/assets/screenshot_offline.png" width="250" alt="Meduza Offline Mode" style="border-radius: 10px; margin: 10px;" />
</p>

#### ⚖️ Comparison: Meduza vs. Traditional RSS Readers
| Feature | Meduza | Traditional RSS Readers |
| :--- | :---: | :---: |
| **Censorship Resistance** | **Yes (P2P & IPFS)** | No (Direct HTTP) |
| **Offline Cache** | **Yes (SQLite Local Sync)** | Partial |
| **Push Notifications** | **Decentralized Pub/Sub** | Centralized APNS/FCM |
| **Privacy / No Tracking** | **Tor/VPN routing ready** | IP/Cookie Logs |

---

### 🌍 Slum Detection (Satellite Image AI Analyser)
[![Paper](https://img.shields.io/badge/Research-Paper-orange?style=flat-square&logo=gitbook)](https://github.com/akilaisadev/slum-detection/raw/main/paper.pdf)
[![Model Card](https://img.shields.io/badge/HuggingFace-Model_Card-yellow?style=flat-square&logo=huggingface)](https://huggingface.co/akilaisadev/slum-detection-unet)

An end-to-end computer vision pipeline powered by deep semantic segmentation (U-Net + ResNet50 backbone) to automatically identify informal settlements in high-resolution satellite imagery.

#### 📊 Model Performance Metrics
```
┌────────────────────────────────────────────────────────┐
│  📈 slum-detection-unet: Validation Metrics (VHR-Sat)   │
├──────────────────────┬─────────────────────────────────┤
│  Metric              │  Score                          │
├──────────────────────┼─────────────────────────────────┤
│  AUC-ROC             │  0.942                          │
│  F1-Score            │  0.897                          │
│  IoU (Slum Class)    │  0.814                          │
│  Precision           │  0.912                          │
│  Recall              │  0.883                          │
└──────────────────────┴─────────────────────────────────┘
```

#### 🐍 Inference Example
```python
import torch
from slum_detector import SlumDetectorUNet

# Load pre-trained model and map to device
detector = SlumDetectorUNet.load_from_checkpoint("best_model.ckpt")
detector.eval().to("cuda" if torch.cuda.is_available() else "cpu")

# Run inference on high-resolution satellite image tile
satellite_image = detector.preprocess_image("data/tile_0912.png")
with torch.no_grad():
    prediction_mask = detector(satellite_image)

# Save classified informal settlement boundary overlay
detector.save_overlay(prediction_mask, "output/slum_overlay.png")
print("Inference completed. Overlay saved to output/slum_overlay.png.")
```

---

## 📈 GitHub Stats

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=akilaisadev&show_icons=true&theme=tokyonight&count_private=true" alt="Akila's GitHub Stats" />
  <br />
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=akilaisadev&layout=compact&theme=tokyonight" alt="Top Languages" />
</p>

---

## 📬 Connect with Me

- 📧 Email: [akilawasalathilaka@gmail.com](mailto:akilawasalathilaka@gmail.com)
- 💼 LinkedIn: [Akila Wasalathilaka](https://www.linkedin.com/in/akila-wasalathilaka)
- 🌐 Portfolio / Blog: [akila.dev](https://akila.dev)

---
Made with ❤️ by [Akila Wasalathilaka](https://github.com/akilaisadev)
