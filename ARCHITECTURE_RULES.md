# ARCHITECTURE_RULES

This document defines non-negotiable architectural constraints of ASI Core.

These rules override optimization attempts, refactoring impulses, and convenience shortcuts.

---

## 1. Contours Do Not Collapse

Contours are isolated logical domains.

No contour may:
- absorb responsibilities of another contour
- shortcut execution order
- introduce cross-contour decision logic

Contours execute in defined sequence only.

---

## 2. Booking Intake Is Not a Decision Layer

Contour 1 (Booking Intake):

- does not interpret
- does not evaluate risk
- does not trigger operations
- does not perform financial reasoning

It normalizes and validates only.

---

## 3. Outcome Is Classification, Not Explanation

Contour 3 (Arrival Outcome):

- classifies factual state
- may return UNDETERMINED
- does not assign blame
- does not compute financial consequences

---

## 4. Finance Is Downstream

Financial logic is applied only after outcome determination.

No contour upstream may:
- assume payment validity
- assume refundability
- infer penalties

---

## 5. Communication Is Reactive

Contour 5 (Communications):

- reacts to state
- does not generate state
- does not override classification

---

## 6. Audit Is Immutable

Contour 6 (Audit / Memory / Accountability):

- records decisions
- never rewrites history
- never auto-corrects previous states

---

## 7. Source of Truth Is Explicit

All derived states must reference:
- Booking ID
- Event origin
- Contour that produced the state

No silent state mutations are allowed.

---

These rules are considered canonical constraints of ASI Core.
Violations must be treated as architectural errors.