# The Pattern of Probity vs. Plunder: Unmasking Fraud with Machine Learning

## Overview
A comprehensive exploration of financial fraud detection using supervised machine learning—a journey from data analysis to model evaluation, inspired by real-world transaction features.

## Dataset
- **Transactions:** 50 unique entries
- **Features:** TransactionID, Amount, TransactionType (Online/ATM/POS), IsInternational, CardHolderAge, FraudReported (target)
- **Balanced Labels:** 29 fraudulent, 21 legitimate

## Approach
1. **Data Quality Checks**
   - No missing values or duplicates

2. **Exploratory Analysis**
   - Scatter, pair, box, and violin plots: No strong one-feature separation for fraud detection
   - Distribution analysis shows overlap between fraudulent and legitimate transactions for amount and age

3. **Feature Engineering**
   - One-hot encoding of categorical variables
   - Exclusion of TransactionID from modeling
   - Defined target variable FraudReported (0/1)

4. **Model Training & Evaluation**
   - Algorithms: Logistic Regression, Decision Tree, Random Forest, SVM, KNN
   - Metrics: Accuracy, Precision, Recall (crucial for fraud), F1-Score

## Results

| Algorithm             | Accuracy | Precision | Recall | F1-Score |
|-----------------------|----------|-----------|--------|----------|
| Logistic Regression   | 26.67%   | 50.00%    | 27.27% | 35.29%   |
| Decision Tree         | 46.67%   | 71.43%    | 45.45% | 55.56%   |
| Random Forest         | 46.67%   | 71.43%    | 45.45% | 55.56%   |
| Support Vector Machine| 40.00%   | 66.67%    | 36.36% | 47.06%   |
| KNN                   | 26.67%   | 50.00%    | 27.27% | 35.29%   |

**Best Models:** Decision Tree and Random Forest

## Key Insights
- No single feature guarantees fraud detection; combinations and nonlinear relationships are crucial
- Recall is the priority—missing fraud can be costly
- Small dataset limits performance; expansion needed
- Feature engineering, model ensemble, and explainability tools (SHAP, LIME) are future steps

## Practical Implications
- Financial institutions: Multi-layered defense (2FA, rules, ML models)
- Data scientists: Focus on Recall, improve features, avoid overfitting
- Consumers: Vigilance and layered protection recommended

## Next Steps
- Expand data and introduce time/geographical features
- Hyperparameter tuning and advanced models (XGBoost, deep learning)
- Real-time deployment and model explainability

## Technical Stack
- Python 3, pandas, numpy, seaborn, matplotlib, scikit-learn
- Platform: Google Colab

## License
MIT

---

*Project demonstrates end-to-end ML workflow for fraud detection from data analysis to model deployment. Full Colab notebook available for code and visualizations.*

