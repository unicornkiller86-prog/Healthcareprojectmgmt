# Healthcare Clinic Project Management System

This repository now contains a practical starter system to run multi-site healthcare operations, with a focus on **ketamine clinic workflows**.

## What this system helps you manage

- Project portfolio for clinic initiatives (openings, accreditation, EHR updates, payer enrollment)
- Policy and procedure governance with review cadences
- Internal communication and accountability loops
- Finance tracking (revenue, cost centers, budget variance)
- Staffing operations (headcount, onboarding, competencies, schedules)
- Supply chain and inventory controls for clinical and non-clinical items

## Repository structure

- `docs/system-blueprint.md` → operating model, roles, workflows, KPIs
- `templates/projects/project-portfolio.csv` → project intake and status
- `templates/policies/policy-register.csv` → policy lifecycle and ownership
- `templates/communication/internal-comms-log.csv` → internal communication tracking
- `templates/finance/monthly-finance-dashboard.csv` → monthly financial management
- `templates/staff/staff-roster-and-competency.csv` → staffing and competency matrix
- `templates/supplies/supply-inventory-par-levels.csv` → inventory and reorder governance

## Quick start (30–60 minutes)

1. Populate each CSV template with your current clinic data.
2. Assign one accountable owner per template.
3. Start a weekly operations review using these files as the single source of truth.
4. Add a monthly quality-and-finance review cadence.
5. Review policy expiry dates and set reminders before due dates.

## Recommended cadence

- **Daily (15 min):** safety, staffing, and supply huddle
- **Weekly (45–60 min):** project and operations review
- **Biweekly (30 min):** policy/procedure and training compliance review
- **Monthly (60–90 min):** finance dashboard and KPI review

## Important note

This package is for operational management only and does not replace legal, clinical, billing, privacy, or regulatory advice. Validate all policies against applicable federal/state requirements and your medical director's standards.


## Deployment

If you are asking "how do I deploy this now," start with `docs/deployment-guide.md`:

- Immediate deployment path (docs + CSV operations workspace)
- Security and access-control minimums
- Next-phase web app deployment path (Next.js + Supabase)

See: `docs/deployment-guide.md`.
