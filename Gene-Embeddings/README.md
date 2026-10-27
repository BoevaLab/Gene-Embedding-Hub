# Gene Embeddings

This repository contains the processing scripts used to construct the standardized gene embeddings available in the Gene Embeddings Hugging Face resource.

The collection brings together human gene representations derived from multiple biological modalities, including protein sequence, DNA, RNA, gene expression, single-cell expression, biomedical literature, biological networks, knowledge graphs, ontologies, and functional annotations.

## Hugging Face resource

* Dataset: [Gene-Embedding-Hub-dataset](https://huggingface.co/datasets/BoevaLab/Gene-Embedding-Hub-dataset)
* Interactive Space: [Gene-Embedding-Hub](https://huggingface.co/spaces/BoevaLab/Gene-Embedding-Hub)

The processed embedding matrices are hosted on Hugging Face and are not duplicated in this GitHub repository.

## Repository structure

Processing scripts are organized under `embeddings/`.

Each subdirectory uses the same identifier as the corresponding Hugging Face package:

&#x20;   embeddings/<embedding\_id>/



A directory may contain one complete processing script or several numbered scripts when multiple processing steps are required.

## Standardized outputs

The processing pipelines generate the standardized files published on Hugging Face:

* `embeddings.npz`: embedding matrix stored under the key `embeddings`
* `genes.tsv`: standardized gene identifiers in the same row order as the matrix
* `metadata.json`: provenance and processing metadata
* `README.md`: embedding-level documentation

## Master gene table

The construction pipeline for the standardized human master gene table is documented in [`master_gene_table/`](master_gene_table/README.md).

## Analysis environment

The root [`env.yaml`](env.yaml) records Python and package versions exported
from the analysis environment. It targets Linux x86\_64
with CPU-only PyTorch and covers the workflows under `analysis/`.

From the repository root:

```bash
conda env create -f env.yaml
conda activate gene-embeddings-analysis
python -m pip check
```

