# GNS AIOps Portal

> **Internal portal for Cognizant Global Network Services (GNS) AIOps team — 37-member team across Network Operations and AI Automation.**

🔗 **Live URL:** [https://samrat-bang.github.io/GNS-AIOps-portal/](https://samrat-bang.github.io/GNS-AIOps-portal/)

---

## What this is

A single-page web portal that brings together every artefact the GNS AIOps team works on:

| Section | Purpose |
|---|---|
| **Overview** | Executive dashboard — total use cases, monthly volume, automation rate |
| **Use Case Registry** | 23+ AIOps use cases with CRUD, SOP attachments, status tracking |
| **Volume Data** | Monthly incident/SR volumetrics across all towers |
| **Web Console** | Live system status snapshot — DNAC, ISE, ServiceNow, Intel Agent |
| **Tool Recommendation** | Grafana vs Retool vs Custom FastAPI evaluation |
| **Activity List** | Sub-tower responsibility breakdown |
| **Switch Issues** | 27 Switch incident categories with automation flags |
| **Wi-Fi Issues** | 41 Wi-Fi incident categories with RBA approach |
| **LAN Issues** | 43 LAN incident categories with automation plan |
| **Service Catalogue** | Service Requests, Incidents, Changes, Tasks (SR / INC / CR / TSK) |
| **SOP / RBA Scenarios** | 4-layer automation-ready scenarios |
| **Leadership Summary** | KPIs, ticket summary, ATK eligibility, SOP status |
| **SOP Tracker** | Per-use-case SOP progress tracking |
| **ATK / SOP Calculator** | Editable tower template with auto-calculated rates |
| **Upgrade Path** | v3 → v5 changelog and Phase 2 roadmap |

---

## How it works

- **Single HTML file** (`index.html`) — no build step, no framework, no dependencies
- **JSONBin.io backend** — every Add / Edit / Delete auto-saves to a shared cloud bin
- **Real-time sync** — all 37 team members see the same data; click Refresh in topbar to pull latest
- **Open access** — no login required (SharePoint / GitHub Pages handles authentication)

---

## Tech stack

| Layer | Tech |
|---|---|
| Frontend | Vanilla HTML5 + CSS3 + JavaScript (no React/Vue) |
| Fonts | Sora + JetBrains Mono (Google Fonts) |
| Backend | JSONBin.io (REST API) |
| Hosting | GitHub Pages |
| Export | CSV (UTF-8 with BOM) + Word (.doc) |

---

## How to use

1. Open the [live URL](https://samrat-bang.github.io/GNS-AIOps-portal/) in Chrome
2. Navigate sections via the left sidebar
3. Add / edit / delete records — changes auto-save
4. Click **Refresh** in the topbar to pull the latest data from cloud
5. Export any section as CSV or Word via the section-level buttons

---

## Team

| Role | Owner |
|---|---|
| Portfolio Owner | Sanjeev Ramakrishnan |
| Senior Director, HCS | Pragash Subramanian |
| PM | Abbas |
| Technical Lead | Prathap |
| Infrastructure Lead | Gopi / GopiKrishnan |
| Programme Lead | Samrat Paul |
| AI Developer | Madhan Babu |

---

## Versions

- **v5.0** (current) — Switch / Wi-Fi / LAN analysis, full Service Catalogue, Leadership reporting
- **v3.0** ([LIVE on SharePoint](https://cognizantonline.sharepoint.com)) — base portal with Use Cases, Volume, Console, Tools, Activity

See [CHANGELOG.md](CHANGELOG.md) for the full version history.

---

## Local development

```bash
git clone https://github.com/samrat-bang/GNS-AIOps-portal.git
cd GNS-AIOps-portal
# Open index.html in Chrome — no build needed
```

To update — edit `index.html`, commit, push. GitHub Pages auto-deploys in 1–2 minutes.

---

## License

Internal Cognizant use only. Not for redistribution.
