# Job Tracker & Search Shield (My Job Search Guard)

Asynchronous, Zero-Noise Market Gatekeeper & Priority Pipeline
**Live Application Link:** [Launch Job Search Guard](https://lookerstudio.google.com/reporting/your-unique-id-string/copy)
**Status:** Live Production | Monitored via continuous user-ingestion validation

***

## 🧐 Why I Built This: The Anti-Noise Approach

When I started this project, job searching felt like drowning in noise. LinkedIn felt like a social media trap, and Indeed was littered with predatory job postings that did not exist. Currently, I use vague search terms on LinkedIn and Indeed for job searches. It becomes time consuming because I get wrapped in the social networking and necessity of LinkedIn. Indeed is becoming less trustworthy when there are often AI farming jobs where a job is advertised but does not really exist, or information is given to third party hiring managers.

I built this because the entry-level search landscape is highly oversaturated with misleading listings. It is incredibly hard to balance your immediate operational needs with what is actually a strategic investment for your future career. Having a parser helps because let us be real: job boards use AI, so why not have AI give you back the summary? 

***

## 🧹 Product Positioning & State Architecture

Unlike legacy career platforms that thrive on endless scrolling, visual clutter, and data harvesting loops, this system acts as a defensive framework for technical professionals. It shifts the workflow from reactive browsing into an isolated, variable-driven dashboard designed to level the algorithmic playing field.

This application is completely plug-and-play and available to use immediately upon launch. Users no longer need to deploy a code block on their own or manually configure a backend template. Anyone can open the published application interface, input their target parameters straight into the UI sidebars, and run a production-ready search immediately.

***

## 👩🏻‍💻 How It Works

### 1. Zero-Friction Input & Parameter Locking
Users interact purely with a clean, client-side dashboard interface. The application isolates parameters within absolute boundary rules:
*   **Built for Quick Adjustments:** The filter parameters live in the visual interface, meaning users can swap out core targets, modify distance rules, or adjust the salary floor in seconds without breaking the system logic.
*   **70% Semantic Match Recommendation Engine:** To break users out of the trap of searching the same two or three keywords, the system runs an alternate job title recommendation generator. It analyzes your target profile and automatically maps comparable positions based on a 70% or higher semantic accuracy overlap, uncovering valuable adjacent roles.

### 2. Multi-Theme Customization
To keep your daily workflow engaging during an active search, the workspace layout is fully interactive and customizable via real-time theme toggles:
*   **Minimal:** A clean, zero-distraction framework using a gray, white, and black base accented by crisp red highlights.
*   **Cyber (Default):** A highly distinct, terminal-style security workspace running custom Data Stream Matrix tokens (`#0b0f16` deep bases, `#151a24` cards, `#00e5ff` neon highlights, and `#00c896` secondary accents) utilizing a 'PT Mono' typography layer for maximum aesthetic separation from the minimal mode.
*   **Dollhouse:** A highly styled interface variant utilizing playful palette choices reminiscent of a classic toy dreamhouse.
*   **Paint Splatter:** An expressive style profile channeling a mid-2010s colorful, high-contrast grunge motif.

### 3. Career Mapping Rules & Automated Bridge
*   **Noise Minimization:** The system automatically drops highly specific or bureaucratic titles from the results layout if they yield zero viable data matching your targets.
*   **Technical Bridging:** If an entry-level position fits the experience threshold but directly aligns with your multi-year Data Engineer goal (such as Analytics Engineering or Data Integration roles), the engine automatically includes it with a clean, single-sentence breakdown explaining how it acts as a pipeline bridge.

***

## 🚧 App Limits & Privacy Boundaries

To bypass expensive paywalls, eliminate tracking cookies, and protect your private data, three strict gatekeeping rules are hardcoded into the pipeline:
*   **Strict Quality & Source Limits:** The engine acts as an explicit security gatekeeper. It completely screens out third-party IT staffing agencies, recruiting firms, and predatory placement mills. If a listing originates from a sourcing pipeline or placement network (like Robert Half or CyberCoders), or demands upfront training fees, it is instantly omitted.
*   **Hard Experience Caps:** The system runs a ruthless evaluation scan on the fine print. Any position demanding more than 1 year of experience is immediately thrown out, ensuring you only evaluate true entry-level benchmarks.
*   **Live Web Grounding:** The architecture leverages live public web searches grounded directly into LinkedIn, Indeed, BuiltIn Boston, and Dice. It uses specialized site-scoping syntax to pull real-time data while bypassing background scraping loops that compromise your local environment.

***

## ☰ The Tech Stack

*   **Where It Lives:** Deployed completely within structured markdown system environments, allowing anyone to instantly fork, paste, and run the configuration natively.
*   **The Parsing Engine:** Powered by Google AI Studio, utilizing isolated rule schemas that map raw text blocks into uniform reporting variables without needing natural language conversational context.
*   **The Sync Layer:** Formatted with a direct Google Sheets and Excel output layout matrix (`Copy Sheets-Ready TSV`), enabling swift data transition back into personal tracking ledgers.

***

## 🗪 What's Next (The Feedback & Iteration Plan)

This project is built to be a living tool that anyone can launch, customize, and use to protect their job search in real-time. Because most platforms lock their functionality behind paywalls, this app keeps the utility open and directly driven by user input.
*   **User Profile Profiles:** Expanding the local state storage so users can save and toggle between multiple distinct search profiles without losing their active funnel analytics.
*   **Active Response Funnel:** Includes a dedicated **Share Feedback Form** button pinned directly to the top header of the application interface. This links to an automated response tracking dashboard, allowing the platform to be continuously refined, patched, and optimized based on real-world user feedback.
