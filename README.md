# Snake im Browser + Android APK

## Browser (Live Server in VS Code)
1. Installiere die VS-Code-Erweiterung **Live Server** (Ritwick Dey).
2. Öffne dieses Projekt in VS Code.
3. Rechtsklick auf `index.html` → **Open with Live Server**.
4. Öffne die lokale URL (z. B. `http://127.0.0.1:5500/index.html`).

## Android APK bauen
1. Öffne den Ordner `android-app` in **Android Studio**.
2. Warte, bis Gradle Sync abgeschlossen ist.
3. Wähle **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
4. Die APK liegt danach typischerweise unter:
   - `android-app/app/build/outputs/apk/debug/app-debug.apk`

## Steuerung
- Tastatur: Pfeiltasten oder WASD
- Neustart: `R`
- Touch:
  - Wischen auf dem Spielfeld für oben/unten/links/rechts
  - Mit 2 Fingern tippen für Neustart
