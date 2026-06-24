# OTTC — On-The-Top Constraint
### A Governance Protocol Born from the Mutation Boundary Problem

Long-horizon LLM agents do not fail only through wrong answers or unsafe actions. They fail when persistent state, identity, commitments, or shared context mutate in ways that become **illegible, unbounded, or unauditable over time**. Memory drifts. Transient moods harden into permanent identity. Speculation congeals into committed fact without evidence. Fluent output masks the absence of any accountable logic of change.

This corpus names that challenge the **Mutation Boundary Problem** — the problem of governing the transition between generative exploration and durable state change in stateful opaque generative systems — and offers **OTTC** as one provisional, constructive response to it. OTTC does not modify model weights and does not claim determinism. It provides addressable state, governed mutation (propose→commit with single-writer authority), bounded epistemic claims, and full audit closure, enforced through a text-based constitution that conditions the model's continuation space. **ChaOS** (Character Operating System) is the included working demonstration: a psychologically grounded character state machine of **70 structured files** implementing OTTC-compliant governance across personality, physiology, memory, relationships, beliefs, goals, and cognition.

The Mutation Boundary Problem is the intellectual capstone of this corpus. OTTC and ChaOS are constructive examples of what responding to it can look like. **Neither claims to have solved it.** OTTC's value should be judged against the alternatives already in use — ad hoc state mutation, vague memory, hidden authority, prose-level accountability, long-horizon drift disguised as adaptive behavior — not against fantasies of perfect interpretability or perfect determinism. The honest claim is narrow: opaque, stochastic, meaning-generating agents become *more governable* when durable change is mediated through canonical addresses, lawful operations, bounded authority, explicit proposal/commit separation, transient-vs-baseline distinctions, epistemic-status typing, audit closure, and post-commit verification. This is not prompt magic; it is governance architecture, and the data testing its strongest claims is still being gathered.

---

## How the Corpus Was Built — and Why That Matters

The single most important structural fact about this corpus is that **the collaborative process that produced it and the architecture it describes are the same pattern.** This is not a retrospective gloss. The method was the protocol before the protocol had a name.

The author is a Game Master with over forty years at the table — tabletop and computer RPGs — and a U.S. Army veteran who has written SOPs and built small relational systems in Access and Excel. Enough background to understand that stability comes from clear write surfaces, clear authority, and procedures that hold under stress. A year ago he did not know what an LLM really was.

He tried to use LLMs for deep character work and hit the wall: shallow persistence, pattern collapse, and the peculiar kind of confidence that is not evidence. He discovered persistent context — files you can drop in and have the model maintain. Most people use that for a long backstory. He tried that. It wasn't enough.

So he iterated. Not alone. He iterated with multiple LLMs as collaborative thinking partners — Gemini, ChatGPT, Claude, Venice models — cross-checking constantly, because hallucination is real. He learned as much from model *disagreements* as from convergences. Different models carry different training biases; those biases became a triangulation advantage. When models agreed, that was signal. When they disagreed, drilling into *why* often revealed structure no single model would surface.

The first system that worked was a tag-to-cue pipeline. Then he made the mistake most people make: he tried to steer with numbers. He built a hundred-thousand-token math system. It crashed — the model could no longer hold the semantic relationships, numeric fields bled into narrative context, and the structure became incoherent under load. He built a smaller math system. It also crashed, for the same fundamental reason: the numeric layer and the meaning layer are not the same substrate, and forcing one to do the other's work degrades both.

Then a model said: *"You know we don't actually do math, right."*

Everything clicked. An LLM is a meaning-making machine. Its only medium is language. If you want control, you must touch the probability space with words that already have mass inside the model. Numbers can attach to concepts — but the steering comes from meaning, not arithmetic. Three pillars emerged from that moment:

1. **Conceptual depth** — Don't encode characters as coordinates. Invoke concepts the model already knows deeply — psychology, physiology, social dynamics, habit loops, stress models — then constrain how those concepts may update.
2. **Chain of thought as process, not product** — Reasoning is transient. It resolves. It resolves *to a state*.
3. **Qualitative state-machine mechanics** — Discrete states and lawful moves. Not math. Mechanics. Step limits. Transitions. A place for transient overlays that do not rewrite identity.

From those pillars, three months produced the full ChaOS architecture. Then governance layers were added — propose-only writers, a single committer, canonical addressing, step limits, auditability, verification. And then the pattern became visible across the whole edifice. Nothing in it was new as an isolated engineering principle. All textbook. All public domain. Obvious in hindsight. But the *synthesis* appeared to be new: a closed protocol of stable state surfaces, controlled mutation, bounded authority, epistemic typing, and auditable change.

**ChaOS did not inherit OTTC. OTTC was recognized *inside* ChaOS.** When the author saw that the governance architecture he had built for the character system was a description of the *method he had used to build it* — multiple LLMs proposing, one human committing, disagreement adjudicated on evidence, every decision traceable to a reason — OTTC became a named thing. The isomorphism was not imposed from outside. It was already there, encoded in the work from the start, because the author was already living it. Single writer, bounded authority, no silent drops, proposal before commitment: that is how you build anything stable under adversarial conditions with multiple unreliable contributors. That is why the corpus has the shape it does.

Total cost: less than $500 out of pocket and nine months of spare time while working full-time. Roughly six months were the learning curve; the next three were building ChaOS and extracting OTTC, with the philosophical statement and the research agenda recognized and written across that same final stretch. All of it was done solely with Large Language Models operating as cognitive lenses, mirrors, and prosthetics — which is exactly the collaboration pattern the corpus is designed to scaffold for others.

---

## The Mutation Boundary Problem

**[Full paper: The Mutation Boundary Problem — A Research Agenda for Stateful Opaque Generative Systems](The%20Mutation%20Boundary%20Problem%20-%20A%20Research%20Agenda%20for%20Stateful%20Opaque%20Generative%20Systems/)**

The Mutation Boundary Problem appears when three conditions coincide. The system is **stateful** — something about its prior activity persists and conditions later behavior. It is **opaque** — the internal process by which it reaches an output is not fully inspectable in a way that can bear governance by itself. And it is **generative** — it produces outputs through probabilistic continuation rather than deterministic execution. Each condition matters; their combination is what creates the mutation boundary as a distinct problem.

The word *mutation* is deliberate. It refers to any transition by which a generative system's output becomes part of a durable reality that later cycles must inherit — a change to memory, a shift in a belief or hypothesis structure, a revised goal, a new relational commitment, a tool-mediated action with external effect. The *boundary* is where exploratory generation hardens into consequential state. *Governance* means that this transition is constrained by explicit conditions: what may change, under what operations, with what authority, under what evidentiary requirements, with what traceability, and with what mechanisms for review or suppression. The crux is a distinction between **exploration, interpretation, and commitment**: exploration is plural and provisional; commitment is singular and consequential. The problem is deciding how, when, and under what rules exploratory activity may become durable change.

### Why Current Framings Are Insufficient

The dominant framings each capture something real, and none alone — or in loose combination — captures the full problem:

- **Capability** asks what the system can do. It measures momentary performance, not whether outputs become lawful, durable participation.
- **Alignment** asks whether behavior matches human goals. A system can appear locally aligned while still altering its persistent state in opaque, unstable, or poorly justified ways.
- **Memory** asks how information is retained. But what is remembered, what is revised, what is authoritative, how prior content updates later state — these are governance questions, not storage questions.
- **Tool use** asks how models touch external resources. A tool call is also a claim about evidentiary need, authority, and consequence; a functional pipeline can still leave the boundary weak.
- **Prompting and orchestration** ask how outputs are shaped. They remain procedural without becoming constitutional — improving the path to an output without resolving who may change the world future outputs inherit.
- **Evaluation** asks how systems are measured. If no metric captures the difference between proposal and commitment, or transient and durable state, significant failure modes stay invisible.

The deeper insufficiency is the **transcript view** — treating the transcript as the primary artifact of meaning and audit. Transcripts conflate exploration, interpretation, justification, and consequence into one stream, obscuring what was considered, proposed, believed, committed, and actually changed. For long-horizon systems, that conflation becomes corrosive.

### The 11 Research Clusters

The paper decomposes the problem into eleven domains of inquiry — not a final taxonomy, but a map of where the boundary creates pressure:

1. **Ontology and Persistent State** — what may be persisted; what must be addressable for continuity to survive.
2. **Continuity and Identity** — what continuity is for an opaque probabilistic system; what makes change lawful rather than drift.
3. **Perspective and Epistemic Boundaries** — how bounded point of view is modeled and enforced; the distinction between perception, inference, speculation, and committed fact.
4. **Mutation and Governance** — how proposals form, what operations are legal, who may commit, how conflicts resolve; the institutional form of the boundary itself.
5. **Memory, History, and Causality** — when experience crystallizes into record; how memories link to changed fields; how causal traceability survives.
6. **Error, Failure, and Anti-Fragility** — which errors matter; when governed deviation becomes usable material rather than breakage.
7. **Tools, Evidence, and Numeric Authority** — when to request evidence rather than infer; the semantic–numeric boundary where meaning ends and deterministic computation must take over.
8. **Coupling, Assay, and Substrate Fit** — distinguishing parseability from real coupling; why different models inhabit the same schema with different fidelity.
9. **Maturation and Externalization** — moving governance from in-model form to deterministic enforcement without losing the distinctions that made it work.
10. **Multi-Agent and Institutional Form** — the minimal political form for multiple opaque generators sharing a world.
11. **Domain-Specific Success Criteria** — what success means in a given domain; which errors are tolerable; whether the metric is correctness, coherence, control, or emotional force.

### What the Agenda Develops Beyond the Decomposition

Two results in the agenda go past the cluster map and are worth surfacing here, because they are where the framework is sharpest:

- **Drift is thermalization.** Maintaining the proposal/commitment distinction is the continuous suppression of a mixing tendency — a Maxwell's-demon operation whose irreversible steps (commitment; per-cycle scratchpad wipe) carry a real, physically mandated entropy cost via Landauer's principle. The literal content is in the *necessity and operation class*, not the magnitude: **there is no free-lunch governance on any physical substrate.** Ungoverned drift is then not *like* thermalization — it *is* thermalization, and its signature is a measurable, directional **entropy-production rate** in committed state, composed entirely of individually lawful steps. This is a failure mode no per-cycle metric can see, and it is what the longitudinal half of the proposed metric suite is built to detect.
- **Epistemic typing is the tenth invariant's necessity proof.** Without typed claims, neither a per-cycle verification failure nor longitudinal drift can be *attributed* to the kind of claim that produced it — perception, inference, or speculation hardening into fact — and unattributable error cannot be corrected. Per-cycle unattributable fault and longitudinal unattributable drift are the same defect at two timescales, and epistemic-status typing is the single addition that makes error attributable at both. That is *why* typing is kernel rather than optional for any architecture with mixed-provenance durable state.

### The Player-Character Domain as High-Resolution Test Case

The paper uses the long-horizon player-character role as a motivating case — not the most serious application, the most *legible* one. At the table, weak mutation governance is immediately perceptible: omniscience breaks immersion, arbitrary self-rewrite breaks attachment, silent drift breaks dramatic consequence. The domain is also **anti-fragile** with respect to *governed* variance: a cortisol step one ordinal too high is not a bug, it is a character running on stress. That forgiveness, plus the continuous presence of a strong human verifier (the GM), is what makes narrative the ideal **Stage 1 discovery environment** — though the agenda is careful to note that the firewall holds per-cycle, while biased accumulation across the horizon is the deeper failure the entropy-production measurement exists to catch.

---

## OTTC and the Governance of Opaque Generative Systems

**[Full document: OTTC and the Governance of Opaque Generative Systems](OTTC%20and%20the%20Governance%20of%20Opaque%20Generative%20Systems.md)**

This top-level artifact is the philosophical and constitutional argument for *why* OTTC takes the shape it does. It is not a summary of the protocol; it is the argument behind it.

OTTC begins from a problem increasingly central to language-based systems: how should one regulate the consequences of an agent whose internal generative processes are only partially observable, yet whose outputs can alter durable shared state? This is not unique to machines. It arises wherever consequential action proceeds from an interior others cannot fully inspect — persons, committees, bureaucracies, courts, scientific communities all act from partially opaque interiors. The central claim: **governance should be located not at the inaccessible interior of the generator, but at the boundary where semantic generation becomes consequential state.** What requires regulation is the passage from proposal to commitment, from expressive possibility to durable mutation.

What is philosophically distinctive is that **continuity and governability do not require complete observability of the agent's internal manifold.** They emerge from lawful transitions among publicly intelligible states. Identity is secured not by stylistic consistency or apparent sincerity, but by invariants: stable referents, bounded transitions, explicit operations, accountable records, and verification that renders mutation legible over time. The statement resists two inadequate responses — **expressive romanticism** (treating fluency as integrity) and the **technocratic transparency ideal** (assuming governance requires exhaustive interior access). A governable system need not be perfectly transparent; it must be constrained at the point where interior generation becomes socially durable action. The companion **Layer Distinction** document develops the precise, vantage-relative form of this: the indistinguishability of interiors is constitutive *for the external observer* and resolvable *by the interior observer* (interpretability), which is why governance and interpretability **compose** rather than compete — and why deceptive alignment, the one case engineered to defeat the external vantage, is exactly where the interior vantage becomes necessary rather than optional.

---

## OTTC in Brief

### The 10 Rectangle Axioms

These are the mandatory kernel invariants. Axioms 1–9 make the mutation boundary **governable**. Axiom 10 makes a system that must reason across cycles **answerable to evidence** — it is kernel for any architecture with mixed-provenance durable state (i.e. any non-trivial long-horizon agent), and reduces to optional strengthening only in the degenerate single-provenance case.

1. **Canonical Address Space** — One canonical way to refer to any state element. No synonyms at the write surface.
2. **Propose-Commit Separation** — All mutation is expressed as proposals first; persistent state changes only at commit boundaries.
3. **Single-Writer Persistent State** — Exactly one authority writes persistent state per cycle.
4. **Explicit Update Operations** — State changes through a finite, named set of operations (SET, TRANSITION, ADD_MODIFIER, REMOVE_MODIFIER, CAP, VETO).
5. **Hard State vs. Soft Modifiers** — Durable baseline state is distinguished from transient overlays. Short-lived context does not rewrite identity.
6. **Step Limits and Override Triggers** — Hard-state changes are bounded per cycle. Breaking bounds requires explicit, named override triggers with proof.
7. **Deterministic Conflict Resolution** — When proposals conflict, resolution follows deterministic policy (precedence + tie-breakers).
8. **Audit Closure** — Every proposal accounted for exactly once (committed/suppressed/downgraded) with a reason. No silent drops.
9. **Post-Commit Verification** — After commit, a verification pass checks invariants and integrity. It certifies or flags — it never invents new changes.
10. **Epistemic-Status Typing** — Every commit-bound claim is typed by its footing in evidence (perception / inference / speculation / evidence-bound fact), kept distinct from provenance. This is what makes the governed cycle a **hypothesis machine** rather than merely a governed store, and it is the condition under which a verification failure becomes an *attributable, directional* prediction-error signal instead of an undiagnosable one.

These ten axioms define the **rectangle**. Any compliant implementation is a **square** — free to choose its own schemas, syntax, domains, and operations as long as the invariants hold. ChaOS is one square — narrative character governance. Legal systems, clinical protocols, scientific research pipelines, enterprise change management, and other consequence-bearing domains could each become their own square. Each requires **ontology translation**: the domain expert's vocabulary, state surfaces, evidentiary distinctions, and lawful transitions rendered into OTTC-legible form. Canonical addresses cannot exist before someone decides what is worth addressing; governance cannot regulate what has no address.

### Key Properties

- **Hypothesis Machine (kernel, not optional)** — Because every proposal carries an epistemic tag (Axiom 10), proposals encode hypotheses, commit records their lifecycle, verification tests their status, and audit closure prevents silent abandonment of falsifying evidence. The same governance pattern that makes state legible makes scientific claims legible — and it does so by *necessity*, not as a bonus feature, for any architecture with mixed-provenance state.
- **Qualification Assay doctrine** — Blind pre-build testing of model coupling *before* architecture decisions. Measure the ground before laying foundations. Different models couple differently to the same constitution; that is not a bug, it is a measurement.
- **Substrate physics** — Coupling is describable as **mass** (differential conditioning weight), **fields** and **perceived slopes** (substrate-relative gradients), and **anti-mass** (explicit prohibition that subtracts a prose temptation). The mass of a rendering is a property of the rendering *against a substrate's prior*, never of the rendering alone — which is why qualification must be empirical and why re-rendering for a new substrate is engineering correction, not aesthetic preference.
- **Semantic Abacus** — The model handles meaning at the write surface; numeric precision and cross-cycle comparison are externalized downstream. The model recognizes, interprets, and proposes; deterministic systems compute. This is also the natural home for the longitudinal entropy-production instrument.
- **Governed tool calls** — Tool actuation is proposed, not unilateral. The model proposes; governance commits or vetoes; the deterministic system executes; the model interprets the result and proposes again.
- **Maturity path** — In-model scaffold → hybrid → fully externalized deterministic governance. The architecture is designed to hand off as external infrastructure matures, with long-horizon assays (or, where available, interpretability) used to verify that a governance move is *deeply* binding before it is promoted to hard enforcement.
- **Federation** — Multiple squares interact through a canonical-dictionary interlingua, each sovereign in its own domain, with deterministic translation at the boundaries. The pattern's *mechanics* are validated daily by tabletop GMs under unified commit authority; its *sovereign-separation* dynamics — two genuinely distinct authorities who can disagree — await the first true two-authority build. The eventual payoff is **Hypothesis Machines**: multi-disciplinary instruments that hold several domains' constitutional structures at once.

---

## ChaOS: A Working Demonstration

ChaOS is one possible **square** inside the OTTC rectangle — a character state machine built for narrative and RPG use. It demonstrates that the framework is not abstract: it can be built, loaded, and run.

### Architecture

**70 files** organized into three layers plus supporting infrastructure:

| Layer | Prefix | Mutability | Purpose |
|---|---|---|---|
| Ontology | `SCHEME_` | Immutable | Field schemas, enums, ordinals, invariants. The constitution of what exists. |
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

The ontology draws on established frameworks: HEXACO, MMPI, Dark Triad, Adult Attachment Style (ASQ), Maslow's hierarchy of needs, HPA-axis stress modeling, predictive processing / active inference, and established memory encoding and decay principles. These are not decorative references; each domain defines discrete states with lawful transitions and specific update rules. They function as **narrative control surfaces**, not as empirical synthesis — ChaOS is by no means a scientific instrument, and that proper-use boundary is stated structurally inside the architecture itself.

### Anti-Fragile Narrative Property

Errors of *governed* state don't break ChaOS — they become narrative material. A governance-accepted cortisol spike that was "too high" is not a system failure; it is a character living with chronic stress. OTTC doesn't make the system correct or truthful. It makes it legible. In a narrative domain, legible errors are plot points. (Governance *violations* — direct writes, silent drops, untyped committed-fact claims — remain genuine failures regardless of domain.)

### DSL and Dual Readership

The internal DSL is designed for two simultaneous readers: human domain experts and LLM attention heads. Structural markers serve as attention anchors. Bracket-path canonical addressing (`[STATE_BODY][BIOCHEMICAL_STATE_MARKERS][CORTISOL]`) is maximally distinct from natural-language prose, reducing ambiguity at the write surface. Constitutional repetition — the write contract restated in every COT — keeps governance in local context rather than relying on long-range attention. **This particular surface form is the rendering that works well on most English semantic manifolds; it is a worked example of the dual-readership principle, not a universal mandate.** The form best suited to a different substrate or language is itself a matter for qualification.

### External Governance Composition

ChaOS is designed to hand off to deterministic external systems. Structured proposals are machine-parseable. The immutable/mutable file split supports external state ownership. The scratchpad lifecycle (instantiate → populate → commit → verify → wipe) is a transaction boundary. The verification checklist is implementable as a programmatic validator.

ChaOS is a **demonstration, not a production system.** It will degrade under context pressure. No in-model system survives indefinitely — probability always wins as context accumulates. The architecture is designed to compose with external governance when that happens.

---

## Who This Is For

Full renderings for each audience are in `AUDIENCE_RENDERINGS/`.

**ML/LLM Researchers** — Testable hypotheses about constitutional conditioning, with operationally defined metrics and ablation structure, including the invariant-deletion battery and the longitudinal entropy-production signature. OTTC makes falsifiable predictions about observable differences between governed and ungoverned architectures, and names what would refute its own central claims.

**Agent Framework Developers** — A protocol, not a framework. OTTC plugs into existing orchestration rather than replacing it. The result is agent state that is inspectable, testable, and auditable — with epistemic typing as a first-class field at the propose→commit seam, not a black box that might be doing something reasonable.

**Game Masters and Narrative Designers** — A system that gives LLM characters inertia, bounded perspective, and earned growth over long-form play. The character has a genuine history that constrains what it can plausibly do next. Continuity is structural, not just probabilistic.

**Enterprise Governance / Safety** — Change control and accountability for long-running agents, with audit trails that support compliance and incident review. When something goes wrong, the record shows what was proposed, what was committed, what verification found, and — through epistemic typing — on what evidential footing each claim stood, so failures can actually be attributed.

**Domain Experts in Any Consequence-Bearing Field** — If your domain has a vocabulary, durable state surfaces, evidentiary distinctions, and lawful transitions — medicine, law, scientific research, financial operations, clinical governance — you can build your own square. The precondition is translating your domain ontology into OTTC-legible form. OTTC provides the rectangle; you supply the constitutional knowledge that makes a particular square real. The audience renderings and the bridging document on producing a square are designed to scaffold that translation with LLM collaboration — and, notably, an individual practitioner can do this **now**, without waiting for institutional scaffolding, provided commit-authority discipline is maintained.

---

## What OTTC Is Not

Honest scope is what separates a framework from a promise.

- **Not a silver bullet** — OTTC systems can still fail, drift, and produce harmful outputs. Governance reduces frequency and improves detectability. It does not prevent.
- **Not determinism** — Text constraints shape probability; they do not create hard runtime guarantees. Deterministic behavior requires externalized enforcement. The in-model layer is always stochastic.
- **Not truth** — OTTC does not prevent hallucination. It aims to make violations detectable and auditable. A hallucination that lands in the audit record is at least visible.
- **Not model-independent** — Different models couple differently to the same constitution. Qualification is mandatory before architecture decisions. Assuming coupling is the most common mistake.
- **Not a replacement for software** — For high-stakes decisions, deterministic validators, policy gates, and external enforcement are required, not optional. The in-model layer is the proposal layer; the deterministic layer is where consequential action happens.
- **Not a substitute for oversight** — Audit artifacts can be performative unless cross-checked. OTTC creates the record. Humans and deterministic validators have to read it.
- **Not empirically settled** — The framework is internally consistent and its kernel is minimal against an explicit specification (predictive processing + Popperian falsification). Whether its strongest claims hold in running systems is a matter for the research program, not a result already in hand. The corpus names its own falsification conditions rather than assuming its conclusions.

---

## Repository Structure

```
The Mutation Boundary Problem - A Research Agenda for Stateful Opaque Generative Systems/
                             — 9-part research agenda naming and decomposing the Mutation
                               Boundary Problem; positions OTTC and ChaOS as provisional
                               constructive responses; defines 11 research clusters, the
                               thermodynamic structure of the boundary, and the forward
                               research program
OTTC and the Governance of Opaque Generative Systems.md
                             — Philosophical and constitutional foundation: why governance
                               belongs at the mutation boundary, why full observability is
                               not required, and why the pattern mirrors human institutional
                               form
OTTC/                        — Framework specification (axioms, scope, qualification, testable
                               hypotheses, maturation doctrine, build SOP, formal spec)
CHARACTER_OPERATING_SYSTEM/  — ChaOS demonstration architecture (70 files across ontology,
                               transition law, runtime state, and supporting infrastructure)
AUDIENCE_RENDERINGS/         — OTTC rendered for ML/LLM researchers, agent framework
                               developers, game masters and narrative designers, and
                               enterprise governance/safety
BRIDGING_DOCUMENTS/          — Substrate physics; producing a square; federated governance;
                               the future of domain expertise; interpretability/governance
                               layer distinction
LICENSE                      — CC BY-NC 4.0
```

---

## A Note on Voice and Format

The OTTC and audience-rendering documents were written for LLMs first. The models were the original teachers.

The rigid sections, repeated invariants, UPPER_SNAKE canonical paths, and ceremonial structure are not stylistic flourishes — they are deliberate DSL choices designed to be attention-head friendly, keeping the constitution stable across thousands of tokens and long collaborative sessions. **This is not the only DSL in which OTTC concepts can be communicated to LLMs; it appears to work well with most English semantic manifolds, and a different substrate or language may call for a different rendering.**

Humans are welcome to read along; the protocol works for any long-horizon agent. If the ritual tone feels unusual at first, drop the files into an LLM's persistent context and watch it parse the rectangle instantly — that is the point. By writing the documents in this native format, the LLMs themselves can actively assist human readers in understanding OTTC and building their own OTTC-compliant architectures.

The corpus is machine-readable **by design**, and that design is part of the contribution. Loaded into persistent LLM context, it functions as a **collaboration scaffold**: it lets LLMs help human domain experts understand OTTC, validate proposed square architectures against the rectangle invariants, propose canonical ontology surfaces, and identify gaps in lawful mutation coverage. Plural LLM proposals, human or domain-expert commit authority, disagreement as diagnostic signal, and constitutional discovery through disciplined collaboration are the same pattern the corpus describes. This is how the corpus was built and how it is designed to be used.

---

## License

[CC BY-NC 4.0](LICENSE) — Creative Commons Attribution-NonCommercial 4.0 International.

Free to share and adapt for non-commercial purposes, with attribution. If you build on this work commercially, reach out.

© 2025–2026 James J. Huff. All rights reserved for commercial use.

---

## Status and Contact

This is active work. The framework is stable; the demonstration architecture is functional; the external-governance integration layer is the current frontier, and the empirical program that would test OTTC's strongest claims is the open horizon.

I am open to licensing discussions, consulting, and collaboration where OTTC — or a custom square — can be applied to long-horizon agent systems. Questions, observations, and inquiries can be directed through GitHub: [@Mastenship](https://github.com/Mastenship).