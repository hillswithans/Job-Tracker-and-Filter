Job Tracker & Search Shield (My Job Search Guard)
Asynchronous, Zero-Noise Market Gatekeeper & Priority Pipeline

Live Application Link: Launch Job Search Guard

Status: Live Production | Monitored via continuous user-ingestion validation

🧐 The Vision: Anti-Noise Recruitment
When job searching, the entry-level landscape is often oversaturated with misleading listings, predatory "AI farming," and staffing agency spam. I built Job Search Guard to shift the workflow from reactive, time-consuming browsing to an isolated, variable-driven dashboard. This system acts as a defensive framework for technical professionals to level the algorithmic playing field.

🔄 Unified Architectural Flow
This system operates as a unified, full-stack recruitment defense pipeline. It bridges a reactive React frontend with a high-intelligence Express backend, designed to filter out staffing agency middle-men, underpaid roles, and tedious application portals.

Plaintext
[Raw Job Listings Input]  ──>  [Ingestion Canvas & Security Rules]
                                       │
                                       ▼
                         [Express Backend /api/parse-job]
                         - Gemini 3.5 Flash Content Parsing
                         - Anti-Middleman & Anti-Scam Rules
                                       │
                                       ▼
                       [Interactive Results Table & Analytics]
                       - Real-Time Risk Analysis
                       - Status Pipeline Tracking (Listed, Applied, etc.)
⚙️ Core Functional Modules
A. Ingestion & Pre-Filtering (DataIngestionCanvas)
Users paste raw job descriptions, unstructured listings, or batch lists into an interactive paste area. Before sending queries to the server, local scripts evaluate simple rules—validating experience limits, identifying potential salary mismatches, and confirming necessary data presence—to reduce server load and provide instant visual feedback.

B. Intelligent Security Gatekeeping (/api/parse-job)
When data is scanned, the client calls the backend API endpoint. A specialized configuration block utilizing Gemini 3.5 Flash acts as an automated security scanner:

The Direct-Hire Gate: Identifies third-party staffing agencies (e.g., CyberCoders, Robert Half, Apex Systems) and flags or blocks them.

Integrity Scan: Automatically detects "ghost" listings, anonymous/hidden employers, and roles failing to meet standard requirements.

Structured Normalization: The model parses unstructured text into a strict JSON payload containing health metrics and structured job pipeline arrays.

C. Live Security Insights (AnalyticsDashboard)
The dashboard reads calculated statistics from scanned listings and maps them to a modern data grid. Aesthetic metric cards display real-time calculations—total scanned positions, blocked listings, and valid direct-hire options—helping users visualize the direct-hire ratio of their active search pool.

D. Interactive Pipeline Tracking (PositionsTable)
Approved positions populate the central table.

Risk Identification: Warning flags (e.g., "Third-Party Agency," "Low Salary Floor") are displayed prominently.

Pipeline Control: Users transition positions dynamically across lifecycle steps (Listed → Applied → Interviewing → Offer Received).

🎨 UI & UX Design
Extended Canvas Layout: The interface utilizes a widescreen, responsive layout, offering an unobstructed visual space for reading dense job descriptions and scanning warnings.

Elegant Slate Aesthetic: The workspace features a clean, high-contrast Slate and Charcoal color theme. Beautiful typography pairings and monospace status indicators create a professional, low-distraction workspace that avoids generic blue and navy palettes.

☰ The Tech Stack
Frontend: React, Tailwind CSS, Vite.

Backend: Node.js, Express.

Parsing Intelligence: Google Gemini API (Gemini 3.5 Flash).

Sync Layer: Copy-to-clipboard TSV Matrix for seamless transition to personal tracking ledgers.

🗪 Feedback & Iteration
This project is a living tool. Because most platforms lock functionality behind paywalls, this app keeps the utility open and user-driven.

Share Feedback Form — Use this link to help refine the engine, report false negatives, or suggest new anti-spam rules.
