# Job Tracker & Search Shield

### AI-Powered Job Search Filtering & Application Pipeline

**Status:** Live  
**Live Application:** https://ais-pre-pnnooqviibfaeziylrpywy-596413656493.us-west2.run.app/

---

## Overview

Job Tracker & Search Shield is an AI-assisted recruitment workflow designed to reduce the noise of modern job searching.

Instead of spending hours sorting through spam listings, staffing agency reposts, ghost jobs, and “entry-level” roles that require senior-level experience, users paste raw job descriptions into the system.

The app parses, cleans, filters, and structures them into a usable application pipeline.

The goal isn’t more jobs. It’s better signal, less noise.

---

## The Problem

Job searching for entry-level technical roles has become inefficient and repetitive.

- Staffing agencies posing as direct employers  
- Ghost listings and AI-generated spam  
- “Entry-level” roles requiring multiple years of experience  
- Hidden or vague salary information  
- Endless manual comparison across job boards  

Traditional job boards reward scrolling, not clarity.

---

## The Solution

This system acts as a filtering layer between raw job listings and the application process.

Users submit unstructured job posts. The system evaluates them for:

- Direct-hire vs recruiter source  
- Experience mismatch  
- Salary alignment  
- Employer transparency  
- Scam or low-quality signals  
- Structured metadata extraction  

Approved roles are placed into a trackable pipeline instead of being lost in tabs or bookmarks.

---

## Architecture

Raw Job Listings  
→ Ingestion Canvas (client-side validation)  
→ Express backend (/api/parse-job)  
→ Google Gemini 3.5 Flash  
→ Structured JSON normalization  
→ Risk and quality filtering  
→ Application pipeline dashboard  

---

## Features

### AI-Powered Job Parsing  
Paste any job post. It becomes structured, searchable data.

### Direct-Hire Filtering  
Flags staffing agencies, recruiters, and third-party listings.

### Salary & Experience Validation  
Filters based on thresholds, skills, and realism checks.

### Application Pipeline  
Listed → Applied → Interviewing → Offer

### Analytics Dashboard  
Tracks scans, approvals, rejection rate, and pipeline progress.

### Multi-Board Ingestion  
Supports LinkedIn, Indeed, Dice, Wellfound, Built In, CollegeGrad, Handshake, FlexJobs, ZipRecruiter, Google Jobs.

---

## AI Workflow

1. Client validation  
2. API request  
3. Gemini parsing  
4. JSON normalization  
5. Risk scoring  
6. Experience validation  
7. Salary validation  
8. Direct-hire check  
9. Dashboard update  
10. Pipeline insertion  

---

## Themes

- Minimalist: high contrast monochrome  
- Cyber: neon blue technical style  
- Dollhouse: soft pastel UI  
- Splatter: graffiti-inspired high contrast system  

Each theme changes visuals only. Core logic stays identical.

---

## UI Language & Design Updates

### Removing AI jargon from the interface

- Export to Spreadsheet (instead of internal sync terms)  
- Match Your Criteria (instead of validation pipelines)  
- Hidden Bad Fits (instead of risk scoring abstractions)  

---

### Dollhouse Theme

- Fixed spacing to prevent shadow overlap  
- Rounded typography (Quicksand / Nunito style)  
- Removed sparkle clutter  
- Icon system:

Listed → 🌸  
Applied → 🎀  
Interview → 🩰  
Offer → 🦢  
Rejected → 🕯️  
Strong Match → 🧸  

---

### Splatter Theme

- Header font: Sedgwick Ave Display  
- Body font: JetBrains Mono  
- High contrast separation between headers and data  

Icon system:

Listed → 🎨  
Applied → 🛹  
Interview → 🎭  
Offer → 🖌️  
Rejected → 🖍️  
Strong Match → 🧱  

---

## Engineering Decisions

- Dynamic UI components replace hardcoded cards  
- Centralized theme system controls styling globally  
- Gemini outputs structured JSON only  
- All logic depends on normalized data, not raw text  

---

## Project Evolution

Originally a simple job search helper.

Now a system that:

- filters recruiter noise  
- evaluates job quality  
- tracks application state  
- enforces consistency across job boards  
- turns job searching into a structured workflow  

---

## Future Improvements

- Persistent database  
- Authentication  
- Saved searches  
- Resume matching  
- Hiring trend analytics  
- Browser extension ingestion  
- Company reputation scoring  
- AI resume tailoring  

---

## Running Locally

```bash
git clone https://github.com/hillswithans/Job-Tracker-and-Filter
cd YOUR_REPO
npm install
npm run dev
```

## Author

**Samantha Hills**

Built as an exploration of AI-assisted workflow automation, structured data processing, and practical full-stack application development.
