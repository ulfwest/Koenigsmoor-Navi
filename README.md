# Koenigsmoor-Navi
Wege zur Parzelle – Wegweiser für den Campingplatz Königsmoor.

**Öffnen:** `index.html` im Browser (zusammen mit `lageplan.png` im selben Ordner).

## Funktionen
- **Suche:** Leeres Feld zeigt alle 17 Wege, Tippen filtert (auch Teilwörter wie „gin“). Ein Treffer zoomt den Plan auf den Weg.
- **Route (➜):** Von–Nach mit kürzestem Weg (als Fußspuren), Entfernung und Gehzeit; ⇅ tauscht Start und Ziel.
- **Reiter Suchen / Route / Info** oben; bei Route stehen Von und Nach untereinander.
- **Parzellen:** Nummer in die Suche tippen („12“, „Rosenweg 12“); Treffer zeigen den nächstgelegenen Weg, „Route hierher“ führt hin.
- **Info:** Wichtige Rufnummern (antippen zum Anrufen), alle Gebäude, Teiche und Plätze.
- **Brandschutzflächen:** Alle 28 rot markierten Parzellen werden auf Wunsch rot blinkend umkreist (Info → Brandschutz oder Suche „brand“).
- **Entfernungen:** Jede Liste zeigt ca. Meter ab Eingang; Weglängen geschätzt und auf 10 m gerundet.

## Wege
Amselweg, Birkenweg, Cliviaweg, Drosselweg, Erlenweg, Fasanenweg, Ginsterweg, Habichtsweg, Igelweg, Kuckucksweg, Lilienweg, Meisenweg, Nelkenweg, Primelweg, Rosenweg, Sonnenweg, Tulpenweg

## Annahmen / offen
- Maßstab 0,57 m pro Planpixel (aus dem Satellitenfoto anhand geparkter Autos ermittelt, ca. ±15 %), Gehtempo 4 km/h. Anpassen über `M_PER_PX` und `WALK_KMH` in `index.html`.
- Die unbenannten Verbindungsstücke (`LINKS`) sollten vor Ort geprüft werden.
- Der Lageplan liegt als hochaufgelöstes `lageplan.png` (2000×1415 px) vor; die Weg-Koordinaten bleiben im 820×580-Raster.

## Als App installieren (PWA)
- **Android (Chrome):** Seite öffnen → Hinweis „App installieren“ bzw. **⋮ → App installieren**.
- **iPhone (Safari):** Seite öffnen → **Teilen → Zum Home-Bildschirm**.
- Danach startet der Wegweiser mit eigenem Symbol ohne Browserleiste und funktioniert auch **offline**.
- **Teilen:** Knopf „Teilen“ bei jedem Weg, Ort oder jeder Parzelle schickt einen Direktlink (`?ziel=…`), „App teilen“ im Info-Reiter den App-Link.
- `qr-plakat.png` (A4) zum Ausdrucken und Aufhängen am Eingang.
- Technik: `manifest.webmanifest`, `sw.js` (Offline-Speicher; bei Änderungen `VERSION` erhöhen), Symbole in `icons/`.
