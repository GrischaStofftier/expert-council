# Weg 1 — Privater Link von überall (Cloudflare, 100 % kostenlos)

**Ergebnis:** Eine eigene Internet-Adresse für deine Cowork-Remote-Seite, auf die **nur du
und Personen, die du einlädst**, zugreifen können. Jeder Aufruf verlangt einen Login per
E-Mail-Code. Alle anderen werden ausgesperrt. Kostenlos bis 50 Personen.

> Du brauchst nur die Datei **`index.html`** (liegt diesem Paket bei) und ~5 Minuten.
> Kein Programmieren, keine Kreditkarte.

---

## Teil A — Seite hochladen (2–3 Min)

1. Gehe auf **dash.cloudflare.com** → **Sign up** → kostenloses Konto mit deiner E-Mail anlegen
   (E-Mail bestätigen, fertig — keine Zahlungsdaten nötig).
2. Links im Menü: **Workers & Pages** → Button **Create** → Reiter **Pages** →
   **Upload assets** (NICHT „Connect to Git" — wir laden direkt hoch).
3. Projektname vergeben, z. B. **`cowork`** → die Datei **`index.html`** ins Upload-Feld ziehen
   (optional `council.html` mit dazu) → **Deploy site**.
4. Cloudflare zeigt dir jetzt deine Adresse, z. B. **`https://cowork.pages.dev`**.
   → Öffne sie einmal zum Test. **Achtung:** Sie ist in diesem Moment noch *öffentlich* —
   das schließen wir gleich in Teil B.

---

## Teil B — Login-Schutz aktivieren (3–4 Min)

> Damit wirklich **nur Eingeladene** reinkommen.

1. Links im Menü: **Zero Trust** öffnen. Beim ersten Mal: Team-Namen wählen (frei erfindbar,
   z. B. `meincowork`) und den **kostenlosen Free-Plan** auswählen (0 €, bis 50 Nutzer).
   Falls nach Zahlungsdaten gefragt wird → es bleibt beim Free-Plan, es wird nichts abgebucht.
2. Im Zero-Trust-Menü: **Access → Applications** → **Add an application** → **Self-hosted**.
3. Felder ausfüllen:
   - **Application name:** `Cowork Remote`
   - **Session duration:** z. B. `24 hours` (wie lange man nach Login eingeloggt bleibt)
   - **Application domain:** deine Adresse von oben eintragen → Subdomain `cowork`,
     Domain `pages.dev` auswählen.
   - Weiter mit **Next**.
4. **Policy anlegen** (= wer darf rein):
   - **Policy name:** `Erlaubte Personen`
   - **Action:** **Allow**
   - **Configure rules → Include →** Selektor **Emails** → deine E-Mail eintragen.
     Weitere Personen = weitere E-Mails ergänzen.
   - **Next → Add application** (speichern).
5. **Login-Methode** (damit ein E-Mail-Code reicht, ohne Google/GitHub):
   **Settings → Authentication → Login methods** → sicherstellen, dass **One-time PIN**
   aktiviert ist (Standard an). Damit bekommt jede eingeladene Person beim Aufruf einen
   **6-stelligen Code per E-Mail**.

**Fertig.** Ab jetzt: Wer `cowork.pages.dev` öffnet, muss seine E-Mail eingeben und den
zugesandten Code bestätigen. Nur Adressen aus deiner Liste kommen rein.

---

## Täglich nutzen

- **Jemanden einladen:** Zero Trust → **Access → Applications → Cowork Remote → Policy
  bearbeiten → E-Mail hinzufügen.** Sofort gültig.
- **Zugang entziehen:** dieselbe Liste → E-Mail entfernen → **sofort gesperrt.**
- **Komfort-Tipp:** Statt einzelner Mails einmal eine **Access-Gruppe** „Cowork-Team" anlegen
  (Zero Trust → **Access → Groups**), dort alle Adressen pflegen und die Policy auf die Gruppe
  zeigen lassen → du pflegst nur **eine** Liste.
- **Aufs iPhone legen:** `cowork.pages.dev` in Safari öffnen → Teilen → **Zum Home-Bildschirm**
  → die Seite startet wie eine App (nach dem einmaligen Login).

---

## Wichtig / ehrlich
- Diesen letzten Schritt (Konto + Liste) **kann nur dein eigener Account** machen — deshalb
  liegt er bei dir, nicht bei mir. Alles andere (die fertige Datei) ist erledigt.
- Solange die Seite ein **Prototyp mit Mock-Daten** ist, steuert sie nichts Echtes. Der
  Login-Schutz ist trotzdem sinnvoll, damit von Anfang an **nur dein Kreis** Zugriff hat.
- Wenn später eine echte Steuerung (Bridge) dahinterkommt, ist genau dieser Access-Gate die
  richtige erste Verteidigungslinie — du baust hier nichts um, sondern darauf auf.
