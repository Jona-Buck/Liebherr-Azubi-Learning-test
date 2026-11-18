# GitHub Pages – Testversion bereitstellen

Für dieses Repository ist ein GitHub-Actions-Workflow unter .github/workflows/deploy-pages.yml angelegt.

## Einmalige Einrichtung

1. Öffne die Repository-Einstellungen von Liebherr-Azubi-Learning-test.
2. Öffne Pages.
3. Wähle bei Build and deployment als Source die Option GitHub Actions.
4. Kontrolliere unter Actions, ob der Workflow Deploy AZUBI.ACADEMY to GitHub Pages erfolgreich durchläuft.

Der Workflow wird bei jedem Push auf main und manuell über workflow_dispatch gestartet.

## Erwartete Projektadresse

GitHub Pages verwendet für dieses Repository voraussichtlich:

https://jona-buck.github.io/Liebherr-Azubi-Learning-test/

Diese Adresse ist erst dann als live zu betrachten, wenn ein erfolgreicher Pages-Deployment-Lauf vorliegt und die Seite im Browser erreichbar ist.

## Sicherheit

Diese Einrichtung betrifft ausschließlich das Test-Repository. Das produktive Repository Liebherr-Azubi-learning und dessen Pages-Konfiguration werden nicht verändert.
