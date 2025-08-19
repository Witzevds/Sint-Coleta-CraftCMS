<<<<<<< HEAD
# Sint-Coleta-CraftCMS

## Installatie en setup

1. Installeer Composer dependencies:
	```sh
	composer install
	```

2. Kopieer het voorbeeld .env-bestand:
	```sh
	cp .env.example .env
	```
	Pas de waarden in `.env` aan naar jouw omgeving (database, url, enz).

3. Importeer de database (optioneel):
	```sh
	ddev import-db --file=dump.sql
	```

4. Pas de project-config toe:
	```sh
	ddev exec php craft project-config/apply
	```

5. Herstart DDEV (indien nodig):
	```sh
	ddev restart
	```

6. Open de site in je browser:
	```
	http://<projectnaam>.ddev.site
	```
=======
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
>>>>>>> a73a9159eddf70060ccbb1f0b9f4a3564bbab9ea
