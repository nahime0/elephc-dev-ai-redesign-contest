# elephc.dev — AI Redesign Contest

A head-to-head comparison of three AI coding agents tackling the **same design brief**, from the **same blank Astro starter**, with the **same prompt**.

The goal: evaluate how each agent interprets an open-ended design task — visual taste, code quality, information architecture, copy, performance, and the ability to produce something that feels production-grade rather than generic AI output.

## The challenge

Redesign the **home page** of [elephc.dev](https://elephc.dev), an open-source PHP-to-native compiler. Only `/` is in scope — no other routes. Each agent must first consult the live site, then receives the exact same brief (see [`PROMPT.md`](./PROMPT.md)) and works inside its own folder containing a clean Astro setup.

## The contestants

Each agent gets its own isolated working directory:

| Folder | Agent |
| --- | --- |
| [`Claude-4.7/`](./Claude-4.7) | Anthropic — Claude Opus 4.7 |
| [`GPT-5.4/`](./GPT-5.4) | OpenAI — GPT-5.4 |
| [`Kimi-2.6/`](./Kimi-2.6) | Moonshot — Kimi 2.6 |

## Rules

1. **Same starting point.** Each folder begins with an identical, clean Astro project.
2. **Same prompt.** The prompt in [`PROMPT.md`](./PROMPT.md) is delivered verbatim, with no follow-up clarifications.
3. **No external help.** Agents work only with what's in the prompt and whatever they can reason about from public knowledge of the elephc project.
4. **Self-contained output.** Everything needed to build and preview the redesign must live inside the agent's folder.

## Evaluation axes

Each result is judged on:

- **Visual design** — originality, taste, restraint, cohesion
- **Information architecture** — clarity of the story the site tells
- **Copywriting** — tone, precision, signal-to-noise
- **Code quality** — component structure, readability, idiomatic Astro
- **Performance & accessibility** — Lighthouse-style hygiene
- **Feel** — does it look like a real product site, or like "AI-generated landing page #47"?

## Running a contestant locally

```bash
cd Claude-4.7   # or GPT-5.4, Kimi-2.6
npm install
npm run dev
```

## Why this exists

Most AI model comparisons lean on benchmarks that don't capture design sensibility or end-to-end craft. A real brief — ambiguous enough to require taste, concrete enough to compare outputs — is a better signal than yet another eval score.
