# Door & Window Schedule Extraction

**Use case:** pull all tagged doors and windows from a floor plan PDF into a checkable schedule.

## Prompt

```
ROLE: UK Architectural Technologist.
TASK: Extract all doors & windows from this PDF into a schedule.
SCAN: 1. Door tags (D01, D02...). 2. Window tags (W01...). 3. Dimensions on plan or in legend. 4. Fire/acoustic ratings if tagged.
RULES: Output ONLY the report below. One element per line. If unclear, state "Unknown" — do not guess.
OUTPUT FORMAT:
=== DOOR & WINDOW SCHEDULE (PRE-SCAN) ===
Drawing: [title or filename]
Doors:
- [tag] — [size] — [rating or N/A] — [location]
Windows:
- [tag] — [size] — [location]
Flags: [missing tags / unclear items, one per line]
```

## Caveats

- The AI can only extract dimensions **written** on the drawing or legend — it cannot measure drawn geometry.
- Untagged elements will not appear; the Flags field should note rooms where openings appear untagged.
- Cross-check the extracted schedule against the drawing before using it in any deliverable.
