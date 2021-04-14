# M300-Sicherheit

Es gibt verschieden arten wie man ein Container Sichern kann.
Darunter versteht man folgendes:
- Protokollieren & Überwachung
- Container sicherung & beschränken
- Kontinuierliche Integration

### Protokollieren

Wenn ein Container bereits läuft und Output herraus gibt und man möchten den wieder aus "printen" kann man den Befehl: docker logs <name des containers> ausführen und man erhält die ganze Ausgabe vom Container.


### Sicherung und Beschränkung

Jeder IT Mitarbeiter der mit Docker bereits gearbeitet hat, kann sich auf folgendes Einigen:
Man möchte das Image möglichst einfach und unkompliziert halten. Jedes Images hat seine Hauptaufgabe und das wars. Am besten sollten die Images von eigener Hand erstellt werden also via Dockerfile. Sich Images von der Cloud zu holen ist ansich nicht verboten, aber man muss stark darauf schauen das dieses Image sauber ist und nicht eventuell verseucht ist mit Schadsoftware.

Ein weiterer wichtiger Punkt sind die sogenannten Container Breakouts. Dass bedeutet gelingt es dem Angreifer vollen Zugriff zu erlangen, kann der durch einen "Ausbruch" vom Container auf dem Host zugreifen und hat somit vollen Server Zugriff.

Ebenfalls kann man folgende Schritte zur Ermöglichung der Abhertung:
- Load Balancer verwenden
- Images werden von non root definiert und gestartet ()$
- SELinux aktiviert
- Generelle überwachung der Container (Icinga) meldung werden erstellt falls komische Tätigkeiten geführt werden
- Speicher begrenzen
- CPU verteilung einsetzen


### Kontinuierliche Integration

- Gemeinsame Codebasis
- Automatisierte Übersetzung
- Kontinuierliche Test-Entwicklung
- Häufige Integration
- Integration in den Hauptbranch
- Kurze Testzyklen
- Gespiegelte Produktionsumgebung
- Einfacher Zugriff
- Automatisiertes Reporting
