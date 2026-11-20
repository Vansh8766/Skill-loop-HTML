# SkillLoop — Student Skill Exchange & Peer Tutoring Marketplace

**CSE326 Web Development Project | HTML + CSS + Vanilla JavaScript**

SkillLoop is a responsive, browser-based demonstration of a student-to-student tutoring marketplace. Students can discover peers with skills they want to learn, browse profiles, set learning interests and availability, and create simulated tutoring requests.

![Tech](https://img.shields.io/badge/HTML-CSS%20%7C%20JavaScript-6555df)

## Features

- Responsive landing page with curated student mentor profiles
- Search peers by name, course, subject or skill
- Filter by skill category and availability
- Peer profile details, skills offered, and skills wanted
- Editable student profile, including interests and availability
- Session request form with subject, date, time and message
- Sent request tracking with demo acceptance, cancellation and completion
- Sessions screen for accepted and completed sessions
- A basic credit system: start with 5, spend 1 when requesting a session and earn 2 when completing a session (demo simulation)
- Local browser persistence using `localStorage`
- Optional demo-only admin activity summary

## Tech stack

- HTML5 — page structure
- CSS3 — responsive layout and styling
- JavaScript (ES6+) — interactive app logic and browser storage
- Google Fonts (optional external fonts; fallback fonts work offline)

**No frameworks, packages, build tools, or backend are required.**

## Project structure

```text
skillloop-project/
├── index.html          # Layout and forms
├── styles.css          # Styling and responsiveness
├── script.js           # Data, matching, requests, storage and interactions
├── README.md           # Project guide
├── .gitignore          # Git exclusions
└── LICENSE             # MIT license
```

## Running locally

1. Download or clone this repository.
2. Open `index.html` in Chrome, Edge, or Firefox.
3. Alternatively, in VS Code, use the Live Server extension and open `index.html`.
4. Explore peers, create/edit your profile and send session requests.

No `npm install` or API keys are needed.

## How to use

1. **Discover:** use the search bar, category chips or availability dropdown.
2. **View profiles:** select **Profile** on any mentor card.
3. **Request a session:** select **Connect**, choose a skill, date and time, and submit.
4. **Requests:** open **My requests** and choose **Simulate accept**. Real students cannot receive requests in this frontend-only version.
5. **Sessions:** view accepted sessions and mark them completed to earn demo credits.
6. **Profile:** edit your name, course, skills you can teach, skills you want to learn and your availability.
7. **Demo admin:** visit `index.html?admin=demo#admin` (or the equivalent deployed URL). This is a convenience-only display, **not authentication or a secure admin feature**.

## Hosting on GitHub Pages

1. Create a public GitHub repository, for example `skillloop-cse326`.
2. Upload `index.html`, `styles.css`, `script.js`, `README.md`, `.gitignore` and `LICENSE` to the **root** of the repository.
3. Navigate to repository **Settings → Pages**.
4. Under **Build and deployment**, select **Deploy from a branch**.
5. Choose branch **main** and folder **/(root)**, then **Save**.
6. Open the GitHub Pages URL shown under Pages after it is deployed.

Git command alternative:

```bash
git init
git add .
git commit -m "Build SkillLoop CSE326 frontend"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/skillloop-cse326.git
git push -u origin main
```

> Create the empty GitHub repository before running the last two commands, and replace `YOUR_USERNAME` with your GitHub username.

## Important limitations

This project meets the **HTML/CSS/JavaScript-only** constraint by using static sample profiles and `localStorage`. It is a **single-browser demonstration**, not a real shared marketplace:

- No real accounts or login/authentication
- No shared database or real-time peer-to-peer requests
- No delivery of notifications to other users
- No secured administrator account or permissions
- No server-side scheduling or payment/credit integrity
- Sample mentor ratings are static display data, not user-submitted reviews

For a real multi-user app, a backend, database, authentication, server-side role checks and consent/privacy controls would be required.

## Testing checklist

- [ ] Open the homepage and view nine profiles.
- [ ] Search for `Python` and verify matching profiles remain.
- [ ] Filter to `Programming` and `Weekends`.
- [ ] Reset all filters.
- [ ] Save a new profile and refresh the page; changes should remain.
- [ ] Send a session request, then find it in My requests.
- [ ] Simulate acceptance and confirm it appears under Sessions.
- [ ] Mark it completed and confirm your demo credits increase.
- [ ] Check layouts on both phone and desktop.

## Credits

Demo student names and biographies are fictional. The layout and implementation were prepared for an educational student project. You may customize sample content and styling for your submission.


## New: Official Course Discovery

Open **Free courses ✦** in the top navigation to explore curated links to official learning providers. This section uses only browser JavaScript and contains:

- Search by subject, topic, or provider (e.g. Python, JavaScript, design, cybersecurity).
- Filters for subjects and providers.
- **Recommend for me**: matches predefined resource topics against the **Skills I want to learn** list on your profile.
- Clickable interest chips from your profile.
- Save/unsave resource bookmarks in existing browser localStorage.
- Official portal links that open in a new tab.
- Responsive layout, empty states and transparent pricing/certificate disclaimers.

**Important:** This is a curated resource directory, not a live provider API, AI recommender or real-time price/enrollment checker. Several links point to official searchable catalogs rather than a specific class. Individual course enrollment, certification fees and availability can change. NPTEL/SWAYAM courses generally allow free learning, but certification exams can cost extra. Other catalogs may contain courses with varying pricing. Always verify the final offer on the official portal.

### To add a new resource

Edit `COURSE_CATALOG` in `script.js`. Each entry has an ID, title, provider, category, search topics, official URL, type, cost description, note and icon. Only link to URLs you have verified. To change matching behavior, edit `courseScore()` and `topicMatch()`. No external packages are required.


## Collaboration Hub: teammates and hackathons

- **Find teammates** (`#teammates`): filter sample student collaborators by name, skill, role and availability; rank matches using your profile's learning and teaching skills; shortlist up to five teammates; copy a team plan or a personalized invitation draft.
- **Find hackathons** (`#hackathons`): search and filter a curated collection of official event directories (Devfolio, Unstop, Devpost, MLH and Hack Club), open the official event pages and bookmark useful platforms.
- All functionality uses **vanilla HTML, CSS and JavaScript**, with saved preferences in browser `localStorage`.

### Important demo limitations

The student profiles are fictional seed data. Shortlisting does not send invitations; invitation text is copied or shown for manual sharing. Hackathon listings are **platform directories**, not a live feed of currently open events. Verify dates, eligibility, fees, team-size restrictions and application deadlines on each official website. To support actual student accounts, cross-device persistence, team messages, or live event listings, a backend and/or a supported API would be required.
