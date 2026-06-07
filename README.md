# scRNA-seq Analysis of Mouse Skin Wound Healing
## Overview
This repository contains a reproduction of the workflow described in the JoVE publication:
**Using R, Seurat, and CellChat to Analyze a Single-Cell Transcriptomics Dataset of Mouse Skin Wound Healing** (Keiser et al., 2025).

The project reproduces a complete single-cell RNA sequencing (scRNA-seq) analysis workflow using R, Seurat, and CellChat. The analysis focuses on mouse skin wound healing and includes data preprocessing, quality control, clustering, cell type annotation, fibroblast subtype analysis, module scoring, and cell-cell communication analysis.

---

## Dataset

**GEO Accession:** GSE204777

The dataset contains single-cell transcriptomic profiles collected from mouse skin wounds at multiple time points and spatial locations during the wound healing process.

---

## Objectives

- Perform quality control of scRNA-seq data
- Remove low-quality cells and doublets
- Normalize and cluster cells using Seurat
- Annotate major cell populations
- Identify fibroblast subtypes
- Analyze wound healing phase-specific gene signatures
- Explore cell-cell communication using CellChat
- Reproduce the analyses and visualizations presented in the original publication

---

## Tools and Packages

### Programming Language

- R

### Main Packages

- Seurat
- CellChat
- scDblFinder
- tidyverse
- ggplot2
- readr
- dplyr

---

## Workflow

### 1. Data Preprocessing

- Download data from GEO
- Import count matrices
- Create Seurat objects
- Demultiplex multiplexed samples using HTO barcodes

### 2. Quality Control

- Filter cells with low feature counts
- Calculate mitochondrial gene percentages
- Remove low-quality cells
- Detect and remove doublets using scDblFinder

### 3. Cell Clustering and Annotation

- Normalize expression data
- Identify highly variable genes
- Perform PCA
- Generate UMAP embeddings
- Cluster cells using Seurat
- Identify marker genes
- Annotate cell types

### 4. Fibroblast Subtype Analysis

- Subset fibroblast populations
- Re-cluster fibroblasts
- Identify subtype-specific marker genes
- Analyze temporal distributions

### 5. Module Scoring

Module scores were calculated for genes associated with:

- Inflammatory phase
- Proliferative phase
- Resolution phase

### 6. Cell-Cell Communication Analysis

CellChat was used to infer ligand-receptor interactions and compare cellular communication patterns during different wound healing stages.

---

## Major Cell Types Identified

- Macrophages
- Neutrophils
- Fibroblasts
- Epithelial Cells
- Endothelial Cells
- T Cells
- Smooth Muscle Cells

---

## Repository Structure

```text
├── README.md
├── Mouse_Skin_Wound_Healing_scRNAseq_Analysis.Rmd
```

---

## Reproducibility

This project follows the workflow presented in the JoVE publication as closely as possible. Minor differences in clustering results or UMAP visualizations may occur due to stochastic components of the algorithms and differences in computing environments.

---

## Reference

Keiser S., Botello N., Cruz E., Wietecha M.S. (2025).

*Using R, Seurat, and CellChat to Analyze a Single-Cell Transcriptomics Dataset of Mouse Skin Wound Healing.*

Journal of Visualized Experiments (JoVE), e67266.

DOI: 10.3791/67266
