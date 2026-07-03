# Job Tracker & Search Shield
### AI-Powered Job Search Filtering & Application Pipeline

![Status](https://img.shields.io/badge/Status-Live-success)
![React](https://img.shields.io/badge/Frontend-React-61DAFB)
![Node.js](https://img.shields.io/badge/Backend-Node.js-339933)
![Express](https://img.shields.io/badge/API-Express-000000)
![Gemini](https://img.shields.io/badge/AI-Google_Gemini_3.5_Flash-4285F4)
![License](https://img.shields.io/badge/License-MIT-blue)

**Live Application:** https://ais-pre-pnnooqviibfaeziylrpywy-596413656493.us-west2.run.app/

---

## Overview

Job Tracker & Search Shield is an AI-assisted recruitment workflow designed to reduce the noise of modern job searching.

Rather than spending hours sorting through misleading listings, staffing agency reposts, ghost jobs, and underqualified opportunities, users can paste raw job descriptions into the application where they are automatically analyzed, filtered, normalized, and organized into a structured application pipeline.

The goal isn't simply finding more jobs—it's finding better ones while eliminating unnecessary manual review.

---

# The Problem

Searching for entry-level technical positions has become increasingly inefficient.

Common issues include:

- Staffing agencies masquerading as direct employers
- Ghost listings and AI-generated spam
- Positions advertised as "entry level" requiring multiple years of experience
- Low salary postings hidden beneath vague descriptions
- Hours spent manually comparing listings across multiple job boards

Traditional job boards encourage endless scrolling.

Job Tracker & Search Shield instead treats job searching like a data pipeline.

---

# The Solution

The application acts as a filtering layer between raw job listings and the user's application process.

Instead of manually evaluating every posting, users submit unstructured listings which are automatically processed through an AI-powered validation workflow.

Listings are evaluated for:

- Direct-hire vs. third-party recruiter
- Experience requirements
- Salary thresholds
- Employer transparency
- Potential scam indicators
- Structured job metadata

Approved positions are then added to a searchable application tracker with analytics and status management.

---

# Architecture

```
Raw Job Listings
        │
        ▼
Data Ingestion Canvas
(Client Validation)
        │
        ▼
Express Backend
/api/parse-job
        │
        ▼
Google Gemini 3.5 Flash
Content Parsing
        │
        ▼
Structured JSON
Normalization
        │
        ▼
Risk Analysis
&
Quality Filtering
        │
        ▼
Application Pipeline
Analytics Dashboard
```

---

# Features

## AI-Powered Job Parsing

Paste raw job descriptions from virtually any source.

The backend converts unstructured text into normalized structured data that can be analyzed and tracked throughout the application.

---

## Direct-Hire Gatekeeping

Automatically identifies and flags:

- Staffing agencies
- Third-party recruiters
- Placement firms
- Anonymous employers
- Potential ghost listings

Designed to reduce time spent applying to intermediary recruiters.

---

## Salary & Experience Validation

Listings can be filtered according to configurable requirements including:

- Minimum salary
- Maximum experience threshold
- Required skills
- Entry-level eligibility

---

## Application Pipeline

Approved positions move through a complete workflow:

```
Listed
    ↓
Applied
    ↓
Interviewing
    ↓
Offer
```

Each listing maintains its own status throughout the hiring process.

---

## Analytics Dashboard

Real-time metrics provide visibility into the current search including:

- Total listings scanned
- Approved positions
- Blocked listings
- Direct-hire ratio
- Pipeline progress

---

## Dynamic Multi-Board Ingestion

Instead of hardcoding individual job boards, the interface generates reusable cards from a centralized configuration.

Supported sources include:

- LinkedIn
- Indeed
- Dice
- Wellfound
- Built In
- CollegeGrad
- Handshake
- FlexJobs
- ZipRecruiter
- Google Jobs

This architecture makes adding or removing job boards significantly easier while keeping the interface maintainable.

---

# AI Workflow

When a user submits a listing, the application performs the following sequence:

1. Client-side validation
2. Backend API request
3. Gemini content parsing
4. JSON normalization
5. Risk assessment
6. Experience validation
7. Salary validation
8. Direct-hire verification
9. Dashboard update
10. Pipeline insertion

---

# Themes

The application includes four interchangeable visual themes while preserving identical functionality.

| Theme | Design |
|-------|--------|
| Minimalist | High-contrast monochrome interface |
| Cyber | Neon blue technical aesthetic |
| Dollhouse | Playful pastel interface inspired by toy packaging |
| Splatter | Graffiti-inspired neon grunge aesthetic |

Each theme updates typography, colors, borders, shadows, backgrounds, and interaction effects without changing application behavior.

---

# Tech Stack

## Frontend

- React
- Vite
- Tailwind CSS

## Backend

- Node.js
- Express

## AI

- Google Gemini 3.5 Flash

## Data

- Structured JSON normalization
- Clipboard TSV export

---

# Engineering Decisions

Several architectural changes were made during development to improve scalability and maintainability.

### Dynamic Component Rendering

Legacy hardcoded ingestion cards were replaced with reusable components generated from a centralized configuration array.

This reduced duplicate code and made new job boards easy to support.

---

### Centralized Theme Architecture

Rather than styling individual components independently, global theme rules control typography, color palettes, shadows, and interaction styles across the application.

---

### Structured AI Responses

Rather than relying on conversational AI output, Gemini is instructed to produce normalized JSON suitable for downstream processing.

This enables:

- analytics
- filtering
- pipeline tracking
- future persistence

without requiring additional parsing.

---

# Project Evolution

The project began as a simple AI prompt intended to automate weekly job searches.

As development progressed, it evolved into a complete workflow that:

- filters recruitment spam
- evaluates listing quality
- tracks applications
- analyzes hiring trends
- supports configurable search criteria

Instead of acting as a chatbot, the application functions as an intelligent gatekeeper between job boards and the application process.

---

# Future Improvements

Planned enhancements include:

- Persistent database storage
- User authentication
- Saved searches
- Resume matching
- Historical hiring trend analysis
- Browser extension support
- Automated job ingestion
- Company reputation scoring
- AI-powered resume tailoring

---

# Lessons Learned

This project reinforced several engineering concepts including:

- Prompt engineering
- Full-stack API integration
- AI-assisted data normalization
- Reusable React component architecture
- State management
- Configuration-driven UI design
- Human-in-the-loop AI workflows

---

# Running Locally

```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPO.git

cd YOUR_REPO

npm install

npm run dev
```

---

# Feedback

Job Tracker & Search Shield is an evolving project.

If you discover false positives, recruiter patterns, or ideas for improving the filtering engine, feedback is always welcome.

---

## Author

**Samantha Hills**

Built as an exploration of AI-assisted workflow automation, structured data processing, and practical full-stack application development.
