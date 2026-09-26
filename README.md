# 🤖 IntelliHire — Multi-Agent AI Recruitment & Candidate Assessment System

IntelliHire is a **multi-agent AI-powered recruitment system** designed to automate key stages of the hiring process — from resume screening and candidate evaluation to skill-gap analysis and personalized interview-question generation.

The system uses **Microsoft AutoGen** to coordinate specialized AI agents and **GPT-4o-mini** to analyze candidate profiles against job requirements.

---

## 🚀 Key Features

* 📄 **Automated Resume Parsing**

  * Extracts candidate information from PDF and DOCX resumes.
  * Identifies education, experience, skills, and other relevant information.

* 🔍 **AI-Powered Resume Screening**

  * Compares candidate resumes against a provided job description.
  * Performs initial keyword-based matching.
  * Uses an LLM for contextual candidate evaluation.

* 🧠 **Skill-Gap Analysis**

  * Identifies skills required by the job description.
  * Detects missing or insufficient skills in the candidate profile.

* 💬 **AI Interview Question Generation**

  * Generates interview questions based on the candidate's skills and identified gaps.
  * Questions can be tailored to the requirements of the target role.

* 🤝 **Multi-Agent Architecture**

  * Uses specialized AI agents for different recruitment tasks.
  * Agents collaborate to complete the recruitment workflow.

* 📊 **Candidate Data Management**

  * Stores candidate information and screening results.
  * Supports structured CSV-based output for further analysis.

---

## 🏗️ System Architecture

```text
                    ┌──────────────────┐
```
