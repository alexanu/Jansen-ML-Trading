# Machine Learning for Algorithmic Trading - 1st Edition

Link to the book: https://drive.google.com/file/d/1hXfMvB_JRHJFZAHs2oBJ-55ZdHxBxbkz/view
Link to a parallel repo: https://github.com/PacktPublishing/Hands-On-Machine-Learning-for-Algorithmic-Trading/tree/master/Chapter01


It was published in January 2019 by [Stefan Jansen](https://www.linkedin.com/in/applied-ai/).

**Update**: I've started working on the **second edition** that will add more end-to-end backtesting examples using zipline to complement the current illustrations how to generate signals using ML models. This should hopefully become available around the end of this year.   

## Installation and Data Sources

- For instructions on setting up a `conda` environment and installing the packages used in the notebooks, see [here](./installation.md).
- To download and preprocess many of the data sources used in this book see [create_datasets](data/create_datasets.ipynb).

# How the book is organized

### [Chapter 01: Machine Learning for Trading] (01_machine_learning_for_trading)

This [chapter] summarizes how and why ML became central to investment, describes the trading process and outlines how ML can add value. 

### Chapter 02: Market & Fundamental Data

This [chapter](02_market_and_fundamental_data) introduces market and fundamental data sources. In particular, this chapter will cover the following topics:
- How market microstructure shapes market data
- How to reconstruct the order book from tick data using Nasdaq ITCH 
- How to summarize tick data using various time, volume and dollar bars
- How to work with eXtensible Business Reporting Language (XBRL)-encoded electronic filings
- How to parse and combine market and fundamental data to create a P/E series
- How to access various market and fundamental data sources using Python

### Chapter 03: Alternative Data for Finance

This [chapter](03_alternative_data) covers:

- How the alternative data revolution has unleashed new sources of information
- How individuals, business processes, and sensors generate alternative data
- How to evaluate the proliferating supply of alternative data used for algorithmic trading
- How to work with alternative data in Python, such as by scraping the internet
- Important categories and providers of alternative data

### Chapter 04: Research & Evaluation of Alpha Factors

[Chapter 4](04_alpha_factor_research):

- How to characterize, justify and measure key types of alpha factors
- How to create alpha factors using financial feature engineering
- How to use `zipline` offline to test individual alpha factors
- How to use `zipline` on Quantopian to combine alpha factors and identify more sophisticated signals
- How the information coefficient (IC) measures an alpha factor's predictive performance
- How to use `alphalens` to evaluate predictive performance and turnover
 
### Chapter 05: Strategy Evaluation & Portfolio Management

[chapter](05_strategy_evaluation) covers:  
- How to build and test a portfolio based on alpha factors using zipline
- How to measure portfolio risk and return
- How to evaluate portfolio performance using pyfolio
- How to manage portfolio weights using mean-variance optimization and alternatives
- How to use machine learning to optimize asset allocation in a portfolio context

### Chapter 06: The Machine Learning Process

this [chapter](06_machine_learning_process) covers:

- How supervised and unsupervised learning using data works
- How to apply the ML workflow
- How to formulate loss functions for regression and classification
- How to train and evaluate supervised learning models
- How the bias-variance trade-off impacts prediction errors
- How to diagnose and address prediction errors 
- How to train a model using cross-validation to manage the bias-variance trade-off 
- How to implement cross-validation using scikit-learn
- Why the nature of financial data requires different approaches to out-of-sample testing

### Chapter 07: Linear Models for Regression & Classification

[Chapter 07](07_linear_models) covers:

- How linear regression works and which assumptions it makes
- How to train and diagnose linear regression models
- How to use linear regression to predict future returns
- How use regularization to improve the predictive performance
- How logistic regression works
- How to convert a regression into a classification problem
- How to design a trading algorithm based on price predictions generated by a ML model

### Chapter 08: Linear Time Series Models

 This [chapter](08_time_series_models) topics:
- How to use time series analysis to diagnose diagnostic statistics that inform the modeling process
- How to estimate and diagnose autoregressive and moving-average time series models
- How to build Autoregressive Conditional Heteroskedasticity (ARCH) models to predict volatility
- How to build vector autoregressive models
- How to use cointegration for a pairs trading strategy

### Chapter 09: Bayesian Machine Learning

This [chapter](09_bayesian_machine_learning) covers:
- How Bayesian statistics apply to machine learning
- How to use probabilistic programming with PyMC3
- How to define and train machine learning models
- How to run state-of-the-art sampling methods to conduct approximate inference
- How to apply Bayesian ML to compute dynamic Sharpe ratios, build Bayesian classifiers, and estimate stochastic volatility

### Chapter 10: Decision Trees & Random Forests

This [chapter](10_decision_trees_random_forests) covers:
- How to use decision trees for regression and classification
- How to gain insights from decision trees and visualize the decision rules learned from the data
- Why ensemble models tend to deliver superior results
- How bootstrap aggregation addresses the overfitting challenges of decision trees
- How to train, tune, and interpret random forests

### Chapter 11: Gradient Boosting Machines

This [chapter](11_gradient_boosting_machines) explores boosting, an alternative tree-based ensemble algorithm that often produces better results. The key difference is that boosting modifies the data that is used to train each tree based on the cumulative errors made by the model before adding the new tree. In contrast to random forests, which train many trees independently from each other using different versions of the training set, boosting proceeds sequentially using reweighted versions of the data. State-of-the-art boosting implementations also adopt the randomization strategies of random forests. 

More specifically, in this chapter we will cover the following topics:
- How boosting works, and how it compares to bagging
- How boosting has evolved from adaptive to gradient boosting (GB)
- How to use and tune AdaBoost and GB models with sklearn
- How state-of-the-art GB implementations speed up computation
- How to prevent overfitting of GB models
- How to build, tune, and evaluate GB models using xgboost, lightgbm, and catboost
- How to interpret and gain insights from GM models using [SHAP](https://github.com/slundberg/shap) values

### Chapter 12: Unsupervised Learning

Dimensionality reduction and clustering are the main tasks for unsupervised learning: 
- Dimensionality reduction transforms the existing features into a new, smaller set while minimizing the loss of information. A broad range of algorithms exists that differ by how they measure the loss of information, whether they apply linear or non-linear transformations or the constraints they impose on the new feature set. 
- Clustering algorithms identify and group similar observations or features instead of identifying new features. Algorithms differ in how they define the similarity of observations and their assumptions about the resulting groups.

More specifically, this [chapter](12_unsupervised_learning) covers:
- how principal and independent component analysis perform linear dimensionality reduction
- how to apply PCA to identify risk factors and eigen portfolios from asset returns 
- how to use non-linear manifold learning to summarize high-dimensional data for effective visualization
- how to use T-SNE and UMAP to explore high-dimensional alternative image data
- how k-Means, hierarchical, and density-based clustering algorithms work
- how to apply agglomerative clustering to build robust portfolios according to hierarchical risk parity

### Chapter 13:	Working with Text Data

This [chapter](13_working_with_text_data) introduces text feature extraction techniques and covers:
- What the NLP workflow looks like
- How to build a multilingual feature extraction pipeline using spaCy and Textblob
- How to perform NLP tasks like parts-of-speech tagging or named entity recognition
- How to convert tokens to numbers using the document-term matrix
- How to classify text using the Naive Bayes model
- How to perform sentiment analysis

### Chapter 14:	Topic Modeling

Unsupervised learning to model latent topics and extract hidden themes from documents. They speed up the review of documents, help identify and cluster similar documents, and can be annotated as a basis for predictive modeling. Applications include the identification of key themes in company disclosures or earnings call transcripts, customer reviews or contracts, annotated using, e.g., sentiment analysis or direct labeling with subsequent asset returns. More specifically, this chapter covers:
- What topic modeling achieves, why it matters and how it has evolved
- How Latent Semantic Indexing (LSI) reduces the dimensionality of the DTM
- How probabilistic Latent Semantic Analysis (pLSA) uses a generative model to extract topics
- How Latent Dirichlet Allocation (LDA) refines pLSA and why it is the most popular topic model
- How to visualize and evaluate topic modeling results
- How to implement LDA using sklearn and gensim
- How to apply topic modeling to collections of earnings calls and Yelp business reviews

### Chapter 15:	Word Vector Embeddings

Neural networks to learn a vector representation of individual semantic units like a word or a paragraph.
- What word embeddings are, how they work and capture semantic information
- How to use trained word vectors
- Which network architectures are useful to train word2vec models
- How to train a word2vec model using keras, gensim, and TensorFlow
- How to visualize and evaluate the quality of word vectors
- How to train a word2vec model using SEC filings
- How doc2vec extends word2vec

### Chapter 16:	Deep Learning

[Deep Learning](16_deep_learning/16_Deep_Learning.pdf) chapter will cover:
- How DL solves AI challenges in complex domains
- How key innovations have propelled DL to its current popularity
- How feed-forward networks learn representations from data
- How to design and train deep neural networks in Python
- How to implement deep NN using Keras, TensorFlow, and PyTorch
- How to build and tune a deep NN to predict asset price moves

### Chapter 17:	Convolutional Neural Networks

CNNs are named after the linear algebra operation called convolution that replaces the general matrix multiplication typical of feed-forward networks. CNNs are designed to learn hierarchical feature representations from grid-like data. One of their shortcomings is that they do not learn spatial relationships, i.e., the relative positions of these features. 

[Convolutional Neural Networks](17_convolutional_neural_nets/17_Convolutional_Neural_Networks.pdf)

More specifically, this [chapter](17_convolutional_neural_nets) covers

- How CNNs use key building blocks to efficiently model grid-like data
- How to design CNN architectures using Keras and PyTorch
- How to train, tune and regularize CNN for various data types
- How to use transfer learning to streamline CNN, even with fewer data
- How Capsule Networks improve on CNN and may enable a new wave of innovation


### Chapter 18:	Recurrent Neural Networks

Each output is a function of both previous output and new data. Prominent architectures include Long Short-Term Memory (LSTM) and Gated Recurrent Units (GRU) that aim to overcome the challenge of vanishing gradients associated with learning long-range dependencies, where errors need to be propagated over many connections. 

RNNs have been successfully applied to various tasks that require mapping one or more input sequences to one or more output sequences and are particularly well suited to natural language. RNN can also be applied to univariate and multivariate time series to predict market or fundamental data. This chapter covers how RNN can model alternative text data using the word embeddings that we covered in [Chapter 15](15_word_embeddings) to classify the sentiment expressed in documents. 

[Recurrent Neural Networks](18_recurrent_neural_nets/18_Recurrent_Neural_Networks.pdf)

Most specifically, this chapter addresses:
- How to unroll and analyze the computational graph for an RNN
- How gated units learn to regulate an RNN’s memory from data to enable long-range dependencies
- How to design and train RNN for univariate and multivariate time series in Python
- How to leverage word embeddings for sentiment analysis with RNN


### Chapter 19:	Autoencoders & Generative Adversarial Networks

This [chapter](19_deep_unsupervised_learning) covers:

[Autoencoders & GANs](19_deep_unsupervised_learning/19_Autoencoders_and_GANs.pdf)

- Which types of autoencoders are of practical use and how they work
- How to build and train autoencoders using Python
- How GANs work, why they're useful, and how they could be applied to trading
- How to build GANs using Python


### Chapter 20:	Reinforcement Learning

Reinforcement Learning (RL) is a computational approach to goal-directed learning performed by an agent that interacts with a typically stochastic environment which the agent has incomplete information about. 

This [chapter](20_reinforcement_learning) shows how to formulate an RL problem and how to apply various solution methods. It covers model-based and model-free methods, introduces the [OpenAI Gym](https://gym.openai.com/) environment, and combines deep learning with RL to train an agent that navigates a complex environment.

More specifically,this chapter will cover:

[Reinforcement Learning](20_reinforcement_learning/20_Reinforcement_Learning.pdf)

- How to define a Markov Decision Problem (MDP)
- How to use Value and Policy Iteration to solve an MDP
- How to apply Q-learning in an environment with discrete states and actions
- How to build and train a deep Q-learning agent in a continuous environment
- How to use OpenAI Gym to train an RL trading agent
