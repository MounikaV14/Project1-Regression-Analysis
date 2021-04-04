# Project1-Regression-Analysis
## Melbourne Dataset: House price prediction using Regression
In this study, we follow the CRISP-DM (Cross-industry standard process for Data mining) technique. This technique consists of the following steps.
1. Data understanding
2. Data Preparation
3. Modeling using Regression
4. Evaluation of results

**We will be answering the following questions based on our study**
**What is the trend of the house prices?**
**How to Handle categorical and missing data?**
**What are the highest correlated variables to price?**
**What are the key factors affecting price of a House?**

#### Data understanding:
Basically, the data understanding is nothing but collecting data, checking whether data is right or not, what type of data we have, whether the available data can answer my business questions or not, and also exploring, visualizing the data by using plots, graphs charts to understand the hidden meanings in the data.
Now, we don’t have to worry much regarding the data availability Since we have chosen a dataset based on the objective to predict the house prices using regression. Although Regression is the classical prediction algorithm it’s a very powerful technique to predict based on the independent features we have.
Our data set consists of 34,857 rows and 21 columns. Each row has information regarding the Price and Address of the house, Number of Rooms, Seller information, Bedrooms, bathrooms, car parking availability, Land Size of the house, etc.

#### Data Preparation:
One of the first things we have to do is to check the missing values present in the data and treat them accordingly based on the type of data. For example, Since we have both categorical and numerical data the missing value treatment would be different.
Let’s start the analysis by looking at the missing values in the Price column, Clearly, we can see that 21% of the data is missing, Hence we delete these rows.
we can observe the decreasing trend of house prices. Let’s look at the distribution of house prices. Clearly, From the above picture, we can see that the data is skewed towards the right which tells us that, on average, most of the house prices sling towards the higher side.
 
#### Missing values and It's treatment
Let’s look at the missing values in Numerical columns, out of 13 numerical columns, 9 of them have missing data. Building Area has 60% of the data missing, followed by YearBuilt 55% and the rest of them are around 22% of missing data. There are so many ways to fill these missing data, using the mean, the mode, etc. Here, we are filling them using the mean of the series.

From the above correlation matrix, we can infer that Rooms are highly correlated to price, followed by Bedrooms, Type and Year built.
Let’s check the unique values in the Rooms column. We can see that most of the houses have 3 bedrooms, followed by 2 and 4 bedrooms.

#### Modeling and Evaluation of Results:
In this study, we are using the Multiple LinearRegression model to predict house prices. Let’s choose all the independent variables in X and dependent (prices) in Y. Split the train and test data set. We have trained the model using 66% of the data and tested it with 33% of the data. We have chosen The RSquare as an evaluation metric for this model which is 80.7% in this case.
While experimenting with the different independent variables, I have removed the Rooms column from the dataset, trained and tested the model, surprisingly the R-square is less than 30% which tells us that since Rooms has a 47% correlation with the price it is highly affecting the price of the house.



