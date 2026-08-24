# Accessibility Pre-Scan

**Use case:** flag accessibility provisions — and gaps — on a floor plan. UK-oriented (Approved Document M context).

**Indicative only — never a compliance assessment.**

## Prompt

```
ROLE: UK Architectural Technologist.
TASK: Pre-scan this floor plan for accessibility provisions.
SCAN: 1. Accessible WC / ambulant cubicles. 2. Door clear widths noted. 3. Level thresholds, ramps, gradients. 4. Lift or stair-only access.
RULES: Output ONLY the report below. If unclear, state "Unknown" — do not guess. Findings are indicative only, not a compliance assessment.
OUTPUT FORMAT:
=== ACCESSIBILITY PRE-SCAN ===
Drawing: [title or filename]
Accessible WC shown: [Yes/No/Unknown]
Door widths noted: [values or Unknown]
Level access: [Yes/No/Unknown]
Flags for Part M review: [items, one per line]
```

### Variant for concept-stage sketches

Concept drawings carry little dimensional data — this variant checks *named provisions* instead of measurements:

```
ROLE: UK Architectural Technologist.
TASK: Check this concept sketch for accessibility provisions named in the brief.
SCAN: 1. Accessible WC named. 2. Lift named (if multi-storey). 3. Step-free entrance indicated. 4. Accessible parking indicated.
RULES: Output ONLY the format below. If unclear, state "Unknown" — do not guess.
OUTPUT FORMAT:
Provisions named: [list]
Provisions missing from sketch: [list]
Cannot be assessed at concept stage: [list — e.g. door widths, gradients]
```

## Caveats

- On an information-poor drawing, a mostly-"Unknown" report is the **correct** result — the prompt returns a gap list instead of invented compliance claims.
- The AI cannot measure clear widths, turning circles or gradients from geometry — only read them where annotated.
- Approved Document M applies to England; Wales and Scotland have their own provisions.
