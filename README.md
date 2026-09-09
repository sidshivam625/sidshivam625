<div align="center">

<img src="assets/name.png" alt="Siddhant Shivam" width="720"/>

<a href="https://linkedin.com/in/siddhantshivam"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/></a>
<a href="mailto:siddhantshivam198@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white"/></a>
<a href="https://github.com/sidshivam625"><img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white"/></a>

</div>

---

### hi, i'm siddhant

- 🧠 &nbsp;**AI Researcher** at Mars Rover Manipal, working on vision and language models
- 🎓 &nbsp;**B.Tech Information Technology** at Manipal Institute of Technology
- 🗂 &nbsp;**Membership Chairperson** at the ACM Manipal Student Chapter
- 🕹 &nbsp;I made a tiny game called **Gradient Descent**. It is about local minima, which is also what most of my week is about.

<div align="center">

<a href="https://sidshivam625.github.io/sidshivam625/"><img src="assets/banner.png" alt="Play Gradient Descent" width="680"/></a>

</div>

> [!NOTE]
> **Currently chasing:** representation transfer. How much a frozen transformer already
> understands about a domain nobody trained it on, and whether that knowledge survives
> being moved to time series forecasting. Early answer: more than it has any right to.

<div align="center">

<img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white"/>
<img src="https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white"/>
<img src="https://img.shields.io/badge/C-A8B9CC?style=flat-square&logo=c&logoColor=black"/>
<img src="https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white"/>
<img src="https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=mysql&logoColor=white"/>
<img src="https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black"/>
<img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white"/>

<img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white"/>
<img src="https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white"/>
<img src="https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white"/>
<img src="https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white"/>
<img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white"/>
<img src="https://img.shields.io/badge/StyleGAN3-9146FF?style=flat-square&logo=nvidia&logoColor=white"/>

<img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white"/>
<img src="https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white"/>
<img src="https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB"/>
<img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white"/>
<img src="https://img.shields.io/badge/GCP-4285F4?style=flat-square&logo=googlecloud&logoColor=white"/>
<img src="https://img.shields.io/badge/Firebase-FFCA28?style=flat-square&logo=firebase&logoColor=black"/>

<img src="https://img.shields.io/badge/MCP-6E56CF?style=flat-square&logo=modal&logoColor=white"/>
<img src="https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square&logo=langchain&logoColor=white"/>
<img src="https://img.shields.io/badge/LlamaIndex-8A3FFC?style=flat-square&logo=meta&logoColor=white"/>
<img src="https://img.shields.io/badge/CrewAI-FF5A5F?style=flat-square&logo=openai&logoColor=white"/>
<img src="https://img.shields.io/badge/ChromaDB-FF6F00?style=flat-square&logo=databricks&logoColor=white"/>
<img src="https://img.shields.io/badge/FAISS-0081FB?style=flat-square&logo=meta&logoColor=white"/>

</div>

---

## what i've built

<details>
<summary><b>Groundhog</b> &nbsp;persistent memory for ML experiments &nbsp;<code>expand</code></summary>

<br>

Named for the film, because that is what running experiments feels like. The same day,
forever, with slightly different hyperparameters.

- Designed the memory graph schema in **Cognee**: typed nodes for experiments, datasets,
  artifacts and hypotheses, joined by lineage edges, with subagents handling config
  resolution, failure analysis and literature research.
- Built config canonicalisation and hashing on **FastAPI**, with duplicate detection that
  returns the earlier run's metrics instead of burning four more GPU hours proving the
  same thing twice.
- Shipped a **Python SDK**, a **React + Recharts** dashboard for parameter sensitivity
  analysis, and an **MCP server** exposing duplicate config checks and lineage lookup.

```mermaid
flowchart LR
    A["SDK<br/>log(run)"] --> B["FastAPI<br/>canonicalise + hash"]
    B --> C{"seen this<br/>config before?"}
    C -->|yes| D["return prior metrics<br/>0 GPU hours"]
    C -->|no| E["Cognee graph<br/>Kuzu + LanceDB"]
    E --> F["React dashboard"]
    E --> G["MCP server"]
    classDef n fill:#161B22,stroke:#8B949E,color:#C9D1D9
    classDef h fill:#1F6FEB,stroke:#1F6FEB,color:#FFFFFF
    class A,B,E,F,G n
    class C,D h
```

</details>

<details>
<summary><b>Synapse</b> &nbsp;MCP driven browser automation &nbsp;<code>expand</code></summary>

<br>

A Chrome extension that lets an agent finish the boring half of the internet.

- Designed the orchestrator schema and tool coordination logic on **FastMCP**, with GitHub
  and Notion MCP servers as the first multi app integration targets.
- Used **LangGraph** for stateful multi step orchestration, covering OTP retrieval,
  document understanding and form filling.
- Shipped as a **Chrome Extension** with secure credential management, because an agent
  holding your passwords deserves more scrutiny than one holding your calendar.

</details>

<details>
<summary><b>GANs from scratch</b> &nbsp;generative modelling and transfer learning &nbsp;<code>expand</code></summary>

<br>

- Implemented a full GAN pipeline in **PyTorch** on MNIST: generator and discriminator
  architecture, the adversarial training loop, and honest mode collapse diagnostics.
- Fine tuned **StyleGAN3** on a large image dataset, then ran latent space exploration and
  representation analysis for transfer learning experiments.
- Turned it into a hands on workshop for **50+ participants**, covering the training
  strategies that actually work rather than the ones in the paper.

</details>

<details>
<summary><b>Gradient Descent</b> &nbsp;the game above &nbsp;<code>expand</code></summary>

<br>

A pixel game about the thing that ruins training runs. A ball rolls down a loss landscape
and will happily settle in the first valley it finds. Your steering is capped, so it cannot
climb a real ridge. Escaping costs momentum, and momentum is limited.

Three landscapes, no engine, no dependencies. Plain canvas and about four hundred lines.
Every level was tuned against a physics simulation to guarantee three things: doing nothing
always ends trapped, level one is solvable by steering alone, and levels two and three
cannot be solved without spending momentum.

</details>

<details>
<summary><b>Open source</b> &nbsp;30+ commits to <code>coral/coral</code> &nbsp;<code>expand</code></summary>

<br>

Two merged pull requests, [#1058](https://github.com/withcoral/coral/pull/1058) and
[#1066](https://github.com/withcoral/coral/pull/1066), adding Chromium and Firefox source
support and improving compatibility across non WebKit engines.

</details>

---

## where it went well

| | | |
|:--|:--|:--|
| <img src="https://img.shields.io/badge/1st-FFB000?style=flat-square"/> | **Samsung PRISM Hackathon** `2025-26` | 450+ participants |
| <img src="https://img.shields.io/badge/2nd-C0C0C0?style=flat-square"/> | **Hack-Some-Thorns**, Best Project, IECSE Manipal | |
| <img src="https://img.shields.io/badge/3rd-CD7F32?style=flat-square"/> | **HackIndia x Adaption Labs**, AI Agent track | 425 teams |
| <img src="https://img.shields.io/badge/Top%2036-8957E5?style=flat-square"/> | **The Earth Prize**, scholars worldwide `2022` | 625 teams |

Also: a **Machine Learning workshop for 50+ students**, and the backend for **Cached CTF**
at Tech Tatva, running live leaderboard tracking for 200+ participants.

<div align="center">

<br>

<img src="https://github-readme-stats.vercel.app/api?username=sidshivam625&show_icons=true&hide_border=true&bg_color=0D1117&title_color=58A6FF&text_color=C9D1D9&icon_color=58A6FF&hide_title=true" height="140"/>
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=sidshivam625&layout=compact&hide_border=true&bg_color=0D1117&title_color=58A6FF&text_color=C9D1D9&langs_count=6" height="140"/>

<br><br>

*"the model is not the product. the loop around it is."*

</div>
