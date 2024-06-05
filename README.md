# Project title: Exploring the Relationship Between Cancer Occurrence and Contributing Factors in the US Using Machine Learning Algorithms.  
## <u> Team Members </u>
- Priti Singh
- Pankaj Dholaniya
- Ikenna Nometa
- Gbocho Masato Terasaki

# Background
In this project, we wish to apply the learnings from the boot camp to study real data collected by the National Cancer Institute, called the Health Information National Trends Survey or HINTS.
HINTS regularly collects nationally representative data about the American public’s knowledge of, attitudes toward, and use of cancer- and health-related information. HINTS data are used to monitor changes in the rapidly evolving fields of health communication and health information technology and to create more effective health communication strategies across different populations. Survey researchers use the data to understand how adults 18 years and older use different communication channels, including the Internet, to obtain vital health information for themselves and their loved ones. 

# Methodology

In this study, we wish to use machine learning models/algorithms to study cancer occurrence in the US population. We have narrowed down to 21 features out of 370 features that we wish to study and think will provide meaningful associations to the occurrence of cancer.
We will select the top 15 features from this list based on feature selection and feature ranking. We will compare the performance of our selected variables to multiple sets of randomly selected 15 variables for performance. After the list of predictors is finalized, we will use supervised learning models to develop predictive modeling and examine its performance.

# Dataset descriptives
We will use survey data collected during the second cycle of HINTS 4 from October 2012 through January 2013. This includes responses collected from 3630 individuals living across multiple regions of the US. The sampling frame of addresses, provided by Marketing Systems Group (MSG), was grouped into three strata: 1) addresses in areas with high concentrations of minority population; 2) addresses in areas with low concentrations of minority population; 3) addresses located in counties comprising Central Appalachia regardless of minority population. For more details about the project, please visit-https://hints.cancer.gov.

## Problem description
1. We wish to investigate the relationship between cancer incidence and three key factors:
  - demographics including age, gender, income, and geography
  - the utilization of health information technology, including the Internet and tablets, for cancer-related education and
  - medical history
2. Which features best predict the outcome of cancer based on classification models?
3. What is the model performance?

## Potential Stakeholders
Individuals suffering from cancer and their families, as well as cancer-free individuals. Results from the study can guide individuals suffering from cancer to better manage their health, as well as cancer-free individuals to engage in their health management by the use of health information technology. The results will also guide physicians and other healthcare providers.

## Key performance indicators 
Model performance will be evaluated by creating a confusion matrix, assessing its accuracy, recall and precision.

## Data analysis 
### Data cleaning
The dataset contains information on 356 features from 3630 individuals. The primary indicator variable of interest is the occurrence of cancer. Thirty-one individuals did not respond to this question, so the observations were deleted from the analysis. In the reamining dataset (n=3599) 464 individuals had cancer (12.89%), while 3135 did not have any history of cancer (87.11%). In our sample, 60% were females, while 38.6% were females. Geographic distribution indicated 93.66% of individuals were from the non-Appalachian regions, 3% were from southern Appalachia, 2.4% were from north Appalachia, and 1.7% were from central Appalachia. Forty-seven percent of individuals in the sample had access to the Internet.


## Preliminary modeling plan
After conducting Exploratory Data Analysis (EDA) and identifying variables that could potentially explain whether someone has had cancer, we decided to explore the question: *What are good predictors of cancer?* Could it be demographic information, access to cancer information, internet usage, geographical region, medical conditions, or a combination of these factors?

### Feature Ranking
To identify the most important features for predicting our target variable by leveraging multiple machine learning models and Recursive Feature Elimination (RFE).
We chose 4 models (Logistic Regression (base model), LinearSVC, Decision Tree, ‘very shallow’ Random Forest), and for each model, we use RFE to recursively eliminate the least important features.
For each model, we apply Recursive Feature Elimination (RFE) to systematically remove the least important features. We obtained the feature rankings from each model, aggregated them, and then calculated the average ranking for each feature across all models.
Finally, we selected the top 15 features based on these average rankings.
![feature ranking](https://github.com/inometa/Hints_Cancer_Project/blob/main/Images/featureranking.png?raw=true)

## Model Selection
Once the features are decided, we construct a Random Forest model. While there exist tree-ensemble models such as Gradient Boosting Trees which generally excel in predictive accuracy, particularly in datasets with imbalance classes, we choose to build our pipeline around Random Forest model. We choose Random Forest, primarily, for its capabilities of addressing overfitting, being easy to train, and having embedded functions like importances_features. 

Then, we perform a hyperparameter tuning of the Random Forest, coupled with a cross-validation technique (K-fold), leading to construction more than 20000 trees. This only took 16minutes to fit all models. 
After getting the best parameters leading to the best cross-validation accuracy, we evaluate the model on the Test set:
We obtain an accuracy of 99.46% as well as a False Negative rate of 0.6%. 


## Future directions
Some work we wish to do to improve the study include:
-  Evaluation of model performance on new data from subsequent years from HINTS,
-  Exploration of the effects of oversampling vs undersampling on the model accuracy and
-  Development of an app that will automatically predict whether a person has had cancer based on the model we develop given input features.

## Acknowledgements
We wish to thank:
1. Roman Holowinsky, Alec Cott, Steven Gubkin, and the entire Erdös Institute Summer-May-2024 team,
2. Our project mentor, Greg Edwards, and
3. NIH’s National Cancer Institute for making the HINTS data available for our use.

![hints logo](https://github.com/inometa/Hints_Cancer_Project/blob/main/Images/HintsLogo2.png?raw=true)
