# Python Development Environment Setup Guide

> This guide covers installing the Python interpreter, PyCharm IDE, and other commonly used Python development tools for Windows, macOS, and Linux.

---

## 1. Installing the Python Interpreter

Python is the foundation for running Python programs. It is recommended to install the latest stable version from the official source.

### Official Installation (Recommended)

Visit the official website to download: [https://www.python.org/downloads](https://www.python.org/downloads)

| Operating System | Download File | Notes |
|-----------------|---------------|-------|
| Windows | `Windows installer (64-bit)` | Check **"Add Python to PATH"** during installation |
| macOS | `macOS 64-bit universal2 installer` | Supports both Apple Silicon and Intel |
| Linux | Usually pre-installed | Install via package manager: `sudo apt install python3` |

### Verify Installation

Open a terminal (Command Prompt / Terminal) and run:

```bash
python --version
# or
python3 --version
```

If a version number is displayed (e.g., `Python 3.12.x`), the installation is successful.

---

## 2. Installing PyCharm

PyCharm is a professional Python IDE developed by JetBrains, available in two editions:

- **Community Edition**: Free and open-source, fully sufficient for learning and small projects
- **Professional Edition**: Paid, supports advanced features like web development, database tools, and scientific computing

> For learning purposes, the **Community Edition** is completely adequate.

### Download URL

[https://www.jetbrains.com/pycharm/download](https://www.jetbrains.com/pycharm/download)

### Installation Steps

#### Windows

1. Download the `.exe` installer
2. Double-click to run and choose the installation path
3. Check the following options:
   - [x] `64-bit launcher` (create desktop shortcut)
   - [x] `Add "Open Folder as Project"` (context menu)
   - [x] `Add to PATH` (add to environment variables)
   - [x] Associate `.py` files (optional)
4. Click `Install` and wait for completion
5. On first launch, choose **Do not import settings**
6. Select a theme (Darcula dark / Light), changeable later in settings

#### macOS

1. Download the `.dmg` installer
2. Double-click to mount and drag PyCharm to the `Applications` folder
3. Open from Launchpad on first launch
4. If prompted about an unidentified developer, go to **System Settings > Privacy & Security** and click Allow

#### Linux

1. Download the `.tar.gz` archive or the **Snap** / **Flatpak** version
2. For the archive:
   ```bash
   tar -xzf pycharm-community-*.tar.gz
   cd pycharm-*/bin
   ./pycharm.sh
   ```
3. Recommended: Install via Snap (auto-updates):
   ```bash
   sudo snap install pycharm-community --classic
   ```

### First-time Configuration

1. **Create New Project**: `File > New Project`
2. **Select Interpreter**: Use system Python or create a virtual environment (Virtualenv)
3. **New File**: Right-click project directory → `New > Python File`

### Common Shortcuts

| Function | Shortcut (Windows/Linux) | Shortcut (macOS) |
|----------|--------------------------|------------------|
| Run current file | `Ctrl + Shift + F10` | `Ctrl + Shift + R` |
| Debug run | `Shift + F9` | `Ctrl + D` |
| Code completion | `Ctrl + Space` | `Ctrl + Space` |
| Quick fix | `Alt + Enter` | `Option + Enter` |
| Format code | `Ctrl + Alt + L` | `Option + Cmd + L` |
| Find class/file | `Ctrl + N` | `Cmd + O` |
| Global search | `Ctrl + Shift + F` | `Cmd + Shift + F` |

---

## 3. Installing VS Code + Python Extension

VS Code is Microsoft's lightweight editor that becomes a powerful Python development environment with extensions.

### Download URL

[https://code.visualstudio.com/download](https://code.visualstudio.com/download)

### Installing the Python Extension

1. Open VS Code
2. Click the Extensions icon (four squares) on the left or press `Ctrl + Shift + X`
3. Search for `Python` and install the official **Microsoft** extension
4. Also install recommended extensions:
   - `Pylance` (Python language server, smart suggestions)
   - `Python Indent` (auto indentation)
   - `autoDocstring` (auto-generate docstrings)

### Configuring the Python Interpreter

1. Press `Ctrl + Shift + P` to open the Command Palette
2. Type `Python: Select Interpreter`
3. Choose the installed Python version

### Running Python Code

- Click the ▶ run button in the top-right corner
- Or press `Ctrl + F5` to run (without debugging)
- Press `F5` to debug

---

## 4. Installing Jupyter Notebook / JupyterLab

Jupyter is a powerful tool for data science and interactive learning, supporting running code line by line and viewing results instantly.

### Installation

```bash
# Install using pip
pip install notebook

# Or install the more feature-rich JupyterLab
pip install jupyterlab

# Or install Anaconda (comes with Jupyter, see next section)
```

### Launch

```bash
# Launch classic Notebook
jupyter notebook

# Launch JupyterLab
jupyter lab
```

The browser will automatically open `http://localhost:8888`.

### Common Operations

| Operation | Shortcut |
|-----------|----------|
| Run current cell | `Shift + Enter` |
| Add cell below/above | `B` / `A` |
| Delete cell | `D, D` (press D twice) |
| Toggle Markdown/Code | `M` / `Y` |
| Save | `Ctrl + S` |

---

## 5. Installing Anaconda / Miniconda

Anaconda is a data science-specific distribution pre-installed with hundreds of scientific computing libraries and Jupyter.

### Choose Your Version

| Version | Use Case | Size |
|---------|----------|------|
| **Anaconda** | Data science, machine learning beginners | ~3GB |
| **Miniconda** | Only need conda package manager, install libraries manually | ~100MB |

### Download URLs

- Anaconda: [https://www.anaconda.com/download](https://www.anaconda.com/download)
- Miniconda: [https://docs.conda.io/en/latest/miniconda.html](https://docs.conda.io/en/latest/miniconda.html)

### Common Commands After Installation

```bash
# Create a new environment
conda create -n myenv python=3.12

# Activate environment
conda activate myenv

# Install packages
conda install numpy pandas matplotlib

# List all environments
conda env list

# Remove environment
conda remove -n myenv --all
```

---

## 6. Other Recommended Tools

### Virtual Environment Management

```bash
# Using venv (built into Python)
python -m venv myenv

# Activate
myenv\Scripts\activate      # Windows
source myenv/bin/activate   # macOS/Linux

# Deactivate
deactivate
```

### Package Management Tools

| Tool | Features | Install Command |
|------|----------|-----------------|
| pip | Official Python package manager | Built-in |
| pipenv | Auto-manages virtual env and dependencies | `pip install pipenv` |
| poetry | Modern dependency management and packaging | `pip install poetry` |
| conda | Anaconda ecosystem package manager | Installed with Anaconda |

### Code Quality Tools

```bash
# Code formatter
pip install black
black your_script.py

# Linter (PEP8)
pip install flake8
flake8 your_script.py

# Type checker
pip install mypy
mypy your_script.py
```

### Version Control Tool: Git

Essential for Python development, used for code version management and collaboration.

**Download**: [https://git-scm.com/downloads](https://git-scm.com/downloads)

**Common Commands**:

```bash
git init                    # Initialize repository
git add .                   # Add files to staging area
git commit -m "message"     # Commit code
git push origin main        # Push to remote repository
```

---

## 7. Environment Setup Checklist

After installation, verify each item:

```bash
# 1. Python version
python --version

# 2. pip version
pip --version

# 3. Install a test package
pip install requests
python -c "import requests; print('requests OK')"

# 4. Git version
git --version

# 5. Editor can run and execute Python files
```

---

## 8. FAQ

### Q1: Windows says "python" is not recognized after installation?

You forgot to check **"Add Python to PATH"** during installation. Reinstall or manually add to environment variables:
- Right-click **This PC > Properties > Advanced system settings > Environment Variables**
- Add the Python installation path to `Path` (e.g., `C:\Users\Username\AppData\Local\Programs\Python\Python312`)

### Q2: PyCharm cannot find the installed Python?

`File > Settings > Project: xxx > Python Interpreter` → Click the gear icon → `Add...` → Select `System Interpreter` → Browse to the Python executable path.

### Q3: pip installation is too slow?

Switch to a domestic mirror:

```bash
# Temporary use
pip install numpy -i https://pypi.tuna.tsinghua.edu.cn/simple

# Permanent configuration
pip config set global.index-url https://pypi.tuna.tsinghua.edu.cn/simple
```

### Q4: PyCharm or VS Code, which one to choose?

| Scenario | Recommendation |
|----------|----------------|
| Pure Python learning, large projects | **PyCharm** |
| Multi-language development, lightweight | **VS Code** |
| Data science, interactive exploration | **Jupyter + VS Code** |

---

## Reference Links

- Python Official: [https://www.python.org](https://www.python.org)
- PyCharm Download: [https://www.jetbrains.com/pycharm/download](https://www.jetbrains.com/pycharm/download)
- VS Code Download: [https://code.visualstudio.com](https://code.visualstudio.com)
- Anaconda Download: [https://www.anaconda.com/download](https://www.anaconda.com/download)
- Git Download: [https://git-scm.com/downloads](https://git-scm.com/downloads)
