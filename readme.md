# Capacity-Constrained Newsvendor RAG Tutor — Audited Symbol/Answer Version

Open `capacity_newsvendor_rag_tutor_audited.html` in a browser. No server or external libraries are required.

## What was corrected

This version audits the answer-routing and symbol glossary after the quick-button issue with **“What does λ mean?”**.

The main bug was an alias collision: the English word **mean** in the sentence “What does λ mean?” was being matched to **μ_i = mean demand** before the λ symbol was selected. The new version gives λ priority and uses a stricter symbol parser.

Additional corrections:

- Removed the generic alias `mean` from μ_i so it no longer hijacks “what does X mean?” questions.
- Removed the incorrect `f_i(q)` alias from `F_i(q)` so CDF and PDF questions are not confused.
- Separated **capital Phi** `Φ(z)` from **little phi** `φ(z)`.
- Removed z-score aliases from `Φ^{-1}(a)` so the inverse-CDF operator is not confused with the z-value itself.
- Regenerated all symbol-card text from the corrected glossary.
- Added audited Q&A examples for all symbols and units.
- Made the glossary popup use each symbol’s audited unit field.

## Training/RAG layer

- Student Q&A examples after audit: 12,772
- Explicit audited symbol Q&A examples added: 106
- Symbol entries: 39
- Concept cards: 124
- The tutor remains fully local and uses no remote APIs, CDNs, analytics, `fetch`, or `XMLHttpRequest` calls.

## Key formula logic retained

When the shared capacity constraint binds and each unit consumes one unit of capacity:

```text
MC_i(q_i*) = λ
F_i(q_i*) = (p_i - c_i - λ) / (p_i - s_i)
```

λ is the dollar value of one additional unit of shared capacity. It is not mean demand μ_i, not a service probability, and not a z-value.
