## **Installationsschritte**

1. Projekt aktualisieren bzw. Github Repo clonen

https://github.com/FreuTi220212/INSY-CaseStudy1-Joomla

Zuerst holt man sich den neuesten Stand (inklusive der backup.sql):

PowerShell: git pull

2. Container starten

Es fährt die Umgebung
hoch. Wenn es schon läuft, schadet ein Neustart nicht:

PowerShell: docker compose up -d

3. Den Namen des Datenbank-Containers finden

Da der Name vom Ordnernamen abhängt, muss man kurz checken, wie der Container heißt:

PowerShell: docker ps (Man sucht den Namen unter NAMES, der auf -db-1 endet).

4. Die Daten importieren

PowerShell: docker cp
./backup.sql [DB_CONTAINER_NAME]:/var/lib/mysql/backup.sql

SQL-Befehl zum Importieren ausführen

PowerShell: docker compose exec -T db /usr/bin/mysql -u root -proot joomla_db -e "pfad"/mysql

5. Homepage öffnen

Browser: localhost:8080
