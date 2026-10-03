
An AI-powered automation system that researches a prospect's company website and generates a personalized cold-email opening line based on verified company information.

---

## 👥 Team Members

- O. Divya
- N. Lalitha
- N. SasiRupaka
- N. DhanaLakshmi

**Team Number:** 19

---

## 📌 Project Overview

Cold Email Personalizer is an AI-based automation project designed to reduce the manual effort involved in researching companies before sending cold emails.

The system takes a company name, website URL, prospect name, and sales representative details as input. It then accesses the company website, extracts useful website information, cleans the content, analyzes it using AI, and generates a short personalized icebreaker.

The generated content is sent for human review before it is used in an email.

### Main Idea

**Company Website → Web Crawling → Content Extraction → Data Cleaning → AI Analysis → Personalized Icebreaker → Human Review**

---

## 🎯 Aim of the Project

The main objectives of this project are:

- Analyze a target company's website.
- Identify useful and recent company information.
- Find achievements, product launches, awards, partnerships, expansion, and important announcements.
- Generate a natural 1–2 sentence cold-email opening line.
- Reduce manual company research.
- Improve personalization in sales outreach.
- Use verified website information instead of inventing company facts.
- Keep a human-review step before sending the final email.

---

## ❓ Problem Statement

Sales representatives often spend significant time researching a prospect's company before writing personalized cold emails.

Manual research can be:

- Time-consuming
- Repetitive
- Difficult to scale
- Inconsistent across different prospects

Our project automates the research and personalization process.

---

## 💡 Proposed Solution

The system automatically processes a company's website and uses AI to identify useful company information.

It then converts the verified information into a short and natural cold-email opening line.

### Example

**Company:** ABC Technologies

**Recent Update:**  
Launched an AI-powered logistics platform.

**Generated Icebreaker:**

> I noticed ABC Technologies recently launched its AI-powered logistics platform — exciting to see your team expanding into intelligent logistics.

The sales representative can review the generated content before using it.

---

# ⚙️ Implementation Process

The complete process consists of the following stages:

### 1. Company Input

The user provides:

- Company name
- Company website URL
- Prospect name
- Sales representative name

### 2. Crawl Website

The workflow accesses the specified company website using an HTTP Request.

### 3. Extract Website Content

Relevant HTML content is extracted from the website.

### 4. Clean Website Text

Unnecessary HTML tags, scripts, styles, and extra spaces are removed.

The cleaned content is prepared for AI processing.

### 5. AI Company Analysis

The AI analyzes the website information and looks for:

- Recent company achievements
- New product launches
- Awards
- Partnerships
- Expansion
- Important announcements

The AI is instructed to use only information supported by the website content.

### 6. Generate Icebreaker

The AI converts the verified company information into a natural 1–2 sentence cold-email opening.

### 7. Final Output

The system prepares the final information including:

- Company name
- Recent update
- Personalized icebreaker
- Supporting information/source

### 8. Human Review

The generated content is sent for human review.

The sales representative can verify the information before using it in an email.

---

# 🏗️ System Architecture

```text
                ┌──────────────────────┐
                │      Sales Rep       │
                └──────────┬───────────┘
                           │
                           ▼
                ┌──────────────────────┐
                │   Company Details    │
                │ Name / URL / Prospect│
                └──────────┬───────────┘
                           │
                           ▼
                ┌──────────────────────┐
                │    Crawl Website     │
                │    HTTP Request      │
                └──────────┬───────────┘
                           │
                           ▼
                ┌──────────────────────┐
                │ Extract Web Content  │
                │      HTML Data       │
                └──────────┬───────────┘
                           │
                           ▼
                ┌──────────────────────┐
                │  Clean Website Text  │
                │ Remove HTML / Noise  │
                └──────────┬───────────┘
                           │
                           ▼
                ┌──────────────────────┐
                │  AI Company Analysis │
                │  Identify Key Facts  │
                └──────────┬───────────┘
                           │
                           ▼
                ┌──────────────────────┐
                │ Generate Icebreaker  │
                │ Personalized Opening │
                └──────────┬───────────┘
                           │
                           ▼
                ┌──────────────────────┐
                │     Final Output     │
                └──────────┬───────────┘
                           │
                           ▼
                ┌──────────────────────┐
                │    Human Review      │
                │   Verify & Approve   │
                └──────────┬───────────┘
                           │
                           ▼
                    Cold Email Use


---

🔄 n8n Workflow

The project workflow is implemented using n8n.

Workflow sequence

When clicking "Execute workflow"
                ↓
        Company Details
                ↓
         Crawl Website
                ↓
   Extract Website Content
                ↓
      Clean Website Text
                ↓
      AI Company Analysis
                ↓
       Generate Icebreaker
                ↓
          Final Output
                ↓
         Human Review
                ↓
           Email Use


---

🛠️ Technologies Used

Technology	Purpose

n8n	Workflow automation
AI / LLM	Company analysis and icebreaker generation
OpenAI GPT model	AI-based content processing
HTTP Request	Website crawling
HTML Extraction	Extract website content
JavaScript	Clean and process website text
Gmail	Human-review notification
GitHub	Project version control and documentation



---

🤖 AI Processing

The AI performs two important tasks.

1. Company Analysis

The AI examines the extracted website information and identifies useful information such as:

Recent achievements

Product launches

Awards

Partnerships

Expansion

Important announcements


The AI is instructed to avoid unsupported claims.

If reliable recent information is not available, the workflow can return:

No reliable recent information found.


---

2. Icebreaker Generation

After company analysis, the AI creates one natural 1–2 sentence cold-email opening.

Rules used

Use only verified information.

Do not invent achievements.

Do not exaggerate.

Keep the language professional.

Keep the opening short and natural.



---

📥 Input

The workflow accepts information such as:

Company Name: ABC Technologies
Website URL: https://example.com
Prospect Name: Ram
Sales Representative: Lalitha


---

📤 Output

The final output can contain:

Company Name:
ABC Technologies

Recent Update:
Launched an AI-powered logistics platform

Personalized Icebreaker:
I noticed ABC Technologies recently launched its AI-powered
logistics platform — exciting to see your team expanding
into intelligent logistics.


---

📧 Human Review

Human review is an important part of the system.

Before the generated content is used:

1. The AI generates the personalized opening.


2. The result is sent for review.


3. The sales representative checks the information.


4. The representative can verify whether the statement is accurate.


5. The approved content can then be used in the cold email.



This helps reduce the risk of inaccurate personalization.


---

🛡️ Reliability and Safe Fallback

The system follows these principles:

No invented information

The AI should only use information supported by the website content.

No reliable information

If useful recent information cannot be found, the system can return:

No reliable recent information found.

Human verification

Generated content should be reviewed before being used.

Source verification

The source website should be retained so the sales representative can verify the information.


---

🚀 How to Use the Workflow

Step 1 – Import the Workflow

Open n8n and import:

My workflow 5 (2).json

Step 2 – Configure Credentials

Configure the required AI and Gmail credentials in n8n.

Step 3 – Enter Company Details

Update the company information in the Company Details node.

Example:

Company Name: ABC Technologies
Website URL: https://example.com
Prospect Name: Ram
Sales Representative: Lalitha

Step 4 – Execute the Workflow

Click:

Execute Workflow

Step 5 – Website Processing

The workflow:

Crawls Website
      ↓
Extracts Content
      ↓
Cleans Text

Step 6 – AI Processing

The AI analyzes the cleaned content and identifies useful company information.

Step 7 – Generate Icebreaker

The AI generates a personalized opening line.

Step 8 – Human Review

Review the generated result before using it in a real email.


---

📁 Repository Structure

Cold-Email-Personalizer/
│
├── README.md
│
├── My workflow 5 (2).json
│
├── Cold_Email_Personalizer_Team_19.pptx
│
└── other project files


---

📄 Project Files

README.md

Contains the complete project documentation.

My workflow 5 (2).json

Contains the n8n workflow used for the project.

Cold_Email_Personalizer_Team_19.pptx

Contains the project presentation, including:

Project aim

Implementation process

Implementation structure

Technology stack

Real-time implementation

System flow

Reliability and fallback

Expected output

Project conclusion



---

🌟 Key Features

🌐 Website-based company research

🤖 AI-powered company analysis

✉️ Personalized cold-email icebreakers

⚙️ Automated workflow using n8n

🧹 Website content cleaning

🔍 Recent company information identification

🛡️ Verified-information approach

👤 Human review before email use

📧 Gmail-based review notification

📂 GitHub-based project documentation



---

🎯 Benefits

Reduces manual research time.

Makes sales emails more personalized.

Automates repetitive research tasks.

Helps sales representatives research prospects quickly.

Provides a consistent workflow.

Keeps a human verification step.

Reduces the risk of unsupported claims.



---

🔮 Future Enhancements

Future versions can include:

Crawl multiple pages automatically.

Support multiple company URLs at once.

Add CSV/Excel input for bulk prospects.

Generate complete personalized cold emails.

Add email scheduling.

Add CRM integration.

Store previous research results.

Add a Streamlit web interface.

Improve source detection and verification.

Add support for multiple languages.

Add analytics for email personalization.



---

⚠️ Limitations

The system may have limitations when:

A website blocks automated requests.

Website content is dynamically loaded.

Important information is not available publicly.

Website pages have complex structures.

The extracted content is incomplete.

AI-generated text requires human verification.


Therefore, generated content should be reviewed before sending.


---

📊 Expected System Flow

Input Company
      ↓
Company Website
      ↓
Website Crawling
      ↓
Content Extraction
      ↓
Text Cleaning
      ↓
AI Company Analysis
      ↓
Recent Company Information
      ↓
Icebreaker Generation
      ↓
Final Output
      ↓
Human Review
      ↓
Cold Email


---

🏆 Project Outcome

The project demonstrates how AI and workflow automation can be combined to automate company research and cold-email personalization.

Instead of manually researching every prospect, the system processes website information and converts relevant company updates into personalized opening lines.

Core principle:

Verified Information → AI Personalization → Human Review → Email


---

👩‍💻 Team

Team Number – 19

Name

O. Divya
N. Lalitha
N. SasiRupaka
N. DhanaLakshmi



---

📌 Conclusion

The Cold Email Personalizer from Prospect Websites project provides an automated approach to personalized sales outreach.

By combining website crawling, content extraction, AI analysis, and human review, the system helps transform publicly available company information into relevant cold-email opening lines.

The goal is to make prospect research faster, more consistent, and more personalized while keeping human verification in the process.


---

⭐ Thank You

Cold Email Personalizer – Team 19

### One important thing before you commit

Your uploaded n8n JSON contains **credential/configuration information**. Before making the GitHub repository public, check that the JSON does **not contain any actual API keys, passwords, OAuth tokens, or other secrets**. If it does, remove/replace those secrets before keeping the repository public.

Your PPT and workflow files are already uploaded to the GitHub repository, so after updating `README.md`, your repository will have the main documentation + presentation + n8n workflow together. 2 3
