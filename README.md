# Citation Structures in Dutch Case Law

**A network analysis of macrostructure, influence, and organization in the Rechtspraak.nl citation network**

Bachelor's thesis, Information Science (Informatiekunde), University of Amsterdam
Author: Vincent H.Z.R. Wiegman · Supervisor: Dr. M.J. Marx · 2025-2026

---

## About this project

Dutch courts do not operate under *stare decisis*, yet judges regularly cite earlier rulings. This project models Dutch case law as a directed citation network (each ruling a node, each citation an edge) to describe its structure and how legal influence is distributed, rather than trying to find "the most important ruling." 

**Main research question:** What structural properties does the Dutch case-law citation network exhibit, and how is legal influence distributed across rulings, legal domains (*rechtsgebieden*), and courts?

Five sub-questions, which structure both the analysis notebook and the thesis itself:

1. **Macrostructure**: connectivity, bow-tie structure, k-core decomposition.
2. **Distribution of influence**: in-degree, PageRank, HITS authority; does it follow a power law?
3. **Agreement between influence measures**: do these different measures point to the same rulings?
4. **Communities vs. legal domains**: does network community structure line up with the official legal-domain labels?
5. **Citation flow between courts**: is there a directional, hierarchical flow of citations between court types?


## Data

The network is built from citation data sourced from **LIDO** (Linked Data Overheid), covering rulings published via [Rechtspraak.nl](https://www.rechtspraak.nl), the Dutch judiciary's open data platform.

- Raw data: ~7.3 million references across ~1.6 million nodes.
- Restricted to the **jurisprudence subgraph** (only citations between rulings, references to legislation etc. are excluded).
- Cleaning: removed 130,206 temporally impossible citations (9.6%, mostly recent ECHR nodes with invalid dates) and distinguished the *Parket bij de Hoge Raad* (PHR, Advocate General opinions) as a distinct node type.
- **Final network: 674,589 rulings, 1,223,458 citations, spanning from 1862-2024.**

Raw data and the large intermediate files are not included in this repository (size and redistribution constraints). See [Reproducing the analysis](#reproducing-the-analysis)

## Repository structure
```
.
├── notebooks/
│   ├── 1-network_analysis.ipynb
│   ├── 2- hele_netwerk.ipynb
│   └── 3- winkels_vergelijking.ipynb         
├── slides/
│   ├── defense.pdf
│   └── defense.tex
├── thesis/
│   └── thesis.pdf              
├── README.md
└── references (4).bib

```
