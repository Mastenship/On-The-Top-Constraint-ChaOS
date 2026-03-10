# OTTC — On-The-Top Constraint
### A Governance Protocol for Stateful LLM Agents

OTTC is a language-native governance protocol that constrains how LLM agents manage persistent state over long horizons. It doesn't modify model weights. It doesn't claim determinism. It provides addressable state, governed mutation (propose→commit with single-writer authority), bounded epistemic claims, and full audit closure — enforced through a text-based constitution that conditions the LLM's continuation space. ChaOS (Character Operating System) is the included working demonstration: a psychologically grounded character state machine with 65 structured files implementing OTTC-compliant governance across personality, physiology, memory, relationships, beliefs, goals, and cognition.

---

## The Problem

LLM agents that maintain state over long horizons fail in predictable ways:

- **State drift** — persistent fields silently mutate without justification or record.
- **Thrash** — competing subsystems overwrite each other; the system converges on nothing.
- **Epistemic overreach** — the model asserts facts, reads minds, and narrates outcomes it has no evidence for.
- **Audit theater** — governance-looking output that fails cross-checks; the record is a story, not a log.
- **Ungoverned tool calls** — syntactically valid but cognitively misguided actuation; the tool fires before reasoning has resolved.

These aren't model failures. They're architectural failures. The model does what models do. The architecture lets it.

---

## The Core Insight

LLMs are meaning-generation systems. Control enters through semantics before it enters through arithmetic.

If the substrate is meaning, governance must be semantic.

The same governance pattern that works for human institutions works for LLM agents: free deliberation → constrained decision → accountable outcome. You don't need to understand the model's internal representations to govern its behavior. You govern the interface — canonical state, lawful transitions, bounded authority, auditable change — and continuity emerges as a system property.

A DM at a tabletop RPG cannot read a player's mind. They can only judge by how the player plays the game. And the game has rules. The rules are what make meaning transferable across sessions, across players, across years. OTTC is those rules, applied to a new substrate.

---

## OTTC in Brief

### The 9 Rectangle Axioms

These are the mandatory kernel invariants. Any compliant implementation must satisfy all nine.

1. **Canonical Address Space** — One canonical way to refer to any state element. No synonyms at the write surface.
2. **Propose-Commit Separation** — All mutation is expressed as proposals first; persistent state changes only at commit boundaries.
3. **Single-Writer Persistent State** — Exactly one authority writes persistent state per cycle.
4. **Explicit Update Operations** — State changes through a finite, named set of operations (SET, TRANSITION, ADD_MODIFIER, REMOVE_MODIFIER, CAP, VETO).
5. **Hard State vs. Soft Modifiers** — Distinguishes durable baseline state from transient overlays. Short-lived context doesn't rewrite identity.
6. **Step Limits and Override Triggers** — Hard-state changes are bounded per cycle. Breaking bounds requires explicit, named override triggers with proof.
7. **Deterministic Conflict Resolution** — When proposals conflict, resolution follows deterministic policy (precedence + tie-breakers).
8. **Audit Closure** — Every proposal accounted for exactly once (committed/suppressed/downgraded) with a reason. No silent drops.
9. **Post-Commit Verification** — After commit, a verification pass checks invariants and integrity. Verification certifies or flags — it never invents new changes.

These nine axioms define the "rectangle." Any compliant implementation is a "square" — free to choose its own schemas, syntax, domains, and operations as long as these invariants hold.

### Key Properties

- **Qualification Assay doctrine** — Blind pre-build testing of model coupling before architecture decisions. Measure the ground before laying foundations. Different models couple differently to the same constitution; this is not a bug, it's a measurement.
- **Authority scaling** — Models get roles matching their demonstrated coupling. The citizen/governor/auditor split maps authority to demonstrated reliability.
- **Maturity path** — From in-model scaffold → hybrid → fully externalized deterministic governance. The architecture is designed to hand off as external infrastructure matures.
- **Semantic Abacus** — LLMs handle meaning at the write surface; numeric precision is externalized downstream. The model doesn't compute — it recognizes, interprets, and proposes. Deterministic systems compute.
- **Governed tool calls** — Tool actuation is proposed, not unilateral. An LLM proposes a tool call; governance commits or vetoes; the deterministic system executes; the LLM interprets the result and sends forward more proposals. This is safer than letting the LLM decide to fire a tool mid-reasoning with no accountability boundary.
- **Hypothesis Machine** — Any OTTC-compliant architecture is a candidate for structured hypothesis tracking. Proposals can encode hypotheses; commit records their status; verification checks their validity; audit closure ensures none are silently abandoned. The same governance pattern that makes state legible makes scientific claims legible.

---

## ChaOS: A Working Demonstration

ChaOS is one possible "square" inside the OTTC rectangle — a character state machine built for narrative and RPG use. It demonstrates that the framework is not abstract. It can be built, loaded, and run.

### Architecture

**65 files** organized into three layers plus supporting infrastructure:

| Layer | Prefix | Mutability | Purpose |
|---|---|---|---|
| Ontology | `SCHEME_` | Immutable | Field schemas, enums, ordinals, invariants. The scientific constitution. |
| Transition law | `DYNAMICS_` | Immutable | Under what conditions and how fields may change. |
| Current values | `STATE_` | Mutable | The only layer that changes at runtime. |

Plus: governance overlay, cascade registry, canonical token dictionary, formatting rules, and the cognitive scratchpad (a volatile, per-cycle transaction surface).

### 16-Step COT Execution Pipeline

ChaOS models cognition as a sequential chain of concern-specific reasoning steps, each contributing proposals to the commit cycle:

1. Spatial awareness
2. Temporal processing
3. Temporal decay
4. Subconscious / Shadow COT
5. Stress cascade
6. Goal pursuit
7. Malevolent behavior (Dark Triad-gated)
8. Attachment mapping
9. Performance state integration
10. Alteration effects
11. Belief integration
12. Memory formation
13. Predictive frame synthesis (DPF)
14. Decision synthesis
15. Governance commit (single writer)
16. Post-commit verification

### Psychological Grounding

The ontology draws on established frameworks: HEXACO, MMPI, Dark Triad, Adult Attachment Style (ASQ), Maslow's hierarchy of needs, HPA axis stress modeling, predictive processing / active inference, and established memory encoding and decay principles. These are not decorative references. Each domain defines discrete states with lawful transitions and specific update rules.

### Anti-Fragile Narrative Property

Errors of state don't break ChaOS — they become narrative material. A governance-accepted cortisol spike that was "too high" is not a system failure. It's a character living with chronic stress. OTTC doesn't make the system correct or truthful. It makes it legible. In a narrative domain, legible errors are plot points.

### DSL and Dual Readership

The internal DSL is designed for two simultaneous readers: human domain experts and LLM attention heads. Structural markers serve as attention anchors. Bracket-path canonical addressing (`[STATE_BODY][BIOCHEMICAL_STATE_MARKERS][CORTISOL]`) is maximally distinct from natural language prose, reducing ambiguity at the write surface. Constitutional repetition — the write contract restated in every COT — keeps governance in local context rather than relying on long-range attention.

### External Governance Composition

ChaOS is designed to hand off to deterministic external systems. Structured proposals are machine-parseable. The immutable/mutable file split supports external state ownership. The scratchpad lifecycle (instantiate → populate → commit → verify → wipe) is a transaction boundary. The verification checklist is implementable as a programmatic validator.

ChaOS is a demonstration, not a production system. It will degrade under context pressure. No in-model system survives indefinitely — probability always wins as context accumulates. The architecture is designed to compose with external governance when that happens.

---

## Who This Is For

Four audiences. Full renderings for each are in `AUDIENCE_RENDERINGS/`.

**ML/LLM Researchers**
Testable hypotheses about constitutional conditioning, with operationally defined metrics and ablation structure. OTTC makes predictions about observable behavior differences between governed and ungoverned architectures. Those predictions are falsifiable.

**Agent Framework Developers**
A protocol, not a framework. OTTC plugs into existing orchestration rather than replacing it. The result is agent state that is inspectable, testable, and auditable — not a black box that might be doing something reasonable.

**Game Masters and Narrative Designers**
A system that gives LLM characters inertia, bounded perspective, and earned growth over long-form play. The character has a genuine history that constrains what it can plausibly do next. Continuity is structural, not just probabilistic.

**Enterprise Governance / Safety**
Change control and accountability for long-running agents, with audit trails that support compliance and incident review. When something goes wrong, the record shows what was proposed, what was committed, and what verification found. That's the minimum viable artifact for responsible deployment.

---

## What OTTC Is Not

This section is here because honest scope is what separates a framework from a promise.

- **Not a silver bullet** — OTTC systems can still fail, drift, and produce harmful outputs. Governance reduces frequency and improves detectability. It does not prevent.
- **Not determinism** — Text constraints shape probability; they do not create hard runtime guarantees. Deterministic behavior requires externalized enforcement. The in-model layer is always stochastic.
- **Not truth** — OTTC does not prevent hallucinations. It aims to make violations detectable and auditable. A hallucination that lands in the audit record is at least visible.
- **Not model-independent** — Different models couple differently to the same constitution. Qualification is mandatory before architecture decisions. Assuming coupling is the most common mistake.
- **Not a replacement for software** — For high-stakes decisions, deterministic validators, policy gates, and external enforcement are required, not optional. The in-model layer is the proposal layer. The deterministic layer is where consequential action happens.
- **Not a substitute for oversight** — Audit artifacts can be performative unless cross-checked. OTTC creates the record. Humans and deterministic validators have to read it.

---

## Origin

The author is a Game Master with over forty years at the table — tabletop and computer RPGs — and a U.S. Army veteran who has written SOPs and built small relational systems in Access and Excel. Enough background to understand that stability comes from clear write surfaces, clear authority, and procedures that hold under stress. A year ago he did not know what an LLM really was.

He tried to use LLMs for deep character work and hit the wall: shallow persistence, pattern collapse, and the peculiar kind of confidence that is not evidence. He discovered Venice AI and persistent context — files you can actually drop in and have the model maintain. Most people use that for a long backstory. He tried that. It wasn't enough.

So he iterated. Not alone. He iterated with multiple LLMs as collaborative thinking partners: Gemini, ChatGPT, Claude, Venice models. Cross-checked constantly, because hallucination is real. He learned as much from model disagreements as from convergences. Different models carry different training biases — those biases became a triangulation advantage. When models agreed, that was signal. When they disagreed, drilling into *why* they disagreed often revealed structure no single model would surface.

The first system that worked was a tag-to-cue pipeline. Then he made the mistake most people make: tried to steer with numbers. Built a hundred-thousand-token math system. It crashed — the model could no longer hold the semantic relationships, numeric fields bled into narrative context, and the whole structure became incoherent under load. Built a smaller math system. Also crashed, for the same fundamental reason. The numeric layer and the meaning layer are not the same substrate; trying to make one do the work of the other degrades both.

Then a model said: *"You know we don't actually do math, right."*

Everything clicked. An LLM is a meaning-making machine. Its only medium is language. If you want control, you must touch the probability space with words that already have mass inside the model. Numbers can attach to concepts — but the steering comes from meaning, not arithmetic.

Three pillars emerged from that moment:

1. **Conceptual depth** — Don't encode characters as coordinates. Invoke concepts the model already knows deeply — psychology, physiology, social dynamics, habit loops, stress models — then constrain how those concepts are allowed to update.
2. **Chain of thought as process, not product** — Reasoning is transient. It resolves. It resolves to a state.
3. **Qualitative state machine mechanics** — Discrete states and lawful moves. Not math. Mechanics. Step limits. Transitions. A place for transient overlays that do not rewrite identity.

Three months from those pillars to the full ChaOS architecture. Then governance layers were added — propose-only writers, a single committer, canonical addressing, step limits, auditability, verification.

And then the pattern became visible across the whole edifice. Nothing in it was new as an isolated engineering principle. All textbook. All public domain. Obvious in hindsight. But the synthesis appeared to be new: a closed protocol of stable state surfaces, controlled mutation, bounded authority, and auditable change.

OTTC was extracted from that pattern.

There is one more thing worth stating: the collaborative process that produced the architecture and the architecture itself turned out to be the same pattern. Multiple generators exploring freely. One authority deciding what gets committed. Deterministic rules for resolving conflicts. Full accountability. The author did not just use the protocol to build ChaOS. He was already running the protocol while building it. He was the commit authority. The LLMs were the proposal layer. The DM training was the conflict resolution policy. When he recognized the isomorphism, OTTC became a named thing.

Total cost: less than $500 out of pocket and nine months of spare time while working full-time. The first six months were the learning curve. The last three months were the build.

---

## Repository Structure

```
OTTC/                        — Framework specification (axioms, scope, qualification, testable hypotheses)
CHARACTER_OPERATING_SYSTEM/  — ChaOS demonstration architecture (65 files)
AUDIENCE_RENDERINGS/         — OTTC rendered for researchers, developers, DMs, and enterprise
LICENSE                      — CC BY-NC 4.0
```

---

A quick note on voice and format:

These documents were written for LLMs first. The models were the original teachers. The rigid sections, repeated invariants, UPPER_SNAKE canonical paths, and ceremonial structure are not stylistic flourishes — they are deliberate DSL choices designed to be attention-head friendly so the constitution remains stable across thousands of tokens and collaborative interaction. Humans are welcome to read along; the protocol works for any long-horizon agent. If the ritual tone feels unusual at first, drop the files into an LLM’s persistent context and watch it parse the rectangle instantly — that is the point. By making the documents themselves attention head friendly, the LLMs can assist human readers in how to use OTTC properly and how to build their own OTTC complaint architectures.

---

## License

[CC BY-NC 4.0](LICENSE) — Creative Commons Attribution-NonCommercial 4.0 International.

Free to share and adapt for non-commercial purposes, with attribution. If you build on this work commercially, reach out.

---

## Status and Contact

This is active work. The framework is stable; the demonstration architecture is functional; the external governance integration layer is the current frontier.

Questions, observations, and collaboration inquiries can be directed through GitHub: [@Mastenship](https://github.com/Mastenship).
