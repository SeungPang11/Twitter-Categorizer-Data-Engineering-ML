# Twitter-Categorizer-Data-Engineering-ML
**Techniques**: Data Collection, Data Cleaning, Data Engineering, Data Science, ML <br/>
**Tools**: Pyspark, SQL, MongoDB

## Problem
* Twitter is a popular online social networking platform that allows users to post texts as “tweets.” <br/>
Hashtags can group similar tweets and link to other tweets that include them, <br/>
however, if a user doesn’t provide hashtags, it is hard to label a given tweet. <br/>

* This project aims to utilize Big Data tools and ML techniques as well as <br/>
Web Application frameworks to categorize a user-provided tweet and correctly label it. <br/>

## Objective
* Provide support for the Data Engineering/ Software Development project in a cross-functional team <br/> 
* **Collect and clean** data from various sources, **load data** to MongoDB, **import data** to Spark <br/> 
* Perform **text-preprocessing**, and implement a **classification model** to categorize Tweets <br/>

<img width="461" alt="Screen Shot 2023-05-29 at 12 06 29 AM" src="https://github.com/SeungPang11/Twitter-Categorizer-Data-Engineering-ML/assets/67944800/83d201b3-5c1e-48a0-bd84-1e7c1fa2acad"> <br/>

<img width="223" alt="Screen Shot 2023-05-29 at 12 06 39 AM" src="https://github.com/SeungPang11/Twitter-Categorizer-Data-Engineering-ML/assets/67944800/c3387c70-f853-4d32-86ff-1405a6c3696d"> <br/>

## Datasets/ Data Collection
* Tweets of various topics collected from sources -  **[Harvard Dataverse](https://library.harvard.edu/services-tools/harvard-dataverse)**, **[Kaggle](https://www.kaggle.com/)**<br />
* The final cleaned and combined dataset contains **40599 unique values and 5 columns** 
* **Topics** include celebrity, politics, sports, stocks, and crypto 
* **Attributes** include username, ID, tweets, date, and label <br /> 
<br /> 
Example - cleaned stocks-related tweets dataset <br />
<img width="600" alt="Screen Shot 2023-06-06 at 7 17 40 PM" src="https://github.com/SeungPang11/Twitter-Categorizer-Data-Engineering-ML/assets/67944800/c7876b23-acff-45c3-9063-4b4ac59c94c5">


## Methods
____**Data Cleaning**____<br />
* Drop unnecessary columns, rename columns
* Rearrange columns, add lables based on topics
* Convert date object to datetime to ensure consistency <br />

<img width="400" alt="Screen Shot 2023-06-08 at 3 22 04 PM" src="https://github.com/SeungPang11/Twitter-Categorizer-Data-Engineering-ML/assets/67944800/71e1b3bd-69b0-4b79-a818-bf104502e5b0"> <br/>


____**Load Data in MongoDB to Spark**____<br />
* Load final combined data to MongoDB
* The following command retrieves data from MongoDB to Spark for further use <br />

<img width="400" alt="Screen Shot 2023-06-08 at 3 23 43 PM" src="https://github.com/SeungPang11/Twitter-Categorizer-Data-Engineering-ML/assets/67944800/7055493c-0431-4cc9-8c9d-150d7bb62142"> <br/>


____**Spark for Text Pre-Processing**____<br />
* Remove punctuation and special characters
* Convert all text to lowercase 
* Tokenizing text using regex
* TF-IDF vectorizer for converting tweet into a matrix of TF-IDF features - <br />
each row corresponds to a document <br />
and each column corresponds to a word or phrase <br />

<img width="400" alt="Screen Shot 2023-08-15 at 2 30 36 PM" src="https://github.com/SeungPang11/Twitter-Categorizer-Data-Engineering-ML/assets/67944800/2a3bffad-9f8a-465f-b7df-7b3d8583bc80"> <br />

____**Logistic Regression Model for Multiclass Classification**____<br />
* Split the dataset into a training and testing dataset (80-20 split) 
* Logistic Regression model on the training set and evaluate its performance


## Result <br/>
* Prediction - the model achieved an accuracy score of ≈ 68% <br />

<img width="400" alt="Screen Shot 2023-06-03 at 11 53 40 AM" src="https://github.com/SeungPang11/Twitter-Categorizer-Data-Engineering-ML/assets/67944800/4d5c6e14-7481-4ea4-8c9d-c9be40823cef"> <br />

<img width="400" alt="Screen Shot 2023-06-06 at 7 24 47 PM" src="https://github.com/SeungPang11/Twitter-Categorizer-Data-Engineering-ML/assets/67944800/6a36a281-7422-4d87-bff4-6d723c621d31"> <br />



