# Recall-bias-toward-highly-cited-and-English-language-papers-in-AI-literature-curation
# Awesome Recall Bias in AI Literature Curation

A curated collection of research papers, tools, implementations, and learning
resources on **citation-popularity bias and English-language bias in AI-assisted
literature curation** — how scholarly search, recommendation, and retrieval
systems can systematically under-retrieve recent, low-citation, or non-English
research even while appearing to perform well in aggregate.

> ⚠️ **Status:** Work in progress — resources below are being added and
> verified incrementally. See commit history for development over time.

## Contents

- [Overview](#overview)
- [AI-Assisted Research Paper](#ai-assisted-research-paper)
- [Citation Integrity Audit](#citation-integrity-audit)
- [Survey Papers](#survey-papers)
- [Foundational Papers](#foundational-papers)
- [Recent Research Papers](#recent-research-papers)
- [Methods / Algorithms](#methods--algorithms)
- [Applications / Evidence](#applications--evidence)
- [Datasets and Scholarly Corpora](#datasets-and-scholarly-corpora)
- [Tools and Libraries](#tools-and-libraries)
- [GitHub Implementations](#github-implementations)
- [Tutorials and Learning Resources](#tutorials-and-learning-resources)
- [License](#license)

## Overview

<!-- TODO: this is a starting draft — edit it in your own words. -->

AI-assisted literature curation increasingly relies on scholarly search
engines, citation databases, recommender systems, and semantic retrieval
models such as SPECTER to help researchers find relevant work. While these
tools improve scalability, they can also reproduce structural inequalities in
scholarly visibility. Two risks stand out: citation-popularity bias, where
highly cited papers receive disproportionate retrieval exposure regardless of
current relevance, and English-language bias, where non-English publications
are less readily indexed, retrieved, and incorporated into evidence
syntheses. These biases can compound — a recent, non-English, low-citation
paper faces several simultaneous disadvantages.

The core problem is that conventional recall metrics hide this because the
full set of relevant literature is rarely known. A more informative approach
is group-conditional recall — measuring retrieval rates separately by
language, citation percentile, or publication age — to reveal disparities
that aggregate metrics conceal. Mitigation strategies include citation-neutral
first-stage retrieval, multilingual query expansion and embeddings,
diversity-aware reranking, transparent display of citation counts as metadata
rather than a ranking signal, and human verification of underrepresented
groups. The goal is not to suppress influential papers or artificially boost
non-English ones, but to give all relevant research a fair opportunity to
enter the candidate evidence set.

## AI-Assisted Research Paper

**Recall Bias Toward Highly-Cited and English-Language Papers in AI
Literature Curation**
[View Paper](paper/Recall_Bias_in_AI_Literature_Curation.pdf)

Examines citation-popularity bias and English-language bias as interacting
properties of the AI literature-curation pipeline, formalizes group-conditional
and intersectional recall metrics, and proposes an 8-stage framework for
bias-resistant literature curation.

## Citation Integrity Audit

All references in the AI-assisted paper above were checked for accuracy —
correct title, authorship, venue, year, and DOI/arXiv ID, and whether each
paper genuinely supports the claim it's cited for.

[View Citation Integrity Audit](citation-audit/Citation_Integrity_Audit.pdf)

## Survey Papers

- **Biases in scholarly recommender systems: Impact, prevalence, and mitigation**
  Michael Färber, Melissa Coutinho, Shuzhou Yuan — 2023, *Scientometrics*, 128, 2703–2736
  [DOI: 10.1007/s11192-023-04636-2](https://doi.org/10.1007/s11192-023-04636-2) · [arXiv:2301.07483](https://arxiv.org/abs/2301.07483)
  Systematic review distinguishing biases from human scholarly behavior vs. those
  introduced/amplified by recommender algorithms; central to this repo's framing.

- **Citation recommendation: Approaches and datasets**
  Michael Färber, Adam Jatowt — 2020, *International Journal on Digital Libraries*, 21, 375–405
  [DOI: 10.1007/s00799-020-00288-2](https://doi.org/10.1007/s00799-020-00288-2) · [arXiv:2002.06961](https://arxiv.org/abs/2002.06961)
  Broad review of content-, metadata-, and graph-based citation recommendation
  approaches, relevant to understanding how citation networks are used in retrieval.

## Foundational Papers

- **The Matthew effect in science**
  Robert K. Merton — 1968, *Science*, 159(3810), 56–63
  [DOI: 10.1126/science.159.3810.56](https://doi.org/10.1126/science.159.3810.56)
  Originates the "cumulative advantage" concept underlying how algorithmic
  citation-based ranking can compound existing visibility.

- **The Matthew Effect in Science, II: Cumulative advantage and the symbolism of intellectual property**
  Robert K. Merton — 1988, *Isis*, 79(4), 606–623
  [DOI: 10.1086/354848](https://doi.org/10.1086/354848)
  Extends the Matthew effect framework, directly informing the paper's feedback-loop argument.

- **SPECTER: Document-level representation learning using citation-informed transformers**
  Arman Cohan, Sergey Feldman, Iz Beltagy, Doug Downey, Daniel S. Weld — 2020, ACL 2020, 2270–2282
  [DOI: 10.18653/v1/2020.acl-main.207](https://doi.org/10.18653/v1/2020.acl-main.207) · [arXiv:2004.07180](https://arxiv.org/abs/2004.07180)
  Key example of a citation-informed embedding model that can inherit existing
  scholarly-visibility structure.

- **S2ORC: The Semantic Scholar Open Research Corpus**
  Kyle Lo, Lucy Lu Wang, Mark Neumann, Rodney Kinney, Daniel S. Weld — 2020, ACL 2020, 4969–4983
  [DOI: 10.18653/v1/2020.acl-main.447](https://doi.org/10.18653/v1/2020.acl-main.447) · [arXiv:1911.02782](https://arxiv.org/abs/1911.02782)
  Large English-language scientific corpus; illustrates how infrastructure
  composition can bias downstream models.

- **SciBERT: A pretrained language model for scientific text**
  Iz Beltagy, Kyle Lo, Arman Cohan — 2019, EMNLP-IJCNLP 2019, 3615–3620
  [DOI: 10.18653/v1/D19-1371](https://doi.org/10.18653/v1/D19-1371) · [arXiv:1903.10676](https://arxiv.org/abs/1903.10676)
  Pretrained scientific-text language model underlying much subsequent scientific NLP.

- **OpenAlex: A fully-open index of scholarly works, authors, venues, institutions, and concepts**
  Jason Priem, Heather Piwowar, Richard Orr — 2022
  [arXiv:2205.01833](https://arxiv.org/abs/2205.01833)
  Open scholarly knowledge graph enabling independent auditing of database coverage.

## Recent Research Papers

- **Language Bias in Information Retrieval: The Nature of the Beast and Mitigation Methods**
  Jinrui Yang, Fan Jiang, Tim Baldwin — 2025
  [arXiv:2509.06195](https://arxiv.org/abs/2509.06195)
  Reports disparities in multilingual retrieval rankings and proposes LaKDA, a
  language-fairness training objective.

- **Evaluating the Linguistic Coverage of OpenAlex: An Assessment of Metadata Accuracy and Completeness**
  L. Céspedes, D. Kozlowski, C. Pradier, et al. — 2024
  [arXiv:2409.10633](https://arxiv.org/abs/2409.10633)
  Finds OpenAlex has more balanced language coverage than traditional databases
  but still overestimates English-language share due to metadata inaccuracies.

## Methods / Algorithms

- **Towards finding non-obvious papers: An analysis of citation recommender systems**
  Han Jia, Erik Saule — 2018
  [arXiv:1812.11252](https://arxiv.org/abs/1812.11252)
  Examines the tension between predicting likely citations and surfacing
  literature that isn't already well-connected in the citation graph.

## Applications / Evidence

- **Languages are still a major barrier to global science**
  Tatsuya Amano, Juan P. González-Varo, William J. Sutherland — 2016, *PLOS Biology*, 14(12), e2000933
  [DOI: 10.1371/journal.pbio.2000933](https://doi.org/10.1371/journal.pbio.2000933) · PMID: 28033326
  Found 35.6% of 75,513 biodiversity-conservation documents (2014) were non-English;
  key empirical evidence for English-only search bias.

- **The effect of English-language restriction on systematic review-based meta-analyses**
  A. Morrison, J. Polisena, D. Husereau, et al. — 2012, *International Journal of Technology Assessment in Health Care*, 28(2), 138–144
  [DOI: 10.1017/S0266462312000086](https://doi.org/10.1017/S0266462312000086) · PMID: 22559755
  Reviews empirical studies on the effect of English-only restrictions in
  systematic reviews and meta-analyses.

<!-- TODO: the paper above lists 13 references. The assignment requires 20+.
Find, read, and independently verify (Google Scholar / Crossref / Semantic
Scholar) at least 7 more papers on citation bias, multilingual IR, or
scholarly recommender fairness and add them to the appropriate category
above using the same format. -->

## Datasets and Scholarly Corpora

This topic concerns retrieval/recommendation systems rather than a domain
dataset, so the closest equivalents are the scholarly corpora and benchmarks
the field trains and evaluates on:

- **S2ORC (Semantic Scholar Open Research Corpus)**
  Source: Allen Institute for AI
  Description: 81.1M English-language academic papers, with structured full
  text for 8.1M open-access papers.
  Application: Training/evaluating scientific NLP and retrieval models.
  [Link](https://github.com/allenai/s2orc)

- **SciDocs**
  Source: Allen Institute for AI
  Description: Benchmark suite (classification, citation prediction,
  recommendation, user activity) used to evaluate SPECTER-style embeddings.
  Application: Evaluating citation-informed document representation models.
  [Link](https://github.com/allenai/scidocs)

- **OpenAlex**
  Source: OurResearch
  Description: Open scholarly knowledge graph of works, authors, venues,
  institutions, and concepts.
  Application: Auditing database coverage and language/citation distributions.
  [Link](https://openalex.org/)

## Tools and Libraries

- **[SPECTER / SPECTER2](https://github.com/allenai/specter)** — Citation-informed document embedding models for scientific papers.
- **[SciBERT](https://github.com/allenai/scibert)** — Pretrained BERT model for scientific text.
- **[OpenAlex API](https://docs.openalex.org/)** — Free API for querying the OpenAlex scholarly graph.
- **[Semantic Scholar API](https://api.semanticscholar.org/)** — API for paper metadata, citations, and precomputed SPECTER embeddings.
- **[SciDocs / SciRepEval](https://github.com/allenai/scidocs)** — Evaluation frameworks for scientific document embeddings.

## GitHub Implementations

- **[allenai/specter](https://github.com/allenai/specter)**
  Official SPECTER implementation, pretrained models, and link to the SciDocs
  evaluation framework.

- **[allenai/SPECTER2](https://github.com/allenai/SPECTER2)**
  Successor to SPECTER with task-specific adapters for classification,
  regression, and retrieval.

- **[allenai/scibert](https://github.com/allenai/scibert)**
  Official SciBERT pretraining and fine-tuning code.

- **[allenai/s2orc](https://github.com/allenai/s2orc)**
  Tools and documentation for working with the S2ORC corpus.

<!-- TODO: find and verify 1+ more implementation relevant to multilingual
retrieval or diversity-aware reranking specifically. -->

## Tutorials and Learning Resources

- **[OpenAlex API documentation](https://docs.openalex.org/)** — Official guide to querying works, authors, and concepts.
- **[Semantic Scholar API documentation](https://api.semanticscholar.org/)** — Official guide to the Semantic Scholar Academic Graph API.
- **[SPECTER model card (Hugging Face)](https://huggingface.co/allenai/specter)** — Usage examples for generating paper embeddings.
- **[SciBERT model card (Hugging Face)](https://huggingface.co/allenai/scibert_scivocab_uncased)** — Usage examples for the pretrained scientific-text model.

<!-- TODO: add 1+ more resource, e.g. a tutorial on bias evaluation in
recommender systems or multilingual IR. -->

## License

This repository's original content (README, audit summary, curation) is
licensed under the [MIT License](LICENSE). Linked third-party papers, tools,
and datasets remain under their own respective licenses — always check
before reuse.
