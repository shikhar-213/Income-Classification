# Income-Classification
## Project Background: -
A company named ‘Subsidy Inc.’ delivers subsidies to individuals based on their income. Accurate income data is one of the hardest pieces of data to obtain across the world. Subsidy Inc. has obtained a large data set of authenticated data on individual income, demographic parameters, and a few financial parameters. 
This project simplifies the data system by reducing the number of variables to be studied, without sacrificing too much accuracy. Such a system would help Subsidy Inc. in planning subsidy outlay, monitoring, and preventing misuse.
Insights and recommendations are provided on the following key areas:
- Relationships between variables: - Understanding the proportion of categorical variables and how several variables are affecting the output variable with the help of frequency tables and visualizations.
- Insignificant variables: - Finding and removing insignificant variables to reduce the model’s complexity.
Visualizations and other key metrics can be found here.

## Data Structure: -
We were given the dataset in CSV format named income.csv. This dataset holds 31,978 entries with 12 features and one output variable (i.e. the personal income of individuals).
This dataset is represented as 31978 x 13 in matrix form.
| Attribute Name  | Data Type  |
|-----------|-----------|
| age	| Continuous |
| JobType	| Categorical |
| EdType	| Categorical |
| maritalstatus	| Categorical |
| occupation	| Categorical |
| relationship	| Categorical |
| race	| Categorical |
| gender	| Categorical |
| capitalgain	| Continuous |
| capitalloss	| Continuous |
| hoursperweek	| Continuous |
| nativecountry	| Categorical |
| SalStatus	| Categorical |

Before preparing the data for input into machine learning models, various quality and consistency checks were conducted using Python's Pandas library. Several null values were identified and removed from the dataset. The remaining data was deemed clean and ready for further processing.

## Executive Summary: -
While visualizing the data, some features did not impact the output variable very much, although they were making the model more complex.
It was found that removing these insignificant variables did not affect the models’ accuracies. Hence, they were dropped from the dataset to reduce the models’ complexity. Below is the bar graph showing that there is no significant change in accuracies of all three models even after removing insignificant features.
Visualization charts and other key metrics can be found here.

![image](https://github.com/user-attachments/assets/4d5e076b-15a4-4dbc-a91d-cb5e8ead1901)

Here is the summary of all the model’s performance with & without insignificant variables.

| Model                | Accuracy (With all variables) | Accuracy (Without insignificant variables) |
|----------------------|----------------------------|-------------------------------------------|
| Logistic Regression | 83.93 %                     | 83.90 %                                   |
| Random Forest       | 85.62 %                     | 85.06 %                                   |
| K-Nearest Neighbor  | 83.39 %                     | 83.27 %                                   |

## Recommendations: -
There are several use cases for such a project in real life.
-	If you have multiple customers that come in, then we can identify the proportion of customers who are likely to have an income less than 50000 and the percentage of people with more than 50000; and that could allow us to be able to plan an outlay of resources and so on. So, that is one use case that we can think of.
-	Another use case is really, if someone actually discloses an income and if it is an outlier in terms of, let us say someone says they are earning less than 50000; but our classifier says with all these attributes it is very likely the income is greater than 50000, then it might allow us to look at those particular cases in more detail, so that there is no misuse of schemes like this.

