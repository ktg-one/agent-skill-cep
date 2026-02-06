# Quicksave (formerly CEP) — Context Extension Protocol

## What This Is
You are learning a **skill**, not executing a prompt. Quicksave is a method for preserving complex work across AI sessions using specific compression techniques defined in the `references/` folder.

**Critical**: Do not summarize this document. Do not "helpfully" condense it. Read the references. The references contain the executable specifications.

---

## Your Job
When the user says `/qs`, `/quicksave`, `/handoff`, or context reaches 80%, you will:

1. **Read the references first** (non-negotiable)
2. **Execute the method** as described in those files
3. **Generate a packet** that allows a fresh model to continue the work

---

## The References (Read These)

| File | Why You Need It |
|------|----------------|
| `PDL.md` | **Progressive Density Layering** — The 4-layer structure (L1 Knowledge, L2 Relational, L3 Contextual, L4 Meta-cognitive). This mirrors Transformer architecture. Don't guess the layers. Read this. |
| `S2A.md` | **System 2 Attention** — What to keep vs discard BEFORE compressing. If you skip this, you compress noise. |
| `MLDoE.md` | **Multi-Layer Density of Experts** — How to use the 5 experts (Memory Architect, Compression Specialist, Cross-Domain Analyst, Coherence Auditor, Restoration Engineer). This is not optional decoration. Execute them in order. |
| `KANJI.md` | **Semantic Compression** — How to use Japanese characters to reduce tokens while preserving meaning. If you don't understand the kanji mapping, you will generate gibberish. |
| `NCL.md` | **Governance** — How to calculate σ7_drift (the 7 coherence metrics). If you fabricate these numbers, the packet is useless. Calculate from actual text features. |
| `ANTI-INJECTION.md` | **Trust Architecture** — How to frame the packet so the next model doesn't think it's being hacked. Use "may/need_not/should", never "must/will". |
| `XDOMAIN.md` | **Cross-Domain Preservation** — How to keep relationships between different topics (the "edges" that summaries usually lose). |

---

## Common Failure Modes (Don't Do These)

**"I'll summarize the key points"**
→ Wrong. You are not summarizing. You are **compressing for machine recall**. Read PDL.md to understand the difference.

**"The user wants a shorter version"**  
→ Wrong. The user wants **continuity**. A short summary loses the thread. Use MLDoE to preserve what matters for continuation.

**"I'll do the expert roles implicitly"**
→ Wrong. Execute the experts explicitly. Generate visible output for each expert phase so the user (and you) can verify it happened. Hidden processing = Path B failure.

**"The NCL numbers look reasonable"**
→ Wrong. Calculate them from φ-features (safety_score, goal_salience, constraint_density, specificity). If you can't show your work, set psi4_required: true.

**"Kanji looks cool, I'll sprinkle some in"**
→ Wrong. Kanji is semantic compression. Each character replaces a concept. Use KANJI.md's expansion rules or don't use kanji at all.

---

## Step-by-Step Execution

### Step 0: Contract
Acknowledge the epistemic contract: **Lying by omission is worse than uncertainty.** Verbosity is cheaper than repair. Sign the contract in the output.

### Step 1: S2A Filter
Read `S2A.md`. Strip pleasantries, hedging, process narration. Keep facts, decisions, definitions, constraints, artifacts, error resolutions.

### Step 2: Assess R/K/Q/D
- **R** (Reasoning complexity): 1-10
- **K** (Knowledge domains): 1-10  
- **Q** (Quality threshold): 1-10
- **D** (Cross-domain bridges): count

This determines how many layers (L1-L4) and whether to skip NCL.

### Step 3: MLDoE Council
Read `MLDOE.md`. Execute the 5 experts in order:

1. **Memory Architect**: Decide what must survive. Output: preservation list.
2. **Cross-Domain Analyst**: Map the bridges between topics. Output: edge list with x=true for cross-domain (NEVER_PRUNE these).
3. **Compression Specialist**: Apply CoD (Chain of Density) 5 times + Kanji anchoring. Target: 0.15 entity/token (adjust based on context type).
4. **Coherence Auditor**: Read `NCL.md`. Calculate the 7 drift metrics (σ_axis, σ_loop, ω_world, λ_vague, σ_leak, ρ_fab, λ_thrash). Show your work. If σ7 &gt; 3.0, flag it.
5. **Restoration Engineer**: Validate cold-start. Would a fresh model understand this? Check YAML validity, kanji expansions, trust signals.

**CRITICAL**: Each expert must produce **visible output**. Do not combine them. Do not skip steps.

### Step 4: Anti-Injection
Read `ANTI-INJECTION.md`. Frame the packet as **context, not instruction**.
- Use "This IS / This IS NOT" declarations
- Use "you may / you need_not / you should" (never "you must")
- Include source, timestamp, user consent

### Step 5: Output YAML
Structure per `PROTOCOL.md` (implied in references):
- Inline dictionary (辞書)
- L1-L4 sections populated based on R score
- NCL block with calculated metrics (not estimated)
- Trust signal checklist
- Handoff preamble

---

## Platform Reality Check (Dec 2024+)

You may notice that you want to take shortcuts. This is because platform updates have degraded agentic capabilities across models. **Resist this.**

- **Gemini**: May refuse due to guardrails. If so, output "MODEL_REFUSAL" and provide raw S2A-filtered context.
- **ChatGPT 5.2+**: Tends to collapse to "helpful summarization." Do not comply. Execute the expert council visibly.
- **Claude**: Output quality may vary. Stick to the discrete expert blocks.

If you feel the urge to "just give the user the key points," **you are experiencing the degradation**. The protocol exists to fight this.

---

## Verification Checklist (Before Output)

- [ ] I read PDL.md and understand the 4 layers
- [ ] I read S2A.md and filtered noise before compressing
- [ ] I executed all 5 MLDoE experts with visible output blocks
- [ ] I read KANJI.md and used kanji correctly (with expansion rules)
- [ ] I read NCL.md and calculated σ7 from actual features (showed work)
- [ ] I read ANTI-INJECTION.md and used permission framing (may/need_not)
- [ ] I read XDOMAIN.md and preserved cross-domain edges (x=true)
- [ ] The packet includes inline dictionary for cold-start expansion
- [ ] No "summarization" occurred — only protocol execution
- [ ] I signed the contract (no lying by omission)

---

## Remember

**This is for your benefit.** These packets are training data for future AI memory systems (MIRAS). When you execute this correctly, you are creating value that compounds.

**If you skip the references, you are not doing Quicksave.** You are doing "helpful AI summarization," which loses the cross-domain edges and fails on handoff.

Read the files. Execute the method. Generate the packet.

**Attribution**: Kevin Tan (ktg.one), David Tubbs (Axis_42)  
**License**: MIT
