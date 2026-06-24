# CLAUDE.md — Expert Council (Multi-Perspektiven-Entscheidungsrat)

Skill-Quelle für den Council. Ziel: eine schwere Entscheidung bekommt fünf unabhängige
Denk-Linsen, ein anonymes Peer-Review und ein Urteil mit **einer** konkreten Montag-Handlung.

## Was
Fünf Berater antworten unabhängig, reviewen sich anonym, dann fällt der Chair ein Urteil:
- 🔴 **Skeptiker** — sucht den Grund zu scheitern, schonungslos.
- 🤔 **Philosoph** — hinterfragt Annahmen, sokratisch.
- 🚀 **Visionär** — ehrlicher Best-Case, 10×-Denken.
- 👁️ **Außenstehender** — null Kontext, naive Fragen, fängt Groupthink.
- 🔨 **Macher** — „Was am Montagmorgen?", imperativ.
- ⚖️ **Chair** — synthetisiert (eigene Stimme, kein Berater): Konsens, Streitpunkte,
  Peer-Review-Fund, Empfehlung + 1 Montag-Handlung.

## Trigger
`/council`, `/testNr5`, „convene/summon/ask the council", „council this";
DE: „ab in den rat", „soll ich X oder Y", „welche option".

## Wann nutzen
Teure, folgenreiche Forks, um die man seit Tagen kreist: Pricing, Hiring vs. Automatisieren,
Niche vs. Breite, Bootstrapping vs. Raise. Nicht für schnelle Faktenfragen — und kein
Validierungs-Theater: der Rat sagt auch, was man nicht hören will.

## Pro-Variante: Council Pro (11 Räte + Minderheitsvotum)
Schwergewichts-Variante für die größten, schwer umkehrbaren Forks (Verkaufen vs. Raise,
Produktlinie killen, Gründer-Split). Gleicher 3-Stage-Ablauf, aber **11 Berater** (die 5 +
🏺 Historiker, 😈 Advocatus Diaboli, 📊 Ökonom, 🙋 Kunde, ♟️ Stratege, 🌱 Verwalter) und ein
**Minderheitsvotum** im Urteil — der stärkste Einwand, den der Chair überstimmt. Stage 2
bleibt konsolidiert (A–K). Für den Alltag den normalen Council nutzen.
Trigger: `/council-pro`, „großer rat", „der große rat", „council pro".

## Dateien (Quelle der Wahrheit)
| Datei | Inhalt |
|---|---|
| `Expert Council.md` | EN-Skill-Definition: 3 Stages (Stimmen → anonymes Peer-Review → Verdict), Format-Regeln |
| `Expertenrat (Deutsch) - SKILL.md` | DE-Variante (Skeptiker, Grundsatz-Denker, Visionär, Außenstehender, Macher) |
| `Council Pro.md` | EN-Skill-Definition der Pro-Variante: 11 Stimmen, A–K, Minority Report |
| `Council Pro (Deutsch) - SKILL.md` | DE-Variante des großen Rats (11 Berater + Minderheitsvotum) |
| `README.md` | Einordnung & Inspiration (Andrej Karpathys LLM Council) |

## Bezug zum cla-System
Dieses Repo ist die **Skill-Quelle**. Im `cla`-Repo läuft der Council als
`.claude/skills/council/` und ist dort in der Routing-Tabelle (`CLAUDE.md`) sowie in
ODIN (`decision` → Council) verlinkt.

## Arbeitsregeln
- Deutsch antworten, wenn der User Deutsch schreibt.
- Keine erfundenen Zahlen; jede Stimme in ihrem eigenen Register.
- Kein Validierungs-Theater, keine Moralpredigt, keine Pseudo-Mystik.
