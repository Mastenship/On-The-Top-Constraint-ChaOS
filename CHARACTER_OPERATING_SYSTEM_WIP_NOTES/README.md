# ChaOS WIP — Design Notes

**Status:** Working discussion record, not a ChaOS runtime module or an approved architecture specification.  
**Started:** 2026-10-16.  
**Companion directory:** `../CHARACTER_OPERATING_SYSTEM_WIP/` (the editable ChaOS architecture).  
**Stable reference:** `../CHARACTER_OPERATING_SYSTEM/` (do not modify merely to explore proposals).

## Why this directory exists

Preserve the reasoning, domain distinctions, proposed mechanisms, unresolved choices, and examples from ChaOS WIP design conversations so a future collaborator or a later conversation can recover the *why*, not merely copy the surface style. The design is still in discovery. Notes here are not self-authorizing instructions to change the architecture.

Keep these notes **outside the WIP module folder and its load-order table of contents**: they are design memory, not runtime instructions. A note does not create canonical tokens, permit new operations, or amend OTTC governance.

## Read in this order

1. [01 — Architectural method and constraints](01_ARCHITECTURAL_METHOD.md) — why ChaOS's formatting, repetition, authority boundaries, and qualitative mechanics matter.
2. [02 — Inventory discovery](02_INVENTORY_DISCOVERY.md) — the principal active design conversation; established directions and unresolved questions.
3. [03 — Capability backlog](03_CAPABILITY_BACKLOG.md) — other future character capabilities and possible inventory dependencies.

## Interpretation and maintenance

- **USER-ESTABLISHED** records ideas explicitly introduced or clarified by the human ChaOS architect. It does not mean a complete schema has been approved.
- **WORKING INFERENCE / ASSISTANT PROPOSAL** records ideas offered during discussion; treat as candidates, not adopted requirements.
- **OPEN** identifies undecided questions. Do not silently turn them into design commitments.
- Dated notes describe the state of the discussion on that date. When decisions change, record the new decision and what it supersedes.
- In all architecture drafting, the human narrative-domain expert holds **commit authority**. The LLM proposes and reviews; it does not independently approve domain ontology.
- Before building a new subsystem, reread relevant authoritative OTTC/ChaOS files. These notes are navigational aids and reasoning continuity, not a substitute for the corpus.

## Current implementation status

The WIP architecture initially contains an exact copy of the 70 stable ChaOS modules. As of these notes (2026-10-16), **no inventory module or inventory canonical vocabulary has been drafted or committed**.
