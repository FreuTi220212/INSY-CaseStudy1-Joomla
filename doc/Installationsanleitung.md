# **Installationsschritte**

## 1. Repository clonen
```bash
git clone https://github.com/FreuTi220212/INSY-CaseStudy1-Joomla.git
cd INSY-CaseStudy1-Joomla
```

## 2. Docker starten

Falls **Docker Desktop** verwendet wird, dieses zuerst öffnen.
```bash
docker compose up -d
```

⏳ *Warte ca. 1 Minute bis alle Container laufen*

## 3. Datenbank importieren

**Container-Name finden:**
```bash
docker ps
```
Suche den Container mit `-joomladb-1` oder `-db-1` am Ende.

**Backup importieren** (ersetze `[CONTAINER_NAME]`):
```bash
docker exec -i [CONTAINER_NAME] mariadb -u root -proot_password_2024 joomla_db < backup.sql
```

**Beispiel:**
```bash
docker exec -i joomla_db mariadb -u root -proot_password_2024 joomla_db < backup.sql
```

## 4. Joomla öffnen

- **Frontend:** http://localhost:8080
- **Backend:** http://localhost:8080/administrator
- **phpMyAdmin:** http://localhost:8081 *(optional)*

## Login-Daten

**Administrator:**
- User: `admin`
- Passwort: `admin1234567`

**Redakteur:**
- User: `redakteur1`
- Passwort: `redakteur123`