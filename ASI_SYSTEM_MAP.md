# ASI System Map

This document describes the high-level operational structure of the ASI system.

The platform is organized around several operational contours that form the decision and execution pipeline.
Booking Intake
↓
Occupancy Risk Evaluation
↓
Arrival Outcome Processing
↓
Operational Decision Layer
↓
Execution Layer

## Core Operational Contours

### Booking Intake
Handles reservation ingestion from OTA channels and direct booking sources.

Document:
01_Contour_Booking_Intake.md

---

### Occupancy Risk Evaluation
Analyzes guest signals and determines operational risk.

Document:
02_Contour_Occupancy_Risk_Level.md

---

### Arrival Outcome Processing
Determines operational outcomes and system actions.

Document:
03_Contour_Arrival_Outcome.md

---

### Finance Contour
Processes revenue flows, ledger entries, and financial state.

Document:
04_Contour_Finance.md

---

### Communications Contour
Manages automated communication workflows.

Document:
05_Contour_Communications.md

---

### Audit Memory & Accountability
Stores traceable operational history and system decisions.

Document:
06_Contour_Audit_Memory_Accountability.md

---

## Core Architecture Context

Additional system architecture is described in:

- ASI_CONTEXT.md
- ASI_SCENARIOS.md
- Operational_Event_Model.md
- ARCHITECTURE_RULES.md
- WORKING_RULES.md

---

This document represents the structural map of the ASI system.
