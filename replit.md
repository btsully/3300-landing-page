# 3300-landing-page — Brendan Sullivan Personal Landing Page

## Project Overview
A single-page personal landing page for Brendan Sullivan, a double major in Finance and Business Analytics & Information Systems at the University of Iowa (graduating May 2026). Targets hiring managers and recruiters for Corporate Financial Analyst roles in B2B solutions, manufacturing, tech, and healthcare.

## File Structure
```
/
├── index.html              # Single-page site (all five sections)
├── css/
│   └── stylesheet.css      # All styles — no inline styles anywhere
├── images/
│   └── Profile.jpeg        # Professional headshot
├── PRD.md                  # Product Requirements Document
├── STANDARDS.md            # Technical and design standards
└── BrendanSullivan-Resume.pdf
```

## Sections
1. **Hero** — Circular headshot (220px), name, professional tagline, sticky nav above
2. **About Me** — Bio paragraph with academic status, double major, graduation, career focus
3. **Skills** — Technical skill pills (navy bg / white text) + Methodology pills (light teal bg / navy text)
4. **Projects** — 2-column grid on desktop, 1-column on mobile: Siemens Dashboard, Grocery Helper, Bloomberg Market Concepts
5. **Contact** — LinkedIn, GitHub, and Email icon badges (all open in new tabs where appropriate)

## Design System
- **Font:** Aleo (Google Fonts) — headings and body
- **Colors:** Navy `#1B3A5C` (primary), Dark Teal `#1B6B5E` (accent / H2), Light Teal `#E2F0EE` (pill bg), `#F4F7F9` (alt section bg)
- **Max content width:** 800px centered
- **Section padding:** 60px top and bottom

## Standards
- Pure HTML5 + CSS3, vanilla — no JS, no frameworks, no inline styles
- WCAG 2.2 Level AA: descriptive alt text, logical heading hierarchy (h1→h2→h3), 4.5:1+ contrast ratios, keyboard-navigable links
- Fully responsive from 320px up, no horizontal scroll
- All external links use `target="_blank" rel="noopener noreferrer"`

## Running the App
Served via Python's built-in HTTP server on port 5000.

- **Workflow**: "Start application" — `python3 -m http.server 5000`
- **Port**: 5000 (webview)

## Deployment
- **Type**: Static site
- **Public directory**: `.` (project root)
