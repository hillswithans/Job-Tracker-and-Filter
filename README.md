
Readme · MD
# Job Tracker & Search Shield
AI-Powered Job Search Filtering & Application Pipeline
 
Repository: https://github.com/hillswithans/Job-Tracker-and-Filter

Live Application: https://ais-pre-pnnooqviibfaeziylrpywy-596413656493.us-west2.run.app/

Status: Live
 
## Overview
 
Job Tracker & Search Shield is an AI-assisted job search tool that reduces the noise in modern recruiting platforms.
 
Instead of manually sorting through spam listings, recruiter posts, ghost jobs, and misleading "entry-level" roles, users paste raw job descriptions into the system. The app parses, filters, and structures them into a usable application pipeline.
 
The goal is simple: better job signals, less manual effort, more real applications sent out per week instead of time lost to triage.
 
## The Problem
 
Job searching for technical roles has become inefficient.
 
Common issues:
- Staffing agencies posing as direct employers
- Ghost or duplicate listings
- "Entry-level" roles requiring mid-level experience
- Hidden or unclear salary ranges
- Time spent manually comparing listings across platforms
- Discovering a cover letter or account signup is required only after you've already customized a resume
- No way to check a company's reputation before applying
Traditional job boards reward volume, not clarity, and none of them offer a public search API that would let a tool like this pull listings on your behalf. Scraping them directly also runs into their terms of service. So this tool works the way a person actually job-hunts: you find listings across whatever sites you use, and you paste them in here to get the noise filtered out.
 
## The Solution
 
This system acts as a filtering layer between job listings and the application process.
 
Users paste in unstructured job posts, one at a time or in a batch. The system evaluates them for:
- Direct-hire vs. recruiter/staffing-agency source
- Experience mismatch
- Salary alignment
- Whether a cover letter or account signup is required
- Company reputation signals
- Structured metadata extraction
Approved jobs are stored in a trackable application pipeline, and the app suggests adjacent job titles worth searching for next based on what's already passing your filters.
 
## Architecture
 
```
Raw job listing (pasted by user)
→ Client-side validation
→ Express API (/api/parse-job)
→ Google Gemini
→ JSON normalization
→ Shield filtering (salary, experience, staffing-agency blacklist, title/location match)
→ Application dashboard
```
 
## Features
 
**AI Job Parsing**
Converts raw job posts you paste in into structured, searchable data.
 
**Direct-Hire Filtering**
Identifies recruiters, staffing agencies, and indirect listings from the text of what you paste.
 
**Salary & Experience Validation**
Filters based on salary thresholds, experience mismatch, skill requirements, and entry-level eligibility.
 
**Cover Letter & Account Detection**
Flags whether a listing requires a cover letter or a portal account signup, before you invest time customizing anything.
 
**Company Reputation Check**
Surfaces reputation signals (e.g. Glassdoor-style rating) for a company before you apply, so a bad employer doesn't cost you an application.
 
**Application Pipeline**
Tracks job status: Listed → Applied → Interviewing → Offer.
 
**Analytics Dashboard**
Provides visibility into total jobs processed, approval rate, rejection rate, and pipeline progress.
 
**Board Recognition**
The app doesn't fetch listings from job boards on its own — there's no public search API for that on any major board, and scraping them isn't something this tool does. Instead, it recognizes board names mentioned in what you paste (LinkedIn, Indeed, Dice, Wellfound, Built In, CollegeGrad, Handshake, FlexJobs, ZipRecruiter, Google Jobs), and flags when you've pasted the same role from more than one source, which is a decent signal it's a real, actively-hiring listing rather than a stale single post.
 
## AI Workflow
 
1. User pastes a job listing (or a batch of listings)
2. Client-side validation
3. API request
4. Gemini parsing into structured fields
5. JSON normalization
6. Risk scoring
7. Salary validation
8. Experience validation
9. Direct-hire detection
10. Company reputation lookup
11. Pipeline update
## Themes
 
- **Minimalist** — monochrome, high contrast
- **Cyber** — neon blue technical UI
- **Dollhouse** — soft pastel interface
- **Splatter** — graffiti-inspired high contrast design
Themes only affect appearance, not logic.
 
## UI Language Improvements
 
Earlier system language was replaced with clearer user-facing terms:
- "Export to Spreadsheet" instead of backend sync language
- "Match Your Criteria" instead of validation pipeline terminology
- "Hidden Bad Fits" instead of risk scoring labels
## Design System Updates
 
**Dollhouse Theme**
- Fixed spacing issues between components
- Improved typography (rounded, readable fonts)
- Removed excessive decorative icons
- Structured status icons: Listed → 🌸, Applied → 🎀, Interview → 🩰, Offer → 🦢, Rejected → 🕯️, Strong Match → 🧸
**Splatter Theme**
- Stronger typography hierarchy
- Clear separation between headers and data
- Fonts: Headers — Sedgwick Ave Display, Body — JetBrains Mono
- Status icons: Listed → 🎨, Applied → 🛹, Interview → 🎭, Offer → 🖌️, Rejected → 🖍️, Strong Match → 🧱
## Engineering Decisions
 
- Dynamic UI components instead of hardcoded cards
- Centralized theme system
- Structured JSON output from AI (no freeform text)
- All downstream logic depends on normalized data
- Distance/location matching is text-based (location string and remote-status matching), not a live geocoding calculation, unless a geocoding API is explicitly wired in
## Project Evolution
 
Originally built as a job search helper. It evolved into a system that:
- Filters recruiter noise
- Evaluates job quality
- Flags cover letter and account requirements up front
- Surfaces company reputation before you apply
- Tracks application states
- Recognizes job board sources from pasted text
- Turns job search into a structured pipeline
## Future Improvements
 
- Persistent database
- User authentication
- Saved searches
- Resume matching
- Hiring analytics
- Browser extension ingestion (would let listings be captured while browsing, instead of copy-pasted)
- Real geocoding for distance filtering
- Live company reputation lookup via AI + search grounding
- Resume tailoring automation
