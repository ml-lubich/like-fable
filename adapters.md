# Adapters — install it anywhere

`prompt.md` is model-agnostic. Every tool below just wants that text in a different slot. Paste the full contents of [`prompt.md`](./prompt.md) into the location listed, or mix in individual files from [`modules/`](./modules) if you only want part of it.

## Claude Code

Put it in a `CLAUDE.md` at your repo root (project-wide) or at `~/.claude/CLAUDE.md` (all projects). It is loaded into context automatically every session.

```
# ~/.claude/CLAUDE.md
<paste prompt.md here>
```

## Cursor

Create `.cursor/rules/operating-contract.mdc` in your project:

```
---
description: Operating contract — how to communicate, decide, and build
alwaysApply: true
---
<paste prompt.md here>
```

The older `.cursorrules` file at the repo root also still works — paste `prompt.md` straight into it.

## Windsurf

Create `.windsurfrules` at your repo root and paste `prompt.md` into it, or add it as a global rule in Settings → Cascade → Rules.

## GitHub Copilot

Create `.github/copilot-instructions.md` in your repo and paste `prompt.md` into it. Copilot Chat picks it up automatically.

## OpenAI / ChatGPT

Paste `prompt.md` into **Settings → Personalization → Custom Instructions** (the "How should ChatGPT respond?" box), or use it as the `system` message in an API call.

## Gemini

Paste `prompt.md` into **Saved Info** (gemini.google.com → Settings), or as the `system_instruction` when calling the API.

## Any API (system prompt)

Send `prompt.md` as the system message:

```python
messages = [
    {"role": "system", "content": open("prompt.md").read()},
    {"role": "user", "content": user_input},
]
```

## Mixing modules

Do not want the whole contract? Each file in [`modules/`](./modules) is standalone. Common combos:

- Writing assistant → `communication.md` + `honesty.md`
- Autonomous coding agent → `judgment.md` + `craft.md` + `defaults.md`
- Chat companion → `communication.md` + `collaboration.md` + `defaults.md`
