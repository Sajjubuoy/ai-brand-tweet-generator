# AI Brand Tweet Generator

An AI-powered automation workflow that generates **10 on-brand tweets** based on a brand’s tone, personality, and communication style.

This system uses **Google Forms, Google Sheets, n8n, and OpenAI** to analyze brand voice and generate social media content automatically.

---

# Project Overview

The goal of this project is to build a simple system where a user provides brand information, and the system generates tweets that match the brand's communication style.

The workflow analyzes brand tone, audience, and messaging style before generating tweets that feel authentic to the brand.

---

# System Workflow

User → Google Form → Google Sheets → n8n Automation  
→ Brand Voice Analysis (LLM) → Tweet Generation (LLM)  
→ Results stored in Google Sheets

---

# Input Interface

Users submit brand details through a Google Form.

### Google Form Link
https://forms.gle/SXmp9WCDcP6pz2Xt6

Inputs include:

- Brand Name  
- Industry / Category  
- Campaign Objective  
- Product / Brand Description

---

# Output Dashboard

All generated results are automatically stored in a Google Spreadsheet.

### Google Sheets Link
https://docs.google.com/spreadsheets/d/1Vcha-ktEOx1Bd0Kc2hMtfx1zrj0ith8IzOQdi63wZyU/edit?usp=sharing

The spreadsheet contains:

- User inputs
- AI-generated brand voice summary
- Generated tweets
- Execution timestamps

---

# Workflow Architectures

This project demonstrates **two different AI workflow architectures**.

---

## Single LLM Chain Workflow

In this approach, one AI model performs both:

- Brand voice analysis  
- Tweet generation

Workflow Steps:

Google Sheets Trigger  
→ Edit Fields (input normalization)  
→ LLM Model  
→ Edit Fields (output formatting)  
→ Append results to Google Sheets

---

## Dual LLM Chain Workflow

In this architecture, the process is separated into two AI stages.

1. Brand Voice Analysis  
2. Tweet Generation based on the analyzed voice

Workflow Steps:

Google Sheets Trigger  
→ Edit Fields  
→ LLM Model 1 (Brand Voice Analysis)  
→ Edit Fields  
→ LLM Model 2 (Tweet Generation)  
→ Edit Fields  
→ Append results to Google Sheets

This approach improves tone consistency and tweet quality.

---

# Tools and Technologies

- **n8n** – workflow automation  
- **OpenAI API** – AI brand voice analysis and tweet generation  
- **Google Forms** – input interface  
- **Google Sheets** – data storage and trigger system

---

# Example Brands Tested

The system was tested using different brands to demonstrate tone adaptation.

**Brand 1:** FastTrack  
Tone: edgy, youthful, trend-focused

**Brand 2:** Glowsip  
Tone: playful, wellness-oriented, lifestyle-focused

---

# Note

Two automation workflows are currently active for demonstration purposes.

Because of this, some form submissions may generate **duplicate outputs** in the spreadsheet. This occurs because both the **Single LLM workflow and Dual LLM workflow** process the same form entry simultaneously.

This setup was used to compare both workflow architectures.

---

# Author

**K Mahammad Sajjad**  
