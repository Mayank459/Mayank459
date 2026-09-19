<!-- ═══════════════════════════════════════════════════════════════
     Profile README · Mayank459
     Lives in: github.com/Mayank459/Mayank459  (README.md at repo root)
     Also needs: assets/pipeline.svg  +  .github/workflows/snake.yml
     ═══════════════════════════════════════════════════════════════ -->

<div align="center">

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:0f0c29,50:302b63,100:24243e&height=240&section=header&text=Mayank&fontSize=80&fontColor=ffffff&fontAlignY=38&animation=fadeIn&desc=I%20build%20engines%20that%20understand%20code%20%E2%80%A2%20AI%20%C3%97%20Systems%20%C3%97%20Data&descSize=18&descAlignY=60&descColor=a5b4fc" alt="header" />

<a href="https://github.com/Mayank459/CodeBase">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&duration=3000&pause=900&color=A78BFA&center=true&vCenter=true&width=760&height=50&lines=%24+whoami+%E2%86%92+Mayank;Building+CodeBase+%E2%80%94+a+Repository+Intelligence+Engine;AST+Parsing+%E2%80%A2+Call+Graphs+%E2%80%A2+Multi-Agent+RAG;Guardrails+%E2%80%A2+Evals+%E2%80%A2+Observability;Python+%7C+FastAPI+%7C+React+%7C+LangGraph+%7C+ML" alt="Typing SVG" />
</a>

<br/>

<img src="https://komarev.com/ghpvc/?username=Mayank459&label=Profile+Views&style=for-the-badge&color=7c3aed" alt="views" />
<a href="https://code-base-tau.vercel.app"><img src="https://img.shields.io/badge/CodeBase-Live%20Demo-22c55e?style=for-the-badge&logo=vercel&logoColor=white&labelColor=0f0c29" alt="live demo" /></a>
<a href="https://github.com/Mayank459?tab=repositories"><img src="https://img.shields.io/badge/Public%20Repos-18-a78bfa?style=for-the-badge&logo=github&labelColor=0f0c29" alt="repos" /></a>

</div>

<br/>

---

## 👨‍💻 &nbsp;About Me

```python
class Mayank:
    handle    = "Mayank459"
    focus     = ["AI-powered developer tools", "RAG & multi-agent systems", "ML applications"]
    flagship  = "CodeBase — repository intelligence engine (FastAPI + LangGraph + Qdrant + React)"
    also_built = ["AutoML dashboard", "AI diet planner", "gesture-based virtual mouse"]
    practices = ["Guardrails first", "Evals over vibes", "Observability by default", "CI on every push"]
    sharpening = ["Data Structures & Algorithms", "System design", "CS fundamentals"]

    def philosophy(self):
        return "If it can't be measured, traced and tested — it isn't production-ready."
```

---

## ⚡ &nbsp;Flagship Project — [CodeBase](https://github.com/Mayank459/CodeBase)

> **An enterprise-style repository intelligence platform.** Point it at a codebase, and it parses it into ASTs, builds a topological call graph, indexes it in a vector DB, and lets you *chat with the architecture* — with safety guardrails, automated evals and Prometheus telemetry built in.

<div align="center">
  <img width="100%" src="assets/pipeline.svg" alt="CodeBase animated pipeline" />
</div>

<br/>

<div align="center">

<a href="https://code-base-tau.vercel.app"><img src="https://img.shields.io/badge/🚀_Live_Demo-code--base--tau.vercel.app-22c55e?style=for-the-badge&labelColor=0f0c29" alt="demo" /></a>
<a href="https://github.com/Mayank459/CodeBase"><img src="https://img.shields.io/badge/📂_Source-Mayank459%2FCodeBase-7c3aed?style=for-the-badge&labelColor=0f0c29" alt="source" /></a>
<a href="https://github.com/Mayank459/CodeBase/blob/main/BACKEND_ARCHITECTURE.md"><img src="https://img.shields.io/badge/🏛️_Architecture-Read_the_Spec-0ea5e9?style=for-the-badge&labelColor=0f0c29" alt="architecture" /></a>

</div>

<table>
  <tr>
    <td width="50%" valign="top">

**🧠 What it does**
- 🌳 Tree-sitter **AST decomposition** into a class/function symbol index
- 🕸️ **NetworkX call-graph** with BFS caller/callee tracing
- 🔎 **Hybrid retrieval** — Cohere 384-d embeddings in **Qdrant**
- 🤖 **LangGraph multi-agent** runtime: router → retriever / traverser / auditor → synthesizer
- 📡 Token-by-token **SSE streaming** to a React workstation UI
- 🔒 CVE-style **security audit**, ✂️ **dead-code detection**, 📐 **UML generation**, 🔄 **multi-repo diff**, 🚀 **human-in-the-loop PR gate**

</td>
    <td width="50%" valign="top">

**🛡️ What makes it production-grade**
- **Input guardrail** — prompt-injection / jailbreak defense
- **Output guardrail** — secret & PII scrubbing (`[REDACTED_API_KEY]`)
- **Citation validator** — flags hallucinated files & symbols
- **Evals harness** — Hit Rate@K, MRR, Faithfulness, Grounding
- **Prometheus** `/metrics` — latency histograms, token counters, violation counters
- **Docker Compose** stack: backend + Qdrant + Prometheus
- **GitHub Actions** CI: `ruff` → `pytest` → evals → Docker build

</td>
  </tr>
</table>

<div align="center">

<sub>📊 Sample output from the repo's own eval suite (`python evals/run_evals.py`)</sub>

| Hit Rate @ 1 | Hit Rate @ 3 | MRR | Citation Grounding | Faithfulness | Answer Relevancy |
|:---:|:---:|:---:|:---:|:---:|:---:|
| **100%** | **100%** | **1.00** | **100%** | **85.2%** | **79.4%** |

</div>

<details>
<summary><b>🗺️ Click to expand — CodeBase agent flow (Mermaid)</b></summary>

```mermaid
flowchart LR
    Q([Developer Query]) --> IG{Input Guardrail}
    IG -->|blocked| X([400 Blocked])
    IG -->|clean| R{Intent Router}
    R -->|architecture| BFS[Graph Traverser · BFS]
    R -->|semantics| VEC[Dense Hybrid Retriever]
    R -->|security / hygiene| AUD[CVE & Dead-Code Engine]
    BFS --> S[Synthesizer Agent]
    VEC --> S
    AUD --> S
    S --> OG[Secret Scrubber + Citation Validator]
    OG --> UI([SSE Stream → React UI])
    OG -.-> M[(Prometheus /metrics)]
```

</details>

---

## 🧪 &nbsp;More Projects

<table>
  <tr>
    <td width="33%" valign="top">

### 📊 [AutoML Dashboard](https://github.com/Mayank459/streamlit-automl-project)
`Streamlit` `mljar-supervised` `scikit-learn` `Plotly`

No-code, **end-to-end data science** in one app: upload CSV/Excel → EDA & visualizations → Random Forest with GridSearchCV, K-Means with the elbow method, or full **AutoML** (Explain / Perform / Compete / Optuna) → predictions → download trained models.

</td>
    <td width="33%" valign="top">

### 🥗 [DietPlanner](https://github.com/Mayank459/DietPlanner)
`Python` `CatBoost` `PyTorch` `Jupyter`

An **ML-driven diet planning system** — calorie-requirement prediction trained on a 10K-user dataset, a meal recommender, and a **food image classifier** built on the NutritionVerse dataset, developed across 9 experiment notebooks with an API layer on top.

</td>
    <td width="33%" valign="top">

### 🖱️ [Virtual Mouse](https://github.com/Mayank459/Virtual_Mouse)
`Python` `Computer Vision`

A **gesture-controlled mouse** experiment — controlling the cursor with hand movements instead of hardware. *(Early stage — just getting started.)*

</td>
  </tr>
</table>

<div align="center">

<a href="https://github.com/Mayank459/CodeBase"><img src="https://github-readme-stats.vercel.app/api/pin/?username=Mayank459&repo=CodeBase&theme=tokyonight&hide_border=true&bg_color=0f0c29" alt="CodeBase" /></a>
<a href="https://github.com/Mayank459/streamlit-automl-project"><img src="https://github-readme-stats.vercel.app/api/pin/?username=Mayank459&repo=streamlit-automl-project&theme=tokyonight&hide_border=true&bg_color=0f0c29" alt="AutoML" /></a>

<a href="https://github.com/Mayank459/DietPlanner"><img src="https://github-readme-stats.vercel.app/api/pin/?username=Mayank459&repo=DietPlanner&theme=tokyonight&hide_border=true&bg_color=0f0c29" alt="DietPlanner" /></a>
<a href="https://github.com/Mayank459/Virtual_Mouse"><img src="https://github-readme-stats.vercel.app/api/pin/?username=Mayank459&repo=Virtual_Mouse&theme=tokyonight&hide_border=true&bg_color=0f0c29" alt="Virtual Mouse" /></a>

</div>

---

## 🛠️ &nbsp;Tech Arsenal

<div align="center">

**Core stack**

<img src="https://skillicons.dev/icons?i=py,fastapi,react,vite,js,html,css&theme=dark" alt="core" />

**ML & Data**

<img src="https://skillicons.dev/icons?i=pytorch,sklearn,pandas,numpy&theme=dark" alt="ml" />

<img src="https://img.shields.io/badge/LangGraph-Multi--Agent-f97316?style=flat-square" />
<img src="https://img.shields.io/badge/Qdrant-Vector_DB-DC2626?style=flat-square&logo=qdrant&logoColor=white" />
<img src="https://img.shields.io/badge/Tree--sitter-AST-22c55e?style=flat-square" />
<img src="https://img.shields.io/badge/NetworkX-Graphs-0ea5e9?style=flat-square" />
<img src="https://img.shields.io/badge/CatBoost-GBDT-fbbf24?style=flat-square" />
<img src="https://img.shields.io/badge/Streamlit-Apps-FF4B4B?style=flat-square&logo=streamlit&logoColor=white" />
<img src="https://img.shields.io/badge/Plotly-Viz-3F4F75?style=flat-square&logo=plotly&logoColor=white" />
<img src="https://img.shields.io/badge/LLMs-Gemini_·_Groq_·_Cohere-7c3aed?style=flat-square" />

**DevOps & Observability**

<img src="https://skillicons.dev/icons?i=docker,githubactions,prometheus,vercel,git,github,linux,vscode&theme=dark" alt="devops" />

</div>

---

## 📊 &nbsp;GitHub Analytics

<div align="center">

<img height="180" src="https://github-readme-stats.vercel.app/api?username=Mayank459&show_icons=true&theme=tokyonight&hide_border=true&count_private=true&include_all_commits=true&bg_color=0f0c29" alt="stats" />
<img height="180" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Mayank459&layout=compact&theme=tokyonight&hide_border=true&langs_count=8&bg_color=0f0c29" alt="top languages" />

<img src="https://streak-stats.demolab.com?user=Mayank459&theme=tokyonight&hide_border=true&background=0f0c29&stroke=302b63&ring=a78bfa&fire=f97316&currStreakLabel=a78bfa" alt="streak" />

<img width="100%" src="https://github-readme-activity-graph.vercel.app/graph?username=Mayank459&theme=tokyo-night&hide_border=true&area=true&custom_title=Mayank%27s%20Contribution%20Graph&bg_color=0f0c29&color=a78bfa&line=7c3aed&point=ffffff" alt="activity graph" />

</div>

---

## 🐍 &nbsp;Contribution Snake

<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)"  srcset="https://raw.githubusercontent.com/Mayank459/Mayank459/output/github-snake-dark.svg" />
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Mayank459/Mayank459/output/github-snake.svg" />
    <img alt="snake eating my contributions" src="https://raw.githubusercontent.com/Mayank459/Mayank459/output/github-snake-dark.svg" />
  </picture>
</div>

---

## 🧠 &nbsp;Engineering Principles

<table align="center">
  <tr>
    <td align="center" width="25%">🛡️<br/><b>Guardrails First</b><br/><sub>Sanitize inputs, scrub outputs,<br/>validate every citation.</sub></td>
    <td align="center" width="25%">📏<br/><b>Measure Everything</b><br/><sub>Hit Rate, MRR, faithfulness —<br/>evals run in CI.</sub></td>
    <td align="center" width="25%">🔭<br/><b>Observable by Default</b><br/><sub>Structured logs, trace spans,<br/>Prometheus metrics.</sub></td>
    <td align="center" width="25%">🚢<br/><b>Ship It Containerized</b><br/><sub>Docker Compose, health checks,<br/>GitHub Actions pipelines.</sub></td>
  </tr>
</table>

---

## 🎯 &nbsp;Currently

- 🔭 Evolving **CodeBase** — deeper agents, better retrieval, more evals
- 📚 Sharpening **DSA & CS fundamentals** ([LeetCode resources](https://github.com/Mayank459/awesome-leetcode-resources) · [GATE/CSE notes](https://github.com/Mayank459/GATE-and-CSE-Resources-for-Students))
- 🧩 Turning experiments (DietPlanner, Virtual Mouse) into polished, documented projects
- 🤝 Open to feedback, ideas and collaboration on AI-for-developer-tools

---

## 🤝 &nbsp;Let's Connect

<div align="center">

<a href="https://github.com/Mayank459"><img src="https://img.shields.io/badge/GitHub-Mayank459-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub" /></a>
<a href="https://code-base-tau.vercel.app"><img src="https://img.shields.io/badge/CodeBase-Live_Demo-22c55e?style=for-the-badge&logo=vercel&logoColor=white" alt="Live demo" /></a>
<!-- Uncomment & fill in whichever you want to show:
<a href="https://www.linkedin.com/in/YOUR_LINKEDIN/"><img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
<a href="mailto:YOUR_EMAIL@example.com"><img src="https://img.shields.io/badge/Email-Say_Hi-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
<a href="https://twitter.com/YOUR_HANDLE"><img src="https://img.shields.io/badge/X-Follow-000000?style=for-the-badge&logo=x&logoColor=white" alt="X" /></a>
-->

</div>

---

<div align="center">

<img src="https://quotes-github-readme.vercel.app/api?type=horizontal&theme=tokyonight&quote_color=a78bfa&bg_color=0f0c29&border_color=302b63" alt="dev quote" />

<br/><br/>

<sub>⭐ Built for engineers who like to look under the hood — a star on <a href="https://github.com/Mayank459/CodeBase">CodeBase</a> keeps the coffee flowing ☕</sub>

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:24243e,50:302b63,100:0f0c29&height=140&section=footer&reversal=true" alt="footer" />

</div>
