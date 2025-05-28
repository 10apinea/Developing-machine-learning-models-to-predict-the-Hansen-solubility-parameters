
## 🧪 Hansen Solubility Parameters – Machine Learning Approach

This project applies machine learning to predict Hansen solubility parameters (HSP) — dispersion (δd), polarity (δp), and hydrogen bonding (δh) — using a Lasso linear regression model. HSPs are critical for understanding solubility in materials science, pharmaceuticals, and formulation chemistry.

### 📋 Overview

* **Goal**: Develop a predictive ML model for HSP using open-source tools and descriptors from molecular structure.
* **Approach**: Python-based Lasso regression using molecular fingerprints (Morgan & MACCS), sigma profiles, electrostatic properties, and shape/size features.
* **Tools**: Jupyter Notebook, RDKit, Scikit-learn, NumPy, Pandas, Matplotlib.

### 📊 Dataset

* Sourced from Sanchez-Lengeling et al.
* Includes 193 solvent molecules (with a subset of 87 for comparison).
* Descriptors: SMILES, charge density, σ-profiles, dipole moments, volume, etc.

### 🧠 ML Techniques

* **Model**: Lasso regression with leave-one-out cross-validation.
* **Evaluation**: R², MAE, and RMSE across different HSP components.
* **Findings**: δh predictions were most accurate. Model performance was stronger on the smaller dataset (n=87).

### 🔍 Key Results

| Dataset | δd R² | δp R² | δh R² |
| ------- | ----- | ----- | ----- |
| n = 193 | 0.32  | 0.54  | 0.77  |
| n = 87  | 0.56  | 0.67  | 0.86  |

### ⚠️ Limitations

* SMILES inconsistencies may reduce model accuracy.
* Dataset bias (e.g., molecular weight distributions) may affect results.
* Kernel Ridge regression attempted but not finalised.

### 🔭 Future Work

* Explore other algorithms (e.g. Gaussian Processes, RGF).
* Transition to SELFIES for better molecular representation.
* Scale up datasets and consider nanoparticle interactions.
* Improve cheminformatics accessibility and standardisation.

