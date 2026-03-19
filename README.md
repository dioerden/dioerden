# Hi, I'm raden muhammad yudie sanjaya 👋
<p align="center">
</p>

### 🔬 Seismology AI & Autonomous Systems | Computational Physicist | LIBS Specialist

I am a physicist and developer focused on the intersection of **Seismology** and **Autonomous AI**. 
My work revolves around building agentic ecosystems for automated earthquake detection, picking, and seismic signal processing in high-noise industrial environments.

---

## ⚡ Current Main Project: SeisAgent-PisDL
**Autonomous Earthquake Detection System for Noisy Environments (Aceh Utara & Lhokseumawe Case)**

Since the study area is located near industrial zones with high cultural noise and lacks high-quality manual picking (Label Scarcity), I've developed a **Self-Supervised / Transfer Learning** framework using **PisDL (Physics-Informed Deep Learning)**.

### 🏗️ Modified System Architecture
```mermaid
graph TD
    subgraph Lab_Data [1. Data Source]
        A[Sensor Node: Aceh Utara] -->|Stream| B[SeedLink Server]
        B -->|mseed| C[Data Buffer]
    end

    subgraph Intelligence [2. ElizaOS Orchestrator]
        C -->|Watchdog| D[ElizaOS Core Agent]
        D -->|Task: Extract Phase| E[Plugin SeisBench-PisDL]
        D -->|Task: Context| F[Memory RAG: Toba & Aceh History]
    end

    subgraph Engine [3. Compute Engine - PisDL]
        E -->|Model| G[PhaseNet - piSDL Weights]
        G -->|Output| H[Pseudo-Labels P & S Picks]
    end

    subgraph Logic [4. Validation Bridge - NO MANUAL LABELS]
        H --> I{Spatial Coincidence?}
        I -->|Single Station| J[Flag: Industrial Noise Filter]
        I -->|Multi-Station| K[Flag: Valid Tectonic Event]
        K --> L[Cross-Correlation Refinement]
    end

    subgraph Output [5. Expert & Dissemination]
        L --> M[LLM: Geophysical Reasoning]
        M --> N[LaTeX Paper Tables]
        M --> O[Telegram Alert: 'PisDL Detected Swarm']
    end

    style Lab_Data fill:#f9f9f9,stroke:#333
    style Intelligence fill:#e6f7ff,stroke:#1890ff
    style Logic fill:#fff7e6,stroke:#fa8c16
    style Engine fill:#fff1f0,stroke:#cf1322
```

### 🛠️ Key Research Strategies
- **Cross-Station Coincidence**: Filtering industrial noise by correlating signal arrival times across the network.
- **PisDL as Synthetic Expert**: Generating high-confidence **Pseudo-Labels** (> 0.95) for model adaptive fine-tuning.
- **Nightly Baseline Calibration**: Automated signal baseline acquisition during midnight (00:00-04:00 WIB) to obtain the cleanest environment signature.

---

### 🧰 Tech Stack
| Domain | Tools & Languages |
| :--- | :--- |
| **Seismology & AI** | ![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white) ![SeisBench](https://img.shields.io/badge/SeisBench-Toolbox-blue?style=flat-square) ![ObsPy](https://img.shields.io/badge/ObsPy-Seismic-green?style=flat-square) |
| **Autonomous Agent**| ![ElizaOS](https://img.shields.io/badge/ElizaOS-Orchestrator-blueviolet?style=flat-square) ![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=node.js&logoColor=white) |
| **Engineering** | ![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white) ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white) ![HPC](https://img.shields.io/badge/HPC-Cluster-blue?style=flat-square) |

---

<p align="center">
  © 2026 raden muhammad yudie sanjaya | Building the Intelligence of Earth 🌍
</p>
