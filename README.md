# buchwerk.dev

Website von Buchwerk Labs, ausgeliefert über GitHub Pages.

| Datei | Zweck |
|---|---|
| `index.html` | Startseite mit allen Apps |
| `impressum.html`, `datenschutz.html` | Rechtstexte |
| `css/style.css` | Gestaltung, Farben für hell und dunkel |
| `css/fonts.css`, `fonts/` | Schriften, lokal eingebunden (SIL OFL 1.1) |
| `buchwerk-icon.svg` | Icon, Quelle für alles andere (eckig, für die Stores) |
| `buchwerk-icon-rund.svg` | Icon mit runden Ecken für Web und Profile |
| `store/` | PNGs für App Store (1024) und Google Play (512), ohne Transparenz |
| `CNAME` | Eigene Domain für GitHub Pages |

## Vor dem Veröffentlichen

Impressum und Datenschutz enthalten Platzhalter. Solange dieser Befehl etwas
findet, ist die Seite nicht fertig:

```bash
grep -rn "PLATZHALTER" --include="*.html" .
```

## Schriften

Absichtlich nicht von Google Fonts geladen: Ein Abruf von Googles Servern
überträgt die IP-Adresse der Besucher, was deutsche Gerichte als DSGVO-Verstoß
gewertet haben (LG München I, 3 O 17493/20). Die Dateien stammen aus Google
Fonts, Teilmengen `latin` und `latin-ext`.

## Subdomains

Jede App kann eine eigene Seite unter `<app>.buchwerk.dev` bekommen: eigenes
Repo mit Pages, darin eine `CNAME`-Datei mit der Subdomain, und beim
Domain-Anbieter ein DNS-Eintrag `CNAME <app>` → `buchwerk-labs.github.io`.
