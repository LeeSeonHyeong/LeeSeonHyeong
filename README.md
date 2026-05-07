<!-- ===== Header ===== -->
<h1 align="center">Hi there, I'm Lee Seon Hyeong 👋</h1>

<p align="center">
  <img src="https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/pokemon/132.png" width="80" alt="Ditto"/>
</p>

<p align="center">
  <em>Currently learning & growing at SSAFY · Aspiring Full-Stack & AI Developer</em>
</p>

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=linear_lee&label=Profile%20views&color=0e75b6&style=flat" alt="profile views"/>
</p>

---

## 🙋‍♂️ About Me

- 🎓 Currently studying at **SSAFY** (Samsung SW Academy For Youth)
- 💼 Job seeker preparing for a developer role
- 🌱 Interested in **AI (fine-tuning, RAG)** and **Full-Stack Development**
- 🛠️ Always exploring new tools and trying to ship better code

---

## 💼 Experience

**Ericsson-LG Korea Partners** — _Intern_
📅 **Jun 2025 – Aug 2025**
- Built an internal RAG-based onboarding chatbot for new and foreign employees
- Developed an automated ASN.1 code review tool to detect Non-Backward-Compatible (NBC) issues before deployment

---

## 🧰 Tech Stack

**Languages**
<p>
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black"/>
  <img src="https://img.shields.io/badge/MATLAB-0076A8?style=flat&logo=mathworks&logoColor=white"/>
</p>

**Frameworks & Tools**
<p>
  <img src="https://img.shields.io/badge/Django-092E20?style=flat&logo=django&logoColor=white"/>
  <img src="https://img.shields.io/badge/Flask-000000?style=flat&logo=flask&logoColor=white"/>
  <img src="https://img.shields.io/badge/Vue.js-4FC08D?style=flat&logo=vue.js&logoColor=white"/>
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white"/>
  <img src="https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white"/>
</p>

**Currently Learning**
<p>
  <img src="https://img.shields.io/badge/C-A8B9CC?style=flat&logo=c&logoColor=black"/>
  <img src="https://img.shields.io/badge/C++-00599C?style=flat&logo=c%2B%2B&logoColor=white"/>
</p>

---

## 🚀 Featured Projects

### 🤖 RAG-based Onboarding Chatbot
An internal AI chatbot designed to help **new hires and foreign employees** quickly find information that was scattered across the company's internal sites.

- **Problem:** All onboarding information existed on internal pages, but employees couldn't realistically read through everything. At the same time, sensitive internal data could not be exposed externally, and answers had to be **highly accurate** — hallucinations were not acceptable.
- **Solution:** Built a **RAG (Retrieval-Augmented Generation)** pipeline. Internal documents were migrated into a vector database, and the LLM generated answers strictly grounded in retrieved context.
- **Outcome:** Delivered a working prototype. Final integration with company SSO accounts was handed off to the in-house team due to internal security policies.
- **Stack:** Python, LLM, RAG, Vector DB

### 📑 ASN.1 NBC Code Review Automation
An AI-powered tool that automatically reviews **ASN.1 protocol diffs** to catch **Non-Backward-Compatible (NBC) issues** before they reach production.

- **Problem:** In telecom systems, NBC issues between equipment versions can cause severe communication failures. Once deployed, the cost of failure is enormous, and these issues are often **impossible to reproduce in a local test environment**.
- **Solution:** The tool parses each Git commit's `.asn` diff into hunks, sends them to an LLM (Qwen3-32B via EricAI) along with a curated set of ASN.1 rules and historical NBC cases, and produces a structured JSON verdict (`OK` / `NOK` + matched rule + reason). Results are rendered in an interactive Flask web report that highlights the exact lines causing each violation.
- **Evaluation:** Built a separate evaluation pipeline that runs predictions against a labeled `correct.csv`, computing **macro F1** and a **rule-match accuracy** metric to track improvements as prompts and rules evolve.
- **Stack:** Python, Flask, EricAI (Qwen3-32B), Git, scikit-learn, Regex-based diff parsing

> 🚧 Currently planning a personal side project — stay tuned.

---

## 📊 GitHub Stats

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=linear_lee&show_icons=true&theme=default&hide_border=true" alt="GitHub Stats" height="170"/>
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=linear_lee&theme=default&hide_border=true" alt="GitHub Streak" height="170"/>
</p>

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=linear_lee&layout=compact&theme=default&hide_border=true" alt="Top Languages" height="170"/>
</p>

---

<p align="center">
  <em>Thanks for stopping by! ✨</em>
</p>
