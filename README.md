<!-- ===== Header ===== -->
<h1 align="center">Hi there, I'm Lee Seon Hyeong 👋</h1>

<p align="center">
  <img src="https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/pokemon/132.png" width="80" alt="Ditto"/>
</p>

<p align="center">
  <em>Telecom engineering background · Building toward Infrastructure & AI Engineering at SSAFY</em>
</p>

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=GITHUB_ID&label=Profile%20views&color=0e75b6&style=flat" alt="profile views"/>
</p>

---

## 🙋‍♂️ About Me

- 🎓 B.S. in Electronics & Communication Engineering, Korea Maritime & Ocean University
- 🏫 SSAFY 15th (Samsung SW Academy For Youth), Python / full-stack track
- 🌱 Interested in **infrastructure & deployment**, **networks**, and **LLM evaluation / fine-tuning**
- 🔍 I build the verification first: test scripts before optimization, deploy scripts treated as test targets

---

## 💼 Experience

**SSAFY (Samsung Software Academy for Youth)**
📅 **Jan 2026 – Present**
- Full-time software engineering program (1,600+ hours), Python / full-stack track
- Team lead of a 6-member project (AJT); owned the infrastructure end-to-end
- Designed and implemented the K3s-based deployment pipeline for the specialized project (Hanjjak)

**Ericsson Korea Partners** — _Intern, PEG4 Site Operation_
📅 **Jun 2025 – Aug 2025**
- Built an internal RAG-based onboarding chatbot for new and foreign employees
- In a 3-person team, built the LLM integration module and evaluation pipeline for an ASN.1 Non-Backward-Compatible (NBC) checker — **F1 0.44 → 0.87**, critical-error detection **70% → 99%**

---

## 📄 Publication

**Performance Analysis of Digital Modulation Schemes for WPT-Powered Maritime Sensor Networks** — _First author_
Journal of Navigation and Port Research (KCI), Vol. 49, No. 6, pp. 742–748, Dec 2025 · [DOI: 10.5394/KINPR.2025.49.6.742](https://doi.org/10.5394/KINPR.2025.49.6.742)
- Showed that low-power rectification efficiency tracks the waveform's PAPR rather than the modulation scheme itself

---

## 🧰 Tech Stack

**Languages**
<p>
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/Kotlin-7F52FF?style=flat&logo=kotlin&logoColor=white"/>
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white"/>
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black"/>
</p>

**Backend & Frontend**
<p>
  <img src="https://img.shields.io/badge/Django-092E20?style=flat&logo=django&logoColor=white"/>
  <img src="https://img.shields.io/badge/Spring%20Boot-6DB33F?style=flat&logo=springboot&logoColor=white"/>
  <img src="https://img.shields.io/badge/Flask-000000?style=flat&logo=flask&logoColor=white"/>
  <img src="https://img.shields.io/badge/Vue.js-4FC08D?style=flat&logo=vue.js&logoColor=white"/>
  <img src="https://img.shields.io/badge/React-61DAFB?style=flat&logo=react&logoColor=black"/>
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white"/>
</p>

**Infra & DevOps**
<p>
  <img src="https://img.shields.io/badge/K3s-FFC61C?style=flat&logo=k3s&logoColor=black"/>
  <img src="https://img.shields.io/badge/Kubernetes-326CE5?style=flat&logo=kubernetes&logoColor=white"/>
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white"/>
  <img src="https://img.shields.io/badge/GitLab%20CI-FC6D26?style=flat&logo=gitlab&logoColor=white"/>
  <img src="https://img.shields.io/badge/Cloudflare-F38020?style=flat&logo=cloudflare&logoColor=white"/>
  <img src="https://img.shields.io/badge/Linux-FCC624?style=flat&logo=linux&logoColor=black"/>
  <img src="https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white"/>
</p>

**Research**
<p>
  <img src="https://img.shields.io/badge/MATLAB-0076A8?style=flat&logo=mathworks&logoColor=white"/>
  <img src="https://img.shields.io/badge/GNU%20Radio-000000?style=flat&logoColor=white"/>
</p>

**Currently Learning**
<p>
  <img src="https://img.shields.io/badge/C-A8B9CC?style=flat&logo=c&logoColor=black"/>
  <img src="https://img.shields.io/badge/C++-00599C?style=flat&logo=c%2B%2B&logoColor=white"/>
</p>

---

## 🚀 Featured Projects

### 🥢 Hanjjak — Idle Desktop Pet Game (SSAFY Specialized Project)
A low-fatigue idle game where a character lives on the Windows desktop. Chosen for the big-data / distributed track because an easy-to-enter game can bring in the real users and traffic the track requires.

- **My role:** Designed and implemented the infrastructure (`infra/k8s` manifests, `.gitlab-ci.yml`, deploy scripts) and built full-stack game features
- **Infra:** Single-node **K3s** on an Ubuntu VM running a Kotlin/Spring Boot API, a React web client, an admin console, and PostgreSQL (StatefulSet)
- **Exposure:** No NodePort / LoadBalancer / Ingress; only a **Cloudflare Tunnel** connects to the web ClusterIP Service, so the API and DB are never directly exposed
- **Deploy flow:** GitLab CI build → manual approval → DB backup → Flyway migration as a separate **Job** → API rolling update → verify the idle **Blue-Green** web slot → switch the Service selector
- **Known limitation:** Backups currently live on the VM's own disk; off-host backup is the next step
- **Stack:** Kotlin, Spring Boot, React, TypeScript, PostgreSQL, K3s, GitLab CI, Cloudflare Tunnel

### 📑 ASN.1 NBC Code Review Automation (Ericsson Korea Partners Internship)
An LLM-based tool that reviews **ASN.1 protocol diffs** and catches **Non-Backward-Compatible (NBC) issues** before they reach production.

- **Problem:** In telecom systems, NBC issues between equipment versions can cause severe communication failures, and they are often **impossible to reproduce in a local test environment**
- **Solution (team of 3):** The tool parses each commit's `.asn` diff into hunks and sends them to an LLM along with curated ASN.1 rules and past NBC cases. It returns a structured JSON verdict (`OK` / `NOK` + matched rule + reason), rendered in a Flask web report
- **My part:** The LLM integration module and a separate **evaluation pipeline** (macro F1 + rule-match accuracy against a labeled set). I used it to tune prompts and inference parameters
- **Result:** **F1 0.44 → 0.87**, critical-error detection **70% → 99%**
- **Stack:** Python, Flask, Qwen3-32B, scikit-learn, Git

### 🤖 RAG-based Onboarding Chatbot (Ericsson Korea Partners Internship)
An internal AI chatbot designed to help **new hires and foreign employees** quickly find information that was scattered across the company's internal sites.

- **Problem:** All onboarding information existed on internal pages, but employees couldn't realistically read through everything. At the same time, sensitive internal data could not be exposed externally, and answers had to be **highly accurate**: hallucinations were not acceptable.
- **Solution:** Built a **RAG (Retrieval-Augmented Generation)** pipeline. Internal documents were migrated into a vector database, and the LLM generated answers strictly grounded in retrieved context.
- **Outcome:** Delivered a working prototype. Final integration with company SSO accounts was handed off to the in-house team due to internal security policies.
- **Stack:** Python, LLM, RAG, Vector DB

### ♻️ Recycling VQA Challenge (SSAFY AI Challenge)
Multimodal multiple-choice VQA: given an image, a Korean question, and 4 options, pick the answer.

- **My role (team of 5):** Model selection and training pipeline design
- **Constraints:** 3 days of compute on a single RTX 5060 GPU
- **Approach:** Compared candidates on task fit, data size, and feasibility, then chose **Qwen2.5-VL-3B + 4-bit QLoRA**. Trained on answer text rather than bare letters and shuffled option order to reduce position shortcuts. Chose checkpoints by validation accuracy instead of loss
- **Inference:** Candidate scoring instead of free-form generation, plus option-order TTA and a seed ensemble
- **Result:** ~92% validation accuracy
