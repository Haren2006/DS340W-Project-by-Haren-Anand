# DS340W-Project-by-Haren-Anand
# Macro + Technical ML Trading on U.S. Tech Stocks  
**DS 340W — Quantitative Trading with Machine Learning and Macroeconomic Signals**  
**Author:** Haren Anand • **Semester:** Fall 2025

This repository contains my DS 340W final project on **how macroeconomic variables change the performance of ML-based trading strategies** for large U.S. technology stocks over **5-, 10-, and 20-day horizons**.

We compare:

- **Tech** models that use only price-based technical indicators  
- **Tech+Macro** models that also include key macroeconomic variables  

The goal is to see when **macro-aware models** actually beat classic purely technical strategies in terms of prediction quality and trading performance.

---

## 1. Quick Start — How to Run

### ✅ Recommended: Google Colab

1. **Open the notebook**
   - Go to this GitHub repo.  
   - Click **`DS340W_Final.ipynb`**.  
   - Click **“Open in Colab”** (or, in Colab: *File → Open notebook → GitHub* and paste the repo URL).

2. **Upload the `data` folder**
   - In Colab, open the **Files** panel (folder icon on the left).  
   - Create a folder called `data` if it doesn’t exist.  
   - Upload:
     - `data/final_dataset/macro_filled_final.xlsx`  
     - The 8 per-ticker files:
       - `AAPL_features.csv`, `ADBE_features.csv`, `AMD_features.csv`, `CRM_features.csv`,  
         `MSFT_features.csv`, `NOW_features.csv`, `NVDA_features.csv`, `ORCL_features.csv`
   - After upload, your Colab filesystem should look like:

     ```text
     /content/
         DS340W_Final.ipynb
         data/
             final_dataset/
                 macro_filled_final.xlsx
             AAPL_features.csv
             ADBE_features.csv
             AMD_features.csv
             CRM_features.csv
             MSFT_features.csv
             NOW_features.csv
             NVDA_features.csv
             ORCL_features.csv
     ```

3. **Run Cell 0 (install packages)**
   - At the very top of `DS340W_Final.ipynb`, run **Cell 0**:

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
     ```

   - Wait until you see: `Finished installing packages.`

4. **Run everything**
   - Go to **Runtime → Run all**, or run the remaining cells from top to bottom.  
   - All tables, equity curves, confusion matrices, and boxplots from the presentation will be generated.

---

### 💻 Alternative: Run Locally

1. **Clone and set up environment**

   ```bash
   git clone https://github.com/Haren2006/DS340W-Project-by-Haren-Anand.git
   cd DS340W-Project-by-Haren-Anand

   python3 -m venv venv
   source venv/bin/activate   # Windows: venv\Scripts\activate

   pip install -r requirements.txt
