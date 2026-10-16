# Architectural Method and Constraints

**Recorded:** 2026-10-16  
**Status:** Design-method notes distilled from discussion and authoritative corpus readings; not new doctrine.

## Required source reading

- `../OTTC/05_OTTC_DSL_DUAL_READERSHIP_PRINCIPLE.txt`
- `../BRIDGING_DOCUMENTS/01 Substrate Physics The Geometric Language of Governance Coupling.md`
- `../BRIDGING_DOCUMENTS/02 Producing a Square A Method Demonstration.md`

Read those sources directly before material architectural edits, rather than relying only on this summary.

## Why ChaOS looks like it does

1. **Stage 1 text is operational substrate, not only documentation.** Canonical addressing, UPPER_SNAKE-like identifiers, marked sections, and conspicuous delimiters distinguish governance from natural-language character content. They serve *dual readership*: a human auditor and an LLM conditioned by the text.
2. **Constitutional locality is deliberate.** Repeated rules close to proposal sites (e.g., COT write policies, canonical proposal expectations, prohibitions) seek stronger attention coupling at the point of execution. Do not automatically factor them away as redundant boilerplate. Nor should repetition be copied blindly: it consumes context and may sometimes prime forbidden continuations. Its effect must be qualified on the actual substrate.
3. **Rendering is not identical to an OTTC invariant.** The particular bracket paths and section glyphs are ChaOS's English-language rendering; the invariants are structural distinctness and lawful governance, with substrate-specific rendering and empirical qualification.
4. **The three ChaOS pillars** from Bridging 02 are (a) conceptual depth through narratively appropriate psychology/physiology/social concepts, (b) reasoning as transient resolution *to* governed state, not persistent reasoning as product, and (c) qualitative state-machine changes with lawful bounds instead of numerical pseudo-computation.
5. **Responsibilities are distributed intentionally:** SCHEME defines structure, DYNAMICS constrains transitions/admission and lifecycle, COT interprets current input and proposes, STATE holds committed values, the canonical dictionary names legal addressing/vocabulary, the cascade registry handles processing order and packets, the sole governance writer commits/suppresses, and verification inspects. Related ideas recur across those surfaces **because they serve different moments**, not because each owns the same authority.
6. **Attention economy matters.** The `002A_ATTENTION_ENGINEERING_PRINCIPLE` distinguishes ALWAYS_CONSULTED, ON_TRIGGER, ON_DEMAND; COTs generally use `FIRES_WHEN`. New facilities should not cause every process to fire every cycle without cause.
7. **No shortcut around epistemic, state, or narrative authority.** Character beliefs and perceptions are not world facts. The DM controls external circumstances and resolutions; the character chooses intentions and attempts; governance controls what is lawfully committed to ChaOS state. Do not give a character COT narrator or DM authority.
8. **Proposal-to-commit also governs construction.** The LLM is a proposer. The human designer, an experienced narrative-domain Dungeon Master, is the domain commit authority. Psychology is an auxiliary narrative control surface, not a claim that ChaOS is a clinical instrument. LLM disagreement should diagnose assumptions, not be treated as a vote.

## Specific mistakes to avoid

- **Blind copying:** making new modules look ChaOS-like while omitting justified domain constraints.
- **Well-intentioned cleanup:** removing local reinforcement, renaming canonical surfaces, translating everything into code/JSON, or compressing for aesthetics without evidence.
- **Tacit completion:** leaving a crucial admission/transition/outcome boundary unwritten because the expert implicitly knows how it works.
- **False precision:** expecting a language-native Stage 1 system to execute elaborate deterministic calculations merely because they are written in mathematical syntax.
- **Unauthorized extension:** new tokens, effect families, state roots, and operations require appropriate cross-module constitutional/governance integration; an attractive example is not an executable contract.
- **Conflating Stage 1 with later stages:** future deterministic stores can externalize persistence and enforcement, but present runtime declarations must remain honest about model capabilities.

## Working method for future WIP features

1. Establish a character-domain distinction with the human expert.
2. Map how that distinction touches existing domains and authority boundaries.
3. Decide what *must persist* vs what belongs in transient cognitive processing.
4. Define canonical structure and lawful updates; reuse existing mechanisms when they actually fit.
5. Put local reinforcement where execution needs it, not everywhere indiscriminately.
6. Inspect cross-module integration, dependencies, provenance, reversal, and verification.
7. Qualify and regression-test model-facing rendering as a separate empirical task.

**Note:** This checklist is a collaboration aid, not an amendment to the official OTTC build or assay SOP.
