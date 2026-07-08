# Projiq Landing Page

Marketing landing page for **[Projiq.app](https://projiq.app)** — a project management platform built for organizations.

Hosted on **GitHub Pages** at `projiq.app` via a custom CNAME.

---

## Tech Stack

| Layer | Details |
|-------|---------|
| Language | Plain HTML5 + CSS3 + Vanilla JS (no framework) |
| Hosting | GitHub Pages (repo root → `main` branch) |
| Domain | `projiq.app` (CNAME points to `Rohitkr321.github.io`) |
| Analytics | Google Analytics 4 (`G-RHZ0CDYYFV`) |
| SEO | Open Graph, Twitter Card, JSON-LD structured data, sitemap.xml |

> All styles and scripts are **inlined** inside `index.html`. No build step, no `package.json`, no dependencies.

---

## File Structure

```
projiq-landing/
├── index.html      # Entire site — all CSS and JS are inlined
├── CNAME           # Custom domain: projiq.app
├── sitemap.xml     # XML sitemap for search engines
├── robots.txt      # Crawler rules (blocks /app/ subdomain)
├── og.png          # Open Graph image (1200×630) for social previews
├── org.png         # Original OG image upload (legacy name)
└── favicon.ico     # Browser tab icon
```

---

## Running Locally

```bash
# Option 1: open directly
open index.html

# Option 2: serve with Python (avoids file:// quirks)
python -m http.server 8080
# visit http://localhost:8080
```

---

## Deployment

Push to `main` → live at `projiq.app` within ~60 seconds.

```bash
git add .
git commit -m "your change"
git push origin main
```

> **Note:** The `CNAME` file must stay at the repo root. Deleting it removes the custom domain.

---

## Features

### Sprint & Issue Management
| Feature | Description |
|---------|-------------|
| Scrum & Kanban boards | Switch between sprint-based Scrum and continuous Kanban at any time — no history lost |
| Issue hierarchy | Epics → Stories → Subtasks — every level searchable and linked end to end |
| Custom workflows | Define your own statuses and transitions per project |
| Threaded comments & @mentions | Discussion stays with the issue; full activity history searchable |
| Labels, priorities & release tags | 5 priority tiers, colour-coded labels, and version tags |

### Sprint Planning
| Feature | Description |
|---------|-------------|
| One-click sprint start & close | Start with an optional end date; close to auto-archive completed issues |
| Live burndown charts | Track remaining work vs. ideal line — day by day |
| Backlog grooming | Filter, search, and bulk-move issues between sprints in seconds |
| Velocity analytics | Sprint-over-sprint velocity tracked automatically — zero manual entry |

### Board & Visualization
| Feature | Description |
|---------|-------------|
| Drag-and-drop board | Move cards across any custom workflow column |
| Live presence | See who's working on what in real time — assignees, priority, story points on every card |

---

## Views

| View | Description |
|------|-------------|
| **Board** | Kanban drag-and-drop across workflow columns — updates live for all team members |
| **Backlog** | Prioritised issue list with filter by type, priority, assignee, and sprint; bulk-move actions |
| **Timeline** | Sprint Gantt view across the calendar — spot scheduling conflicts and plan capacity |
| **Roadmap** | Epic-level Gantt across months and quarters — present long-term plans to stakeholders |
| **Calendar** | Month view of all due dates across every project — see deadline collisions before they happen |
| **Sprint Report** | Burndown chart (ideal vs. actual) + story point metrics and issue-status breakdown per sprint |

---

## Platform

| Platform | Status | Details |
|----------|--------|---------|
| **Web App** | ✅ Live | Full-featured on Chrome, Safari, Firefox, Edge — all 6 views, all features |
| **Real-time Sync** | ✅ Live | WebSocket via Socket.io — every change syncs in under 100ms for all users |
| **Mobile App (iOS & Android)** | 🔜 Coming Soon | Native app in development — full feature parity with web |

---

## Pricing

> **Billing model:** Per organization per month — **not per seat**. Every invited member gets full access under one plan. Billed via Razorpay in USD. 14-day free trial on any plan. No long-term contracts.

### Starter — $149 / month
_Up to 10 members · Up to 5 active projects_

- Kanban & Scrum boards
- Backlog & issue tracking
- Threaded comments & attachments
- Calendar & Timeline view
- 3 access roles
- Email support
- ~~Sprint reports & burndown~~
- ~~Roadmap & release management~~
- ~~Custom fields~~

**Sign-up:** `https://app.projiq.app/register-org?plan=starter`

---

### Professional — $299 / month ⭐ Most Popular
_Up to 50 members · Up to 10 active projects_

- Everything in Starter
- Sprint planning & burndown charts
- Roadmap & epic tracking
- Release management
- Custom fields per project
- 5-tier role-based access control
- Velocity & sprint analytics
- Real-time WebSocket sync
- Priority support

**Sign-up:** `https://app.projiq.app/register-org?plan=professional`

---

### Enterprise — $599 / month+
_Unlimited members · Unlimited projects_

- Everything in Professional
- Unlimited members & projects
- Dedicated customer success support
- Custom workflow configuration
- Hands-on team onboarding
- Data migration assistance
- Priority uptime & monitoring
- Priority support & escalation
- Custom billing & invoicing

**Contact:** `sales@projiq.com` or `https://app.projiq.app/register-org?plan=enterprise`

---

## Implementation (Enterprise / Onboarding)

4-week managed rollout included with Enterprise plans:

| Week | Phase | What happens |
|------|-------|-------------|
| 1 | **Discovery & Setup** | Kickoff call, org & project structure, admin accounts, roles mapped to org chart, workspace live |
| 2 | **Configuration** | Custom workflows per team, custom fields & labels, data migration, permissions & notifications |
| 3 | **Pilot & Training** | 5–10 pilot users onboarded, live role-based training, first sprint run end-to-end, feedback actioned |
| 4 | **Full Rollout** | All users invited, all projects migrated, go-live sign-off, 30-day post-launch helpdesk, QBR scheduled |

---

## SEO

- **Meta description** — matches `og:description`
- **Open Graph** — `og:image` at `https://projiq.app/og.png` (1200×630)
- **Twitter Card** — `summary_large_image`
- **JSON-LD** — `Organization`, `WebSite`, `SoftwareApplication` schema
- **Sitemap** — `sitemap.xml` submitted to Google Search Console
- **Robots** — all pages allowed; `/app/` subdomain blocked from indexing

To update the OG image: replace `og.png` at the repo root (keep the filename).

---

## Mobile Responsiveness

| Breakpoint | Changes |
|-----------|---------|
| `≤ 900px` | Gallery stacks to single column |
| `≤ 768px` | Hamburger nav, all 3D transforms flattened, grids → single column |
| `≤ 560px` | Hero buttons stack vertically, footer single column |
| `≤ 480px` | Announcement bar truncated to single line, hero padding increased to 96px to clear nav, container padding tightened to 16px |
| `≤ 400px` | Section titles and hero headline use smaller `clamp()` floor |

`overflow-x: hidden` is set on both `html` and `body` (iOS Safari requires it on both to fully block horizontal scroll).

---

## Page Sections

| Section | Anchor |
|---------|--------|
| Hero — headline, CTA, live app mock | `#hero` |
| Features — sprint, issues, boards | `#features` |
| Views — Board / Backlog / Timeline / Roadmap / Calendar / Sprint Report | `#views` |
| Platform — Web app, real-time sync, mobile | `#platform` |
| Security — RS256 JWT, 2FA, RBAC roles | `#security` |
| Pricing — Starter / Professional / Enterprise | `#pricing` |
| Testimonials — social proof + metrics | `#testimonials` |
| Implementation — 4-week rollout | `#implementation` |
| FAQ — accordion | `#faq` |
| CTA — final sign-up | `#cta` |

---

## Google Search Console

1. Go to [search.google.com/search-console](https://search.google.com/search-console)
2. Property: `projiq.app`
3. Submit `https://projiq.app/sitemap.xml` under **Sitemaps**
4. Use **URL Inspection → Request Indexing** after major content changes

---

## Contact

| Purpose | Contact |
|---------|---------|
| General | In-page contact modal |
| Enterprise sales | sales@projiq.com |
| App sign-up | https://app.projiq.app/register-org |
| App login | https://app.projiq.app/login |
