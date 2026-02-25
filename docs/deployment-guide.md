# Deployment Guide

Right now this repository is a **documentation + CSV operations system**, not an executable application. So "deployment" means putting these files somewhere your team can use them consistently and securely.

## Option 1 (Fastest): Deploy as an internal operations workspace (recommended this week)

### 1) Create a private GitHub repository
- Push this repo to a private organization repo.
- Restrict access to leadership and role-based staff.
- Enable branch protection for `main` and require PR review.

### 2) Add operational access paths
- Keep the source-of-truth files in GitHub.
- Mirror each CSV into Google Sheets or Airtable for non-technical staff updates.
- Keep versioned policy files in a secured document system (SharePoint/Google Drive) and store links in `policy-register.csv`.

### 3) Automate reminders (no-code)
- Use Zapier/Make/Power Automate to send reminders for:
  - policy review due dates
  - credential expirations
  - below-par inventory items
  - overdue project milestones

### 4) Run the management cadence
- Daily: site huddle using comms + staffing + supplies sheets.
- Weekly: project portfolio and open blocker review.
- Monthly: finance and KPI review.

### 5) Security / compliance minimums
- Use SSO + MFA for all systems.
- Restrict PHI in trackers (use IDs, not full patient-identifying details).
- Apply least-privilege access and audit logs.

---

## Option 2: Deploy as a web app (recommended next phase)

If you want dashboards, role-based login, and workflows, deploy a simple app stack:

- **Frontend:** Next.js (Vercel)
- **Database/Auth:** Supabase (Postgres + Row Level Security)
- **Storage:** Supabase Storage / S3 for policy docs
- **Automation:** Supabase scheduled functions or n8n

### Suggested rollout
1. Build database tables matching current CSV schemas.
2. Import existing CSV data.
3. Add auth roles: Executive, Ops, Site Manager, Finance, HR, Clinical Lead.
4. Build views:
   - Executive dashboard (KPI + risks)
   - Site dashboard (staffing/supplies/actions)
   - Finance dashboard (budget variance)
   - Policy dashboard (review/expiry calendar)
5. Add notifications for due dates and escalations.
6. Enable backups, audit logging, and environment separation (dev/stage/prod).

---

## Concrete deployment checklist

- [ ] Private repo created and populated
- [ ] Owners assigned for each template
- [ ] Team edit/view permissions configured
- [ ] Reminder automations enabled
- [ ] Weekly and monthly meeting cadence started
- [ ] KPI baseline captured
- [ ] Security controls verified (MFA, access reviews, audit logs)

---

## What to do right now (today)

1. Put the CSV templates into Google Sheets tabs by function.
2. Assign one accountable owner per tab.
3. Fill current-state data for all clinic sites.
4. Schedule a 45-minute weekly operations review.
5. Review this setup after 2 weeks, then decide whether to proceed to the web app phase.
