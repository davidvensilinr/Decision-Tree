# Decision Tree Exploration

## Overview
This repository is dedicated to exploring and building **Decision Tree** models to solve various problem statements. The goal is to understand the versatility of Decision Trees in classification and regression tasks by applying them to different datasets.

## Projects

### 1. Loan Approval Prediction
**Directory**: `loanApproval/`

#### Problem Statement
The objective is to build a machine learning model to predict the **Loan Approval Status** (Approved/Rejected) for an applicant based on their profile and financial history.

#### Dataset
The dataset (`loan_data.csv`) includes the following features:
- **Demographics**: Gender, Marital Status, Education, Dependents.
- **Financials**: Applicant Income, Co-applicant Income, Loan Amount, Loan Amount Term, Credit History.
- **Property**: Property Area (Urban, Rural, Semiurban).
- **Target Variable**: `Loan_Status` (Y/N).

#### approach
1.  **Data Preprocessing**:
    -   Handled missing values (if any).
    -   Encoded categorical variables (Gender, Married, Education, etc.) using `LabelEncoder`.
    -   Split data into training (80%) and testing (20%) sets.
2.  **Model Building**:
    -   Used `DecisionTreeClassifier` from `scikit-learn`.
    -   Configured with `criterion='gini'` and `max_depth=5` to prevent overfitting.
3.  **Evaluation**:
    -   Evaluated model performance using:
        -   **Accuracy Score**
        -   **Confusion Matrix**
        -   **Classification Report**
4.  **Prediction**:
    -   Implemented a prediction system to take new user input and output the loan status.

#### Key Files
-   `loanApproval/Loan_Approval.ipynb`: Jupyter notebook containing the complete workflow from EDA to Model building.
-   `loanApproval/loan_approval.py`: Python script version of the workflow.
-   `loanApproval/dataset/`: Directory containing the dataset `loan_data.csv`.

## Dependencies
The project requires the following Python libraries:
-   `pandas`
-   `numpy`
-   `scikit-learn`
-   `matplotlib`
-   `seaborn`

To install the dependencies, run:
```bash
pip install -r requirements.txt
```

## Usage
1.  Clone the repository.
2.  Navigate to the project directory:
    ```bash
    cd loanApproval
    ```
3.  Run the python script:
    ```bash
    python loan_approval.py
    ```
    Or open and run the `Loan_Approval.ipynb` notebook in Jupyter/Colab.
