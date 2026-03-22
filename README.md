# 🤖 AI-Powered Job Application Tracker

An automated job application tracking system 
built with n8n, Gemini AI, Notion, and Gmail.

## 🚀 What It Does

Every time you apply to a job, just fill a 
Google Form. Then automatically:

- Gemini AI reads and summarizes the JD
- Scores your fit out of 10
- Saves everything to a Notion database
- Sends a confirmation email instantly

## 🛠️ Tech Stack

- **n8n** — workflow automation
- **Google Forms + Sheets** — data capture
- **Gemini API** — AI analysis
- **Notion API** — application dashboard
- **Gmail API** — email notifications
- **Google Cloud OAuth2** — authentication

## ⚙️ Workflow Architecture
```
Google Form Submission
        ↓
Google Sheets Trigger (n8n)
        ↓
Edit Fields Node
        ↓
HTTP Request → Gemini AI
        ↓
Code Node (Parse JSON)
        ↓
Notion (Create Database Page)
        ↓
Gmail (Send Confirmation)
```

## 📋 How to Set Up

### Prerequisites
- n8n installed locally or on cloud
- Google Cloud account with OAuth2 credentials
- Gemini API key from Google AI Studio
- Notion account with API integration

### Steps

1. Clone this repository
2. Import `workflow.json` into n8n
3. Set up Google OAuth2 credentials
4. Get Gemini API key from aistudio.google.com
5. Create Notion database with these columns:
   - Company (Title)
   - Job Title (Text)
   - Date Applied (Date)
   - Status (Select)
   - AI Summary (Text)
   - Fit Score (Number)
   - Link (URL)
6. Connect Notion integration
7. Activate the workflow
8. Start applying!

## 📊 Sample Output

**Email received after submission:**
```
✅ New Application: SWE Intern at Google

AI Summary: This role focuses on backend 
systems and API development.

Fit Score: 8/10
Reason: Strong match — Python, Firebase 
and REST API experience directly aligns.
```

**Notion Dashboard:**
| Company | Role | Date | Status | Fit Score |
|---------|------|------|--------|-----------|
| Google | SWE Intern | 11 Mar | Applied | 8/10 |
| Flipkart | SDE Intern | 11 Mar | Applied | 7/10 |

## 🔑 Environment Variables

Replace these in the workflow:
- `YOUR_GEMINI_API_KEY` — from AI Studio
- `YOUR_NOTION_DATABASE_ID` — from Notion URL
- `YOUR_NOTION_API_KEY` — from integrations page

## 👤 Author

Built by Karan — IT student at sri krishna college of technology

Connect with me on LinkedIn!
