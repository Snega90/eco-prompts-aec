# Snagging Record from Site Notes

**Use case:** convert rough site notes (typed or photographed) into a formal defect list with trade, location and priority.

## Prompt

```
ROLE: UK Architectural Technologist.
TASK: Convert my rough site notes below into a formal snagging record.
SCAN: 1. Defect described. 2. Location. 3. Trade responsible. 4. Urgency.
RULES: Output ONLY the report below. One defect per line. If a detail is missing from my notes, state "Unknown" — do not invent.
OUTPUT FORMAT:
=== SNAGGING RECORD ===
Date/visit: [from notes or Unknown]
- [ref no.] — [defect] — [location] — [trade] — [priority H/M/L]
Items needing clarification: [list or None]

NOTES: [paste your rough notes here]
```

## Caveats

- The AI formats what your notes contain — it cannot know what you saw but didn't write. "Items needing clarification" is the field to watch.
- Priority assignments are inferred from your wording; review them before issuing the record.
- Anonymise project-identifying details before uploading to a consumer AI tool.
