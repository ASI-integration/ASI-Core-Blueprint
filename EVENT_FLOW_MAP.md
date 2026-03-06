# ASI Event Flow Map

This document describes how operational events move through the ASI system.

The ASI architecture is event-driven. Operational decisions are produced through a sequence of evaluation layers.

## Core Event Flow

Guest Booking Event
↓
Booking Intake
↓
Occupancy Risk Evaluation
↓
Arrival Outcome Processing
↓
Operational Decision
↓
Execution Layer

## Event Processing Layers

### Booking Intake
Receives reservation data from OTA platforms and direct booking channels.

Triggers:
- booking_created
- booking_modified
- booking_cancelled

Document:
01_Contour_Booking_Intake.md

---

### Occupancy Risk Evaluation
Evaluates the risk profile of the reservation using guest and contextual signals.

Triggers:
- risk_evaluation_requested

Document:
02_Contour_Occupancy_Risk_Level.md

---

### Arrival Outcome Processing
Determines the operational action required by the system.

Possible outcomes:
- approve_arrival
- flag_for_review
- deny_arrival

Document:
03_Contour_Arrival_Outcome.md

---

### Finance Contour
Handles revenue accounting and ledger events.

Triggers:
- booking_confirmed
- payout_calculated

Document:
04_Contour_Finance.md

---

### Communications Contour
Executes automated communication flows.

Triggers:
- send_guest_message
- send_checkin_instructions
- send_reminder

Document:
05_Contour_Communications.md

---

### Audit Memory & Accountability
Records system decisions and operational history.

Triggers:
- decision_recorded
- event_logged

Document:
06_Contour_Audit_Memory_Accountability.md

---

## Event Model Reference

The detailed event model is defined in:

Operational_Event_Model.md
