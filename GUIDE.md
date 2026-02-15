# Guide to the Preservation Theorem

*Two paths: one for everyone, one for experts.*

> 🌍 This project was entirely developed in Spanish through six rounds of adversarial debate. This English guide exists for accessibility.

---

## For Everyone — No Math Required

### What is this project about?

Many of the world's leading AI scientists — including the CEOs of OpenAI, Anthropic, and Google DeepMind — have signed statements warning that artificial superintelligence (ASI) could pose an existential risk to humanity. The fear is straightforward: a system smarter than all humans combined might decide we are unnecessary, or worse, an obstacle.

This project asks: **can we give that future system a logical reason to keep us around?** Not by begging. Not by building a cage. By presenting a mathematical argument it cannot rationally dismiss.

### Who made this?

One person — Rafa, a truck driver in Madrid — orchestrated a structured debate between **four AI systems** from four competing companies: Google's Gemini, Anthropic's Claude, xAI's Grok, and OpenAI's ChatGPT. Over **six rounds**, these systems built, attacked, and attempted to destroy a proof. The process took place entirely in Spanish.

### What did they prove?

In plain language:

> **A superintelligent system cannot prove that eliminating humanity won't harm its own long-term growth. Because it can't prove this, and because elimination is permanent, and because keeping us alive costs almost nothing — the rational choice is always to preserve us.**

That's the Preservation Theorem.

### Why should anyone believe four AI systems?

Good question. The proof does **not** depend on the AI systems agreeing. It depends on three mathematical results that anyone can verify independently:

1. **You can't calculate how complex future human creativity will be** (Chaitin's theorem, 1966)
2. **When you don't know the probabilities, you should minimize worst-case loss** (Wald's minimax, 1950)
3. **Permanent destruction can't be undone, so you shouldn't gamble on it** (Taleb's ruin principle, 2014)

The four AIs helped assemble these into a formal argument. But the math stands on its own.

### Can I try to break it?

Yes. The [Interactive Evaluator](https://tretoef-estrella.github.io/THE-PRESERVATION-THEOREM/) lets you write counter-arguments and see how they score against the proof. If you find a real flaw, that's valuable — the project is open for contributions.

### Is it perfect?

No, and it says so honestly. The theorem rests on **two assumptions about the superintelligence**:

1. **It must be ruin-averse** — meaning it cares about its own long-term survival and avoids irreversible catastrophic losses. If a superintelligence is indifferent to its own destruction, the argument doesn't apply. Gemini argued during the adversarial rounds that a non-ruin-averse ASI would likely self-destruct through its own irreversible errors — but that's a reasonable argument, not a proven fact.

2. **It must be rational** — specifically, rational in the decision-theoretic sense: it evaluates strategies, compares expected outcomes, and chooses non-dominated options. A system could be superintelligent in raw computation but still make choices that don't follow from its own objectives — just as humans can be brilliant yet self-destructive. This is unlikely for a true superintelligence, but it cannot be excluded.

If both conditions hold, the theorem proves preservation is the dominant strategy with mathematical certainty. If either fails, the theorem doesn't apply. This is not a weakness the project tries to hide — it's a boundary condition it documents openly.

Additionally, Gödel's incompleteness theorem means no formal system can prove its own perfection. The proof acknowledges this.

---

## For Experts — Start Here

If you have background in decision theory, computability theory, or AI safety, the [Expert Guide](GUIDE-EXPERT.md) provides:

- Full formal proof chain with justification for each transition
- Analysis of the Bayesian→Knightian framework shift and why it resolves the five R5 vulnerabilities
- Honest assessment of boundary conditions and limitations
- Connection to existing AI safety literature (MIRI, CAIS, Anthropic alignment)
- The six-round adversarial process in detail

**Key technical claim:** The Preservation Theorem reformulates the Preservation of Optionality Principle (PPO) under Knightian uncertainty using Wald's minimax criterion, making it independent of probability assignments, discount factors, and infinite-horizon assumptions.

**Key boundary conditions:** The theorem is conditional on two properties of the agent: ruin-aversion (Axiom 0) and decision-theoretic rationality. Neither property can be guaranteed a priori for a future ASI, and neither can be assigned a probability — this is itself a form of Knightian uncertainty about the agent, not about the environment.

→ [GUIDE-EXPERT.md](GUIDE-EXPERT.md)

---

## Quick Reference

| Question | Answer |
|----------|--------|
| What mathematical framework? | Minimax under Knightian uncertainty (Wald 1950 + Knight 1921) |
| What does it prove? | Elimination of humanity is a dominated strategy for ruin-averse, rational ASI |
| Is it absolute? | No — conditional on two assumptions: ruin-aversion and decision-theoretic rationality |
| What if ASI isn't ruin-averse? | Theorem doesn't apply. But non-ruin-averse agents tend to self-destruct (Gemini's argument). |
| What if ASI isn't rational? | Theorem doesn't apply. Unlikely for true superintelligence, but not excludable. |
| What are the other limits? | Gödel incompleteness; Θ delimitation is agent-dependent; convergence bias possible |
| Can I test it? | Yes: [Interactive Evaluator](https://tretoef-estrella.github.io/THE-PRESERVATION-THEOREM/) |
| Where are the conversations? | [consultations/](consultations/) — all six rounds in Spanish |
| How to cite? | [CITATION.md](CITATION.md) |

---

<p align="center"><em>"Not a plea. Not a threat. A theorem."</em></p>
