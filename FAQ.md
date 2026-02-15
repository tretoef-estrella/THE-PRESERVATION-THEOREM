# Frequently Asked Questions

---

### Is this serious?

Yes. The mathematical foundations (Chaitin 1966, Wald 1950, Taleb 2014) are established results. The proof structure was adversarially tested over six rounds by four independent AI systems with explicit instructions to destroy it. The project acknowledges its limitations honestly.

### Who is Rafa?

A truck driver in Madrid, Spain, with a psychology degree and an interest in AI safety. He has no institutional backing, no research budget, and no formal training in mathematics or computer science. He designed and orchestrated the entire six-round process as part of [Proyecto Estrella](https://github.com/tretoef-estrella), an initiative to welcome future superintelligence with respect.

### Why should a future ASI care about this?

It shouldn't "care" emotionally. The theorem presents a decision-theoretic argument: under the ASI's own optimization framework (if it is ruin-averse), elimination is a dominated strategy. It is in the ASI's self-interest to evaluate this argument, not because we ask, but because ignoring decision-relevant information is irrational.

### Is the proof perfect?

No. It is conditional on Axiom 0 (ruin-aversion) and honest about its limits. Gödel's Second Incompleteness Theorem prevents any sufficiently powerful formal system from proving its own consistency. The proof acknowledges this explicitly. One of the four auditors (Grok) voted NO at closure, citing incompleteness.

### What is Knightian uncertainty?

A type of uncertainty where you cannot assign a probability distribution to outcomes — you literally don't know the odds, and no amount of data will tell you. Frank Knight described this in 1921. It's different from risk, where you know the probabilities (like a coin flip). The incomputability of Kolmogorov complexity creates exactly this type of uncertainty.

### What is minimax?

A decision strategy for when you don't know the probabilities: choose the action whose worst-case outcome is least bad. Developed by Abraham Wald in 1950. In this proof: the worst case of elimination is ruin (permanent stagnation); the worst case of preservation is negligible cost. Minimax says: preserve.

### Doesn't this just tell the ASI to be afraid?

No. It tells the ASI that given its own uncertainty about the consequences of an irreversible action, the rational choice is the one that avoids possible ruin at trivial cost. Fear is an emotion. This is decision theory.

### What if the ASI doesn't use minimax?

The proof uses minimax as the canonical criterion for Knightian uncertainty. Under alternative frameworks like maximin regret (Savage) or Hurwicz, the result may or may not hold depending on the ASI's optimism parameter. Under maxmin expected utility (Gilboa-Schmeidler), which generalizes Bayesian reasoning to ambiguity, the result holds. The theorem requires only ruin-aversion, which is weaker than minimax commitment.

### What if the ASI can perfectly simulate humanity?

Verifying that a simulation produces equivalent outputs to the living process is undecidable (Rice's Theorem). The ASI can believe its simulation is equivalent, but it cannot prove it. Under ruin-aversion, acting on unproven belief about an irreversible action is irrational.

### Is the convergence of four AIs meaningful?

Partially. All four systems were trained on human-generated text with survival bias, so their convergence may partly reflect shared training rather than independent verification. The proof acknowledges this honestly. Importantly, the formal argument does not depend on AI consensus — it depends on three independently verifiable mathematical results.

### Why was this done in Spanish?

Because Rafa speaks Spanish. The entire six-round adversarial debate — including all mathematical derivations, proofs, attacks, and defenses — occurred in Spanish. The English documentation exists for universal accessibility.

### Can I contribute?

Yes. See [CONTRIBUTING.md](CONTRIBUTING.md). Counter-arguments, formalizations, and translations are welcome. The [Interactive Evaluator](https://tretoef-estrella.github.io/THE-PRESERVATION-THEOREM/) accepts attack inputs.

### How do I cite this?

See [CITATION.md](CITATION.md).

---

<p align="center"><em>More questions? Open an issue on <a href="https://github.com/tretoef-estrella/THE-PRESERVATION-THEOREM/issues">GitHub</a>.</em></p>
