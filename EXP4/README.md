# Experiment 4: Binary Classification (Spam Classification)

## 🎯 Objective

To classify emails as **Spam** or **Ham** (non-spam) using **Logistic Regression** and **Support Vector Machines (SVM)**. We analyze the effectiveness of different SVM kernels and the impact of hyperparameter tuning on high-dimensional word frequency data.

## 📊 Dataset

- **Name**: Spambase Dataset
- **Features**: 57 continuous features representing word frequencies (e.g., "free", "money", "win") and character frequencies (e.g., "!", "$").
- **Target**: `label` (1 = Spam, 0 = Ham)
- **Samples**: 4,601 instances.

## 🛠️ Methodology

1. **Preprocessing**:
   - Scaled features using `StandardScaler` (Crucial for SVM convergence).
   - Stratified split (80/20) to maintain class balance in training and testing.
2. **EDA**:
   - Distribution analysis of target classes.
   - Correlation analysis to identify features most indicative of spam (e.g., character frequency of '$' and '!').
3. **Modeling & Tuning**:
   - **Logistic Regression**: Optimized `C`, `penalty` (L1/L2), and `solver`.
   - **SVM**: Evaluated Linear, Poly, RBF, and Sigmoid kernels. Optimized `C` and `gamma` for the best-performing kernel.
4. **Evaluation**:
   - 5-Fold Cross-Validation.
   - Metrics: Accuracy, Precision, Recall, F1-Score, and AUC-ROC.
   - Learning Curves for bias-variance diagnostics.

## 📈 Results

### Model Performance (Best Tuned)

| Model                   | Accuracy | Precision | Recall | F1 Score | AUC  |
| :---------------------- | :------- | :-------- | :----- | :------- | :--- |
| **Logistic Regression** | 0.9262   | 0.9202    | 0.8898 | 0.9048   | 0.98 |
| **SVM (RBF Kernel)**    | 0.9207   | 0.9143    | 0.8815 | 0.8976   | 0.98 |

### SVM Kernel Comparison

| Kernel         | Accuracy   | F1 Score   | Training Time |
| :------------- | :--------- | :--------- | :------------ |
| **Linear**     | **0.9294** | **0.9093** | 0.41s         |
| **Polynomial** | 0.7796     | 0.6220     | 0.31s         |
| **RBF**        | 0.9273     | 0.9055     | 0.22s         |
| **Sigmoid**    | 0.8849     | 0.8528     | 0.32s         |

## 🖼️ Visualizations

- **Confusion Matrices**: Detailed check on false positives (important for spam filters).
- **ROC Curve Overlay**: Comparing the discriminative power of LogReg vs SVM.
- **Learning Curves**: Confirming that the models are well-generalized and not suffering from high variance.

## 🚀 How to Run

1. Ensure the dataset is in `../dataset/spambase_csv.csv`.
2. Run the notebook: `jupyter notebook notebooks/experiment4.ipynb`.
3. Results are logged in `notebooks/results_exp4.txt`.
