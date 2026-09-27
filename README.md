# Speicher-Ledger

Eine Web-App (PWA), die dich mit einer Checkliste durch die typischen
Speicherfresser auf deinem Handy führt – Fotos, Apps, Downloads, Chat-Anhänge,
Cache. Läuft im Browser, lässt sich aber wie eine echte App auf den
Homescreen legen und funktioniert danach auch offline.

**Wichtig zu wissen:** Eine Web-App darf aus Sicherheitsgründen (bei iPhone
und Android gleichermaßen) nicht auf deine Fotos, Apps oder Dateien
zugreifen und nichts automatisch löschen. Diese App zeigt dir stattdessen,
wo du selbst nachsehen solltest, und merkt sich deinen Fortschritt.

## 1. Auf GitHub hochladen

1. Erstelle ein neues Repository auf [github.com](https://github.com/new),
   z. B. `speicher-ledger`. Öffentlich ("Public") muss es sein, damit GitHub
   Pages kostenlos funktioniert.
2. Lade alle Dateien aus diesem Ordner hoch (per Drag & Drop im Browser
   reicht: Repository öffnen → "Add file" → "Upload files").
3. Gehe zu **Settings → Pages**.
4. Bei "Source" wähle **Deploy from a branch**, Branch **main**, Ordner **/ (root)**.
   Speichern.
5. Nach ein bis zwei Minuten ist die App erreichbar unter:
   `https://DEIN-BENUTZERNAME.github.io/speicher-ledger/`

## 2. Auf dem iPhone installieren

1. Öffne den Link oben in **Safari** (nicht Chrome – "Zum Home-Bildschirm"
   funktioniert auf iOS nur in Safari).
2. Tippe auf das Teilen-Symbol (Quadrat mit Pfeil nach oben).
3. Wähle **„Zum Home-Bildschirm"**.
4. Fertig – die App liegt jetzt als Icon auf dem Homescreen und startet ohne
   Browser-Leiste.

## 3. Auf Android installieren

1. Öffne den Link in **Chrome**.
2. Tippe oben rechts auf das Menü (⋮).
3. Wähle **„App installieren"** (oder „Zum Startbildschirm hinzufügen").
4. Fertig – die App erscheint im App-Drawer wie eine normale App.

## Dateien in diesem Projekt

| Datei | Zweck |
|---|---|
| `index.html` | Die gesamte App (HTML, CSS, JS in einer Datei) |
| `manifest.json` | Macht die Seite auf dem Homescreen installierbar |
| `service-worker.js` | Speichert die App für die Offline-Nutzung zwischen |
| `icon-192.png`, `icon-512.png` | App-Icons für Android |
| `apple-touch-icon.png` | App-Icon für iOS |

## Anpassen

Alle Kategorien und Aufgaben stehen am Anfang des `<script>`-Blocks in
`index.html` im Array `DATA` – dort lassen sich Texte, Tipps oder ganze
Kategorien ändern, ohne den Rest des Codes anzufassen. Der Fortschritt wird
lokal im Browser (localStorage) gespeichert, pro Gerät getrennt.
