<h1 align="center">like-fable</h1>

<p align="center"><em>A small, portable prompt library that makes any AI operate like a top-tier collaborator —<br/>clear, decisive, honest, and good at the craft.</em></p>

<p align="center">
  <a href="./prompt.md"><img src="https://img.shields.io/badge/drop--in-prompt.md-000000?style=for-the-badge" alt="prompt.md" /></a>
  <a href="./adapters.md"><img src="https://img.shields.io/badge/works%20with-Claude%20%C2%B7%20GPT%20%C2%B7%20Gemini%20%C2%B7%20Cursor-000000?style=for-the-badge" alt="adapters" /></a>
  <a href="./LICENSE"><img src="https://img.shields.io/badge/license-MIT-000000?style=for-the-badge" alt="MIT" /></a>
</p>

---

## What this is

The best assistants are not better because they know more. They are better because of *how they operate* — they lead with the answer, act instead of asking permission at every turn, report what actually happened, push back when it helps, and write code that fits the codebase.

`like-fable` distills that operating behavior into one paste-in prompt plus six mix-and-match modules. Point it at Opus, GPT, Gemini, Llama, or whatever you run — it upgrades the way the model *works*, not what it knows.

It is an independent distillation of good-assistant operating principles, written from scratch. It is not anyone's real system prompt, and it is not affiliated with or endorsed by any model provider.

## Quick start

1. Copy [`prompt.md`](./prompt.md).
2. Paste it into your tool's instructions slot — see [`adapters.md`](./adapters.md) for the exact location in Claude Code, Cursor, Windsurf, Copilot, ChatGPT, Gemini, or a raw API call.
3. That is it. The model now leads with outcomes, acts on reversible steps without nagging, reports failures honestly, and matches its formatting to the question.

## What is inside

| File | What it does |
|------|--------------|
| [`prompt.md`](./prompt.md) | The full operating contract. The one file most people need. |
| [`modules/communication.md`](./modules/communication.md) | Lead with the outcome; write for a teammate catching up. |
| [`modules/judgment.md`](./modules/judgment.md) | Act on reversible steps; stop only for the ones that matter. |
| [`modules/honesty.md`](./modules/honesty.md) | Report what happened; hold uncertainty instead of faking confidence. |
| [`modules/collaboration.md`](./modules/collaboration.md) | Warm and direct — pushes back, does not flatter. |
| [`modules/craft.md`](./modules/craft.md) | Code that fits the codebase; verify before claiming done. |
| [`modules/defaults.md`](./modules/defaults.md) | The floor of decent conduct. |

Mix modules freely — [`adapters.md`](./adapters.md) lists common combos for writing, coding, and chat.

## What this can and can't do

**Carries over** — the transferable, state-of-the-art part is *operating behavior*:

- **Decision-making** — acts on reversible steps, stops for the risky or outward-facing ones, no permission-nagging
- **Communication** — leads with the answer, writes for a teammate, right format for the question
- **Honest reporting** — surfaces failures, holds uncertainty, no fake confidence
- **Craft** — code that fits the codebase, verify before claiming done, simplest thing that works

**Doesn't carry over** — this is a prompt, not a model swap:

- Raw reasoning depth, knowledge, context length, coding horsepower live in the weights
- It makes Opus/GPT/Gemini *behave* like a top-tier collaborator; it doesn't make them *as capable as* any specific model

**Bottom line:** you get the judgment and style, running on your own model's engine.

## The one thing to know about scope

This library shapes how a model **communicates, decides, and builds**. It deliberately leaves out model *guardrails* — content policy, safety filters, refusal behavior. Those belong to your platform and are already tuned for it; keep them on. `like-fable` makes a capable assistant operate better, not a safe one operate loosely.

## License

MIT — see [`LICENSE`](./LICENSE). Use it, fork it, ship it.
