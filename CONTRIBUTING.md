# Contributing

Contributions are welcome: new resources, corrections and updated links.

## What belongs here

- Databases, features and descriptors, representation learning, property-prediction models (classical ML, GNNs, transformers, equivariant networks, foundation models and universal potentials), OOD generalization, uncertainty, small-data learning, benchmarks, leaderboards, and language-model approaches for inorganic and crystalline materials.
- Peer-reviewed papers, preprints with a stable identifier, maintained code, and open datasets. Prefer a DOI or arXiv link for papers.

## Entry format

One bullet per entry, in the matching section, in this form:

```
* [Name or title](https://link) - One sentence on what it is or does (First-author et al., Year, Venue)
```

- Describe what the resource does, not how good it is.
- For code with a paper, link the code and add the paper at the end as `[[paper](https://doi.org/...)]`.
- State access limits when they matter, for example `(subscription)`.
- Put the entry in alphabetical or chronological order within its subsection, matching the neighbours.

## Before you open a pull request

```bash
python scripts/lint_readme.py        # format and duplicate checks
python scripts/check_links.py        # optional: confirms every URL still resolves
```

Add the entry to `data/papers.csv` as well, and add BibTeX for new papers to `data/references.bib`.

## Corrections

If an entry is wrong or a link is dead, open an issue or a pull request with the replacement. Please include a source for factual changes such as metrics, years and licences. Leaderboard numbers must state the date they were read.
