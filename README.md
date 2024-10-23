# UCBerkeleyMLCertificate - Practical Application 3
# Analysis of Bank Markering Campaign

## 1. Background
A portugese bank has collected data from 17 campaigns that occurred between May 2008 and November 2010. During these campaigns, applications for long-term deposit were offered to 41,188 prospects.

The primary objective of the project was to predict whether the prospect will subscribe to the service based on the observed characteristics of the prospect. In other words, we were trying to uncover the attributes which differentiate subscribers and non-subscribers. 

## 2. Data Preparation
The following steps were taken as a result of data exploration:

* Dropped the 'duration' variable since it is a target leaker. The duration is not known before the call is made, and therefore cannot be used for model implementation.
* Dropped variables highly correlated with the other variables.
* Hot encoded and label encoded the categorical variables.
* Scaled the variables.
* Prepared train (70%) and test (30%) samples for model development.

## 3. Modeling
As the result of the analysis we developed several models (KNN, Logistic regression, Decision Tree annd SVM) to identify factors which impact the decision of a prospect to subscribe to the service. We used accuracy, precision, recall, F1 metrics and ROC-AUC curve to identify the best model.

Logistic regression outperformed the other models in terms of performance metrics and runtime. The ROC curve shows that the logistic regression captures more of the subscribers for the same percentage of non-subscribers when both bank variables and socioeconmic variables are included in the analysis.

## 4. Findings
The following prospects are morely likely to accept the offer to subscribe:

* Prospects without defaults
* Students and retired customers
* Older prospects
* Single prospects
* Highly educated prospects
  
Additionally, timing plays a significant role in campaign success (month, day of week), as well as the way the prospects were contacted.

## 5. Recommendations and Next Steps
The dataset provided by the bank seems to have multiple issues with data quality (some variables and relationship with the target did not make sense). I recommend contacting the data provider and asking questions regarding the data, then further fine-tuning the models. 

Additionally, it would be interesting to conduct a cost-benefit analysis in order to create a strategy for the bank, based on cost of contacting a prospect vs profit from a booked account. 

As immediate next steps, the bank may start implementing the strategy based on the findings above - i.e. targeting the groups of prospects who are more likley to subscribe and increasing the call volume on the days the prospects ar more likely to accept the offers.

You can find the Jupyter notebook in this location:https://github.com/LianaGafarova/BerkeleyMLCertificate-BankMarketingCampaign/blob/main/prompt_III_LianaGafarova.ipynb
