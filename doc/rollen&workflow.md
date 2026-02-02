## **1. Projektüberblick**

Für die studentischen
Clubs wird eine lokal betriebene Website auf Basis eines CMS bereitgestellt.  
Die Website dient zur Darstellung der Clubs sowie zur Veröffentlichung von
Berichten über Clubaktivitäten.  
Ein kontrollierter Freigabeprozess stellt sicher, dass Inhalte erst nach
Prüfung veröffentlicht werden.

---

## **2. Rollen &Berechtigungen**

**Administrator**

- Vollzugriff auf das CMS
- Verwaltung von Benutzern und Rechten
- Prüfung und Freigabe von Berichten
- Veröffentlichung und ggf. Bearbeitung
   freigegebener Inhalte
- Systemadministration (Backup, Einstellungen,
   Sicherheit)

**Redakteur**

- Erstellung und Bearbeitung **eigener** Berichte
- Hochladen von Texten und optional Bildern
- Keine Veröffentlichungsrechte
- Einsicht in den Status der eigenen Berichte
   (Entwurf / zur Prüfung / freigegeben)

---

## **3. Workflow: Berichtserstellung & Freigabe**

1. **Anmeldung**
- Redakteur meldet sich im Backend des CMS an.
3. **Bericht erstellen**
- Redakteur erstellt einen neuen Bericht.

- Inhalte: Titel, Text, optional Bilder.

- Bericht wird als *Entwurf* gespeichert.
5. **Zur Prüfung einreichen**
- Redakteur markiert den Bericht als *zur
   Freigabe*.

- Der Bericht ist nun für den Administrator
   sichtbar.
7. **Prüfung durch Administrator**
- Administrator überprüft Inhalt, Form und
   ggf. Bilder.

- Entscheidung:

- **Freigabe** → Bericht wird veröffentlicht.

- **Ablehnung / Überarbeitung** → Bericht bleibt unveröffentlicht,
   Redakteur kann nachbessern.
9. **Veröffentlichung**
- Freigegebene Berichte erscheinen automatisch
   im Frontend im Bereich „Berichte“, sortiert nach Datum.

---

**4. Frontend-Logik**

- Übersicht aller Clubs
- Detailseiten je Club
- Berichtsbereich mit chronologischer oder
   archivierter Ansicht
- Nur freigegebene Berichte sind öffentlich
   sichtbar

---

**5. Erweiterbarkeit
(Ausblick)**

- Kommentarfunktion für Berichte
- Kategorien oder Tags für Clubs und Berichte
- Benachrichtigungssystem für Freigaben
- Mehrsprachigkeit
