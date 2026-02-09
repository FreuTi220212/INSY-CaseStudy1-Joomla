Reflexion: Herausforderungen & Learnings
Die technische Umsetzung des Projekts war durch drei zentrale Problemstellungen geprägt, die maßgeblichen Einfluss auf den Entwicklungsverlauf und die Systemarchitektur hatten:

1. Datenkonsistenz und Docker-Infrastruktur
Die Nutzung von Docker stellte uns vor Herausforderungen bei der Team-Kollaboration. Da die Datenbank in lokalen Volumes gekapselt war, konnte kein automatisierter Abgleich über das Versionskontrollsystem (GitHub) erfolgen.

Problem: Inkonsistente Datenstände zwischen den Entwicklern.

Lösung: Etablierung eines Workflows für manuelle Datenbank-Exporte und -Importe sowie die Optimierung der Container-Abhängigkeiten, um Start-Fehler der Dienste zu minimieren.

2. Software-Stabilität und Versionsmanagement
Der Einsatz der neuesten Joomla-Version (5.x) erwies sich aufgrund funktionaler Mängel als kontraproduktiv. Kritische Bugs im Workflow-Plugin sowie im UI-Rendering (verschwindende Buttons) behinderten die Implementierung der Kernprozesse. Zudem traten unvorhersehbare Permission-Fehler auf.

Konsequenz: Um die Projektabgabe nicht zu gefährden, wurde ein Downgrade auf die stabilere LTS-Version vollzogen. Dies unterstreicht das Learning, dass Stabilität in produktiven Umgebungen Vorrang vor der Nutzung neuester Features haben muss.

3. Konfiguration des Berechtigungssystems (ACL)
Das feingranulare Access Control List (ACL)-System von Joomla erforderte eine hohe Einarbeitungszeit. Das komplexe Zusammenspiel von „Allowed“, „Denied“ und „Inherited“ führte anfangs zu Fehlkonfigurationen im Freigabeprozess.

Learning: Eine präzise Dokumentation der Rollen-Matrix vor der technischen Umsetzung ist essenziell, um die Vererbung von Rechten innerhalb der Zugriffsebene fehlerfrei abzubilden.

Fazit
Das Projekt verdeutlichte die Notwendigkeit einer robusten Versionsstrategie. Die wichtigsten Erkenntnisse liegen im sicheren Umgang mit Docker-basierten Datenbanken, der Priorisierung von LTS-Software für geschäftskritische Workflows und der systematischen Konfiguration komplexer Berechtigungsstrukturen.