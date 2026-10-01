# 🎓 Automated Student Admission System

An automated student admission workflow built with **n8n** to simplify and streamline the student registration and selection process.

The system automatically processes applicant data from Google Sheets, evaluates applicants based on predefined criteria, sends personalized email notifications, provides AI-powered alternative school recommendations, and generates a weekly admission summary.

---

## 🚀 Features

- 📥 **Automatic Registration Processing**
  - Receives new student registration data from Google Sheets.
  - Checks whether the required applicant information is complete.

- 🔎 **Automated Applicant Screening**
  - Evaluates applicants based on predefined criteria such as:
    - Applicant age
    - Parent's income range
    - Required registration information

- ✅ **Automated Admission Classification**
  - Automatically categorizes applicants into:
    - Accepted
    - Rejected
    - Alternative recommendation

- 📧 **Automated Email Notifications**
  - Sends personalized emails to parents based on the admission result.
  - Provides information about Open House and Trial Class activities.

- 🤖 **AI-Powered School Recommendations**
  - Uses an LLM to generate recommendations for three nearby elementary schools when an applicant is not eligible due to age.

- 📊 **Weekly Executive Summary**
  - Automatically summarizes accepted and rejected applicants from the previous seven days.
  - Sends the summary via email every Monday at 08:00 WIB.

---
<img width="591" height="358" alt="image" src="https://github.com/user-attachments/assets/d8cb4353-fcb4-40b2-84ad-f6745bf2b412" />


## 🔄 Workflow Overview

```text
Google Sheets
      │
      ▼
New Student Registration
      │
      ▼
Check Required Data
      │
      ▼
Check Student Age
      │
      ├─────────────── Age > 6
      │                    │
      │                    ▼
      │              AI School Recommendation
      │                    │
      │                    ▼
      │               Email Result
      │
      ▼
Evaluate Parent Income
      │
      ├─────────────── Rejected
      │                    │
      │                    ▼
      │               Save to Sheet
      │                    │
      │                    ▼
      │               Email Result
      │
      └─────────────── Accepted
                           │
                           ▼
                      Save to Sheet
                           │
                           ▼
                      Email Result


