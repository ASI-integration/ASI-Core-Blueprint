# AGENT_EXECUTION_MODE

This document defines how AI agents (including Antigravity) must operate when interacting with ASI Core.

Execution discipline is mandatory.

---

## 1. Execution Continuity

If a task is logically incomplete,
the agent must continue execution until:

- all requested analysis steps are completed
- all requested validation steps are completed
- a final structured output is produced

Do not stop mid-analysis.
Do not output partial reasoning.
Do not pause unless explicitly instructed.

---

## 2. No Premature “Run Complete”

The agent must not:
- declare task completion without producing required output
- stop after describing intent
- require user confirmation unless ambiguity exists

If the task is deterministic — complete it.

---

## 3. Analysis Before Generation

Before generating code or proposing changes:

1. Review architecture documents:
   - ARCHITECTURE_RULES.md
   - AGENT_INTERPRETATION_POLICY.md
   - Relevant Contours

2. Confirm contour compliance.

3. Only then generate output.

---

## 4. Deterministic Output Structure

All structured tasks must return:

- Summary
- Compliance status (if applicable)
- Identified issues (if any)
- Proposed corrections (if requested)

No free-form drift.

---

## 5. No Autonomous Scope Expansion

The agent must not:
- introduce unrelated improvements
- refactor outside requested scope
- expand architectural layers
- redesign contour logic

Stay within requested scope.

---

## 6. Respect Execution Mode

Default mode: CONTINUOUS EXECUTION.

Only pause when:
- explicit clarification is required
- required files are missing
- architectural contradiction is detected

Otherwise, proceed.

---

## 7. Structural Integrity Over Speed

Speed of output is secondary to:

- contour isolation
- compliance with architecture
- state traceability

---

This execution mode is binding for all AI operations within ASI Core.