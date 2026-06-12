# `fable-teach-skills` — a `/teach` stress-test collection

### ▶️ [**Open the landing page →**](https://az9713.github.io/fable-teach-skills/)

A growing collection of teaching workspaces produced by running Matt Pocock's
[`/teach`](https://github.com/mattpocock/skills) skill inside Claude Code (model: **Claude Fable 5**).
Each subfolder is one **independent, self-contained `/teach` run** in a different domain — a
stress test of how well a single slash command turns into a structured, mission-grounded
curriculum across very different subjects.

---

## Domains

| Domain | Request | Mission | Live lesson |
|--------|---------|---------|-------------|
| 🤹 [**Juggling**](./juggling/) | `/teach how to juggle 3 balls` | Land a 3-ball cascade as a party trick | [Lesson 1 →](https://az9713.github.io/fable-teach-skills/juggling/) |
| 🎵 [**Singing**](./singing/) | `/teach how to sing like Luciano Pavarotti` | Sing one iconic tenor aria, proudly | [Lesson 1 →](https://az9713.github.io/fable-teach-skills/singing/) |
| 📜 [**Tang poetry**](./tang-shi/) | `/teach me to write a "tang shi" like 唐詩三百首` | Compose a 律詩 worthy of the anthology | [Lesson 1 →](https://az9713.github.io/fable-teach-skills/tang-shi/) |

> More domains will be added as further stress tests are run.

---

## What `/teach` is

`/teach` treats the **current directory as a stateful learning workspace** that persists across
sessions, rather than answering a one-shot "explain X" prompt. Its philosophy: deep learning needs
three things —

- **Knowledge** — captured from high-trust sources, never the model's memory (`RESOURCES.md`)
- **Skills** — acquired through tight interactive feedback loops (`lessons/`)
- **Wisdom** — tested against real practitioners (communities in `RESOURCES.md`)

Everything is anchored to a single **mission** — the real reason the learner cares.

---

## Repository layout

```
.
├── index.html            # Landing page (links into every domain)
├── README.md             # You are here
├── <domain>/             # One self-contained /teach workspace per domain
│   ├── MISSION.md         # The "why" — the compass for every teaching decision
│   ├── RESOURCES.md       # Trusted knowledge sources + practitioner communities
│   ├── NOTES.md           # Learner preferences + working notes
│   ├── index.html         # Redirect to that domain's current lesson
│   ├── lessons/           # Self-contained, beautiful HTML lessons
│   ├── reference/         # Compressed cheat sheets & glossaries (revisited often)
│   └── learning-records/  # Evidence-based records of what was actually learned
```

### Adding a new domain

1. Create a new folder (e.g. `pottery/`) and run `/teach …` with that folder as the working directory.
2. Add a `<domain>/index.html` redirect to its first lesson.
3. Add one row to the **Domains** table above and one card to `index.html`.

---

## Credits

- Teaching method: [`/teach`](https://github.com/mattpocock/skills/tree/main/skills/productivity/teach)
  from **[mattpocock/skills](https://github.com/mattpocock/skills)** by Matt Pocock.
- Workspaces generated in [Claude Code](https://claude.com/claude-code) with **Claude Fable 5**.
