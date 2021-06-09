# Health-Insurance-Claim-Detector

## Backgroud:
There are many fraudalent claims being made to health insurance companies, resulting in huge losses. 

The types of health insurance fraud are as follows:
1.Claim fraud: This means that the insured is claiming for a health care benefit that he is not entitled to receive as per the policy terms and conditions.
2.Application fraud: In such cases, the insured aware of all the facts, enters wrong information relating to his pre-existing diseases, date of birth, claims, etc.
3.External and internal frauds: External fraud simply means that the false claim is made either by the policyholder, beneficiaries, medical service provider against the insurance company. Internal fraud is carried out by the employees of the company against the policyholder.
4.Deliberate and opportunity fraud: Deliberate fraud is nothing but purposefully presenting the company with an accident, disease or loss which is covered under the policy.

On the basis of pre existing dataset, a machine learning alorithm can be developed to closely predict whether the claim made is genuine or not. The dataset contains various features like hospital location, type of illness, surgical description, cost for hospital,total charges etc.

## Objective:
To check whether the insurance claim made by claimant to the insurance company is genuine or not.
This is a supervied machine learning project done over a large dataset.

## Procedure:
### 1)EDA : Exploratory Data Analysis
- Delete the duplicate values
- Fill the null values with median or mode
- Convert the categorical columns into numerical with label encoder function
- Visualise the frequency of parameters in each feature with bar plot
- Check for outliers using boxplot
### 2)Feature Engineering
- Check the importance of features by calculating their scores with Extra trees classifier
- The least important features which arent impacting much on final result are discarded
- Check correlation between features using pandas profiling
- The features which are highly correlated, one of them is discarded if its removal is not affecting the result
### 3)Check whether data is imbalanced
- The data was found to be impalanced as 75% results were genuine and 25% only were fraud.
### 4)Balancing the data
- Random Forest Oversampling is used to balance the data so that genuine and fraud claims are both equal in number.
- Undersampling was not done as most of the valuable information would be lost and accuracy of the final model was coming out to be quite low.
### 5)Dividing the dataset into train and test
- The dataset is divided into train and test in the ratio 80:20
### 6)Model Building
- Different models were run on dataset and it was found out that decision tree model showed the most accuracy for both training and test dataset.
### 7)Generating pickle file
- Pickle file was dumped so that it could be used in deployment
### 8)Model Deployment:
-Streamlit was used to deploy the model which hosts the user interface on a webpage.


