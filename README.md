# Job Tracker & Search Shield (My Job Search Guard)

Asynchronous, Zero-Noise Market Gatekeeper & Priority Pipeline

* **Live Application Link:** [Launch Job Search Guard](https://ais-pre-pnnooqviibfaeziylrpywy-596413656493.us-west2.run.app/)
* **Status:** Live Production | Monitored via continuous user-ingestion validation

---

## 🧐 The Vision: Anti-Noise Recruitment

When job searching, the entry-level landscape is often oversaturated with misleading listings, predatory "AI farming," and staffing agency spam. I built Job Search Guard to shift the workflow from reactive, time-consuming browsing to an isolated, variable-driven dashboard. This system acts as a defensive framework for technical professionals to level the algorithmic playing field.

---

## 🗺️ Unified Architectural Flow

This system operates as a unified, full-stack recruitment defense pipeline. It bridges a reactive React frontend with a high-intelligence Express backend, designed to filter out staffing agency middle-men, underpaid roles, and tedious application portals.

```text
[Plaintext Raw Job Listings Input]
               │
               ▼
 [Ingestion Canvas & Security Rules]
               │
               ▼
   [Express Backend /api/parse-job] ──► Gemini 3.5 Flash Content Parsing
               │                       (Anti-Middleman & Anti-Scam)
               ▼
[Interactive Results Table & Analytics] ──► Real-Time Risk Analysis & Status Pipeline Tracking
```

---

## ⚙️ Core Functional Modules

### A. Ingestion & Pre-Filtering (`DataIngestionCanvas`)
Users paste raw job descriptions, unstructured listings, or batch lists into an interactive paste area. Before sending queries to the server, local scripts evaluate simple rules—validating experience limits, identifying potential salary mismatches, and confirming necessary data presence—to reduce server load and provide instant visual feedback.

#### 🛠️ Dynamic 10-Board Ingestion Engine
To resolve the rigid legacy layout that locked users into exactly 5 static, hardcoded HTML blocks, the canvas features a high-density, reusable, and responsive `<Card>` component mapped dynamically over a global configuration matrix:

```typescript
const ALL_BOARDS = [
  'LinkedIn', 'Dice', 'Indeed', 'Wellfound', 'Built In', 
  'CollegeGrad', 'Handshake', 'FlexJobs', 'ZipRecruiter', 'Google Jobs'
];
```

* **Interactive State Binding:** Styled each card with dynamic states ("Active / Shield Online" vs "Inactive / Shield Offline") paired with custom icons, customized details, and specialized visual highlights corresponding perfectly to whether they are currently activated.
* **Theme Integration:** Card states conform seamlessly across all 4 system presets: Minimalist, Cyber, Dollhouse, and Splatter.

### B. Intelligent Security Gatekeeping (`/api/parse-job`)
When data is scanned, the client calls the backend API endpoint. A specialized configuration block utilizing **Gemini 3.5 Flash** acts as an automated security scanner:
* **The Direct-Hire Gate:** Identifies third-party staffing agencies (e.g., CyberCoders, Robert Half, Apex Systems) and flags or blocks them.
* **Integracy Scan:** Automatically detects "ghost" listings, anonymous/hidden employers, and roles failing to meet standard requirements.
* **Structured Normalization:** The model parses unstructured text into a strict JSON payload containing health metrics and structured job pipeline arrays.

### C. Live Security Insights (`AnalyticsDashboard`)
The dashboard reads calculated statistics from scanned listings and maps them to a modern data grid. Aesthetic metric cards display real-time calculations—total scanned positions, blocked listings, and valid direct-hire options—helping users visualize the direct-hire ratio of their active search pool.

### D. Interactive Pipeline Tracking (`PositionsTable`)
Approved positions populate the central table.
* **Risk Identification:** Warning flags (e.g., *"Third-Party Agency"*, *"Low Salary Floor"*) are displayed prominently.
* **Pipeline Control:** Users transition positions dynamically across lifecycle steps (`Listed` ➔ `Applied` ➔ `Interviewing` ➔ `Offer Received`).

---

## 🎨 UI & UX Design Themes

### Global Typography Normalization
Declared a highly legible, neutral typography standard across all interfaces to ensure consistent, premium rendering across all user platforms and operational body copy:

```css
font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
```

---

### System Presets Matrix

The application layout shifts dynamically across 4 core design ecosystem presets:

| Theme Preset | Card Borders & Frames | Background Architecture | Focal Highlights & Accents |
| :--- | :--- | :--- | :--- |
| **Minimalist** | Clean monochrome white-on-black borders | Solid white-on-black canvas | Sharp, high-contrast boundaries |
| **Cyber** | Glowing cyan borders | Dark technical backdrops | Radial blue-cyan glow fields |
| **Dollhouse** | Thick Rose Gold borders (`#D8A7B1`) | 3-way pastel warm gradient backdrop | Heavy coral 3D flat shadows |
| **Splatter** | Kinetic neon green border-box outlines | SVG noise-grain texturing layer | High-octane violet-cyan gradients |

---

### Deep Dive: Hard Theme Mutations

#### 1. Splatter (Neon Grunge / Oasis Rebrand) Overhaul
A high-energy, raw, graffiti-inspired technical workspace.
* **Typography Infusion:** Configured a high-energy artistic typeface stack including `'Permanent Marker'`, `'Nosifer'`, and `'Sedgwick Ave Display'` exclusively mapped to headings (`h1`, `h2`, `h3`, `h4`), establishing a gritty, street-style graffiti visual hierarchy.
* **Main Header Drip Effect:** Refactored the dashboard header to sport an immersive multi-step linear gradient mimicking a paint drip flowing down into deep midnight charcoal:
  ```css
  linear-gradient(180deg, #0D0C16 0%, #0D0C16 70%, #7b2cbf 75%, #00b4d8 83%, #39FF14 91%, #05050A 100%)
  ```
* **Tactile Texture Layering:** Applied a micro-grain noise overlay integrated dynamically via high-performance inline SVG filters combined with dual-tone dark purple backgrounds to provide cards with physical substance:
  ```css
  background-image: url("data:image/svg+xml,..."), linear-gradient(135deg, rgba(13,12,22,0.95), rgba(24,14,48,0.95))
  ```
* **Bouncing Interaction Physics:** Programmed custom micro-animations utilizing spring-like cubic-beziers so buttons rise and cast an electric cyan neon glow (`rgba(0, 180, 216, 0.5)`) on hover, and press down realistically on active click.
* **Consistent Accents:** Integrated focus outlines with high-visibility neon-lime glow (`#39FF14`) and retrofitted custom dual-gradient scrollbars (Violet to Cyan).

#### 2. Dollhouse (Barbie Dreamhouse) Refining
A playful, high-contrast structural overhaul mimicking a physical playset.
* **Background Vignette:** Swapped the flat pastel pink background with a soft fixed gradient utilizing three warm tones:
  ```css
  linear-gradient(135deg, #FFB7C5, #E6E6FA, #FDFD96)
  ```
* **Toy Molding Shadow:** Outfitted card modules with a solid, high-contrast offset 3D shadow block bordered by soft rose-gold lines mimicking physical plastic frames:
  ```css
  box-shadow: 10px 10px 0px 0px #FF9AA2;
  border: 3px solid #D8A7B1;
  ```
* **Miniature Scale Hover:** Programmed a subtle physical "press down" scale transition on buttons to replicate pressing a mechanical toy button:
  ```css
  transform: scale(0.95);
  ```
* **Display Elements:** Playful typographic selections (`Pacifico`, `'Dancing Script'`) applied to top-level headers alongside miniature scale-down click-triggers on hover.

---

## 🛠️ The Tech Stack

* **Frontend:** React, Tailwind CSS, Vite
* **Backend:** Node.js, Express
* **Parsing Intelligence:** Google Gemini API (Gemini 3.5 Flash)
* **Sync Layer:** Copy-to-clipboard TSV Matrix for seamless transition to personal tracking ledgers

---

## ❌ Eliminations & Purges

To preserve high rendering speeds and strict architectural clarity, a complete codebase purge was executed:
* **Purged Static Cards:** Completely deleted all 5 legacy, hardcoded HTML blocks for Google, LinkedIn, Indeed, ZipRecruiter, and Wellfound cards from `DataIngestionCanvas.tsx` to clear out outdated layouts.
* **Eradicated Inline Typography Rules:** Stripped away inconsistent inline header classes throughout individual views, centralizing all custom thematic styling inside target container-scoped selectors within the global stylesheet.
* **Flat Layout Depreciation:** Standard solid color backgrounds within themed views were completely phased out, upgraded uniformly to vibrant gradients, grain textures, and soft vignette offsets.

---

## 📣 Feedback & Iteration

This project is a living tool. Because most platforms lock functionality behind paywalls, this app keeps the utility open and user-driven.

👉 **[Share Feedback Form](https://forms.gle/your-form-link)** — Use this link to help refine the engine, report false negatives, or suggest new anti-spam rules.
