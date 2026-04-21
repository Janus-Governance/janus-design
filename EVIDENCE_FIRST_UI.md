# Evidence-First UI Validation

## Principle

Visual anomalies must be validated against evidence before modifying the system.

## Rationale

User interfaces can misrepresent system state due to:
- browser zoom
- cache
- rendering differences
- local environment conditions

Intervening based on perception alone can introduce unnecessary changes and break system consistency.

## Rule

Do not modify styles, layout, or typography unless the anomaly is reproducible and confirmed by inspecting the actual source (CSS, HTML, tokens).

## Validation Steps

1. Inspect source styles (CSS / tokens)
2. Compare against baseline definitions
3. Verify environment:
   - zoom level
   - cache state
   - device / viewport
4. Confirm reproducibility

Only after these steps, apply changes.

## Example

A typography inconsistency was perceived in the core surface.

Investigation revealed:
- no discrepancy in CSS or tokens
- browser zoom set to 80%

Conclusion:
- no system change required

## Principle Summary

The UI can mislead.
The source of truth is the system definition.
