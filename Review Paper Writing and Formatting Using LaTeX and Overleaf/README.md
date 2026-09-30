# Benchmarking Factual Accuracy of Large Language Models Across Scientific Domains

## Included files

- `main.tex` — ACM `acmart` manuscript source with section, figure, table, and equation cross-references.
- `references.bib` — BibTeX bibliography used by `main.tex`.
- `figures/taxonomy.png` — taxonomy diagram.
- `figures/pipeline.png` — modular evaluation pipeline flowchart.
- `benchmarking_factual_accuracy_scientific_domains_final.pdf` — final assignment PDF compiled from the ACM LaTeX source.

## Compile in Overleaf

1. Create a blank Overleaf project.
2. Upload `main.tex`, `references.bib`, and the complete `figures/` folder.
3. Set the compiler to **XeLaTeX** (the source was validated with XeLaTeX/Tectonic).
4. Recompile twice so BibTeX and cross-references settle.
5. The manuscript uses the official ACM small-trim manuscript class with assignment mode: `\\documentclass[manuscript,nonacm]{acmart}`. The `nonacm` option removes the ACM submission footer and ACM publication block while preserving the official ACM layout.

The manuscript demonstrates `\\label{}`, `\\ref{}`, and `\\eqref{}` for sections, figures, tables, and the factuality equation. The bibliography is managed with BibTeX through `\\bibliographystyle{ACM-Reference-Format}` and `\\bibliography{references}`.
