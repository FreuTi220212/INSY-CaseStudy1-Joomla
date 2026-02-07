# **Installationsschritte**

1. Github Repo clonen oder mit pull aktualisieren

    - clone

    ```
    git clone https://github.com/FreuTi220212/INSY-CaseStudy1-Joomla.git
    ```

    - pull

    ```
    git pull
    ```

2. Docker und container starten

    - Wenn Docker Desktop genützt wird, den zuerst öffnen

    - Dann Container starten mit 

    ```
    docker compose up -d
    ```

3. Den Namen des Datenbank-Containers finden

    Da der Name vom Ordnernamen abhängt, muss man kurz checken, wie der Container heißt:

    PowerShell:

    ```
    docker ps
    ```

    Man sucht den Namen unter NAMES, der auf -db-1 endet.

    Zum Beispiel

    ```
    insy-casestudy1-joomla-db-1
    ```

4. Die Daten importieren

    PowerShell: 
    
    ```
    docker cp ./backup.sql [DB_CONTAINER_NAME]:/var/lib/mysql/backup.sql
    ```

    Zum Beispiel

    ```
    docker cp ./backup.sql insy-casestudy1-joomla-db-1:/var/lib/mysql/backup.sql
    ```

    Dann SQL-Befehl zum Importieren ausführen

    ```
    docker compose exec -T db /usr/bin/mysql -u root -proot joomla_db -e "source /var/lib/mysql/backup.sql"
    ```

5. Homepage und Administrator Login öffnen

    Browser: 

    ```
    localhost:8080
    ```

    ```
    localhost:8080/administrator
    ```