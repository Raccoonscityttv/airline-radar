# Airline-Radar

Neue, geänderte und gestrichene Strecken sowie Flottenänderungen von Condor und Sunclass Airlines.

## Abfragen

Die Seite läuft über GitHub Pages und zeigt alle Einträge in einer Liste.

- **Suche:** Das Suchfeld durchsucht Strecke, Flughafen, Flugzeug, Datum, Frequenz, Hinweis und Airline. Mehrere Wörter gelten gemeinsam (`hurghada stuttgart`). Treffer sind markiert. Auf dem Computer springt die Taste `/` ins Suchfeld.
- **Filter:** Airline (eine oder beide), Bereich (Alle, Routen, Flotte) und Status (Neu, Geändert, Entfällt). Die Zahlen an den Status-Filtern zeigen, wie viele Einträge es jeweils gibt.
- **Details:** Ein Tipp auf eine Zeile zeigt Frequenz und Hinweis. „Alle aufklappen“ öffnet alles.
- **Lesezeichen:** Die Auswahl steht im Link, zum Beispiel `?airlines=condor&bereich=routen&q=hurghada` oder `?status=cut`.

## Selbst aktualisieren

Auf `edit.html` (Link unten auf der Seite) kannst du Strecken, Flugzeuge und Bestand hinzufügen, ändern und löschen. „Änderungen veröffentlichen“ speichert direkt ins Repo, die Seite aktualisiert sich nach ein bis zwei Minuten.

Einmalig brauchst du einen GitHub-Zugangsschlüssel: GitHub, Settings, Developer settings, Personal access tokens, Fine-grained tokens. Nur Repo `airline-radar` auswählen, Berechtigung Contents auf „Read and write“. Der Schlüssel wird nur im Browser gespeichert.

## Aufbau

- `index.html` ist die Seite
- `edit.html` ist die Bearbeitungsseite
- `data/airlines.json` listet die Airlines (Kennung und Anzeigename)
- `data/<kennung>.json` enthält je Airline `routen` (`neu`, `weg`), `flotte` (`bestand`, `plus`, `minus`), `log` und `quellen`

Eine weitere Airline kommt dazu, indem du eine Datei `data/<kennung>.json` im gleichen Aufbau anlegst und sie in `data/airlines.json` einträgst.

## Aktualisierung

Eine wöchentliche geplante Aufgabe recherchiert neu und committet geänderte Dateien in `data/`.

## Einrichtung

Settings, Pages, Source: Deploy from a branch, Branch `main`, Ordner `/ (root)`.
