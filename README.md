# financial-document-analyzer
# 📊 Financial Document Analyzer (CrewAI Based System)

## 📌 Project Overview

The Financial Document Analyzer is an AI-powered system that processes corporate financial reports, earnings statements, and investment documents using CrewAI agents.

The system extracts insights, summarizes financial data, and generates structured analysis outputs.

This project was debugged, optimized, and improved to ensure stable execution and clean architecture.

---

# 🐞 Bugs Identified & Fixes Applied

### 1️⃣ Large File Push Error (GitHub 100MB limit)
**Issue:**
The `venv/` folder was accidentally committed, causing:
File size exceeded 100MB limit.

**Fix:**
- Removed `venv` from Git tracking
- Deleted Git history
- Added `.gitignore`
- Reinitialized repository

---

### 2️⃣ Missing Dependencies Error
**Issue:**
Application crashed due to missing packages.

**Fix:**
- Generated `requirements.txt` using:
  pip freeze > requirements.txt
- Ensured all required libraries are listed

---

### 3️⃣ Environment Configuration Issues
**Issue:**
API keys not detected properly.

**Fix:**
- Added `.env` support
- Used environment variables securely

---

# 🏗️ System Architecture

User Input → CrewAI Agents → Document Processing → Analysis Engine → Output Generation

Core Components:
- Agent Manager (CrewAI)
- Document Parser
- Analysis Engine
- Vector Storage (LanceDB)
- Output Generator

---

# ⚙️ Setup Instructions

## 1️⃣ Clone Repository
