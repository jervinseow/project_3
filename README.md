<img src="http://imgur.com/1ZcRyrc.png" style="float: left; margin: 20px; height: 55px">

# Project 3: Web APIs & NLP

## 1. Problem Statement
A newly established game store is looking to set up an online space on its website for users to hold discussions, which in turn will result in an increase in site traffic.<br>

They have hired us to develop a classification model that is able to accurately predict which category a discussion thread belongs to. This would reduce the man hours needed to manually classify threads, and would also streamline the thread creation procedure for users.<br>

At the same time, they would also like to find out more about the popularity of major consoles, products and games, so that they would be able to enhance their marketing strategy.<br>

## 2. Introduction:
In order to address the problem issued, a preliminary goal was created to use Reddit posts to do a preliminary classification model.<br>

For this project, I selected two subreddits that are within the same main category scope but are different topics - `r/PS5` and `r/XboxSeriesX`. Both subreddits are relating to gaming consoles but of different types and the aim is to extract out keywords/tokens with the main aim of using those tokens to classify whether the author is referring to the Earbuds subreddit or the Headphones subreddit.<br>

## 3. Executive Summary
<br>

Notebook 1: Data Collection and Export<br>
Notebook 2: Cleaning, Preprocessing and EDA<br>
Notebook 3: Model Selection 
<br>

<br>

### Best Vectorizer + Model and Best Parameters
<br>

TfidfVectorizer:
- max_features: 10000
- max_df: 0.7
- min_df: 2
- ngram_range: (1, 2)

LogisticRegression:
- max_iter: 1000
- penalty: l2
- C: 0.9
- solver: newton-cg



## 4. Insights

Our final model has a 78.4% rate of success of classifying a thread correctly. But, more can be done to increase the accuracy and hence the predictive strength of the model. 

Game store to focus more on trending topics/products identified:

- Console: PS5
- Game Titles(PS5): Elden Ring, Final Fantasy, Horizon Forbidden West, Gran Turismo
- Game Titles(Xbox): Elden Ring, Halo Infinite, Dying Light
- Hardware: Controllers

A possible expansion on this would be to identify emotions and sentiments on these topics, to ensure proper treatment.


## 5 Limitations
Our model might not be able to classify as accurately as required because both PS5 and Xbox are similar products. Both subreddits we used contain similar top words (i.e. game, play, elden ring), and we can expect the same results on other platforms.
<br>

Model selection wise, some of the limitations were mostly related to time and resource constraints whereby using a GridSearchCV with all the hyper parameters for tuning is not feasible. As such, some variations with better accuracy scores may have been missed out. We can explore the option of using Cloud GPUs to speed up processing times in the future.
<br>

Although Logistic regression is easily interpretable, it has some assumptions:
- Linearity between the features and the logit of the probability when Y=1
- Features are independent of each other
<br>

## 6 Possible Future Direction
- Further customize stopwords list, i.e. adding top few common words that appear in both subreddits
- Use autoML libraries to gain access to wider varieties of models
- Run sentiment and emotion analysis to gain further insights on customers' thoughts.
- Automate the process so that frequent market analysis can be done in order to revise marketing strategies.





