<h1 align="center">Cyrille FOTSO</h1>
<p align="center"><b>Data Engineer / DataOps</b> · ESEO, Big Data & AI · Paris, France</p>

<p align="center">
  <a href="https://www.linkedin.com/in/cyrille-fotso-a25609428/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="mailto:cyrillefotso388@gmail.com"><img src="https://img.shields.io/badge/Email-333333?style=flat&logo=gmail&logoColor=white" alt="Email"></a>
</p>

---

### About me

I build data pipelines that are tested, reproducible and easy to run, and, lately, applications
that put a **local LLM** to work on real data without sending anything to the cloud. I care
about the DataOps side of the job: version control, automated tests, CI and containers, so that
the numbers, and the answers of the model, can be trusted.

- 🎓 Engineering graduate from **ESEO**, Big Data & Artificial Intelligence major
- 🔭 Recently built a local job-application assistant and an AI analyst that writes SQL, both on **Ollama**
- 🎯 Looking for a full-time (CDI) **Data Engineer / DataOps** position

### Tech stack

**Data** &nbsp;
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat&logo=postgresql&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![dbt](https://img.shields.io/badge/dbt-FF694B?style=flat&logo=dbt&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat&logo=redis&logoColor=white)

**AI** &nbsp;
![Ollama](https://img.shields.io/badge/Ollama-000000?style=flat&logo=ollama&logoColor=white)
![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=flat&logo=langchain&logoColor=white)

**Backend & web** &nbsp;
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat&logo=nextdotjs&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat&logo=streamlit&logoColor=white)

**DataOps** &nbsp;
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat&logo=githubactions&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat&logo=linux&logoColor=black)

**BI** &nbsp;
![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=flat&logo=powerbi&logoColor=black)
![Tableau](https://img.shields.io/badge/Tableau-E97627?style=flat&logo=tableau&logoColor=white)

**Also** &nbsp;
![Java](https://img.shields.io/badge/Java-007396?style=flat&logo=openjdk&logoColor=white)
![C](https://img.shields.io/badge/C-A8B9CC?style=flat&logo=c&logoColor=black)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)

### Featured projects

#### [job-copilot](https://github.com/CyrilleAdrien/job-copilot) &nbsp;[![CI](https://github.com/CyrilleAdrien/job-copilot/actions/workflows/ci.yml/badge.svg)](https://github.com/CyrilleAdrien/job-copilot/actions/workflows/ci.yml)

A job-application assistant that runs entirely on your laptop: it finds the offers that match your
profile, writes a CV and a cover letter for each one with a local LLM, then follows every
application from the recruiter's reply to the interview.

- **7 FastAPI microservices** behind a gateway, a **Next.js 15** interface, one **PostgreSQL** schema per service and **Redis Streams** events between them
- CV and letter written by **Ollama** (Qwen 2.5 7B), typeset with **Typst**, with a veracity check that flags any number or tool missing from the profile
- A full CV and letter studio: templates, automatic spacing to fit one page, live preview, AI tools to rewrite, proofread and translate
- Recruiter replies read over **IMAP** and classified, interviews synced over **CalDAV**, an assistant that only acts after the user confirms
- One `make up` with **Docker Compose**, daily backups, **CI** with 550+ Python tests, 300+ web tests and a Playwright end-to-end run

<p align="center">
  <a href="https://github.com/CyrilleAdrien/job-copilot"><img src="https://raw.githubusercontent.com/CyrilleAdrien/job-copilot/main/docs/images/architecture.svg" alt="job-copilot architecture" width="820"></a>
</p>

#### [Olist AI Analyst](https://github.com/CyrilleAdrien/olist-ai-analyst) &nbsp;[![CI](https://github.com/CyrilleAdrien/olist-ai-analyst/actions/workflows/ci.yml/badge.svg?branch=main)](https://github.com/CyrilleAdrien/olist-ai-analyst/actions/workflows/ci.yml)

An AI agent that answers business questions in French on the Olist warehouse and replies with a chart.

- **LangGraph** agent on `qwen2.5-coder:7b` through **Ollama**: the model writes the SQL, Python checks every number of the answer
- Safe by construction: **sqlglot** lets through one `SELECT` on the marts only, run by a read-only PostgreSQL role with a timeout
- Self-correcting: a refused or failing query goes back to the model with the error and a hint
- Measured on 30 questions with reference SQL: **29 / 30** answered correctly, median 5.4 s per question on a laptop
- **Streamlit** chat interface, unit and integration tests in **GitHub Actions**

<p align="center">
  <a href="https://github.com/CyrilleAdrien/olist-ai-analyst"><img src="https://raw.githubusercontent.com/CyrilleAdrien/olist-ai-analyst/main/docs/olist-ai-analyst-architecture.svg" alt="Olist AI Analyst architecture" width="820"></a>
</p>

#### [Olist Analytics](https://github.com/CyrilleAdrien/Olist-Analytics) &nbsp;[![CI](https://github.com/CyrilleAdrien/Olist-Analytics/actions/workflows/ci.yml/badge.svg?branch=main)](https://github.com/CyrilleAdrien/Olist-Analytics/actions/workflows/ci.yml)

End-to-end analytics pipeline on ~100,000 orders from a Brazilian marketplace, the warehouse
that Olist AI Analyst reads.

- Python ingestion of 9 raw CSV files into a **PostgreSQL** warehouse
- **dbt** layers (staging, intermediate, marts) with a star schema and automated data tests
- Fully containerised with **Docker**, rebuilt from scratch with a single `make all`
- **GitHub Actions** CI runs the whole pipeline and the tests on every pull request
- **Power BI** and **Tableau** dashboards with the same headline KPIs (revenue, orders, basket, review score)

<p align="center">
  <a href="https://github.com/CyrilleAdrien/Olist-Analytics"><img src="https://raw.githubusercontent.com/CyrilleAdrien/Olist-Analytics/main/docs/olist-architecture.svg" alt="Olist Analytics architecture" width="820"></a>
</p>

### Other projects

| Project | What it is | Stack |
|---|---|---|
| [Sudoku solver](https://github.com/CyrilleAdrien/Resolution-du-Sudoku) | Sudoku solver | C |
| [Connect Four](https://github.com/CyrilleAdrien/Jeu_Puissance_4) | Connect Four strategy game | Java |
| [MyZoo](https://github.com/CyrilleAdrien/MyZoo) | Web app to manage the animals of a zoo park | PHP, React |
