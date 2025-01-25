# Jupyter Notebooks for Loan Default Prediction Model 📚

This folder contains the **Jupyter Notebooks** used for building, training, evaluating, and interpreting the **Loan Default Prediction Model**. The model aims to predict the likelihood of a loan being charged off (i.e., defaulting) based on factors like financial health and loan terms. The notebooks also include model interpretation using SHAP and LIME for explaining the model's predictions.

## Notebooks Overview

### 1. **loan_default_model.ipynb**
This notebook contains the complete process for building the loan default prediction model.

**Key steps covered**:
- **Data Preprocessing**: Cleaning the data, handling missing values, encoding categorical variables, and scaling numerical features.
- **Model Training**: Building and training a machine learning model (e.g., Random Forest, Logistic Regression, etc.) to predict loan default status (`Charged Off` vs `Current/Fully Paid`).
- **Model Evaluation**: Evaluating the model performance using classification metrics such as accuracy, precision, recall, F1-score, and ROC-AUC.
- **Hyperparameter Tuning**: If applicable, this section involves tuning the model to improve performance (e.g., GridSearchCV).

### 2. model_interpretation_lime.md
This notebook focuses on interpreting the model’s predictions using LIME (Local Interpretable Model-Agnostic Explanations).

Key steps covered:

- **LIME Explainer**: Using LIME to explain individual predictions by approximating the model locally around the prediction.
- 
- **LIME Visualization**: Visualizing which features had the most significant impact on a specific loan prediction. For the images, please visit the folder `Plot_images`.


## Running the Notebooks
To run the Jupyter notebooks, follow these steps:
1. **Activate your virtual environment** (if using one):
    ```bash
    source env/bin/activate  # Linux/macOS
    .\env\Scripts\activate   # Windows
    ```
2. **Launch Jupyter Notebook**:
    ```bash
    jupyter notebook
    ```
3. **Open the Notebooks**: From the Jupyter Notebook interface, navigate to the folder containing the notebooks and open the desired notebook (e.g., `loan_default_model.ipynb`).

## Prerequisites
Ensure you have the following dependencies installed:
- **pandas**: For data manipulation.
- **numpy**: For numerical operations.
- **scikit-learn**: For building and evaluating machine learning models.
- **lime**: For model interpretation using LIME.
- **matplotlib**, **seaborn**: For data visualization.

## License
This project is licensed under the MIT License - see the [LICENSE](https://github.com/hanh-analytics/Bank-loan-analysis/blob/67d03f16ca5d92e9102fda5c64670d9130ebd6c1/LICENSE) file for details.
