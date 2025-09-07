# FLUXNET GPP ML

This repository contains my final project for the **Technion Data Science program**.  
The project applies supervised and unsupervised machine learning methods to **FLUXNET2015 ecosystem flux data**, focusing on predicting **Gross Primary Productivity (GPP)** across diverse ecosystems.  

Models explored include linear regression (OLS, Ridge, Lasso), ensemble methods (Random Forest, XGBoost), and clustering (K-Means, Agglomerative, DBSCAN).

---

## Notebooks
Main notebook (open directly in Colab):  
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/gideon-szamet/fluxnet-gpp-ml/blob/main/notebooks/Final_ML_Project_Gideon_Sz.ipynb)

---

## Project Structure
```
.
├── notebooks/ # project notebooks
├── data/
│ ├── raw/ # raw data (not tracked in Git)
│ └── processed/ # processed data (not tracked in Git)
├── results/ # plots, metrics, and outputs
├── requirements.txt
└── README.md
```


---

## Quickstart

```bash
# 1. Clone the repo
git clone https://github.com/gideon-szamet/fluxnet-gpp-ml.git
cd fluxnet-gpp-ml

# 2. Create and activate a virtual environment
python -m venv .venv
.\.venv\Scripts\activate        # on Windows
# source .venv/bin/activate     # on Linux/Mac

# 3. Install dependencies
pip install -r requirements.txt

# 4. Launch Jupyter Lab / Notebook
jupyter lab
```

## Data

The project uses FLUXNET2015 daily flux data from six U.S. sites (grasslands, savannas, forests).

Data is not included in this repository due to licensing and size.

Place your input files under data/raw/ following the same structure expected in the notebook.

(Optional) Add a small synthetic sample dataset in data/raw/sample/ to demonstrate the schema.


## Results

- **Supervised learning:**  
  - Random Forest and XGBoost achieved the best performance, with **R² ≈ 0.90** and **RMSE ≈ 1.3 gC/m²/day**, predicting GPP from environmental and seasonal variables.  
  - Linear models explained ~80% of variance, but tree-based models captured non-linear interactions more effectively.  

- **Unsupervised learning:**  
  - Clustering algorithms (K-Means, Agglomerative, DBSCAN) revealed only weak groupings, reflecting continuous ecological gradients rather than discrete clusters.  




