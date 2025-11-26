PROJECT REPORT – CUSTOMER LIFETIME VALUE (CLV) PREDICTION



1. Introduction

Customer Lifetime Value (CLV) is one of the most important metrics used by e-commerce and retail companies to understand the total monetary value a customer brings during their relationship with the business. Companies use CLV to plan marketing budgets, retention strategies, targeted campaigns, and personalized product recommendations.
In this project, CLV is predicted using machine learning based on customer purchase behavior derived from three uploaded e-commerce files (customer master, orders, and transactions). The objective is to preprocess the data, engineer meaningful features such as Recency, Frequency, Monetary Value (RFM), build a regression model, evaluate it, and generate actionable business insights.

2. Abstract

This project focuses on predicting Customer Lifetime Value using Python-based machine learning techniques. Three datasets were merged to generate customer-level aggregated metrics. The data was cleaned, missing values were handled, and key purchasing behavior features were engineered. A Random Forest regression model was trained to predict CLV using Frequency, Recency, Average Order Value, and Customer Age (tenure). The model achieved strong predictive accuracy and helped segment customers into high-value, medium-value, and low-value groups. The analysis provides insights that can help e-commerce companies optimize marketing spend and retention strategies.

3. Tools Used

Programming Language: Python

Libraries: Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn

Environment: Google Colab

Machine Learning Model: Random Forest Regressor

4. Steps Involved in Building the Project
Step 1: Data Import and Understanding

Three e-commerce files were uploaded into Google Colab:

customers.csv → customer demographics

orders.csv → order details

order_items.csv → transaction-level product data

The datasets were inspected for structure, missing values, duplicate entries, and consistency across keys.

Step 2: Data Cleaning & Preprocessing

Removed duplicates and invalid records

Converted date columns to datetime format

Handled missing order amounts using median imputation

Standardized customer IDs and merged tables using primary keys

Dropped incomplete rows that could distort model accuracy

Step 3: Feature Engineering

Customer-level metrics were generated from the merged dataset:

Recency: Days since last purchase

Frequency: Number of transactions per customer

Monetary Value: Total spend

Average Order Value: Revenue / Frequency

Customer Tenure: Days between first and last purchase

These features formed the basis of CLV prediction.

Step 4: Exploratory Data Analysis (EDA)

Visualizations were created using Matplotlib and Seaborn:

Distribution of customer spending

Relationship between Frequency and CLV

Recency vs Spending heatmap

Boxplots showing high-value vs low-value customer groups

EDA revealed that frequent buyers exhibited higher consistency in CLV, while long periods of inactivity reduced lifetime value.

Step 5: Model Building

A Random Forest Regressor was selected because it handles non-linear relationships and avoids overfitting.
Dataset split:

80% training

20% testing

Model parameters:

300 trees

Max depth optimized through grid search

Step 6: Model Evaluation

Metrics used:

MAE (Mean Absolute Error)

RMSE (Root Mean Square Error)

R² Score

Feature importance analysis showed:

Frequency

Monetary value

Recency

These were the strongest predictors of CLV.

Step 7: Customer Segmentation

Based on predicted CLV, customers were grouped using quantiles:

Top 25% → High Value

Middle 50% → Medium Value

Bottom 25% → Low Value

These segments help companies allocate marketing budgets efficiently.

5. Conclusion

This project demonstrates how machine learning can accurately predict Customer Lifetime Value using historical purchasing data. The Random Forest model provided strong accuracy and highlighted Frequency and Monetary Value as key drivers. The segmentation approach gives actionable insights to improve retention, optimize marketing, and increase customer profitability.

📄 PROJECT REPORT – MOVIE SUCCESS PREDICTION & SENTIMENT ANALYSIS


1. Introduction

The movie industry relies heavily on data to predict whether a film will perform well at the box office. Factors such as genre, budget, runtime, IMDB rating, and viewer sentiment significantly influence a film's success.
This project uses two uploaded movie datasets (movie metadata + movie reviews) to analyze sentiment, visualize patterns, and build a machine learning model to predict box office revenue.

2. Abstract

This project applies Natural Language Processing (NLP) and regression modeling to predict movie success. Viewer reviews were analyzed using VADER sentiment scoring, and metadata like budget, runtime, rating, and votes were combined with sentiment features. A Random Forest regression model was trained to estimate box office revenue. Sentiment trends were analyzed by genre, demonstrating that positive sentiment strongly correlates with movie success. The output provides insights useful for producers, marketers, and streaming platforms.

3. Tools Used

Programming Language: Python

Libraries: Pandas, NumPy, Seaborn, Matplotlib, NLTK (VADER), Scikit-learn

Machine Learning Model: Random Forest Regressor

Environment: Google Colab

4. Steps Involved in Building the Project
Step 1: Dataset Upload

Two files were uploaded:

movies_metadata.csv → film details such as budget, genres, rating, votes

movie_reviews.csv → user reviews for each movie

Both files were merged using Title or Movie ID.

Step 2: Data Cleaning

Converted numeric columns (budget, revenue, rating, votes)

Handled null values in reviews by replacing with empty text

Encoded genres through one-hot encoding

Ensured correct alignment between movies and reviews

Step 3: Sentiment Analysis Using VADER

The VADER tool was applied to each review:

Negative score

Neutral score

Positive score

Compound sentiment score

Multiple reviews per movie were aggregated using mean sentiment.

Step 4: Exploratory Data Analysis

Visualizations included:

Sentiment distribution across genres

Correlation heatmap between numeric features

Budget vs Revenue scatterplot

Reviews sentiment vs Revenue bar graph

Findings indicated that movies with high compound sentiment had significantly larger box office returns.

Step 5: Feature Engineering

Features used:

Budget

Runtime

Rating

Votes

Sentiment scores (pos, neg, compound)

Genre dummies

The target variable: Box Office Revenue.

Step 6: Model Building

A Random Forest Regressor was trained using:

300 trees

20% test split

Evaluation metrics used:

MAE

RMSE

R² score

Genre and sentiment features collectively improved prediction accuracy.

Step 7: Interpretation & Insights

Feature importance ranking showed:

Budget

Rating

Votes

Sentiment compound score

Genre-wise sentiment analysis revealed that Comedy and Action films received the highest positivity, correlating with higher revenues.

5. Conclusion

This project successfully combined NLP and machine learning to predict movie success. Sentiment analysis proved essential in improving accuracy and understanding audience perception. The predictive model and visual insights can assist filmmakers, producers, and streaming platforms in decision-making, marketing strategies, and investment planning.
