### README: **CIBMTR Post-HCT Complications Risk Prediction**

---

#### **Project Title**
**Post-Hematopoietic Cell Transplantation (HCT) Complications Risk Prediction**

---

#### **Project Overview**
This project is designed to predict risk scores for complications following hematopoietic cell transplantation (HCT) using machine learning models. By leveraging the **CIBMTR** datasets, this project aims to provide accurate and interpretable risk predictions to support clinicians in proactive patient care.

The primary focus is on building a robust model pipeline using XGBoost and scikit-survival to predict post-HCT complications. The results are submitted to Kaggle's competition platform, ensuring scalability and adaptability to real-world use cases.

---

#### **Objectives**
- **Predict Risk Scores:** Develop a machine learning model to predict the likelihood of post-HCT complications.
- **Optimize Model Performance:** Utilize advanced evaluation metrics such as the Concordance Index to measure model accuracy.
- **Generate Insights:** Provide interpretable predictions to guide clinical decision-making.

---

#### **Datasets**
- **Training Data:** `preprocessed_train.csv`
- **Test Data:** `preprocessed_test.csv`

Both datasets contain anonymized patient data, including clinical features, demographic information, and survival outcomes.

---

#### **Workflow**
1. **Data Preprocessing**
   - Load and inspect the preprocessed training and test datasets.
   - Handle missing values, standardize features, and engineer additional inputs if needed.

2. **Model Training**
   - Train an **XGBoost regression model** to predict risk scores.
   - Use the survival time and event indicators as targets.

3. **Evaluation**
   - Use metrics such as the **Concordance Index** to evaluate survival prediction performance.

4. **Generate Submission**
   - Generate predictions on the test dataset and format them as required for Kaggle submission.

---

#### **Key Features**
- **Machine Learning Models:** XGBoost is used for efficient and interpretable risk prediction.
- **Survival Analysis:** `scikit-survival` provides metrics and methods tailored for survival data.
- **Scalable Workflow:** The pipeline is modular, allowing further enhancements with models like LightGBM or CatBoost.

---

#### **Dependencies**
The project requires the following Python packages:
```plaintext
numpy
pandas
scikit-learn
xgboost
scikit-survival
```

Install all dependencies via:
```bash
pip install -r requirements.txt
```

---

#### **How to Run**
1. **Clone the Repository**
   ```bash
   git clone https://github.com/YourUsername/CIBMTR-Survival-Predic.git
   cd CIBMTR-Survival-Predic
   ```

2. **Set Up the Environment**
   Create a virtual environment and activate it:
   ```bash
   python3 -m venv venv
   source venv/bin/activate
   pip install -r requirements.txt
   ```

3. **Run the Code**
   Train the model and generate predictions:
   ```bash
   python CIBMTR_XGBoost_Survival_Model.py
   ```

4. **Generate Kaggle Submission**
   After running the script, the predictions will be saved to a file named `submission.csv`.

---

#### **Evaluation Metrics**
The project uses the **Concordance Index**, a survival-specific metric, to measure the quality of predictions:
- A higher value indicates better predictive performance.
- The Concordance Index also accounts for censored survival data, making it ideal for HCT outcomes.

---

#### **File Structure**
```plaintext
CIBMTR-Survival-Predic/
│
├── Kaggle comp/                 # Contains the main notebook and data files
│   ├── CIBMTR_XGBoost_Survival_Model.ipynb
│   └── submission.csv           # Final Kaggle submission file
│
├── requirements.txt             # List of dependencies
├── README.md                    # Project overview
```

---

#### **Future Enhancements**
1. **Additional Models:** Experiment with LightGBM, CatBoost, and ensemble methods.
2. **Feature Engineering:** Incorporate domain-specific knowledge for better features.
3. **Explainability:** Use SHAP or similar techniques to explain predictions.
4. **Fairness:** Ensure equitable predictions across demographic groups.

---

#### **License**
This project is licensed under the MIT License.
