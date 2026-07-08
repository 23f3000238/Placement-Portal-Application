# Placement-Portal-Application



**Placement Portal Application V2** is a full-stack campus recruitment management system that digitizes and streamlines the entire college placement process — from company onboarding to student job applications and final selections.

Built as part of the IIT Madras BS Degree Modern Application Development II course project, it replaces the typical spreadsheet/email-based coordination with a structured, role-based web platform. Three types of users interact with the system: the **Admin** (institute placement cell), **Companies** (recruiters), and **Students** (job seekers).

The admin approves company registrations and placement drives before they go live, keeping the process gated and trustworthy. Companies can then post drives, review applicants, shortlist candidates, schedule interviews, and mark final selections — all from a dedicated dashboard. Students browse approved drives filtered by their eligibility (CGPA, branch, year), apply in one click, and track every stage of their application in real time.

Under the hood, **Celery + Redis** power three background jobs: daily email reminders to students about closing deadlines, an automated monthly placement report sent to the admin on the first of each month, and an async CSV export that lets students download their full application history. **Redis caching** is also used to speed up frequently hit API endpoints.

The stack follows the course requirements exactly — **Flask** for the REST API, **Vue.js 3** (Composition API + Pinia) for the frontend, **Bootstrap 5** for styling, **SQLite** for the database (created entirely via SQLAlchemy models, no manual setup), and **JWT-based** role-aware authentication.
