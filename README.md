# ComfyUI-ROCm-Install-Guide (AMD 6xxx Series on Windows)
This document provides a structured installation guide for ComfyUI utilizing the ROCm framework and ZLUDA translation layer on Windows for AMD 6xxx series GPUs.

---

## 🇬🇧 English Version

### I. Easy Installation (Prerequisites)

| No. | Link | Title | Action/Remark |
| :---: | :---: | :--- | :--- |
| 1. | https://aka.ms/vs/17/release/vc_redist.x64.exe | **Visual C++ Runtime** | Install the executable. |
| 2. | https://git-scm.com/install/windows | **Git** | Ensure Git is installed. |
| 3. | https://strawberryperl.com/ | **Strawberry Perl** | Ensure Strawberry Perl is installed. |
| 4. | https://www.amd.com/en/developer/resources/rocm-hub/hip-sdk.html | **HIP SDK 6.4.2** | Install the specific version. |

---

### II. Medium Installation (Core Tools & Environment)

| No. | Link | Title | Action/Remark |
| :---: | :---: | :--- | :--- |
| 1. | https://aka.ms/vs/17/release/vs_BuildTools.exe | **Visual Studio Build Tools** | Tick **"Desktop development with C++"** during installation. |
| 2. | (Python Website) | **Python 3.11.9** | **⚠️ Crucially, ensure you tick "Add Python to PATH"** during installation. |

---

### III. Hard Configuration (ZLUDA & Patching)

| No. | Link | Title | Action/Remark |
| :---: | :---: | :--- | :--- |
| 1. | (System Settings) | **HIP\_PATH Environment Variable** | Add/set system variables **HIP_PATH** and **HIP_PATH64**. |
| 2. | (System Settings) | **Python PATH Optimization** | Move the Python 3.11 path to the **top** of the system 'Path' variable list. |
| 3. | https://github.com/likelovewant/ROCmLibs-for-gfx1103-AMD780M-APU/releases/ | **ROCm Library Replacement** | Download files and **replace the roblas binary files**. |
| 4. | https://github.com/lshqqytiger/ZLUDA/releases/download/LATEST_TAG/ZLUDA-windows-rocm6-amd64.zip | **ZLUDA Main Program** | **ACTION**: Copy the download link for the latest `zluda.zip`. (Replace `LATEST_TAG` with the actual release tag, e.g., `rel.d60bddbc870827566b3d2d417e00e1d2d8acc026`). |
| 5. | (CMD Command) | **ComfyUI-Zluda Clone** | Run: `git clone https://github.com/patientx/ComfyUI-Zluda` |
| 6. | (CMD Command) | **Execute Patch and Launch** | **a.** Run `patch zluda 2` then **paste the Zluda zip link**. **b.** Run `run comfyui`. |

---
---

## 🇨🇳 简体中文版本

### I. 简易安装 (Easy) - 下载即安装

| 序号 | 链接 | 标题 | 操作/备注 |
| :---: | :---: | :--- | :--- |
| 1. | https://aka.ms/vs/17/release/vc_redist.x64.exe | **Visual C++ 运行时** | 安装此可执行文件。 |
| 2. | https://git-scm.com/install/windows | **Git** | 确保已安装 Git。 |
| 3. | https://strawberryperl.com/ | **Strawberry Perl** | 确保已安装 Strawberry Perl。 |
| 4. | https://www.amd.com/en/developer/resources/rocm-hub/hip-sdk.html | **HIP SDK 6.4.2** | 安装特定版本。 |

---

### II. 中等难度安装 (Medium) - 工具和特定版本

| 序号 | 链接 | 标题 | 操作/备注 |
| :---: | :---: | :--- | :--- |
| 1. | https://aka.ms/vs/17/release/vs_BuildTools.exe | **Visual Studio Build Tools** | 勾选 **"Desktop development with C++"** (使用 C++ 的桌面开发)。其他默认。 |
| 2. | (Python 网站) | **Python 3.11.9** | **⚠️ 关键：确保安装时勾选 "Add Python to PATH"** (将 Python 添加到 PATH)。 |

---

### III. 复杂配置 (Hard) - 高级设置和补丁

| 序号 | 链接 | 标题 | 操作/备注 |
| :---: | :---: | :--- | :--- |
| 1. | (系统设置) | **HIP\_PATH 环境变量** | 添加/设置系统变量 **HIP_PATH** 和 **HIP_PATH64**。 |
| 2. | (系统设置) | **Python PATH 优化** | 将 Python 3.11 的路径移动到系统 'Path' 变量列表的**最上方**。 |
| 3. | https://github.com/likelovewant/ROCmLibs-for-gfx1103-AMD780M-APU/releases/ | **ROCm 库替换** | 下载文件并**替换 roblas 二进制文件**。 |
| 4. | https://github.com/lshqqytiger/ZLUDA/releases/download/LATEST_TAG/ZLUDA-windows-rocm6-amd64.zip | **ZLUDA 主程序** | **操作**: 复制最新 `zluda.zip` 文件的下载链接 (替换 `LATEST_TAG` 为实际版本号，例如 `rel.d60bddbc870827566b3d2d417e00e1d2d8acc026`)。 |
| 5. | (CMD 命令) | **ComfyUI-Zluda 克隆** | 运行: `git clone https://github.com/patientx/ComfyUI-Zluda` |
| 6. | (CMD 命令) | **执行补丁和启动** | **a.** 运行 `patch zluda 2` **并粘贴 Zluda zip 链接**。 **b.** 运行 `run comfyui`。 |

---
This guide should serve perfectly as a **`README.md`** file. The steps for the advanced configuration are detailed in the video [Zluda on Windows with AMD RX6900XT | Complete Guide with HIP SDK, Strawberry Perl, Miniconda, Python](https://www.youtube.com/watch?v=XG2vROmaXto), which provides a full walkthrough for setting up ZLUDA and HIP SDK on AMD GPUs.


http://googleusercontent.com/youtube_content/1
