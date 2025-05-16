# Credit Card Fraud Detection

## Business Goal
Credit card fraud causes significant financial losses each year. An effective fraud detection model enables early fraud prevention, reduces financial losses, and improves customer trust. This project helps financial institutions balance security and usability, improving fraud detection without unnecessary disruptions to legitimate transactions.

## Data Sources
The dataset originates from an [IEEE competition](https://www.kaggle.com/competitions/ieee-fraud-detection/data) and was supplied by Vesta Corporation.

The data is broken into two files *identity* and *transaction*, which are joined by *TransactionID*. 

The dataset comprises 590,540 transactions, of which 20,663 are marked as fraudulent — around 3.5% of the total. The Transactions table includes 394 features, 14 of which are categorical; while the Identity table contains 41 features, with 17 being categorical. 

## Project Structure
- **original_data:** Holds the original ZIP archive and the extracted CSV files. (Because of its large size, you can download the ZIP from the provided URL, unzip it, and place the files here.)
- **process_data:** Stores the merged dataset after data preparation, exploratory data analysis (EDA), and feature engineering. (Due to its large size, you can follow the notebook steps and save the generated txn_identity.csv file in this location.)
- **Notebooks:**
    - *[Data Prepration and Feature Engineering](https://github.com/JunGaoca/creditCardFraudDetection/blob/main/credit-card-fraud-detection.ipynb)*
    - *[Model Evaluations and Performance Metrics Analysis](https://github.com/JunGaoca/creditCardFraudDetection/blob/main/credit-card-fraud-detection-part2.ipynb)*

## Business Insights
- CatBoost and XGBoost offer the best trade-off between catching fraud (recall) and avoiding false alarms (precision), achieving the highest F1-scores.

- Logistic Regression and KNN have high recall but unacceptably low precision, leading to many false positives, which could result in poor customer experience and increased manual review cost and operational overhead.

## Business Recommendations
- Deploy XGBoost or CatBoost in production, as these models balance fraud detection and user experience better than others.

- Use Logistic Regression as a secondary monitoring tool, utilizing its high recall to flag potential fraud cases that other models might miss.

- Implement continuous monitoring of false positives and false negatives to refine model performance and reduce operational risk over time.

## Future Work
- Further refine CatBoost/XGBoost with grid or randomized search to enhance recall while maintaining acceptable precision.

- Leverage ensemble or stacking methods to improve recall and model robustness by capturing a wider variety of fraud patterns.

- Investigate deep learning approaches to further boost the performance and adaptability of the fraud detection pipeline.

## Tech Stack
- Python: pandas, NumPy, scikit-learn
- Data Visualization: Matplotlib, Seaborn
- Machine Learning Techniques: Linear Regression, Decision Trees, Random Forest, Gradient Boosting, XGBoost
- Model Evaluation Metrics: 
- Feature Engineering: One-Hot Encoding, Scaling