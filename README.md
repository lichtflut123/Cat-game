# Pfotenjagd 🐾

Ein Tablet-Spiel **für Katzen**: Beute huscht über den Bildschirm, die Katze jagt sie mit der Pfote.
Jeder Fang wird mit einem Geräusch und einem kleinen Funkenregen belohnt.

## Spielen

`index.html` im Browser öffnen, am besten auf einem Tablet, das flach auf dem Boden liegt.
Es gibt keine Abhängigkeiten und keinen Build-Schritt. Über GitHub Pages lässt sich die Datei direkt veröffentlichen.

## Was drin ist

- **Vier Beutearten** mit eigenem Verhalten und Hintergrund
  - **Maus**: flitzt bevorzugt an den Rändern entlang, bleibt stehen, schaut sich um, verschwindet und taucht woanders wieder auf
  - **Fisch**: gleitet weich durch einen Teich mit Lichtspiel
  - **Laserpunkt**: zappelig, schnell, mit abrupten Stopps
  - **Käfer**: krabbelt langsam mit wuselnden Beinen über Gras
- **Natürliches Beuteverhalten**: Pausen, Sprints, Schlendern, Verstecken außerhalb des Bildschirms und Flucht, wenn die Pfote knapp danebenhaut
- **Großzügige Trefferzone**, Multitouch für mehrere Pfoten, Pfotenabdrücke bei jedem Tipper
- **Synthetische Geräusche** (Web Audio, keine Dateien): Quieken, Plätschern, Zirpen. Optionale **Lockrufe** kommen per Stereo aus der Richtung der Beute
- **Einstellungen**: Tempo, 1–3 Beutetiere gleichzeitig, Spielzeit (5/10/15 Minuten oder unbegrenzt), Ton
- **Katzensicheres Beenden**: Pfote oben rechts 2 Sekunden gedrückt halten (oder `Esc`)
- Vollbild und Wake Lock, damit der Bildschirm während der Runde nicht ausgeht
- Statistik der letzten Runde: Fänge, Pfotentipper, Trefferquote, Dauer

## Tipps

- Auf dem iPad „Geführter Zugriff“ (Bedienungshilfen), auf Android „App anheften“ aktivieren, damit die Katze in der App bleibt.
- Eine Displayschutzfolie schützt vor Krallen.
- Kurze Runden spielen und danach ein echtes Spielzeug oder Leckerli geben, damit die Jagd mit einem echten Fang endet.
