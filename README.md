# 🧠 Employee Attrition Insight & Prediction App  

## 📋 Project Overview  
This project focuses on understanding and predicting **employee attrition** using data analytics, statistical validation, and machine learning techniques.  
It provides HR teams with actionable insights to improve **employee retention**, **work satisfaction**, and **productivity**.  

The solution integrates:  
- **Python** → EDA, Statistical Testing, and Predictive Modeling  
- **Power BI** → Interactive Visualization  
- **Streamlit** → Model Deployment (Web App Interface)  

---

## 🎯 Business Objective  
1. Identify key factors influencing employee attrition.  
2. Perform detailed exploratory analysis to understand behavioral patterns.  
3. Statistically validate assumptions using **Hypothesis Testing**.  
4. Build and compare machine learning models to predict attrition probability.  
5. Visualize insights using Power BI for decision-makers.  

---

## 🧩 Dataset Information  

| Feature | Description |
|----------|-------------|
| `satisfaction_level` | Employee satisfaction score (0–1) |
| `last_evaluation` | Last performance evaluation score |
| `number_project` | Total projects assigned |
| `average_montly_hours` | Average monthly working hours |
| `time_spend_company` | Tenure in years |
| `Work_accident` | 1 = Had accident, 0 = No accident |
| `promotion_last_5years` | 1 = Got promoted, 0 = Not promoted |
| `department` | Department name |
| `salary` | Salary level: low / medium / high |
| `left` | Target variable: 1 = Left, 0 = Stayed |

📊 **Total Employees:** 15,000  
📈 **Overall Attrition Rate:** 24%  

---

## 🔍 Exploratory Data Analysis (EDA)  

**Key Observations:**  
- Attrition is highest among **low-salary employees (≈52%)**.  
- **Satisfaction Level** below 0.5 correlates strongly with attrition.  
- Employees with **no promotion in the last 5 years** show higher churn.  
- **Working hours:** Attrition peaks at both low (<150) and high (>280) monthly hours.  
- **Departments:** HR, Technical, and Support departments face the most attrition.  

**Visual Insights (Power BI Dashboard):**  
- **KPIs Displayed:** Total Employees, Attrition Rate, Avg Monthly Hours, Avg Satisfaction.  
- **Charts Include:**  
  - Attrition by Salary, Department, Projects, Promotions.  
  - Satisfaction trend by Evaluation Score.  
  - Attrition vs Average Monthly Hours.  

---

## 🧪 Hypothesis Testing  

| Hypothesis | Test Used | p-value | Result | Interpretation |
|-------------|------------|----------|----------|----------------|
| Salary affects attrition | Chi-Square | < 0.05 | Reject H₀ | Salary has significant effect on attrition |
| Average monthly hours influence attrition | t-test | < 0.05 | Reject H₀ | Workload impacts employee retention |
| Promotion status affects attrition | Chi-Square | < 0.05 | Reject H₀ | Lack of promotion drives attrition |

📌 **Conclusion:** Salary, workload, and promotions significantly influence attrition.  

---

## 🤖 Machine Learning Model  

### 🧱 Steps Performed  
1. Data Preprocessing – Encoding categorical features, scaling numerical ones.  
2. Train-Test Split – 80:20 ratio.  
3. Model Training – Logistic Regression, Random Forest, XGBoost.  
4. Evaluation Metrics – Accuracy, Precision, Recall, Confusion Matrix.  
5. Hyperparameter Tuning – Used RandomizedSearchCV for optimization.  

### 🧮 Model Comparison  

| Model | Accuracy | Comments |
|--------|-----------|-----------|
| Logistic Regression | 85% | Interpretable baseline model |
| Random Forest | **88%** | Best accuracy, stable results |
| XGBoost (Tuned) | 88% | Similar accuracy; no major gain post tuning |

✅ **Final Choice:** **Random Forest Classifier** (high accuracy + interpretability)  

### 📊 Feature Importance  
1. Satisfaction Level  
2. Average Monthly Hours  
3. Salary  
4. Number of Projects  
5. Promotion in Last 5 Years  

---

## 💡 Power BI Dashboard Highlights  

The **Employee Attrition Dashboard** presents:  
- Total Employees: **15K**  
- Attrition Rate: **0.24 (24%)**  
- Avg Monthly Hours: **201.05 hrs**  
- Avg Satisfaction: **0.61**  

### Key Insights  
- Employees with **low satisfaction and low salary** form the largest attrition segment.  
- Departments like **HR, Support, and Technical** show higher churn.  
- **Promotions and balanced workloads** correlate with better retention.  

---

## 🌐 Streamlit App (Deployment Component)  

### App Features  
- Upload employee dataset (CSV) for prediction.  
- Interactive filters: Salary, Department, Tenure.  
- Predict attrition probability for individual employees.  
- Visualize key metrics (satisfaction, workload, projects).  

### Run Locally  
```bash
streamlit run app.py
```

### Project Structure  
```
📁 Employee_Attrition_Project
│
├── 📄 Employee_Attrition_model.ipynb   # Python notebook (EDA + ML)
├── 📊 PowerBI_Dashboard.pbix           # Power BI file
├── 💻 app.py                           # Streamlit web app
├── 📁 data                             # Dataset folder
├── 📁 models                           # Saved ML models (.pkl)
└── 📄 README.md                        # Documentation
```

---

## 🧰 Tech Stack  

| Category | Tools Used |
|-----------|-------------|
| Programming | Python |
| Data Analysis | Pandas, NumPy, Matplotlib, Seaborn |
| Machine Learning | Scikit-learn, XGBoost |
| Statistics | Scipy (t-test, chi-square) |
| Visualization | Power BI, Streamlit |
| Version Control | Git, GitHub |

---

## 📈 Key Business Learnings  
- Employee retention is **driven by satisfaction, recognition, and balance**.  
- Overworking and underpaying employees increases churn risk.  
- Regular promotions and fair workload distribution reduce attrition.  
- Data-driven HR decisions can save recruitment and training costs.  

---

## 🚀 Future Enhancements  
- Deploy predictive API for HR systems.  
- Integrate real-time HR data pipeline.  
- Add SHAP explainability for feature interpretation.  
- Automate alerts for high attrition risk employees.  

---

## 👨‍💻 Author  
**Biswanath Bhuyan**  
📊 AI/ML Engineer| Data Scientiat  
📧   
🌐 [LinkedIn](https://www.linkedin.com/in/biswanath-bhuyan/) • [GitHub](https://github.com/Biswanath-bis)
