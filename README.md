# IGotU 🛡️

> A lightweight Python antimalware scanner – “I Got You” has your back.

![License](https://img.shields.io/badge/license-Apache%202.0-blue.svg)  
![Python](https://img.shields.io/badge/python-3.6%2B-blue.svg)  
![CI](https://github.com/sampolmx/IGotU/actions/workflows/ci.yml/badge.svg)  

---

## 📖 Overview

**IGotU** is a simple, command-line antimalware tool written in Python.  
Scan files or entire directories for known malware signatures, quarantine infected items, and generate quick reports—all without heavy dependencies.  

---

## 🚀 Features

- 🔍 **File & Directory Scanning**: Target individual files or recurse through folders  
- 🛑 **Signature-Based Detection**: Works out of the box with built-in rules (YARA support planned)  
- 🗄️ **Quarantine Mode**: Move infected files to a safe directory  
- 📋 **Reporting**: Summary output in console and optional log file  
- ⚙️ **Configurable**: Command-line flags for scan depth, verbosity, and quarantine path  

---

## 🛠️ Requirements

- Python **3.6** or higher :contentReference[oaicite:0]{index=0}  
- *(Optional)* Virtual environment tool (venv, virtualenv)  

---

## 📦 Installation

```bash
# Clone the repo
git clone https://github.com/sampolmx/IGotU.git
cd IGotU

# (Optional) create & activate virtualenv
python3 -m venv .venv
source .venv/bin/activate

# Install dependencies (if any)
pip install -r requirements.txt

----
# Show help & available options
python Antimalware.py --help

# Scan a single file
python Antimalware.py --scan /path/to/suspicious.exe

# Scan a directory (recursive)
python Antimalware.py --scan /home/user/downloads

# Scan + quarantine infected files
python Antimalware.py --scan /path/to/dir --quarantine ./quarantine
---
IGotU/
├── .github/               # CI workflows & actions
│   └── workflows/
├── Antimalware.py         # Main antimalware scanner script
├── LICENSE                # Apache 2.0 license :contentReference[oaicite:1]{index=1}
└── README.md              # This document
