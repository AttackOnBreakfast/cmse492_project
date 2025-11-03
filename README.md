# Predicting Exfoliation Energy of 2D Materials

**Author:** Artemiy Filippov  
**Course:** CMSE 492 – Machine Learning, Michigan State University (Fall 2025)

---

## 🧭 Project Overview

This project aims to predict the **exfoliation energy** of layered 2D materials using machine learning techniques.  
The dataset is sourced from the **MatBench JDFT-2D benchmark** (via the [Matminer](https://hackingmaterials.lbl.gov/matminer/) library), which contains density-functional-theory (DFT)–calculated exfoliation energies for a diverse set of compounds.  

By extracting structural features (such as density, packing fraction, and atomic volume per atom) and training regression models, this project seeks to explore how physical and geometric properties influence exfoliation energy — a key factor in determining how easily 2D materials can be isolated from their bulk counterparts.

---

## 🧩 Repository Structure

```plaintext
cmse492_project/
│
├── README.md                   <- Project overview and setup instructions
├── .gitignore                  <- Excludes unnecessary files from version control
├── requirements.txt            <- Python dependencies
│
├── data/
│   ├── raw/                    <- Original/unprocessed data (excluded from git)
│   └── processed/              <- Cleaned or featurized datasets
│
├── notebooks/
│   └── exploratory/
│       └── materials_eda.ipynb <- Main Jupyter notebook for data loading, EDA, and baseline model
│
├── src/
│   ├── preprocessing/           <- Future scripts for data cleaning and feature engineering
│   ├── models/                  <- Machine learning models (baseline + advanced)
│   └── evaluation/              <- Metrics and cross-validation scripts
│
├── figures/                    <- Generated visualizations (EDA, correlations, baseline results)
│
└── docs/                       <- LaTeX proposal, reports, and documentation

## ⚙️ Setup Instructions

This project runs directly in **VS Code** with any Python version ≥ 3.10 — no virtual environment or Conda setup is required.  
Once you clone the repository, you can open it in VS Code and run everything immediately.

1. **Clone the repository**  
   Open a terminal and run:  
   `git clone https://github.com/AttackOnBreakfast/cmse492_project.git`  
   `cd cmse492_project`

2. **Install required packages**  
   From the integrated terminal in VS Code, install dependencies with:  
   `pip install -r requirements.txt`  
   If the file is missing, install the essentials manually:  
   `pip install matminer pandas seaborn matplotlib scikit-learn missingno`

3. **Open and run in VS Code**  
   - Launch VS Code  
   - Go to **File → Open Folder…** and select `cmse492_project/`  
   - Open the notebook at `notebooks/exploratory/materials_eda.ipynb`  
   - Run all cells using the **Jupyter extension**

4. **Generated figures**  
   All plots (distributions, heatmaps, scatterplots, etc.) are automatically saved to the `figures/` directory.  
   If the folder doesn’t exist, it will be created when the notebook runs.

## 📊 Current Progress

The project is fully set up and functional within the defined repository structure.  
A comprehensive exploratory analysis has been completed, supported by both feature engineering and baseline modeling.  

- **Dataset Acquisition:**  
  Successfully loaded the `matbench_jdft2d` dataset from Matminer, which contains density-functional-theory (DFT)–calculated exfoliation energies for 636 layered 2D materials.  

- **Feature Engineering:**  
  Extracted structural descriptors using `DensityFeatures`, including density, packing fraction, and atomic volume per atom. These features capture key geometric and physical attributes relevant to exfoliation energy prediction.  

- **Exploratory Data Analysis (EDA):**  
  Produced a complete suite of visualizations, now stored in the `figures/` directory:
  - Exfoliation energy distribution  
  - Feature correlation heatmap  
  - Exfoliation energy vs. density scatterplot  
  - Pairwise feature relationships  
  - Missing-value visualization  

- **Baseline Model:**  
  Implemented a linear regression model as an initial benchmark to predict exfoliation energy from the extracted features.  
  Performance was evaluated using **Mean Absolute Error (MAE)** and **Root Mean Squared Error (RMSE)**, and results were visualized through an actual-vs-predicted scatter plot.  

- **Next Steps:**  
  The next development phase will expand the modeling approach by introducing non-linear algorithms such as Random Forest Regressors and Neural Networks.  
  Future work will include hyperparameter tuning, cross-validation, and model comparison to improve predictive accuracy beyond the baseline.


