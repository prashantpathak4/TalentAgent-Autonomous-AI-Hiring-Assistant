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
                    │   Resume (PDF)   │
                    │   / DOCX File    │
                    └────────┬─────────┘
                             │
                             ▼
                    ┌──────────────────┐
                    │ Resume Processing│
                    │   & Extraction   │
                    └────────┬─────────┘
                             │
                             ▼
                  ┌──────────────────────┐
                  │   Screening Agent    │
                  │ Resume vs Job        │
                  │ Description Analysis │
                  └──────────┬───────────┘
                             │
                             ▼
                  ┌──────────────────────┐
                  │   Skill Gap Analysis │
                  │ Required vs Candidate│
                  │       Skills         │
                  └──────────┬───────────┘
                             │
                             ▼
                  ┌──────────────────────┐
                  │   Interview Agent    │
                  │ Personalized         │
                  │ Question Generation  │
                  └──────────┬───────────┘
                             │
                             ▼
                  ┌──────────────────────┐
                  │ Data Management Agent│
                  │ Candidate & Results  │
                  │      Storage         │
                  └──────────────────────┘
```

---

## 🤖 AI Agents

### 1. Screening Agent

Responsible for evaluating the candidate's resume against the job description.

**Responsibilities:**

* Resume analysis
* Job-description matching
* Candidate evaluation
* Initial screening

---

### 2. Interview Agent

Generates relevant interview questions based on the candidate's profile.

**Responsibilities:**

* Analyze identified skill gaps
* Generate technical questions
* Generate role-specific questions
* Create personalized interview preparation

---

### 3. Data Management Agent

Handles structured candidate information and recruitment results.

**Responsibilities:**

* Candidate information extraction
* Screening-result storage
* CSV generation
* Recruitment data organization

---

### 4. User Proxy Agent

Acts as the workflow coordinator and manages communication between the different agents.

```text
User Proxy Agent
       │
       ├──► Screening Agent
       │
       ├──► Interview Agent
       │
       └──► Data Management Agent
```

---

## 🛠️ Technology Stack

| Technology            | Purpose                            |
| --------------------- | ---------------------------------- |
| **Python**            | Core programming language          |
| **Microsoft AutoGen** | Multi-agent orchestration          |
| **GPT-4o-mini**       | LLM-based reasoning and evaluation |
| **spaCy**             | NLP and text processing            |
| **pdfplumber**        | PDF text extraction                |
| **docx2txt**          | DOCX text extraction               |
| **CSV**               | Candidate/result storage           |
| **python-dotenv**     | Environment configuration          |

---

## 📁 Project Structure

```text
IntelliHire/
│
├── assets/
│   ├── CV-English.pdf
│   └── job_description.txt
│
├── app.py
├── requirements.txt
├── .env
├── .gitignore
└── README.md
```

---

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone https://github.com/prashantpathak4/AI-Recruitment-Agent.git
cd AI-Recruitment-Agent
```

### 2. Create a virtual environment

```bash
python -m venv venv
```

Activate it:

**macOS / Linux**

```bash
source venv/bin/activate
```

**Windows**

```bash
venv\Scripts\activate
```

---

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

---

## 🔑 Environment Variables

Create a `.env` file in the project root:

```env
OPENAI_API_KEY=your_openai_api_key
```

Replace `your_openai_api_key` with your OpenAI API key.

**Never commit your `.env` file or API key to GitHub.**

---

## 📄 Add Resume & Job Description

Place the candidate's resume inside:

```text
assets/CV-English.pdf
```

Add the target job description to:

```text
assets/job_description.txt
```

The system will use these inputs to perform the recruitment analysis.

---

## ▶️ Run the Application

Run:

```bash
python app.py
```

The agents will process the resume and job description and execute the recruitment workflow.

---

## 🔄 Recruitment Workflow

```text
Resume
   │
   ▼
Resume Information Extraction
   │
   ▼
Job Description Analysis
   │
   ▼
Candidate Screening
   │
   ▼
Skill-Gap Identification
   │
   ▼
Interview Question Generation
   │
   ▼
Candidate Data Storage
```

---

## 💡 Example Use Case

A recruiter provides:

**Job Description**

```text
Looking for a Machine Learning Engineer with:
- Python
- TensorFlow
- PyTorch
- SQL
- Machine Learning
- MLOps
```

**Candidate Resume**

```text
Python
TensorFlow
Machine Learning
SQL
Docker
```

IntelliHire can identify the candidate's matching skills and potential gaps, then generate interview questions focused on areas relevant to the role.

---

## 🔮 Future Improvements

The system can be extended into a complete AI-powered Applicant Tracking System (ATS) with:

* 🌐 Web-based recruiter dashboard
* 🗄️ MongoDB/PostgreSQL candidate database
* 📊 AI-based candidate scoring
* 🔎 Semantic resume-job matching using embeddings
* 🧠 RAG-based candidate knowledge retrieval
* 🔗 GitHub profile analysis
* 📧 Automated candidate communication
* 📅 Interview scheduling
* 🔐 Recruiter authentication and authorization
* 📈 Recruitment analytics dashboard
* 🤖 Automated candidate shortlisting
* 🧩 Integration with existing ATS platforms

---

## 🎯 Project Objective

The goal of IntelliHire is to demonstrate how **LLMs and multi-agent systems can automate repetitive recruitment tasks** while providing recruiters with structured candidate insights and personalized interview preparation.

---

## 👨‍💻 Author

**Prashant Pathak**

GitHub: [prashantpathak4](https://github.com/prashantpathak4)

---

## ⭐ Acknowledgements

Built using:

* Microsoft AutoGen
* OpenAI APIs
* Python
* spaCy
* pdfplumber
* docx2txt

---

## 📜 License

This project is intended for educational and experimental purposes.
