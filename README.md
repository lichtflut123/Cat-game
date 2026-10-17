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

---

# Brummer (Projektor-Spiel)

Ein Projektor wirft eine leuchtende Fliege auf den Boden. Du steuerst sie mit dem Handy, die Katze jagt sie.

- `brummer/index.html` läuft auf dem **Laptop am Projektor** und zeigt die Fliege auf Schwarz (Schwarz = kein Licht)
- `brummer/handy.html` ist die **Fernbedienung** auf dem Handy

## So geht's

1. `brummer/` auf dem Laptop öffnen. Es erscheinen ein QR-Code und ein 6-stelliger Code.
2. QR-Code mit dem Handy scannen (oder `handy.html` öffnen und den Code eintippen).
3. **Ecken anpassen**: die vier gelben Griffe ziehen, bis das Raster auf dem Boden rechtwinklig und der Kreis rund aussieht. Damit wird das Trapez eines schräg stehenden Projektors ausgeglichen. Die Einstellung wird gespeichert.
4. **Start**: Der Laptop geht in den Vollbildmodus.

## Steuerung

| Handy | Laptop | Wirkung |
|---|---|---|
| Wischen auf der Fläche | Maus/Touchpad bewegen | Fliege steuern (relativ, wie ein Touchpad) |
| Gefangen! | Leertaste | Fang zählen, Funkenregen, Fliege kommt woanders wieder. Das Handy vibriert (Android) bzw. die Wischfläche blinkt (iPhone) |
| Landen / Abheben | L | Fliege setzt sich hin oder fliegt los |
| Autopilot | A | Fliegt selbst, sobald 2,5 s niemand steuert |
| Summen | – | Summton an/aus (Laptop-Lautsprecher, Stereo nach Position) |
| Größe − / + | – | S, M, L, XL |
| – | Esc | Zurück ins Menü |

## iPhone

- QR-Code einfach mit der Kamera-App scannen, die Fernbedienung öffnet sich in Safari.
- Safari erlaubt Webseiten kein Vibrieren. Stattdessen blinkt die Wischfläche bei einem Fang kurz gelb.
- Tipp: In Safari „Teilen“ → „Zum Home-Bildschirm“. Dann startet die Fernbedienung ohne Adressleiste wie eine App.
- Das Display bleibt während des Spiels an, solange die Fernbedienung offen ist (ab iOS 16.4). Wird das iPhone gesperrt oder die App gewechselt, bricht die Verbindung ab; dann einfach „Verbinden“ tippen.

## Verbindung und Hosting

Handy und Laptop verbinden sich direkt per WebRTC ([PeerJS](https://peerjs.com/)). Der öffentliche PeerJS-Dienst wird nur fürs Kennenlernen gebraucht, also brauchen beide Geräte Internet.

Das Handy muss `handy.html` über eine echte Adresse laden können. Eine lokal geöffnete Datei (`file://`) reicht dafür nicht:

- **GitHub Pages** (empfohlen): Repo-Einstellungen → Pages → Branch auswählen. Bei privaten Repos braucht das einen kostenpflichtigen GitHub-Plan, sonst muss das Repo öffentlich sein.
- **Lokal im WLAN**: Auf dem Laptop `python3 -m http.server 8000` im Projektordner starten und die Seite über `http://<IP-des-Laptops>:8000/brummer/` öffnen, nicht über `localhost`. Dann zeigt der QR-Code eine Adresse, die das Handy erreicht.
