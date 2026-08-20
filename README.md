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

## Key findings

- **Macrostructure (DV1):** The network is connected (largest weakly connected component = 73.6% of nodes) but almost acyclic (largest strongly connected component = only 26 nodes). Unlike the WWW, it shows **no bow-tie structure**. The densest k-core (k=19) consists of rechtbanken (district courts) citing each other within the same legal domain, not the most-cited authorities.
- **Distribution of influence (DV2):** Influence is highly concentrated: the top 1% of rulings receive 36% of all citations. Gini coefficients range from 0.447 (PageRank) to 0.994 (HITS authority). The tail resembles a power law (exponent ≈ 2), but likelihood-ratio tests show a log-normal distribution fits at least as well: a heavy tail, but power law is not confirmed as the underlying model. The single most authoritative ruling is the *Haviltex* judgment (HR:1981:AG4158), the leading case on contract interpretation; 92 of the top 100 rulings by HITS authority are Hoge Raad decisions.
- **Agreement between measures (DV3):** In-degree and PageRank are strongly correlated (Spearman's ρ = 0.880) and largely interchangeable as general influence measures. HITS authority diverges (ρ = 0.39 vs. PageRank), capturing a more positional property rather than broad influence.
- **Communities vs. legal domains (DV4):** Leiden community detection on the largest component finds 272 communities (modularity Q = 0.86). Communities are internally very pure (avg. purity 0.94) but each legal domain fragments into many small communities (ARI = 0.079, homogeneity = 0.72): the network reconstructs law as many specialized sub-fields rather than a few broad domains.
- **Citation flow between courts (DV5):** Contrary to the expectation of citations flowing mostly upward (lower courts citing higher courts), assortativity is slightly positive (r = 0.105), driven by high self-citation rates in the highest administrative courts (Raad van State 67%, Centrale Raad van Beroep 64%, College van Beroep voor het bedrijfsleven 81%).

**Conclusion:** the citation network is connected but nearly acyclic, with extremely unevenly distributed influence, organized along three principles: temporal ordering (citations point to the past), specialization (citations stay within their legal domain), and hierarchy (upward cassation flow, partly offset by self-citation).

## Reproducing the analysis

The notebooks were run in Python with:

```
pandas, numpy, scipy, scikit-learn
networkx, python-igraph, leidenalg, powerlaw
matplotlib, seaborn
```

```bash
pip install pandas numpy scipy scikit-learn networkx python-igraph leidenalg powerlaw matplotlib seaborn
```

The underlying citation data is derived from Rechtspraak.nl open data via LIDO and is not redistributed here; see the [Rechtspraak.nl open data documentation](https://www.rechtspraak.nl/Uitspraken/paginas/open-data.aspx) for access.

## Limitations

- Citation types are not differentiated: the network does not distinguish whether a citation affirms, distinguishes, or rejects the cited ruling.
- Data cleaning isolates roughly 23,000 nodes.
- Legal domain (*rechtsgebied*) is known for 91% of rulings, PHR opinions require separate interpretation.
- Covers case law only, not legislation, and Rechtspraak.nl itself is a curated selection of Dutch case law rather than a complete record.

## Future work

- Incorporate citation function (affirming vs. distinguishing vs. rejecting).
- Study the temporal dynamics of influence following a landmark ruling.
- Explicitly weight or separate out PHR opinions in the network.
- Compare against citation networks from other legal systems.


## Citation

If you use this work, please cite:

> Wiegman, V.H.Z.R. (2026). *Citatiestructuren in de Nederlandse rechtspraak: Een netwerkanalyse van macrostructuur, invloed en organisatie* [Bachelor's thesis, University of Amsterdam].

## Contact

Vincent H.Z.R. Wiegman, [vinwiegman@gmail.com](mailto:vinwiegman@gmail.com)

