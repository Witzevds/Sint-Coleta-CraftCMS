# Sint-Coleta CraftCMS

## Snel starten

1. **Clone deze repo**
2. **Installeer DDEV** (zie https://ddev.com/)
3. **Start project**
   ```bash
   ddev start
   composer install
   ```
4. **Importeer database**
   ```bash
   ddev import-db --src=docs/db/dump.sql
   ```
5. **Assets**
   Alle uploads en assets staan in `web/uploads/` en `web/assets/` en worden meegepusht. Je hoeft niets extra te downloaden.

## Inloggen Craft
- Ga naar `/admin` (standaard: `http://localhost:8080/admin`)

## Opmerkingen
- Project config en content zijn direct up-to-date na import.
- Zie `docs/DB_EXPORT_GUIDE.md` voor export/import tips.
- Zie `docs/SUBMISSION_CHECKLIST.md` voor de laatste controle.

## Contact
- Vragen? Mail: witzevds@gmail.com
