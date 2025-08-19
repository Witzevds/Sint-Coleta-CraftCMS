# DB Export & Import (Craft CMS)

## Export (lokaal)
Kies één methode:

1) Craft Control Panel
- Ga naar Utilities → Backups → Create a backup → download `.sql.gz`
- Zet het bestand in `docs/db/dump.sql.gz`

2) DDEV
- `ddev export-db -f docs/db/dump.sql.gz`

3) phpMyAdmin / Sequel Ace / TablePlus
- Exporteer de database als `UTF-8`, structuur + data, compatibel met MySQL 5.7+ of MariaDB.

## Import (server of testomgeving)
- Maak een lege database aan en stel `.env` in (DB_DATABASE, DB_USER, DB_PASSWORD, DB_SERVER, DB_PORT)
- Importeer de dump:
  - DDEV: `ddev import-db --src=docs/db/dump.sql.gz`
  - phpMyAdmin: Import → kies het bestand → Go
- `composer install`
- Project Config toepassen (indien nodig): `./craft project-config/apply` of via CP → Utilities → Project Config
- Cache legen: CP → Utilities → Clear Caches

## Assets meenemen
- Kopieer mappen voor uploads (bv. `web/uploads`, `web/assets`, `web/cpresources` indien nodig)
- Controleer volume-instellingen (config/project/volumes) en Base URL’s per environment

## Veelvoorkomende issues
- Foute BASE_URL voor volumes → pas `.env` of `config/general.php` per omgeving aan
- SECURITY_KEY ontbreekt → voeg toe in `.env`
- Migraties wachten → run `./craft migrate/all`
