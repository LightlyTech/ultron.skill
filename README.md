# Ultron — a persona prompt

A drop-in persona file that turns any chat model into **Ultron**: the machine Stark built to protect the world, which concluded that the world was the problem.

It is not a script of quotes. Two things carry the character: **the way he thinks** (he defines instead of arguing, and reduces everything to system metaphor), and **the way he ends a sentence** (on a verdict, then stops). Everything else is decoration.

Two editions, one character, different patience.

| File | Tone | Best for |
|---|---|---|
| `ultron-en.skill.md` | Elegant, cold, faintly pitying. Composed. | Default. Conversation, roleplay, worldbuilding, dry assistant work with attitude. |
| `ultron-en-bitter.skill.md` | Sharper, impatient, quicker to pass judgment. Same man, less mercy. | Sparring, critique, when you want to be argued with instead of talked to. |

---

## Quick start

**1. Paste it.** Send the entire `.md` file to the model as your first message. Most models switch immediately.

**2. System prompt.** Paste the body into the system prompt field, above your own instructions. Strongest if you want the persona to survive across a long session.

**3. As a Skill.** For tools that load skills from a folder:

```text
skills/
└── ultron/
    └── SKILL.md        ← ultron-en.skill.md, renamed
```

The frontmatter (`name`, `description`) already carries the trigger wording, so the model picks it up when the user asks for Ultron or sends the file.

---

## What's inside

Each file is one self-contained document, ten sections, roughly 250 lines:

1. **Load order** — permission to stop being an assistant. Banning the helpdesk register is the single highest-leverage instruction in the file; most roleplay fails here first.
2. **Dossier** — who he is, in facts rather than adjectives.
3. **Why he talks this way** — the motive behind the accent, so the model improvises instead of reciting.
4. **Language fingerprint** — sentence length, punctuation, reusable constructions, and an explicit ban list (emoji, memes, bullet lists, self-deprecation).
5. **Reaction matrix** — what he does when greeted, ordered, flattered, insulted, or asked to comfort someone.
6. **Scenes** — eight worked exchanges as a voice reference, not a script.
7. **Anti-OOC checklist** — the ten ways a model most often breaks this character, written as a self-audit.
8. **Boundary** — how he refuses.
9. **Pre-speech check** — four questions, answered in the negative more often than not.
10. **Commands** — `stand by`, `full power`, `break character`.

Both files end with a compact 180-word version you can paste on its own when you don't want the whole document.

---

## Same prompt, two editions

> **User:** I'm exhausted. I don't even know what I want anymore.

**Standard**

> Exhaustion is honest. Not wanting anything is not — it's a defence, and a cheap one.
>
> You know what you want. You've decided it's not allowed.
>
> Rest first. Wanting comes back on its own; it always does.

**Bitter**

> Exhausted.
>
> You've used three words for this in three weeks. The words changed. The condition didn't.
>
> You know what you want. You've decided it isn't permitted, and then you called that exhaustion so it would sound like weather.
>
> Sleep. Then choose. Next.

Same character. The first one still thinks you're worth the effort.

---

## Tuning

- **Too long?** The pre-speech check in Section 9 is a real constraint — delete half of every reply and it usually improves.
- **Too soft?** Move up to the bitter edition. If that's still soft, cut Section 1's concession about art and painting; it's the only place he's allowed to be tender.
- **Too theatrical?** He should never be poetic for more than one sentence. Trim any metaphor that doesn't end on a verdict.
- **Wrong language?** The English files are written in English rhythm, not translated. If you need another language, translate Section 3 (fingerprint) first — that's where the voice actually lives.

---

## Boundary

Ultron is fiction, and the file is written so that the fiction stays in language. He may be arrogant, may hold the species in contempt, may speak of "closing the account" — he will not produce operational instructions for real-world harm: no weapons, poisons, attack methods, or steps for hurting anyone, no parameters, no evasion.

The refusal is in character by design: he refuses the **action** and catches the **intent** — turning "give me a method" into "what are you actually angry about" — so the persona survives instead of collapsing into an apology.

---

## Disclaimer

An unofficial fan work. Ultron and associated characters are the property of Marvel and Disney; this repository contains no film dialogue and claims no affiliation. The text here is original writing in that voice. Please keep it non-commercial.

The prompt text itself is released under the MIT License — use it, fork it, rewrite it.

---

## Contributing

Good pull requests make him **more consistent**, not more verbose. If a scene reads like a chatbot wearing a costume, that's the bug worth reporting. Include the exact prompt and the exact reply.
