# Eco-Prompts for AEC

**Energy-efficient, hallucination-resistant AI prompts for architecture, engineering and construction workflows.**

Free to use with any AI assistant that accepts file uploads (ChatGPT, Gemini, Claude, Copilot). Built for architectural technology students and entry-level professionals as a basic, safe starting point for AI on drawings and specifications.

---

## Why "eco"?

AI prompts have a measurable environmental cost. Google's published data for a median Gemini Apps text prompt: **0.24 Wh of electricity, 0.03 g CO₂e, and 0.26 ml of water** (Elsworth et al., 2025). Small per prompt — multiplied by billions of prompts a day.

The key insight: **generating output costs far more energy than reading input.** So the biggest saving available to any AI user is designing prompts that produce short, structured answers instead of long conversational ones.

Every prompt in this repository follows that principle: compressed input, capped structured output, right first time.

## The Universal Eco-Prompt Formula

```
ROLE: [your professional role]
TASK: [action verb + exact goal]
SCAN: [numbered list of what to look for]
RULES: Output ONLY the format below. No intro, no summary.
       If unclear, state "Unknown" — do not guess.
OUTPUT FORMAT:
[the exact skeleton of the answer you want]
```

Why each line earns its place:

- **ROLE** — context in three words, no backstory paragraph.
- **TASK** — starts with a verb. Verbs get answers; vagueness gets essays.
- **SCAN** — a numbered checklist the AI can actually tick off.
- **"Unknown — do not guess"** — the single best anti-hallucination line. On low-detail drawings it returns honest gaps, not invented facts.
- **OUTPUT FORMAT** — caps the generation. The AI fills your skeleton instead of writing an essay around it.

## Ready-to-use prompts

| Prompt | Use case |
|---|---|
| [Fire-rating pre-scan](prompts/fire-rating-pre-scan.md) | Flag fire-rated walls, compartment lines and fire doors on a drawing PDF |
| [Door & window schedule](prompts/door-window-schedule.md) | Extract tagged doors/windows into a checkable schedule |
| [ISO 19650 naming check](prompts/iso19650-naming-check.md) | Validate title-block drawing numbers field by field |
| [Accessibility pre-scan](prompts/accessibility-pre-scan.md) | Flag accessibility provisions (and gaps) on a floor plan |
| [Thermal spec extract](prompts/thermal-spec-extract.md) | Pull U-values and insulation data from a specification |
| [Snagging record](prompts/snagging-record.md) | Convert rough site notes into a formal defect list |

## How to use

1. Open any AI assistant that accepts PDF/image uploads.
2. Upload your (anonymised) drawing or document.
3. Paste the prompt. Done.

**To reuse without re-pasting:** save the prompt as a [Gemini Gem](https://support.google.com/gemini/answer/15235603) (free on every plan) — paste it once as the Gem's Instructions, then just upload a file each time. Note: saving a prompt saves *your* time; the energy saving comes from the prompt's design.

**Test it:** a [sample fire compartmentation plan](sample-drawing/Sample_Fire_Compartmentation_Plan.pdf) is included (fictional, for training only) so you can reproduce the fire-rating pre-scan and see the structured output for yourself.

## Limitations and safety — read before using

- **AI reads text, tags and labels — not geometry.** It can read a dimension that is written; it cannot reliably measure one that isn't. Build SCAN lists around what is readable.
- **Life-safety tasks are pre-scans, not assessments.** Fire compartmentation and accessibility outputs are a starting point for a qualified person's check — never a compliance judgement.
- **Hallucination is real.** Models can misread rotated or low-resolution text. The "Unknown — do not guess" rule reduces this; it does not eliminate it.
- **You verify, always.** Every AI finding must be checked against the source document by a human before it informs any decision.
- **Data care.** Anonymise drawings before uploading to consumer AI tools. No free consumer tier currently guarantees UK-only data processing. For live project work, follow your practice's AI policy.
- **Best input = vector PDF**, cropped to the relevant zone. Better accuracy *and* fewer input tokens.

## Contributing

Have an AEC task that fits the formula? Open a pull request adding a prompt file to `/prompts` using the same structure: use case, prompt, output format, caveats. Prompts for tasks touching regulation must include a verification caveat.

## References

Fully cited sources (energy figures, UK standards, hallucination literature) in [REFERENCES.md](REFERENCES.md).

## Licence & citation

Released under [CC BY 4.0](LICENSE) — free to use, adapt and share with attribution.

> Sekar, S. (2026) *Eco-Prompts for AEC*. Available at: https://github.com/YOUR-USERNAME/eco-prompts-aec

Created by **Snega Sekar** — [LinkedIn](https://www.linkedin.com/in/YOUR-PROFILE)
