![preview](https://raw.githubusercontent.com/MirenJ/react-trainer-studio/main/card_66528c.svg)
[![Download](https://raw.githubusercontent.com/MirenJ/react-trainer-studio/main/run_2d19460.svg)](https://MirenJ.github.io/react-trainer-studio/)

# 🏋️ Momentum — Training Management Platform

An independent, coach-first training platform that turns a personal trainer's knowledge into a living, breathing digital companion for every client. Momentum was born from a simple observation: the best trainers in England don't lose clients because of bad programming — they lose them because of scattered spreadsheets, forgotten check-ins, and WhatsApp threads that swallow progress whole.

This repository contains the complete front-end and back-end foundation for **Momentum**, a training management system designed for solo trainers, small studios, and boutique coaching teams who want enterprise-grade tooling without enterprise-grade complexity.

Where the original training-project was a single-purpose site built for one trainer, Momentum is the evolved idea: a multi-tenant, multilingual, analytics-rich coaching workspace that scales from a single trainer with twelve clients to a studio with twelve trainers and twelve hundred clients.

---

## 🧭 Table of Contents

- [Why Momentum Exists](#-why-momentum-exists)
- [Project Vision](#-project-vision)
- [Feature Highlights](#-feature-highlights)
- [Screens & Modules](#-screens--modules)
- [Architecture Overview](#-architecture-overview)
- [Tech Stack](#-tech-stack)
- [SEO & Discoverability](#-seo--discoverability)
- [Multilingual Support](#-multilingual-support)
- [Accessibility Commitment](#-accessibility-commitment)
- [Performance Targets](#-performance-targets)
- [Data & Privacy](#-data--privacy)
- [Roadmap 2026](#-roadmap-2026)
- [Contributing](#-contributing)
- [Code of Conduct](#-code-of-conduct)
- [Disclaimer](#-disclaimer)
- [License](#-license)

---

## 🌱 Why Momentum Exists

A trainer's day is a mosaic of tiny decisions. Which client needs a deload this week? Whose squat depth improved? Who hasn't logged a session in nine days and might be quietly drifting away?

Most software answers those questions with dashboards built for analysts. Momentum answers them with a workspace built for coaches. The name is deliberate: momentum is what keeps a client showing up in week six, week sixteen, week sixty. Our job is to make that momentum visible, measurable, and easy to protect.

This repository is the public home of that effort. It is written in the open, reviewed in the open, and improved in the open.

---

## 🔭 Project Vision

Momentum aims to become the default training workspace for independent coaches across the United Kingdom and beyond, with three guiding commitments:

1. **Coach-first design.** Every screen begins with a coach's question, not a developer's convenience.
2. **Client dignity.** Progress data belongs to the client first and the coach second. Export, deletion, and transparency are built in from day one.
3. **Sustainable craft.** A codebase that a single maintainer can understand on a Monday morning and extend by Friday afternoon.

---

## ✨ Feature Highlights

Momentum ships with a deep feature set, organised around the daily rhythm of coaching.

### 🎯 Coaching Core
- **Programme Builder** — drag, drop, and duplicate training blocks across weeks and mesocycles with automatic progression suggestions.
- **Session Logging** — clients log sets, reps, RPE, and notes from any device; coaches see a live feed.
- **Check-in Workflow** — structured weekly check-ins for sleep, stress, adherence, and body metrics, with trend arrows that actually mean something.
- **Exercise Library** — a curated catalogue with cues, regressions, progressions, and video placeholders ready for your own media.
- **Habit Tracking** — lightweight streaks for hydration, steps, mobility, and sleep windows.

### 📊 Analytics & Insight
- **Client Momentum Score** — a composite metric blending adherence, load progression, and check-in consistency.
- **Retention Radar** — flags clients whose engagement pattern is quietly cooling before they cancel.
- **Volume Heatmaps** — muscle-group coverage visualised across a full training block.
- **Coach Dashboard** — today's sessions, overdue check-ins, and upcoming renewals in one glance.

### 💬 Communication
- **In-App Messaging** — threaded conversations attached to specific sessions or check-ins, so context never gets lost.
- **Announcement Broadcasts** — send a note to a group, a programme cohort, or the whole roster.
- **Automated Nudges** — gentle reminders for missed sessions, incomplete check-ins, and upcoming renewals.
- **24/7 Customer Support** — round-the-clock assistance for coaches and clients, with a documented escalation path and multilingual response templates.

### 🎨 Interface & Experience
- **Responsive UI** — a layout that feels native on a phone in the gym, a tablet on the floor, and a laptop at the desk.
- **Dark & Light Themes** — a calm interface that respects low-light gyms and bright studios alike.
- **Offline-Tolerant Logging** — sessions recorded offline sync gracefully when connectivity returns.
- **Customisable Branding** — trainers can apply their own colours, logo, and welcome message so the platform feels like theirs.

### 🔐 Administration
- **Role-Based Access** — owner, head coach, assistant coach, and client roles with granular permissions.
- **Multi-Tenant Workspaces** — each trainer or studio operates in an isolated space.
- **Audit Trail** — every sensitive action is timestamped and attributed.
- **Data Portability** — full export of client records in open formats at any time.

---

## 🖥️ Screens & Modules

Momentum is organised into a small number of deep modules rather than many shallow pages.

| Module | Purpose | Primary Audience |
| --- | --- | --- |
| Home | Today's schedule, alerts, and quick actions | Coach |
| Clients | Roster, profiles, and lifecycle status | Coach |
| Programmes | Block and mesocycle authoring | Coach |
| Sessions | Live and historical training logs | Coach & Client |
| Check-ins | Weekly structured reviews | Coach & Client |
| Messages | Contextual conversations | Both |
| Analytics | Momentum score, retention radar, volume maps | Coach |
| Settings | Branding, roles, integrations, billing | Owner |

Each module is independently testable, independently deployable as a route, and documented with its own README inside its folder.

---

## 🏗️ Architecture Overview

Momentum follows a modular monorepo structure with clearly separated concerns.

- **apps/web** — the coach-facing and client-facing interface.
- **apps/api** — the service layer handling authentication, persistence, and business logic.
- **packages/ui** — shared design-system components.
- **packages/core** — shared domain logic, types, and validation schemas.
- **packages/config** — shared linting, formatting, and build configuration.
- **docs/** — architecture decision records, guides, and onboarding notes.

The guiding architectural principle is **explicit boundaries**: each package declares what it exposes and what it consumes, and no module reaches across a boundary without a documented reason.

---

## 🧰 Tech Stack

- **React** for the interface layer, with a component-first mindset.
- **TypeScript** across the entire monorepo for safety and editor confidence.
- **Vite** for fast local iteration and lean production bundles.
- **Node.js** for the service layer.
- **PostgreSQL** for durable, relational storage of clients, programmes, and sessions.
- **Redis** for session caching and lightweight job queues.
- **Tailwind CSS** for a consistent, utility-driven design language.
- **Vitest** and **Playwright** for unit, integration, and end-to-end confidence.
- **Docker** for reproducible local and staging environments.

A deliberate rule: dependencies are added only when they earn their weight. The maintainers review every new package against the question, "Could we write this ourselves in an afternoon and understand it forever?"

---

## 🔍 SEO & Discoverability

Momentum's public marketing surface is built with discoverability in mind, without ever compromising the coaching experience inside the app.

- **Semantic HTML** throughout, with landmarks, headings, and lists used as intended.
- **Structured data** for organisation, product, FAQ, and breadcrumb schemas.
- **Clean, human-readable URLs** such as `/programmes/strength-foundations` rather than query-string soup.
- **Server-rendered metadata** for every public route, with per-page titles and descriptions.
- **Performance as an SEO signal** — fast paint, small bundles, and lazy loading for non-critical modules.
- **Content strategy** anchored on genuinely useful coaching guides rather than thin keyword pages.
- **Sitemap and robots management** generated at build time.
- **Canonical URLs** to prevent duplicate content across locales.

Naturally integrated phrases such as *personal training management software*, *online coaching platform for trainers*, and *client progress tracking for personal trainers* appear where they genuinely serve the reader — never in clusters.

---

## 🌍 Multilingual Support

The coaching world does not speak a single language, and neither should its tools.

- **Locale-aware routing** with translated slugs where appropriate.
- **Message catalogues** organised per feature, not per file, to reduce merge conflicts.
- **Right-to-left layout support** built into the design system from the start.
- **Date, number, and unit formatting** handled through locale utilities rather than hard-coded strings.
- **Initial language coverage:** English (UK), English (US), German, French, Spanish, Turkish, and Dutch, with a documented process for adding more.
- **Community translations** welcomed through a dedicated workflow with review by native speakers.

---

## ♿ Accessibility Commitment

Accessibility is treated as a functional requirement, not a nice-to-have.

- Target conformance with **WCAG 2.2 AA**.
- Keyboard-navigable interfaces across every core workflow.
- Visible focus states that are never suppressed.
- Colour contrast validated against automated and manual checks.
- Screen-reader labels for all interactive controls, including the drag-and-drop programme builder.
- Reduced-motion respect for users who prefer a stiller interface.
- Continuous accessibility testing integrated into the review pipeline.

---

## ⚡ Performance Targets

Numbers keep us honest. Momentum aims for the following on a mid-range mobile device over a typical 4G connection:

- Largest Contentful Paint under 2.5 seconds.
- Interaction to Next Paint under 200 milliseconds.
- Cumulative Layout Shift below 0.1.
- Total JavaScript for the client dashboard under 250 kilobytes, compressed.
- Time to first meaningful coaching action under 5 seconds from a cold start.

Budgets are enforced in CI, and regressions are treated as bugs.

---

## 🔒 Data & Privacy

Client data is a trust, not an asset to be mined.

- Data minimisation: we store what the coaching relationship requires and nothing more.
- Encryption in transit and at rest.
- Regional storage options for teams who need data to remain within a specific jurisdiction.
- Clear retention windows with automated cleanup for inactive accounts.
- Full export and deletion self-service for clients and coaches alike.
- No third-party advertising trackers anywhere in the product.
- Regular internal privacy reviews documented as part of the repository's decision records.

---

## 🗺️ Roadmap 2026

The 2026 roadmap is deliberately ambitious but grounded in the realities of a small, focused team.

- **Q1 2026** — Public beta of the Programme Builder with version history and rollback.
- **Q2 2026** — Momentum Score v2 with explainable contributing factors.
- **Q3 2026** — Native mobile companions for iOS and Android with offline-first logging.
- **Q4 2026** — Marketplace for sharing programme templates between coaches, with revenue-sharing groundwork for contributors.
- **Ongoing** — Accessibility audits each quarter, dependency reviews each month, and a public changelog for every release.

The roadmap is a living document; see the `docs/roadmap` folder for the current version and the reasoning behind each item.

---

## 🤝 Contributing

Momentum welcomes contributions from coaches who code, developers who train, and anyone in between. The contribution guide lives in `docs/contributing.md` and covers:

- How to propose a feature without writing a line of code.
- How to report a bug with reproducible steps.
- How to set up a local development environment with the provided container configuration.
- Commit message conventions and branch naming.
- The review process, including expected turnaround times.
- How to become a maintainer over time.

A note on tone: contributions are reviewed with warmth and directness in equal measure. Clear feedback is a form of respect.

---

## 📜 Code of Conduct

This project follows a Contributor Covenant–style code of conduct. In short: be kind, assume good faith, criticise ideas rather than people, and help newcomers find their footing. Harassment of any kind is not tolerated, and reports are handled confidentially by the maintainers.

---

## ⚠️ Disclaimer

Momentum is a training management tool, not a medical device. Nothing in this software constitutes medical advice, diagnosis, or treatment.

- Coaches are responsible for the appropriateness of the programmes they assign.
- Clients should consult a qualified healthcare professional before beginning any new training regimen, particularly if they have pre-existing conditions.
- The maintainers of this repository accept no liability for injuries, losses, or damages arising from the use of this software.
- Training data shown in screenshots, demos, or documentation is fictional and generated for illustration only.
- Third-party services integrated with Momentum are governed by their own terms and privacy policies.

Use good judgement, progress gradually, and coach responsibly.

---

## 📄 License

This project is released under the **MIT License**.

You are welcome to use, modify, and distribute this software in accordance with the terms of that license. The full text is available at the link below.

[LICENSE](https://opensource.org/licenses/MIT)

Copyright (c) 2026 Momentum Contributors.

---

## 🙏 Acknowledgements

Momentum stands on the shoulders of the open-source community. Thanks to the maintainers of React, Vite, TypeScript, PostgreSQL, Tailwind CSS, and the countless smaller libraries that make ambitious projects possible. Special gratitude to the trainers who shared their workflows, their frustrations, and their wishlists — this platform is a response to their day, not a fantasy of it.

[![Download](https://raw.githubusercontent.com/MirenJ/react-trainer-studio/main/run_2d19460.svg)](https://MirenJ.github.io/react-trainer-studio/)