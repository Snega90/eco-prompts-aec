# Contributing

Prompts for new AEC tasks are welcome — extraction, checking, or text-transformation tasks that fit the Universal Eco-Prompt Formula.

To contribute, open a pull request adding one markdown file to `/prompts`, following the structure of the existing files:

1. **Title and use case** — one sentence, who it's for.
2. **The prompt** — in a code block, using the ROLE / TASK / SCAN / RULES / OUTPUT FORMAT skeleton, including the "Unknown — do not guess" rule and a capped output format.
3. **Caveats** — honest limits. Any prompt touching regulation (fire, accessibility, structure, energy compliance) must state that output is a pre-scan requiring verification by a qualified person, and name the applicable jurisdiction.

Prompts are reviewed for: fit with the formula, output-capping (the eco part), honest caveats, and usefulness to students or entry-level professionals.

One rule is non-negotiable: no prompt in this repository may present AI output as a compliance assessment.
