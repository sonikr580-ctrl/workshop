# Workshop Management System (WorkshopHub)
**B.Tech Computer Science & Engineering — Web Technologies Project**  
*A Modern, Professional SaaS Frontend Administrative Portal built exclusively with Semantic HTML5 and CSS3.*

---

## 1. Project Overview

The **Workshop Management System** is an enterprise-grade administrative web interface engineered to streamline, schedule, track, and monitor academic and industrial technical workshops. 

Traditionally, academic institutions rely on disconnected spreadsheets, paper rosters, and informal messaging channels. This creates chronic inefficiencies:
* Accidental double-booking of high-demand laboratory spaces and computer labs.
* Difficulty tracking participant registration caps, fee clearances, and attendance rosters.
* Lack of real-time visibility into specialized laboratory hardware custody (e.g., microcontrollers, single-board computers, projectors).
* Slow manual approval chains for workshop proposals and equipment requisitions.

**WorkshopHub** delivers a centralized, unified portal designed following modern SaaS design aesthetics (resembling professional tools like Linear, GitHub Enterprise, and Stripe Dashboard) while remaining strictly compliant with academic technology constraints.

---

## 2. Technology Stack & Strict Restrictions

This project strictly adheres to **zero-JavaScript** and **zero-framework** guidelines:

| Permitted Technologies | Prohibited Technologies (Strictly Not Used) |
| :--- | :--- |
| **HTML5** (Living Standard semantic elements) | **JavaScript** (No vanilla JS, no Node.js, no TypeScript) |
| **CSS3** (Grid, Flexbox, Custom Properties, Transitions) | **CSS Frameworks** (No Bootstrap, Tailwind, Bulma, Foundation) |
| **Inline Scalable Vector Graphics (SVG)** | **JS Libraries** (No React, Vue, Angular, Svelte, jQuery) |
| **Native HTML5 Form Validation APIs** | **Third-Party UI Widgets** (No external charting or slider libraries) |
| **CSS `:focus-within` & `:checked` State Handlers** | **Backend Stacks** (No PHP, Python Django/Flask, Java Spring, Express) |

---

## 3. Syllabus Unit Mapping (B.Tech CSE Web Technologies)

This project comprehensively demonstrates every core concept specified in the undergraduate curriculum:

### Unit I: HTML Fundamentals
* **Document Architecture**: Standard `<!DOCTYPE html>`, `<html>`, `<head>`, `<meta charset="UTF-8">`, viewport scaling meta tags, `<title>`, and structured `<body>`.
* **Block & Inline Elements**: Proper separation of block containers (`<div>`, `<p>`, `<h1>`-`<h6>`, `<ul>`, `<ol>`, `<figure>`) and inline semantic text tags (`<span>`, `<code>`, `<time>`, `<strong>`, `<a>`).
* **Hyperlinks & Relative Navigation**: Robust, portable relative URL paths (`href="workshops.html"`, `href="css/style.css"`) ensuring flawless local offline execution.
* **Tables**: Complete tabular layouts with `<table>`, `<caption>`, `<thead>`, `<tbody>`, `<tr>`, `<th scope="col">`, and `<td>` for structured tabular datasets.

### Unit II: Semantic HTML and Forms
* **Structural Semantics**: Total avoidance of "div-soup". Layouts are explicitly organized using `<header>`, `<nav>`, `<aside>`, `<main>`, `<section>`, `<article>`, and `<footer>`.
* **Accessible Metadata**: Semantic `<time datetime="...">` tags for machine-readable dates, `<address>`, `<figcaption>`, and descriptive ARIA landmark attributes.
* **Native Form Controls**: Utilization of diverse HTML5 input types:
  * `type="text"`, `type="email"`, `type="password"`, `type="tel"`, `type="number"`, `type="date"`, `type="time"`, `type="search"`, `type="checkbox"`, and `type="radio"`.
* **Client-Side Validation Constraints**: Complete native validation leveraging `required`, `minlength`, `maxlength`, `min`, `max`, `step`, `pattern` (regular expressions for course codes, asset tags, and student roll numbers), `autocomplete`, `readonly`, and `placeholder`.
* **Accessible Grouping**: Every form utilizes `<fieldset>` with styled `<legend>` elements and explicitly bound `<label for="...">` associations.

### Unit III: Cascading Style Sheets (CSS3)
* **CSS Selectors**:
  * *Element & Class*: `body`, `table`, `.card`, `.badge`, `.btn`
  * *Descendant & Child*: `.sidebar-nav a`, `.nav-list > li`, `.card-header > h2`
  * *Attribute Selectors*: `input[type="search"]`, `input[type="checkbox"]`, `[aria-current="page"]`
  * *Group Selectors*: `h1, h2, h3`, `th, td`
  * *Pseudo-Classes*: `:hover`, `:focus`, `:focus-visible`, `:active`, `:checked` (for pure CSS responsive mobile drawer toggle), `:disabled`, `:focus-within` (for pure CSS dropdown menus), `:required`, `:valid`, `:invalid`, and `:nth-child(even)` (for zebra striping).
  * *Pseudo-Elements*: `::before`, `::after` (for status badge dots, breadcrumb dividers, and visual indicators), `::placeholder`, and `::selection`.
* **CSS Box Model**: Universal `box-sizing: border-box;`, controlled padding, margins, borders, and outlines.
* **Modern Layout Engines**:
  * **CSS Flexbox**: Used for top navigation bars, breadcrumb trails, user identity pills, button groups, and search bars.
  * **CSS Grid**: Used for the overall application frame (`270px 1fr`), 4-column statistics decks, responsive workshop cards, and multi-column fieldset arrangements.
* **CSS Custom Properties (Variables)**: Centralized `:root` design tokens for primary midnight navy, indigo accents, cyan highlights, slate typography, semantic alerts, and spacing scales.
* **Pure CSS Data Visualizations**:
  * Vertical interactive Bar Chart built with CSS Flexbox, custom percentage heights, and pure CSS `:hover` tooltips.
  * Multi-colored Donut Chart generated via CSS3 `conic-gradient()` with center cutout mask and styled legend.
  * Capacity progress meters using CSS gradient tracks.
* **Responsive Web Design**: Mobile-first media queries (`@media screen and (max-width: 1024px)` and `@media screen and (max-width: 768px)`), fluid card grids, and horizontal scrolling wrappers for tables (`.table-responsive`).
* **Accessibility**: Respects `@media (prefers-reduced-motion: reduce)`.

---

## 4. Directory & Folder Structure

```text
workshop-management-system/
│
├── index.html                   # PAGE 1: Executive Dashboard (Hero, Stats, Table, Activity, Actions)
├── workshops.html               # PAGE 2: Workshops Management (Search, Category Filter, Card Grid)
├── participants.html            # PAGE 3: Participant Directory (Roster Table, Search, Dept Filter)
├── registrations.html           # PAGE 4: Registrations Ledger (Payment Status, Fee Waiver Audits)
├── equipment.html               # PAGE 5: Equipment Inventory (Asset Tags, Readiness Status, Counts)
├── rentals.html                 # PAGE 6: Equipment Rentals (Requisition Approval, Checkouts, Returns)
├── requests.html                # PAGE 7: Special Requests (Curriculum Proposals, Ticket Form)
├── reports.html                 # PAGE 8: Analytics & Reports (CSS Bar Chart, Donut Chart, KPIs)
├── settings.html                # PAGE 9: Settings (Profile, Department Info, Notifications, Theme)
├── login.html                   # PAGE 10: Authentication Portal (Validated Login Form, Disclaimer)
├── register.html                # PAGE 11: Public Registration (Participant Onboarding, Validation)
├── create-workshop.html         # PAGE 12: Workshop Creation Form (Schedule, Venue, Limits, Deadlines)
├── add-equipment.html           # PAGE 13: Add Equipment Form (Serial, Inventory, Lab Compartment)
├── register-participant.html    # PAGE 14: Manual Enrollment Form (Fee Category, Special Needs)
│
├── css/
│   └── style.css                # Master unified stylesheet (Variables, Reset, Grid, UI Components)
│
├── assets/
│   ├── images/                  # Directory reserved for static image assets
│   └── icons/                   # Directory reserved for static icon assets
│
└── README.md                    # Comprehensive technical documentation & project report