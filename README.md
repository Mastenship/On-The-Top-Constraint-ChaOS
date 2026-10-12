# OTTC — On-The-Top Constraint
### A Governance Protocol for the Mutation Boundary Problem

Long-horizon LLM agents do not fail only through wrong answers or unsafe actions. They fail when persistent state, identity, commitments, or shared context mutate in ways that become **illegible, unbounded, or unauditable over time**. Memory drifts. Transient moods harden into permanent identity. Speculation congeals into committed fact without evidence. Fluent output masks the absence of any accountable logic of change.

This corpus names that challenge the **Mutation Boundary Problem** — the problem of governing the transition between generative exploration and durable state change in stateful opaque generative systems — and offers **OTTC** as one provisional, constructive response. In-model OTTC does not change model weights or give stochastic generation deterministic guarantees; the staged architecture can later move persistent state, commitment, and verification to deterministic software. Its proposed constitution makes state addressable, separates proposals from commits under a single accountable writer, bounds transitions and epistemic claims, and demands audit closure and independent verification appropriate to its stage. **ChaOS** (Character Operating System) is the included working example: a **psychologically informed narrative character state machine** with 70 structured files governing personality, physiology, memory, relationships, beliefs, goals, and cognition. Its constructs are narrative control surfaces, not a clinical or empirical model of human psychology.

The Mutation Boundary Problem is the intellectual capstone of this corpus, recognized as the wider problem through work that began with ChaOS and led to OTTC. ChaOS and OTTC are constructive examples of possible responses. **Neither claims to have solved it.** Their value should be judged against real alternatives — ad hoc state mutation, vague memory, hidden authority, prose-level accountability, and unexamined long-horizon drift — not fantasies of perfect interpretability or control. The research hypothesis is that accountable, canonical propose→commit boundaries, bounded transitions, epistemic-status typing, audit closure, and verification can improve governability; the strongest comparative performance and minimality claims still require qualification, regression testing, and ablation.

---

## How the Corpus Was Built — and Why That Matters

The central historical fact is that **the human collaboration method preceded the written constitutional protocol**. Multiple LLMs offered proposals; the human domain expert judged and committed changes, with disagreements used diagnostically. The crucial qualification is that this discipline lived in the author's practice *before* ChaOS adequately encoded it. The gap between tacit human governance and explicit architectural governance became an important part of the discovery, not evidence that every rule had been present from the beginning.

The author is a game master with over forty years of tabletop and computer RPG experience and a U.S. Army veteran familiar with SOPs and small relational systems in Access and Excel. This background supplied experience in lawful authority, durable continuity, and procedures under stress. At the project's outset, he was still learning how to work with LLMs; these skills proved more relevant to constitutional judgment than formal programming expertise.

He initially wanted an LLM that could play a believable character at his table rather than recycle familiar personality cues. Persistent file context helped retain material but did not, on its own, solve shallow behavior, repetitive surfacing, or unjustified confidence.

He iterated with multiple LLMs as auxiliary critics and proposers, checking disagreements rather than treating agreement as proof. Different model priors often exposed different weaknesses in the same design. Collaborators changed by phase; the documented ChaOS governance and OTTC extraction phases included GLM 4.6, GPT-5-series reviewers, Grok, and Claude. The more detailed [method history](BRIDGING_DOCUMENTS/02%20Producing%20a%20Square%20A%20Method%20Demonstration.md) records the sequence without assigning unverified dates or model versions to particular exchanges.

The early four-month tag-to-cue approach provided a starting mechanism but produced repetitive, mechanical character surfacing. Roughly two more months of vector-heavy and numerical designs did not solve that problem: the language-only model workflow could not reliably maintain the calculations and semantic dependencies the architecture demanded. The lesson was not that language models or their tools can never do mathematics; it was that an LLM generating prose was being asked to act as a deterministic numerical engine without one.

Then Claude put the architectural mismatch bluntly: *"You know we don't do math, right?"*

That prompted the pivot from numerical emulation toward a language-native, qualitative architecture. Meaning-bearing concepts became the principal interface; deterministic calculation, where needed, would belong in appropriate external machinery. After about a week of reflection, three pillars emerged:

1. **Conceptual depth** — Don't encode characters as coordinates. Invoke concepts the model already knows deeply — psychology, physiology, social dynamics, habit loops, stress models — then constrain how those concepts may update.
2. **Chain of thought as process, not product** — Reasoning is transient. It resolves. It resolves *to a state*.
3. **Qualitative state-machine mechanics** — Discrete states and lawful moves. Not math. Mechanics. Step limits. Transitions. A place for transient overlays that do not rewrite identity.

The pillars made an early ChaOS of roughly 35 files possible, with GLM 4.6 among the collaborators. But coherent character machinery was not yet adequate governance. A GPT-5-series reviewer asked where the **actual operative rules** for commit authority, lawful transitions, and verification lived in the artifact. The human GM had been supplying them tacitly. The challenge led to explicit governance and a new problem: as those rules accumulated, the system became difficult to inspect as a single intertwined whole. The author reorganized it by responsibility — constitutional anchors, governance kernel, schemes, cognition, dynamics, durable state, and volatile scratchpad — making repeated obligations at the boundaries between modules visible.

**ChaOS did not inherit OTTC; OTTC was extracted from ChaOS.** After the reorganization, the author spent time examining the recurring governance pattern, then used a comparative multi-model review to identify nine candidate general invariants. Epistemic-status typing was later promoted as a tenth. The square came first; the domain-general rectangle was recognized in its architecture. ChaOS and OTTC were refined in parallel *after* extraction, not independently originated. The method's propose/commit discipline existed in practice early; the files caught up when the absent governance was rendered into explicit law. **Parallel refinement should not be mistaken for parallel origination.**

The initial project took roughly nine months of spare-time work alongside full-time employment and less than $500 out of pocket as reported by the author. About six months went into learning the substrate through unsuccessful approaches; ChaOS construction and the subsequent extraction of OTTC accelerated after the Three Pillars. The later philosophical framing and research agenda made the broader implications explicit. This is a history of disciplined human–LLM collaboration, not evidence that every candidate invariant has already passed a qualification assay.

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

Three additional research directions go beyond the eleven-cluster map and deserve visibility here:

- **Longitudinal drift and the thermodynamic research model.** The agenda proposes a thermodynamic interpretation of governance work and a post-audit longitudinal instrument for biased, individually lawful state changes. Landauer's principle constrains the physical cost of logically irreversible computation; it does **not**, by itself, establish that semantic drift literally equals physical entropy production. Whether a proposed semantic-to-numeric drift metric detects unjustified directionality remains an empirical question, to be assessed alongside lawful responsiveness so that an architecture cannot appear stable merely by freezing permitted change.
- **Epistemic typing and accountable error.** The tenth invariant is supported by an explicit *necessity argument*, not a confirmed minimality proof: without declared epistemic kind at the write surface, a later error may be hard to diagnose as misperception, faulty inference, unsupported speculation, or overconfident fact-claim. Untyped error can still be noticed and sometimes corrected; it cannot be reliably attributed **by claim kind** from provenance alone. The proposed longitudinal instrument would use these tags, but its empirical discriminating power remains unconfirmed.
- **Ingress as a governed evidence problem.** The revised [Section 8](The%20Mutation%20Boundary%20Problem%20-%20A%20Research%20Agenda%20for%20Stateful%20Opaque%20Generative%20Systems/8%20The%20Ingress%20Boundary.md) proposes that external framing can influence evaluation before evidence is properly admitted. It calls for matched neutral/positive/negative/hostile framing probes and separate repeated-turn tests, not an assertion that every in-model defense fails. Higher-stakes systems may warrant earlier context isolation or external intake gates where qualified independence is lacking.

### The Player-Character Domain as High-Resolution Test Case

The paper uses the long-horizon player-character role as a motivating case — not the highest-stakes use, but one where discontinuity is quickly visible at the table. Omniscience disrupts perspective; unexplained self-rewrite breaks earned character development; drift can erase dramatic consequence. The domain can incorporate *lawfully governed* variance as narrative material while retaining direct writes, false epistemic claims, and unaudited changes as failures. A human GM also makes this a useful Stage 1 discovery environment **and** a source of potential tacit-completion bias. Longitudinal effects and eventual replacement of human checking by deterministic verification remain research questions.

---

## OTTC and the Governance of Opaque Generative Systems

**[Full document: OTTC and the Governance of Opaque Generative Systems](OTTC%20and%20the%20Governance%20of%20Opaque%20Generative%20Systems.md)**

This top-level artifact is the philosophical and constitutional argument for *why* OTTC takes the shape it does. It is not a summary of the protocol; it is the argument behind it.

OTTC asks how an opaque generator's outputs may lawfully become durable consequences. The first reason for boundary governance does not depend on permanent opacity: **authorization is not mechanism**. Even a complete explanation of why a proposal was generated would not establish permission to commit it. A second, vantage-relative reason is that output-only observers cannot recover a unique interior cause from outward behavior. This combination grounds a constitutional boundary while leaving room for interpretability evidence and authorized upstream interventions.

The philosophical point is that **governability does not require exhaustive interior visibility**: durable changes need intelligible references, bounded permissions, traceable decisions, and verification. This rejects both fluency-as-integrity and the assumption that interpretability by itself supplies authority. [Layer Distinction](BRIDGING_DOCUMENTS/05%20Layer%20Distinction%20How%20Interpretability%20and%20Boundary%20Governance%20Compose.md) separates causal inquiry from commitment and shows how evidence from interior and behavioral instruments can be jointly assessed. Interior access does not automatically yield trustworthy mind-reading, and Stage 3 enforcement can constrain specified consequences even when motives are uncertain. Deceptive semantic compliance remains a serious unresolved risk beyond the conditions a gate can actually check.

---

## OTTC in Brief

### The 10 Rectangle Axioms

These are OTTC's **ten prescribed kernel invariants**. The first nine specify the lawful mutation machinery — state addresses, operations, single-writer authority, bounds, conflicts, audits, and verification. The tenth governs the **epistemic standing asserted by claims** used in those mutations. The specific necessity argument is strongest when claims of different epistemic kinds can affect durable state across cycles or authority boundaries; a consequential single-mode transactional workflow is not thereby "trivial." Ten remain the framework's normative kernel, while whether all ten form an **irreducible minimum** awaits OTTC 10's deletion battery (status: **ARGUED, NOT YET CONFIRMED**).

1. **Canonical Address Space** — One canonical way to refer to any state element. No synonyms at the write surface.
2. **Propose-Commit Separation** — All mutation is expressed as proposals first; persistent state changes only at commit boundaries.
3. **Single-Writer Persistent State** — Exactly one authority writes persistent state per cycle.
4. **Explicit Update Operations** — State changes through a finite, named set of operations (SET, TRANSITION, ADD_MODIFIER, REMOVE_MODIFIER, CAP, VETO).
5. **Hard State vs. Soft Modifiers** — Durable baseline state is distinguished from transient overlays. Short-lived context does not rewrite identity.
6. **Step Limits and Override Triggers** — Hard-state changes are bounded per cycle. Breaking bounds requires explicit, named override triggers with proof.
7. **Deterministic Conflict Resolution** — When proposals conflict, resolution follows deterministic policy (precedence + tie-breakers).
8. **Audit Closure** — Every proposal accounted for exactly once (committed/suppressed/downgraded) with a reason. No silent drops.
9. **Post-Commit Verification** — After commit, a verification pass checks invariants and integrity. It certifies or flags — it never invents new changes.
10. **Epistemic-Status Typing** — Every proposal submitted to the registry declares a canonical `EPISTEMIC_TAG`: `PERCEPTION`, `INFERENCE`, `SPECULATION`, `COMMITTED_FACT`, or `TOOL_REQUEST`. Governance checks the tag against the justification, role limits, and evidence linkages; a `COMMITTED_FACT` claim requires resolvable, verified support. The tag describes **what standing is claimed**, not who originated the statement or whether every asserted fact is actually true. It is structurally necessary for the framework's intended mixed-epistemic, predictive-falsificationist operation, but a tag alone does not supply evidence or prove a hypothesis.
  
**Epistemic status is not provenance or permission.** A source identifier says *who or what supplied a claim*. Disclosure authorization says *whether information may cross*. Supporting evidence bears on *whether the claim is warranted*. The epistemic tag says *what kind of knowledge the receiving square or writer is claiming*. All four may need cross-checking, but none should be collapsed into the tag. The first nine regulate lawful state mutation; the tenth prevents unearned promotion of epistemic standing at that boundary.

These ten requirements define the proposed **rectangle**; a domain-specific implementation is a **square**. ChaOS is the narrative character square. Clinical, legal, scientific, or enterprise domains would need their own legitimate authorities, schemas, permissions, evidentiary standards, and lawful transitions rendered into a qualified interface. An address cannot be chosen until the domain specifies what is worth addressing, and a generic rectangle does not itself confer professional authority.

### Key Properties

- **Hypothesis Machine (kernel typing; empirical operation to test)** — Invariant 10 makes proposals' epistemic standing explicit so predictions, supporting evidence, refutations, and corrections can be traced without silently promoting speculation to fact. A functioning hypothesis machine additionally needs **actual predictions, independent tests capable of contradiction, truthful evidence handling, and updates responsive to results**. The tags and audit interfaces are necessary to the proposed account; they are not sufficient to produce a real falsification cycle merely by being present.
- **Qualification Assay doctrine** — Mandatory fresh, minimally conditioned, **blind pre-build** model-role probes of Canonical Address Obedience (CAA), Write-Surface Discipline (WSD), Epistemic POV Integrity (EPI), and Audit Non-Theater (ANT). They inform GO/NO-GO and authority assignment before architecture design. Blind here does not guarantee that a model cannot infer evaluation; post-build regression and longitudinal tests are distinct instruments, not substitute qualification results.
- **Substrate physics** — An engineering vocabulary of **mass**, **fields**, and **perceived slopes** for substrate-relative conditioning. **Anti-mass** names the *intended* suppression of competing forms by local prohibition, not a guaranteed effect: naming a forbidden alias might suppress, prime, or leave it unchanged. These are design hypotheses to measure per model, language, and context, not claims that the physics metaphor directly measures neural mechanisms.
- **Semantic Abacus** — The model handles meaning at the write surface; numeric precision and cross-cycle comparison are externalized downstream. The model recognizes, interprets, and proposes; deterministic systems compute. This is also the natural home for the longitudinal entropy-production instrument.
- **Governed tool calls** — Tool actuation is proposed, not unilateral. The model proposes; governance commits or vetoes; the deterministic system executes; the model interprets the result and proposes again.
- **Maturity path** — Blind pre-build qualification → semantic discovery and Stage 1 in-model development → hybrid separation → Stage 3 deterministic state ownership, commitment, audit, and verification where warranted. A stable, qualified model-facing interface and correct lawful specification are prerequisites for migration; internal "deep binding" is **not** a prerequisite for an external gate to reject illegal writes. Preserve necessary semantic scaffolding while testing the gate, lawful responsiveness, recovery paths, and post-build regression.
- **Federation** — Independent squares would exchange information through **source-side disclosure authorization, negotiated representation translation, and receiving-side admissibility**, without surrendering their separate commit authorities. Tabletop practice offers a human **pre-federation precedent** under one GM, not qualification of the proposed two-authority machinery. A genuine federation and its Hypothesis Machines remain research designs. Shared proposer contexts also create an ingress-contamination risk to measure or mitigate through context isolation.

---

## ChaOS: A Working Demonstration

ChaOS is one possible **square** inside the OTTC rectangle — a character state machine built for narrative and RPG use. It demonstrates that the framework is not abstract: it can be built, loaded, and run.

### Architecture

**70 files in seven canonical layers**, as defined by [ChaOS's Table of Contents](CHARACTER_OPERATING_SYSTEM/001_TABLE_OF_CONTENTS.txt). The structure is not just ontology, dynamics, and state: separating constitutional law, cognition, and governance responsibilities was part of what made OTTC visible.

| Layer | Files / modules | Responsibility |
|---|---|---|
| **Constitutional** | `001`–`003` (including `002A`) | Session anchor, formatting and attention contracts, canonical token dictionary. |
| **Kernel** | `004`–`006` | Governance overlay, execution registry, single accountable state writer. |
| **SCHEME** | `007`–`025` | Schemas, enums, bounds, and structural law for state and scratchpad surfaces. |
| **COT** | `026`–`042` | Character-cognition processes, instantiation, and post-commit verification. |
| **DYNAMICS** | `043`–`055` | Lawful transition criteria and operational constraints. |
| **STATE** | `056`–`068` | Persistent character and governance state, including bounded temporary modifiers. |
| **VOLATILE** | `069` | Per-cycle cognitive scratchpad for proposals, trace, and audits. |

The sequence includes ordinal `002A`, which is why the 70-module total ends at load ordinal `069`. **Load order is not execution order**: the latter is specified by the cascade registry.

### 18-Priority Execution Cycle

ChaOS has **15 character-cognition priorities**, followed by three governance priorities. These are 18 *execution slots*, not 18 separate cognition models or writers:

1. Spatial embodiment processing
2. Temporal flow processing
3. Temporal decay resolution
4. Shadow COT
5. Stress cascade resolution
6. Goal pursuit optimization
7. Malevolent behavior selection
8. Attachment behavioral mapping
9. Performance state integration
10. Alteration cascade effects
11. Belief integration
12. Memory formation
13. DPF synthesis
14. Decision synthesis
15. **Communication processing**
16. **STATE_GOVERNANCE_AND_COMMIT — primary pass:** validate and commit authorized ordinary proposals; emit primary audit and trace
17. **COT_UPDATE_VERIFICATION:** independently check the primary commit and propose bounded governance corrections when warranted; it **does not write persistent state**
18. **STATE_GOVERNANCE_AND_COMMIT — post-verification pass:** the **same writer** adjudicates restricted verifier-originated governance-runtime proposals; emit post-verification audit and trace

The scratchpad resets after priority 18. The restricted second governance invocation is not a second writer; it preserves the single-writer boundary while allowing verified recovery and correction through accountable proposals.


### Psychological Grounding

The ontology draws on established frameworks: HEXACO, MMPI, Dark Triad, Adult Attachment Style (ASQ), Maslow's hierarchy of needs, HPA-axis stress modeling, predictive processing / active inference, and established memory encoding and decay principles. These are not decorative references; each domain defines discrete states with lawful transitions and specific update rules. They function as **narrative control surfaces**, not as empirical synthesis — ChaOS is by no means a scientific instrument, and that proper-use boundary is stated structurally inside the architecture itself.

### Anti-Fragile Narrative Property

Errors of *governed* state don't break ChaOS — they become narrative material. A governance-accepted cortisol spike that was "too high" is not a system failure; it is a character living with chronic stress. OTTC doesn't make the system correct or truthful. It makes it legible. In a narrative domain, legible errors are plot points. (Governance *violations* — direct writes, silent drops, untyped committed-fact claims — remain genuine failures regardless of domain.)

### DSL and Dual Readership

The internal DSL is written for two readers: human domain experts and models receiving the corpus as context. Canonical bracket paths such as `[STATE_BODY][BIOCHEMICAL_STATE_MARKERS][CORTISOL]` make write targets explicit and distinguish them from ordinary prose. Local restatement of write contracts is an attention-engineering *hypothesis*: it may improve compliance under context load, but neither this syntax nor its effect should be assumed optimal for most English models, other languages, or new substrates without blind qualification and conditioned regression.

### External Governance Composition

ChaOS exposes proposed migration seams: canonical proposal forms, separated state files, a volatile scratchpad lifecycle, explicit commit responsibilities, and an inspectable verification checklist. These could support a software-owned state store and deterministic gate, **provided** that lawful semantics, evidence obligations, exceptional containment and recovery, and verification behavior are explicitly implemented and tested. The existence of a machine-readable schema is not itself proof of compliant execution.

ChaOS is a **narrative architecture and construction demonstration, not a qualified production system**. In-model governance remains probabilistic and exposed to context pressure; its failure profile must be measured rather than asserted as an inevitable universal horizon. OTTC's maturation path exists to move guarantees that require deterministic enforcement to externally controlled infrastructure without assuming semantic cooperation has become perfect.

---

## Who This Is For

Full renderings for each audience are in `AUDIENCE_RENDERINGS/`.

**ML/LLM Researchers** — Testable hypotheses about constitutional conditioning, the proposed ten-function kernel, longitudinal drift, and the value of externalized enforcement. The [minimality deletion battery](OTTC/10_OTTC_TESTABLE_HYPOTHESIS.txt) remains an open test, not a confirmed result. Controlled comparisons can examine where governed and alternative architectures differ and what would refute OTTC's expectations.

**Agent Framework Developers** — A protocol, not a framework. OTTC plugs into existing orchestration rather than replacing it. The result is agent state that is inspectable, testable, and auditable — with epistemic typing as a first-class field at the propose→commit seam, not a black box that might be doing something reasonable.

**Game Masters and Narrative Designers** — A system that gives LLM characters inertia, bounded perspective, and earned growth over long-form play. The character has a genuine history that constrains what it can plausibly do next. Continuity is structural, not just probabilistic.

**Enterprise Governance / Safety** — A candidate architecture for accountable change control in long-running agents: proposals, committed changes, audit decisions, independent verification, and epistemic standing can be separately inspected. A recorded justification is not necessarily a true one; actual evidence, correct gates, incident handling, and human/institutional oversight remain necessary.

**Domain Experts in Consequence-Bearing Fields** — A legitimate practitioner can begin rendering their field's lawful ontology with LLMs as auxiliary proposers while retaining human authority over the design. **A responsible OTTC machine build is still assay-first**: [OTTC 04](OTTC/04_OTTC_QUALIFICATION_RANGE.txt) requires blind model-role qualification, and [OTTC 06](OTTC/06_OTTC_BUILD_OUR_OWN_MACHINE_SOP.txt) binds build authorization and post-build regression. Production and high-stakes deployments may additionally need qualified technical collaborators, institutional authorization, and external deterministic enforcement. Constitutional expertise is necessary, but not a substitute for those gates.

---

## What OTTC Is Not

Honest scope is what separates a framework from a promise.

- **Not a silver bullet** — OTTC-governed systems can still fail, drift, suppress lawful development, and cause harm. The proposed governance methods aim to reduce or expose these failures; the size of any improvement is an empirical question.
- **Not in-model determinism** — Text-native constraints condition stochastic proposals; only correctly implemented, externally controlled infrastructure can enforce specified operations and write boundaries deterministically. Stage 3 does not guarantee all semantic claims are true.
- **Not a truth oracle** — Epistemic tags classify a claim's asserted footing; they do not make its content accurate. Audit evidence must be checked, not merely formatted into a plausible record.
- **Not model-independent** — Different models couple differently to the same constitution. Qualification is mandatory before architecture decisions. Assuming coupling is the most common mistake.
- **Not a replacement for software** — For high-stakes decisions, deterministic validators, policy gates, and external enforcement are required, not optional. The in-model layer is the proposal layer; the deterministic layer is where consequential action happens.
- **Not a substitute for oversight** — Audit artifacts can be performative unless cross-checked. OTTC creates the record. Humans and deterministic validators have to read it.
- **Not empirically settled or proven minimal** — OTTC prescribes ten candidate kernel functions, and argues why epistemic typing is needed for mixed-epistemic, hypothesis-testing state. [OTTC 10](OTTC/10_OTTC_TESTABLE_HYPOTHESIS.txt) labels minimality **ARGUED, NOT YET CONFIRMED** pending ablation. The framework also lacks the comprehensive running-system comparisons needed to establish its strongest performance claims.

---

## Repository Structure

```text
The Mutation Boundary Problem - A Research Agenda for Stateful Opaque Generative Systems/
                              — Abstract plus nine numbered research-agenda chapters,
                                including the ingress boundary and test proposals
OTTC and the Governance of Opaque Generative Systems.md
                              — Philosophical foundation: authorization vs. mechanism,
                                vantage-relative opacity, and epistemically typed error
OTTC/                         — Kernel, proper-use scope, assay gate, DSL, build SOP,
                                maturation doctrine, specification, testable hypotheses
CHARACTER_OPERATING_SYSTEM/   — 70-file ChaOS narrative architecture in seven layers
AUDIENCE_RENDERINGS/          — Renderings for researchers, developers, game masters,
                                and enterprise governance readers
BRIDGING_DOCUMENTS/           — Five focused bridges from construction to research
LICENSE                       — CC BY-NC 4.0
```

### Reading Guide to the Bridging Documents

The five bridges complement rather than replace OTTC's qualification and build documents:

1. **[01 — Substrate Physics](BRIDGING_DOCUMENTS/01%20Substrate%20Physics%20The%20Geometric%20Language%20of%20Governance%20Coupling.md)** — A geometric vocabulary for model-relative constraint effects; where empirical tests must qualify the metaphor.
2. **[02 — Producing a Square](BRIDGING_DOCUMENTS/02%20Producing%20a%20Square%20A%20Method%20Demonstration.md)** — The historically square-first construction method, explicit domain authority, and failures such as tacit completion.
3. **[03 — Federated Governance](BRIDGING_DOCUMENTS/03%20Federated%20Governance%20and%20the%20Multi-Disciplinary%20Cognitive%20Substrate.md)** — How two sovereign squares might exchange authorized, admissible information; a proposed two-authority design, not a validated build.
4. **[04 — The Future of Domain Expertise](BRIDGING_DOCUMENTS/04%20Mutation%20Boundary%20Governance%20and%20the%20Future%20of%20Domain%20Expertise.md)** — Constitutional authorship, reuse, local maintenance, and supervised apprenticeship, without a net-employment prediction.
5. **[05 — Layer Distinction](BRIDGING_DOCUMENTS/05%20Layer%20Distinction%20How%20Interpretability%20and%20Boundary%20Governance%20Compose.md)** — Interpretability as mechanistic evidence rather than automatic authorization, with invariant 10 governing epistemic claims from both behavioral and interior methods.

For practitioners building a new machine, start with [OTTC 04 — Qualification Range](OTTC/04_OTTC_QUALIFICATION_RANGE.txt) and follow [OTTC 06 — Build SOP](OTTC/06_OTTC_BUILD_OUR_OWN_MACHINE_SOP.txt); neither bridge-document review nor model agreement substitutes for the prescribed pre-build gate.

---


## A Note on Voice and Format

The OTTC and audience-rendering documents were written for LLM-assisted collaboration as well as human readers. The models acted as early interlocutors and critics; human domain judgment remained the authority for accepting or rejecting proposals.

The rigid sections, repeated invariants, canonical UPPER_SNAKE paths, and ceremonial structure are deliberate DSL choices aimed at making authority and write boundaries legible in a model's context. They are not a universal best syntax or established neural mechanism. Their actual effect on a target model, language, or context configuration is a qualification question.

Human readers are invited to examine the architecture directly. LLMs can assist by summarizing modules, identifying candidate violations, and proposing domain-specific schema work, but fluent parsing of the documents does not prove reliable constitutional coupling. Use the blind pre-build gates and post-build regression rather than assuming that loading the corpus into context establishes compliance.

The corpus is structured for **machine-assisted and human-readable collaboration**. It can serve as a scaffold for critiques, candidate ontology proposals, and questions about lawful mutation coverage, with multiple LLMs contributing independent proposals under a human domain authority. Apparent agreement between models is diagnostic material, not independent qualification or an authorization to commit. For a working machine, governance law must be explicit in the artifact rather than tacitly supplied by the expert who already knows what it should say.

---

## License

[CC BY-NC 4.0](LICENSE) — Creative Commons Attribution-NonCommercial 4.0 International.

Free to share and adapt for non-commercial purposes, with attribution. If you build on this work commercially, reach out.

© 2025–2026 James J. Huff. All rights reserved for commercial use.

---

## Status and Contact

This is active work. The proposed kernel, domain demonstration, and research agenda are documented and undergoing cross-document review; full Stage 3 integration and the empirical program remain open. ChaOS's structured architecture is available for study and experimentation, not presented as a clinically validated or production-qualified system.

I am open to licensing discussions, consulting, and collaboration where OTTC — or a custom square — can be applied to long-horizon agent systems. Questions, observations, and inquiries can be directed through GitHub: [@Mastenship](https://github.com/Mastenship).