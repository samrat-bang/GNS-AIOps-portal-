# Changelog

All notable changes to the GNS AIOps Portal are documented here.

The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/) and the project uses [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

---

## [5.0] — 2026-05-25

### Added
- **Switch Issues** page — 27 incident categories with automation flags, RBA approach, View/Edit/Delete/Add CRUD, CSV + Word export
- **Wi-Fi Issues** page — 41 incident categories with the same CRUD pattern
- **LAN Issues** page — 43 incident categories
- **Service Catalogue** group — separate pages for:
  - Service Requests (SR)
  - Incidents (INC)
  - Changes (CR)
  - Tasks (TSK)
  - Each row tracks ATK Eligible / SOP Available / Native Automation in Place
- **SOP / RBA Scenarios** page — 4-layer model (Input Simplification → Data Enrichment → Decision Logic → Execution)
- **Leadership Summary** page — KPIs, ticket summary by tower, ATK eligibility table, SOP status by tower
- **SOP Tracker** page — per-use-case progress monitoring with status, owner, last review
- **ATK / SOP Calculator** page — editable tower template with auto-calculated percentages
- **Upgrade Path** page — version roadmap and Phase 2 plan
- **View action** — read-only modal on every use case row, with Edit transition
- **CSV + Word export** on every section (14 sections, 28 export buttons total)
- **SOP file attachment** on Use Cases, Switch / Wi-Fi / LAN, Service Catalogue, SOP Scenarios modals
- **Expanded sub-tower options** — 40 sub-towers across 5 towers (was 11)

### Changed
- Sidebar grouping reorganized into Main / Strategy / Incident Analysis / Service Catalogue / Leadership sections
- Topbar shows `GNS AIOps v5` breadcrumb
- View → Edit transition now uses 120ms delay to prevent modal animation conflicts

### Preserved from v3
- All 23 original use cases
- Volume Data with inline editing
- Web Console terminals (DNAC, ISE, ServiceNow, Intel Agent)
- Tool Recommendation matrix (Grafana / Retool / Custom FastAPI)
- Activity List
- JSONBin sync (same bin, same data)
- v3 design language, CSS variables, layout grid

---

## [4.0] — 2026-05-18

### Added
- View action button on every row (later refined in v5)
- Initial Service Catalogue prototype
- Initial Leadership Summary draft

### Note
v4 was deprecated due to layout misalignment. v5 rebuilds these features cleanly on the v3 foundation.

---

## [3.0] — 2026-05-15

### Initial release (LIVE on SharePoint)
- Overview dashboard with 5 KPI cards
- Use Case Registry with full CRUD and SOP file upload
- Volume Data with inline cell editing
- Web Console with live API snapshots
- Tool Recommendation matrix
- Activity List with expandable tower cards
- JSONBin.io cloud sync — all changes auto-saved
- CSV export
- Print-to-PDF support

---

## Roadmap (Phase 2 — target v6)

- Azure AD SSO replacing open access
- FastAPI + PostgreSQL on AKS replacing JSONBin
- Live data feed from DNAC, ISE, ServiceNow APIs
- RBA execution console with human-in-the-loop approval
- Audit trail (who, what, when) for every change
- Real-time notifications via webhooks
- Drill-through dashboard links
- ServiceNow webhook integration for auto-updating SOP Tracker progress

---

[5.0]: https://github.com/samrat-bang/GNS-AIOps-portal/releases/tag/v5.0
[4.0]: https://github.com/samrat-bang/GNS-AIOps-portal/releases/tag/v4.0
[3.0]: https://github.com/samrat-bang/GNS-AIOps-portal/releases/tag/v3.0
