# vkf-wiesloch.de – Relaunch

Neue Website der **VKF Wiesloch (Väter-Kinder-Freizeit)**, einem einwöchigen Zeltlager der KjG Wiesloch für Papas mit ihren Kindern von 4 bis 12 Jahren.

Statische Seite ohne Build-Schritt. Sie wird über Vercel direkt aus diesem Repo veröffentlicht.

## Struktur

| Pfad | Inhalt |
| --- | --- |
| `index.html` | Entwurf 2 „Abendrot“ (aktuelle Startseite) |
| `entwurf-1/index.html` | Entwurf 1, Flat-Stil mit dicken Konturen (zum Vergleich) |
| `docs/VKF-Projektbriefing.md` | Projektbriefing mit Inhalten und offenen Punkten |
| `docs/referenz-zelt.png` | Referenzbild für die Zelte |
| `docs/logo-vkf.png` | Original-Logo (auch als Favicon) |
| `vercel.json` | Vercel-Konfiguration (saubere URLs) |
| `CLAUDE.md` | Übergabe und Arbeitsregeln für Claude Code |

## Lokal ansehen

```bash
npx serve .
```

## Veröffentlichen

Jeder Push auf `main` löst über die Vercel-Git-Integration automatisch ein neues Deployment aus.

Die Seite hat noch `noindex`, solange sie ein Entwurf ist.
