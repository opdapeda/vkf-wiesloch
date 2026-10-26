# Übergabe für Claude Code: Relaunch vkf-wiesloch.de

Lies zuerst `docs/VKF-Projektbriefing.md`. Dort stehen die Inhalte, die Anmelde-Regeln und die offenen Punkte.

## Projekt in Kürze

- **VKF = Väter-Kinder-Freizeit Wiesloch.** Ein Zeltlager für Papas mit Kindern von 4 bis 12 Jahren, eine Woche in der 3. Woche der Sommerferien in Baden-Württemberg, Samstag bis Samstag.
- Rund 95 Teilnehmende und rund 30 Ehrenamtliche. Träger ist die KjG Wiesloch (Katholische junge Gemeinde).
- Kontakt: lagerleitung@vkf-wiesloch.de. Förderverein: „Freunde der VKF Wiesloch“, seit 2023.
- Auftraggeber und Designer ist Jan (JPO), Kommunikationsdesigner und Teil des VKF-Teams. Er arbeitet auf Deutsch.

## Stand (Oktober 2026)

- `index.html` ist **Entwurf 2 „Abendrot“** und die aktuelle Richtung.
  - Flache Vektor-Illustration ohne Konturen, mit weichen Verläufen, gestaffelten Bergsilhouetten, vierzackigen Funkelsternen und leuchtendem Lagerfeuer.
  - Infobereiche als bunte Bänder mit Hügelkanten, runde, große Schriften (Baloo 2 und Nunito).
  - Jans Wunsch: spaßig, comicartig, kindgerecht, aber gut lesbar, große Schriften, fröhlich, offen und bunt.
- `entwurf-1/index.html` ist der ältere Entwurf (Flat-Icons mit dicker Kontur). Er dient nur zum Vergleich.

## Aufbau der Seite (`index.html`)

Alles steckt in einer Datei: HTML, CSS und JavaScript. Es gibt keine Abhängigkeiten außer Google Fonts.

1. **Scroll-Story „Ein Tag in der VKF“** (`#story`, 1000vh hoch, sticky SVG `#scene`).
   - `render()` mappt den Scroll-Fortschritt `p` von 0 bis 1 auf Keyframe-Paletten: Himmel (`SKYT/SKYM/SKYB`), Bergketten (`M1*`, `M2*`, `M3*`), Wiese (`GA/GB`) und Bäume (`TREE`).
   - Die Vignetten (`vig(id,a,b,html)`) blenden in ihrem Abschnitt ein: Frühstück, Morgenkreis, Spiele, Mittag, Ausflug, Abendessen.
   - Die Lagerrunde (`#runde`) hat Bänke im Kreis, das Feuer und Gitarristen, die mit `orbit()` um das Feuer laufen.
   - Die Story-Texte liegen in `S[]`. Sie sind zentriert, blenden ein, wandern nach oben und blenden aus. Die Textfarbe folgt dem Himmel.
   - Die Zeitleiste `.clock` enthält Sprungmarken.
   - Zeitgesteuerte Szenen-Animationen stehen in `life(ts)` (läuft im `orbit()`-Loop): Reh und Vögel (Start), Frühstückschaos mit umfallendem Becher, Fußballspiel mit Tor, Schöpfkelle und Kinder mit Tellern (Mittag), Schmetterlinge (Ausflug), Glühwürmchen (Abend), Sternschnuppe und Zzz (Nacht). Bei `prefers-reduced-motion` stehen sie still (feste Zeit `FIX`).
2. **Über die VKF** `#ueber`
3. **Team** `#team`: Die Rollen stehen in `ROLES[]`.
4. **Anmeldung** `#anmeldung`: 4 Schritte, Tipp-Box und ein Button zum Kopieren der E-Mail-Adresse.
5. **Packliste** `#packliste`: Die Icons stehen in `ICON{}` als SVG mit viewBox 64×64, die Liste in `PACK[]`.
6. **Footer** mit Lagerfeuer-Nachtszene.

Farben und Schriften sind als CSS-Tokens in `:root` definiert. Der Dunkelmodus läuft über `prefers-color-scheme` und `[data-theme]`.

## Regeln

- Sprache und Texte auf Deutsch. Der Name lautet „Katholische junge Gemeinde“, nicht „Junge Katholische Gemeinde“.
- Keine Fakten erfinden. Fehlende Infos als Platzhalter markieren und bei Jan nachfragen.
- Die Seite muss ab 360 px Breite ohne horizontales Scrollen funktionieren.
- Fließtext mindestens 18 px, gute Kontraste.
- `prefers-reduced-motion` respektieren.
- Statisch bleiben (kein Build), solange nichts anderes entschieden ist. Deployment über Vercel bei jedem Push auf `main`.
- `noindex` erst entfernen, wenn Jan den Launch freigibt.

## Offene Punkte

- Gründungsjahr klären: 2000 oder 2001.
- Original-Logo ist eingebaut (Header, Intro, Footer, Favicon; Datei `docs/logo-vkf.png`). Als Vektor (SVG) wäre es noch schärfer. Die alten Icons wurden im neuen Stil nachgezeichnet.
- Uhrzeiten und Teamtexte sind Platzhalter.
- Echte Fotos zwischen der Story und den Infobereichen einbauen.
- Die Figuren auf dem Handy größer und besser lesbar machen.
- Seiten für Impressum und Datenschutz anlegen. Die Links zeigen aktuell auf `#`.
- Später auf die Domain vkf-wiesloch.de umziehen. Die alte Seite läuft dort noch mit WordPress.
- Optional: Sound oder Musik für die Lagerrunde. Jan kann sie mit Magnific erstellen, und sie startet nur per Klick.
