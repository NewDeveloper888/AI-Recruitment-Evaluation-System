# AI Recruitment Evaluation System

An AI-powered recruitment automation workflow built with n8n that analyzes candidate resumes against job requirements using LLMs (OpenAI & Gemini), generates structured evaluation results, and stores the output automatically.

---

# Overview

This system automates the technical recruitment screening process by:

- Uploading a candidate CV
- Uploading a Job Description file
- Extracting text from both documents
- Comparing the candidate against the job requirements using AI
- Generating structured evaluation scores
- Saving the results into Google Sheets
- Sending recruiter notifications via Gmail

---

# Features

- AI-powered CV evaluation
- Job Description vs Resume comparison
- Semantic matching using LLMs
- Automated PDF text extraction
- Structured JSON evaluation output
- Risk & reward scoring
- Candidate fit rating
- Google Sheets integration
- Gmail notification support
- Fully automated n8n workflow

---

# Workflow Architecture

```text
Form Submission
      │
      ▼
Upload CV + Job Description
      │
      ▼
Google Drive Storage
      │
      ▼
PDF Text Extraction
      │
      ├── Resume Text
      └── Job Requirement Text
      │
      ▼
AI Evaluation Agent
      │
      ▼
Structured Information Extractor
      │
      ▼
Google Sheets Storage
      │
      ▼
Gmail Notification
```

---

# Technologies Used

| Technology | Purpose |
|---|---|
| n8n | Workflow orchestration |
| OpenAI Chat Model | AI candidate evaluation |
| Google Gemini Chat Model | Information extraction |
| Google Drive | File storage |
| PDF Extractor | Text extraction |
| Gmail | Notifications |
| Google Sheets | Data storage |

---

# AI Evaluation Logic

The AI agent compares:

- Candidate skills
- Experience level
- AI & automation background
- Technical stack
- Strengths & weaknesses
- Overall compatibility with the role

The system then generates:

- Risk Score
- Reward Score
- Overall Fit Rating
- Hiring justification

---

# System Prompt

The AI agent uses a strict structured-output prompt to ensure valid JSON responses.

Main constraints include:

- JSON-only output
- Fixed scoring values
- Integer fit rating
- No schema generation
- Consistent response structure

---

# Example Output

```json
{
  "Candidate_Name": "John Doe",
  "Candidate_Email": "john@example.com",
  "Candidate_Strengths": "Strong experience in Python and AI automation",
  "Candidate_Weaknesses": "Limited experience with vector databases",
  "Risk_Score": "Medium",
  "Risk_Explanation": "Requires onboarding for advanced AI infrastructure",
  "Reward_Score": "High",
  "Reward_Explanation": "Strong automation engineering background",
  "Reward_Fit": "Long-term",
  "Overall_Fit_Rating": 8,
  "Justification_for_Rating": "Matches most core technical requirements"
}
```

---

# Workflow Components

## 1. Form Submission

Receives:
- Candidate CV
- Job Description document

---

## 2. Google Drive Upload

Stores uploaded files for processing.

---

## 3. PDF Extraction

Extracts text content from:
- Resume PDF
- Job Description PDF

---

## 4. AI Agent

Analyzes the candidate against the job requirements.

Uses:
- OpenAI Chat Model

---

## 5. Information Extractor

Converts AI output into structured attributes.

Uses:
- Google Gemini Chat Model

---

## 6. Google Sheets

Stores evaluation results for recruiter review.

---

## 7. Gmail Notification

Sends candidate evaluation notifications.

---

# Folder Structure

```text
/Recruitment
    /CVs
    /JobDescriptions
    /Processed
```

---

# Use Cases

- Technical recruitment automation
- AI engineer screening
- Automation engineer hiring
- Resume filtering
- Candidate ranking
- HR workflow automation

---

# Future Improvements

- Vector database integration
- Embedding-based semantic search
- Multi-agent architecture
- PostgreSQL integration
- Recruiter dashboard
- Validation & retry layers

---

# Notes

- The workflow compares both the Job Description and the Candidate Resume.
- The system is designed for AI, automation, and software engineering roles.
- Output is generated in strict JSON format for easy downstream processing.

---

# Author

Mahmoud Yasser
