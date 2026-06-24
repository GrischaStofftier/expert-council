# COUNCIL – Multi-Perspective Decision Skill for Claude

Claude is agreeable. Ask it "should I launch this?" and it'll find five reasons you should. Flip the question, it'll find five reasons you shouldn't. Both answers sound smart. Neither moves you forward.

This skill fixes that. Type `/council` and five advisors with fundamentally different ways of thinking answer your question independently, peer-review each other anonymously, and a Chair delivers a verdict with one concrete first step. All in a single Claude response.

Inspired by [Andrej Karpathy's LLM Council](https://github.com/karpathy/llm-council), adapted for the Claude consumer app — instead of polling five different models, five different thinking lenses argue inside one session.

## What it does

- Runs your decision past five distinct advisors: **the Skeptic, the Philosopher, the Visionary, the Outsider, the Operator**
- Anonymizes their answers and forces a peer review on content, not on role
- Surfaces the thing all five missed individually – that's the most valuable part
- Ends with a real verdict and one action for Monday morning, not "it depends"
- Refuses to play validation service – if you're fishing for a nod, the council will hurt

## How to use

1. Install the skill in Claude (Settings → Capabilities → Skills → Upload)
2. Type `/council` followed by your question
3. Read all three stages – Stage 2 is where the gold is
4. Do the one thing the Chair told you to do Monday morning

## Triggers

`/council` · "convene the council" · "summon the council" · "ask the council" · "council this"

**Council Pro** — for the biggest, hardest-to-reverse forks there's a heavyweight variant: `/council-pro` ("großer rat") runs **eleven** advisors (the five above plus the Historian, Devil's Advocate, Economist, Customer, Strategist, Steward) and adds a **Minority Report** — the strongest dissent the Chair overrules. See `Council Pro.md` / `Council Pro (Deutsch) - SKILL.md`.

## What to council

The council was built for decisions where being wrong is expensive and you've been circling for days. Pricing. Hiring vs automation. Niching down vs broadening. Bootstrapping vs raising. Any fork in the road where you keep going back and forth.

If the answer is obvious and you just want validation – skip it. The council will tell you things you don't want to hear. That's the point.

## Why this exists

A single LLM answer is shaped by how you asked the question. Your framing, your assumptions, your emotional lean – Claude picks up on all of it and tells you a version of what you already believed. That's fine for writing emails. It's dangerous for actual decisions.

Karpathy's original LLM Council polled multiple frontier models and had them peer-review each other. This skill runs the same method inside Claude using distinct thinking lenses instead of distinct models – so you get the disagreement, the blind-spot catching, and the synthesis without leaving your chat.
