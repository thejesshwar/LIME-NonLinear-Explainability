# 🔍 Demystifying Black Box Models with LIME

### **Project Overview**
Trust is the bottleneck of AI adoption. Modern black box models like Random Forests and Deep Neural Networks achieve high accuracy but sacrifice interpretability. This project explores **Local Interpretable Model Agnostic Explanations** to bridge this gap.

Using synthetic non linear data, this repository demonstrates how LIME approximates complex global decision boundaries with interpretable local surrogates.

### 📂 Repository Structure
* **`reports/`**: Contains the formal academic report covering the theoretical framework and mathematical formulations.
* **`notebooks/`**: Contains the implementation code.
  * *Note:* The notebook includes an **Extended Analysis** featuring Stability Tests and Hyperparameter Tuning that verifies the robustness of the results in the report.

### 📊 Key Results

#### 1. Visualizing Local Linearity

*LIME successfully fits a linear decision boundary to the non linear manifold of the Random Forest.*

#### 2. Robustness & Stability
A common critique of LIME is its stochastic nature. We conducted a stability analysis by running the explainer **10 times** on the same instance.
* **Result:** The standard deviation of feature weights was **< 0.01** confirming that the explanations are stable and reproducible.

#### 3. Hyperparameter Sensitivity
We analyzed how the Kernel Width affects the locality of the explanation.
* **$\sigma = 0.75$:** Captures local nuance.
* **$\sigma = 5.0$:** Over smooths the boundary, reverting to a global average that fails to capture non linearities.

### 🛠️ Tech Stack
* **Core:** Python 3.10+
* **Libraries:** `lime`, `scikit-learn`, `numpy`, `matplotlib`, `mlxtend`

### 🚀 How to Run
1. Clone the repo:
   ```bash
   git clone [https://github.com/YOUR_USERNAME/LIME-NonLinear-Explainability.git](https://github.com/YOUR_USERNAME/LIME-NonLinear-Explainability.git)
