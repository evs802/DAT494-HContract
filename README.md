
🚀 **SED FITTING WITH MACHINE LEARNING**
=====================================
A machine learning approach to predicting **SED (Spectral Energy Distribution) fitting parameters** from **photometric magnitudes and redshift**. Traditional SED fitting methods rely on **template matching** or **Bayesian inference**, which can be **computationally expensive**. This project explores whether **Support Vector Machines (SVM) and Neural Networks (MLP)** can serve as **accurate and efficient alternatives**.

---

## 📂 **Project Overview**
🔹 **Goal**: Use ML models to predict SED parameters and explore alternatives to traditional fitting methods.  
🔹 **Data**: Photometric magnitudes from 8 filters (`F090W` - `F444W`) and redshift (`z_m1(EAZY)`).  
🔹 **Methods**: Implemented **SVM, Random Forest, and Neural Networks** for regression.  
🔹 **Evaluation**: Used **cross-validation, hyperparameter tuning, and overfitting analysis**.  

---

## 📊 **Dataset**
**Input Features**:  
✔️ Photometric magnitudes across 8 filters (`F090W, F150W, ..., F444W`)  
✔️ Redshift: `z_m1(EAZY)`

**Target Variables** (SED parameters):  
✔️ `log10(mass)`, `log10(age)`, `Log10(SSFR)`, `Log10(Tau)`, `A_V`

**Preprocessing Steps**:  
✔️ Filtered objects with `F444W ≤ 25` (brighter sources).  
✔️ Standardized inputs using `StandardScaler()`.  
✔️ Applied **train/test split (70/30)** for model evaluation.  

---

## 🚀 **Models Implemented**
| **Model**  | **Purpose**  | **Pros** | **Cons** |
|------------|-------------|----------|----------|
| **Random Forest** | Baseline Model | Easy to interpret, captures non-linearity | Lower accuracy, slower inference |
| **SVM (Support Vector Machine)** | Best Performing Model | High accuracy (R² ≈ 0.93), handles small datasets well | Computationally expensive, requires careful tuning |
| **Neural Network (MLP)** | Deep Learning Approach | Scalable, learns complex relationships | Requires large dataset, prone to overfitting |

---

## 📈 **Final Model Performance**
| **Model**  | **Test MSE** | **Test R²** |
|------------|-------------|-------------|
| **SVM** | **0.078** | **0.925** |
| **Neural Network** | **0.150** | **0.932** |

✔️ **SVM outperformed Neural Networks**, showing that traditional ML methods can be just as effective for structured astrophysical data.

---

## 🛠 **Installation & Setup**
### **1️⃣ Clone the Repository**
```bash
git clone https://github.com/yourusername/SED-ML.git
cd SED-ML
