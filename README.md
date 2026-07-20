# Quantum-Computing-Lab
M.Sc and M.Tech hands-on QC Lab IIT Jodhpur.

# About Teachers 
[`Maitreyee Sarkar`](https://sites.google.com/iitj.ac.in/maitreyee-sarkar-m-sa/home)
[`Vivek Balasaheb Sabale`](https://viveksabale1998.github.io)

[`Prof. Atul kumar`](https://atulk4.wixsite.com/atulk)


# 🧪 Setting up Python Environment with `uv`

This guide explains how to set up and use a Python environment using 

[`uv`](https://docs.astral.sh/uv/) — a fast Python package manager and project tool.

If your repository contains a `uv.lock` file, it means dependencies are already pinned and reproducible.

We'll use that to create an isolated environment.



---

## ✅ Prerequisites
- Python **3.8+** installed  
- Internet connection (for initial dependency resolution)  
- Access to a terminal or shell (PowerShell on Windows, bash/zsh on macOS or Linux)

---

## ⚙️ 1️⃣ Install `uv`

`uv` can be installed globally or used temporarily.  
Choose your operating system below:

### **🖥 macOS / Linux**
You can install via the installation script or with `pip`:

```bash
# Recommended fast install
curl -LsSf https://astral.sh/uv/install.sh | sh

# or using pip
pip install uv


Confirm installation:
```bash
uv --version
```

### 🪟 Windows Installation (PowerShell)

To install `uv` on Windows, open **PowerShell** and run either of the following commands:

```powershell
# Using PowerShell installer (recommended)
powershell -c "irm https://astral.sh/uv/install.ps1 | iex"

# Or install via pip
pip install uv


---

## 2️⃣ Create or Sync Environment from `uv.lock`
If your repository already includes a `uv.lock` file, you can create a virtual environment with all dependencies locked and reproducible.

```bash
uv sync
```

This command:
- Creates a `.venv/` folder (if it doesn't exist)
- Installs dependencies exactly as specified in `uv.lock`
- Uses the fastest available wheels and build cache


```

---

## 3️⃣ Activate the Environment
Once installed, activate the environment:

```bash
source .venv/bin/activate  # macOS / Linux
.venv\Scripts\activate    # Windows
```

If you are inside a Jupyter notebook, you can directly use the interpreter via:
```bash
uv run python
```

---

## 4️⃣ Running Your Code
You can execute any script or module from the environment using `uv run`.

Example:
```bash
uv run python main.py
```

Or launch Jupyter Notebook:
```bash
uv run jupyter notebook
```

---

## 5️⃣ Adding or Updating Dependencies
To add a new dependency:
```bash
uv add numpy
```


Then re-sync:
```bash
uv sync
```

---

## 6️⃣ Exporting Dependencies
To export your lock file for `pip` users:
```bash
uv export --format requirements.txt --output requirements.txt
```

---

## 🎯 Summary
- `uv` manages environment setup and dependency locking efficiently.  
- `uv sync` ensures reproducibility using `uv.lock`.  
- Use `uv run` to execute commands in the environment.

Now you can start developing or running your Quantum Computing Codes! 🚀
