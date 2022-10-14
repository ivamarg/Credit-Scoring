# Credit-Scoring
The objective of this project is to build a credit scoring model.
This model defines client scoring based on a statistical analysis of past borrowers’ characteristics instead of using judgmental rules. Statistical models improve the accuracy of credit decisions and make lending more cost-efficient.

## Data
Data downloaded from the site [kaggle.com](https://www.kaggle.com/c/sf-dst-scoring)

#### Features Defination
- client_id - identification

- education - education level (SCH - School; GRD - Graduated (Master degree); UGR - UnderGraduated (Bachelor degree); PGR  - PostGraduated; ACD - Academic Degree)

- sex - client sex

- age - client age

- car - binary/ has a car or not

- car_type - whether car is international

- decline_app_cnt - declined application count in the past

- good_work - binary/ has 'good' work or not

- bki_request_cnt - requests to BKI

- home_address - category of home address

- work_address - category of work address

- income - income

- foreign_passport - binary/ has foreign passport

- sna - connection with bank employee

- first_time - age of information about the client

- score_bki - BKI score

- region_rating - region rating

- app_date - application date

- default - default flag

## Implementation
In this project, the algorithms LogisticRegression, RandomForestClassifier, GradientBoostingClassifier,
XGBClassifier, CatBoostClassifier were used to predict default. The data was divided 
into training and test in a ratio of 80:20, since the dataset is large. 
The imbalance of classes was taken into account, the emphasis was on increasing the recall.


## Result
The best model showed a roc auc score of 75%. The decision of the model was most influenced by the score according to the data from the BKI, the combined addresses of home and work, the relationship of the borrower with the bank's customers.
In general, a higher rating of the region has a positive effect on loan issuance. The influence of the rating of regions 
for clients with ACD education is especially noticeable. For clients with a school background, the rating values are spread out over a narrower range and does not affect the decision to issue a loan
