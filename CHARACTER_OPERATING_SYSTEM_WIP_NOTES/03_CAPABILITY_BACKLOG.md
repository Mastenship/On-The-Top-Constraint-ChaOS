# Future Character Capabilities — Discussion Backlog

**Recorded:** 2026-10-16  
**Status:** Topics identified during design discussion; not specifications or implementation commitments.

The WIP directory provides a safe place to extend ChaOS, but **character-domain meaning and cross-module authority boundaries must come before file drafting**.

## Inventory / item continuity — ACTIVE DISCOVERY

See [02_INVENTORY_DISCOVERY.md](02_INVENTORY_DISCOVERY.md). Proposed item records are sparse, line-oriented, governed by a broad schema and canonical token dictionary, and extendible as new DM-established facts enter the character's experience. Items can affect action affordances, skill performance, cascades, and personal meaning. No canonical schema adopted yet.

## Equipment and tools

Ordinary weapons, tools, protective gear, and special devices may enable attempts or improve/constrain performance without conferring permanent mastery. Distinguish item properties, access/activation, current performance, personal skill, subjective beliefs, and DM resolution. May be a facet of inventory rather than a separate persistent subsystem; undecided.

## Money and economic resources

Purchases, trade, price/value interpretations, spending, scarcity, opportunity costs, and resource decisions. The character chooses whether and how to spend; the DM establishes external transactions and outcomes. Still open whether fungible currency belongs as item records, a special inventory resource category, or an adjacent economic surface. Avoid false precision in Stage 1 calculations.

## Item attachment and sentimental meaning

Mother's Locket, a love letter, heirlooms, gifts, important possessions. Material presence vs durable memory/identity/relationships must remain distinct; emotional meaning may persist after loss or transfer. Open whether attachment is a conditional line within the item record or a separately governed link.

## Embodied self-concept

Separate objective or DM-established physiological capabilities/conditions (`SCHEME_BODY`) from the character's perceived bodily competence, self-image, confidence, or mistaken beliefs about bodily capacity. Must not grant objective physical capabilities from self-perception alone.

## Appearance, clothing, and personal style

Objects and clothing connect Inventory to character self-presentation and personal choice. Choice of what to wear belongs to the character; DM establishes material availability and external consequences. Appearance affects identity, social interpretation, possibly performance, but is not reducible to equipment bonuses.

## Delayed processing / “Memories of Obligations of the Future” — DEFERRED BY CHOICE

The human architect explicitly chose **not** to design this first. Later exploration may address persistent promises, pending requests, intentions, uncompleted concerns, avoidance, deferral, and eventual completion or abandonment.

Potential distinction from existing modules:
- `MEM_XX`: past episodic experience
- `GOAL_XX`: desired outcome or motivation
- `PRD_XX`: future expectation/prediction
- `DEFERRED_NARRATIVE_CUES`: governance-related postponed update processing

A potential `OBL_XX` is **only an assistant-side candidate**, not an approved record type. Prospective memory must allow the character to voluntarily postpone, ignore, reject, or abandon commitments; do not turn character cognition into a productivity application. Bounded active attention should not silently erase significant unresolved history. Integration decisions remain open.

## Design order

Inventory is the present exploration topic. The remaining list is a **backlog, not a mandated sequence**. Dependencies will become clearer as the human architect evaluates concrete DM scenarios. No subsystem here has been canonically registered.
