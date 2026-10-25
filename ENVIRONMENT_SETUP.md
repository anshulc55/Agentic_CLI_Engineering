# Python Virtual Environment & Jupyter Setup Guide (macOS & Windows)

Follow these steps to create an isolated Python virtual environment, install the required libraries, and connect the environment on **macOS** or **Windows**.

---

## 0. Windows Prerequisite: Bash Shell (`Git Bash` or `WSL2`)

Because Claude Code and these course notebooks execute POSIX shell pipelines (`%%bash`), **Windows users** need either:
1. **Git for Windows (Git Bash)** installed with `C:\Program Files\Git\bin` and `C:\Program Files\Git\usr\bin` added to your system `PATH` (recommended for running natively on Windows), **OR**
2. **WSL2 (Ubuntu)** enabled.

*(macOS and Linux users already have `bash` and Unix utilities built in.)*

---

## 1. Navigate to the Project Directory

Open your terminal (**Terminal / iTerm2** on macOS, or **Git Bash / PowerShell** on Windows) and navigate to your workspace folder:

```bash
cd /path/to/Agentic_CLI_Engineering
```

---

## 2. Create and Activate the Virtual Environment

### On macOS / Linux / WSL2 (`zsh` / `bash`)
```bash
# Create the virtual environment
python3 -m venv .venv

# Activate the virtual environment
source .venv/bin/activate
```

### On Windows (`Git Bash`)
```bash
# Create the virtual environment
python -m venv .venv

# Activate the virtual environment in Git Bash
source .venv/Scripts/activate
```

### On Windows (`PowerShell`)
```powershell
# Create the virtual environment
python -m venv .venv

# Activate the virtual environment in PowerShell
.\.venv\Scripts\Activate.ps1
```

> **Tip:** Once activated, your terminal prompt will display `(.venv)`.

---

## 3. Install Required Libraries

With `(.venv)` active, upgrade `pip` and install all course dependencies from `requirements.txt`:

```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```

---

## 4. Register the Virtual Environment as a Jupyter Kernel

Register `.venv` as a named kernel so it appears in Jupyter and IDE kernel pickers:

```bash
python -m ipykernel install --user --name=agentic-cli --display-name="Python (Agentic CLI)"
```

---

## 5. Select the Kernel & Run the Notebooks

### Option A: In Your IDE (Antigravity / VS Code / Cursor)

1. Open `1_1_the_agentic_shift.ipynb` or `1_2_engine_initialization.ipynb`.
2. Click **Select Kernel** in the top-right corner of the notebook toolbar.
3. Select **Python Environments...** (or **Jupyter Kernel...**).
4. Choose **`.venv`** or **`Python (Agentic CLI)`**.

### Option B: In Browser via Jupyter Notebook / JupyterLab

With `.venv` active in your terminal (macOS Terminal or Windows Git Bash), launch Jupyter directly:

```bash
jupyter notebook
```

*(Launching Jupyter from the active `.venv` shell automatically passes your virtual environment's `PATH` into all `%%bash` cells.)*

---

## 6. Deactivating the Environment (When Finished)

To exit the virtual environment at any time, run:

```bash
deactivate
```
