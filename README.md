# Snake im Browser + Android APK

Ein kleines Snake-Spiel für den Browser und als Android-WebView-App. Das Spiel unterstützt Tastatur, Wischgesten und große Touch-Buttons für Handy und Tablet.

## Features
- Größeres Spielfeld mit 560 × 560 Pixel Canvas
- Score-Anzeige und gespeicherter Bestwert / Highscore
- Pause / Weiter
- Neustart
- Autoplay-Modus mit Kollisionsprüfung und einfachem Vorausdenken
- Touch-Steuerkreuz für Handy und Tablet
- Wischsteuerung direkt auf dem Spielfeld
- Synchronisierte Web- und Android-Version

## Browser starten

### Variante 1: Direkt öffnen
Öffne `index.html` im Browser.

### Variante 2: Live Server in VS Code
1. Installiere die VS-Code-Erweiterung **Live Server** von Ritwick Dey.
2. Öffne dieses Projekt in VS Code.
3. Rechtsklick auf `index.html` → **Open with Live Server**.
4. Öffne die lokale URL, zum Beispiel `http://127.0.0.1:5500/index.html`.

## Android APK bauen
1. Öffne den Ordner `android-app` in **Android Studio**.
2. Warte, bis der Gradle Sync abgeschlossen ist.
3. Wähle **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
4. Die APK liegt danach typischerweise unter:
   - `android-app/app/build/outputs/apk/debug/app-debug.apk`

## Steuerung

### Tastatur
- Bewegen: Pfeiltasten oder WASD
- Pause / Weiter: `P` oder Leertaste
- Neustart: `R`

### Touch / Handy / Tablet
- Bewegen: großes Steuerkreuz unter dem Spielfeld
- Pause / Weiter: Pause-Button oder mittlerer Button im Steuerkreuz
- Neustart: Neustart-Button
- Autoplay: Autoplay-Button
- Alternativ: auf dem Spielfeld wischen

## Autoplay
Der Autoplay-Modus kann per Button aktiviert oder deaktiviert werden. Der Bot prüft vor jedem Zug:
- ob der nächste Zug innerhalb des Spielfelds bleibt,
- ob er nicht mit dem eigenen Körper kollidiert,
- ob nach dem Zug noch Bewegungsraum vorhanden ist,
- ob ein Weg zum Futter erreichbar ist.

Der Autoplay-Modus ist eine einfache Spielhilfe und nicht garantiert perfekt, vermeidet aber viele direkte Kollisionen und Sackgassen.

## Projektstruktur
```text
.
├── index.html
└── android-app/
    └── app/src/main/assets/index.html
```

Die Datei `index.html` ist die Browser-Version. Die Datei `android-app/app/src/main/assets/index.html` wird von der Android-App im WebView geladen.
