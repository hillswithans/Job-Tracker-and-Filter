# Job Tracker & Search Shield

**An AI-powered tool that helps you decide which jobs are worth applying to.**

**Live App:**  
https://ais-pre-pnnooqviibfaeziylrpywy-596413656493.us-west2.run.app/

**GitHub Repository:**  
https://github.com/hillswithans/Job-Tracker-and-Filter

**Status:** Live

---

## What It Does

Job Tracker & Search Shield helps make job searching less annoying.

You paste a job listing into the app, and it checks the posting for things like:

- Salary
- Experience requirements
- Staffing agencies
- Cover letter requirements
- Account signup requirements
- Company ratings
- Location
- Remote or hybrid options

The app then helps you decide whether to:

- Apply now
- Review the job later
- Skip the job

It also saves approved jobs in an application tracker.

---

## Why I Built It

Job searching takes too much time.

A listing might look promising at first, but then you discover:

- It is posted by a staffing agency
- The salary is too low
- The job says “entry-level” but wants five years of experience
- You need to create another account
- A cover letter is required
- The company has poor reviews
- The job is not actually remote
- You already saw the same job somewhere else

This app helps catch those problems before you spend time applying.

---

## How It Works

1. Paste a job description into the app.
2. The app sends the job listing to Google Gemini.
3. Gemini pulls out important details.
4. The app compares the job against your preferences.
5. The job is marked as a match, warning, or bad fit.
6. Approved jobs can be added to your application tracker.

---

## What the App Checks

### Salary

The app compares the listed salary to your minimum salary.

It can warn you when:

- The salary is too low
- No salary is listed
- The salary range is unclear

---

### Experience

The app checks how many years of experience the job requires.

This helps catch “entry-level” jobs that are not actually entry-level.

---

### Staffing Agencies

The app looks for staffing agencies and third-party recruiters.

This helps separate direct employer jobs from recruiter listings.

---

### Cover Letters

The app checks whether a cover letter, writing sample, or extra application question is required.

This helps you know how much time the application may take.

---

### Account Signups

The app checks whether you may need to create an account on sites like:

- Workday
- Taleo
- iCIMS
- Greenhouse
- Lever

The job is not automatically rejected. The app simply warns you about the extra work.

---

### Company Reputation

The app lets you check a company’s rating in two ways.

#### AI Check

You can paste a company review or Glassdoor link.

Gemini searches for information about:

- Company ratings
- Recent layoffs
- Common complaints
- Workplace concerns

#### Manual Rating

You can also type in a company rating yourself.

The app can label companies as:

- Highly Rated
- Low Rating
- Unverified

---

### Location

The app compares the location in the job listing to your preferred location.

It can recognize words like:

- Remote
- Hybrid
- On-site
- Boston
- Providence

The app currently uses text matching.

It does not calculate real driving distance or commute time.

---

### Job Board Sources

The app can recognize job board names inside the text you paste.

Supported job boards include:

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

If the same job appears on more than one site, the app can flag it as a possible duplicate or cross-posted listing.

The app does not scrape job boards or collect listings in the background.

---

## Job Results

The app sorts jobs into three groups.

### Strong Match

The job matches your main preferences.

This may mean:

- The salary is acceptable
- The experience requirement fits
- The location matches
- It appears to be direct hire

**Recommended action:** Apply Now

---

### Review Later

The job mostly matches, but there is something to check.

For example:

- No salary is listed
- A cover letter is required
- An account signup is required
- The company rating is unknown
- The experience requirement is slightly high

**Recommended action:** Review Details

---

### Hidden Bad Fit

The job does not match your main requirements.

For example:

- The salary is too low
- The experience requirement is too high
- It is posted by a staffing agency
- The location does not match
- The company rating is very low

**Recommended action:** Skip

---

## Application Tracker

Jobs that pass your filters can be tracked through the application process.

```text
Listed → Applied → Interviewing → Offer
````

Jobs can also be marked as rejected.

---

## Dashboard

The dashboard shows:

* Total jobs checked
* Jobs approved
* Jobs rejected
* Applications sent
* Interviews
* Offers
* Approval rate
* Rejection rate

This helps you see how your job search is going without building another spreadsheet from scratch.

---

## Search Tools

The app can help prepare searches for different job boards.

You choose:

* Job title
* Location
* Job boards

The app can then open searches for sites like LinkedIn, Indeed, Dice, and Google Jobs.

It can also add staffing agency names to the search exclusions when supported.

The app opens the searches in your browser.

It does not crawl or scrape job boards.

---

## Suggested Job Titles

The app can suggest similar job titles based on jobs that match your filters.

For example:

* Data Analyst
* Reporting Analyst
* Business Intelligence Analyst
* Operations Analyst
* Data Quality Analyst
* Junior Analytics Engineer

This can help you find roles you may not have searched for yet.

---

## Spreadsheet Export

You can export your job data to a spreadsheet.

This makes it easier to save, sort, or review your job search outside the app.

---

## Themes

The app includes four visual themes.

### Minimalist

A simple black-and-white design.

### Cyber

A neon blue technical design.

### Dollhouse

A soft pastel design with playful icons.

### Splatter

A high-contrast graffiti-inspired design.

Themes only change how the app looks.

They do not change how the filters work.

---

## Technology Used

The project was built with:

* React
* TypeScript
* Vite
* Node.js
* Express
* Google Gemini
* JSON
* Local storage

---

## Basic Technical Flow

```text
User pastes a job listing
        ↓
The app checks the input
        ↓
The listing is sent to the Express server
        ↓
Google Gemini reads the job description
        ↓
The job is turned into structured JSON
        ↓
The app checks salary, experience, location, and other rules
        ↓
The job appears in the dashboard
```

---

## Why the App Uses JSON

Gemini returns job information in a structured format.

This makes it easier for the app to consistently read fields like:

* Company
* Job title
* Salary
* Location
* Experience
* Skills
* Application requirements

The app does not rely only on a paragraph written by AI.

---

## Project Changes

The project started as a simple job tracker.

It later grew to include:

* AI job description parsing
* Staffing agency filtering
* Salary checks
* Experience checks
* Cover letter detection
* Account signup warnings
* Company reputation checks
* Job board recognition
* Application tracking
* Analytics
* Theme options
* Suggested job titles

---

## Current Limits

The app depends on the information inside the job listing.

It may not always correctly identify:

* Salary
* Experience level
* Staffing agencies
* Company ratings
* Cover letter requirements
* Job board sources

AI results should still be reviewed by the user.

The app helps with decisions, but it does not make the final decision for you.

---

## Future Plans

Possible future updates include:

* User accounts
* A permanent database
* Saved searches
* Resume matching
* Resume tailoring
* Better duplicate detection
* More application analytics
* A browser extension
* Real distance and commute calculations
* More export options

---

## Setup

Create a `.env` file and add your Gemini API key.

```env
GEMINI_API_KEY=your_gemini_api_key_here
```

The API key stays on the server and is not shown in the browser.

---

## Main Goal

Job Tracker & Search Shield helps you spend less time sorting through bad job listings.

It helps you:

* Find better matches
* Avoid staffing agency noise
* Catch misleading requirements
* See application requirements early
* Track your progress
* Focus on jobs that are actually worth your time

```
```
