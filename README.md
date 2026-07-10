<p align="center">
  <img src="assets/dragon-fly.svg" alt="Animated fire-breathing dragon flying across the header" width="920" height="260" />
</p>

<h1 align="center">Akila Wasalathilaka</h1>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=22&pause=1000&color=34D399&center=true&vCenter=true&width=820&lines=Full-Stack+AI+Engineer;Security+Researcher;Deep+Learning+%7C+Computer+Vision+%7C+Threat+Intelligence" alt="Typing intro" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/License-Apache_2.0-2563EB?style=for-the-badge&logo=apache&logoColor=white" alt="License" />
  &nbsp;
  <img src="https://img.shields.io/github/stars/akilaisadev?style=for-the-badge&logo=github&color=111827" alt="GitHub Stars" />
  &nbsp;
  <a href="https://www.linkedin.com/in/akila-wasalathilaka">
    <img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" />
  </a>
  &nbsp;
  <img src="https://img.shields.io/badge/Portfolio-akila.dev-F97316?style=for-the-badge&logo=vercel&logoColor=white" alt="Portfolio" />
</p>

<p align="center">
  <a href="https://akila.dev">
    <img src="https://img.shields.io/badge/🌐_Visit_Portfolio-Live_Experience-10B981?style=for-the-badge&logo=vercel&logoColor=white" alt="Portfolio link" />
  </a>
</p>

<p align="center">
  <strong>Full-Stack AI Engineer &amp; Security Researcher</strong><br/>
  Crafting intelligent, secure, and high-performance systems across deep learning, computer vision, and proactive threat intelligence.
</p>

<br/>

<!-- ──────────────────────────────────────────────── -->
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=rect&color=gradient&customColorList=12,20,24&height=2&width=100%25" alt="divider"/>
</p>

## ⚡ Quick Snapshot

<div align="center">

| 🎯 Focus | 🛠 Stack | 🚀 What I Build |
|:---:|:---:|:---:|
| **AI / ML** | PyTorch · TensorFlow · HuggingFace · Scikit-Learn | Vision systems, predictive models, automation pipelines |
| **Backend** | FastAPI · Node.js · Express · Go-Fiber | APIs, secure services, real-time data flows |
| **Frontend / Mobile** | React · Next.js · Android | Clean interfaces, dashboards, mobile experiences |
| **Infra** | Docker · Kubernetes · AWS · PostgreSQL · Redis · GitHub Actions | Scalable deployments, CI/CD, observability |

</div>

<br/>

## 🔭 Featured Work

### 🛡️ PRISM: Threat Intelligence &amp; Risk Assessment
<p>
  <a href="https://prism.akila.dev"><img src="https://img.shields.io/badge/🔴_Live_Demo-prism.akila.dev-EF4444?style=for-the-badge" alt="Live Demo"/></a>
  &nbsp;
  <a href="https://prism.akila.dev/docs"><img src="https://img.shields.io/badge/📄_Docs-Read_More-64748B?style=for-the-badge" alt="Docs"/></a>
</p>

PRISM is a proactive threat intelligence and security risk assessment platform that helps identify, analyze, and mitigate cyber threats before they impact infrastructure.

- Proactive threat hunting with automated anomaly detection and traffic classification.
- Real-time risk scoring for faster incident prioritization.
- Interactive dashboards for telemetry, triage, and response workflows.

<details>
<summary>Risk tiers</summary>

- Critical: active exfiltration indicators or anomalous SSH behavior.
- High: repeated failed logins combined with suspicious origin signals.
- Medium: internal scanning or configuration drift.

</details>

<details>
<summary>Quick self-hosting</summary>

```bash
git clone https://github.com/akilaisadev/prism.git
cd prism
make setup
make up
```

</details>

---

### 🛰️ Slum Detection: Satellite Image AI Analyser
<p>
  <a href="https://github.com/akilaisadev/slum-detection/raw/main/paper.pdf"><img src="https://img.shields.io/badge/📑_Paper-Read_PDF-8B5CF6?style=for-the-badge" alt="Paper"/></a>
  &nbsp;
  <a href="https://huggingface.co/akilaisadev/slum-detection-unet"><img src="https://img.shields.io/badge/🤗_Model_Card-HuggingFace-FFB347?style=for-the-badge" alt="Model Card"/></a>
</p>

An end-to-end semantic segmentation pipeline built with U-Net and a ResNet50 backbone to identify informal settlements in high-resolution satellite imagery.

<details>
<summary>Validation metrics</summary>

| Metric | Score |
|:---|:---:|
| AUC-ROC | 0.942 |
| F1-Score | 0.897 |
| IoU (Slum Class) | 0.814 |
| Precision | 0.912 |
| Recall | 0.883 |

</details>

<details>
<summary>Inference example</summary>

```python
import torch
from slum_detector import SlumDetectorUNet

detector = SlumDetectorUNet.load_from_checkpoint("best_model.ckpt")
detector.eval().to("cuda" if torch.cuda.is_available() else "cpu")

satellite_image = detector.preprocess_image("data/tile_0912.png")
with torch.no_grad():
    prediction_mask = detector(satellite_image)

detector.save_overlay(prediction_mask, "output/slum_overlay.png")
print("Inference completed. Overlay saved to output/slum_overlay.png.")
```

</details>

<br/>

## 🧰 Tech Stack

<p align="center">
  <!-- Languages -->
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python"/>
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript"/>
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript"/>
  <img src="https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white" alt="C++"/>
  <img src="https://img.shields.io/badge/Kotlin-7F52FF?style=for-the-badge&logo=kotlin&logoColor=white" alt="Kotlin"/>
  <img src="https://img.shields.io/badge/Go-00ADD8?style=for-the-badge&logo=go&logoColor=white" alt="Go"/>
  <br/>
  <!-- AI/ML -->
  <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white" alt="PyTorch"/>
  <img src="https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white" alt="TensorFlow"/>
  <img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white" alt="OpenCV"/>
  <img src="https://img.shields.io/badge/HuggingFace-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black" alt="HuggingFace"/>
  <img src="https://img.shields.io/badge/Scikit--Learn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white" alt="Scikit-Learn"/>
  <br/>
  <!-- Backend -->
  <img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white" alt="FastAPI"/>
  <img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white" alt="Node.js"/>
  <img src="https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white" alt="Express"/>
  <br/>
  <!-- Frontend -->
  <img src="https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black" alt="React"/>
  <img src="https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white" alt="Next.js"/>
  <img src="https://img.shields.io/badge/Android-3DDC84?style=for-the-badge&logo=android&logoColor=white" alt="Android"/>
  <br/>
  <!-- Infra -->
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker"/>
  <img src="https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white" alt="Kubernetes"/>
  <img src="https://img.shields.io/badge/AWS-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white" alt="AWS"/>
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL"/>
  <img src="https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white" alt="Redis"/>
  <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white" alt="GitHub Actions"/>
</p>

<br/>

## 📊 GitHub Stats

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=akilaisadev&show_icons=true&theme=tokyonight&count_private=true&border_radius=12&hide_border=false&cache_seconds=1800&rank_icon=github" alt="Akila's GitHub Stats" />
  <br/><br/>
  <img src="https://streak-stats.demolab.com?user=akilaisadev&theme=tokyonight&hide_border=false&border_radius=12&date_format=j%20M%5B%20Y%5D" alt="GitHub Streak" />
  <br/><br/>
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=akilaisadev&layout=compact&theme=tokyonight&border_radius=12&hide_border=false&cache_seconds=1800&langs_count=8" alt="Top Languages" />
</p>

<br/>

## 🤝 Connect

<p align="center">
  <a href="mailto:akilawasalathilaka@gmail.com">
    <img src="https://img.shields.io/badge/Email-akilawasalathilaka@gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"/>
  </a>
  <br/><br/>
  <a href="https://www.linkedin.com/in/akila-wasalathilaka">
    <img src="https://img.shields.io/badge/LinkedIn-Akila_Wasalathilaka-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/>
  </a>
  <br/><br/>
  <a href="https://akila.dev">
    <img src="https://img.shields.io/badge/Portfolio_/_Blog-akila.dev-10B981?style=for-the-badge&logo=vercel&logoColor=white" alt="Portfolio"/>
  </a>
</p>

---

<p align="center">Made with ❤️ by <a href="https://github.com/akilaisadev">Akila Wasalathilaka</a></p>
