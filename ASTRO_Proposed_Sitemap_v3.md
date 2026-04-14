# ASTRO.org — Proposed Sitemap v3
**Project:** astro.org Redesign  
**Prepared by:** Alley Interactive  
**Last updated:** April 2026 — post IA session with Susan Finkelpearl  
**Status:** Working draft — 2 open decisions remaining  
**Previous version:** ASTRO_Proposed_Sitemap_v2.md

---

## What changed from v2 → v3

| Item | v2 | v3 | Reason |
|------|----|----|--------|
| Learn (top-level) | Standalone L1 item | Folded into Practice as "Learn & Certify" L2 | Education serves same practicing clinician audience |
| Journals | Inside Research & Journals | Anchor L2 inside Publications & News | Susan confirmed Journals as a key item; kept prominent |
| Society Communications | Proposed merge with Journals | "Society News" L2 inside Publications & News | Susan's grouping — preserved as distinct L2, not separate L1 |
| Meetings & Events | Inside Connect | Standalone L1 — Susan confirmed | Susan's confirmed anchor |
| Advocacy | Inside Connect | Standalone L1 — Susan confirmed | Susan's confirmed anchor |
| Connect (top-level) | Standalone L1 | Dissolved — contents distributed | Meetings & Events and Advocacy now standalone; Community moves to About & Join |
| Reimbursement | Listed as L3 items in dropdown | L2 item linking to landing page; sub-items on landing page only | Susan's progressive disclosure pattern |
| APEx Accreditation | Listed as L3 items in dropdown | L2 item linking to landing page | Same progressive disclosure pattern applied for consistency |

---

## OPEN DECISIONS (must resolve before Slickplan v3)

| # | Item | Question | Options |
|---|------|----------|---------|
| 1 | Publications & News label | Susan wants Journals distinct from Society News — what's the parent called? | "Publications & News" / "News & Journals" / "Publications" / other |
| 2 | State Regulations Library | Primary users are providers, lives in Advocacy | Keep in Advocacy / Move to Practice > Manage Your Practice / Cross-link both |
| 3 | Learn & Certify placement | Does education stay inside Practice or become its own L1? | Inside Practice (current v3) / Standalone "Learn" L1 (v2 approach) |

---

## UTILITY NAVIGATION
*5 items — simplified from current 9*

- Search
- For Patients → Speed of Light Foundation / RTAnswers [↗]
- Speed of Light Foundation [↗]
- Become a Member *(CTA button)*
- Welcome Back, [Name] ▾ *(logged-in dropdown)*
  - My Profile
  - ROhub [↗]
  - ASTRO Academy [↗]
  - Member Directory
  - Manage Membership
  - Newsletters
  - Log Out

---

## L0: HOME — astro.org

**Homepage audience pathways (above the fold — replaces carousel)**
- Radiation Oncologist → Guidelines, coding, CME, meeting registration
- Physicist / Dosimetrist → eContouring, technical standards, ASTRO Academy
- Resident / Student → Free membership, ARRO, career resources, mentorship
- Practice Administrator → Coding guidance, APEx accreditation, industry

---

## L1: MEETINGS & EVENTS
*Susan confirmed. No structural changes from v2.*

### L2: Annual Meeting
- Attend
- Learn
- Exhibitors
- Become an Exhibitor

### L2: Events
- Head & Neck Symposium
- RPT Symposium
- Annual Refresher Course
- Coding & Coverage Seminar
- Advocacy Day

---

## L1: PRACTICE
*Merges: Practice Support + Provider Resources + Education*  
*Organized by what clinicians are trying to DO*

### L2: Treat patients
- Clinical Practice Guidelines
- Collaborative Guideline Process
- Consensus Documents
- Guideline Development Process
- Patient Videos
- Patient Brochures
- Radiation Oncology Presentations
- RPT Roundtable
- AU Status for RPT
- RPT Learning Collaboratives

### L2: Manage your practice
- Reimbursement *(links to landing page)*
  - [On landing page:] Coding
  - [On landing page:] Medicare Resources
  - [On landing page:] Model Policies
  - [On landing page:] Practice Management Resources
  - [On landing page:] Private Payers

### L2: Improve quality
- RO-ILS
- Safety is No Accident
- Data Standards
- Quality Measures
- Functional Radiation Medicine
- Disaster Management
- APEx Accreditation *(links to landing page)*
  - [On landing page:] About APEx
  - [On landing page:] Accredited Facilities
  - [On landing page:] Application Process
  - [On landing page:] APEx Portal
  - [On landing page:] Become a Surveyor

### L2: Learn & certify
*[OPEN DECISION #3 — may become standalone L1]*
- ASTRO Academy [↗]
- Sessions on Demand
- Meetings on Demand
- eContouring
- Webinars
- Journal Activities
- Continuing Certification
- ASTRO ROCKS
- RO Communities Corner
- Past Meetings
- RPT in ASTRO Academy

---

## L1: PUBLICATIONS & NEWS
*[OPEN DECISION #1 — label TBD]*  
*Replaces: News and Publications*  
*Rationale: Journals and Society News are distinct content types but serve same reading behavior — one parent, two L2 groupings. Susan's distinction preserved at L2, not L1.*

### L2: Journals *(anchor — featured first in dropdown)*
- Red Journal
- Practical Radiation Oncology (PRO)
- Advances in Radiation Oncology
- Journal News
- Author Instructions

### L2: Society news *(Susan's grouping)*
- ASTROgram
- ASTROblog
- ASTROnews
- President's Corner
- Podcasts

### L2: News & media
- News Releases
- Press Kits
- Media Resources
- Media Experts

### L2: Research
- Funding Opportunities
- Professional Development

---

## L1: ADVOCACY
*Susan confirmed. No structural changes from v2.*

### L2: Key issues
- Radiation Oncology Case Rate Program
- Cancer Research
- Access to Care
- Source Security
- Obtaining AU Status
- Disparities in Health Care

### L2: What's happening in Washington
*(Editorial feed / landing page — no sub-items in dropdown)*

### L2: Become an advocate
- Resources
- Key Legislation
- Patient Stories [↗]

### L2: ASTRO PAC
- PAC Donors
- PAC Toolkit
- Donate Now
- PAC Board

### L2: State Regulations Library
*[OPEN DECISION #2 — may move to Practice > Manage Your Practice]*

---

## L1: ABOUT & JOIN
*Promoted from footer-only*

### L2: About ASTRO
- Mission & Vision
- Board & Leadership
- Governance
- History
- What is Radiation Oncology?
- Jobs at ASTRO

### L2: Membership
- Why Join ASTRO *(value prop page)*
- Categories & Benefits
- Renew Membership
- ASTRO Policies
- Demographics
- Workforce
- Recognition Awards

### L2: Career pathways
- Medical Students (free membership)
- Residents — ARRO
- Early Career
- Established Practitioners
- Career Center

### L2: Community
- ROhub [↗]
- Physician Networking
- International Members
- ADROP
- SCAROP
- Industry

---

## FOOTER (retained)
- Advertising
- Terms of Use & Privacy Policy
- Contact Us
- Connect With Us
- Cookie Settings

---

## FOR CLAUDE CODE — HTML PROTOTYPE NOTES

When building the HTML prototype from this sitemap, prioritize these templates:

### Priority 1 — Navigation shell
- Desktop mega menu with 5 L1 items
- Each L1 opens a dropdown showing L2 groupings as column headers
- L3 items listed under each L2 header
- Utility nav bar above with 5 items
- Logged-in state for Welcome Back dropdown
- Mobile hamburger menu with accordion pattern for L1 → L2 → L3

### Priority 2 — Homepage
- Utility nav
- Primary nav
- Hero: 4 audience pathway cards (no carousel)
- Quick-link bar for most common tasks
- Featured content sections below fold

### Priority 3 — Progressive disclosure landing pages
- Reimbursement landing page (shows Coding, Medicare, Model Policies, Practice Management, Private Payers as cards)
- APEx Accreditation landing page (shows all 5 sub-items as cards with descriptions)

### Design tokens to apply
- Primary blue: #185FA5
- Dark blue: #0C447C  
- Green: #27500A
- Pink/burgundy: #72243E
- Amber: #633806
- Purple: #3C3489
- Teal CTA (Become a Member): #0F6E56
- Nav background: white
- Dropdown background: white with subtle shadow
- Body font: system sans-serif stack

### Key UX behaviors to prototype
- Mega menu opens on hover (desktop), tap (mobile)
- Active/current section highlighted in nav
- Welcome Back dropdown shows member-specific links
- Audience pathway cards on homepage are clickable
- Mobile: hamburger → full-screen overlay → accordion L1 items

---

*Use this file as the single source of truth for the HTML prototype.*  
*Resolve open decisions 1–3 before finalizing nav labels in code.*
