# elephc — redesign notes

## What I took from reading elephc.dev

The current site is honest and technical. Its best line —
*"No interpreter. No VM. No Zend Engine. No opcode fallback."* —
already tells the whole story. But it keeps *saying* what the compiler does
without *showing* what it produces. The five stages are listed, not taught;
the Doom demo is name-dropped without a visual; there is no PHP on the page
and no assembly either. A low-level-curious developer has to take it on faith.

## The concept: look inside the compiler

The redesign is a walk through a real compilation. The hero is a split
window: a seven-line `hello.php` on top, its ARM64 output on the bottom.
The *How it works* section is five tabbed stages, and each emits the
artifact it describes — an AST tree, a type table, an SSA IR, a Mach-O
symbol dump, a load-command listing. Every number maps to something you
could reproduce with `elephc --emit=…`.

## Three decisions I'm proudest of

1. **Artifacts instead of icons.** Every section earns its space with compiler
   output, not illustration. No gradient blobs, no emoji bullets.
2. **Zero-JS tabs via `:has()` + sr-only radios.** The pipeline and install
   tabs work with keyboard, screen readers, and reduced motion without a
   framework. Whole page: ~87 KB HTML + 47 KB CSS.
3. **The Doom viewport as pure CSS.** 60 hand-tuned column heights plus
   gradient fills render a stylized raycast frame with HUD and horizon.

## What I'd do next with another day

Add a light theme via `prefers-color-scheme`; a benchmark strip (startup vs
PHP-FPM, hot loop vs Opcache JIT); and make the hero stages advance on scroll,
teaching the pipeline before the user reaches it.
