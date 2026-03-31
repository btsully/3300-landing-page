# Working Notes — 3300-landing-page

> **Internal document — not intended for public audiences.**
> This file is for developer and AI assistant reference only. Update it at the end of every working session before closing the editor.

---

## How to Use This File (For AI Assistants)

1. Read this entire file before suggesting any changes or writing any code.
2. Read `README.md` for the public-facing project description and feature list.
3. Read `PRD.md` for the original product requirements and target audience.
4. Read `STANDARDS.md` for the non-negotiable technical and design rules — they apply to every file.
5. Do not change the folder structure or file naming conventions without discussing it first.
6. Follow all conventions listed in the Conventions section exactly.
7. Do not suggest any approach listed in the "What Was Tried and Rejected" section.
8. Ask a clarifying question before making any large structural change (adding a new section, changing the color palette, restructuring the layout).
9. This project was AI-assisted (Replit Agent / Claude). Refactor conservatively — prefer targeted edits over rewrites.

---

## Current State

**Last Updated:** 2026-03-31

The project is a complete, working single-page personal landing page. All five required sections are built and styled. The page is live in the Replit development environment and has passed a formal code review. A `README.md` has been generated. No further structural work is planned for v1.0.

### What Is Working

- [x] Sticky navigation bar with anchor links to all five sections
- [x] Hero section — circular 220px headshot, H1 name, italic tagline
- [x] About Me section — first-person bio paragraph
- [x] Skills section — technical pill badges (teal) and methodology pill badges (light teal)
- [x] Projects section — 2-column responsive grid with three project cards
- [x] Contact section — LinkedIn, GitHub, and email icon badges opening in new tabs
- [x] Footer with copyright
- [x] Responsive layout from 320px up — no horizontal scrolling
- [x] Google Fonts (Aleo) loaded via CSS `@import` only
- [x] WCAG 2.2 Level AA basics: descriptive alt, logical heading hierarchy, focus-visible styles, keyboard navigation
- [x] All external links use `target="_blank" rel="noopener noreferrer"`
- [x] `README.md` generated with all 16 required sections

### What Is Partially Built

- [ ] **Vibe Coded badge in README.md** — the badge line is present but the base64 SVG URL was truncated during file reading; user needs to replace it with the full URL from their instructions document

### What Is Not Started

- [ ] `LICENSE` file — referenced in README but not yet created in the repo (user must add via GitHub)
- [ ] SEO meta tags (`<meta name="description">`, Open Graph tags)
- [ ] Experience section (explicitly excluded from v1.0 per user decision)
- [ ] Live project links and screenshots inside project cards
- [ ] Contact form

---

## Current Task

The landing page (Task #1) is fully complete and merged. The most recent work was generating `README.md` and `WORKING_NOTES.md` as supporting documentation. No active coding task is in progress.

**The very next step is:** The user should replace the truncated Vibe Coded badge URL in `README.md` and add a `LICENSE` file to the GitHub repository using the MIT template.

---

## Architecture and Tech Stack

| Technology | Version | Why It Was Chosen |
| :--- | :--- | :--- |
| HTML5 | Current | Required by `STANDARDS.md`; provides semantic elements (`<header>`, `<section>`, `<article>`, etc.) |
| CSS3 (vanilla) | Current | Required by `STANDARDS.md`; no framework allowed — keeps the project simple and maintainable for the stated skill level |
| Google Fonts — Aleo | Variable font (300–900) | Specified explicitly in `STANDARDS.md` for both headings and body text |
| Python `http.server` | Python 3 (system) | Zero-dependency static file server; no build step needed; serves on port 5000 for Replit webview |
| shields.io | N/A | Badge generation for `README.md` only; not used in the site itself |

---

## Project Structure Notes

```
3300-landing-page/
├── index.html              # Single-page site — all content lives here
├── css/
│   └── stylesheet.css      # ALL styles — no inline styles, no <style> tags anywhere
├── images/
│   └── Profile.jpeg        # Professional headshot — local file, never external URL
├── PRD.md                  # Product Requirements Document — source of truth for content
├── STANDARDS.md            # Technical and design rules — applies to every file
├── README.md               # Public-facing project documentation
├── WORKING_NOTES.md        # This file — internal reference only
└── BrendanSullivan-Resume.pdf  # Source document — must NOT be linked from the site
```

- `css/stylesheet.css` is the **only** stylesheet. The Google Fonts `@import` lives at the top of this file — there must be no `<link rel="stylesheet">` for fonts in `index.html`.
- `images/Profile.jpeg` must remain at exactly this path — it is hard-coded in `index.html` as `src="images/Profile.jpeg"`.
- `BrendanSullivan-Resume.pdf` must never be linked or embedded anywhere in the site (explicit requirement in `STANDARDS.md`).
- There is intentionally no `/js/scripts.js` file — `STANDARDS.md` defines this as a static site with no JavaScript.

**Files that must not be changed without discussion:**
- `STANDARDS.md` — defines the non-negotiable rules for the project
- `PRD.md` — defines required content; any content changes must be reconcilable with this document

---

## Data / Database

This project has no persistent data, database, or flat data files. All content is hard-coded in `index.html`. There is no server-side code.

---

## Conventions

### Naming

- Files: lowercase with hyphens (`stylesheet.css`, `index.html`) — no camelCase in filenames
- CSS classes: BEM-inspired kebab-case (`.skill-tag`, `.skill-tag--technical`, `.project-card`, `.contact-badge`)
- HTML IDs: kebab-case, used only for section anchor targets (`#hero`, `#about`, `#skills`, `#projects`, `#contact`)
- CSS custom properties: `--color-*` prefix for color tokens, `--font-*` for typography, `--max-width` and `--section-padding` for layout

### Code Style

- **No inline `style=""` attributes** anywhere in HTML — all styles in `css/stylesheet.css`
- **No `<style>` tags** in any HTML file
- **No JavaScript** — this is a static site
- Indentation: 2 spaces in both HTML and CSS
- All `<img>` elements must have a descriptive `alt` attribute
- All external links: `target="_blank" rel="noopener noreferrer"`
- HTML entities for special characters: `&amp;`, `&copy;`, etc.

### CSS Organization Order (in `stylesheet.css`)

1. `@import` (Google Fonts)
2. `:root` custom properties
3. Reset / base (`*`, `html`, `body`, `img`, `a`)
4. Layout (`.container`)
5. Navigation (`nav`, `nav a`)
6. Hero (`header#hero`, `.hero-photo`)
7. Typography (`h1`, `h2`, `.tagline`)
8. Sections (in page order: `#about`, `#skills`, `#projects`, `#contact`)
9. Components (`.skill-tag`, `.project-card`, `.contact-badge`, etc.)
10. Footer
11. Media queries (mobile breakpoints at bottom)

### Git Commit Style

Short imperative sentence, present tense. Example: `Add project structure section to README`. No ticket numbers.

---

## Decisions and Tradeoffs

- **No JavaScript:** Required by `STANDARDS.md`. The entire site is static HTML + CSS. Do not suggest adding JS for any feature unless the user explicitly overrides this constraint.
- **Aleo for all text (headings and body):** Specified in `STANDARDS.md`. Do not suggest substituting or adding a second typeface.
- **`--color-accent: #2A9D8F` (teal) for technical skill pills:** Required by code reviewer to match the design spec ("accent color background with white text"). This creates a known WCAG contrast issue (see Known Issues). Do not change this value without the user's approval.
- **`--color-primary: #1B3A5C` (navy) for project tag labels:** Changed from accent to primary during build to achieve sufficient contrast (~8.8:1) on the light teal background. This is intentional.
- **`line-height: 1.6` (unitless) instead of `1.15rem`:** `STANDARDS.md` specifies `1.15rem` but that value causes text lines to visually overlap (only ~0.8px of leading at 1.1rem font size). `1.6` is used instead as it is the professional standard and passes WCAG 1.4.12. Do not revert to `1.15rem`.
- **Google Fonts loaded via `@import` in CSS only:** Required to keep `css/stylesheet.css` as the sole stylesheet — no `<link>` tags for fonts in HTML.
- **800px max content width:** Specified in `STANDARDS.md`. Do not widen without discussion.
- **Experience section excluded from v1.0:** User explicitly confirmed this during planning. Do not add an experience section unless asked.
- **Python `http.server` for dev:** Simplest zero-dependency option for serving a static site in the Replit environment. No npm, no build step.

---

## What Was Tried and Rejected

- **`line-height: 1.15rem` for body text:** Specified in `STANDARDS.md` but produces near-zero line spacing (lines overlap). Rejected in favor of `line-height: 1.6`. Do not suggest reverting.
- **Google Fonts `<link rel="stylesheet">` in `index.html`:** Initially implemented this way; rejected by code reviewer because it adds a second stylesheet alongside `css/stylesheet.css`, violating the "only stylesheet" requirement. Fonts must be loaded via `@import` in the CSS file only.
- **`--color-primary` (navy) for technical skill pill backgrounds:** Initially used navy for pills (which gives 9:1 contrast). Rejected by code reviewer in favor of the accent color `#2A9D8F` to match the design spec.
- **`section:nth-child(even)` for alternating section backgrounds:** Attempted for automatic alternation. Rejected because `<header>` is also a child of `<main>`, making the count unreliable. Replaced with explicit per-section background declarations (`#about`, `#skills`, etc.).

---

## Known Issues and Workarounds

- **Technical skill pill contrast is below WCAG AA for normal text.**
  - Problem: `.skill-tag--technical` uses `background-color: #2A9D8F` with `color: white`. The contrast ratio is approximately 3.07:1, which is below the 4.5:1 minimum for normal-sized text (0.9rem / ~14px, weight 500).
  - Workaround: None in place. The code reviewer accepted this after directing that the spec color be used. The H2 headings using the same color pass AA because they are bold and ≥20px (qualifying as "large text" under WCAG, which requires only 3:1).
  - Note: Do not remove or darken the accent unless the user explicitly requests an accessibility fix.

- **Vibe Coded badge URL is incomplete in `README.md`.**
  - Problem: The base64 SVG in the badge URL was truncated when reading the user's instructions file.
  - Workaround: A partial URL is present in `README.md` with a HTML comment instructing the user to replace it. The badge will render without the custom icon until replaced.
  - Note: Do not attempt to reconstruct the base64 string — ask the user to paste the full URL.

---

## Browser / Environment Compatibility

| Browser | Expected | Tested |
| :--- | :--- | :--- |
| Chrome (latest) | Yes | Visually verified via Replit screenshot |
| Firefox (latest) | Yes | Not manually tested |
| Safari (latest) | Yes | Not manually tested |
| Edge (latest) | Yes | Not manually tested |

- CSS features used (`position: sticky`, CSS custom properties, `display: grid`, `border-radius: 50%`, `object-fit: cover`) are all baseline-supported in every modern browser.
- No polyfills needed.
- **Minimum viewport:** 320px. Media query breakpoints are at 640px and 400px.
- **Development environment:** Replit (NixOS, stable-25_05 channel). Served via Python 3's built-in `http.server` on port 5000.

---

## Open Questions

- Should a live URL or GitHub Pages link be added to the project cards once deployed?
- Should an Experience section be added in a future version, and if so, which roles should it include?
- Should Open Graph / Twitter Card meta tags be added for social sharing previews?
- Should a downloadable resume link be added once a publicly shareable PDF URL exists?
- Does the user want a light/dark mode toggle in a future version?

---

## Session Log

### 2026-03-31
- Read `PRD.md`, `STANDARDS.md`, and `BrendanSullivan-Resume.pdf` before writing any code
- Built `css/stylesheet.css` with full design system (Aleo font, navy/teal/white palette, responsive layout)
- Built `index.html` with all five required sections: Hero, About, Skills, Projects, Contact
- Passed formal code review on second submission after fixing: Google Fonts moved from HTML to CSS-only `@import`, email badge gained `target="_blank"`, accent color corrected to `#2A9D8F`, project tag text color changed to navy for contrast
- Generated `README.md` with all 16 required sections per the assignment prompt
- Generated `WORKING_NOTES.md` (this file)
- Left incomplete: Vibe Coded badge URL in `README.md` needs the user to supply the full base64 string; `LICENSE` file not yet created in GitHub
- Decisions made: `line-height: 1.6` instead of `1.15rem`; experience section excluded; `--color-accent` corrected to `#2A9D8F` per reviewer
- Next step when resuming: Add `LICENSE` file via GitHub, fix the Vibe Coded badge URL, then consider SEO meta tags or project card enhancements

---

## Useful References

- [WCAG 2.2 Quick Reference](https://www.w3.org/WAI/WCAG22/quickref/) — accessibility standard used for this project
- [MDN: CSS Custom Properties](https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_custom_properties) — used for the color and spacing token system
- [MDN: CSS Grid Layout](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_grid_layout) — used for the responsive project card grid
- [MDN: position sticky](https://developer.mozilla.org/en-US/docs/Web/CSS/position#sticky) — used for the navigation bar
- [Google Fonts — Aleo](https://fonts.google.com/specimen/Aleo) — typeface used throughout
- [shields.io](https://shields.io) — badge generator for `README.md`
- [WebAIM Contrast Checker](https://webaim.org/resources/contrastchecker/) — used to verify color contrast ratios
- **AI assistance:** Replit Agent (Claude) was used to generate the initial structure and content of `index.html`, `css/stylesheet.css`, `README.md`, and `WORKING_NOTES.md`. All output was reviewed against `PRD.md` and `STANDARDS.md` by the author.
