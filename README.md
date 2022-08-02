## Business Problem


Tanzania ministry of agriculture wishes to upgrade the available waterpoints in Tanzania. They wish to know in advance which waterpoints are still functional, those that are functional but are in poor conditions and hence may need repairs and also to know those that are not functional at all. The ministry wishes for me to come up with a cost effective way which will enable them to identify and allocate sufficient resources to the needed areas.Through this project, the ministry is able to sufficiently plan and allocate resources to areas which would be in need of access to water. We all know how important water is to the daily activity of human beings, therefore the solutions in this project will go a long way in helping governments and organizations to plan how to implement water policies in Tanzania.

## Data

This data was obtained from the DrivenData platform, which is a platform that hosts competitions for data scientist with regards to data that is about the social aspects of the human life. The data set contains about 42 columns with majority of the variables being categorical variables. This will suit out analysis as we aim to come up with a classification model that best suits the problem we are trying to solve.

Explanation of the datafeatures is contained in the features file within these repo.

## EDA
In these stage the following was done to prepare data for preprocessing

#### Duplicates
No duplicates were found in the initial search.
#### Missing values
1. Most of the columns were categorical variables, therefore missing values were imputed as "unknown" categories in their respective fields.
2. Some of the columns contained significant zero values in their entries:
    The population column contained most values as entries zero, I left it as it was.
    Some categorical columns contained also zeros as entries, these were transformed to "unknown" category.
3. Some of the numeric columns which had zero entries, the median value wa imputed in their place.

## Preprocessing
1. Numeric columns were transfomed using StandardScaler from the sklearn library into a similar scale.
2. I transformed the categorical columns using the OneHotEncoding module from sklearn.

## Modeling
I tried various models but the one with the most accuracy was the random forest model classifier with about 80% accuracy, with about 81% (functional) and 83% (non functional) precision on the majority classes. The model however was struggling to interpret the minority class with a less than 50% precision