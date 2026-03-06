# ARCHITECTURE_COMPLIANCE_CHECKLIST

This checklist is used to verify architectural integrity of ASI Core.

It must be applied before:
- major refactors
- contour modifications
- new feature integration
- AI-generated structural changes

---

## 1. Contour Isolation

[ ] Does each contour operate within its defined responsibility?
[ ] Are any cross-contour responsibilities merged?
[ ] Are execution steps preserved in correct sequence?

If any contour absorbs another’s responsibility → NON-COMPLIANT.

---

## 2. Booking Intake Integrity (Contour 1)

[ ] Does Intake avoid business decisions?
[ ] Does Intake avoid financial logic?
[ ] Does Intake avoid risk evaluation?
[ ] Does Intake avoid operational triggers?

Intake must normalize and validate only.

---

## 3. Occupancy Risk Level (Contour 2)

[ ] Is risk calculated independently from financial assumptions?
[ ] Is risk treated as assessment, not decision?
[ ] Does risk logic avoid altering booking state directly?

Risk must inform, not execute.

---

## 4. Arrival Outcome Classification (Contour 3)

[ ] Is outcome strictly classification?
[ ] Is UNDETERMINED allowed?
[ ] Are explanations separated from classification?
[ ] Are financial consequences computed downstream only?

Outcome must not interpret intent.

---

## 5. Finance Containment (Contour 4)

[ ] Is financial logic executed only after outcome?
[ ] Are refunds, penalties, or payments computed downstream?
[ ] Is there any upstream financial assumption?

Finance must never influence earlier contours.

---

## 6. Communications Reactivity (Contour 5)

[ ] Does communication react to state?
[ ] Does communication avoid generating state?
[ ] Does it avoid overriding classification?

Communication must not mutate core state.

---

## 7. Audit Immutability (Contour 6)

[ ] Are historical records immutable?
[ ] Are decisions recorded without rewrite?
[ ] Is retroactive mutation prevented?

Audit must record, never reinterpret.

---

## 8. Source of Truth Enforcement

[ ] Does every derived state reference:
      - Booking ID
      - Contour origin
      - Event source?
[ ] Are silent state mutations prevented?

All state must be traceable.

---

## 9. Structural Stability Over Convenience

[ ] Were any optimizations performed that collapse contours?
[ ] Were abstractions introduced that blur contour boundaries?
[ ] Was DRY applied at the cost of isolation?

If structural clarity decreases → NON-COMPLIANT.

---

# Compliance Result

COMPLIANT / NON-COMPLIANT

If NON-COMPLIANT:
- list violated sections
- propose corrections without collapsing contour structure