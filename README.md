
# Restaurant Recomndation Using Zomato Dataset
### Objective: 

To use Content based Filtering to recommend a restaurant in Bangalore using User's preferences in location, cuisine, cost of two.

<p align="center">
<img src="https://storage.googleapis.com/scrabbl-com.appspot.com/5727647023759360"width=60% height=60%>
</p>

#### How the Restaurant Recommendation System Works?

The rapid growth in data collection has led to a new era of a data-driven world. Data is used to create more efficient systems and that’s where recommender systems come in.

Recommendation systems are a type of information filtering systems because they improve the quality of search results and provide elements that are more relevant to the search item or that are related to the search history of the user.

These are active information filtering systems that personalize the information provided to a user based on their interests, relevance of the information, etc. Recommendation systems are widely used to recommend movies, items, restaurants, places to visit, items to buy, etc.

There are three types of recommendation systems:


  i) Content-based filtering :It uses similarities in products, services, or content features, as well as information accumulated about the user to make recommendations. 
  
  ii) Collaborative filtering : It relies on the preferences of similar users to offer recommendations to a particular user.
  
  iii) Hybrid recommender:  It combines two or more recommender strategies, using the advantages of each in different ways to make recommendations.


## About the Dataset
 We used [Zomato Dataset](https://www.kaggle.com/datasets/absin7/zomato-bangalore-dataset?select=zomato.csv) available on Kaggle.
 The dataset contains 51717 restaurants of different parts of Bangalore, India.

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

Some insights into our dataset:
![Graph 1](link)

![Graph 2](link)


## Documentation

### Packages Used


### Part: i
Our Project began with EDA and some basic cleaning of our dataset to have a better understanding of it and to make it better to work with.







After EDA, we moved to Sentiment Analysis of our reviews list. To apply Sentiment Analysis, we must pass our reviews through a pipeline (`Tokenization` → `Text_Cleaning` → `Stopwords`  → `Lemmetization`) which cleans the data making it fit for Sentiment Analysis.

For Sentiment Analysis, we are using  `blob.sentiment.polarity` from the `TextBlob` library. After getting the sentiment scores, we merge the score column with our Dataset for further use.

### Part: ii

After the sentiment scores for each restaurant is obtained, we move on to our objective i.e. to recomend restaurant based using Sentiment Analysis. As our dataset has other important features like Average Rating and no. of votes, we made a metric which take equal weightage from the mentioned features and calculate a score. This score is used to rank the restaurant.


## 🚀 CONTRIBUTORS

- [Ameesha Arora](https://github.com/ameesha26)

- [Gagandeep Singh Bindra](https://github.com/gagandeep00)

- [Nibhir Tongchangya](https://github.com/nibton)

- [Jiya Chintur](https://github.com/jiyac)
