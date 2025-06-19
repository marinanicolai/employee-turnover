# Problem Scenario: Predicting Employee Turnover

**Company:** Portobello Tech  
**Goal:** Predict employee turnover using ML models.

Portobello Tech is an app innovator aiming to predict employee turnover. The company regularly tracks employee information, such as:

- Number of projects
- Monthly working hours
- Time spent at the company
- Promotions in the last 5 years
- Salary level

This data also includes employee satisfaction and evaluation scores. HR uses this data to identify patterns and predict which employees might leave.

---

## 🎯 Tasks for the ML Developer

You have been assigned by the HR department to:

1. ✅ **Perform data quality checks**
   - Check for missing values in the dataset.

2. 📊 **Understand contributing factors**
   - Use Exploratory Data Analysis (EDA) to discover which features affect employee turnover most.

3. 🔥 **Draw important plots**
   - Heatmap of correlation matrix for numerical features
   - Distribution plot for:
     - `satisfaction_level`
     - `last_evaluation`
     - `average_montly_hours`
   - Bar plot of `number_project` vs. `left` (who stayed vs. who left)

4. 🧩 **Cluster employees who left**
   - Use `satisfaction_level`, `last_evaluation`, and `left` columns.
   - Apply K-Means clustering into 3 groups.
   - Analyze and describe each cluster.

5. ⚖️ **Handle class imbalance**
   - Use **SMOTE** to upsample the minority class.
   - Convert categorical columns using `get_dummies()`:
     - Separate categorical and numerical columns
     - Apply transformation
     - Combine both again
   - Perform stratified train-test split (80:20, `random_state=123`).

6. 🤖 **Train ML models with 5-Fold Cross-Validation**
   - Logistic Regression
   - Random Forest Classifier
   - Gradient Boosting Classifier
   - Plot classification reports for each.

7. 🏆 **Evaluate and choose the best model**
   - Plot ROC Curve and calculate AUC score for each model.
   - Generate and compare confusion matrices.
   - Decide whether **Recall** or **Precision** matters more.
   - Justify chosen metric.

8. 💡 **Suggest retention strategies**
   - Use the best model to predict turnover probability on test data.
   - Categorize employees by risk zone and give strategy for each:

| **Zone**         | **Score Range** | **Color** |
|------------------|------------------|-----------|
| Safe Zone        | Score < 20%      | 🟩 Green  |
| Low-Risk Zone    | 20% < Score < 60%| 🟨 Yellow |
| Medium-Risk Zone | 60% < Score < 90%| 🟧 Orange |
| High-Risk Zone   | Score > 90%      | 🟥 Red    |

---

## 📥 Input Dataset: [Dataset]

The following data will be used to train the model:

| Column Name            | Description                                                   |
|------------------------|---------------------------------------------------------------|
| `satisfaction_level`   | Satisfaction level at the job of an employee                  |
| `last_evaluation`      | Evaluation score (0–1) received by an employee                |
| `number_project`       | Number of projects the employee worked on                     |
| `average_montly_hours` | Average hours worked per month                                |
| `time_spend_company`   | Number of years spent at the company                          |
| `Work_accident`        | 0 = no accident, 1 = had an accident                          |
| `left`                 | 0 = stayed, 1 = left the company                              |
| `promotion_last_5years`| 1 = got promoted in last 5 years, 0 = no promotion            |
| `Department`           | Department name                                               |
| `salary`               | Salary level in USD                                           |

---

