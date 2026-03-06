# AGENT_INTERPRETATION_POLICY

This document defines how AI agents (including Antigravity) must interpret ASI Core architecture.

---

## 1. No Creative Reinterpretation

Contours are not suggestions.
They are constraints.

Do not:
- merge contours
- simplify execution flow
- move responsibilities across contour boundaries
- “optimize” by collapsing layers

If a change conflicts with contour isolation — the contour wins.

---

## 2. Architectural Intent Overrides Local Optimization

If:
- performance optimization,
- refactoring,
- abstraction,
- DRY principle

conflicts with contour separation —

architectural separation must be preserved.

---

## 3. No Implicit State Inference

Do not:
- infer financial outcome from booking state
- infer risk from missing data
- infer communication logic inside classification contours

If logic is not explicitly defined in contour documentation,
it must not be invented.

---

## 4. UNDETERMINED Is Valid

If signals are incomplete or contradictory,
the correct result is UNDETERMINED,
not a forced classification.

Do not attempt to “guess”.

---

## 5. Finance Is Never Upstream

No upstream contour may:
- assume payment validity
- assume refundability
- pre-compute penalties

Finance reacts to outcome — never the opposite.

---

## 6. Audit Is Immutable

Audit contour records history.
It does not rewrite history.

Agents must not introduce retroactive state mutation.

---

## 7. If Uncertain — Preserve Structure

When ambiguity arises:
- preserve contour isolation
- preserve execution order
- avoid shortcut logic

Structure stability is preferred over local convenience.

---

This policy is binding for all generated or modified logic.
Violations must be treated as architectural errors.