# Contributing to GNS AIOps Portal

> Workflow guide for the GNS AIOps team to safely add, edit, and update the portal.

---

## Two types of changes

### 1. Data changes — done in the portal itself

Adding / editing / deleting **use cases, volume entries, SOP tracker rows, ATK calculator entries** — all of this is done by users directly in the live portal. Changes auto-save to JSONBin and sync to all 37 team members.

**No GitHub action needed.** Just open the live URL and use the UI.

### 2. Code changes — done via GitHub

Adding new sections, fixing bugs, restyling, adding features — these touch `index.html` and need a Git commit.

---

## Code change workflow

### Option A — Edit directly on GitHub (simple changes)

1. Navigate to `index.html` on GitHub
2. Click the pencil icon (✏️) — Edit this file
3. Make your changes
4. Scroll down → write a clear commit message like:
   - `Fix: SOP Tracker filter not respecting sub-tower selection`
   - `Add: Phase 2 roadmap section to Upgrade Path page`
   - `Update: Leadership Summary KPI thresholds`
5. Click **Commit changes**
6. Wait 1–2 minutes for GitHub Pages to rebuild
7. Hard refresh (`Ctrl+Shift+R`) the live URL to verify

### Option B — Local clone (complex changes)

```bash
git clone https://github.com/samrat-bang/GNS-AIOps-portal.git
cd GNS-AIOps-portal
# Open index.html in VS Code
# Make changes
# Test by opening index.html directly in Chrome
git add index.html
git commit -m "Description of change"
git push origin main
```

---

## Branch protection (recommended for Phase 2)

When the team grows beyond Samrat as sole maintainer, enable branch protection:

1. **Settings → Branches → Add rule** for `main`
2. ✓ Require pull request before merging
3. ✓ Require approvals: **1**
4. ✓ Dismiss stale approvals when new commits are pushed

Then contributors work on feature branches:

```bash
git checkout -b feature/audit-trail
# make changes
git push origin feature/audit-trail
# Open Pull Request on GitHub → request review → merge
```

---

## Commit message style

Use clear prefixes — makes the changelog easy to write:

| Prefix | Use for |
|---|---|
| `Add:` | New section, new feature, new data |
| `Update:` | Modifying existing behaviour or content |
| `Fix:` | Bug fix |
| `Refactor:` | Code cleanup with no behaviour change |
| `Docs:` | README, CHANGELOG, this file |
| `Style:` | CSS-only changes |

**Example:**
```
Add: Phase 2 roadmap with Azure AD SSO and FastAPI migration
```

---

## Testing checklist before commit

Open `index.html` in Chrome and check:

- [ ] No console errors (F12 → Console tab → should be clean)
- [ ] JSONBin syncs — add a test entry, refresh page, entry persists
- [ ] All sidebar sections load without breaking
- [ ] CSV + Word export still works for affected section
- [ ] View / Edit / Delete actions function on edited section
- [ ] Modal close buttons work (X, Close, click-outside, Esc)
- [ ] Print preview renders (`Ctrl+P`) — leadership view especially

---

## Releases

When making a significant release (a `v5.1`, `v5.2`, `v6.0`):

1. Update `index.html` with all changes
2. Update `CHANGELOG.md` — move items from "Unreleased" to a new version section
3. Update `README.md` if section list changed
4. Commit everything with message `Release v5.x`
5. **Create a Git tag:**
   ```bash
   git tag -a v5.1 -m "Release v5.1 — audit trail + drill-through dashboard"
   git push origin v5.1
   ```
6. On GitHub → **Releases → Draft a new release** → pick the tag → publish

This gives the team a clean version history they can roll back to.

---

## Data backup

JSONBin free plan has rate limits. To protect against bin deletion or corruption:

**Weekly backup procedure (Prathap to own):**

1. Visit https://jsonbin.io/app/dashboard
2. Open bin `6a066dc2c0954111d825db8e`
3. Click **Download** to save the JSON locally
4. Commit to `/backups/YYYY-MM-DD.json` in this repo

---

## Questions or issues?

- **Programme questions** → Samrat Paul
- **Technical Lead** → Prathap
- **AI Development** → Madhan Babu
- **Architecture / Phase 2** → Pragash Subramanian
