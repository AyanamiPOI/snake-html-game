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

Öffne `index.html` direkt im Browser.

## Android APK für Anfänger bauen

Mit diesen Schritten kannst du aus dem Projekt eine installierbare Android-Datei (`.apk`) erstellen.

### Was du brauchst
- Einen Computer mit **Android Studio**
- Dieses Projekt auf deinem Computer
- Optional: ein Android-Handy oder Tablet zum Testen

### 1. Android Studio installieren
1. Lade Android Studio von der offiziellen Android-Developer-Webseite herunter.
2. Installiere Android Studio mit den Standard-Einstellungen.
3. Starte Android Studio einmal vollständig.
4. Wenn Android Studio zusätzliche Komponenten wie Android SDK, Gradle oder Build Tools installieren möchte, bestätige die Installation.

### 2. Projekt richtig öffnen
1. Öffne Android Studio.
2. Klicke auf **Open** oder **Open an existing project**.
3. Wähle **nicht** den Hauptordner des ganzen Repositories aus, sondern den Ordner:
   - `android-app`
4. Klicke auf **OK** oder **Open**.

Wichtig: In Android Studio muss also der Ordner `android-app` geöffnet sein. Dort liegen die Android-Dateien wie `build.gradle.kts`, `settings.gradle.kts` und der App-Ordner.

### 3. Gradle Sync abwarten
Nach dem Öffnen startet Android Studio normalerweise automatisch den **Gradle Sync**.

1. Warte, bis unten oder oben keine Ladeanzeige mehr läuft.
2. Wenn Android Studio fragt, ob fehlende SDKs oder Tools installiert werden sollen, klicke auf **Install** oder **Accept**.
3. Wenn der Sync erfolgreich ist, sollte keine rote Fehlermeldung mehr angezeigt werden.

Falls ein Fehler erscheint, prüfe zuerst:
- Ist wirklich der Ordner `android-app` geöffnet?
- Ist deine Internetverbindung aktiv?
- Hat Android Studio alle vorgeschlagenen SDK-Komponenten installiert?

### 4. APK bauen
1. Klicke oben in der Menüleiste auf **Build**.
2. Wähle **Build Bundle(s) / APK(s)**.
3. Klicke auf **Build APK(s)**.
4. Warte, bis Android Studio fertig ist.

Wenn alles funktioniert hat, zeigt Android Studio unten rechts oder unten im Fenster eine Meldung wie **APK(s) generated successfully** an.

### 5. APK-Datei finden
Die fertige APK liegt normalerweise hier:

```text
android-app/app/build/outputs/apk/debug/app-debug.apk
```

In Android Studio kannst du nach dem Build oft direkt auf **locate** klicken. Dann öffnet sich der Ordner mit der APK-Datei.

### 6. APK auf Handy oder Tablet installieren
Es gibt zwei einfache Möglichkeiten.

#### Möglichkeit A: APK-Datei übertragen
1. Kopiere `app-debug.apk` auf dein Android-Gerät, zum Beispiel per USB-Kabel, Cloud oder Messenger.
2. Öffne die APK-Datei auf dem Gerät.
3. Android fragt eventuell, ob Apps aus dieser Quelle erlaubt sind.
4. Erlaube die Installation für diese Quelle.
5. Tippe auf **Installieren**.

#### Möglichkeit B: Direkt aus Android Studio installieren
1. Aktiviere auf deinem Android-Gerät die Entwickleroptionen und USB-Debugging.
2. Verbinde das Gerät per USB mit dem Computer.
3. Wähle das Gerät oben in Android Studio aus.
4. Klicke auf den grünen **Run**-Button ▶.
5. Android Studio installiert und startet die App automatisch.

### 7. App testen
Nach der Installation heißt die App aktuell **Snake**. Öffne sie auf deinem Android-Gerät und teste:
- Steuerkreuz
- Pause / Weiter
- Neustart
- Autoplay
- Wischen auf dem Spielfeld

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
