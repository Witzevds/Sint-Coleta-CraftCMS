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
