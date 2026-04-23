# elephc.dev Redesign — Design Notes

## What I took away from reading elephc.dev

The current site is already well-written and technically honest. It clearly communicates the core value proposition: a true PHP-to-assembly compiler, not a packager. Key artifacts I preserved: the Doom 3D engine demo, the seven-stage pipeline, the 1800+ tests / 220+ functions / 10 types / 0 deps stats, the "PHP 4 and MySQL" origin story, and the honest FAQ about framework compatibility. The existing tone is confident but understated — I wanted to amplify that seriousness without adding marketing noise.

## Design concept

**"The Compiler as Craft"** — A dark, terminal-informed editorial aesthetic that treats code and assembly as first-class design materials. The palette refines the existing amber/cyan accents against a near-black background, using Instrument Serif for display type (carried over from the original site) and JetBrains Mono for everything code-related. The goal is a page that feels like reading a high-end technical journal: information-dense where it helps, restrained where it doesn't.

## Decisions I'm proudest of

1. **The PHP → Assembly hero pairing.** Instead of a generic terminal screenshot, the hero places the familiar `elephc hello.php` command side-by-side with real annotated ARM64 assembly output. This immediately answers "what does this actually do?" for a skeptical systems developer.

2. **The pipeline as a teaching layout.** The seven compilation stages are presented as a scroll-driven vertical list on the left, while the right column stays sticky showing a single function transforming from PHP source to assembly. The arrow-connecting pipeline bar at the bottom (`.php → tokens → AST → typed AST → .s → .o → binary`) reinforces the linear mental model.

3. **Information density without chaos.** The types grid, constructs tags, and platform matrix present real technical constraints as features rather than limitations. No emoji, no gradient blobs, no "blazing fast" — just accurate data organized clearly.

## What I'd do next

- Add a small interactive playground island (pre-hydrated) where visitors can type a PHP snippet and see the emitted assembly update live.
- Implement a benchmark section with reproducible numbers against PHP 8.3 JIT for computationally intensive workloads.
- Add a "Why Rust?" micro-essay, since the audience would care about that engineering decision.
