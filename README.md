# Yuliia Medun

Data Science & AI student at BUas with hands-on project experience across machine learning, deep learning, computer vision, NLP, and MLOps. Seeking an internship in data science or machine learning to apply these skills to real-world problems and keep learning.

**Contact Info:** [LinkedIn](https://www.linkedin.com/in/yuliia-medun-a2408233a/) ·  [Email](yuliiamedun@gmail.com)

---

## Skills

<table>
<tr>
<td valign="top"><b>Languages</b></td>
<td>

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white)

</td>
</tr>
<tr>
<td valign="top"><b>ML/DL</b></td>
<td>

![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white)
![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21E?style=flat-square&logo=huggingface&logoColor=black)
![scikit--learn](https://img.shields.io/badge/scikit--learn-F89939?style=flat-square&logo=scikitlearn&logoColor=white)
![Stable--Baselines3](https://img.shields.io/badge/Stable--Baselines3-F89939?style=flat-square)

</td>
</tr>
<tr>
<td valign="top"><b>Computer Vision</b></td>
<td>

![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white)
![U--Net](https://img.shields.io/badge/U--Net-6A5ACD?style=flat-square)
![scikit--image](https://img.shields.io/badge/scikit--image-6A5ACD?style=flat-square)

</td>
</tr>
<tr>
<td valign="top"><b>Robotics & RL</b></td>
<td>

![PyBullet](https://img.shields.io/badge/PyBullet-6A5ACD?style=flat-square)
![Gymnasium](https://img.shields.io/badge/Gymnasium-6A5ACD?style=flat-square)

</td>
</tr>
<tr>
<td valign="top"><b>NLP</b></td>
<td>

![spaCy](https://img.shields.io/badge/spaCy-09A3D5?style=flat-square&logo=spacy&logoColor=white)
![Whisper](https://img.shields.io/badge/Whisper-09A3D5?style=flat-square)
![RoBERTa](https://img.shields.io/badge/RoBERTa-09A3D5?style=flat-square)

</td>
</tr>
<tr>
<td valign="top"><b>MLOps & Infra</b></td>
<td>

![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2496ED?style=flat-square&logo=githubactions&logoColor=white)
![MLflow](https://img.shields.io/badge/MLflow-2496ED?style=flat-square&logo=mlflow&logoColor=white)
![Azure ML](https://img.shields.io/badge/Azure%20ML-2496ED?style=flat-square&logo=microsoftazure&logoColor=white)
![ClearML](https://img.shields.io/badge/ClearML-2496ED?style=flat-square)

</td>
</tr>
<tr>
<td valign="top"><b>Backend/Data</b></td>
<td>

![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-009688?style=flat-square&logo=postgresql&logoColor=white)
![MinIO](https://img.shields.io/badge/MinIO-009688?style=flat-square&logo=minio&logoColor=white)
![Azure Blob Storage](https://img.shields.io/badge/Azure%20Blob%20Storage-009688?style=flat-square)

</td>
</tr>
</table>

---

## 📌 Featured Projects

### Plant Phenotyping CV Platform | MLOps & Cloud Deployment
*Group project · Built on our earlier NPEC-related computer vision work*
 
A CV system that segments plant shoots and roots from images and extracts root-tip coordinates, deployed and continuously retrained across local, on-premise, and cloud environments. I was responsible for endpoint deployment and blue-green deployment on Azure (so new model versions ship with zero downtime), co-authored the project roadmap, and helped build the Docker/Docker Compose setup, the CI/CD pipeline, and the MinIO - Azure Blob Storage integration.
 
- Built a CI/CD pipeline (GitHub Actions -> GitHub Container Registry) publishing one set of container images that run unmodified across local, on-premise, and Azure Container Apps — no separate versions per environment, just different environment variables
- Set up blue-green deployment on Azure so new model versions go live with no downtime
- Implemented closed-loop retraining: the system retrains weekly on real usage data — user-confirmed correct predictions feed straight back into the training set, wrong ones go to professionals for manual labeling first
- Each new model is evaluated against a held-out test set and only replaces the current one in production if it actually scores better
- Set up test coverage gating in CI (70% minimum)
 
**Stack:**
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![MLflow](https://img.shields.io/badge/MLflow-0194E2?style=flat-square&logo=mlflow&logoColor=white)
![Azure ML](https://img.shields.io/badge/Azure%20ML-0078D4?style=flat-square&logo=microsoftazure&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4479A1?style=flat-square&logo=postgresql&logoColor=white)
![MinIO](https://img.shields.io/badge/MinIO-C72E49?style=flat-square)
 
[![Repo](https://img.shields.io/badge/-View%20Repo-181717?style=flat-square&logo=github)](#)

---

### Autonomous Root-Inoculation Robot | CV & RL Control
*Individual project · Built for [NPEC](https://www.npec.nl/) (Netherlands Plant Eco-phenotyping Centre)*
 
Built a full CV-to-control pipeline for a simulated Opentrons OT-2 lab robot: U-Net segmentation and skeletonization detect plant root tips, then a controller guides the pipette to each one with sub-millimeter precision.
 
- Benchmarked PPO (reinforcement learning) against a custom-tuned PID controller — PID won on results (99.7% vs. 40% success rate)
- Achieved 96% end-to-end success across 10 simulated test plates

**Stack:**
![PyBullet](https://img.shields.io/badge/PyBullet-4B8BBE?style=flat-square)
![Gymnasium](https://img.shields.io/badge/Gymnasium-00A98F?style=flat-square)
![Stable--Baselines3](https://img.shields.io/badge/Stable--Baselines3-6A5ACD?style=flat-square)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white)
![scikit--image](https://img.shields.io/badge/scikit--image-F7931E?style=flat-square)
![ClearML](https://img.shields.io/badge/ClearML-2D9CDB?style=flat-square)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
 
[![Repo](https://img.shields.io/badge/-View%20Repo-181717?style=flat-square&logo=github)](#)

---

### Ukrainian Video Emotion Classification | NLP Pipeline
*Group project · Built for [Content Intelligence Agency](https://www.contentintelligence.nl/), which builds AI tools for media makers to analyze film, TV, and video content*
 
Full pipeline: Ukrainian-language video in -> transcription -> translation -> emotion tagged per sentence -> output file. My part was the emotion classification stage and the full error analysis.
 
- Fine-tuned a Ukrainian RoBERTa transformer for 7-class emotion classification: genuinely underexplored territory, since labeled Ukrainian emotion data is extremely scarce
- Solved data scarcity by generating synthetic training data with a local LLM as a team, iterating past a naive first attempt that didn't match the real data's style — scaling the dataset from 48K to 556K sequences
- Model reached 78% accuracy (weighted F1 = 0.79), but my error analysis caught that this was actually just below a naive "always predict Neutral" baseline (macro F1 = 0.39) — a distinction that's easy to miss and easy to hide. Surfacing it, and diagnosing exactly why it happened, was what made our team's presentation stand out
- Authored a full model card covering ethics, PII masking, and a quantified carbon-footprint analysis
  
**Stack:**
![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21E?style=flat-square&logo=huggingface&logoColor=black)
![RoBERTa](https://img.shields.io/badge/RoBERTa-EE4C2C?style=flat-square)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![spaCy](https://img.shields.io/badge/spaCy-09A3D5?style=flat-square&logo=spacy&logoColor=white)
![Whisper](https://img.shields.io/badge/Whisper-412991?style=flat-square)
 
[![Repo](https://img.shields.io/badge/-View%20Repo-181717?style=flat-square&logo=github)](#)

---

### Temporal Root-Tip Tracking | Independent CV Research
*Individual project*
 
Designed and ran a statistically rigorous benchmark of 5 tip-tracking methods against a single-frame baseline on real plant time-series data.
 
- Applied repeated-measures ANOVA with Bonferroni correction across methods
- Found no significant accuracy improvement from temporal tracking (Hedges' g = 0.017) — a validated null result that redirected the team's engineering priorities
  
**Stack:**
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![scikit--image](https://img.shields.io/badge/scikit--image-F7931E?style=flat-square)
![Statistical Analysis](https://img.shields.io/badge/Statistical%20Analysis-8E44AD?style=flat-square)
 
[![Repo](https://img.shields.io/badge/-View%20Repo-181717?style=flat-square&logo=github)](#)

---

### IKEA PIN Terminal Analysis | Power BI Dashboard
*Individual project · Built for IKEA*
 
Power BI dashboard investigating terminal deployment patterns and compliance gaps to flag potential skimming risk.
 
- Identified a systematic terminal-rotation pattern (Eco 2–Eco 12) worth flagging as a compliance gap
- Found only 4 of 59 locations met the twice-weekly check requirement
  
**Stack:**
![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=flat-square&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-666666?style=flat-square)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
 
[![Repo](https://img.shields.io/badge/-View%20Repo-181717?style=flat-square&logo=github)](#)

---

 Currently completing my BSc in Applied Data Science & AI (anticipated July 2028) — looking for an internship in data science or ML engineering.
