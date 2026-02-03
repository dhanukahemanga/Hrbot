# WhatsApp HR Bot (n8n Workflow)

This project is a WhatsApp based HR automation bot built using n8n.  
It allows candidates to view job vacancies, apply for jobs, upload CVs, and check application status directly via WhatsApp.

The bot integrates WhatsApp (via Unipile API), Microsoft Excel, and OneDrive to manage the entire recruitment flow.

---

## Features

- WhatsApp-based interactive HR bot
- Job vacancy listing from Excel
- Job details retrieval using Job ID
- Job application via WhatsApp
- CV upload and storage in OneDrive
- Automatic Application ID generation
- Application data storage in Excel
- Application status checking via Application ID

---

## Technology Stack

- n8n (Workflow Automation)
- WhatsApp API (Unipile)
- Microsoft Excel Online
- Microsoft OneDrive
- Webhooks

---

## Bot Workflow Overview

1. User sends "Hi" on WhatsApp
2. Bot displays main menu
   - Apply for a job
   - Check application status
3. Apply for a job flow
   - Bot retrieves available jobs from Excel
   - User enters Job ID
   - Bot displays job details
   - User applies using `apply <JobID>`
   - Bot requests candidate name
   - Bot requests CV upload
   - CV is stored in OneDrive
   - Application details are saved in Excel
   - Application ID is generated and sent to the user
4. Check application status flow
   - User enters Application ID
   - Bot retrieves application status from Excel
   - Status is sent to the user
