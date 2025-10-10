# Single-cell profiling of frog tail regeneration identifies ROC markers

**Author:** María Dolores Navarro Maturana (Lola) — mn3312

(https://colab.research.google.com/drive/1ZEFRZO5GRudCBl7NQhhmSN5nyY40UvkT?usp=sharing)

This repository contains the code and notebook used to identify the **Regenerative Organizing Cell (ROC)** in *Xenopus laevis* tail single-cell RNA-seq data, reproduce Fig. 1B-like views, and compare ROC markers to Supplementary Table 3. It implements two clustering algorithms (Leiden & Louvain), two marker methods (Wilcoxon & logistic regression), two denoising strategies (MAGIC & PCA low-rank), and two batch-integration methods (Harmony & BBKNN), with metrics and figures saved to disk.

---

## What's inside
- **`frog_and_tail.ipynb`** — main Colab notebook (fully reproducible).
- **`figures/`** — key plots (created on run), e.g.
  - `umap_Figure1_clustering.png`
  - `umap_Figure2_ROCscore.png`, `violin_Figure2_ROCscore_violin.png`
  - `umap_part11_magic_small.png`, `umap_part11_pca_small.png`
  - `umap_harmony.png`, `umap_bbknn.png`
  - `umap_Figure1B_broad_tissue.png`, `umap_Figure1B_skin_only_polished.png`
- **`outputs/*.csv`** — metrics and marker tables (created on run), e.g.
  - `extra_clustering_metrics.csv`, `denoise_metrics_compare.csv`
  - `batch_integration_metrics_rounded.csv`
  - `compare_supptable3_metrics_top100.csv`
- **`/data`** (not tracked) — place the input H5AD here.

---

### Run in Colab
1. Click the **Open in Colab** badge above.
2. Upload `cleaned_processed_frogtail.h5ad` to 'content' folder.
3. Run all cells. Figures/CSVs will be written to `figures/` and `outputs/`.


