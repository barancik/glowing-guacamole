# Evaluating Metrics for Machine Translation Evaluation: From Paraphrases to Semantic Embeddings

LaTeX source of the doctoral thesis by **Mgr. Petra Barančíková**,
Institute of Formal and Applied Linguistics (ÚFAL), Faculty of Mathematics and Physics, Charles University.

- **Study programme:** Computational Linguistics
- **Supervisor:** doc. RNDr. Markéta Lopatková, Ph.D.
- **Consultant:** doc. RNDr. Ondřej Bojar, Ph.D.
- **Year:** 2026

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

**Keywords:** machine translation evaluation, automatic evaluation metrics, paraphrasing, sentence embeddings

## Repository structure

```
en/             thesis source (English)
  thesis.tex      main file – metadata, abstract, chapter list
  autoreferat.tex stand-alone thesis summary (autoreferát), built separately
  bibliography.bib
  macros.tex      custom commands
  Makefile
img/            figures (PNG, PDF, SVG sources)
tex/            additional TeX macros (searched via TEXINPUTS)
```

### Thesis outline

| Chapter | Files |
|---|---|
| Introduction | `preface.tex` |
| Machine Translation Evaluation | `evaluation.tex`, `rw.tex` |
| Targeted Sentence Paraphrasing for MT Evaluation (incl. Parmesan) | `data.tex`, `substitution.tex`, `parmesan.tex`, `moses.tex`, `treex_paraphrasing.tex` |
| Sentence Embedding Evaluation | `second_part.tex`, `linear_relations.tex`, `costra.tex`, `extrinsic.tex` |
| Conclusion | `epilog.tex` |
| Appendix | `appendix.tex` |

Files not included in the build: `rw2.tex`, `todo.tex`, `notes.txt` (drafts and working notes).

## Building

Requires a TeX distribution (TeX Live or MiKTeX) with `pdflatex` and `bibtex`.

**Linux / macOS**

```sh
cd en
make            # produces thesis.pdf
make clean
```

**Windows / any platform with latexmk**

```powershell
cd en
$env:TEXINPUTS = "../tex//;"
latexmk -pdf thesis.tex
latexmk -pdf autoreferat.tex
```

The thesis can also be compiled on Overleaf (set `en/thesis.tex` as the main document).
