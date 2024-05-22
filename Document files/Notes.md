# Document content
This file contains notes, todos, and reminders for the Cancer HINTS project. It will also be used to keep track of important information relating to this project, and generally, the May-2024 Erdös Institute Data Science Boot Camp.

## May 13, 2024 (Zoom meeting notes)
* Primary goal of the project is to learn and improve individuals' python data science skills 
### Todos: 
- > Setup GitHub repo
- > Start notes document (this)
- > Go through data and codebook
- Think about possible research questions to consider
- Go through the article Priti will share on Slack

Next Zoom meeting: Tuesday 5/14 at 7pm EST

## May 16, 2024 (Zoom meeting)
Discussed our initial insights into data. Was difficult to work on as it is, so we need to figure out variables of interest. However, these variables will be determined by the questions we want to ask or are interested in finding their answers.

- Pankaj wrote some code to explore data (To be added to GitHub later).
- Pankaj also identified about 77 variables out of the 300+ variables that may be significant.
- Ikenna talked about the need to see the variable definitions in the codebook to ensure we are choosing the right variables.
- Priti emphasized the need to have a [literature] basis for our questions. Also encouraged looking for how use of (or access to) technology relates to cancer diagnosis.
- Our mentor has been added to our slack channel.
- Priti shared another literature that may help guide our questions
### Todos:
- Priti to add the one page writing on the Readme file (in GitHub) by the deadline of this weekend containing description of our data, identification of stakeholders, outlining KPIs (key performance indicators), tables, etc
- Pankaj to add his python notebook to GitHub.
- **Everyone**: Add possible questions to the GitHub.
- **Everyone**: work on identifying important variables.
- **Everyone**: Read the literatures Priti shared.
- Try to meet our project mentor to establish initial communication and get suggestions for possible questions to work on.

> **Next meeting**: _Monday, 5/20/2024 at 1pm Eastern time_.

## May 21, 2024 (Zoom meeting with Greg, our Project mentor)
After describing the data we have and the Python explorations done, the meeting with Greg had these as the main takeaways: 

- Dealing with missing data: input value that doesn’t bias other estimates. Use regression model to get more, KNN also (Pankaj), also input the median value (which doesn’t) cause bias
- Matplotlib and Seaborn can be used to get good graphics for descriptive statistics of our data.
- It was observed that most of our variables are categorical, and the ML methods we employ will have to be suited for categorical data
- Non-categorical variables can be converted to a categorical variable with dummy variables
- About looking for variables/features to focus on:
> - Try logistic regression with all variables and what will come out as the most predictive features.
> If you have specific questions, just select the most relevant features  to help reduce the dimension 
> Can we ask more questions, not focusing on cancer but figuring out what more will be outward?
> How does the health care info tech data break down
> Maybe do feature selection / automatically select feature — forward …
> Scikit-Learn has feature selection methods https://scikit-learn.org/stable/api/sklearn.feature_selection.html#module-sklearn.feature_selection
> Recursive elimination: Do some dimension reduction 
> Focus on narrowing down your questions and selecting variables 
> What is balanced data, and when is it considered an issue?
- Todos: 
> Do a simple (logistic) regression model that is easy to explain and analyze. 
> Compare that to a more advanced ML model (whichever is appropriate)
> Finish up with exploratory data analysis
- Last notes:
> Greg won’t be available to meet after May 31, 2024
> Need to suggest meeting again in two days at a time that works for all members of the group.

@Pankaz, please add anything else I forgot to note down.
