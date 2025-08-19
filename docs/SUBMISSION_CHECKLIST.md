# Submission Checklist (School Project)

Use this list to prepare everything before you submit.

- GitHub repo URL + tag of final commit (e.g. v1.0):
  - Repo: <paste>
  - Tag: <paste>
- Design & Wireframes
  - Figma/XD link with view access: <paste>
  - Optional: export PDF of key screens in `/docs/design/`
- Database Schema (ERD)
  - Screenshot/PDF of tables and relations in `/docs/db/`
  - How: phpMyAdmin (Designer) screenshot, or use TablePlus/Sequel Ace export to PDF
- Database Export (content)
  - Place `dump.sql.gz` (or `.sql`) in `/docs/db/`
  - How (choose one):
    - Craft Control Panel → Utilities → Backups → Create a backup
    - DDEV: `ddev export-db -f docs/db/dump.sql.gz`
- Video Screencast (~5 min)
  - Put final video in `/docs/video/` or upload to the LMS and paste link here: <paste>
  - Outline (recommendation):
    1) Homepage + navigatie
    2) Dienstverlening + detail
    3) Residentiële ouderenzorg
    4) Vacatures (lijst + detail)
    5) Werknemers filter (slugs + autosubmit)
    6) Kort over Project Config & assets
- Online URL (indien relevant)
  - https://<your-site>

## Local run (teacher/dev)
- Requirements: Docker + DDEV (of eigen PHP/MySQL omgeving)
- Stappen (DDEV):
  1) `ddev start`
  2) `composer install`
  3) (optioneel) `ddev import-db --src=docs/db/dump.sql.gz`
  4) Site openen via `ddev describe` URL

## Notes (Rubric mapping)
- Data & database: project config + db export + schema bijgevoegd
- Front-end/design: responsive pages, accentkleuren (#ee7919, #cab37f)
- Backend: Craft sections/fields + filters (werknemers), detailpagina’s
- Code kwaliteit: gestructureerde Twig + CSS, pagina-specifieke styles
- Presentatie: 5-min screencast volgens outline
- Q&A: README + docs voor installatie en data
