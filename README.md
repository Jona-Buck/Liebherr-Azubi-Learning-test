# AZUBI.ACADEMY

Eine lokale Lernplattform-Demo zur Vorbereitung auf die IHK-Prüfung für **Elektroniker:innen für Betriebstechnik**. Das Projekt orientiert sich bei Navigation, visueller Hierarchie, Typografie, Feedback und Barrierefreiheit an Apples Human Interface Guidelines.

## Aktueller Stand

Diese erste Version ist ein **statischer Frontend-Prototyp**, der direkt über GitHub Pages ausgeliefert werden kann.

Enthalten:
- Dashboard mit Lernfortschritt und Fachbereichen
- Lernmodule mit Kapiteln, Erklärungen, Formeln und Beispielen
- Übungsrunden mit Single-Choice, Mehrfachauswahl, Richtig/Falsch, Rechenaufgaben, Zuordnungen und Freitext-Selbstkontrolle
- Sofortfeedback und Auswertung
- Karteikarten
- Merkliste
- lokale Lernanalyse
- lokale Suche (Tastenkürzel Ctrl/⌘ + K)
- Lernassistent mit klar gekennzeichneten Demo-Antworten
- lokale Inhaltsverwaltung mit Frage erstellen, löschen, importieren und exportieren
- Light Mode, Dark Mode und Systemmodus
- responsive Navigation und Layout
- lokale Speicherung von Lernstand, Einstellungen und Ergebnissen im Browser

## Lokal starten

Es ist kein Build-Schritt erforderlich.

1. Repository klonen oder herunterladen.
2. index.html im Browser öffnen oder einen lokalen statischen Webserver verwenden.
3. Die Anwendung läuft vollständig im Browser.

Für die GitHub-Pages-Bereitstellung muss der Pages-Workflow auf den Branch main und den Ordner / (root) zeigen.

## Daten und Datenschutz

Der aktuelle Prototyp speichert Lernfortschritt, Einstellungen, Merkliste und Übungsergebnisse ausschließlich im localStorage des verwendeten Browsers. Die Daten werden nicht zwischen Geräten synchronisiert und sind nicht mit einem Benutzerkonto verknüpft.

Die Beispielinhalte und Fragen sind lokal im Frontend hinterlegt. Eigene Fragen aus dem Admin-Demo-Bereich können als JSON exportiert und wieder importiert werden.

## Wichtige Grenzen – noch kein Produktivbetrieb

GitHub Pages ist ein statischer Hosting-Dienst. Die aktuelle Version besitzt daher **kein Backend**. Folgende Funktionen sind ausdrücklich noch nicht produktionsreif:

- echte Registrierung und Anmeldung
- serverseitige Rollen- und Rechteprüfung
- geschützter Adminbereich
- gemeinsamer Datenbankbestand für mehrere Nutzer
- dauerhafter Datei-Upload und PDF-Verwaltung
- KI-Anbindung
- geräteübergreifende Synchronisierung

Der Verwaltungsbereich ist nur eine lokale Demonstration. Er bietet keinerlei Sicherheitsgrenze. Keine vertraulichen oder personenbezogenen Inhalte dort hinterlegen.

Für einen echten Mehrbenutzerbetrieb wird eine Backend-Architektur benötigt, zum Beispiel eine API mit relationaler Datenbank, Authentifizierung, serverseitiger Autorisierung und Objektspeicher. Zugangsdaten und API-Schlüssel dürfen nicht in Frontend-Dateien abgelegt werden.

## Fachliche Hinweise

Die Inhalte sind selbst erstellte Lernbeispiele und keine offiziellen IHK-Prüfungsfragen. Sie ersetzen weder Ausbildungsunterlagen noch aktuelle Normen, Vorschriften, betriebliche Unterweisungen oder die fachliche Prüfung durch qualifizierte Personen. Insbesondere sicherheitsrelevante Inhalte müssen vor einem produktiven Einsatz fachlich geprüft und aktualisiert werden.

## Designgrundlage

- [Apple Human Interface Guidelines – Design principles](https://developer.apple.com/design/human-interface-guidelines/design-principles/)
- [Designing for macOS](https://developer.apple.com/design/human-interface-guidelines/designing-for-macos)
- [Layout](https://developer.apple.com/design/human-interface-guidelines/layout)
- [Typography](https://developer.apple.com/design/human-interface-guidelines/typography)
- [Color](https://developer.apple.com/design/human-interface-guidelines/color)
- [Accessibility](https://developer.apple.com/design/human-interface-guidelines/accessibility)
- [Sidebars](https://developer.apple.com/design/human-interface-guidelines/sidebars)
- [Motion](https://developer.apple.com/design/human-interface-guidelines/motion)

AZUBI.ACADEMY ist ein eigenständiges Projekt und keine offizielle Apple-Anwendung.
