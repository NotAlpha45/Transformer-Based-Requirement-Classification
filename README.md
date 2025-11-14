# A Transformer Based Pipeline for Software Requirements Classification

This repository contains the LaTeX source and figures for the paper titled "A Transformer Based Pipeline for Software Requirements Classification".

It explores two approaches for improving software requirements processing:
- A lightweight transformer-based approach using DistilBERT and RoBERTa with an "Ensemble Pooling" method to identify relevant requirements.
- A retrieval-augmented generation (RAG) approach using GPT-4 and ChromaDB to classify functional vs non-functional requirements.

The paper presents dataset information, model architecture, experimental setup, and results (78% accuracy for the first approach and 86.67% for the second approach).

---

## Table of Contents
- Project Overview
- Building/Compiling the paper
- Repository structure
- Figures
- Datasets and Experiments
- Authors
- How to cite
- License & Contact

---

## Building / Compiling the paper ✅

Prerequisites:
- A TeX distribution on your system (TeX Live, TeXworks, or MiKTeX). 
- Optional: latexmk (recommended for easy compilation and dependency handling).

Compile using pdflatex + bibtex (PowerShell example):

```powershell
pdflatex conference_101719.tex
bibtex conference_101719
pdflatex conference_101719.tex
pdflatex conference_101719.tex
```

Or if you have latexmk installed (recommended):

```powershell
latexmk -pdf conference_101719.tex
latexmk -c   # clean auxiliary files (optional)
```

Open the generated PDF with the default system viewer:

```powershell
start .\conference_101719.pdf
```

Notes:
- The manuscript uses the `IEEEtran` class. Make sure your TeX distribution has it installed (it generally is included in most distributions).
- If you add or modify a reference in `Bibliography.bib`, re-run the compilation steps above to refresh citations.

---

## Repository structure 📁

- `conference_101719.tex` — Main LaTeX manuscript source
- `conference_101719.pdf` — Compiled PDF (built artifact)
- `Bibliography.bib` — BibTeX bibliography used in the manuscript
- `fig1.png` — a figure used in the manuscript (root-level figure)
- `Figures/` — Directory containing the manuscript figures
- `IEEEtran.cls` — IEEE LaTeX class used for formatting
- `IEEEtran_HOWTO.pdf` — Class HOWTO for formatting guidance

---

## Figures 🔍
All figures referenced in the paper are located under `Figures/`. Examples include: 
- `distilbert.png`, `roberta.png`, `transformer_architecture.png`
- `chromaDB.png`, `embedding.png`, `ensemble_pooling_classification.png`, `rerank.png` etc.

If you intend to edit figures, please place sources in a new `Figures/src/` subfolder (recommended) and update the `.tex` file accordingly.

---

## Datasets & Experiments 🔬
- The experiments discussed in the paper use the PURE dataset (Ferrari et al.) and a small custom FR-NFR dataset built from three real projects by the Ministry of ICT, Bangladesh.
- This repository contains the manuscript and figures only — there is no experiment code or dataset packaged in the repository. For experiment code, training scripts, or datasets, contact the authors or check a companion repository if available.

---

## Authors ✍️
- Maheen Mashrur Hoque
- Arman Hossain Dipu Khan
- Ahsan Habib
- Ajwad Abrar

See the manuscript for affiliations and more details.

---

## How to cite 📝
Please cite the paper if you use any of the methods or results presented in this manuscript. Use the BibTeX entries in `Bibliography.bib` to generate references.

---

