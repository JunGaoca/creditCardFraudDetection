# Credit Card Fraud Detection

## Business Goal
Credit card fraud causes significant financial losses each year. An effective fraud detection model enables early fraud prevention, reduces financial losses, and improves customer trust. This project helps financial institutions balance security and usability, improving fraud detection without unnecessary disruptions to legitimate transactions.

## Data Sources
The dataset originates from an [IEEE competition](https://www.kaggle.com/competitions/ieee-fraud-detection/data) and was supplied by Vesta Corporation.

The data is broken into two files *identity* and *transaction*, which are joined by *TransactionID*. 

The dataset comprises 590,540 transactions, of which 20,663 are marked as fraudulent — around 3.5% of the total. The Transactions table includes 394 features, 14 of which are categorical; while the Identity table contains 41 features, with 17 being categorical. 

## Project Structure
- **original_data:** Contains the original zip archive along with the extracted CSV files.
- **process_data:** Stores the merged dataset after data preparation, exploratory data analysis (EDA), and feature engineering.
- **Notebooks:**
    - *[Data Prepration and Feature Engineering](https://github.com/JunGaoca/creditCardFraudDetection/blob/main/credit-card-fraud-detection.ipynb)*
    - *[Model Evaluations and Performance Metrics Analysis](https://github.com/JunGaoca/creditCardFraudDetection/blob/main/credit-card-fraud-detection-part2.ipynb)*

#### Note: This repository requires Git Large File Storage (LFS) for uploading certain data files. The setup will be completed at a later stage.