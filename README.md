![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat)
<!-- Replace the URL below with the full Vibe Coded badge URL from your instructions document -->
![Vibe Coded badge](https://img.shields.io/static/v1?message=Vibe%20Coded&labelColor=5c5c5c&color=7c3aed&logoColor=white&label=%20&style=for-the-badge)

# Brendan Sullivan — Personal Landing Page

*Replace this heading with your project name if reusing as a template.*

A single-page personal landing page built for BAIS:3300 — Digital Product Management at the University of Iowa. The page presents Brendan Sullivan's academic background, technical skills, and key projects to hiring managers and recruiters targeting Corporate Financial Analyst roles in B2B solutions, manufacturing, tech, and healthcare. It is designed to complement a resume by demonstrating the ability to communicate insights professionally.

---

## Features

*List what the site does from a visitor's perspective.*

- Professional hero section with circular headshot, name, and tagline
- About section written in first-person with academic and career context
- Skill badges organized into Technical and Methodology categories
- Project cards for three featured works, displayed in a responsive two-column grid
- Labeled contact badges for LinkedIn, GitHub, and email
- Sticky top navigation bar with smooth-scroll anchor links
- Fully responsive layout — works on screens 320 px and wider
- Accessible design following WCAG 2.2 Level AA guidelines

---

## Tech Stack

*Update this table if you add or remove any tool.*

| Technology | Purpose |
| :--- | :--- |
| HTML5 | Page structure and semantic markup |
| CSS3 (vanilla) | All styling and responsive layout — no frameworks |
| Google Fonts — Aleo | Typography for headings and body text |
| shields.io | Badges in this README |
| Python 3 (`http.server`) | Local development server |

---

## Getting Started

### Prerequisites

*Everything a developer needs before running the project locally.*

- [Python 3](https://www.python.org/downloads/) (for the local dev server) — or any static file server of your choice
- A modern web browser (Chrome, Firefox, Safari, or Edge)
- [Git](https://git-scm.com/) to clone the repository

### Installation

*Steps to get the project running on your machine.*

1. Clone the repository:

```bash
git clone https://github.com/btsully/3300-landing-page.git
cd 3300-landing-page
```

2. Start a local development server using Python:

```bash
python3 -m http.server 5000
```

3. Open your browser and navigate to:

```
http://localhost:5000
```

The site will load directly — no build step or package installation required.

---

## Usage

*How to view and interact with the page once it is running.*

Open `http://localhost:5000` in your browser. Use the sticky navigation bar at the top to jump to any section: About, Skills, Projects, or Contact. The contact badges link to LinkedIn and GitHub (both open in a new tab) and trigger your email client for the email link. The layout adapts automatically for mobile, tablet, and desktop viewports — no configuration needed.

To customize content, edit `index.html` directly. To change colors, fonts, or layout, edit `css/stylesheet.css`. All design tokens are defined as CSS custom properties at the top of the stylesheet for easy updates.

---

## Project Structure

```
3300-landing-page/
├── index.html          # Single-page site — all five sections live here
├── css/
│   └── stylesheet.css  # All styles; Google Fonts imported via @import
├── images/
│   └── Profile.jpeg    # Professional headshot (local, not externally linked)
├── PRD.md              # Product Requirements Document
├── STANDARDS.md        # Technical and design standards for this project
├── README.md           # This file
└── BrendanSullivan-Resume.pdf  # Source document (not linked from the site)
```

---

## Changelog

*Add a new entry each time you release a meaningful update.*

### v1.0.0 — 2026-03-31

Initial release.

- Hero section with circular headshot, H1 name, and professional tagline
- About Me section with first-person bio
- Skills section with pill badges for technical and methodology skills
- Projects section with three cards in a responsive two-column grid
- Contact section with LinkedIn, GitHub, and email badges
- Sticky navigation bar with anchor links
- Fully responsive from 320 px up
- WCAG 2.2 Level AA accessibility: descriptive alt text, logical heading hierarchy, focus-visible styles, keyboard-navigable links
- Deployed as a static site

---

## Known Issues / To-Do

*Check these off or update them as you work on future versions.*

- [ ] Skill pill contrast: the teal accent (`#2A9D8F`) on white text yields ~3.1:1, below the 4.5:1 WCAG AA threshold for normal-sized text — consider darkening the accent or increasing pill font size
- [ ] No `LICENSE` file is present in the repository yet — add an MIT License file via GitHub
- [ ] The Projects section does not include live links or screenshots for the Grocery Helper and Bloomberg Market Concepts entries
- [ ] The page has no `<meta name="description">` tag for SEO
- [ ] Contact form not implemented — currently links to external profiles only

---

## Roadmap

*Planned features for a hypothetical future version.*

- Add an Experience section surfacing internship and work history once more roles are completed
- Include live project links and screenshots inside each project card
- Add a downloadable resume button (once a publicly shareable PDF is available)
- Integrate a simple contact form using a service such as Formspree — no back-end required
- Add Open Graph meta tags so the page previews correctly when shared on LinkedIn and other platforms

---

## Contributing

*Follow these steps to suggest improvements to this project.*

This is a personal portfolio project, but constructive feedback and suggestions are welcome. To propose a change:

1. Fork the repository on GitHub.
2. Create a new branch for your change: `git checkout -b your-branch-name`
3. Make your edits to `index.html` or `css/stylesheet.css`.
4. Commit with a clear message: `git commit -m "Brief description of change"`
5. Push to your fork: `git push origin your-branch-name`
6. Open a pull request against the `main` branch and describe what you changed and why.

Please keep all changes consistent with the design and technical standards defined in `STANDARDS.md`.

---

## License

This project is licensed under the [MIT License](LICENSE).

---

## Author

*Update this section if reusing this template.*

**Brendan Sullivan**
University of Iowa — Tippie College of Business
Course: BAIS:3300 — Digital Product Management

---

## Contact

- GitHub: [@btsully](https://github.com/btsully)

---

## Acknowledgements

*Credit any resources, tools, or people that helped you build this.*

- [Google Fonts — Aleo](https://fonts.google.com/specimen/Aleo) — typography used throughout the site
- [shields.io](https://shields.io) — badge generation for this README
- [MDN Web Docs](https://developer.mozilla.org) — HTML5 and CSS3 reference throughout development
- [WCAG 2.2 Guidelines](https://www.w3.org/TR/WCAG22/) — accessibility standards reference
- AI assistant (Replit Agent / Claude) — initial code structure generated with AI assistance and reviewed, tested, and modified by the author
- Icon: [vibe coding](https://thenounproject.com) by iqonica from [Noun Project](https://thenounproject.com) (CC BY 3.0)
