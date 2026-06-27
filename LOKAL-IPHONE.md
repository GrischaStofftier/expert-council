# Weg 2 — Nur auf deinem iPhone (kostenlos, kein Konto, kein Link)

**Ergebnis:** Die Cowork-Remote-Seite liegt **nur auf deinem Gerät** und startet wie eine App.
Es gibt **keinen Internet-Link**, also kann **niemand sonst** je darauf zugreifen. Null
Angriffsfläche, kein Account, keine Cloud.

> Du brauchst nur die Datei **`index.html`** (liegt diesem Paket bei).

---

## So geht's (1 Min)

1. **`index.html` aufs iPhone holen** — z. B. die Datei aus diesem Chat speichern, oder dir
   per Mail / AirDrop / in die **Dateien**-App legen.
2. In der **Dateien**-App auf `index.html` tippen → sie öffnet sich in **Safari**.
3. In Safari unten auf **Teilen** (das Quadrat mit Pfeil) → **Zum Home-Bildschirm**.
4. Name bestätigen („Cowork Remote") → **Hinzufügen**.

Jetzt liegt ein App-Symbol auf deinem Home-Bildschirm. Tippen = die Oberfläche startet
**offline**, im Vollbild, ohne Browser-Leiste.

---

## Gut zu wissen
- Läuft **komplett offline** — die Seite lädt nur Schriftarten aus dem Netz nach (kosmetisch);
  ohne Netz nutzt sie System-Schriften, alles funktioniert trotzdem.
- **Nur auf diesem einen Gerät.** Willst du sie auch auf einem zweiten Gerät, dort die Datei
  ebenso ablegen — oder nimm **Weg 1 (Cloudflare)**, dann reicht ein privater Login von überall.
- Es ist ein **Prototyp mit Mock-Daten** — er zeigt die Bedienoberfläche, steuert aber noch
  nichts Echtes an deinem Rechner. Genau deshalb ist die lokale Variante völlig risikolos.
