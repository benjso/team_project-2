# Team Project Part 2

## Description

The team continues to apply newly acquired skills and revisit the team project 1 salary dataset, adding a new dataset - cost of living dataset by country to the existing one. All of us adopted different methods and approaches to preprocess and analyze the data.

This project applies skills from the following previous modules:

* Introduction to Building Software (Shell, Git, Python)
* SQL
* Applying Statistical Concepts (Linear regression, classification, and resampling
* Scaling to Production
* Algorithm & Data Structures (Machine Learning Software Foundations Certificate)
* Deep Learning (Machine Learning Software Foundations Certificate)

Below includes a summary of the dataset, issues to solve, approaches/models adopted, performance comparison, insights as well as the list of videos regarding this project from each member. 

1. Summary of the dataset:

The salary data is from Kaggle. Due to the large dataset, the portion below 50k has been removed. There are 94 countries and over 3000 job titles in the dataset. 

The cost of living index data is merged to the salary data on Country name. The cost of living data is from https://www.numbeo.com/cost-of-living/rankings_by_country.jsp?title=2024, using the Cost of Living by Country data for year 2024.

2. Issues to solve:
   
Multi-classification issue: Predict the salary bins/buckets at 10000 intervals.

Regression issue: Use available predictors to predict the target value Salary.

3. Approach used to solve the issue and reason
   
(1) Pipeline approach to solve the multi-classification issue

  Reason to use this approach appy the knowledge and skills learned in the scaling to production sections. Utilizing a different models and different hyperparameters can easily be tested against one another and scoring metrics can be accurately compared with cross validation and grid search methods.
   
(2) Deep learning embedding model to solve the regression issue
   
   Reason to use this approach apply the knowledge and skills learned in the ML sessions. Also in the dataset, there are many categorical values. For example, there are 95 values for country and around 3500 values for job titles. Embedding approach is a good way to solve the issue with many categorical values.
   
(3) Neural Network model to solve the regression issue
   
   Reason to use this approach is to apply the knowledge points and skills we learned most recently in ML sessions. 
4. Use Auto ML 
   To get indication which Model will be best for classificaiton problem. Used this approach as per ML sessions small introductions to AutoML.
   
   Best pipeline: DecisionTreeClassifier

5. Performance comparison
   
(1) Pipeline approach:

The final Logistic Regression model achieved the following performance on the test set tuned by RandomizedSearch:
Log loss: 0.7338,
Accuracy: 0.7451,
Balanced accuracy: 0.4944,
ROC AUC: 0.8573.

The final Logistic Regression model achieved the following performance on the test set tuned by GridSearch:
Log loss: 0.9242,
Accuracy: 0.6659,
Balanced accuracy: 0.5557,
ROC AUC: 0.8651.

(2) Deep learning embedding model:

Mean Absolute Error: 0.42, which is within 5% of the mean target value (salary) 8.4; Mean Squared Error: 0.699.

The predicted value is within 5% range (4.2k) of the average true value (84k).

(3) Neural Network model:

Loss: 0.0039 - Mean Absolut Error: 0.0039 - Mean Squared Error : 8.6752e-05, with the prediction variance within 5% range.

6. Insights from visualization:

From the TSNE graph of embedding approach, we can see that certain job titles do get compensated better in comparison with others in general. The salary variance is more obvious by different job titles, than with different countries.


7. Video links:

* Benjamin Su - https://drive.google.com/file/d/1mB_5qPZJzdtjhonOlV7kl8dqJLuWDiVw/view?usp=sharing
* Yuanyuan (Caroline) Zhang - https://drive.google.com/file/d/1xX5G11Nhl22CtSwT_tFi0o3HFe0Y1BvM/view?usp=drive_link
* Sergii Khomych - https://drive.google.com/file/d/1dEOo2AlyYynxMLBJ2NyEb9c9BqQrSchH/view?usp=drive_link
* Melih Can Alan - https://www.youtube.com/watch?v=KY8nMaQJAKY  

# Team Project 2 - Project Repository Activities/Logs

* Benjamin Su - Explored and identified the source data from Kaggle.com, performed data pre-processing and then collaborated with team members to merge other datasets from multiple channels, loaded the data into SQL DB for feeding the training model. Determined and used Neural Network model with implementation of algorithm through Python programming for training the model and testing as well as model tuning-up. Organized the meetings and discussions in the team to catch up with the project timeline, and worked with the team to compare different models and training/test results with relevant analysis.

* Caroline Zhang - Explored and made suggestion on combining existing salary dataset with cost of living dataset on country name, so that the predictors are not only limited to categorical values, such as Country, and Job Title, it also contains the cost of living index numerical value; merged the two dataset into one on Country; developed a deep learning regression model with embeddings, produced visualizations to gain insights; set the structure and drafted the README file to include a summary of the dataset, issue to solve, approaches adopted and reasons, performance comparison, insights; leveraged github, slack and google meet to collaborate with the team while working on the project.

* Tarun Vashisht - Explored the dataset and cleansed the dataset to remove unncessary columns with no real impact. Also cleaned columns with NaN values which were making no contibution to the prediction model. When working with AutoML, used only cost of 
living index to figure out SalaryinUSD. To achiehve we used Tree-based Pipeline Optimization Tool(TPOT). After running multiple instances of the model, it gave result as  Best pipeline: DecisionTreeClassifier. But upon testing the model with actual and predicted result, results were not good. 


#### Below paragraphs are the orginal requirements for this team project ####
---------------------------------------------------------------------------------------------------------------------


# Team Project

## Description


The team project consists of two modules. Each module requires participants to apply the skills they have learned to date, and explore a dataset of their choosing. The first part of the team project involves creating a simple program with a database in order to analyze a dataset from an open source, such as Kaggle. In the second part of the team project, teams will come together again and apply the skills developed in each of the data science or machine learning foundations certificate streams. Teams will either create a data visualization or a machine learning model.

Participants will work in assigned teams of 4-5. 

#### Project Descriptions

* [First Team Project Description](./team_project_1.md)
* [Second Team Project Description](./team_project_2.md)

## Learning Outcomes
By the end of Team Project Module 1, participants will be able to:
* Resolve merge conflicts
* Describe common problems or challenges a team encounters when working collaboratively using Git and GitHub
* Create a program to analyze a dataset with contributions from multiple team members

By the end of Team Project Module 2, participants will be able to:
* Create a data visualization as a team
* Create a machine learning model as a team

### Contacts
**Questions can be submitted to the _#cohort-3-help_ channel on Slack**

* Technical Facilitator: 
  * **Kamilah Ebrahim**(she/her)
  kamilah.ebrahim@mail.utoronto.ca

* Learning Support Staff:

  * **Farzaneh Hashemi** (she/her )
  fhashemi.ma@gmail.com
  * **Tong Su** (she/her)
  tong.su@mail.utoronto.ca

### Delivery of Team Project Modules

Each Team Project module will include two live learning sessions and one case study presentation. During live learning sessions, facilitators will introduce the project, walk through relevant examples, and introduce various team skills that support project success. The remaining time will be used for teams to assemble and work on their projects, as well as get help from the facilitator or the learning support to troubleshoot any issues a team may be encountering. 

Work periods will also be used as opportunities for teams to collaborate and work together, while accessing learning support. 

### Schedule

|Day 1|Day 2|Day 3|Day 4|Day 5|
|-----|-----|-----|-----|-----|
|Live Learning Session |Live Learning Session|Case Study|Work Period|Work Period|

## Requirements
* Participants are expected to attend live learning sessions and the case study as part of the learning experience. Participants are encouraged to use the scheduled work period time to complete their projects.
* Participants are encouraged to ask questions and collaborate with others to enhance learning.
* Participants must have a computer and an internet connection to participate in online activities.
* Participants must not use generative AI such as ChatGPT to generate code to complete assignments. It should be used as a supportive tool to seek out answers to questions you may have.
* We expect participants to have completed the [onboarding repo](https://github.com/UofT-DSI/onboarding/tree/main/onboarding_documents).
* We encourage participants to default to having their camera on at all times, and turning the camera off only as needed. This will greatly enhance the learning experience for all participants and provides real-time feedback for the instructional team. 

### How to get help
![image](/steps-to-ask-for-help.png)

## Folder Structure

### Project 1
```markdown
|-- data
|---- processed
|---- raw
|---- sql
|-- reports
|-- src
|-- README.md
|-- .gitignore
```

### Project 2
```markdown
|-- data
|---- processed
|---- raw
|---- sql
|-- experiments
|-- models
|-- reports
|-- src
|-- README.md
|-- .gitignore
```

* **Data:** Contains the raw, processed and final data. For any data living in a database, make sure to export the tables out into the `sql` folder, so it can be used by anyone else.
* **Experiments:** A folder for experiments
* **Models:** A folder containing trained models or model predictions
* **Reports:** Generated HTML, PDF etc. of your report
* **src:** Project source code
* README: This file!
* .gitignore: Files to exclude from this folder, specified by the Technical Facilitator

# Team Project 2 - Project Repository Activities/Logs
* Benjamin Su - Explored and identified the source data from Kaggle.com, performed data pre-processing and then collaborated with team members to merge other datasets from multiple channels, loaded the data into SQL DB for feeding the training model. Determined and used Neural Network model with implementation of algorithm through Python programming for training the model and testing as well as model tuning-up. Organized the meetings and discussions in the team to catch up with the project timeline, and worked with the team to compare different models and training/test results with relevant analysis.


# Team Project 2 - Video Links
* Benjamin Su - https://drive.google.com/file/d/1mB_5qPZJzdtjhonOlV7kl8dqJLuWDiVw/view?usp=sharing   

