# STANDARDS.md

## BAIS:3300 - Digital Product Management · Module 8 | Personal Landing Page Project

_This file contains technical instructions for this project. Every time you
begin a coding session, ask your LLM to read this file before writing any code.
The LLM will follow these standards automatically without you needing to repeat
them in every prompt._

_To start a session, paste this into your LLM:_
_"Please read my STANDARDS.md file before we begin. I will be asking you to build
and modify my personal landing page."_

---

## 1. Project Overview

- Brendan Sullivan is a double major in Finance and Business Analytics & Information Systems at the University of Iowa, graduating in May 2026. While his resume highlights strong technical skills, it does not fully demonstrate his ability to communicate and present insights to others. This landing page solves that by providing a professional space to showcase his personality and motivation, specifically targeting Financial Analyst roles within the manufacturing, tech, and healthcare industries. The primary audience includes hiring managers and recruiters at companies of all sizes within the target industries. These visitors are looking for a candidate who is not only technically proficient but also professional and highly motivated. The page aims to make them feel his strong work ethic the moment they arrive.
---

## 2. Technical Standards

These rules apply to every file in this project without exception.

**Languages and versions:**

- HTML5 — use semantic elements throughout: `<header>`, `<main>`, `<section>`,
  `<article>`, `<footer>`, `<nav>`
- CSS3 — all styles must be written in `css/stylesheet.css`; no inline `style=""`
  attributes; no `<style>` tags in any HTML file
- HTML5 and CSS3 code must pass validation

**Folder structure:**

<pre>
/your-website-project (Root Folder)  
├── index.html  
├── /css  
│    └── stylesheet.css  
├── /js  
│    └── scripts.js  
├── /images  
│    └── Profile.jpeg
</pre>

**Framework:**

- No framework — vanilla CSS only

**Architecture:**

- Static site — no JavaScript, no server-side code, no database, no back-end
- Single `index.html` file in the project root
- External stylesheet: `css/stylesheet.css` in the css folder and referenced by relative path
- All images stored in the `images/` subfolder and referenced by relative path
  (e.g., `src="images/Profile.jpeg"`) — never link to external image URLs
- Do not link to or embed my resume anywhere on the site

**Responsiveness:**

- Fully responsive at all screen widths from 320px and wider
- No horizontal scrolling on any viewport

**Accessibility — WCAG 2.2 Level AA (non-negotiable):**

- All `<img>` elements must have a descriptive `alt` attribute
- Color contrast ratio: minimum 4.5:1 for normal text, 3:1 for large text
- Heading hierarchy must be logical: `<h1>` → `<h2>` → `<h3>`, no levels skipped
- All link text must be descriptive — no "click here", "read more", or bare URLs
- Page `<title>` element must be descriptive (not "Untitled" or "index")
- All interactive elements (links, buttons) must be keyboard navigable

**Compatibility:**

- Must render correctly on Chrome, Safari, Edge, and Firefox; must be mobile-responsive (works on screens 375px and wider)

## **Security:**

- Links to external sites should open in a new tab (`target="_blank"` with `rel="noopener noreferrer"`)

---

## 3. Design Standards

These visual rules apply to the entire site. Claude must follow them on every
build and every revision.

**Color palette:**

Shades of blue / green / white. Clean and modern, not flashy.

**Typography:**

- Heading font: Aleo — import from Google Fonts
- Body font: Aleo
- Body size: 1.1rem, line height: 1.15rem
- H1 (page name): 1.5rem, bold
- H2 (section headings): 1.25rem, bold, accent color

**Imagery:** Professional headshot only. No stock photos or clip art. No emojis.

**Layout:**

- Maximum content width: [800px], centered on the page
- Navigation: sticky top bar with anchor links to each section
- Section spacing: 60px top and bottom padding on each section
- Single column on mobile, two-column on desktop for project cards. Generous whitespace.

**Component styles:**

_Profile photo:_

- Circular crop, 220px diameter, centered in the hero section

_Skill tags:_

- Rounded pill badges — accent color background with white text for
  technical skills; secondary background with dark text for professional skills

_Contact links:_

- Display as labeled icon badges opening in a new tab; include LinkedIn,
  GitHub, and email

_Navigation links:_

- Plain text links, accent color on hover, no underline by default

**Tone:**

- **Three words that describe the desired feel:** 
- Professional, Approachable, Data-driven
- Clean and minimal. Professional but approachable. Not a corporate brochure, not a creative portfolio.

- **Writing tone:** First person, direct, and confident. Avoid buzzwords like 'passionate' or 'synergy.'

_Remember: this document is a living artifact. Update it as you learn more._
