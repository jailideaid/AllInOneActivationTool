<p align="center">
<img width="300" alt="AllInOne Activation Tool" src="https://github.com/user-attachments/assets/3cf7f3af-8a77-449b-bc07-13f736978266" />
</p>

<h1 align="center">AllInOneActivationTool</h1>

A registry-based Windows & Microsoft Office license administration and activation management tool. Designed to operate without requiring WMI queries, utilizing Windows built-in management tools (`slmgr.vbs` and `ospp.vbs`).
Regarding the update, I am not placing it in the release location; instead, I will focus on the release location specifically for the update logs.
> [!TIP]
> **NEW UPDATE METHOD**
> **🚀 Fast One-Line Execution Available:** You can now run this tool directly using the standalone encrypted PowerShell command (`irm ... | iex`) without installing Python, or download the precompiled standalone executable (`main.exe`)!

---

**PLEASE READ THIS**

I can no longer make my code publicly available, as doing so would be a clear violation. I am now focused on restricting access to all of my code. Please refrain from attempting to breach or extract the source code of the tools I have created; doing so shows a lack of respect for me, the person who built them. A warning: please never misuse my tool, as it has repercussions for me; please use it wisely.

---

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
> **VERSION .PY**
<p align="center">
<img width="750" alt="Screenshot 2026-11-12 151009" src="https://github.com/user-attachments/assets/912955c7-c2a4-4673-b9f6-67766d552d44" />
</p>

> **VERSION .PS1**
<p align="center">
<img width="750" alt="Screenshot 2026-11-13 130401" src="https://github.com/user-attachments/assets/94c24807-2fa7-4d8a-b005-3c9c34718c2b" />
</p>

> **VERSION .EXE**
<p align="center">
<img width="750" alt="Screenshot 2026-11-13 130417" src="https://github.com/user-attachments/assets/e40bc63b-7e0b-4eac-a039-5b8f1b6518f5" />
</p>

---

## 📋 Prerequisites

1. **Operating System**: Windows 10 / 11 (32-bit / 64-bit).
2. **Internet Connection**: Required for connecting to KMS activation hosts.
3. **Privileges**: Administrator rights (the tool will automatically prompt for UAC elevation if not already running as Admin).

---

## 🚀 How to Run

Choose the method that best suits your workflow:

### 🔹 Method 1: One-Line PowerShell (Direct `irm | iex`) — *Most Convenient*
No file download or third-party software (Python/Git) required. Simply open **PowerShell as Administrator** and execute:

```powershell
irm https://raw.githubusercontent.com/jailideaid/AllInOneActivationTool/refs/heads/main/MainScript/main.ps1 | iex
```

> **Security Note**: This script is fully encrypted using **AES-256** and GZip. The payload is securely decrypted directly in RAM (*in-memory execution*) without ever writing raw unencrypted scripts to disk.

---

### 🔹 Method 2: Standalone Executable (`main.exe`) — *No CLI Needed*
1. Download **`main.exe`** from this repository's releases or files.
2. Double-click **`main.exe`**.
3. Click **Yes** on the User Account Control (UAC) prompt. The interactive menu will launch immediately.

---

### 🔹 Method 3: Manual Clone via Git (Local Execution)
If you prefer to clone and inspect the repository locally:

```powershell
git clone https://github.com/jailideaid/AllInOneActivationTool/
cd AllInOneActivationTool
```

Then run either:
- The compiled standalone executable:
  ```powershell
  .\main.exe
  ```
- Or the encrypted PowerShell script:
  ```powershell
  powershell -ExecutionPolicy Bypass -File .\main.ps1
  ```

---

## 📂 Repository Structure

```text
├── main.exe                 # Standalone compiled executable (AES-256 protected)
├── main.ps1       # Encrypted PowerShell script (One-line irm | iex compatible)
├── build_secure.ps1         # Security builder to compile & encrypt source
├── app.manifest             # Windows UAC elevation manifest
└── README.md
```

---

## ⚠️ Disclaimer

This utility is provided strictly for educational purposes, IT system administration, and internal testing environments. Use responsibly in accordance with local software license agreements.
I am currently focused on fixing bugs in this tool. If you encounter any troublesome bugs, please report them to my Gmail address: jailideaid@gmail.com
