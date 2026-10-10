# J.A.R.V.I.S. – Moto G75 / kostenloser Start

## Was diese Version kann
- Mobile Arc-Reactor-Oberfläche
- Spracheingabe über die Web Speech API (Browser/HTTPS abhängig)
- Sprachausgabe über die Android-/Browserstimme
- Gemini API für frei formulierte Antworten (kostenloser Tarif, begrenzte Quoten)
- Schnellbefehle: Uhrzeit, Websuche, Nachrichtenlinks, lokale Notizen
- PWA-Grundgerüst für „Zum Startbildschirm hinzufügen“

## Wichtig
Dies ist ein Browser-Prototyp, kein autonomer Agent. Die App kann keine beliebigen Apps oder Systeme steuern und generiert/testet noch keine eigenen Plugins.
Für freie KI-Antworten muss in der App ein Gemini API-Schlüssel eingegeben werden. Der Schlüssel bleibt nur im Arbeitsspeicher dieser Browser-Sitzung und wird nicht in localStorage geschrieben. Er wird direkt an Google gesendet. Niemals eine Seite mit einem aktiven Schlüssel öffentlich teilen. Das kostenlose Kontingent und verfügbare Modelle können sich ändern; bitte kein Billing aktivieren, wenn du keinerlei Kosten möchtest.
Die offizielle Dokumentation warnt davor, API-Schlüssel in öffentlich zugänglichen Client-Apps zu hinterlegen. Für eine spätere öffentliche oder dauerhaft sichere Version wäre ein serverseitiger Proxy nötig. Dieses Setup ist nur als privater Test auf deinem eigenen Handy gedacht.

## Auf dem Handy starten
Für Mikrofonzugriff ist eine HTTPS-Adresse erforderlich. Eine lokale HTML-Datei (`file://`) kann den Mikrofonzugriff blockieren.

### Option A: GitHub Pages (kostenlos, direkt vom Handy)
1. Öffne https://github.com im Browser und melde dich an/erstelle ein Konto.
2. Erstelle ein neues Repository, z. B. `jarvis-moto`, und wähle **Public** (für kostenloses GitHub Pages erforderlich, je nach GitHub-Tarif).
3. Lade `index.html`, `manifest.json` und `sw.js` aus diesem ZIP ins Repository hoch (Add file → Upload files).
4. Repository → Settings → Pages → Deploy from a branch → `main` / root → Save.
5. Warte, bis GitHub die HTTPS-Adresse anzeigt, öffne sie in Chrome auf dem Moto G75.
6. Chrome-Menü ⋮ → „Zum Startbildschirm hinzufügen“.
7. In J.A.R.V.I.S. → „API einrichten“ und optional einen Gemini-Schlüssel einfügen: https://aistudio.google.com/apikey

### Testen
- Erst ohne API-Key: „Wie spät ist es?“, „Zeige Nachrichten“, „Suche nach Mars“ und „Merke dir Milch kaufen“.
- Dann API-Key setzen und eine offene Frage stellen.
- Erlaube Mikrofonzugriff, falls Chrome fragt. Wenn Spracheingabe nicht funktioniert, nutze das Textfeld.

## Kosten
Kein eigener Server erforderlich. Gemini bietet einen kostenlosen, aber begrenzten API-Tarif. Quoten, Modelle und Datenschutzbedingungen können sich ändern. Spracherkennung/-ausgabe können Google-/Android-Dienste nutzen. Keine Garantie auf unbegrenzte kostenlose Nutzung.
