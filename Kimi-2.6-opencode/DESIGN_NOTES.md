# Design Notes: elephc.dev Home Page Redesign

## What I took away from elephc.dev

The current site is honest and technically dense — a no-nonsense landing page that clearly communicates what elephc is and isn't. It leads with the compilation pipeline, distinguishes itself from packagers, and includes a Doom 3D engine demo as proof. The personal story in the footer adds warmth to an otherwise cold technical subject. What it lacks is visual authority: it reads like a README, not a product that serious developers should bet on.

## Design concept

**"The Compiler's Interface"** — a dark, terminal-inspired aesthetic that treats code and compilation as first-class visual elements. The design language borrows from developer tools (IDEs, terminals, debuggers) rather than SaaS marketing pages. Every section uses monospace typography, terminal windows, syntax highlighting, and structured data to reinforce that this is a tool built by developers, for developers.

The color palette is restrained: deep blacks and grays with precise accent colors (blue for primary actions, green for success, orange for warnings, purple for keywords). No gradients, no blobs, no stock imagery.

## Decisions I'm proudest of

1. **The hero terminal** — Instead of a generic headline, the hero features a live terminal window showing the actual compilation pipeline. It demonstrates the product before the user reads a word.

2. **Scroll-driven pipeline visualization** — The "How it works" section transforms the compilation stages into an interactive, vertical pipeline with real code snippets at each stage (PHP source → type error → ARM64 assembly). This teaches the user how the compiler works through progressive disclosure.

3. **The Doom ASCII demo** — Rather than a screenshot, the demo section uses an ASCII art representation of the 3D engine inside a terminal window. It reinforces the "no runtime" claim viscerally: this is what native code looks like when you strip away all the abstraction.

## What I'd do next

With another day, I would add a live benchmark comparison (elephc vs PHP vs HHVM), an interactive playground where visitors can type PHP and see the generated assembly, and smooth scroll-triggered animations for the pipeline stages using a lightweight library like GSAP.
