# Airline-Radar

Neue, geänderte und gestrichene Strecken sowie Flottenänderungen von Condor und Sunclass Airlines.

## Abfragen

Die Seite läuft über GitHub Pages. Oben wählst du die Airlines und den Bereich (Flotte und Routen, nur Flotte, nur Routen). Die Auswahl steht im Link und lässt sich als Lesezeichen speichern:

- `?bereich=flotte` zeigt nur die Flotte beider Airlines
- `?airlines=condor&bereich=routen` zeigt nur die Routen von Condor
- `?airlines=sunclass` zeigt Flotte und Routen von Sunclass

## Aufbau

- `index.html` ist die Seite
- `data/airlines.json` listet die Airlines (Kennung und Anzeigename)
- `data/<kennung>.json` enthält je Airline `routen` (`neu`, `weg`), `flotte` (`bestand`, `plus`, `minus`), `log` und `quellen`

Eine weitere Airline kommt dazu, indem du eine Datei `data/<kennung>.json` im gleichen Aufbau anlegst und sie in `data/airlines.json` einträgst.

## Aktualisierung

Eine wöchentliche geplante Aufgabe recherchiert neu und committet geänderte Dateien in `data/`.

## Einrichtung

Settings, Pages, Source: Deploy from a branch, Branch `main`, Ordner `/ (root)`.
