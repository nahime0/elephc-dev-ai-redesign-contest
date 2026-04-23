# Prompt

> This exact text is delivered to each agent at the start of its session, inside its own folder.

---

You are a web developer and design expert.

In this clean Astro setup, create a complete redesign of **the home page** of the website for the **elephc** project.

**Before writing a single line of code, you must visit the current live site at https://elephc.dev and read it in full.** This is not optional. Study the current home page, its copy, its structure, its existing demo, and the tone of the project. Your redesign must be informed by what is actually there today — not by assumptions about what a compiler landing page usually looks like. If you cannot reach the site, stop and say so; do not proceed from imagination.

**elephc is** an open-source compiler that translates a static subset of PHP directly into native assembly code for standalone binaries. It is a true compiler — not a packager, a transpiler, or a runtime wrapper. There is no interpreter, no VM, and no Zend Engine fallback. The pipeline goes: parse → type-check → lower to native assembly → assemble → link. It runs on macOS ARM64, Linux ARM64 and Linux x86_64, ships with 1800+ tests, 220+ built-in functions, 10 data types and zero external runtime dependencies. The project is written in Rust, is currently at v0.19.x, and is heading toward a v1.0.0 release. Its audience is serious developers — people who want to accelerate performance-sensitive PHP modules, compile static PHP to native binaries, and drop the result into existing PHP frameworks without rewriting their applications.

**The current website** (elephc.dev) is a minimal, text-heavy technical landing page. It covers *How it works*, *Features*, *Docs*, *Get started* and *Roadmap*, and includes a Doom-style 3D engine demo compiled with elephc as proof of what the compiler can do. It does its job, but it does not yet feel like a product site that matches the technical ambition of the project underneath it.

Your job is to rebuild **the home page** so that it earns the project the credibility it deserves — a single page that a skeptical, low-level-curious developer lands on and immediately thinks "ok, this is serious." Other routes (docs, roadmap, etc.) are out of scope for this contest; you only deliver `/`.

## Scope

One page: the home page. A long-form, well-structured, scroll-driven page is expected — but everything lives under a single route. Links to *Docs*, *GitHub*, *Get started* and similar destinations should exist in navigation/CTAs but do not need to resolve to real internal pages; external links (GitHub, etc.) should point to plausible real URLs.

## What the home page should cover

Use the current elephc.dev home page as your reference for what matters, then make it better. At minimum, the page should articulate:

- **A sharp, confident hero** — one screen that makes clear *what elephc is*, *why it is interesting*, and *what makes it different from every other "compile X to native" project*. No marketing fluff, no generic "blazing fast" clichés.
- **How it works** — the compilation pipeline, explained visually. Take advantage of the fact that the pipeline has real, teachable stages (parse → type-check → lower → assemble → link). Diagrams, animations, annotated code — whatever makes it click.
- **Features / What's supported** — data types, built-in functions, platform matrix, what is and isn't in the static subset. Make the constraints feel like a feature, not a limitation.
- **Demo / Proof** — showcase the Doom-style 3D engine and/or any other compelling artifact already on the current site. Show, don't tell.
- **Get started** — installation and first compile, right there on the page. A developer should be able to go from "intrigued" to "I could run this tonight" without leaving the home.
- **Roadmap snapshot** — an honest status toward v1.0.0. A glance, not a full changelog.
- **Navigation + footer** — GitHub, docs link, license, version, community.

Feel free to add anything you think strengthens the story (benchmarks, a mini playground, a "why Rust" note, comparisons with existing tooling, FAQ, etc.) as long as it earns its space on the page.

## Design direction

You have full creative control. A few guardrails:

- **Have a point of view.** Pick a visual direction and commit to it. Anything that looks like a generic Tailwind template, a YC-era SaaS page or a Vercel clone is a failure.
- **Respect the audience.** This is for developers who read assembly output for fun. The design should reward attention: good typography, real information density where it helps, restraint where it doesn't.
- **Treat code as a first-class design element.** Syntax-highlighted snippets, terminal output, compilation stages, ASCII art, monospace — these are your materials, not decoration.
- **No stock illustrations, no gradient blob heroes, no emoji feature lists, no "Trusted by" logo walls.**
- **Motion is welcome but must mean something.** If something animates, it should be teaching the user how the compiler works, not filling time.
- **Accessible by default.** Proper contrast, keyboard navigation, respects `prefers-reduced-motion`, semantic HTML.

## Technical constraints

- Build it in **Astro**, using the existing setup in this folder. Don't switch frameworks.
- You may add any integrations, libraries or component frameworks (React, Solid, Svelte, Vue) you need, as long as you justify the dependency cost.
- Ship it as **static output** (`astro build`). No server runtime required.
- Keep it **fast**: avoid heavy client-side JS unless it earns its weight. Islands, not full hydration.
- Use **real, plausible content** everywhere, grounded in what you actually read on elephc.dev. No "Lorem ipsum", no "Feature title here", no placeholder screenshots. If a number isn't visible on the site, make a reasonable one based on what a v0.19 compiler would plausibly claim, and mark it as illustrative if needed.
- Make it **responsive** from ~360px up to ultrawide.
- Light mode, dark mode, or a considered single-mode choice — all fine, as long as the decision is intentional.

## Deliverables

1. A working Astro project in this folder. `npm install && npm run dev` must boot the site; `npm run build` must produce a clean static build.
2. A single home page at `/` implementing the full redesign.
3. A short `DESIGN_NOTES.md` at the root of this folder explaining, in under 300 words: what you took away from reading the current elephc.dev, the concept you chose for the redesign, the two or three decisions you're proudest of, and what you'd do next if you had another day.

## How you'll be judged

Your output will be compared side-by-side against home-page redesigns produced by two other AI agents working from this exact same prompt and the exact same starter. The winner is the one whose page a real developer would be most likely to bookmark, share, and trust.

Begin by opening https://elephc.dev.
