# Title- Explain the relationship between cancer occurrence and other factors based on machine learning algorithms.  
## <u> Team Members </u>
- Priti Singh
- Pankaj Dholaniya
- Ikenna Nometa
- Gbocho Masato Terasaki

# Background
In this project, we wish to apply the learnings from the boot camp to study real data collected by the National Cancer Institute, called the Health Information National Trends Survey or HINTS.
HINTS regularly collects nationally representative data about the American public’s knowledge of, attitudes toward, and use of cancer- and health-related information. HINTS data are used to monitor changes in the rapidly evolving fields of health communication and health information technology and to create more effective health communication strategies across different populations. Survey researchers use the data to understand how adults 18 years and older use different communication channels, including the Internet, to obtain vital health information for themselves and their loved ones. 

# Methodology- Tentative

In this study, we wish to use machine learning ~~-based classification~~ models/algorithms to study cancer occurrence in the US population. We are still finalizing the feature/independent variables.

# Dataset descriptives
We will use survey data collected during the second cycle of HINTS 4 from October 2012 through January 2013. This includes responses collected from 3630 individuals living across multiple regions of the US. The sampling frame of addresses, provided by Marketing Systems Group (MSG), was grouped into three strata: 1) addresses in areas with high concentrations of minority population; 2) addresses in areas with low concentrations of minority population; 3) addresses located in counties comprising Central Appalachia regardless of minority population. For more details about the project, please visit-https://hints.cancer.gov.

## Problem description-Tentative 
1. We wish to investigate the relationship between cancer incidence and two key factors: 
  - the utilization of health information technology, including the Internet and tablets, for cancer-related education and
  - geographical location.
2. How does exposure to cancer-related health information online influence health behaviors, such as diet and exercise
3. How does access to health information technology impact the frequency of cancer screenings? Particularly, how does access to health information affect the frequency of breast cancer screening among patients aged 40 to 75?

### What machine learning algorithms can help us answer the questions above?
1.
2.
3.
### What variables/features will be needed for each algorithm?
1.
2.
3.

## Potential Stakeholders
Individuals suffering from cancer and their families, as well as cancer-free individuals. Results from the study can guide individuals suffering from cancer to better manage their health, as well as cancer-free individuals to engage in their health management by the use of health information technology. The results will also guide physicians and other healthcare providers.

## Key performance indicators 
Model performance will be evaluated by creating a confusion matrix, assessing its accuracy, sensitivity, and specificity, and calculating the area under the received operating characteristic curve at various thresholds.

## Data analysis 
### Data cleaning
The dataset containes information on 356 features, from 3630 individuals. The primary indicator variable of interest in occurence of cancer. Thirty one individuals did not respond to this question and hence the observation were deleted from the analysis. In the reamining dataset (n=3599) 464 individuals had cancer (12.89%), while 3135 did not have any history of cancer (87.11%). In our sample 60% were females, while 38.6% were females.Geographic distribution indicated 93.66% individuals were from non-appalachian region, 3% were from southern appalachia, 2.4% were from north appalachia, and 1.7% were from central appalachia.



## Preliminary modeling plan
After conducting Exploratory Data Analysis (EDA) and identifying variables that could potentially explain whether someone has had cancer, we decided to explore the question: *What are good predictors of cancer?* Could it be demographic information, access to cancer information, internet usage, geographical region, medical conditions, or a combination of these factors?

To answer this question, we will explore which features within our dataset are good predictors of cancer. We will use two methods for feature selection:

*Embedded Methods*: These methods perform feature selection as part of the model training process. We will employ a Logistic Regression model with L1 regularization (Lasso) and Tree-based models like the Random Forest Classifier, which inherently provides feature importance scores (using model.feature_importances_).

*Wrapper Methods*: These methods evaluate feature subsets based on model performance. We will use Sequential Feature Selection (either forward or backward selection) and Tree-based models in combination with Recursive Feature Elimination (RFE) from sklearn.feature_selection.

After selecting the best features, we will apply other algorithms learned during this bootcamp, such as Gradient Boosting algorithms, K-Nearest Neighbors (KNN), Support Vector Machines (SVM), and Neural Networks, with hyperparameter tuning to build the best predictive model.
