<img src="https://upload.wikimedia.org/wikipedia/commons/1/10/Columbia_University_1754.svg" width="400" valign="left">

<div align="center">
  
  # Single-Cell Profiling of Frog Tail Regeneration 🐸🧬
  **Identifying Regenerative Organizing Cells (ROC) in *Xenopus laevis***
  
  [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1ZEFRZO5GRudCBl7NQhhmSN5nyY40UvkT?usp=sharing)
</div>

---

## 👤 Author
**María Dolores Navarro Maturana (Lola)** — `mn3312`

## 🔬 Project Overview
This project presents an end-to-end computational pipeline to analyze single-cell RNA sequencing (scRNA-seq) data from the regenerating tail of *Xenopus laevis*. The primary biological objective is to computationally identify and characterize the **Regenerative Organizing Cell (ROC)** population and reproduce key findings (such as Figure 1B) from the original literature.

To ensure robustness, the pipeline systematically compares multiple computational strategies across the scRNA-seq workflow:
* **Clustering Algorithms:** Leiden vs. Louvain 
* **Marker Gene Discovery:** Wilcoxon Rank-Sum vs. Logistic Regression
* **Data Denoising:** MAGIC vs. PCA Low-Rank Approximations
* **Batch Effect Integration:** Harmony vs. BBKNN

## 📂 Repository Structure

* 📓 **`frog_and_tail.ipynb`**: The main Jupyter/Colab notebook. Fully reproducible pipeline from raw counts to final visualizations.
* 📄 **`project_report.pdf`**: Comprehensive final report summarizing the methodology, quantitative metrics, biological results, and conclusions.
* 📁 **`figures/`**: Auto-generated visualizations produced by the pipeline:
  * UMAP projections (`umap_Figure1_clustering.png`, `umap_Figure1B_skin_only_polished.png`, etc.)
  * Feature scoring and distributions (`violin_Figure2_ROCscore_violin.png`)
  * Batch integration & denoising comparisons (`umap_harmony.png`, `umap_part11_magic_small.png`, etc.)
* 📁 **`outputs/`**: Tabular data, statistical metrics, and marker tables generated during execution (e.g., `batch_integration_metrics_rounded.csv`, `compare_supptable3_metrics_top100.csv`).

## 🚀 Quick Start: Run in Colab

You can run the entire analysis in the cloud without local environment setup.

1. **Open the Notebook:** Click the [Open in Colab](https://colab.research.google.com/drive/1ZEFRZO5GRudCBl7NQhhmSN5nyY40UvkT?usp=sharing) badge at the top of this README.
2. **Download Required Data:**
   * Single-cell count data: [`cleaned_processed_frogtail.h5ad`](https://drive.google.com/file/d/1boRVP8VCptxxvfEEjlg8OW4xUFQbgn--/view)
   * Ground truth marker tables: [`aav9996_tables3.xlsx`](https://www.science.org/doi/full/10.1126/science.aav9996) (From *Science* Supplementary Materials).
3. **Upload to Colab:** Drag and drop both downloaded files into the `/content` folder in the Colab file explorer (left sidebar).
4. **Execute:** Run all cells (`Runtime` > `Run all`). The pipeline will automatically generate and save all plots into a `figures/` directory and CSVs into an `outputs/` directory within the Colab environment.

## 📚 References
* Aztekin, C., et al. (2019). *"Identification of a regeneration-organizing cell in the Xenopus tail."* Science.
