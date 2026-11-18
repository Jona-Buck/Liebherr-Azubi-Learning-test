# Technische Zielarchitektur

## Aktueller Stand

Die erste Ausbaustufe ist ein statischer Vanilla-JavaScript-Prototyp. Das Frontend kann über GitHub Pages bereitgestellt werden. Lernfortschritt, Merkliste, Einstellungen und Übungsergebnisse liegen lokal im Browser.

Diese Architektur ist bewusst begrenzt: localStorage ist kein Ersatz für eine Datenbank, und eine clientseitige Admin-Oberfläche ist keine Zugriffskontrolle.

## Zielbild für einen Mehrbenutzerbetrieb

### Frontend
- Statische oder gebaute Web-App
- Responsives UI und zugängliche Komponenten
- API-Client als einzige Schnittstelle zu geschützten Daten
- Keine Secrets und keine privilegierten Schlüssel im Browser

### Backend/API
- Authentifizierung und Session-Verwaltung
- Serverseitige Autorisierung für jede geschützte Operation
- Validierung aller Eingaben
- Rate-Limits und nachvollziehbare Fehlerantworten
- Audit-Log für administrative Änderungen
- API-Versionierung

### Datenbank – konzeptionelles Schema

- users: Identität, Anzeigename, Status
- roles: learner, admin, später erweiterbar
- user_roles: Zuordnung von Nutzern zu Rollen
- professions: Ausbildungsberufe
- exam_tracks: Prüfungsarten und Ausbildungsordnungen
- subjects: Fachbereiche
- modules: Lernmodule
- lessons: Kapitel und Lerninhalte
- questions: Aufgabenstamm mit Typ und Metadaten
- question_options: Antwortoptionen
- question_assets: Bilder und Dokumentreferenzen
- question_solutions: Musterlösung und Erklärung
- attempts: gestartete und abgeschlossene Übungsrunden
- attempt_answers: Antworten und Bewertung
- lesson_progress: Kapitelstatus je Nutzer
- favorites: gespeicherte Inhalte je Nutzer
- flashcards: Karteikarten
- flashcard_reviews: Wiederholungsstatus
- uploads: Metadaten und Speicherpfade

### Dateispeicher
PDFs und Bilder gehören in einen privaten oder kontrollierten Objektspeicher. Der Zugriff erfolgt über kurzlebige, serverseitig erzeugte Download-URLs oder geschützte API-Endpunkte. Dateityp, tatsächlicher MIME-Typ, Dateigröße und Berechtigung müssen serverseitig geprüft werden.

### KI-Anbindung
Eine KI-Anbindung darf nur über das Backend laufen. Der API-Schlüssel bleibt serverseitig. Für Antworten mit Lerninhalten sollte Retrieval auf veröffentlichte und freigegebene Inhalte beschränkt werden. Jede Antwort sollte als KI-generiert erkennbar sein.

## Migrationsreihenfolge

1. Datenmodell und API-Verträge definieren.
2. Authentifizierung und Rollen serverseitig implementieren.
3. Inhalte, Fragen und Dateien in Datenbank/Objektspeicher migrieren.
4. Frontend auf API-Daten umstellen.
5. Lernfortschritt und Prüfungsergebnisse nutzerbezogen speichern.
6. Admin-Änderungen protokollieren und Berechtigungen testen.
7. KI-Assistent als separaten, serverseitigen Dienst anbinden.

## Entscheidung

Für die statische Vorschau bleibt die aktuelle Anwendung bewusst lokal und transparent. Ein echter Adminbereich wird erst aktiviert, wenn Backend, Authentifizierung und serverseitige Rechteprüfung vorhanden sind.
