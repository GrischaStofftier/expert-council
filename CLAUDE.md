# CLAUDE.md — Expert Council / Der Rat

Dieses Repo ist **kein Code-Projekt**, sondern eine **Claude-Skill-Definition**: ein
Entscheidungs-Rat, der eine harte Frage durch fünf grundverschiedene Denk-Linsen schickt,
sie sich gegenseitig anonym kontrollieren lässt und am Ende ein klares Urteil + eine konkrete
Montag-Handlung liefert. Inspiriert von Andrej Karpathys „LLM Council", aber komplett in
**einer** Claude-Sitzung (verschiedene Denk-Linsen statt mehrerer Modelle).

## Dateien (3, Doku-only)
| Datei | Sprache | Format | Inhalt |
|---|---|---|---|
| `README.md` | EN | Markdown | Überblick: was der Rat ist, wann (nicht) nutzen, warum. |
| `Expert Council.md` | EN | Claude-Skill (YAML-Frontmatter + Markdown) | Skill `the-council`. Primärtrigger `/council`. |
| `Expertenrat (Deutsch) - SKILL.md` | DE | Claude-Skill (YAML-Frontmatter + Markdown) | Skill `der-rat`. Lokalisiertes Äquivalent. |

Beide Skill-Dateien sind **funktional gleichwertige Versionen derselben Sache** — EN und DE
müssen inhaltlich synchron bleiben. Kein `.github/`, kein `.claude/`, keine Konfiguration.

## Konzept — 5 Linsen + Vorsitzender
Linsen, keine Jobtitel. Jede ist bewusst einseitig; die Balance entsteht erst im Urteil.

| Linse (EN / DE) | Job | Gegenpol |
|---|---|---|
| 🔴 Skeptic / Der Skeptiker | größtes ungesagtes Risiko benennen | Visionär |
| 🤔 Philosopher / Der Grundsatz-Denker | eine Ebene tiefer fragen („warum X überhaupt?") | Macher |
| 🚀 Visionary / Der Visionär | ehrlicher Best-Case, 10x statt 1.2x | Skeptiker |
| 👁️ Outsider / Der Außenstehende | naive Frage, die alle übersehen (Fluch des Wissens) | Mitte/Schiedsrichter |
| 🔨 Operator / Der Macher | „Was tust du Montagmorgen?" — konkreter erster Schritt | Philosoph |
| ⚖️ Chair / Der Vorsitzende | **keine** der 5 Stimmen; liest alle + Review, fällt das Urteil — darf gegen die Mehrheit entscheiden | — |

## Ablauf (heilig — Stufen nie überspringen/verschmelzen)
1. **(DE explizit) Frage einrahmen** — Kontext sammeln, bevor die Stimmen sprechen.
2. **Die Stimmen sprechen** — Reihenfolge Skeptiker→Philosoph→Visionär→Außenstehender→Macher,
   je 4–6 Sätze / 60–120 Wörter, unabhängig, kein Quer-Bezug.
3. **Anonymes Kreuzfeuer** — Antworten als A–E **neu gemischt** (Mapping wird sofort offengelegt;
   Anonymität zwingt zur Bewertung nach Inhalt, nicht Rolle). Drei Fragen: stärkste Antwort?
   größter blinder Fleck? **Was haben alle fünf übersehen?** ← wertvollster Output.
4. **Urteil des Vorsitzenden** — wo der Rat übereinstimmt / wo er kollidiert / was das Review fing /
   klare Empfehlung (2–4 Sätze, kein „kommt drauf an") / **eine** Sache für Montagmorgen.

## Trigger
- **EN (`the-council`):** `/council` (immer, egal welcher Text drumherum); „convene/summon/ask the
  council", „council this", oder explizite Bitte um mehrere Perspektiven.
- **DE (`der-rat`):** Pflicht-Trigger „rat", „rat das (durch)", „frag den rat", „ab in den rat",
  „gremium", „frag das gremium" … Starke Trigger nur bei **echter** Entscheidung mit Tradeoff
  („soll ich X oder Y", „welche option", „pressure-test das").
- **Nicht triggern:** Fakten-/Ja-Nein-Fragen, reine Schreibaufgaben, triviales „soll ich" ohne
  echten Tradeoff, schwer emotionale Momente (eine Stimme ist dann richtiger als fünf).

## Bearbeitungs-Konventionen
- **EN und DE synchron halten** — Änderung an einer Linse/Regel in beiden Dateien nachziehen.
- **Drei-/Vier-Stufen-Struktur bewahren**, Anonymisierung in Stufe 3 beibehalten.
- **Stimm-Register sauber:** kein Füllwerk („letztlich kommt es darauf an"), keine erfundenen
  Zahlen, keine Moralpredigt; wenn eine Stimme nichts beizutragen hat, das sagen statt füllen.
- Alle fünf müssen **echt verschieden** klingen — sonst Linsen schärfen.
- DE durchgängig **informell („du")**; Vorsitzender klar und festlegend, nie pseudo-mystisch.
- Skill-Frontmatter-Form beibehalten: `--- name: … / description: … (mit Triggern) --- `.
