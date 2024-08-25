---
layout: post
author: Name
title: "Applied Data Science Project Documentation"
categories: ITD214
---
## Project Background
This project aims to enhance the passenger experience on Singapore's Mass Rapid Transit (SMRT) system by analyzing key factors that influence reliability and by examining related social media posts. Through this analysis, we intend to uncover actionable insights and provide recommendations that will help SMRT improve service quality and meet our business objectives.

## Work Accomplished
As part of the project team, my focus was on conducting sentiment analysis of social media posts (X/Twitter) related to Singapore's Mass Rapid Transit (SMRT) system. I began by collecting and preprocessing the social media data to ensure it was sutiable for analysis. This involved removing irrelevant content, tokenizing the text, and normalizing it for consistency. I then applied sentiment analysius techniques using VADER model to seess public sentiment, identifying trends and key areas where passenger satisfaction was notably positive or negative. The insights derived from this analysis translated to the overall recommendations below.

### Data Preparation
The data preparation involved several key steps to ensure the text data was ready for sentiment analysis. First, missing values were handled by dropping posts with no text content. The text data was then converted to lowercase to maintain consistency, tokenization was performed before and after preprocessing to observe the impact on the word count. URLs, punctuation, and numbers were removed, followed by the elimination of stopwords and domain-specific terms. Lemmatization was applied to reduce words to their base forms, resulting in a cleaner and more relevant dataset. The processed text was then tokenized and joined back into strings for further analysis.

### Modelling
The sentiment analysis modeling phase included the application of multiple machine learning algorithms. Text data was vectorized using TF-IDF, transforming it into numerical features for model training. Logistic Regression, Random Forest, and XGBoost models were developed and fine-tuned using GridSearchCV to identify the best hyperparameters. Additionally, a deep learning model was constructed using a neural network architecture with dense and dropout layers to prevent overfitting. The deep learning model was trained on standardized features and one-hot encoded target variables to classify sentiments as positive, negative or neutral. 

### Evaluation
The evaluation phase focused on assessing the performance of the different models. The Logistic Regression, Random Forest, and XGBoost models were evaluated using metrics such as accuracy, classification reports, confusion matrices, and ROC-AUC scores. The deep learning model was also assessed based on its accuracy and loss during training and validation. The performance of each model was compared to identify the most accurate and reliable method for sentiment classification. These evaluations provided a comprehensive understanding of the models' strengths and weaknesses in predicting sentiment from  X/Twitter social media posts.

## Recommendation and Analysis
The sentiment analysis models provide valuable insights that can be used to enhance the passenger experience on Singapore's Mass Rapid Transit (SMRT) system. By identifying the prevailing sentiments among passengers, SMRT can address issues more proactively, such as improving train punctuality or enhancing customer service. The analysis of topic distributions alongside sentiment can also reveal specific areas of concern or satisfaction, allowing for targeted interventions. For instance, negative sentiments associated with particular stations or times of day could inform scheduling changes or infrastructure improvements.

## AI Ethics
The sentiment analysis project raises several AI ethics considerations. Privacy concerns are important, given the collection and processing of social media data, which requires careful and responsible handling of user-generated content to protect individuals' privacy. Ensuring fairness in the model is also critical to avoid biases that could lead to inaccurate representations of passenger sentiments. For example, passengers who stays in the eastern part of Singapore might naturally express more concerns related to East-West MRT line compared to those from other areas. Therefore, ensuring a balanced data distribution is essential to prevent any unfair bias in the model. Additionally, accuracy poses a significant challenge when analyzing social media posts. Social media is a personal platform where individuals express their thoughts freely, often using sarcasm or other nuanced language that can be difficult to interpret through text analysis. Misinterpretation of such subtleties could lead to inaccuracies in sentiment classification, underscoring the need for careful model design and validation.   

## Source Codes and Datasets
https://github.com/qyuanwen/itd214_proj
