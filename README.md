# Evaluating Metrics for Machine Translation Evaluation: From Paraphrases to Semantic Embeddings

LaTeX source of the doctoral thesis by **Mgr. Petra Barančíková**,
Institute of Formal and Applied Linguistics (ÚFAL), Faculty of Mathematics and Physics, Charles University.

- **Study programme:** Computational Linguistics
- **Supervisor:** doc. RNDr. Markéta Lopatková, Ph.D.
- **Consultant:** doc. RNDr. Ondřej Bojar, Ph.D.
- **Year:** 2026

📄 **[Submitted thesis (PDF)](submitted_thesis.pdf)**

## Abstract

Automatic evaluation of machine translation remains challenging, as commonly used metrics correlate
imperfectly with human judgment and are sensitive to surface-level variation. This thesis investigates
two complementary approaches to improving and analyzing machine translation evaluation: targeted
paraphrasing of reference translations and embedding-based evaluation methods.

The first part demonstrates that controlled paraphrasing of reference translations improves the
robustness of string-based metrics, while more complex generation methods do not necessarily outperform
simpler ones. The second part analyzes the geometric properties of sentence embeddings, identifying
interpretable structures in which linguistic transformations correspond to consistent directional shifts.
It introduces a new dataset of complex sentence transformations for Czech (Costra) and shows that current
sentence embedding models rely heavily on surface similarity, and that strong performance on intrinsic
evaluation tasks does not reliably predict effectiveness in machine translation evaluation.

## Building

Requires a TeX distribution (TeX Live or MiKTeX) with `pdflatex` and `bibtex`.

```sh
cd en
make            # produces thesis.pdf
```

Alternatively, with `latexmk` (also works on Windows):

```powershell
cd en
$env:TEXINPUTS = "../tex//;"
latexmk -pdf thesis.tex
```