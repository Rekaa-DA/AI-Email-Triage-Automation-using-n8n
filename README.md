# AI-Email-Triage-Automation-using-n8n

## Workflow Architecture

<img width="1641" height="847" alt="workflow-execution screenshot" src="https://github.com/user-attachments/assets/6f768115-3e06-4b73-9ad1-2373076e3caf" />


## Project Overview

This project automates Gmail email management using the n8n workflow automation platform. The workflow automatically retrieves incoming Gmail emails, analyzes their content using JavaScript, classifies emails into predefined categories, and applies Gmail labels to organize the inbox.

Unlike manual workflows, this solution runs automatically every minute using a Schedule Trigger, eliminating manual intervention and improving email management efficiency.

## Project Objectives

- Automate Gmail email processing.
- Retrieve incoming emails automatically.
- Classify emails into Important, Job, and Spam categories.
- Apply Gmail labels automatically.
- Reduce manual email management.
- Improve inbox organization and productivity.
- Demonstrate workflow automation using n8n and Gmail API.

## Tools and Technologies

| Tool | Purpose |
|------|---------|
| n8n Cloud | Workflow Automation |
| Gmail API | Retrieve and Update Gmail Messages |
| JavaScript | Email Classification Logic |
| Switch Node | Conditional Routing |
| Edit Fields Node | Data Preparation |
| Gmail Labels | Automatic Email Organization |
| GitHub | Version Control |

## Workflow Explanation

### Schedule Trigger

The workflow starts automatically every one minute without manual intervention.

### Gmail – Get Many Messages

Retrieves incoming Gmail emails and extracts:

- Email ID
- Subject
- Sender
- Receiver
- Email Body
- Existing Labels

### JavaScript Email Classification

The JavaScript node analyzes email content and classifies emails into:

- Important
- Job
- Spam

It also generates:

- Category
- Priority
- Summary

### Sample Output

```json
{
  "category": "Job",
  "priority": "Medium",
  "summary": "Email classified as Job"
}
```

### Switch Node

Routes emails to the appropriate branch based on the detected category.

| Category | Output Branch |
|----------|---------------|
| Important | Important Branch |
| Job | Job Branch |
| Spam | Spam Branch |

### Edit Fields

Prepares Gmail label information before updating emails.

### Gmail Label Management

Automatically applies Gmail labels based on the classified category.

| Category | Gmail Label |
|----------|-------------|
| Important | Important |
| Job | Job |
| Spam | AI-Spam |

## Workflow Execution

The workflow automatically:

- Retrieves Gmail messages
- Reads email content
- Classifies emails using JavaScript
- Routes emails using the Switch Node
- Applies Gmail labels
- Runs every minute

## Key Features

- Automated Gmail email processing
- JavaScript-based email classification
- Automatic Gmail label assignment
- Conditional routing using Switch Node
- Continuous workflow execution
- Gmail inbox organization

## Business Benefits

- Reduces manual email sorting
- Organizes Gmail inbox automatically
- Identifies job-related emails quickly
- Highlights important notifications
- Improves productivity

## Future Enhancements

- Integrate Google Gemini or OpenAI
- Generate automatic email replies
- Store classified emails in Google Sheets
- Build a Power BI dashboard
- Add sentiment analysis

## Project Outcome

The project successfully automates Gmail email classification and organization using n8n, JavaScript, and Gmail API. The workflow runs automatically every minute, reducing manual effort while improving inbox management and productivity.

## 👤 Author

**Rekaa**

📊 Aspiring Data Analyst

🚀 Open to Data Analyst and Automation Opportunities
