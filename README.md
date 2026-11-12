# AllInOneActivationTool

A registry-based Windows & Microsoft Office license administration and activation management script. Designed to operate without requiring WMI queries, utilizing Windows built-in management tools (`slmgr.vbs` and `ospp.vbs`).

> [!TIP]
> **🚀 Coming Soon:** A dedicated standalone PowerShell execution mode (`.ps1`) is currently under development to enable one-line execution directly via `irm ... | iex` without requiring Python to be installed!

---

**PLEASE READ THIS**

I can no longer make my code publicly available, as doing so would be a clear violation. I am now focused on restricting access to all of my code. Please refrain from attempting to breach or extract the source code of the tools I have created; doing so shows a lack of respect for me, the person who built them. A warning: please never misuse my tool, as it has repercussions for me; please use it wisely.

----
## 📌 Features & Menu Options

When launched with elevated Administrator privileges, the tool auto-detects the current Windows edition and displays an interactive menu:

| Option | Name | Description | Supported Editions / Targets |
| :---: | :--- | :--- | :--- |
| **1** | **Activate Windows 10** | Configures KMS setup and activates Windows 10 installations. | Home, Pro, Enterprise, Education, Single Language, etc. |
| **2** | **Activate Windows 11** | Configures KMS setup and activates Windows 11 installations. | Home, Pro, Enterprise, Education, SE, etc. |
| **3** | **Activate Microsoft Office 365** | Installs Volume License (VL) certificates and activates Office 365. | ProPlus VL suite with dedicated KMS hosts. |
| **4** | **Activate Microsoft Office 2021** | Installs Volume License (VL) certificates and activates Office 2021. | Standard & Professional Plus 2021. |
| **5** | **Activate Microsoft Office 2019** | Converts retail/MAK licenses to VL and activates Office 2019. | Standard & Professional Plus 2019. |
| **6** | **Activate Microsoft Office 2016** | Converts retail/MAK licenses to VL and activates Office 2016. | Standard & Professional Plus 2016. |
| **7** | **Activate Microsoft Visio** | Auto-detects installed Visio version and applies proper VL KMS license. | Visio 2016, 2019, 2021, and Visio 365. |
| **0** | **Exit** | Safely exits the tool. | - |

---

<p align="center">
<img width="750" alt="Screenshot 2026-11-12 151009" src="https://github.com/user-attachments/assets/912955c7-c2a4-4673-b9f6-67766d552d44" />
</p>

---

## 📋 Prerequisites

1. **Operating System**: Windows 10 / 11 (32-bit / 64-bit).
2. **Python**: Python 3.10+ installed on the system.
3. **Privileges**: Administrator rights (the script will automatically prompt for UAC elevation if not already running as Admin).

---

## 🚀 Installation & Usage

### 1. Clone the Repository
Open **PowerShell** or **Command Prompt** and run:

```bash
git clone https://github.com/jailideaid/AllInOneActivationTool/
cd AllInOneActivationTool
```

---

### 2. Run the Script

Run the main file:

```bash
python main.py
```

Follow the on-screen numbered prompts by selecting `1` through `7` according to your target activation.

---

## 📂 Repository Structure

```text
├── main.py                  # Obfuscated execution script
├── pyarmor_runtime_000000/  # Required binary runtime module
│   ├── pyarmor_runtime.pyd
│   └── __init__.py
├── .gitignore
└── README.md
```

> [!IMPORTANT]
> The `pyarmor_runtime_000000` directory must always be kept alongside `main.py` in the root repository. Do not delete or rename it.

---

## ⚠️ Disclaimer

This utility is provided strictly for educational purposes, IT system administration, and internal testing environments. Use responsibly in accordance with local software license agreements.
I am currently focused on fixing bugs in this tool. If you encounter any troublesome bugs, please report them to my Gmail address: jailideaid@gmail.com
