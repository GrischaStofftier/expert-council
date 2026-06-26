# Cowork Remote — online stellen (Runbook)

Statische Web-App + Konzept-Doku, bereit für GitHub Pages.

| Datei | Inhalt |
|---|---|
| `index.html` | **Cowork Remote** — mobile Kommandozentrale (PWA-Prototyp, Mock-Daten, 11 Themes, 0 Build-Schritte) |
| `council.html` | **IT-Council** — Konzept der zwei festen Security-Stimmen (Red-Team & Mobile-Security) |
| `404.html` | Freundliche Fehlerseite → zurück zur Kommandozentrale |
| `HOSTINGSICHER.md` | Leitfaden für **privaten** Zugang (Cloudflare Access / nur lokal) |
| `.github/workflows/pages.yml` | Optionaler Auto-Deploy, sobald Pages-Source = „GitHub Actions" |

> **Sicherheit:** `index.html` ist ein **Prototyp mit Mock-Daten ohne echte Verbindung** zum
> Rechner. Ein öffentlicher Link darauf ist daher **risikolos** — es gibt nichts zu steuern.
> Erst wenn eine echte Bridge dahinterhängt, brauchst du Zugangsschutz (siehe `HOSTINGSICHER.md`).

---

## Öffentlicher Link — 2 Klicks, nur von dir machbar

Die Dateien liegen fertig auf dem Branch dieses PRs. Nach dem Merge nach `main`:

1. **Repo öffentlich schalten** (falls noch privat): *Settings → General → Danger Zone →
   Change visibility → Public*. Kostenloses GitHub-Pages-Hosting braucht ein öffentliches Repo.
2. **Pages aktivieren**: *Settings → Pages → Build and deployment → Source*:
   - Einfach: **„Deploy from a branch"** → Branch `main`, Ordner `/ (root)` → *Save*.
   - Oder: **„GitHub Actions"** → der mitgelieferte Workflow `pages.yml` übernimmt das Deploy.

Danach live unter:

```
https://grischastofftier.github.io/expert-council/
```

(Konzept-Doku unter `…/expert-council/council.html`.)

---

## Privater Zugang (nur du + eingeladene Personen)

Soll der Link **nicht** öffentlich sein → nicht über GitHub Pages, sondern via `HOSTINGSICHER.md`:

- **Weg A — nur lokal:** `index.html` aufs iPhone → Safari → Teilen → *Zum Home-Bildschirm*.
  Läuft offline, null Angriffsfläche.
- **Weg B — privat von überall:** Cloudflare Pages + Zero-Trust **Access**-Policy auf deine
  E-Mail / eine Access-Gruppe. Jeder Aufruf verlangt Login; Zugang jederzeit entziehbar.
  Free-Tier bis 50 Personen. (Erfordert deinen Cloudflare-Account.)
