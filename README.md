# DS340W-Project-by-Haren-Anand  
## Macro + Technical ML Trading on U.S. Tech Stocks  
**DS 340W — The Impact of Macroeconomic Variables on Quantitative Trading Performance Across Market Cycles** 
**Author:** Haren Anand • **Semester:** Fall 2025  

This repository contains my DS 340W final project testing whether **macroeconomic variables** improve **ML-based trading strategies** for large U.S. technology stocks across **5-, 10-, and 20-day** prediction horizons.

I compare:

- **Tech-only models:** price/volume-based technical indicators only  
- **Tech + Macro models:** technical indicators + macroeconomic variables  

The objective is to measure when macro-aware models outperform technical-only strategies in both:
- **prediction quality** (error metrics)
- **trading performance** (strategy outcomes)

---

## Dataset (Included in Repo)

All required data is included in this repository:

- Main combined dataset (macro + technical):
  - `data/final_dataset/macro_filled_final.xlsx`

- Per-stock feature exports:
  - `data/final_dataset/AAPL_features.csv`
  - `data/final_dataset/ADBE_features.csv`
  - `data/final_dataset/AMD_features.csv`
  - `data/final_dataset/CRM_features.csv`
  - `data/final_dataset/MSFT_features.csv`
  - `data/final_dataset/NOW_features.csv`
  - `data/final_dataset/NVDA_features.csv`
  - `data/final_dataset/ORCL_features.csv`

---

## Repository Layout

```text
DS340W-Project-by-Haren-Anand/
├── data/
│   └── final_dataset/
│       ├── macro_filled_final.xlsx
│       ├── AAPL_features.csv
│       ├── ADBE_features.csv
│       ├── AMD_features.csv
│       ├── CRM_features.csv
│       ├── MSFT_features.csv
│       ├── NOW_features.csv
│       ├── NVDA_features.csv
│       ├── ORCL_features.csv
│       └── .gitkeep
├── reference_code/
├── DS340W_Final.ipynb
├── requirements.txt
└── README.md


---

## Run in Google Colab (

1) Open `DS340W_Final.ipynb` in Google Colab.

2) In Colab, go to **Files** (left sidebar) → **Upload** and upload:
- `macro_filled_final.xlsx`

3) Run the first setup cell in the notebook to install required packages:

```python
import sys, subprocess

packages = [
    "numpy",
    "pandas",
    "matplotlib",
    "seaborn",
    "scikit-learn",
    "catboost",
    "openpyxl",
    "xlrd"
]

for pkg in packages:
    subprocess.check_call([sys.executable, "-m", "pip", "install", pkg])

print("Finished installing packages.")

