# Verified Research Papers — Recall Bias in AI Literature Curation

This file mirrors the categorized paper lists in the main README. Minimum
requirement: **20 verified papers**. The 13 below are drawn from the
student's own AI-assisted paper's reference list and should still be
independently checked (title, authors, year, venue, DOI, existence, link
match) before final submission — do not assume they are correct just
because they came from the paper.

## Format

```
- **Paper Title**
  Authors, Year, Journal/Conference
  [Paper / DOI](link)
  One-line explanation of why the paper is relevant.
```

## Survey and Review Papers

- **Biases in scholarly recommender systems: Impact, prevalence, and mitigation**
  Michael Färber, Melissa Coutinho, Shuzhou Yuan — 2023, Scientometrics, 128, 2703–2736
  [DOI: 10.1007/s11192-023-04636-2](https://doi.org/10.1007/s11192-023-04636-2)
  Systematic review of bias sources in scholarly recommender systems and mitigation strategies.

- **Citation recommendation: Approaches and datasets**
  Michael Färber, Adam Jatowt — 2020, International Journal on Digital Libraries, 21, 375–405
  [DOI: 10.1007/s00799-020-00288-2](https://doi.org/10.1007/s00799-020-00288-2)
  Review of content-, metadata-, and graph-based citation recommendation approaches.

## Foundational Papers

- **The Matthew effect in science**
  Robert K. Merton — 1968, Science, 159(3810), 56–63
  [DOI: 10.1126/science.159.3810.56](https://doi.org/10.1126/science.159.3810.56)
  Originates the cumulative-advantage concept central to algorithmic visibility feedback loops.

- **The Matthew Effect in Science, II**
  Robert K. Merton — 1988, Isis, 79(4), 606–623
  [DOI: 10.1086/354848](https://doi.org/10.1086/354848)
  Extends the Matthew effect framework used to explain citation-based ranking bias.

- **SPECTER: Document-level representation learning using citation-informed transformers**
  Arman Cohan, Sergey Feldman, Iz Beltagy, Doug Downey, Daniel S. Weld — 2020, ACL 2020
  [DOI: 10.18653/v1/2020.acl-main.207](https://doi.org/10.18653/v1/2020.acl-main.207)
  Citation-informed embedding model that can inherit existing scholarly-visibility structure.

- **S2ORC: The Semantic Scholar Open Research Corpus**
  Kyle Lo, Lucy Lu Wang, Mark Neumann, Rodney Kinney, Daniel S. Weld — 2020, ACL 2020
  [DOI: 10.18653/v1/2020.acl-main.447](https://doi.org/10.18653/v1/2020.acl-main.447)
  Large English-language scientific corpus illustrating infrastructure-level language bias.

- **SciBERT: A pretrained language model for scientific text**
  Iz Beltagy, Kyle Lo, Arman Cohan — 2019, EMNLP-IJCNLP 2019
  [DOI: 10.18653/v1/D19-1371](https://doi.org/10.18653/v1/D19-1371)
  Pretrained scientific-text language model underlying much subsequent scientific NLP work.

- **OpenAlex: A fully-open index of scholarly works, authors, venues, institutions, and concepts**
  Jason Priem, Heather Piwowar, Richard Orr — 2022
  [arXiv:2205.01833](https://arxiv.org/abs/2205.01833)
  Open scholarly knowledge graph used for independently auditing coverage and bias.

## Recent Research Papers

- **Language Bias in Information Retrieval: The Nature of the Beast and Mitigation Methods**
  Jinrui Yang, Fan Jiang, Tim Baldwin — 2025
  [arXiv:2509.06195](https://arxiv.org/abs/2509.06195)
  Documents ranking disparities across languages and proposes a language-fairness
  training objective (LaKDA).

- **Evaluating the Linguistic Coverage of OpenAlex**
  L. Céspedes, D. Kozlowski, C. Pradier, et al. — 2024
  [arXiv:2409.10633](https://arxiv.org/abs/2409.10633)
  Finds OpenAlex overestimates English-language share due to metadata inaccuracies.

## Methods / Algorithms

- **Towards finding non-obvious papers: An analysis of citation recommender systems**
  Han Jia, Erik Saule — 2018
  [arXiv:1812.11252](https://arxiv.org/abs/1812.11252)
  Examines the tension between predicting likely citations and surfacing less-visible literature.

## Applications / Evaluation Evidence

- **Languages are still a major barrier to global science**
  Tatsuya Amano, Juan P. González-Varo, William J. Sutherland — 2016, PLOS Biology, 14(12), e2000933
  [DOI: 10.1371/journal.pbio.2000933](https://doi.org/10.1371/journal.pbio.2000933)
  Found over a third of biodiversity-conservation documents were non-English; key
  empirical evidence for English-only search bias.

- **The effect of English-language restriction on systematic review-based meta-analyses**
  A. Morrison, J. Polisena, D. Husereau, et al. — 2012, Int'l Journal of Technology Assessment in Health Care, 28(2), 138–144
  [DOI: 10.1017/S0266462312000086](https://doi.org/10.1017/S0266462312000086)
  Reviews empirical studies on the effect of English-only restrictions in systematic reviews.

## Evaluation Methods / Benchmarks

<!-- TODO: add papers specifically about Recall@k, group-conditional recall,
or fairness benchmarking in IR -->

---

**TODO: this list currently has 13 papers. Find, read, and independently
verify at least 7 more (via Google Scholar / Crossref / Semantic Scholar) to
meet the 20-paper minimum, and slot them into the categories above.**
