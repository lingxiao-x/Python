# Python 开发环境搭建指南

> 本指南涵盖 Python 解释器安装、PyCharm IDE 以及其他常用 Python 编程工具的配置，适用于 Windows、macOS 和 Linux 系统。

---

## 一、安装 Python 解释器

Python 是运行 Python 程序的基础环境。推荐从官方渠道安装最新稳定版。

### 官方安装（推荐）

访问官网下载：[https://www.python.org/downloads](https://www.python.org/downloads)

| 操作系统 | 下载文件 | 注意事项 |
|---------|---------|---------|
| Windows | `Windows installer (64-bit)` | 安装时勾选 **"Add Python to PATH"** |
| macOS | `macOS 64-bit universal2 installer` | 支持 Apple Silicon 和 Intel |
| Linux | 通常已预装 Python | 可用包管理器安装 `sudo apt install python3` |

### 验证安装

打开终端（命令提示符 / Terminal），执行：

```bash
python --version
# 或
python3 --version
```

如果显示版本号（如 `Python 3.12.x`），说明安装成功。

---

## 二、安装 PyCharm

PyCharm 是 JetBrains 出品的专业 Python IDE，分为两个版本：

- **Community（社区版）**：免费开源，功能完全满足学习和小型项目开发
- **Professional（专业版）**：付费，支持 Web 开发、数据库工具、科学计算等高级功能

> 学习使用 **Community 版** 完全足够。

### 下载地址

[https://www.jetbrains.com/pycharm/download](https://www.jetbrains.com/pycharm/download)

### 安装步骤

#### Windows

1. 下载 `.exe` 安装包
2. 双击运行，选择安装路径
3. 勾选以下选项：
   - [x] `64-bit launcher`（创建桌面快捷方式）
   - [x] `Add "Open Folder as Project"`（右键菜单）
   - [x] `Add to PATH`（添加到环境变量）
   - [x] `.py` 文件关联（可选）
4. 点击 `Install`，等待完成
5. 首次启动选择 **Do not import settings**
6. 选择主题（Darcula 暗色 / Light 亮色），后续可在设置中更改

#### macOS

1. 下载 `.dmg` 安装包
2. 双击挂载，将 PyCharm 拖入 `Applications` 文件夹
3. 首次启动在 Launchpad 中打开
4. 如提示来自不明开发者，前往 **系统设置 > 隐私与安全性** 点击允许

#### Linux

1. 下载 `.tar.gz` 解压版 或 **Snap** / **Flatpak** 版本
2. 解压版：
   ```bash
   tar -xzf pycharm-community-*.tar.gz
   cd pycharm-*/bin
   ./pycharm.sh
   ```
3. 推荐通过 Snap 安装（自动更新）：
   ```bash
   sudo snap install pycharm-community --classic
   ```

### 首次配置

1. **创建新项目**：`File > New Project`
2. **选择解释器**：使用系统 Python 或创建虚拟环境（Virtualenv）
3. **新建文件**：右键项目目录 → `New > Python File`

### 常用快捷键

| 功能 | 快捷键（Windows/Linux） | 快捷键（macOS） |
|------|------------------------|----------------|
| 运行当前文件 | `Ctrl + Shift + F10` | `Ctrl + Shift + R` |
| 调试运行 | `Shift + F9` | `Ctrl + D` |
| 代码补全 | `Ctrl + Space` | `Ctrl + Space` |
| 快速修复 | `Alt + Enter` | `Option + Enter` |
| 格式化代码 | `Ctrl + Alt + L` | `Option + Cmd + L` |
| 查找类/文件 | `Ctrl + N` | `Cmd + O` |
| 全局搜索 | `Ctrl + Shift + F` | `Cmd + Shift + F` |

---

## 三、安装 VS Code + Python 插件

VS Code 是微软推出的轻量级编辑器，配合插件可成为强大的 Python 开发环境。

### 下载地址

[https://code.visualstudio.com/download](https://code.visualstudio.com/download)

### 安装 Python 扩展

1. 打开 VS Code
2. 点击左侧扩展图标（四个方块）或按 `Ctrl + Shift + X`
3. 搜索 `Python`，安装 **Microsoft** 官方发布的插件
4. 同时安装推荐插件：
   - `Pylance`（Python 语言服务器，智能提示）
   - `Python Indent`（自动缩进）
   - `autoDocstring`（自动生成文档字符串）

### 配置 Python 解释器

1. 按 `Ctrl + Shift + P` 打开命令面板
2. 输入 `Python: Select Interpreter`
3. 选择已安装的 Python 版本

### 运行 Python 代码

- 点击右上角 ▶ 运行按钮
- 或按 `Ctrl + F5` 运行（不调试）
- 按 `F5` 调试运行

---

## 四、安装 Jupyter Notebook / JupyterLab

Jupyter 是数据科学和交互式学习的利器，支持逐行运行代码并即时查看结果。

### 安装方式

```bash
# 使用 pip 安装
pip install notebook

# 或安装功能更全的 JupyterLab
pip install jupyterlab

# 或安装 Anaconda（自带 Jupyter，见下一节）
```

### 启动

```bash
# 启动经典 Notebook
jupyter notebook

# 启动 JupyterLab
jupyter lab
```

浏览器会自动打开 `http://localhost:8888`。

### 常用操作

| 操作 | 快捷键 |
|------|--------|
| 运行当前单元格 | `Shift + Enter` |
| 新增单元格 | `B`（下方）/ `A`（上方） |
| 删除单元格 | `D, D`（按两次 D） |
| 切换 Markdown/代码 | `M` / `Y` |
| 保存 | `Ctrl + S` |

---

## 五、安装 Anaconda / Miniconda

Anaconda 是数据科学专用发行版，预装了数百个科学计算库和 Jupyter。

### 选择版本

| 版本 | 适用场景 | 大小 |
|------|---------|------|
| **Anaconda** | 数据科学、机器学习初学者 | ~3GB |
| **Miniconda** | 只需要 conda 包管理，自行安装库 | ~100MB |

### 下载地址

- Anaconda：[https://www.anaconda.com/download](https://www.anaconda.com/download)
- Miniconda：[https://docs.conda.io/en/latest/miniconda.html](https://docs.conda.io/en/latest/miniconda.html)

### 安装后常用命令

```bash
# 创建新环境
conda create -n myenv python=3.12

# 激活环境
conda activate myenv

# 安装包
conda install numpy pandas matplotlib

# 查看所有环境
conda env list

# 删除环境
conda remove -n myenv --all
```

---

## 六、其他推荐工具

### 虚拟环境管理

```bash
# 使用 venv（Python 内置）
python -m venv myenv

# 激活
myenv\Scripts\activate      # Windows
source myenv/bin/activate   # macOS/Linux

# 退出
deactivate
```

### 包管理工具

| 工具 | 特点 | 安装命令 |
|------|------|---------|
| pip | Python 官方包管理 | 已内置 |
| pipenv | 自动管理虚拟环境和依赖 | `pip install pipenv` |
| poetry | 现代化依赖管理和打包 | `pip install poetry` |
| conda | Anaconda 生态包管理 | 随 Anaconda 安装 |

### 代码质量工具

```bash
# 代码格式化
pip install black
black your_script.py

# 代码检查（PEP8）
pip install flake8
flake8 your_script.py

# 类型检查
pip install mypy
mypy your_script.py
```

### 版本控制工具：Git

Python 开发必备，用于代码版本管理和协作。

**下载**： [https://git-scm.com/downloads](https://git-scm.com/downloads)

**常用命令**：

```bash
git init                    # 初始化仓库
git add .                   # 添加文件到暂存区
git commit -m "提交说明"     # 提交代码
git push origin main        # 推送到远程仓库
```

---

## 七、环境配置检查清单

安装完成后，建议逐项验证：

```bash
# 1. Python 版本
python --version

# 2. pip 版本
pip --version

# 3. 安装测试包
pip install requests
python -c "import requests; print('requests OK')"

# 4. Git 版本
git --version

# 5. 编辑器能否正常运行并执行 Python 文件
```

---

## 八、常见问题

### Q1：Windows 安装 Python 后命令行提示找不到 python？

安装时忘记勾选 **"Add Python to PATH"**。重新安装或手动添加环境变量：
- 右键 **此电脑 > 属性 > 高级系统设置 > 环境变量**
- 在 `Path` 中添加 Python 安装路径（如 `C:\Users\用户名\AppData\Local\Programs\Python\Python312`）

### Q2：PyCharm 无法识别已安装的 Python？

`File > Settings > Project: xxx > Python Interpreter` → 点击齿轮图标 → `Add...` → 选择 `System Interpreter` → 浏览到 Python 可执行文件路径。

### Q3：pip 安装包速度慢？

切换国内镜像源：

```bash
# 临时使用
pip install numpy -i https://pypi.tuna.tsinghua.edu.cn/simple

# 永久配置
pip config set global.index-url https://pypi.tuna.tsinghua.edu.cn/simple
```

### Q4：PyCharm 和 VS Code 选哪个？

| 场景 | 推荐 |
|------|------|
| 纯 Python 学习、大型项目 | **PyCharm** |
| 多语言开发、轻量快速 | **VS Code** |
| 数据科学、交互式探索 | **Jupyter + VS Code** |

---

## 参考链接

- Python 官方：[https://www.python.org](https://www.python.org)
- PyCharm 下载：[https://www.jetbrains.com/pycharm/download](https://www.jetbrains.com/pycharm/download)
- VS Code 下载：[https://code.visualstudio.com](https://code.visualstudio.com)
- Anaconda 下载：[https://www.anaconda.com/download](https://www.anaconda.com/download)
- Git 下载：[https://git-scm.com/downloads](https://git-scm.com/downloads)
