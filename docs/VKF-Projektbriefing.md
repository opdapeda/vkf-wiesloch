# Projektbriefing: Relaunch vkf-wiesloch.de

Übergabe aus einem früheren Chat. Bitte lies dieses Briefing und die angehängte Datei `vkf-lagertag-prototyp.html` und arbeite am Prototyp weiter.

## Über die VKF

- **VKF = Väter-Kinder-Freizeit Wiesloch.** Ein Zeltlager für Papas mit ihren Kindern von 4 bis 12 Jahren, eine Woche lang.
- **Termin:** 3. Woche der Sommerferien in Baden-Württemberg, jeweils Samstag bis Samstag.
- **Träger:** Die VKF gehört zur KjG Wiesloch (offizieller Name: Katholische junge Gemeinde. Auf der alten Seite steht fälschlich „Junge Katholische Gemeinde“).
- **Teilnehmende:** rund 95 Personen, Väter und Kinder zusammen.
- **Team:** rund 30 Ehrenamtliche im Betreuerstab, zum Beispiel Lagerleitung, Programmkoordination, Küche, Einkauf und Technik. Ich (JPO) gehöre zum Team.
- **Kontakt:** lagerleitung@vkf-wiesloch.de
- **Förderverein:** „Freunde der VKF Wiesloch“, gegründet 2023.
- **Gründungsjahr:** offen. Auf der alten Seite steht 2000, ich hatte 2001 im Kopf. Das muss noch geklärt werden.

## Die alte Website

- Ich habe sie vor über zehn Jahren gebaut, mit WordPress. Es ist ein One-Pager mit den Menüpunkten „VKF“ und „Förderverein“.
- **Was bleiben soll:**
  - das Logo, ein Emblem im Abzeichen-Stil mit Zelt, Mond und Sonnenstrahlen
  - die flachen, bunten Icons wie Zelt, Rucksack, Wanderschuh und Laterne
  - die Farben Rot, Nachtblau und Olivgrün, dazu Creme mit Höhenlinien wie auf einer Wanderkarte
  - die echten Fotos
- **Was schwach ist:**
  - Die Textspalte ist schmal und die Schrift klein.
  - Die drei Schwerpunkte haben denselben Platzhaltertext.
  - Die Anmeldung ist eine lange Textwand.
  - Die Packliste ist ein Fließtext.
  - Die Neuigkeiten sind veraltet, der neueste Beitrag ist von 2023.
  - Der Kontakt geht im Footer unter.
  - Das Team kommt nicht vor.

## Anmeldung und Platzvergabe (Inhalt der alten Seite)

1. Die Interessenten-Phase läuft jedes Jahr von Januar bis Ende März. Das Interesse muss jedes Jahr neu bekundet werden, es gibt keine Warteliste.
2. Familien, die schon dabei waren, haben ein Vorbuchungsrecht.
3. Die freien Plätze vergibt die Teamleitung, und zwar nicht nach dem Windhund-Prinzip, sondern so, dass die Gruppe gut zusammenpasst.
4. Die Zu- oder Absage kommt von Ende März bis Ende April. Eine Interessensbekundung ist keine Platzgarantie.

Was die Chancen erhöht: ein kurzer Einblick, wer man ist, die Motivation und gegebenenfalls eine Empfehlung durch eine teilnehmende Familie oder jemanden aus dem Team.

## Konzept des Prototyps

Ein One-Pager mit einer scrollgesteuerten Animation „Ein Tag im Lager“, vom Sonnenaufgang bis zur Nacht. Darunter folgen ruhige Infobereiche.

**Ablauf der Scroll-Story (von mir vorgegeben):**

1. Die Sonne geht auf.
2. Frühstück: Kinder und Papas essen gemeinsam an Bierbänken.
3. Morgenkreis: Die Lagerleitung erzählt etwas.
4. Fußball, Versteckspiel oder Verkleiden
5. Mittagessen
6. Gemeinsam ins Schwimmbad oder zum Wandern
7. Abendessen
8. **Lagerrunde:** Bierbänke stehen im Kreis, in der Mitte ein großes Lagerfeuer, und es wird gemeinsam gesungen. Kinder und Papas sitzen auf den Bänken, während zwei oder drei Gitarrenspieler in der Mitte um das Feuer laufen.
9. Die Sonne geht unter, Sterne und Mond kommen hoch, und es wird dunkel. Man sieht das Lager, und nur das Küchenzelt ist noch hell, mit flackerndem Licht.

**Infobereiche unter der Story:**

- Über die VKF
- Team mit den Rollen
- Anmeldung in vier Schritten mit Tipps
- Packliste zum Abhaken, die sich im Browser merkt, was schon abgehakt ist
- Footer mit Förderverein, Kontakt, Impressum und Datenschutz

**Technik:**

- Eine einzige HTML-Datei ohne Abhängigkeiten.
- Die Szene ist ein SVG, das per JavaScript an den Scroll-Fortschritt gekoppelt ist. Himmelsfarben, Sonne und Mond laufen über Keyframes, und jede Station blendet sich in ihrem Scroll-Abschnitt ein.
- Dazu gibt es eine Tageszeitleiste mit Sprungmarken.
- Die Bewegungen berücksichtigen die Systemeinstellung für reduzierte Bewegung.

## Feedback, das schon umgesetzt ist

- **Zelte:** beige Hauszelte mit Firstdach, grauem Bodenstreifen, offener Tür an der Giebelseite und Sprossenfenster an der Längsseite. Siehe `referenz-zelt.png`.
- Die **Teilnehmerzelte** sind alle gleich groß.
- Das **Küchenzelt und das Aufenthaltszelt** sind doppelt so lang und etwas höher.

## Offene Punkte und nächste Schritte

- Das Gründungsjahr klären: 2000 oder 2001.
- Das Original-Logo und die Icons von der alten Seite als SVG oder PNG einbauen.
- Weiteres Feedback zu den Figuren und zur Lagerrunde einholen.
- Die Figuren auf dem Handy größer und besser lesbar machen.
- Uhrzeiten und Teamtexte sind Platzhalter und müssen echt werden.
- Echte Fotos zwischen die Szene und die Infobereiche einbauen.
- Später die Umsetzung als echte Website planen, zum Beispiel weiter mit WordPress oder als statische Seite.
- Eventuell Sound oder Musik für die Lagerrunde. Das kann ich auch mit Magnific erstellen, falls ich es im privaten Account verbinde.
