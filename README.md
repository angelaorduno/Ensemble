# 🌳 Tree-Based Ensemble Models for Obesity Risk

This project builds and evaluates **tree-based classification models** for the Kaggle competition **“Multi-Class Prediction of Obesity Risk.”** The notebook includes **EDA**, **model training**, **interpretation**, and **Kaggle submission file generation** for:

- ✅ Decision Tree  
- ✅ Bagging (Bootstrap Aggregating)  
- ✅ Random Forest  
- ✅ Gradient Boosting  

A custom **pink → purple** visualization theme is used throughout the EDA and evaluation plots.

---

## 🎯 Project Goals

1. Perform targeted EDA for a multi-class classification dataset  
2. Train and evaluate four tree-based models  
3. Interpret model performance using Accuracy, Macro F1, and class-level metrics  
4. Create **separate Kaggle submission files for each model**  
5. Produce visuals to support interpretability:
   - Decision tree structure plot
   - Feature importance (RF + Boosting)
   - Averaged feature importance (Bagging)

---

## 📦 Dataset

**Source:** Kaggle competition dataset  
**Files:**
- `train.csv` → labeled training set  
- `test.csv` → unlabeled test set used for Kaggle submission  

**Target column:** `NObeyesdad`  
**ID column:** `id`

---

## 🧪 Methods & Models

### 1) Decision Tree
- Baseline model for interpretability and rule-based structure
- Visualized using `sklearn.tree.plot_tree()`

### 2) Bagging (Bootstrap Aggregating)
- Fits many trees on bootstrap samples
- Aggregates predictions by majority vote
- Visualized using **averaged feature importance across trees**

### 3) Random Forest
- Bagging + random feature subsampling per split
- Visualized using **feature importance**

### 4) Gradient Boosting
- Sequential tree building where each tree corrects prior errors
- Visualized using **feature importance**

---

## 📊 Evaluation Metrics

Models are evaluated using:
- **Accuracy**
- **Macro F1-score** (important for multi-class balance)
- `classification_report` (precision/recall/F1 per class)
- Confusion matrix (optional visuals)

---

## 🎨 Visual Theme

A custom **pink → purple** color palette is applied globally for:
- EDA plots
- Heatmaps (correlation + missingness maps)
- Confusion matrices
- Feature-importance plots

---

## 🗂️ Outputs

The notebook generates **four Kaggle submission files**:

- `submission_dt.csv`
- `submission_bag.csv`
- `submission_rf.csv`
- `submission_gb.csv`

Each submission contains:
- `id`
- predicted `NObeyesdad`

---

## ▶️ How to Run

### Option A — Google Colab (recommended)
1. Open the notebook in Colab
2. Mount Google Drive (already included in the notebook)
3. Set your working directory to the folder containing `train.csv` and `test.csv`
4. Run all cells top to bottom

### Option B — Local Jupyter
1. Place `train.csv` and `test.csv` in your project directory
2. Update or remove the Colab Drive mounting code
3. Run the notebook

---

## ✅ Requirements

Core libraries used:

- Python 3.9+
- pandas, numpy
- matplotlib, seaborn
- scikit-learn

Install (example):

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
