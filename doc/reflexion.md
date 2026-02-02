## Reflexion: Herausforderungen & Learnings

Eine zentrale Herausforderung im Projekt war der Umgang mit der Datenbank innerhalb der Docker-Umgebung. Da die Datenbank in einem Docker-Volume gespeichert ist, konnte sie nicht direkt über GitHub geteilt werden, was zu Problemen bei der Zusammenarbeit führte. Erst durch manuelle Datenbank-Exporte und -Importe konnte ein einheitlicher Projektstand hergestellt werden. Zusätzlich traten Schwierigkeiten auf, wenn Container noch nicht vollständig gestartet waren oder Dienste unerwartet stoppten.

Auch das Rechte- und Rollensystem von Joomla stellte eine Herausforderung dar. Die sehr feingranulare Struktur bietet zwar große Flexibilität, ist jedoch komplex und fehleranfällig. Besonders das Zusammenspiel von „Allowed“, „Denied“ und „Inherited“ musste durch mehrfaches Testen verstanden werden, um den gewünschten Freigabe-Workflow korrekt umzusetzen.

Insgesamt zeigte das Projekt, dass Joomla ein leistungsfähiges, aber vergleichsweise komplexes CMS ist, das eine strukturierte Herangehensweise und gute Dokumentation erfordert. Als wichtigste Learnings ergaben sich ein besseres Verständnis für Docker-basierte Systeme, Datenpersistenz sowie die Bedeutung von sauber konfigurierten Benutzerrechten und klarer Teamkommunikation.
