# Cowork Remote — sicher bereitstellen (nur du)

Anforderung: erreichbar **nur von dir und von dir eingeladenen, ausgewählten Personen** — identitätsgebunden, rollenfähig, jederzeit entziehbar, kostenlos. Datei: `index.html`.

---

## Entscheid (Council)
Öffentliches Gratis-Hosting (GitHub Pages, Netlify Drop) hat **keine** Zugriffskontrolle → ungeeignet.
Geheime URL = kein Schutz. Client-Passwort in statischer Datei = steht im Quelltext = kein Schutz.
**Korrekt:** Identitäts-Gate per **Cloudflare Access (Zero Trust)** — frei bis 50 Nutzer.

## Weg A — Maximal sicher (Empfehlung, wenn nur du / wenige Geräte)
**Nicht veröffentlichen.** App nur lokal:
1. `index.html` aufs Gerät sichern (Dateien).
2. In Safari öffnen → Teilen → **Zum Home-Bildschirm**.
Ergebnis: läuft offline, nur auf deinem Gerät, **niemand sonst** kann zugreifen. Null Angriffsfläche.

## Weg B — Privater Zugang von überall (Cloudflare Access)
Du führst aus (nur dein Account kann das):
1. **Cloudflare-Account** anlegen (kostenlos).
2. **Workers & Pages → Pages → Upload assets** → `index.html` hochladen → Deploy → du erhältst eine `*.pages.dev`-URL.
3. **Zero Trust** öffnen (linkes Menü) → ggf. kostenloses Team-Setup abschließen.
4. **Access → Applications → Add an application → Self-hosted.**
   - Application domain = deine `*.pages.dev`-Adresse.
5. **Policy** anlegen: Action **Allow**, Include → **Emails** → *deine* E-Mail. Für weitere Personen: weitere Adressen ergänzen, **oder** eine **Access Group** „Cowork-Team" anlegen (Zero Trust → Access → Groups), dort alle eingeladenen Adressen pflegen und die Policy auf die Gruppe zeigen lassen → Einladen/Entziehen = eine Liste pflegen (Single Source of Truth).
6. Speichern. Fertig.

Ab jetzt: jeder Aufruf verlangt Login. Cloudflare schickt einen **Einmalcode** an die hinterlegte Mail (oder Google/GitHub-Login). Nur Adressen aus deiner Liste/Gruppe kommen rein. Zugang jederzeit entziehbar (Adresse aus der Gruppe entfernen → sofort gesperrt). Free-Tier deckt bis 50 Personen.

### Rollen (Betrachter / Operator / Admin)
Die In-App-Rollenverwaltung (Tab **Zugang**) bildet das Modell ab. Cloudflare Access selbst kennt nur „rein/raus" — die eigentliche **Rollendurchsetzung** gehört an die spätere **Bridge**: sie stellt pro Person/Rolle ein Token mit passenden Scopes aus (Betrachter = nur lesen, Operator = steuern, Admin = + Zugang/Not-Aus). Bis dahin ist die Rollenwahl in der App ein dokumentiertes Mock-Modell.

## Echte Sicherheit kommt später vom Bridge-Dienst
Die Web-App ist nur die Oberfläche. Sobald sie wirklich deinen Rechner steuert, ist die kritische Grenze der **Bridge-Dienst**:
- Pflicht-**Token-Auth** (kein offener Port), nur über TLS.
- Erreichbarkeit von außen ausschließlich über **Cloudflare Tunnel** (kein Port-Forwarding).
- Least-Privilege: die Zugriffs-Scopes (Lesen/Schreiben/Senden/Löschen) gelten serverseitig, nicht nur in der UI.
Ohne authentifizierte Bridge bleibt die App ein Mock — und genau deshalb aktuell kein Risiko.

## Empfehlung
Brauchst du es nur selbst → **Weg A**. Brauchst du eine URL über mehrere Geräte → **Weg B**.
