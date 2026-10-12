# Credit_Risk_Analysis-Loan-Scoring
This project develops and evaluates machine-learning models to classify loan applicants according to their observed credit risk. The goal is to explore how applicant characteristics and loan information can support risk assessment and how prediction thresholds affect potential business costs.

Two classification algorithms were evaluated: 
Logistic Regression and Random Forest.


 Business Problem
   
Lenders need to assess the risk associated with loan applications. Incorrectly classifying a risky applicant as low-risk may expose a lender to financial losses, while incorrectly flagging a good applicant may lead to missed lending opportunities.
This project investigates model performance and the trade-offs between these two types of errors.


 Dataset
   
•	Source: UCI Machine Learning Repository

•	Dataset: Statlog (German Credit Data)

•	Applicants: 1,000

•	Predictor variables: 20

•	Target: Good credit (0) or bad credit (1)

Dataset source: https://archive.ics.uci.edu/dataset/144/statlog+german+credit+data

 Tools and Technologies

•	Python
•	Pandas and NumPy
•	Matplotlib
•	Scikit-learn
•	Jupyter Notebook
•	GitHub

 Methodology

1.	Loaded and inspected the dataset.
3.	Checked data types and missing values.
4.	Renamed columns for readability and encoded the target variable.
5.	Conducted exploratory data analysis using statistical summaries and visualizations.
6.	Split the data into training (80%) and testing (20%) sets using stratification.
7.	Standardized numerical features and one-hot encoded categorical features.
8.	Trained Logistic Regression and Random Forest models.
9.	Evaluated accuracy, precision, recall, F1 score, ROC-AUC, and confusion matrices.
10.	Compared decision thresholds using hypothetical business costs.
11.	Examined Random Forest feature importance.
  
 Model Performance

Metric	    Logistic Regression	       Random Forest
Accuracy	           78.0%	                76.5%
Precision            66.7%	                61.0%
Recall	             53.3%	                60.0%
F1 Score	           59.3%	                60.5%
ROC-AUC	             80.4%	                80.1%

At the default 0.50 threshold, Logistic Regression achieved higher accuracy and precision, while Random Forest achieved higher recall and F1 score.

 Business Cost Analysis
    
For an illustrative business-cost analysis, the following hypothetical error costs were assigned:

•	False negative: ₦100,000
•	False positive: ₦10,000

At a probability threshold of 0.30:
   Model	          False Positives	        False Negatives	   Modeled Error Cost
Logistic Regression	         38	                11	             ₦1,480,000
Random Forest	               73	                 7	             ₦1,430,000

Random Forest produced a ₦50,000 lower modeled error cost on the test set under these assumptions. However, it also incorrectly flagged more good-credit applicants as risky.

These figures are illustrative estimates, not actual financial losses or guaranteed savings.

Key Findings
    
•	Credit amount and loan duration were among the strongest features in the Random Forest model.

•	Exploratory analysis showed associations between observed credit risk and variables such as loan duration, checking-account status, savings, and credit history.

•	Lowering the classification threshold increased bad-credit detection but also increased false positives.

•	Model selection depends on the relative business costs of different errors, not accuracy alone.

 Visualizations
    
The visuals/ folder contains charts created during the analysis, including:

•	Credit-risk distribution
•	Credit amount and loan duration by credit risk
•	Bad-credit rates across selected applicant categories
•	Threshold versus business cost
•	Business-cost comparison between models
•	Random Forest feature importance

 Limitations and Responsible Use

This project uses a historical dataset containing 1,000 applicants. Its results may not generalize to current lending populations.

The assigned error costs are hypothetical, and the selected threshold requires further validation. Feature importance does 
not establish causation. Variables such as age, sex-related categories, and foreign-worker status also raise fairness concerns that would require careful legal and ethical review.
Neither model should be considered ready for real lending decisions without independent validation, fairness assessment, appropriate governance, and ongoing monitoring.

Conclusion
This project demonstrates an end-to-end machine-learning workflow for credit-risk classification, from data preparation and exploratory analysis to model comparison, threshold optimization, and business-cost evaluation.

It illustrates how predictive performance can be connected to business decisions while recognizing the importance of validation, fairness, and responsible use.

Author
Alabi Temidayo Gabriel
 Data Analyst / Data Scientist

