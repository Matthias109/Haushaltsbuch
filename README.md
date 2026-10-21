# Haushaltsbuch – Einrichtung

Die App besteht aus **einer Datei** (`index.html`). Die Daten liegen getrennt davon in einem **privaten** Repository, damit niemand eure Finanzen sieht. Ihr beide arbeitet mit denselben Daten, Änderungen erscheinen beim anderen nach spätestens 30 Sekunden.

## 1. App veröffentlichen (öffentliches Repository)

1. Auf github.com anmelden → oben rechts **+** → **New repository**.
2. Name: `haushaltsbuch`, **Public**, Häkchen bei **Add a README file** → **Create repository**.
3. **Add file → Upload files** → `index.html` hineinziehen → **Commit changes**.
4. **Settings → Pages** → bei *Branch* `main` und `/ (root)` wählen → **Save**.
5. Nach 1–2 Minuten ist die App erreichbar unter
   `https://DEIN-BENUTZERNAME.github.io/haushaltsbuch/`

> In diesem Repository liegt nur die App, keine Zahlen.

## 2. Daten-Repository anlegen (privat)

1. Wieder **+ → New repository**.
2. Name: `haushaltsbuch-daten`, **Private**, Häkchen bei **Add a README file** → **Create repository**.

## 3. Zugriffs-Token erstellen

1. Oben rechts auf dein Profilbild → **Settings** → ganz unten **Developer settings**.
2. **Personal access tokens → Fine-grained tokens → Generate new token**.
3. Name: `Haushaltsbuch`, Ablauf: z.B. 1 Jahr.
4. **Repository access → Only select repositories** → `haushaltsbuch-daten`.
5. **Permissions → Repository permissions → Contents → Read and write**.
6. **Generate token** und den Code (`github_pat_…`) kopieren. Er wird nur einmal angezeigt.

> Der Token gibt nur Zugriff auf das Daten-Repository. Behandle ihn trotzdem wie ein Passwort.

## 4. App verbinden – auf beiden Handys

1. App-Adresse öffnen → **⚙️ Einstellungen → Gemeinsamer Zugriff**.
2. Eintragen: dein Name, GitHub-Benutzername, `haushaltsbuch-daten`, Branch `main`, Datei `daten.json`, Token.
3. **Speichern & verbinden**. Oben rechts erscheint ✓ mit der Uhrzeit.
4. Deine Frau macht dasselbe auf ihrem Handy mit **demselben Token** (sie braucht kein eigenes GitHub-Konto).
5. Tipp: Im Browser **Teilen → Zum Home-Bildschirm** – dann öffnet sich die App wie eine normale App.

## Bedienung kurz erklärt

- **Konto:** Unter Einstellungen den Titel und den Kontostand per Stichtag eintragen.
- **Gruppen:** z.B. Wohnen, Versicherungen, Einnahmen. Darunter erscheinen die Daueraufträge.
- **Daueraufträge:** Rhythmus wählbar: einmalig, monatlich, alle 2 Monate, quartalsweise, alle 4 Monate, halbjährlich, jährlich. Fällige Ausführungen werden automatisch als Buchung festgeschrieben.
- **Dauerauftrag ändern:** Mit „Änderung gilt ab“ wählst du den Stichtag. Vergangene Buchungen bleiben unverändert, nur die Zukunft wird angepasst.
- **Überträge (Sparen):** Unter Einstellungen weitere Konten anlegen, z.B. «Sparkonto Ferien» oder «Sparkonto Steuern». Bei einer Buchung oder einem Dauerauftrag «Übertrag» wählen und «Von Konto» / «Auf Konto» festlegen. Das Geld wird beim einen Konto abgezogen und beim anderen gutgeschrieben, es zählt aber nicht als Ausgabe.
- **Buchungen:** Alle vergangenen (und geplanten) Buchungen ansehen und einzeln ändern oder löschen. Eine Buchung mit Datum in der Zukunft zählt in der Prognose.
- **Prognose:** Kontostand für 6–36 Monate, mit Warnung, falls das Konto ins Minus fällt. Auf einen Monat tippen zeigt die einzelnen Zahlungen.
- **Sicherung:** Unter Einstellungen jederzeit exportieren. Zusätzlich speichert GitHub jede Änderung als Version im Daten-Repository.
