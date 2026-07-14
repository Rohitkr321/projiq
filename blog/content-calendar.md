# Projiq Blog Content Calendar

This file is read by the scheduled blog writer. Each entry has a status:
- `pending` = not yet written
- `done` = post exists at the listed path

When writing a new post, mark it `done` and update the path.
Always pick the next `pending` entry in order.

---

## Queue

| # | Status | Keyword Target | Title | Path |
|---|--------|---------------|-------|------|
| 1 | done | best ai coding tools | Best AI Coding Tools for Engineering Teams in 2026 | /blog/best-ai-coding-tools/ |
| 2 | done | jira vs linear | Jira vs Linear: Which Is Better for Engineering Teams in 2026? | /blog/jira-vs-linear/ |
| 3 | done | sprint retrospective template | 7 Sprint Retrospective Templates Your Team Will Actually Use | /blog/sprint-retrospective-templates/ |
| 4 | done | how to write user stories | How to Write User Stories: Complete Guide with Examples | /blog/how-to-write-user-stories/ |
| 5 | done | kanban vs scrum | Kanban vs Scrum: Which Agile Framework Is Right for Your Team? | /blog/kanban-vs-scrum/ |
| 6 | done | dora metrics | DORA Metrics Explained: How to Measure Engineering Team Performance | /blog/dora-metrics/ |
| 7 | done | sprint planning meeting | How to Run an Effective Sprint Planning Meeting (2026 Guide) | /blog/sprint-planning-guide/ |
| 8 | done | product roadmap template | How to Build a Product Roadmap Your Engineers Will Actually Follow | /blog/product-roadmap-guide/ |
| 9 | done | technical debt | Technical Debt: How to Identify, Prioritize, and Pay It Down | /blog/technical-debt-management/ |
| 10 | done | okrs for engineering teams | OKRs for Engineering Teams: A Practical Guide with Real Examples | /blog/okrs-for-engineering-teams/ |
| 11 | done | sprint velocity | Sprint Velocity: What It Is, How to Measure It, and Why It Matters | /blog/sprint-velocity/ |
| 12 | done | engineering team structure | Engineering Team Structures: Squads, Tribes, and Guilds Explained | /blog/engineering-team-structure/ |
| 13 | done | story points estimation | Story Points vs Hours: How to Estimate User Stories Accurately | /blog/story-points-estimation/ |
| 14 | done | definition of done | Definition of Done vs Acceptance Criteria: What's the Difference? | /blog/definition-of-done/ |
| 15 | done | scrum ceremonies | Scrum Ceremonies: A Complete Guide to All 5 Events | /blog/scrum-ceremonies/ |
| 16 | done | engineering manager vs tech lead | Engineering Manager vs Tech Lead: Roles, Differences, and When You Need Both | /blog/engineering-manager-vs-tech-lead/ |
| 17 | done | how to run standup meeting | How to Run a Daily Standup That Doesn't Waste Everyone's Time | /blog/how-to-run-standup/ |
| 18 | done | software development lifecycle | The Software Development Lifecycle (SDLC) Explained for Engineering Teams | /blog/software-development-lifecycle/ |
| 19 | pending | project management for startups | Project Management for Startups: How to Stay Organized While Moving Fast | /blog/project-management-for-startups/ |
| 20 | pending | how to reduce meeting time | Engineering Teams: How to Cut Meeting Time in Half Without Losing Alignment | /blog/reduce-meeting-time/ |
| 21 | pending | platform engineering | Platform Engineering: What It Is and Why Every Tech Company Needs It in 2026 | /blog/platform-engineering/ |
| 22 | pending | continuous deployment | Continuous Deployment for Engineering Teams: A Practical Getting-Started Guide | /blog/continuous-deployment-guide/ |
| 23 | pending | burndown chart | How to Read a Burndown Chart (And What to Do When It Looks Wrong) | /blog/burndown-chart-guide/ |
| 24 | pending | epic vs user story | Epics vs User Stories vs Tasks: The Complete Hierarchy Explained | /blog/epic-vs-user-story/ |
| 25 | pending | remote work tools | Best Remote Work Tools for Engineering Teams in 2026 | /blog/remote-work-tools/ |
| 26 | pending | how to prioritize backlog | How to Prioritize a Product Backlog: 5 Frameworks That Work | /blog/how-to-prioritize-backlog/ |
| 27 | pending | engineering kpis | Engineering KPIs: 12 Metrics Every Engineering Leader Should Track | /blog/engineering-kpis/ |
| 28 | pending | code review best practices | Code Review Best Practices for Engineering Teams in 2026 | /blog/code-review-best-practices/ |
| 29 | pending | onboarding new engineers | How to Onboard New Engineers in 30 Days Without Slowing Down the Team | /blog/onboarding-new-engineers/ |
| 30 | pending | async communication | Async-First Communication: How Engineering Teams Ship Without Constant Meetings | /blog/async-communication/ |

---

## Instructions for the Scheduled Writer

When this cron fires, do the following:

1. Read this file and find the first row with `status = pending`
2. Write a full blog post at the path listed — use the same HTML/CSS structure as existing posts in `/blog/`
3. The post must include:
   - Article + BreadcrumbList + FAQPage JSON-LD schemas
   - Canonical URL, OG tags, Twitter Card tags
   - Reading progress bar (`.prog`)
   - Hidden SVG defs block (brand-grad + projiq-p symbol) before the nav
   - Sticky TOC sidebar
   - Real content minimum 8 min read (aim for 1800+ words)
   - FAQ accordion section (minimum 5 questions)
   - Internal links to 2–3 other existing blog posts
   - CTA box linking to https://app.projiq.app/register-org
   - Footer with blog and alternatives links
   - Mobile responsive (same breakpoints as existing posts)
   - JS progress bar + TOC highlight script
4. Update this file — change the post's status from `pending` to `done`
5. Add a new card for the post in `/blog/index.html` — insert it into the `<div class="post-grid">` before the first `coming-soon` card, or as the featured post if more impactful
6. Add the new URL to `/blog/sitemap.xml` with today's date, changefreq monthly, priority 0.7
7. Do NOT commit any changes — editing files only

Always match the visual style, accent colors, and content quality of the existing blog posts.
