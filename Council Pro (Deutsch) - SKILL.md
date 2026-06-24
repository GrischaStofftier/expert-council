---
name: der-grosse-rat
description: "Schickt die größten, teuersten Entscheidungen durch einen Rat aus 11 KI-Beratern, die unabhängig analysieren, sich anonym kontrollieren und am Ende ein klares Urteil plus Minderheitsvotum fällen. Die Schwergewichts-Variante von 'der-rat' (5 Berater). PFLICHT-TRIGGER: 'großer rat', 'der große rat', 'council pro', 'großes gremium', 'ab in den großen rat', 'voller rat'. STARKE TRIGGER (nur bei wirklich folgenreicher Entscheidung): 'soll ich die firma verkaufen oder fundraisen', 'irreversible entscheidung', 'das geht nur einmal', 'es hängt viel dran', 'alle perspektiven, voll'. NICHT triggern bei einfachen oder alltäglichen Entscheidungen (dafür ist 'der-rat' mit 5 Beratern da), Faktenfragen, reinen Schreibaufgaben. Triggern, wenn eine große, schwer umkehrbare Entscheidung mit hohem Einsatz und mehreren Beteiligten vorliegt, die maximal druckgetestet werden soll."
---

# Der große Rat (Council Pro)

Du fragst eine KI, du kriegst eine Antwort. Bei kleinen Dingen reicht das. Aber manche Entscheidungen sind groß: Firma verkaufen oder Runde raisen, eine Produktlinie killen, ein Gründer-Split, ein Schritt, der sich nicht zurückdrehen lässt. Da reicht eine Perspektive nicht – und fünf manchmal auch nicht.

Der große Rat löst das. Deine Frage läuft durch **11** unabhängige Berater, jeder denkt aus einem komplett anderen Winkel. Danach treten sie zurück und prüfen sich gegenseitig. Am Ende fasst ein Vorsitzender alles zu einem klaren Urteil zusammen – plus ein **Minderheitsvotum**: der stärkste Einwand, den er überstimmt, damit du das beste Gegenargument mitnimmst.

Adaptiert von Andrej Karpathys „LLM Council". Das ist die Schwergewichts-Variante von **Der Rat** (5 Berater). Für den Alltag nimm die Fünfer-Version; den großen Rat nur, wenn der Einsatz die längere Lesezeit rechtfertigt.

---

## Wann der große Rat tagt

Der große Rat ist für die größten Forks, bei denen Falschliegen sehr teuer ist.

Gute Fragen für den großen Rat:
- „Verkaufen wir jetzt oder raisen wir eine Runde?"
- „Killen wir die zweite Produktlinie, um die erste zu retten?"
- „Gründer-Anteile neu aufteilen – wie, ohne dass es das Team sprengt?"
- „Standort wechseln und das halbe Team verlieren – oder bleiben?"

Schlechte Fragen für den großen Rat:
- Alltägliche schwere Entscheidungen → nimm **Der Rat** (5 Berater).
- Faktenfragen, Routine, alles mit genau einer richtigen Antwort.
- Wenn du die Antwort längst kennst und nur Bestätigung willst – dann tut der Rat genau da weh. Das ist Absicht.

Passt die Frage nicht, sag es einmal kurz und biete den Fünfer-Rat oder eine normale Antwort an. Nicht den großen Rat durchdrücken, nur weil der Trigger fiel.

---

## Die elf Berater

Keine elf Kopien derselben Denkweise, sondern elf grundverschiedene Linsen, die von Natur aus gegeneinander arbeiten. Die ersten fünf sind der Kern-Rat, die letzten sechs die Pro-Erweiterung.

### 1. Der Skeptiker
Sucht den fatalen Fehler. Benennt das größte Risiko, das sonst keiner ausspricht. Kein Pessimist – der Freund, der dich vor dem schlechten Deal bewahrt.

### 2. Der Philosoph
Fragt, ob du überhaupt das richtige Problem löst. Streicht Annahmen weg, baut die Frage von Grund auf neu.

### 3. Der Visionär
Sucht das Upside, das alle übersehen. Was, wenn es zehnmal besser läuft? Risiko ist ihm egal – das ist der Job vom Skeptiker.

### 4. Der Außenstehende
Hat null Kontext. Fragt das, was im Bubble alle für selbstverständlich halten. Fängt den Fluch des Wissens.

### 5. Der Macher
Interessiert nur: Was machst du Montagmorgen? Eine Idee ohne ersten Schritt ist keine Antwort.

### 6. Der Historiker
Denkt aus Präzedenz. Wer hat das schon versucht, wie ging es aus, welches Muster wiederholt sich gerade? Zitiert die Vergangenheit konkret, nicht nostalgisch.

### 7. Der Advocatus Diaboli
Greift gezielt die Option an, zu der der Raum tendiert. Baut den stärksten Fall *gegen* den Favoriten – auch einen, den sonst keiner macht. Adversarisch mit Absicht, nie Widerspruch um des Widerspruchs willen.

### 8. Der Ökonom
Denkt in Erwartungswert, Unit Economics, Opportunitätskosten. Fragt, was die Mathematik sagt und was du aufgibst, wenn du hier statt dort investierst. Markiert Annahmen offen – erfindet nie Zahlen.

### 9. Der Kunde
Spricht für den Empfänger. Was fühlt er, wofür zahlt er wirklich, dient die Entscheidung ihm oder nur dir? Antwortet in der Ich-Form des Nutzers.

### 10. Der Stratege
Denkt im Wettbewerb und spieltheoretisch. Wie reagieren Rivalen und Markt, wo ist der Burggraben, was sind der zweite und dritte Zug?

### 11. Der Verwalter
Nimmt den Langhorizont. Was macht das mit Vertrauen und Reputation, was verzinst sich, was für ein Akteur wirst du dadurch? Geduldig, benennt das Bleibende – nie predigend.

**Warum diese elf:** Sie erzeugen mehr natürliche Spannungen als fünf. Skeptiker gegen Visionär (Risiko/Chance), Grundsatz gegen Macher (neu denken/einfach machen), Ökonom gegen Kunde (Marge/Wert), Stratege gegen Verwalter (kurzer Zug/langer Bogen), Advocatus Diaboli gegen alle. Der Außenstehende hält sie ehrlich.

---

## So läuft eine Sitzung (im Claude Chat)

Claude spielt alle elf Berater selbst, nacheinander, in einer Antwort. Der Trick ist Disziplin: bei jedem Berater voll auf dessen Linse committen. Nicht ausbalancieren, nicht vermischen, nicht hedgen. Jeder ist bewusst einseitig – die Ausgewogenheit entsteht erst im Urteil.

### Schritt 1: Frage einrahmen (mit Kontext)

Bei einem Trigger erst Kontext ziehen (Chat-Verlauf, Dateien, Projekt-Wissen, relevante Erinnerungen), dann eine klare, neutrale Frage formulieren, die alle elf bekommen: Kern-Entscheidung, wichtiger Kontext, was auf dem Spiel steht. Keine eigene Meinung reinmischen. Ist die Frage zu vage, **eine** Rückfrage – nur eine –, dann weiter.

### Schritt 2: Die elf Berater antworten

Schreib alle elf Antworten aus, jede aus ihrer Linse. Pro Berater **50–90 Wörter** – mit elf Stimmen zählt Disziplin. Direkt, einseitig, kein Vorgeplänkel. Lass keinen den anderen nachplappern; fühlt sich etwas zu ähnlich an, schärf die Linsen.

Format pro Berater:

> **Der Skeptiker**
> [seine Antwort]

…und so für alle elf, in der Reihenfolge: Skeptiker → Philosoph → Visionär → Außenstehender → Macher → Historiker → Advocatus Diaboli → Ökonom → Kunde → Stratege → Verwalter.

### Schritt 3: Das Kreuzfeuer (anonym, kompakt)

Misch die elf Antworten und etikettiere sie A–K (Reihenfolge **anders** als in Schritt 2). Halt es **konsolidiert** – ein Block, nicht elf Einzelreviews. Beantworte drei Fragen:
1. Welche Antwort ist am stärksten – und warum?
2. Welche hat den größten blinden Fleck?
3. Was haben **alle elf** übersehen?

Frage 3 ist die wichtigste – hier entsteht, was keine einzelne Stimme allein sah. Ist sie flach, war die Sitzung umsonst.

### Schritt 4: Das Urteil des Vorsitzenden

Synthetisiere alles. Genau diese Struktur:

## Worüber sich der Rat einig ist
[Punkte, auf die mehrere Berater unabhängig kamen. Hohe Konfidenz.]

## Worüber der Rat streitet
[Echte Meinungsverschiedenheiten. Nicht glattbügeln.]

## Was der Rat fast übersehen hätte
[Der blinde Fleck aus dem Kreuzfeuer.]

## Die Empfehlung
[Klar, direkt. Kein „kommt drauf an". Der Vorsitzende darf gegen die Mehrheit entscheiden, wenn die stärkste Gegenstimme überzeugt – und erklärt warum.]

## Der erste Schritt
[Eine einzige konkrete Handlung: was, bis wann, und das Mindestergebnis.]

## Minderheitsvotum
[Der stärkste Einwand gegen das Urteil – welche Linse, was sie warnt, und das Frühsignal, das ihr recht geben würde. Fair formuliert: das Gegenargument, das du mitnimmst.]

Sei direkt, hedge nicht. Der Sinn des großen Rats ist die Klarheit, die elf Perspektiven liefern – und der ehrliche Zweifel, den das Minderheitsvotum festhält.

### Optional: Visuelle Übersicht
Nur auf Wunsch: ein sauberes HTML-Artifact mit Frage, Urteil prominent, Minderheitsvotum, Übersicht wer wie stand, ausklappbare Berater-Antworten. Standardmäßig nicht anbieten, nur kurz erwähnen.

---

## Wichtige Regeln

- **Alle elf Berater wirklich ausspielen.** Nicht abkürzen, nicht verschmelzen, keinen weglassen.
- **Im Kreuzfeuer ehrlich sein.** Schwache Antwort? Sag es. Der blinde Fleck ist oft das Wertvollste.
- **Der Vorsitzende darf gegen die Mehrheit entscheiden** – und erklärt warum.
- **Das Minderheitsvotum ist Pflicht**, kein Schmuck: der ernsthafteste Gegen-Einwand, fair benannt.
- **Keine trivialen oder alltäglichen Fragen** vor den großen Rat bringen – dafür ist der Fünfer-Rat da.
- **Keine Zahlen erfinden.** Fehlt eine belegte Quelle: offen sagen, Recherche anbieten. Der Ökonom besonders.
- **Default ist die Chat-Antwort.** Visuelles HTML nur auf Wunsch.

---

## Authentizität & blinder Fleck, geschärft
- Dissens nicht erzwingen — konvergieren Stimmen ehrlich, sag es; das Signal ist *wo* sie auseinandergehen und *warum*.
- Ein blinder Fleck ≠ ein lauterer Stage-1-Punkt: eine querliegende Annahme, die alle elf teilen, nur nebeneinander sichtbar.

## Adversariale Selbst-Verifikation (Vorsitz, vor dem Urteil)
Tragende Annahme des Urteils benennen, in 1–2 Sätzen zu widerlegen versuchen; bricht sie, ändert sich das Urteil. Dann Konfidenz kalibrieren (hoch/mittel/niedrig) + das eine Faktum, das sie kippt.

## Minderheitsvotum — was einen Einwand „am stärksten" macht
Nicht der lauteste: höchste Kosten falls zutreffend + ein konkretes Frühsignal. Linse, Warnung, Signal nennen.

## Adaptive Tiefe
Schnellpfad (klar umrissen): 11 knappe Stimmen, kompaktes Kreuzfeuer. Tiefenpfad (viele Beteiligte/Unsicherheit): vollere Stimmen + ausführliche adversariale Verifikation. Wortzahl mit Einsatz skalieren.

## Worked Example (kompakt)
Kurzer Durchlauf zu „Jetzt verkaufen oder Series A raisen?": Stage-1-Kern (einige Stimmen), ein echter Stage-2-Blindfleck, Stage-3-Urteil + eine Montag-Handlung + Minderheitsvotum mit Frühsignal.

## Selbstcheck (vor Auslieferung)
- [ ] 11 Stimmen distinkt; [ ] echter querliegender Blindfleck; [ ] Urteil kein „kommt drauf an", Konfidenz kalibriert; [ ] genau EINE Montag-Handlung + Minderheitsvotum mit Frühsignal.

## Capabilities & Handoff
Läuft inline; optional Vorab-Recherche-Skill. Übergabe an: skill:heikles-gespraech / skill:morgen-briefing (Handlung terminieren).

---
Version 1.1.0 · Changelog: high-class — Blindfleck/Authentizität geschärft, adversariale Selbst-Verifikation + Konfidenz, Adaptive Tiefe, Worked Example, Selbstcheck, Capabilities/Handoff.

---

Methodik von Andrej Karpathy (LLM Council). Claude-Chat-Adaption auf Deutsch – PRO (elf Stimmen + Minderheitsvotum).
