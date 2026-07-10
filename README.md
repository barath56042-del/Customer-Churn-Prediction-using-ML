Customer churn is one of the most important metrics for a growing business to evaluate. It's easier to save an existing customer before they leave than to convice them to come back. Understanding and preventing customer churn is critical to company's long-term success.

In this project, we will use statistical testing to analyze the key factors of customers who are more likely to churn, develop a classification model to predict churn based on those factors, and provide recommendations for retaining customers as well as predictions of churn for a list of customers (delivered via csv).

💹 Business Goals
Find drivers for customer churn at Telco. Why are customers churning?

Construct a ML classification model that accurately predicts customer churn.

Deliver a report that a non-data scientist can read through and understand what steps were taken, why and what was the outcome?

📝 Initial Questions
Which variables are associated with churn?

Are average monthly charges higher for customers who churn?

Are tenure shorter for customer who churn?

Are additional services independent with churn?

📂 Data Dictionary
Variable	Value	Meaning
Contract Type	1) Month-to-month 2) One year 3) Two year	This indicates what type of contract the customer has
Internet Service Type	1) DSL 2) Fiber Optic 3) None	This indicates what type of internet service the customer has, if any
Payment Type	1) Bank transfer 2) Credit card 3) Electronic check 4) Mailed check	This tells us how is the customer paying for the service
Monthly Charges	Float number	This tells us how much is the customer paying each month
Teunure	Integer ranging from 0-72	This shows how long (months) does the customer stay with the company
Online Bakcup	1) Yes 2) No 3) No internet service	This indicates if the customer has online backup service
Online Security	1) Yes 2) No 3) No internet service	This indicates if the customer has online security service
Tech Support	1) Yes 2) No 3) No internet service	This indicates if the customer has tech support service
Device Protection	1) Yes 2) No 3) No internet service	This indicates if the customer has device protection service
Streaming TV	1) Yes 2) No 3) No internet service	This indicates if the customer has streaming tv service
Streaming Movies	1) Yes 2) No 3) No internet service	This indicates if the customer has streaming movies service
🪧 Process
1️⃣ Data Acquisition
Gather data from mySQL database
acqure.py
2️⃣ Data Preparation
Data Cleaning
Data Splitting
3️⃣ Exploratory Analysis
Ask questions to find what are the key variables that are driving the churn

Gather and sort churn rate from each driver into .xlsx file

Import churn_rates.xlsx and store the data in the form of dataframe

Create visualizations for the churn rate for each variable

Explore each feature's dependency with churn and create visualization for each

4️⃣ Statistical Testing & Modeling
Conduct T-Test for categorical variable vs. numerical variable

Conduct Chi^2 Test for categorical variable vs. categorical variable

Conclude hypothesis and address the initial questions

5️⃣ Modeling Evaluation
Create decision tree classifer and fit train dataset

Find the max depth for the best performing decision tree classifer (evaluated using classification report, accuracy score)

Create random forest classifier and fit train dataset

Find the max depth for the best performing random forest classifier (evaluated using classification report, accuracy score)

Create KNN classifier and fit train dataset

Find the k for the best performing KNN classifier (evaluated using classification report, accuracy score)

Create logistic regression model and fit train dataset

Find the parameter C for the best performing logistic regression model (evaluated using classification report, accuracy score)

Pick the top 3 models among all the models and evaluate performance on validate dataset

Pick the model with highest accuracy and evaluate on test dataset

🔁 Steps to Reproduce
 You will need an env.py file that contains the hostname, username and password of the mySQL database that contains the telco table. Store that env file locally in the repository.
 Clone my repo (including the acquire.py, prepare.py and churn_rates.xlsx)
 Confirm .gitignore is hiding your env.py file
 Libraries used are pandas, matplotlib, seaborn, plotly, sklearn, scipy
 Follow instructions in telco_analysis workbook and README file
 Good to run telco_report 😸
🔑 Key Findings
churn_drivers

▪️ The top 4 drivers of churn are:
electronic payment type

sernior citizens

month-to-month contract type

fiber optic internet service type

▪️ Average monthly charges is higher for customers who churn

▪️ Average tenure is shorter for customers who churn

▪️ Additional services (device protection, online security, online backup, tech support, streaming tv, streaming movies) are dependent on churn

▪️ The meachine learning model: logistic regression classifier is expected to predict churn with 81% accuracy on future unseen data

🔆 Recommendations
▪️ Raise price of month-to-month contract type and offer discounts for two-year contract to lead customers towards the other two contract types

▪️ Offer discount on device protection, streaming tv and streaming movies services

▪️ Offer online security, online backup, tech support services for free for one-year and two-year contracts customers

revenue_predictions

🔜 Next Steps
▪️ Collect more data on customers' demographic information (eg. place of residence, socio-economic data such as occupation, household income.)

▪️ Develop machine learning models with higher accuracy with these additonal data and more accurate features.

▪️ Conduct price discrimination analysis to further determine the price point for each contract type and service.
