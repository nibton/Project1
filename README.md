
# Restaurant Recomndation Using Zomato Dataset
#### This repository contains our Project on Restaurant Recomnedation System Using Sentiment Analysis developed using Python.

## About the Dataset
 We used [Zomato Dataset](https://www.kaggle.com/datasets/absin7/zomato-bangalore-dataset?select=zomato.csv) available on Kaggle.
 The dataset contains 51717 restaurants of Bangalore, India.

### The dataset contains the following features:

URL - contains the URL of the restaurant on the zomato website

address - contains the address of the restaurant in Bengaluru

name - contains the name of the restaurant

online_order - if the restaurant accepts online orders.

book_table - if the restaurant has reservation option.

rate - contains the overall rating of the restaurant out of 5

votes - contains total number of rating for the restaurant.

phone - contains the phone number of the restaurant

location - contains the neighborhood in which the restaurant is located

rest_type - restaurant type

dish_liked - dishes people liked in the restaurant

cuisines - food styles, separated by a comma

approx_cost(for two people) - contains the approximate cost for a meal for two people

reviews_list - list of tuples containing reviews for the restaurant, each tuple consists of two values


## Documentation

### Part: i

We began our project by importing the necessary Libraries for statrting our project.

`import Pandas as pd`

`import numpy as np`

As we are interested in the finding the sentiment score of the reviews of each restaurant,we started with the cleaning of the reviews.

We used `ast.literal_eval`method from `ast`: Abstract Syntax Trees library to convert the strings to a list of tuples to extract the needed information.

After converting the strings to list of tuples, we cleaned out the characters that are unnecessary and  might affect the accuracy of the sentiment score towards the end.

Further, we used `re` library to further clean the data like Removing Non ALphabets, Non English Words and to convert all Upper Cases to Lowere Cases.


 For the final part of the cleaning, we put the reviews through NLTK pipeline of: 
 
`Text_Cleaning` → `Stopwords`  → `Lemmetization`.


 After getting the Cleaned Text(reviews in this case), we pass it through our Sentiment Analyzer.

 For that, we are using  `blob.sentiment.polarity` from the `TextBlob` library. After getting the sentiment scores, we merge the score column with our Dataset for further use.

### Part: ii








## 🚀 CONTRIBUTORS

   -[Ameesha Arora](https://github.com/ameesha26)
   
   -[Gagandeep Singh Bindra](https://github.com/gagandeep00)
   
   -[Nibhir Tongchangya](https://github.com/nibton)
   
   -[Jiya Chintur](https://github.com/jiyac)
