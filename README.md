# Gene Embedding Hub

Gene Embedding Hub brings together standardized human gene embeddings derived from multiple biological modalities. This repository contains the code for constructing and analysing the collection, together with the infrastructure for validating and publishing community contributions.

## Repository structure

| Directory | Purpose |
| --- | --- |
| [`Gene-Embeddings/`](Gene-Embeddings/README.md) | Embedding processing pipelines, construction of the standardized master gene table, and comparative analyses. |
| [`Gene-Embeddings-contributions/`](Gene-Embeddings-contributions/README.md) | Community submission validation, contribution registry management, publication workflows, and the interactive catalogue. |

Each component has its own documentation and retains its internal directory structure.

## Processing and analysis

The [`Gene-Embeddings/`](Gene-Embeddings/) component contains:

- [`embeddings/`](Gene-Embeddings/embeddings/): processing scripts organized by embedding identifier.
- [`master_gene_table/`](Gene-Embeddings/master_gene_table/README.md): construction and harmonization of the human gene reference table.
- [`analysis/`](Gene-Embeddings/analysis/): configurations, scripts, and cluster job files for pairwise comparisons, directional predictability, and consensus graph analyses.

Processed embedding matrices are hosted on Hugging Face and are not duplicated in this repository.

## Community contributions

The [`Gene-Embeddings-contributions/`](Gene-Embeddings-contributions/README.md) component provides the infrastructure for receiving, validating, and publishing additional gene embeddings.

Contributors submit packages through Hugging Face. A GitHub account or fork is not required. See the [submission guide](Gene-Embeddings-contributions/docs/HUGGINGFACE_SUBMISSION.md) for instructions and the [automatic acceptance policy](Gene-Embeddings-contributions/docs/AUTOMATIC_ACCEPTANCE_POLICY.md) for validation criteria.

Acceptance indicates compliance with the technical submission policy; it does not constitute independent scientific or legal endorsement.

## Hugging Face resources

- [Embedding dataset](https://huggingface.co/datasets/BoevaLab/Gene-Embedding-Hub-dataset)
- [Interactive catalogue](https://huggingface.co/spaces/BoevaLab/Gene-Embedding-Hub)
- [Community submission dataset](https://huggingface.co/datasets/BoevaLab/Gene-Embedding-Hub-contributions-staging)

