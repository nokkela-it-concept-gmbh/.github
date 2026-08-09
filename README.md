# `.github` — Organisationsprofil der Nokkela-IT-Concept GmbH (deutsch)

Dieses Repository ist das besondere `.github`-Repository der GitHub-Organisation
[`nokkela-it-concept-gmbh`](https://github.com/nokkela-it-concept-gmbh). GitHub rendert
[`profile/README.md`](profile/README.md) auf der Startseite der Organisation – diese Datei ist
die Unternehmensvorstellung auf Deutsch.

Die englische Fassung liegt in einer eigenen Organisation:
[`nokkela-it-concept-com`](https://github.com/nokkela-it-concept-com). Beide werden gemeinsam
gepflegt: Eine Änderung hier ist auch eine Änderung dort.

## Aufbau

```
.github/
├─ README.md                     # diese Datei – nur im Repository sichtbar
├─ SECURITY.md                   # organisationsweiter Standard: Sicherheitskontakt
└─ profile/
   ├─ README.md                  # ← wird auf github.com/nokkela-it-concept-gmbh gerendert
   └─ assets/
      ├─ banner.png              # Kopfbild: das Open-Graph-Bild der Hub-Website
      ├─ logo-mark.svg           # die „N"-Bildmarke
      └─ services/               # je Leistungsdomain ein Anzeigenbild (deutscher Satz)
         ├─ nokkela-systems.png  ├─ nokkela-cloud.png   ├─ nokkela-app.png
         ├─ nokkela-host.png     ├─ nokkela-ai.png
         └─ nokkela-network.png  └─ nokkela-io.png
```

Dateien hier wirken zugleich als organisationsweite Voreinstellung: Jedes Repository der
Organisation ohne eigene `SECURITY.md` fällt auf die Datei aus diesem Repository zurück.

## Woher die Bilder stammen

- `assets/banner.png` ist das Open-Graph-Bild von `nokkela-it-concept.gmbh`. Das GitHub-Profil
  zeigt damit dieselbe Karte wie eine Linkvorschau der Website.
- `assets/services/*.png` sind die **deutschen** 1200×628-Assets aus dem Nokkela-Anzeigensatz
  (7 Services × 2 Sprachen × 2 Formate). Die Motive sind kein Nachbau: Jedes bettet die echte
  Hero-Grafik der zugehörigen Landingpage ein, gerendert gegen das Stylesheet der jeweiligen
  Domain. Überschriften und Sublines stammen aus genau der Seite, auf die das Bild verlinkt –
  Absicht: Ein Versprechen im Bild, das die Zielseite nicht einlöst, kostet in der Werbung
  Qualitätsfaktor und hier Glaubwürdigkeit.
- Die englische Organisation nutzt denselben Satz in den englischen Varianten.

Zum Aktualisieren den Anzeigensatz neu bauen und die Dateien `*-de-quer-1200x628.png` unter
Beibehaltung der Dateinamen nach `profile/assets/services/` kopieren.

## Bild-URLs sind absolut – und festgenagelt

Die Bilder in `profile/README.md` sind als absolute
`https://raw.githubusercontent.com/nokkela-it-concept-gmbh/.github/main/profile/assets/…`-URLs
eingebunden, nicht als relative Pfade. Relative Pfade werden gegen das Repository aufgelöst,
nicht gegen die Organisationsseite, die die Datei anzeigt; absolut ist hier der verlässliche Weg.

Der Preis dafür: Organisationsname und Branch `main` stecken in jeder Bild-URL. **Wird die
Organisation umbenannt oder der Standard-Branch geändert, brechen sämtliche Bilder in
`profile/README.md`** und müssen in einem Durchgang neu geschrieben werden.

## Bearbeiten

Schlichtes Markdown mit etwas HTML – GitHub erlaubt `<table>`, `<img>`, `<a>`, `<sub>` und
Ausrichtungs-Attribute, entfernt aber `<style>`; CSS steht also nicht zur Verfügung. Das
Leistungsraster ist eine zweispaltige Tabelle, jede Zelle enthält ein verlinktes Bild, die
verlinkte Domain und eine Zeile Beschreibung.

Zwei Dinge müssen beim Bearbeiten stimmen:

- **Beide Sprachen, eine Änderung.** Was hier geändert wird, wird auch in der englischen
  Organisation geändert. Ein Profil, das je Sprache etwas anderes behauptet, ist schlechter als
  eines in nur einer Sprache.
- **Keine Aussage über die Website hinaus.** Das Unternehmen ist NIS2- und
  ISO-27001-**orientiert**, nicht zertifiziert; es veröffentlicht keine Kundenzahlen, Umsätze,
  Referenzen, Auszeichnungen oder Bewertungen. Die Rechtsangaben (HRB 7780, EUID, D-U-N-S,
  USt-IdNr.) müssen exakt dem Impressum entsprechen.

## Lizenz und Marken

Texte, Marken und Bilder in diesem Repository gehören der Nokkela-IT-Concept GmbH und sind hier
zur Darstellung des Unternehmens veröffentlicht. Sie stehen unter keiner Open-Source-Lizenz und
sind nicht zur freien Weiterverwendung freigegeben. Davon unberührt bleibt Individualsoftware
für Kunden, die das Unternehmen auf MIT-Lizenzbasis übergibt.
