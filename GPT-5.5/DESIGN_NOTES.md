# Design Notes

The live elephc page is already unusually specific: it leads with a real compiler contract, not vague speed claims. The important takeaways were the hard distinction from packagers and PHP runtime wrappers, the explicit parse -> type-check -> lower -> assemble -> link pipeline, the Doom-style demo, and the credibility signals around v0.19.7, 1800+ tests, 220+ built-ins, 10 data types, three native targets and zero external runtime dependencies.

I chose a "compiler bench" concept: dense, dark, terminal-native and source-oriented, with code and assembly treated as the main visual material. The goal is to make the page feel like a serious systems project while still giving a skeptical PHP developer a clear path from concept to first compile.

The decisions I am proudest of are: keeping the page dependency-free and static, making the compiler pipeline the central diagram instead of decorative art, and turning the static subset into a strength by presenting it as the reason elephc can make native-code promises. I also kept the Doom proof prominent, but represented it honestly as a CSS recreation rather than pretending to ship a benchmark.

With another day, I would add a tiny WASM-free interactive source/assembly switcher fed by real examples from the repository, plus measured build/test output from the current release.
