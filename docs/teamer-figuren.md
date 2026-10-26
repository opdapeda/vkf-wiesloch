# Teamer-Figuren (Stil A)

Echte Teamer als wiedererkennbare Figuren. Gezeichnet mit dem Baukasten aus
`docs/figuren-stil-a-referenz.html` (Funktionen `F()`, `headParts()`, `hatParts()`).
Die Fotos liegen bewusst NICHT im Repo.

## Neue Baukasten-Optionen (in der Referenz bereits umgesetzt)

| Option | Wirkung |
|---|---|
| `hs:'capback'` + `capc` | Kappe verkehrt herum, hellgraues Verschlussband über der Stirn, Haare seitlich sichtbar |
| `glasses:'round'` | runde, dünne Metallbrille (Bügel bis zu den Ohren) |
| `mous:1` | Schnurrbart zusätzlich zu einem anderen Bart (z. B. `beard:'stub'`) |
| `beardc` | eigene Bartfarbe, unabhängig von der Haarfarbe |
| `lanyard:1` | schwarzes Band um den Hals |
| `hat:'straw'` | großer Strohhut mit dunklem Rand und Kinnband |
| `cord:1` | Kinnband läuft über die Brust, mit Stopper |
| `deco:'logo'` | kleines rot-blaues Brustlogo (ohne Schriftzug) |
| `stout:1` | kräftigere Statur (breiterer Rumpf bei Erwachsenen) |

Hinweis: In `index.html` ist `big` schon als Skalierungsfaktor belegt, deshalb heißt die Statur-Option `stout`.

## Kalle (Lagerleiter)

```js
{pose:'stand', arms:'clip', hs:'capback', capc:'#1c1c22', hair:'#8a6a48',
 beard:'stub', mous:1, beardc:'#b8794a', glasses:'round', skin:'#f3c6a6',
 shirt:'#7a1f35', lanyard:1, sleeve:'short', m:'grin'}
```

## HTL (Lagerleiter)

```js
{pose:'stand', arms:'wave', hs:'short', hair:'#6b5a4a', hat:'straw', cord:1,
 beard:'stub', beardc:'#8a8580', skin:'#f0bfa0', shirt:'#f4f3ef', deco:'logo',
 stout:1, pants:'#2e3346', sleeve:'short', m:'grin', eyes:'happy', look:-1}
```
HTL wird gespiegelt platziert (schaut zu Kalle).

## Einsatz

- Morgenkreis: Kalle und HTL stehen nebeneinander in der Mitte, der Kreis ist vorne offen,
  damit beide frei sichtbar sind. Kalle hat die Sprechblase.
