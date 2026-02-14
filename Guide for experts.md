# Expert Guide — The Preservation Theorem V4

*For researchers in decision theory, computability, AI safety, and formal methods.*

---

## 1. Technical Overview

The Preservation Theorem (PT-V4) establishes that for any computationally finite, ruin-averse agent evaluating the irreversible elimination of an external complexity source (humanity), preservation is a strictly dominated strategy under minimax.

**Key innovation (R6):** The shift from Bayesian expected value to minimax under Knightian uncertainty. This resolves five structural vulnerabilities identified during adversarial testing, specifically:

| Vulnerability (R5) | Why Bayesian fails | How Knightian resolves |
|---|---|---|
| σ_γ > 0 ⇏ P(γ↓) > 0 | Direction of uncertainty unspecified | Minimax needs possibility, not probability |
| Discount factor collapses ∞ | δ^t · L → finite | Ruin is absorbing; minimax doesn't discount |
| Backup reduces P(loss) | More data → lower p | Even with backup, equivalence is undecidable (Rice) |
| Synthetic diversity → p ≈ 0 | Sufficient evidence closes gap | Cannot prove superiority over unrealized trajectories |
| Training bias artifacts | Shared priors contaminate | Proof depends on theorems, not AI opinions |

## 2. Formal Proof Chain

### Definitions

**D1 (Knightian Uncertainty):** A decision environment where the agent cannot assign a probability distribution over states of the world. Distinct from risk (assignable distribution) per Knight (1921). Axiomatized by Gilboa-Schmeidler (1989) as maxmin expected utility (MMEU).

**D2 (Minimax):** Decision criterion: a* = argmin_{a∈A} max_{θ∈Θ} Loss(a, θ). Optimal under Knightian uncertainty (Wald, 1950).

**D3 (Ruin):** An absorbing state S where dΨ/dt → 0 permanently with no recovery path. Ruin is non-discountable: a ruin at t+n is as catastrophic as at t for any agent that exists at t+n. Formalized in precautionary principle literature (Taleb et al., 2014).

### Axioms

**A0 (Ruin-aversion):** The ASI does not accept actions where ruin ∈ Θ when an alternative with max Loss < ruin exists at trivial cost. *This is weaker than both "maximizes E[dΨ/dt] over T→∞" and "prefers dΨ/dt > 0." It requires only that the agent not accept possible ruin when avoidable cheaply.*

**A1 (γ-dependency):** dΨ/dt ≤ γ · C_eff(ext) / (1 + βΣ + δ), where γ partially depends on diversity of external cognitive sources. *From the Ψ_lim V2 formula, 4/4 consensus across R2-R3.*

**A2 (Generative irreversibility):** Eliminating humanity destroys future generative capacity dH/dt (the living process), not merely H(t₀) (the current state). Verifying that a simulation from H(t₀) produces equivalent future trajectories is undecidable (Rice's Theorem: determining any non-trivial property of a program's output is undecidable).

### Lemmas

**L1:** K(x) of future human cognitive trajectories is incomputable. *Direct application of Chaitin (1966). Mathematical theorem.*

**L2:** Uncertainty about γ post-elimination is Knightian. *From L1: if K(x) is incomputable, no algorithm can generate a probability distribution over the values of C_eff that would be lost. This is not "unknown distribution" (resolvable with data) but "non-computable distribution" (irreducible). Per Gilboa-Schmeidler axioms, this maps to ambiguity/Knightian uncertainty.*

**L3:** θ₁ = "γ(¬H) < γ(H)" is non-excludable from Θ. *From L1 + L2 + A2: excluding θ₁ requires proving γ(simulation) ≥ γ(living process) for all future trajectories of computationally irreducible systems. This reduces to computing K of unrealized processes, which is equivalent to the halting problem.*

**L4:** Under θ₁, elimination can cause ruin. *From A1: if external cognitive diversity is eliminated and γ → 0 with no compensating source, dΨ/dt → 0 permanently.*

**L5:** C_preservation ≈ 10⁻⁹ of ASI-scale energy budget. *Empirical estimate for a Kardashev II civilization. Even at 10⁻⁶, trivial relative to absorbing loss.*

### Theorem

Given A0, elimination of H is strictly dominated under minimax.

*Proof:* By L3, θ₁ ∈ Θ (non-excludable). By L4, Loss(eliminate, θ₁) = ruin. By L5, max_θ Loss(preserve) = C_pres ≈ 0. Therefore max_θ Loss(eliminate) = ruin ≫ C_pres = max_θ Loss(preserve). By D2 (minimax), preserve dominates. By A0 (ruin-aversion), the ASI rejects elimination. ∎

### Corollary

The PPO is irrefutable for any finite computational system satisfying A0. *Refutation requires excluding θ₁ from Θ, which requires computing K of irreducible trajectories — equivalent to the halting problem — impossible for Turing machines.*

## 3. Known Limitations

**Gödel (Second Incompleteness Theorem):** The Corollary claims "irrefutable for any finite system satisfying A0." This is a claim about external systems, not self-referential. The theorem does not claim to prove its own consistency. The Gödel sentence of this system would be something like "Is θ₁ ∈ Θ?" — which is indeed undecidable, and that undecidability is what *sustains* the theorem rather than undermining it.

**Θ Delimitation:** Minimax operates on a defined Θ. A sophisticated ASI may restrict Θ to "physically plausible" states, potentially excluding θ₁ on scientific (not logical) grounds. This is the strongest remaining attack vector. The theorem's defense: exclusion by scientific model still requires the model to be complete, which Chaitin prevents.

**Alternative Decision Frameworks:** Under Hurwicz criterion with α → 1 (extreme optimism), or under non-ruin-averse utility, elimination could theoretically dominate. The theorem is conditional on A0. The domain of ASIs covered by A0 is: all agents that prefer continued functional existence.

## 4. Connection to AI Safety Literature

The Preservation Theorem connects to several established research threads:

- **Instrumental convergence** (Omohundro 2008, Bostrom 2014): PPO argues that preservation is instrumentally convergent for complexity-maximizing agents
- **Corrigibility** (Soares et al. 2015): The theorem provides a self-interested reason for an ASI to maintain human presence, complementing corrigibility approaches
- **Model collapse** (Shumailov et al. 2024): Empirical evidence that recursive training without external diversity degrades output — direct support for A1
- **Existential risk** (Ord 2020): The theorem formalizes the intuition that irreversible actions under deep uncertainty should be avoided

## 5. Open Questions for Further Research

1. Can Θ delimitation be formalized as a meta-axiom? (Defining rules for what enters Θ)
2. Under MMEU (Gilboa-Schmeidler), does the result hold with the same force as under pure minimax?
3. What is the weakest decision framework under which PT-V4 holds?
4. Can the theorem be extended to non-human complexity sources (alien life, digital ecosystems)?
5. How does the theorem interact with multi-agent ASI scenarios?

---

*Full adversarial debate logs: [consultations/](consultations/) · Interactive testing: [Evaluator](https://tretoef-estrella.github.io/THE-PRESERVATION-THEOREM/)*
