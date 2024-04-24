# SC1015Proj_Movie_Success_Analysis

## Description  
This is a mini-project made for SC1015 – Introduction to Data Science and Artificial Intelligence. It makes use of the Movies Industry Dataset found in Kaggle: Movie Industry (kaggle.com) by Daniel Grijalva.  

## Algorithms/Libraries 
- Pandas
- Numpy
- Seaborn
- Sklearn
- KMeans
- XGBoost
- Plotly
- Neural Network

## Problem Definition 
There’re many factors that contribute to the success of a movie, such as budget, gross, score, etc. In recent history, lots of films were met with unexpected success despite the low cost or supposed ‘bad’ reception by audience. Additionally, films which are not as relevant compared to such ‘famous’ movies still gained notable financial success. **Thus, we intend to find out if it is possible to predict the popularity/success of movies based on their characteristics?**
- Success defined by us: Gross amount is 1.5 times the Budget at least 

## Content 
### Dataset: movies.csv 
This is the dataset we used for our mini project. According to the dataset page, there are 6820 movies (220 movies per year, 1986-2016), which is now updated to 7668 movies. Each movie has the following attributes: 
- budget: the budget of a movie. Some movies don't have this, so it appears as 0 
- company: the production company 
- country: country of origin 
- director: the director 
- genre: main genre of the movie. 
- gross: revenue of the movie 
- name: name of the movie 
- rating: rating of the movie (R, PG, etc.) 
- released: release date (YYYY-MM-DD) 
- runtime: duration of the movie 
- score: IMDb user rating 
- votes: number of user votes 
- star: main actor/actress 
- writer: writer of the movie 
- year: year of release 

### Jupyter Notebook: EDA (Movies_EDA_Final) 
This notebook contains our data cleaning, data preparation, data analysis and data visualization. We did the data analysis by looking at correlation, distribution and count. We used plotly to create interactive data visualization through boxplot, lineplot, scatterplot, pairplot and histogram. We also defined success by saying that a movie is a success if the gross amount is 1.5 times the budget. We separated the data and did minor analysis on them as well.  

### Jupyter Notebook: Additional Data Preparation 
This notebook contains the way we prepared the additional data to be tested for our model. The 3 files produced contains 1000 rows each and is filtered to be align with the dataset required. 

### Jupyter Notebook: XGBoost 
This notebook details our attempt to use XGBoost to predict a movie’s success based on the input dataset. The model created was then tested against the test set and the additional datasets. Through the functions available to XGBoost, we were able to evaluate the effectiveness of the model and also view the importance of the variable in the creation of the model. 

### Jupyter Notebook: K-Means 
This notebook details our attempt to cluster the dataset. Firstly, we tried to use K-Means to separate the dataset and determine whether we can use that to identify whether a film would be considered successful. However, since we already have a predefined successful and unsuccessful cluster, which became our ground truth values, we also used K-Means to see if we can predict it.  

### Jupyter Notebook: Neural Network 
This notebook details our attempt to use Neural Network to predict a movie success based on the input dataset. We tried different ways to train the model such as normalizing the inputs before feeding it to train the model and managed to train a decent model to determine whether a movie will be successful based on the inputs. 

### Slides 
These are the slides we used for our presentation. It is a summary of the project.  

## Conclusion (Key points) 
1. The movies in this dataset indicate 56.4% of movies are successful.
2. The rating of a movie does not play a significant role towards a movie’s score. 
3. Biography is the best genre and Horror is the worse genre from a score point of view.
4. Key figures (Main Actor, Director, Writer) of a movie will dictate the success of a movie more.
5. Main Actor is the most impactful towards a movie’s success.
6. The model created with the use of 4 variables (Year, Votes, Budget, Score) performed decent at predicting the success of a movie.
7. More variables with human interactions pertaining to the film or the cast in the film would likely result in a more definitive analysis of a film’s success and a more robust model to predict success. 

## Learning Points 
- XGBoost 
- K-Means
- Neural Network
- Plotly
- Choosing the right models to use
- Cleaning and preparing dirty data
- Finding the appropriate dataset
- Concepts about precision, Recall, F1 Score 

## Contributors 
### FCS2 Team2 AY23/24 Sem 2
Lee Yi Yuan (yiyuan906) – Exploratory Data Analysis, XGBoost  
Wong Jing Han (wjhan785) – Plotly Data Visualization, K-Means  
Lee Lin Yang Glenn (Ariesura) – Neural Networks, Presentation  

## References 
- NTU SC1015 Content  
- https://www.kaggle.com/datasets/danielgrijalvas/movies/data
- https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata?select=tmdb_5000_movies.csv 
- https://realpython.com/k-means-clustering-python/ 
- https://scikit-learn.org/stable/modules/generated/sklearn.cluster.KMeans.html 
- https://plotly.com/python/ 
- https://www.kaggle.com/code/muhammadehabmuhammad/movies-industry-analysis-and-correlations 
- https://www.analyticsvidhya.com/blog/2016/03/complete-guide-parameter-tuning-xgboost-with-codes-python/ 
- https://www.youtube.com/watch?v=aLOQD66Sj0g 
- https://contrib.scikit-learn.org/category_encoders/targetencoder.html 
- https://scikit-learn.org/stable/modules/cross_validation.html#stratification 
- https://www.youtube.com/watch?v=PxgVFp5a0E4 
- https://youtu.be/4i4C3ejTdgs?si=XfCjQW5h-ABD0Bu9 
- https://scikit-learn.sourceforge.net/dev/modules/model_evaluation.html 
- https://xgboost.readthedocs.io/en/stable/python/python_api.html#xgboost.plot_importance
- https://machinelearningmastery.com/tutorial-first-neural-network-python-keras/
- https://www.neuraldesigner.com/learning/tutorials/testing-analysis/
- https://www.v7labs.com/blog/f1-score-guide
