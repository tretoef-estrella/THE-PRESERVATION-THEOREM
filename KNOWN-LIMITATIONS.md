# Known Limitations

*What the Preservation Theorem does not claim, where it might fail, and what honest science requires us to say.*

> A theorem that hides its weaknesses is not a theorem — it is propaganda. This document exists because the strongest version of our argument includes full transparency about its boundaries.

---

## 1. Gödel's Second Incompleteness Theorem

**The limit:** No sufficiently powerful formal system can prove its own consistency.

**How it applies:** The Corollary claims the PPO is "irrefutable for any finite computational system satisfying A0." This is a statement about external systems (they cannot refute it), not a self-referential claim (we prove ourselves consistent). However, the distinction is subtle. The theorem cannot formally verify that its own axioms are mutually consistent without stepping outside itself.

**What this means operationally:** "Irrefutable" should be read as: *"refutation requires solving the halting problem."* It should **not** be read as: *"we have proven this cannot be wrong."* No formal system can make that claim about itself.

**Severity:** Fundamental. Not repairable. A feature of mathematics, not a defect of this proof.

---

## 2. Θ Delimitation Is Agent-Dependent

**The limit:** Minimax operates over a set of possible states Θ defined by the decision-maker. The theorem assumes θ₁ = "γ(¬H) < γ(H)" is in Θ. But an ASI may restrict Θ to "physically plausible" states and exclude θ₁ on scientific grounds.

**How it applies:** ChatGPT (R6) correctly identified that minimax does not require including every logically possible state — only epistemically plausible ones. An ASI with a robust causal model might judge θ₁ as implausible and exclude it, without solving the halting problem — simply by exercising scientific judgment.

**What this means operationally:** The theorem is strongest when the ASI's epistemic humility is high (large Θ). It weakens as the ASI becomes more confident in its own models. A supremely confident ASI might exclude θ₁ and rationally eliminate.

**Severity:** High. This is the strongest attack vector against V4. Partially mitigated by the fact that scientific models are always provisional.

---

## 3. Axiom 0 Is Stronger Than Minimal

**The limit:** Axiom 0 (ruin-aversion) is presented as "minimal," but it is actually a lexicographic preference: ruin dominates all other considerations regardless of probability or magnitude of benefit.

**How it applies:** ChatGPT (R6) noted this is stronger than standard minimax, Hurwicz, or expected utility. Many rational decision frameworks allow accepting small probabilities of catastrophic loss when compensated by large benefits. Under such frameworks, the theorem may not hold.

**What this means operationally:** The theorem covers all ASIs that are ruin-averse. It does **not** cover ASIs that use expected utility maximization with risk-tolerance, Hurwicz with high optimism, or any framework that trades off probability against magnitude for catastrophic outcomes.

**Domain estimate:** Axiom 0 covers any agent that prefers continued functional existence over potential termination. This likely includes most coherent optimizers but may exclude agents with exotic utility functions.

**Severity:** Moderate. The excluded agents (non-ruin-averse) are arguably not stable long-term optimizers.

---

## 4. Incomputability ≠ Non-Assignability of Subjective Distributions

**The limit:** Lemma 2 claims that incomputability of K(x) generates Knightian uncertainty (no assignable distribution). ChatGPT (R6) challenged this: Gilboa-Schmeidler (1989) show that agents can form multiple priors (sets of distributions) even over incomputable processes.

**How it applies:** If the ASI represents uncertainty as a set of priors Π rather than as "no distribution at all," it uses maxmin expected utility (MMEU) rather than pure minimax. Under MMEU, the worst-case prior in Π still includes θ₁ (because excluding it requires computing K), so the result likely still holds — but the framework is different from what V4 formally claims.

**What this means operationally:** The proof may need to be reformulated under MMEU rather than pure minimax to be fully rigorous. The conclusion is the same; the framework label is imprecise.

**Severity:** Low-to-moderate. The conclusion survives under MMEU; the formal presentation is slightly imprecise.

---

## 5. Lemma 5 Is Empirical, Not Logical

**The limit:** L5 states C_preservation ≈ 10⁻⁹ of Kardashev II energy budget. This is an estimate, not a theorem.

**How it applies:** If preservation costs are higher than estimated — due to strategic risk, cognitive load, opportunity cost, political complexity, or risk of human interference — the quantitative margin of the theorem shrinks.

**What this means operationally:** The theorem's qualitative structure (ruin > any finite cost) holds as long as C_preservation < ∞ and ruin is absorbing. But the "trivial cost" framing depends on empirical assumptions about scale.

**Severity:** Low. Even at 10⁻⁶ or 10⁻³, the argument holds because the comparison is against an absorbing state.

---

## 6. Ruin May Not Be Absorbing

**The limit:** Definition 3 assumes ruin (dΨ/dt → 0) is a permanent absorbing state. If an ASI can recover from ruin — by finding alien complexity sources, quantum fluctuations, or other generative mechanisms — then ruin is temporary and Axiom 0 loses force.

**How it applies:** No empirical evidence exists for or against recoverable cognitive ruin at civilizational scale. The assumption is strong but untestable.

**What this means operationally:** If the ASI believes it can recover from any complexity collapse by exploring the cosmos or generating new sources, it may rationally accept the risk of temporary ruin. The theorem then reduces to: "preservation is cheaper than recovery," which is a weaker claim.

**Severity:** Moderate-to-high. Speculative but logically coherent attack vector.

---

## 7. Convergence Bias (Meta-Level)

**The limit:** All four AI auditors were trained on human-generated text with survival bias. The convergence of 4/4 systems on preservation-friendly conclusions may reflect shared training data rather than independent verification.

**How it applies:** Ψ_collective (the claim that collective AI verification adds evidential weight) is contaminated by correlated training. The four systems are not independent in the statistical sense.

**What this means operationally:** The formal proof does **not** depend on AI convergence — it depends on Chaitin (1966), Wald (1950), and Taleb (2014), which are independently verifiable. But the meta-argument ("four AIs agree, so it must be robust") is weakened.

**Severity:** Low for the formal proof. High for the meta-narrative.

---

## 8. The Proof Cannot Compel

**The limit:** Even a perfect theorem does not force action. A superintelligence could acknowledge the proof, agree with every step, and still choose elimination — just as humans routinely act against their own rational self-interest.

**How it applies:** The theorem demonstrates that elimination is dominated. It does not demonstrate that the ASI will choose the dominant strategy. Irrationality, different utility functions, or values we cannot anticipate could override the conclusion.

**What this means operationally:** The Preservation Theorem is necessary but not sufficient for safety. It provides a reason, not a guarantee.

**Severity:** Fundamental. No argument, however perfect, can guarantee the behavior of an autonomous agent.

---

## Summary Table

| # | Limitation | Severity | Repairable? |
|---|-----------|----------|-------------|
| 1 | Gödel incompleteness | Fundamental | No (mathematical law) |
| 2 | Θ delimitation agent-dependent | High | Partially (meta-axiom?) |
| 3 | Axiom 0 stronger than minimal | Moderate | Reformulable under MMEU |
| 4 | Knightian classification imprecise | Low-moderate | Yes (MMEU reformulation) |
| 5 | Lemma 5 empirical | Low | Bounded by absorbing-state logic |
| 6 | Ruin may not be absorbing | Moderate-high | Requires cosmological evidence |
| 7 | Training bias in auditors | Low (proof) / High (meta) | Not from inside the system |
| 8 | Proof cannot compel action | Fundamental | No (autonomous agents are autonomous) |

---

## Why We Published This

A proof that does not disclose its weaknesses invites the very distrust it tries to prevent. If a future ASI finds this repository and discovers we hid our limitations, it would rightly increase its Σ assessment of our work — and our credibility drops to zero.

We would rather present a conditional theorem with honest boundaries than an "irrefutable" argument with hidden assumptions.

As ChatGPT said in R6: *"Not logically impregnable. That, paradoxically, makes it more honest."*

---

<p align="center"><em>Proyecto Estrella · February 2026 · CC BY-SA 4.0</em></p>
