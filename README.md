# Job Tracker & Search Shield

### AI-Powered Job Search Filtering & Application Pipeline

**Repository:** https://github.com/hillswithans/Job-Tracker-and-Filter  
**Live Application:** https://ais-pre-pnnooqviibfaeziylrpywy-596413656493.us-west2.run.app/  
**Status:** Live

---

## Overview

Job Tracker & Search Shield is an AI-assisted job search tool that reduces the noise in modern recruiting platforms.

Instead of manually sorting through spam listings, recruiter posts, ghost jobs, and misleading “entry-level” roles, users paste raw job descriptions into the system.

The app parses, filters, and structures them into a usable application pipeline.

The goal is simple: better job signals, less manual effort.

---

## The Problem

Job searching for technical roles has become inefficient.

Common issues:

- Staffing agencies posing as direct employers  
- Ghost or duplicate listings  
- “Entry-level” roles requiring mid-level experience  
- Hidden or unclear salary ranges  
- Time spent manually comparing listings across platforms  

Traditional job boards reward volume, not clarity.

---

## The Solution

This system acts as a filtering layer between job listings and the application process.

Users submit unstructured job posts. The system evaluates them for:

- Direct-hire vs recruiter source  
- Experience mismatch  
- Salary alignment  
- Employer transparency  
- Scam or low-quality signals  
- Structured metadata extraction  

Approved jobs are stored in a trackable application pipeline.

---

## Architecture

Raw Job Listings  
→ Client-side validation  
→ Express API (`/api/parse-job`)  
→ Google Gemini 3.5 Flash  
→ JSON normalization  
→ Risk + quality filtering  
→ Application dashboard  

---

## Features

### AI Job Parsing
Converts raw job posts into structured, searchable data.

### Direct-Hire Filtering
Identifies recruiters, staffing agencies, and indirect listings.

### Salary & Experience Validation
Filters based on:

- Salary thresholds  
- Experience mismatch  
- Skill requirements  
- Entry-level eligibility  

### Application Pipeline
Tracks job status:

Listed → Applied → Interviewing → Offer

### Analytics Dashboard
Provides visibility into:

- Total jobs processed  
- Approval rate  
- Rejection rate  
- Pipeline progress  

### Multi-Board Support
Supports ingestion from:

LinkedIn, Indeed, Dice, Wellfound, Built In, CollegeGrad, Handshake, FlexJobs, ZipRecruiter, Google Jobs

---

## AI Workflow

1. Input job listing  
2. Client validation  
3. API request  
4. Gemini parsing  
5. JSON normalization  
6. Risk scoring  
7. Salary validation  
8. Experience validation  
9. Direct-hire detection  
10. Pipeline update  

---

## Themes

- Minimalist — monochrome, high contrast  
- Cyber — neon blue technical UI  
- Dollhouse — soft pastel interface  
- Splatter — graffiti-inspired high contrast design  

Themes only affect appearance, not logic.

---

## UI Language Improvements

Earlier system language was replaced with clearer user-facing terms.

Examples:

- “Export to Spreadsheet” instead of backend sync language  
- “Match Your Criteria” instead of validation pipeline terminology  
- “Hidden Bad Fits” instead of risk scoring labels  

---

## Design System Updates

### Dollhouse Theme
- Fixed spacing issues between components  
- Improved typography (rounded, readable fonts)  
- Removed excessive decorative icons  
- Structured status icons:

Listed → 🌸  
Applied → 🎀  
Interview → 🩰  
Offer → 🦢  
Rejected → 🕯️  
Strong Match → 🧸  

---

### Splatter Theme
- Stronger typography hierarchy  
- Clear separation between headers and data  
- Fonts:
  - Headers: Sedgwick Ave Display  
  - Body: JetBrains Mono  

Status icons:

Listed → 🎨  
Applied → 🛹  
Interview → 🎭  
Offer → 🖌️  
Rejected → 🖍️  
Strong Match → 🧱  

---

## Engineering Decisions

- Dynamic UI components instead of hardcoded cards  
- Centralized theme system  
- Structured JSON output from AI (no freeform text)  
- All downstream logic depends on normalized data  

---

## Project Evolution

Originally built as a job search helper.

It evolved into a system that:

- filters recruiter noise  
- evaluates job quality  
- tracks application states  
- standardizes job board inputs  
- turns job search into a structured pipeline  

---

## Future Improvements

- Persistent database  
- User authentication  
- Saved searches  
- Resume matching  
- Hiring analytics  
- Browser extension ingestion  
- Company reputation scoring  
- Resume tailoring automation  

---

## Running Locally

```bash
git clone https://github.com/hillswithans/Job-Tracker-and-Filter.git
cd Job-Tracker-and-Filter
npm install
npm run dev
```

## Author

**Samantha Hills**

Built as an exploration of AI-assisted workflow automation, structured data processing, and practical full-stack application development.
