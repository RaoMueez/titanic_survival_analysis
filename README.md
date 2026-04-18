# Titanic_Survival_Analysis  
A comprehensive Data Science project analyzing the Titanic dataset to uncover survival patterns using Python, Pandas, Matplotlib, and Seaborn.

- **Phase 1:** Data Reconnaissance  

#### Dataset Features:
1. **PassengerId**: Unique ID for each passenger.
2. **Survived**: 0 = No, 1 = Yes (Target Variable).
3. **Pclass**: Ticket class (1, 2, or 3).
4. **Sex**: Male or Female.
5. **Age**: Age in years.
6. **SibSp**: Siblings or spouses aboard.
7. **Parch**: Parents or children aboard.
8. **Fare**: Passenger fare.
9. **Embarked**: Port of Embarkation (C, Q, S).

#### Data Insights:
- **Total Records:** 891 rows and 12 columns.
- **Missing Values:** 
  - `Age`: 177 missing.
  - `Cabin`: 687 missing.
  - `Embarked`: 2 missing.
- **Target Variable:** Data shows more non-survivors (0) than survivors (1).

- **Phase 2:** Data Cleaning & Imputation

Handled missing values for `Age` using `Pclass`-based imputation, missing `Embarked` values with mode and dropped high-null `Cabin`  column.

- **Phase 3:** Exploratory Data Analysis (EDA)  

#### Key Findings from EDA:
1. **Gender:** Females had a significantly higher survival rate than males.
2. **Social Class:** Pclass 1 passengers were prioritized over Pclass 3.
3. **Multivariate:** Even within females, those in Pclass 3 had lower survival chances compared to Pclass 1 & 2.

- **Phase 4:** Feature Engineering  

#### Key Findings:
- **FamilySize:** Combined `SibSp` and `Parch` to see the impact of traveling with family.
- **IsAlone:** Created a binary feature to identify solo travelers.
- **Title Extraction:** Extracting titles from the `Name` column to capture social status.

## Final Insights & Conclusions 

1. **Women & Children First:** It was proven that the "Women and Children First" policy was strictly followed. Females and children had a survival rate exceeding 70%.  
2. **Social Class Impact:** The data confirms that social status played a crucial role in survival. Passengers in 1st Class had significantly higher chances of survival compared to those in 3rd Class, highlighting the disparity in rescue priority.
3. **Family Size Dynamics:**

| Feature | Observation | Impact on Survival |
| :--- | :--- | :--- |
| **Gender** | Females had much higher survival rates compared to males. | Very High |
| **Pclass** | 1st Class passengers were prioritized; 3rd Class had most casualties. | High |
| **Family Size** | Small families (2-4) survived better than solo or very large families. | Medium |
| **Age** | Children had a higher priority, especially in higher classes. | Medium |

### Tools Used:
- Python (Pandas, NumPy)
- Visualization (Matplotlib, Seaborn)
- Jupyter Notebook