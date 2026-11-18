# Designentscheidungen – Apple Human Interface Guidelines

Dieses Dokument beschreibt, wie ausgewählte Apple-HIG-Prinzipien auf AZUBI.ACADEMY als responsive Webanwendung übertragen wurden. Es behauptet keine offizielle Apple-Zertifizierung.

## Quellen

- Design principles: https://developer.apple.com/design/human-interface-guidelines/design-principles/
- Designing for macOS: https://developer.apple.com/design/human-interface-guidelines/designing-for-macos
- Layout: https://developer.apple.com/design/human-interface-guidelines/layout
- Typography: https://developer.apple.com/design/human-interface-guidelines/typography
- Color: https://developer.apple.com/design/human-interface-guidelines/color
- Accessibility: https://developer.apple.com/design/human-interface-guidelines/accessibility
- Sidebars: https://developer.apple.com/design/human-interface-guidelines/sidebars
- Motion: https://developer.apple.com/design/human-interface-guidelines/motion
- UI Design Dos and Don'ts: https://developer.apple.com/design/tips/

## Umgesetzte Prinzipien

### Purpose
Die Startseite priorisiert den nächsten sinnvollen Lernschritt, den Lernfortschritt und die Fachbereiche. Dekorative Elemente sind bewusst zurückhaltend.

### Agency
Lernende können Fachbereiche frei öffnen, Kapitel selbst auswählen, Antworten prüfen und eine Übungsrunde verlassen. Bei der Prüfungsrunde wird vor dem Verlassen nachgefragt.

### Responsibility
Die Anwendung kennzeichnet Demo-Inhalte, lokale Datenspeicherung, fehlendes Backend und den nicht geschützten Admin-Demobereich ausdrücklich. Es werden keine echten Anmeldedaten oder API-Schlüssel abgefragt.

### Familiarity
Eine dauerhaft erkennbare Sidebar, Breadcrumbs, vertraute Buttons, Suchfunktion, Formularfelder und eindeutige Rückmeldungen sorgen für vorhersehbare Bedienung.

### Flexibility
Die Navigation klappt auf kleinen Displays zu einer mobilen Seitenleiste um. Die Darstellung unterstützt Light, Dark und Systemmodus. Tastaturbedienung und sichtbare Fokuszustände sind vorgesehen.

### Simplicity
Die Oberfläche nutzt eine begrenzte Farbpalette, wenige wiederkehrende Oberflächen, kurze Beschriftungen und eine klare Informationshierarchie.

### Craft
Abstände, Radien, Typografie, Zustände und Komponenten folgen zentralen CSS-Variablen. Animationen sind kurz und werden bei prefers-reduced-motion reduziert.

### Delight
Kleine Interaktionsdetails und dezente Übergänge geben Feedback, ohne den Lerninhalt zu überlagern.

## Visuelle Umsetzung

- Systemfont-Stack statt eingebetteter Apple-Schriftdateien.
- Semantische Farben für Akzent, Erfolg, Hinweis und Fehler.
- Zurückhaltende Oberflächen, Trennlinien und Schatten.
- Responsive Sidebar und Inhaltsraster.
- Lesbare Textbreiten und klare Hierarchie.
- Fokuszustände und Skip-Link.
- Dark Mode mit eigenen Oberflächen- und Textfarben statt bloßer Invertierung.

## Bewusste Abweichungen

Die HIG sind primär für Apple-Plattformen geschrieben. AZUBI.ACADEMY ist eine Webanwendung. Native macOS-Fensterrahmen, Menüleisten, SF Symbols und Liquid Glass werden deshalb nicht künstlich nachgebaut. Stattdessen werden die zugrunde liegenden Prinzipien – Orientierung, Konsistenz, Lesbarkeit, Feedback und Anpassungsfähigkeit – in Webmustern umgesetzt.

## Noch zu prüfen

Vor einem Produktiveinsatz sind Browser- und Gerätetests erforderlich, insbesondere:
- reale Tastaturbedienung aller Flows
- Screenreader-Ausgabe
- Kontrastmessung nach WCAG
- Vergrößerung und Zoom
- mobile Touch-Ziele
- tatsächliche Darstellung auf mehreren Browsern
- fachliche Prüfung aller Lerninhalte
