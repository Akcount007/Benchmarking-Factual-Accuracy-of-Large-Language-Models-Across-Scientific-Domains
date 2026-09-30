# Awesome Scientific LLM Factuality

A curated research and assignment repository on **benchmarking factual accuracy of large language models across scientific domains**.

This repository brings together an AI-assisted research paper, a citation-integrity audit, citation mapping, a structured literature review, Prism/LaTeX conversion evidence, and a final ACM-style review manuscript.

## Quick navigation

- [Assignment portfolio](#assignment-portfolio)
- [Repository evidence at a glance](#repository-evidence-at-a-glance)
- [Research scope](#research-scope)
- [Benchmark and method map](#benchmark-and-method-map)
- [Recommended evaluation protocol](#recommended-evaluation-protocol)
- [Literature-review workflow](#literature-review-workflow)
- [Repository structure](#repository-structure)
- [Compile the LaTeX projects](#compile-the-latex-projects)
- [Citation policy](#citation-policy)
- [References](#references)

## Assignment portfolio

| Assignment | Description | Deliverables |
|---|---|---|
| **1 — AI-assisted research paper** | Initial paper establishing the topic, benchmark families and seed references | [Research paper PDF](paper/AI_Assisted_Research_Paper.pdf) |
| **2 — Citation-integrity audit** | Systematic authenticity and claim-support audit of the paper's 10 references | [Audit PDF](citation-audit/Citation_Integrity_Audit.pdf.pdf) |
| **3 — Curated GitHub repository** | Organized papers, datasets, tools, implementations and learning materials | [References](references/references.md) · [Datasets](datasets/datasets.md) · [Tools](tools/tools.md) · [Implementations](implementations/github-repositories.md) |
| **4 — Citation verification and mapping** | Claim-level verification worksheet and ResearchRabbit citation-network evidence | [Assignment PDF](citation%20mapping/citation%20mapping.pdf) · [Verification workbook](citation%20mapping/mcl2026012_citation_verification%20%281%29.xlsx) · [Folder guide](citation%20mapping/README.md) |
| **5 — AI-assisted literature-review writing** | Comparative review of 20 papers using ResearchRabbit, Litmaps, Semantic Scholar and Elicit | [Review PDF](AI-assisted%20Literature%20Review%20Writing/ai%20assited%20litrature%20review%20writing.pdf) · [Literature workbook](AI-assisted%20Literature%20Review%20Writing/LiteratureList_T1.xlsx) · [Folder guide](AI-assisted%20Literature%20Review%20Writing/README.md) |
| **6 — Scientific writing using Prism and LaTeX** | Original paper, Prism conversion, Overleaf validation, prompt log, error log, comparison and reflection | [Prism project](Scientific%20Writing%20Using%20Prism%20and%20LaTeX/) · [Prism final PDF](Scientific%20Writing%20Using%20Prism%20and%20LaTeX/Prism_Final_Paper.pdf) · [LaTeX source](Scientific%20Writing%20Using%20Prism%20and%20LaTeX/main.tex) |
| **Final review paper — LaTeX and Overleaf** | Expanded nine-page ACM-style review with two figures and a 21-entry BibTeX bibliography | [Final PDF](Review%20Paper%20Writing%20and%20Formatting%20Using%20LaTeX%20and%20Overleaf/benchmarking_factual_accuracy_scientific_domains_final.pdf) · [Source project](Review%20Paper%20Writing%20and%20Formatting%20Using%20LaTeX%20and%20Overleaf/) |

## Repository evidence at a glance

| Evidence | Repository result |
|---|---|
| Initial research paper | 4 pages and 10 references |
| Citation-integrity audit | 10 references audited; the submitted worksheet reports 10 verified references and an authenticity score of 100/100 |
| Citation-support worksheet | 10 claim–citation records: 7 fully supported, 2 partially supported and 1 not supported/misattributed |
| Literature-review evidence base | 20 selected papers published from 2019–2024 |
| Research tools compared | ResearchRabbit, Litmaps, Semantic Scholar and Elicit |
| Tool contribution records | Semantic Scholar 17 papers, Elicit 14, ResearchRabbit 12 and Litmaps 11 before final synthesis |
| Prism evidence | 7 recorded prompts with screenshots, plus error log, paragraph comparison, reflection and checklist |
| LaTeX bibliographies | 21 BibTeX entries in each complete manuscript project |
| Final formatted review | 9 pages, 2 figures, benchmark table, cross-references and ACM-style bibliography |

The counts above come directly from the submitted PDFs, Excel workbooks, LaTeX projects and checklists stored in this repository.

## Research scope

Scientific factuality is not captured by a single accuracy score. The reviewed literature distinguishes several related evaluation targets:

1. **Knowledge and reasoning accuracy** — whether the model selects or derives a correct answer.
2. **Evidence-grounded verification** — whether a claim is supported or refuted by an identified source, as operationalized by SciFact.[^scifact]
3. **Biomedical research QA** — whether a model can reason over specialized PubMed abstracts, as tested by PubMedQA.[^pubmedqa]
4. **Truthfulness under misconceptions** — whether a model reproduces common human falsehoods, as examined by TruthfulQA.[^truthfulqa]
5. **Hallucination recognition** — whether generated or supplied content can be classified as hallucinated, as evaluated by HaluEval.[^halueval]
6. **Long-form atomic factuality** — whether individual propositions in a response are supported, as measured by FActScore.[^factscore]
7. **Black-box consistency checking** — whether independently sampled generations reveal unstable claims, as used by SelfCheckGPT.[^selfcheckgpt]
8. **Retrieval and temporal freshness** — whether search or retrieval helps answer changing questions while preserving evidence provenance, as studied by RAG and FreshLLMs.[^rag][^freshllms]
9. **Multilingual factuality** — whether atomic factual precision transfers across languages, as explored by Multi-FAct.[^multifact]
10. **Expert scientific reasoning** — whether models can answer difficult biology, physics and chemistry questions, as tested by GPQA.[^gpqa]

The repository's review papers therefore recommend reporting a **profile of performance** rather than one undifferentiated score.

## Benchmark and method map

| Resource | Primary evaluation target | Typical unit | Scientific relevance |
|---|---|---|---|
| [PubMedQA](https://doi.org/10.18653/v1/D19-1259) | Biomedical QA | Yes/no/maybe answer with abstract context | Biomedical evidence interpretation |
| [SciFact](https://doi.org/10.18653/v1/2020.emnlp-main.609) | Scientific claim verification | Claim, evidence rationale and support/refute label | Claim-level scientific evidence |
| [TruthfulQA](https://doi.org/10.18653/v1/2022.acl-long.229) | Resistance to common falsehoods | Adversarial question and answer | Misconception and truthfulness testing |
| [HaluEval](https://doi.org/10.18653/v1/2023.emnlp-main.397) | Hallucination recognition | Generated response or passage | Controlled hallucination evaluation |
| [SelfCheckGPT](https://arxiv.org/abs/2303.08896) | Black-box hallucination detection | Multiple sampled generations | Screening without model probabilities |
| [FActScore](https://arxiv.org/abs/2305.14251) | Long-form factual precision | Atomic proposition | Fine-grained response evaluation |
| [Multi-FAct](https://arxiv.org/abs/2402.18045) | Multilingual factuality | Multilingual atomic proposition | Language-aware evaluation |
| [GPQA](https://arxiv.org/abs/2311.12022) | Graduate-level scientific reasoning | Expert multiple-choice question | Biology, physics and chemistry |
| [Med-HALT](https://arxiv.org/abs/2307.15343) | Medical hallucination and reasoning | Medical reasoning and recall task | Domain-specific medical risk |
| [FreshLLMs](https://doi.org/10.18653/v1/2024.findings-acl.813) | Dynamic and search-augmented factuality | Time-sensitive or false-premise question | Temporal freshness and retrieval |
| [QAGS](https://doi.org/10.18653/v1/2020.acl-main.671) | Source-grounded summary factuality | Generated question–answer pair | Scientific summarization |
| [FacTool](https://arxiv.org/abs/2307.13528) | Tool-augmented factuality checking | Decomposed claim and tool result | Heterogeneous verifiable claims |

No row is a complete substitute for another: constrained QA, claim verification, atomic scoring and retrieval-enabled evaluation expose different failure modes.

## Recommended evaluation protocol

The final review project proposes a layered cross-domain protocol:

1. **Run two conditions:** closed-book generation and controlled evidence-grounded generation.
2. **Cover four task families:** constrained QA, claim–evidence verification, long-form synthesis and temporally changing questions.
3. **Stratify by scientific domain:** medicine, biology, chemistry, physics, climate science and engineering.
4. **Score at multiple levels:**
   - answer correctness;
   - atomic claim precision and coverage;
   - contradiction and numerical/unit accuracy;
   - evidence retrieval and citation entailment;
   - calibration, uncertainty and abstention; and
   - severity of potential scientific harm.
5. **Control contamination and staleness:** use hidden items, temporal splits, versioned evidence snapshots and refreshed test streams.
6. **Audit automated judges:** calibrate model- or entailment-based evaluation against blinded expert review.
7. **Report disaggregated results:** publish scores by domain, task, retrieval condition and error type rather than only a macro-average.

This design combines evidence retrieval with generation instead of assuming that retrieval alone guarantees factuality.[^rag][^retrievalpretraining] It also treats time-sensitive knowledge as a separate evaluation dimension.[^freshllms]

## Literature-review workflow

The workbook records the following staged process:

| Stage | Recommended tool(s) | Purpose |
|---|---|---|
| Topic exploration | Semantic Scholar and Elicit | Test terminology and identify benchmark families |
| Initial discovery | Semantic Scholar | Retrieve a precise, metadata-rich starting set |
| Foundational literature | ResearchRabbit and Litmaps | Follow backward citations and chronological origins |
| Recent literature | Semantic Scholar and Litmaps | Apply year filters and forward-citation expansion |
| Related-paper expansion | ResearchRabbit | Explore similar work and citation networks |
| Comparison and synthesis | Elicit | Structure research questions, methods, findings and limitations |
| Gap identification | Elicit, Litmaps and human review | Compare limitations and inspect sparse or emerging areas |
| Final writing | Human synthesis supported by all four tools | Read sources, reconcile definitions and cite accurately |

The process intentionally retains human verification: tool-generated summaries and citation-network proximity are discovery aids, not evidence by themselves.

## Repository structure

```text
.
├── README.md
├── paper/
│   └── AI_Assisted_Research_Paper.pdf
├── citation-audit/
│   └── Citation_Integrity_Audit.pdf.pdf
├── citation mapping/
│   ├── README.md
│   ├── citation mapping.pdf
│   └── mcl2026012_citation_verification (1).xlsx
├── AI-assisted Literature Review Writing/
│   ├── README.md
│   ├── ai assited litrature review writing.pdf
│   └── LiteratureList_T1.xlsx
├── Scientific Writing Using Prism and LaTeX/
│   ├── README.md
│   ├── Original_Paper.pdf
│   ├── Prism_Final_Paper.pdf
│   ├── Overleaf_Final_Paper.pdf
│   ├── main.tex
│   ├── references.bib
│   ├── Prompt_Log.pdf
│   ├── Error_Log.pdf
│   ├── Paragraph_Comparison.pdf
│   ├── Reflection.pdf
│   ├── Submission_Checklist.pdf
│   └── figure/
├── Review Paper Writing and Formatting Using LaTeX and Overleaf/
│   ├── README.md
│   ├── benchmarking_factual_accuracy_scientific_domains_final.pdf
│   ├── main.tex
│   ├── references.bib
│   └── figure/
├── datasets/
├── implementations/
├── references/
├── tools/
└── LICENSE
```

## Compile the LaTeX projects

### Prism conversion project

```bash
cd "Scientific Writing Using Prism and LaTeX"
pdflatex main.tex
bibtex main
pdflatex main.tex
pdflatex main.tex
```

### ACM-style review project

```bash
cd "Review Paper Writing and Formatting Using LaTeX and Overleaf"
pdflatex main.tex
bibtex main
pdflatex main.tex
pdflatex main.tex
```

The ACM-style source uses:

```latex
\documentclass[manuscript,nonacm]{acmart}
```

Upload `main.tex`, `references.bib` and the `figure/` folder together when using Overleaf.

## Citation policy

When adding a new resource:

1. Prefer the DOI, ACL Anthology, publisher, official repository or arXiv record.
2. Confirm that the identifier resolves to the stated publication.
3. Check title, authors, year and venue.
4. Distinguish publication authenticity from claim support.
5. Cite the source immediately after the statement it supports.
6. Do not leave unresolved citation placeholders; use a working persistent link or a Markdown footnote.
7. Record limitations and partial support rather than forcing a binary verified/not-verified judgment.

## References

[^pubmedqa]: Q. Jin, B. Dhingra, Z. Liu, W. Cohen, and X. Lu. “PubMedQA: A Dataset for Biomedical Research Question Answering.” EMNLP-IJCNLP, 2019. [DOI](https://doi.org/10.18653/v1/D19-1259).
[^scifact]: D. Wadden, S. Lin, K. Lo, et al. “Fact or Fiction: Verifying Scientific Claims.” EMNLP, 2020. [DOI](https://doi.org/10.18653/v1/2020.emnlp-main.609).
[^truthfulqa]: S. Lin, J. Hilton, and O. Evans. “TruthfulQA: Measuring How Models Mimic Human Falsehoods.” ACL, 2022. [DOI](https://doi.org/10.18653/v1/2022.acl-long.229).
[^halueval]: J. Li, X. Cheng, X. Zhao, J.-Y. Nie, and J.-R. Wen. “HaluEval: A Large-Scale Hallucination Evaluation Benchmark for Large Language Models.” EMNLP, 2023. [DOI](https://doi.org/10.18653/v1/2023.emnlp-main.397).
[^selfcheckgpt]: P. Manakul, A. Liusie, and M. J. F. Gales. “SelfCheckGPT: Zero-Resource Black-Box Hallucination Detection for Generative Large Language Models.” EMNLP, 2023. [arXiv](https://arxiv.org/abs/2303.08896).
[^factscore]: S. Min, K. Krishna, X. Lyu, et al. “FActScore: Fine-Grained Atomic Evaluation of Factual Precision in Long-Form Text Generation.” EMNLP, 2023. [arXiv](https://arxiv.org/abs/2305.14251).
[^multifact]: S. Shafayat, E. Kim, J. Oh, and A. Oh. “Multi-FAct: Assessing Factuality of Multilingual LLMs Using FActScore.” 2024. [arXiv](https://arxiv.org/abs/2402.18045).
[^gpqa]: D. Rein, B. L. Hou, A. C. Stickland, et al. “GPQA: A Graduate-Level Google-Proof Q&A Benchmark.” 2023. [arXiv](https://arxiv.org/abs/2311.12022).
[^rag]: P. Lewis, E. Perez, A. Piktus, et al. “Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks.” NeurIPS, 2020. [Paper](https://proceedings.neurips.cc/paper/2020/hash/6b493230205f780e1bc26945df7481e5-Abstract.html).
[^retrievalpretraining]: B. Wang, W. Ping, P. Xu, et al. “Shall We Pretrain Autoregressive Language Models with Retrieval? A Comprehensive Study.” EMNLP, 2023. [DOI](https://doi.org/10.18653/v1/2023.emnlp-main.482).
[^freshllms]: T. Vu, M. Iyyer, X. Wang, et al. “FreshLLMs: Refreshing Large Language Models with Search Engine Augmentation.” Findings of ACL, 2024. [DOI](https://doi.org/10.18653/v1/2024.findings-acl.813).

## License

Released under the [MIT License](LICENSE).
