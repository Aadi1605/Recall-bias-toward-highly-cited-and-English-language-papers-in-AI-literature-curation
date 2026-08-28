# Datasets and Scholarly Corpora — Recall Bias in AI Literature Curation

This topic concerns literature retrieval/recommendation systems rather than
a domain-specific dataset (e.g. images, sensor readings). Traditional
"datasets" are not directly applicable in the usual sense. The closest
equivalents — and what's most relevant here — are the scholarly corpora and
benchmarks the field itself is trained and evaluated on. These are included
below to satisfy the spirit of the requirement.

## Format

```
- **Name**
  Source: ...
  Description: ...
  Application: ...
  [Link](url)
```

- **S2ORC (Semantic Scholar Open Research Corpus)**
  Source: Allen Institute for AI
  Description: 81.1M English-language academic papers, with structured full
  text for 8.1M open-access papers.
  Application: Training/evaluating scientific NLP and retrieval models;
  cited in the paper as an example of English-language infrastructure bias.
  [Link](https://github.com/allenai/s2orc)

- **SciDocs**
  Source: Allen Institute for AI
  Description: Benchmark suite (classification, citation prediction,
  recommendation, user-activity) accompanying the SPECTER model.
  Application: Evaluating citation-informed document representation models.
  [Link](https://github.com/allenai/scidocs)

- **OpenAlex**
  Source: OurResearch
  Description: Open scholarly knowledge graph of works, authors, venues,
  institutions, and concepts.
  Application: Auditing database coverage and language/citation-percentile
  distributions; used in Céspedes et al. (2024) to evaluate linguistic coverage.
  [Link](https://openalex.org/)

<!-- TODO: if you find a dataset more specific to your sub-focus (e.g. a
multilingual IR benchmark like the one used in Yang, Jiang & Baldwin 2025),
verify and add it here. -->
