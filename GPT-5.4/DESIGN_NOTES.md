Reading the current `elephc.dev` home page, the main takeaway was that the project already had the right substance but not yet the right framing. The existing site is technically honest, very text-heavy, and centered on a few crucial ideas: this is a real compiler, not a PHP wrapper; the pipeline is parse -> type-check -> lower -> assemble -> link; the DOOM renderer is the proof; and the near-term roadmap is about turning standalone binaries into something framework-adjacent.

The redesign concept is a "compiler dossier": darker, denser, and more artifact-driven than a normal SaaS landing page. I treated code, assembly, build logs, and target matrices as first-class visual material. The goal was to make the page feel like something low-level-curious developers would actually slow down and read.

The decisions I am happiest with are:

1. The hero board, which shows PHP source, assembly output, build timings, and targets immediately instead of hiding the mechanics.
2. The pipeline section, which teaches the compiler stages through intermediate representations rather than vague diagrams.
3. The supported-subset section, which frames the constraint as leverage and ties it directly to compiler extensions like `packed class`, `buffer<T>`, `extern`, and `ptr`.

With another day, I would add a small interactive pipeline explainer with user-controlled stepping, generate a custom still/poster for the DOOM demo instead of using a remote asset, and tighten typography further with self-hosted fonts.
