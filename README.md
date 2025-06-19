# Employee Turnover

## Problem Scenario

Portobello Tech is an app innovator who has devised an intelligent way of predicting employee turnover within the company. It periodically evaluates employees' work details, including the number of projects they worked on, average monthly working hours, time spent in the company, promotions in the last five years, and salary level.

Data from prior evaluations shows the employees’ satisfaction in the workplace. The data could be used to identify patterns in work style and their interest in continuing to work for the company.

The HR Department owns the data and uses it to predict employee turnover. Employee turnover refers to the total number of workers who leave a company over time.

As the ML Developer assigned to the HR Department, you have been asked to create ML programs to:
- Perform data quality checks by checking for missing values, if any.
- Understand what factors contributed most to employee turnover at EDA.
- Perform clustering of employees who left based on their satisfaction and evaluation.
- Handle the left Class Imbalance using the SMOTE technique.
- Perform K-fold cross-validation model training and evaluate performance.
- Identify the best model and justify the evaluation metrics used.
- Suggest various retention strategies for targeted employees.

---

## Dataset Description

### Input Dataset: [Dataset 🔗](https://www.kaggle.com/datasets/liujiaqi/hr-comma-sepcsv)

| Column Name           | Description                                                                 |
|-----------------------|-----------------------------------------------------------------------------|
| satisfaction_level    | Satisfaction level at the job of an employee                                |
| last_evaluation       | Rating between 0 and 1, received by an employee at his last evaluation       |
| number_project        | The number of projects an employee is involved in                           |
| average_monthly_hours | Average number of hours in a month spent by an employee at the office       |
| time_spend_company    | Number of years spent in the company                                        |
| Work_accident         | 0 - no accident during employee stay, 1 - accident during employee stay     |
| left                  | 0 = stayed, 1 = left                                                         |
| promotion_last_5years | Number of promotions in the last 5 years                                    |
| Department            | Department to which an employee belongs to                                  |
| salary                | Salary in USD                                                               |

---

## Tasks to Perform

- Perform data quality checks by checking for missing values, if any.
- Understand what factors contributed most to employee turnover at EDA:
  - Draw a heatmap of the correlation matrix between all numerical features.
  - Draw distribution plots for:
    - Employee Satisfaction (`satisfaction_level`)
    - Employee Evaluation (`last_evaluation`)
    - Employee Average Monthly Hours (`average_monthly_hours`)
  - Draw a bar plot of employee project count (by `number_project`) and `left` status.
- Perform clustering:
  - Use `satisfaction_level`, `last_evaluation`, and `left`.
  - Apply K-means clustering into 3 clusters.
  - Interpret cluster results.
- Handle Class Imbalance using SMOTE:
  - Convert categorical columns using `get_dummies()`.
  - Separate categorical and numeric features.
  - Combine and split (80/20 stratified).
  - Apply SMOTE from `imblearn`.
- Model Training and Cross-Validation:
  - Train a Logistic Regression model, Random Forest, and Gradient Boosting using 5-fold CV.
  - Plot and compare classification reports.
- Model Evaluation:
  - Plot ROC/AUC for each model.
  - Generate and interpret confusion matrix.
  - Justify metric choice: Precision or Recall?
- Suggest Retention Strategies:
  - Predict probability of turnover for test data.
  - Categorize employees into:
    - **Green Zone** (< 20%)
    - **Yellow Zone** (20%–60%)
    - **Orange Zone** (60%–90%)
    - **Red Zone** (> 90%)
  - Recommend strategies for each group.

---

## Submission Instructions

- Preferred format: a **.pdf** of your Jupyter Notebook (with all output shown).
  - Save it from the menu: `File → Save and Export Notebook As → PDF`.
- Alternate format: submit the **.py** file + a separate output file.
- Submit via the "Start Assignment" button, drag file(s), and click Submit.

---

