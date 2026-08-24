# ISO 19650 Drawing-Naming Check

**Use case:** validate the drawing number in a title block against an ISO 19650-style field structure.

## Prompt

```
ROLE: UK BIM information manager.
TASK: Check the drawing number in this PDF's title block against the ISO 19650 naming convention.
SCAN: 1. Title block: drawing number, revision, status code. 2. Field structure: Project-Originator-Volume/System-Level-Type-Role-Number.
RULES: Output ONLY the report below. If unclear, state "Unknown" — do not guess.
OUTPUT FORMAT:
=== NAMING CHECK REPORT ===
Drawing number found: [string]
Compliant: [Yes/No/Unknown]
Field breakdown:
- [field] = [value]
Issues: [missing/malformed fields, or None]
```

## Caveats

- ISO 19650 permits project-specific field conventions — the AI checks structure, not your project's information standard. Adjust the SCAN field list to match your project's agreed convention.
- Status codes and revisions vary by project information protocol; treat "Compliant: Yes" as a structural check only.
