**Credit Card Fraud Detection:**
- This project focuses on detecting fraudulent credit card transactions using machine learning techniques. It applies data preprocessing, visualization, and classification models to identify fraud effectively.

**Overview:**
- Credit card fraud detection is a highly imbalanced classification problem where fraudulent transactions are rare compared to legitimate ones.
- This project uses:
  - Data preprocessing & normalization
  - Exploratory Data Analysis (EDA)
  - Machine Learning models: Decision Tree, Support Vector Machine (SVM)
  - Evaluation using ROC-AUC score

**Installation:**
- Install the required dependencies:
  - Scikit-learn 
  - Pandas
  - Matplotib

**Project Workflow:**

1. Data Loading:
    -raw_data = pd.read_csv(url)
   
2. Exploratory Data Analysis:
    - Visualize class imbalance using a pie chart
    - Analyze feature correlations with the target variable

3. Data Preprocessing
    - Standardization using StandardScaler
    - Normalization using L1 norm
    - Train-test split (70% training, 30% testing)

4. Handling Class Imbalance
    - Used sample weighting:
    - compute_sample_weight('balanced', y_train)

6. Model Training
    - Decision Tree
        - DecisionTreeClassifier(max_depth=4, random_state=35)
    - Support Vector Machine (SVM)
        - LinearSVC(class_weight='balanced', loss="hinge")
  
7. Model Evaluation
    -  Metric used: ROC-AUC Score
        -roc_auc_score(y_test, y_pred)

**Visualization:**
- Class distribution (Fraud vs Normal)
- Feature correlation with target variable

**Key Learnings:**
- Handling imbalanced datasets is critical
- Feature scaling improves model performance
- ROC-AUC is a better metric than accuracy for fraud detection
- Simpler models can still perform well with proper preprocessing
 
**Notes:**
- Replace "Enter url of Dataset" with the actual dataset link
- Ensure the dataset structure matches expected columns
