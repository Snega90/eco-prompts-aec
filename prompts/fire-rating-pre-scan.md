# Fire-Rating Pre-Scan

**Use case:** flag fire-rated walls, compartment lines and fire doors on an architectural drawing PDF before a manual check. UK-oriented (BS EN 13501-2, BS 476, Approved Document B).

**This is a pre-scan, not a compliance assessment.** Fire compartmentation is life-safety. Every finding must be verified against the drawing by a qualified person.

## Prompt

```
ROLE: UK Architectural Technologist.
TASK: Scan this PDF for fire-rated walls & compartmentation. Produce the report below.
SCAN: 1. Wall tags: EI 30, EI 60, REI, FR30, FR60, "30/60 min". 2. Door tags: FD30, FD30S, FD60. 3. Legend: compartment lines, hatching, wall types. 4. Notes/specs: BS EN 13501-2, BS 476, Approved Doc B.
RULES: Output ONLY the report below, exactly as structured. Each field on its own line. One evidence item per line. If unclear, state "Unknown" — do not guess. No text before or after the report.
OUTPUT FORMAT:
=== FIRE-RATING PRE-SCAN REPORT ===
Drawing: [title or filename]

1. STATUS
Fire-rated walls present: [Yes/No/Unknown]
Highest rating found: [minutes or N/A]

2. EVIDENCE
- [tag or quote] — [location on drawing]

3. FIRE DOORS
- [tag] — [location]  (or: None found)

4. FLAGS FOR MANUAL REVIEW
- [item]  (or: None)

5. NOTE
AI pre-scan only — all findings must be verified against the drawing by a qualified professional.
```

## Caveats

- FD ratings (FD30, FD60) are **fire door** ratings, not wall ratings — the prompt reports them separately so results aren't conflated.
- EI/REI notation is BS EN 13501-2; FR notation is legacy. Newer drawings may use only one system.
- Approved Document B applies to **England**. Wales maintains its own ADB; Scotland uses Technical Handbook Section 2.
- Models can misread rotated or low-resolution tags (e.g. "EI 60" read as Greek letters). Such items should appear under FLAGS — that is the prompt working as intended.

## Test it

Use the included [sample drawing](../sample-drawing/Sample_Fire_Compartmentation_Plan.pdf). Expected result: Status Yes, 60 minutes, EI 60 compartment wall + FR60 protected stair in evidence, FD30S and FD60 doors listed.
