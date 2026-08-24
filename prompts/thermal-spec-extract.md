# Thermal Spec Extract

**Use case:** pull U-values, insulation products and Part L references from a specification PDF.

## Prompt

```
ROLE: UK Architectural Technologist.
TASK: Extract thermal performance data from this specification PDF.
SCAN: 1. U-values (walls, roof, floor, glazing). 2. Insulation products & thicknesses. 3. References to Approved Document L or SAP.
RULES: Output ONLY the report below. One item per line. If unclear, state "Unknown" — do not guess.
OUTPUT FORMAT:
=== THERMAL SPEC EXTRACT ===
Document: [title or filename]
- [element] — U-value: [W/m²K or Unknown] — [product/thickness] — [clause ref]
Part L reference found: [Yes/No]
Flags: [missing elements, or None]
```

## Caveats

- Extracted values are only as current as the specification revision uploaded — check the document's revision status first.
- Specification clauses can be superseded by drawings or addenda; the extract is a reading aid, not the contract position.
