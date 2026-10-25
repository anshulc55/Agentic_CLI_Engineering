# Agentic CLI Engineering - Complete Claude Code Masterclass

[![Course](https://img.shields.io/badge/Course-Agentic%20CLI%20Engineering-blue)](https://github.com/anshulc55/Agentic_CLI_Engineering)
[![Claude Code](https://img.shields.io/badge/CLI-Claude%20Code%20v2.1+-purple)](https://docs.anthropic.com/en/docs/agents-and-tools/claude-code/overview)
[![Python](https://img.shields.io/badge/Python-3.11%20%7C%203.12-brightgreen)](https://www.python.org/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

A complete, hands-on, executable masterclass on architecting, governing, and scaling terminal-native autonomous coding agents using **Claude Code**.

---

## 🧭 Course Syllabus & Interactive Notebooks

### 🟢 Section 1 — Foundation & Memory Architecture
| Lecture | Title | Target Notebook | Focus Areas |
| :--- | :--- | :--- | :--- |
| **1.1** | The Agentic Shift: Terminal-Native vs. GUI IDE | [`1_1_the_agentic_shift.ipynb`](Foundation%20%26%20Memory%20Architecture/1_1_the_agentic_shift.ipynb) | OS-level agent execution, POSIX exit codes, Zero-copy Bash telemetry pipelines |
| **1.2** | Engine Initialization, OpenRouter Gateway & `/doctor` | [`1_2_engine_initialization.ipynb`](Foundation%20%26%20Memory%20Architecture/1_2_engine_initialization.ipynb) | Claude Code installation, OpenRouter settings, `ripgrep` indexing, system diagnostics |
| **1.3** | The `CLAUDE.md` Manifesto & Project Memory | [`1_3_claude_md_manifesto.ipynb`](Foundation%20%26%20Memory%20Architecture/1_3_claude_md_manifesto.ipynb) | `/init` package discovery, `<150-line` memory budget, Pydantic v2 & Async contracts |
| **1.4** | Hierarchical Memory Injection | [`1_4_hierarchical_memory.ipynb`](Foundation%20%26%20Memory%20Architecture/1_4_hierarchical_memory.ipynb) | 3-tier memory inheritance (`~/.claude`, `./`, `./backend`), instant `#` memory rules |
| **1.5** | Multi-Surface Synchronization (`/ide`) | [`1_5_ide_synchronization.ipynb`](Foundation%20%26%20Memory%20Architecture/1_5_ide_synchronization.ipynb) | VS Code/Cursor `/ide` IPC bridge, selection sync, live LSP diagnostics, visual diffs |

### 🟢 Section 2 — Interactive Session Mastery & Context Hygiene
| Lecture | Title | Target Notebook | Focus Areas |
| :--- | :--- | :--- | :--- |
| **2.1** | Read-First Reconnaissance | [`2_1_read_first_recon.ipynb`](Interactive%20Session%20Mastery%20%26%20Context%20Hygiene/2_1_read_first_recon.ipynb) | Sensor triad (`--allowedTools "Read,Grep,Glob"`), legacy microservice audit, zero disk mutations |
| **2.2** | Architectural Planning (`/plan` Mode) | [`2_2_architectural_plan_mode.ipynb`](Interactive%20Session%20Mastery%20%26%20Context%20Hygiene/2_2_architectural_plan_mode.ipynb) | `Shift+Tab` / `--permission-mode plan`, batch SQL queries, Redis cache-aside, HMAC JWT rotation |
| **2.3** | Context Window Hygiene & Surgical `/compact` | [`2_3_context_hygiene.ipynb`](Interactive%20Session%20Mastery%20%26%20Context%20Hygiene/2_3_context_hygiene.ipynb) | `/context` token telemetry, surgical compaction directives, Alembic PostgreSQL schema preservation |
| **2.4** | Dynamic Brain Swapping (`/model`, `/effort`, `/btw`) | [`2_4_dynamic_brain_swapping.ipynb`](Interactive%20Session%20Mastery%20%26%20Context%20Hygiene/2_4_dynamic_brain_swapping.ipynb) | 3-gear cognitive gearbox, ephemeral `/btw` queries, test scaffolding downshift, FinOps audit |
| **2.5** | Time Travel & State Recovery (`/rewind`) | [`2_5_state_recovery_rewind.ipynb`](Interactive%20Session%20Mastery%20%26%20Context%20Hygiene/2_5_state_recovery_rewind.ipynb) | Atomic code + context rollback (`double-Esc` / `/rewind`), avoiding split-brain hallucinations |

---

## 🚀 Quickstart & Environment Setup

### 1. Prerequisites
- **macOS** or **Linux** / **Windows (WSL2)**
- **Node.js 18+** (`npm install -g @anthropic-ai/claude-code`)
- **Python 3.11+**
- **Git** & **Ripgrep** (`brew install ripgrep` or `apt-get install ripgrep`)

### 2. Virtual Environment Setup
```bash
# Clone the repository
git clone https://github.com/anshulc55/Agentic_CLI_Engineering.git
cd Agentic_CLI_Engineering

# Create and activate Python virtual environment
python3 -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate

# Install required dependencies
pip install --upgrade pip
pip install -r requirements.txt
```

For detailed platform-specific notes, refer to [ENVIRONMENT_SETUP.md](ENVIRONMENT_SETUP.md).

### 3. Running the Notebooks
Launch Jupyter Lab or Notebook:
```bash
jupyter lab
```
Navigate to any section folder (`Foundation & Memory Architecture/` or `Interactive Session Mastery & Context Hygiene/`) and run through the cells step-by-step. Each notebook contains deterministic mock fallbacks and live CLI terminal execution guides.

---

## 🛡️ License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
