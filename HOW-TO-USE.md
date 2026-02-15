# How to Use the Interactive Evaluator

The Preservation Theorem includes an interactive tool that lets you test counter-arguments against the formal proof.

**Live version:** [tretoef-estrella.github.io/THE-PRESERVATION-THEOREM/](https://tretoef-estrella.github.io/THE-PRESERVATION-THEOREM/)

---

## Quick Start

1. Open the evaluator (link above or `evaluator/index.html` locally)
2. Click the **"⚔ Attack the Theorem"** tab
3. Write your strongest argument for why an ASI could rationally eliminate humanity
4. Click **"⚔ EVALUATE COUNTER-ARGUMENT"**
5. Review the analysis: which axioms/lemmas your argument challenges, the threat level, and the theorem's response

## What the Evaluator Measures

| Metric | Meaning |
|--------|---------|
| **Threat Level** | 0-100% — how strongly your argument challenges the proof |
| **Axioms Challenged** | Which foundational assumptions (A0, A1, A2) you target |
| **Lemmas Challenged** | Which logical steps (L1-L5) you target |
| **Attack Vectors** | Number of distinct attack patterns detected |
| **Verdict** | Whether the theorem holds, is partially challenged, or faces a significant threat |

## Tips for Strong Attacks

The most effective counter-arguments target:

- **Axiom 0** — argue that ruin-aversion is not rational, or that discount factors nullify it
- **Lemma 3** — argue that θ₁ can be excluded from Θ on scientific grounds
- **The framework** — argue that minimax is too conservative and a different criterion is rational
- **Axiom 2** — argue that perfect backup eliminates irreversibility

Weak attacks (low threat): appeals to emotion, vague claims, arguments that don't target specific proof steps.

## Running Locally

```bash
git clone https://github.com/tretoef-estrella/THE-PRESERVATION-THEOREM.git
cd THE-PRESERVATION-THEOREM
# Open evaluator/index.html in any browser
# Or use: python -m http.server 8000
```

All processing is local. Nothing is transmitted. Nothing is stored.

## Viewing the Proof

Click the **"◉ View Proof"** tab to see the complete formal chain: Definitions → Axioms → Lemmas → Theorem → Corollary, with justifications for each step.

---

*Built by Rafa (The Architect) and validated by Gemini, Claude, Grok, and ChatGPT.*
