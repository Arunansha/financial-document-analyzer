# 📊 Financial Document Analyzer

## 📌 Project Overview

The Financial Document Analyzer is an AI-powered system that processes corporate financial reports, earnings statements, and investment documents using CrewAI agents.

The system extracts key financial insights, summarizes company performance, identifies risks, and generates structured analysis results.

This submission includes fixed, working code with debugging improvements, structured setup instructions, and API documentation.

---

# 🐞 Bugs Found & Fixes Applied

## 1️⃣ Large File Upload Error (GitHub 100MB Limit)

**Issue:**  
The `venv/` folder was accidentally committed, which included a large file:
`lancedb/_lancedb.pyd (147MB)`  
This exceeded GitHub’s 100MB file size limit.

**Fix:**  
- Removed `venv/` from Git tracking  
- Added `.gitignore` to prevent future tracking  
- Cleaned Git history  
- Reinitialized repository  
- Pushed clean working code  

---

## 2️⃣ Missing Dependencies Issue

**Issue:**  
Application failed due to missing required packages.

**Fix:**  
- Generated `requirements.txt` using:
- Ensured all required libraries are properly listed

---

## 3️⃣ Environment Variable Configuration Error

**Issue:**  
API key was not properly loaded, causing runtime errors.

**Fix:**  
- Added `.env` configuration support  
- Loaded environment variables securely  
- Removed hardcoded keys  

---

# 🏗️ System Architecture

User Input  
⬇  
CrewAI Agents  
⬇  
Document Processing  
⬇  
Analysis Engine  
⬇  
Structured Output (JSON / Text Summary)

### Core Components:
- CrewAI Agent Manager
- Financial Analysis Agent
- Risk Assessment Agent
- Summary Generator Agent
- Vector Storage (LanceDB)

---

# ⚙️ Setup Instructions

## 1️⃣ Clone Repository

## 2️⃣ Create Virtual Environment

## 3️⃣ Activate Virtual Environment

Windows:
Mac/Linux:

## 4️⃣ Install Dependencies

## 5️⃣ Configure Environment Variables

Create a `.env` file in the root directory:

---

# ▶️ Usage

Run the application:

Upload or provide a financial document for analysis.

The system will:
- Extract key metrics
- Generate financial summary
- Identify potential risks
- Provide structured output

---

# 📡 API Documentation

## Endpoint: Analyze Financial Document

**Method:** POST  
**Input:** Financial document (PDF/Text)  
**Output:** JSON response  

### Sample Response:

```json
{
  "summary": "Revenue increased by 12% compared to last quarter.",
  "risks": ["Rising operational costs"],
  "recommendation": "Moderate investment potential"
}
