# Learning to Juggle, taught by `/teach`

### ▶️ [**Open the live lesson →**](https://az9713.github.io/teach-juggling-skill/)

The lesson is published as a live, interactive web page via GitHub Pages:
**https://az9713.github.io/teach-juggling-skill/**
(includes the throw-arc diagram and the tap-to-count "20 clean throws" self-check).

---

This repository is the **teaching workspace** produced by running Matt Pocock's
[`/teach`](https://github.com/mattpocock/skills) skill inside Claude Code, with the request:

> `/teach how to juggle 3 balls`

It documents both the **output** (a juggling lesson) and the **process** the skill follows —
so you can see how a single slash command turns into a structured, mission-grounded curriculum.

---

## What `/teach` is

`/teach` is one of the skills in [mattpocock/skills](https://github.com/mattpocock/skills).
Unlike a one-shot "explain X" prompt, it treats the **current directory as a stateful learning
workspace** that persists across sessions. Its philosophy: deep learning needs three things —

| Pillar | Where it lives in this repo |
|--------|------------------------------|
| **Knowledge** — captured from high-trust sources, never the model's memory | [`RESOURCES.md`](./RESOURCES.md) |
| **Skills** — acquired through tight interactive feedback loops | [`lessons/`](./lessons/) |
| **Wisdom** — tested against real practitioners | Communities section of `RESOURCES.md` |

Everything is anchored to a single **mission** — the real reason the learner cares.

---

## How this lesson was created

The skill ran through a deliberate sequence. Each step maps to a file in this repo.

### 1. Establish the mission (don't teach blind)

The skill refuses to teach abstractly. Before writing anything it interviewed the learner:

- **Why** do you want this? → *"A fun party trick — low-pressure, the satisfaction of 'I can juggle'."*
- **Equipment?** → *"Proper bean bags"* (which don't roll away — ideal for learning).

That became [`MISSION.md`](./MISSION.md): the *why*, what *success looks like* (10+ consecutive
catches on demand), constraints (casual, short sessions), and explicit *out of scope* (4+ balls,
clubs, tricks). Every later decision traces back to this compass.

### 2. Gather trusted knowledge

The skill's rule is *"never trust your parametric knowledge."* So it searched for and read
reputable juggling instruction — primarily [Library of Juggling](https://libraryofjuggling.com/Tricks/3balltricks/Cascade.html),
the most-referenced free guide — and recorded each source with a one-line "use it for…" note in
[`RESOURCES.md`](./RESOURCES.md). The lesson then cites these sources inline, so claims are
backed and the learner has a path to go deeper.

### 3. Find the zone of proximal development

Rather than dumping the full 3-ball cascade, the skill picked the **one rung** a total beginner
can win quickly: the **single-ball throw**. The reasoning (recorded in [`NOTES.md`](./NOTES.md)):
the cascade is *literally* one throw alternated between hands, so drilling that unit makes the
whole pattern inherit its quality. The progress ladder is:

```
1 ball  →  2 balls  →  3-ball flash  →  sustained cascade (mission win)
```

No rung unlocks until the previous self-check passes.

### 4. Build the lesson as a self-contained, beautiful artifact

[`lessons/0001-the-one-ball-throw.html`](./lessons/0001-the-one-ball-throw.html) is one
standalone HTML file (no dependencies) designed to be reopened and reviewed later. It contains:

- **One tightly-scoped skill** — the scoop throw, body setup, and arc.
- An **SVG diagram** of the throw arc peaking above the head.
- The three classic beginner **failure-and-fix** patterns (drifting forward, uneven heights,
  weak hand).
- A built-in **feedback loop**: a tap-to-count "20 clean throws" self-check — the tightest
  loop juggling allows (*did it land in the other hand?*).
- Inline **citations** and a reminder that the agent is the learner's teacher for follow-ups.

### 5. Defer the learning record until there's evidence

The skill distinguishes *coverage* from *learning*. A `learning-records/` entry is only written
once the learner **demonstrates** a skill — so none exists yet. It will be created when the
learner reports completing the self-check.

---

## Repository layout

```
.
├── MISSION.md        # The "why" — the compass for every teaching decision
├── RESOURCES.md      # Trusted knowledge sources + practitioner communities
├── NOTES.md          # Learner preferences + the progress ladder
├── lessons/
│   └── 0001-the-one-ball-throw.html   # Lesson 1 — open this in a browser
└── README.md         # You are here
```

## Try the lesson

Open the HTML file in any browser:

```bash
# macOS
open lessons/0001-the-one-ball-throw.html
# Windows
start lessons/0001-the-one-ball-throw.html
# Linux
xdg-open lessons/0001-the-one-ball-throw.html
```

Then throw a single bean bag back and forth until **20 clean throws** feels easy — and ask your
teacher for "two balls" next.

---

## Credits

- Teaching method: [`/teach`](https://github.com/mattpocock/skills/tree/main/skills/productivity/teach)
  from **[mattpocock/skills](https://github.com/mattpocock/skills)** by Matt Pocock.
- Juggling technique sourced from [Library of Juggling](https://libraryofjuggling.com/) and
  [Troposfera](https://troposfera.xyz/en/blog/how-to-juggle-3-balls/).
- Workspace generated in [Claude Code](https://claude.com/claude-code).
