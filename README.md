# Idea for Codefundo++

- Team Members

HIMANCHAL CHANDRA,
ANKUR SIKARWAR

- what are we planning to build

  
We are planning to build a project which comprises of 2 parts:-
 In the first part we are planning to build a system which can categorize or classify a textual data using python Deep Neural Network with the help of google TensorFlow.  

In the second part we are planning to extract some important tweets (twitter tweets) from a dataset of twitter tweets related to some natural disaster and then firstly extract some useful tweets from them and then finally summarizing to get a summarized form of tweets. 

- how does it works


First part:-

Our project is based on text classication of textual data which simply means to classify feeded text into some class or category which is possible using Tensorflow which is a deep learning library. Sentiment analysis is also a type of text classification in which we classify text into positive sentiment and negative sentiment using TextBlob natural language processing library.  

Our aim is to assign a category to an input text. This can be achieved by training a neural network on data indicating what text represents(category). 

We will be using Natural Language Processing for our classification project. As we know text cannot be processed by tensorflow, so we need to convert the data into bag of words model and then feed it in our tensorflow model. 

The data processing step involves- stemming and tokenizing
and finally a bag of words model is created.

The bag of words model is a simplified representation used in natural language processing and information retreival . Also known as vector space model, it is used to create a unique list of words. It is a way o extract features from text for use in modelling such as in machine learning algorithms. 

There is no need of data preparation as we are using a dataset of 2014_India_floods which contains tweets from twitter as text and its assigned category. In this dataset we are having 9 different categories like Injured or dead people,Missing, trapped, or found people etc.

Once the csv is loaded, we need to clean the data and then form bag of words and convert the data to tensorflow specification. Then we need to start our model and feed the training dataset into it.

After training our model, now we can test the neural network  text classification model on newer sentences to predict their
category.


Second Part:-


In this part we are going to extract some useful tweets from the same dataset used in first part ie, 2014_India_floods and summarize it. 

Not all the tweets in our dataset will be useful and contains some useful information which can be used for disaster analysis etc. Useful tweets are classified as relevant tweets which contains some recent status update, emergency helpline number, information about hospitals etc. Irrelevant tweets contains someone sentiments, opinions etc which are not quite useful. 

Now we need to seperate relevant and irrelevant tweets from dataset which can be firstly by tokenizing and tagging the words in tweets with the help of spacy library. Spacy is a powerful nlp library which can extract text sentiment like date, person etc. Hence, Spacy can tokenize text and tell its entity type.

I marked token to be a content word if its entity type was recognised by spacy.  

This helped us to differentiate between relevant and irrelevant tweets as relevant tweets will contain more content words and vice versa.

Another concept which we are using is tf-idf from information retrieval because content words weights any content word the same weightage but we try to avoid this in our project as some words add more weightage than the other words.
 
Term frequency-inverse document frequency reflects how important a word is to a document in a collection or corpus.It is often used as a weighting factor in searches of information retrieval, text mining, and user modeling.Tf-idf can be calculated easily using spacy library of nlp. So, now it is easy to differentiate relevant and irrevelant tweets as tweets containing more number of content words with high tf-idf scores are categorised as relevant tweets. We know need to summarize tweets using content words with more tf-idf scores and it should be short(obviously!).

Therefore, we need to generate a summary of less than 150 words and full of content words which can be used by an organisation or rescue team helping in disaster situation. An equation can be framed for maximizing the total tf-idf score of our summary and using constraint like it should be less than 150 words. 
By using Pymathproj library of python this equation can be solved and we can get a summarized form of tweets.


- How users can get started with the project


Users like NGO's, organisations etc can get categorical tweets from our project which can help them to get different informations like information of infrastructure damage, no. of deaths etc. Real time summary can be created of useful text from a corpus of data which contains huge amount of data and is very difficult to figure out like what is the current status. So, this project can help them to figure out current situation and act accordingly.


- Dataset we are using


We are using dataset of the 2014 India flood in Jammu and Kashmir.


- Technologies used by us 


1.Python
2.Machine Learning
3.Data Science
4.Information Retrieval
5.Natural Language Processing
6.Deep learning.
7.Neural Network
8.Tensorflow

