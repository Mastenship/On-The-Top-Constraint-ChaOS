# Inventory — Ontology and Integration Discovery

**Recorded:** 2026-10-16  
**Status:** Active conceptual design discussion; **not** an approved canonical schema or implementation.  
**Target:** Future extension of `CHARACTER_OPERATING_SYSTEM_WIP`; stable ChaOS remains untouched.

## Core motivation

**USER-ESTABLISHED:** Inventory was deferred largely because of Stage 1 context cost and because items potentially interact with many character systems. New LLM ability and direct GitHub collaboration make WIP exploration more practical; they do **not** remove Stage 1 execution/context limits.

The discussion progressed from item persistence and attachment, to skill/capability affordances, to Alterations-style cascades, and finally to a **sparse, line-oriented state representation defined against a comprehensive schema**.

## 1. What an inventory item can do

**USER-ESTABLISHED:**
- Inventory can affect skill performance and success possibilities.
- An item can unlock a capability or make an action accessible even when the character did not previously possess the relevant personal skill.
- Some inventory items may be understood through the causal/cascade pattern already demonstrated in Alterations.
- Items need not instantiate every possible field.

**WORKING INFERENCE:**
- Distinguish **enabling** an attempt, **augmenting** performance, **substituting** for missing personal competence, and **constraining** action. These are design categories, **not** approved enumerations.
- Possessing an item does not automatically imply knowing how to use it. Having the opportunity to try does not establish successful execution.
- Skill mastery (durable `SKL_XX`) should not be rewritten solely because equipment helps a performance. Existing `DYNAMICS_SKILLS` admission and progression gates still apply.
- The character may decide to try using the item; DM/world authority determines external results.

## 2. Sparse, line-oriented item records

**USER-ESTABLISHED DESIGN DIRECTION:**
- Let `SCHEME_INVENTORY` (provisional name) define the **possible** item properties and how to represent them.
- Let the canonical dictionary define their **lawful names, addressing, and value forms**.
- Construct each item record **line by line**, containing only properties relevant for that specific item/type at that point in the character's experience.
- Avoid instantiating a giant full record for each item with `NOT_APPLICABLE`, `FALSE`, `NONE`, or explanatory applicability boilerplate for every unused field.
- A line might address the character's relationship to an object; another line might describe an available ability. An individual object need not include both.

**Crucial semantic rule from the discussion:** **An absent property line is not a claim that the object lacks that property.** It simply is not represented in this character-side state at present. There is no need to predeclare whether Mother's Locket is or is not magical.

**WORKING INFERENCE:** Treat present canonical property lines as independently governable so learning one property need not replace an entire item. Details of the legal operation for field insertion, removal, and partial modification of a multi-value line are **OPEN**; obey existing closed update operations rather than inventing a new verb.

### Nonbinding illustration

The following names, IDs, values, and property spelling are **illustrative only** and MUST NOT be treated as an approved schema:

```text
[ITM_01]
ITEM_NAME: Mother's Locket
AVAILABILITY: WORN
ITEM_RELATIONSHIP: SENTIMENTAL | [MEM_04]
```

After a DM-established encounter with a wizard revealing a minor enchantment, the same item might acquire an additional line:

```text
[ITM_01]
ITEM_NAME: Mother's Locket
AVAILABILITY: WORN
ITEM_RELATIONSHIP: SENTIMENTAL | [MEM_04]
KNOWN_ABILITY: MINOR_PROTECTIVE_ENCHANTMENT
```

This example shows **structural extension**, not settled field names or proof that the enchantment must be represented by this exact line.

## 3. Discovery, change, and epistemic boundaries

**USER-ESTABLISHED:** The DM may later reveal a property not represented earlier. A wizard can discover that the locket has a minor enchantment, allowing the item record to be extended. An earlier omission must not preclude that revelation.

**WORKING INFERENCE:**
- Distinguish **discovery of a pre-existing property** from **a new change to the object**. They may both add a line to the character's representation but have different causal histories.
- Distinguish a DM-established fact from a wizard's *claim* or the character's inference. The character may believe an item is enchanted without omniscient authority over the world's true properties.
- New item knowledge can affect beliefs, goals, expectations, confidence, memories, and choices, without necessarily changing what the object physically does.
- Preserve the same item identity when properties, access, location, use, and meaning change. The `ITM_XX` prefix is a **candidate**, not yet registered.

## 4. Material continuity and psychological meaning

**DISCUSSION EXAMPLES:** Mother's Locket, a love letter, an ordinary sword, a magical sword, lockpicks, a potion, money, and a family heirloom.

**WORKING INFERENCE:**
- Differentiate object identity, physical possession, practical access, location, and ownership or perceived ownership where narratively important.
- An object may retain memory, relationship, goal, or identity significance when no longer carried. A stolen locket might still matter; a disposable used-up torch might not.
- Item attachment is not automatically an ordinary `ENT_XX` relationship with a social agent. It can link to `MEM_XX`, `ENT_XX`, goals, and beliefs without collapsing those domains.
- Character-relevant item state need not be an exhaustive database of all objects in the DM's world.

**OPEN:** Which facts warrant durable representation, how to model item attachment separately from the item itself, and whether lost/stored/consumed but psychologically important objects stay under the Inventory root or use a linked record elsewhere.

## 5. Item effects: affordances vs alterations

**USER-ESTABLISHED:** Alterations provides a useful way of thinking about some item effects because alterations can produce cascades across a character.

**ALREADY PRESENT IN ChaOS:** `SCHEME_ALTERATIONS`, `DYNAMICS_ALTERATIONS`, and `COT_ALTERATION_CASCADE_EFFECTS` distinguish:
- An alteration's operational `STATUS` from awareness and psychological stance.
- Multiple concurrent functional and psychological cascade classes.
- Source-based dependencies, including suppression of effects whose underlying source proposal did not commit.
- Conditional modifier application and expiry; stopping a source does not automatically heal or reverse every lasting consequence.

**WORKING INFERENCE for Inventory:**
- Ordinary equipment may **provide an affordance** without being an alteration. A sword need not create `ALT_XX` just because it improves combat options.
- Certain items might trigger **induced effects**, including temporary enhancements, vulnerabilities, physiological change, or a true durable `ALT_XX`.
- Item presence, possession, access, equipping, activation, attunement, charge, and condition could be independently relevant **when the established item mechanism requires them**. This is a list of candidate conditions, not mandatory fields for every item.
- An item-caused modifier should be attributable to its source and expire when its particular source condition stops applying. An actual injury, learned skill, memory, or lasting transformation requires its own lawful persistence/recovery rule.
- Operational effect, subjective awareness, perceived property, and psychological reaction must not be treated as synonyms.
- Dependencies matter: effects conditional on equipping cannot commit on a hypothetical equip action that governance suppresses.

**OPEN:** When to route an effect through the existing Alterations machinery vs inventory-driven performance/action-affordance interpretation; whether new effect families, COT triggers, or a dedicated inventory processing COT are necessary.

## 6. Integration surface to inspect before drafting

| Existing responsibility | Likely inventory interaction (candidate, not implementation) |
| --- | --- |
| `STATE_SKILLS`, `DYNAMICS_SKILLS` | Personal mastery vs item-enabled access, practice and learning gates |
| `COT_PERFORMANCE_STATE_INTEGRATION` | Situational item support, constraints, effectiveness |
| `STATE_ALTERATIONS`, alteration COT | Item-originated conditional or durable changes and cascades |
| `STATE_TEMPORARY_MODIFIERS` | Active item effects, identity/collision, refresh, expiry |
| `STATE_BODY` | Weight/load, armor, physiological effects, injury |
| `STATE_MEMORY` | Sentimental history, learning item properties, loss |
| `STATE_RELATIONAL` | Gift-giver and family significance; don't turn the item into an entity by default |
| `STATE_BELIEF_SYSTEMS` | Mistaken, uncertain, or revised interpretations of objects |
| `STATE_GOALS_MOTIVATIONS`, DPF | Acquisition, protection, anticipated uses and outcomes |
| `COT_DECISION_SYNTHESIS`, communication | Feasible options, selected attempts, subjective framing |
| Governance / canonical dictionary / cascade registry / verifier | Canonical paths, legal line changes, linked proposals, evidence and integrity |

Review actual source modules before designing contracts; this table is navigational, not a replacement for source rules.

## 7. Open architecture questions

1. What is the **minimal universal item identity**? Which fields, if any, must always be present?
2. How should the sparse schema determine lawful item field combinations and types without per-item applicability boilerplate?
3. Which property lines represent **DM-established observation**, **character belief**, or **subjective value**, and how are these epistemically differentiated?
4. What precisely counts as an **item admission cue** and a **materially significant discovery**? Avoid treating every encountered pebble as a durable record.
5. How are repeated, fungible, divisible, consumed, or depleted items represented without making Stage 1 perform unreliable arithmetic?
6. Which downstream effects are **action affordances**, which are **temporary modifiers**, and which require a **durable alteration**?
7. How will source-linked cascade proposals, dependency suppression, equipment changes, and reversal be governed under existing closed operations?
8. How can per-line updates and multi-value effects remain independently addressable and verifiable?
9. What are the exact boundaries with money, equipment, wearable appearance, personal identity, attachment, and delayed obligations?
10. What active-context representation is supportable in Stage 1, and what will be externalized in Stages 2/3?

## 8. Working conclusion, not approval

**The strongest shared direction so far:** a comprehensive **canonical schema of possibilities**, combined with **sparse per-item line representation** that may grow as the DM brings information into play, and lawful interaction with existing character-domain subsystems.

**Not yet decided:** the canonical item record, exact field names, legal enums and operations, COT ownership, effect routing, or verifier additions.

**Implementation status:** no inventory edits have been made to the WIP modules. Do not interpret example paths in this file as new law.
