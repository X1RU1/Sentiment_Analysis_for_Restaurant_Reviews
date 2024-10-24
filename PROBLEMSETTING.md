# Sentiment Analysis with Reinforcement Learning for Restaurant Reviews

## Problem Setting
The project is sentiment analysis applied to restaurant reviews using a combination of Language Models (LLM) and Reinforcement Learning (RL). The aim is to classify the sentiment of comments extracted from reviews of restaurants. Each comment will be initially processed using LLM to predict its sentiment class, which will be further refined using existing ratings from the dataset through Reinforcement Learning. 
Given a sequence of restaurant reviews, $s = {s_{1}, s_{2}, \dots, s_{n}}$, where $s_{i}$ represents the $i{th}$ comment in the sequence, the goal is to find a model, $f(s)$, capable of predicting a sentiment label, $y$, where $y \in { 0, 1 }$. The sentiment scores $y$ will be categorized into 2 classes: 0 (negative) and 1 (positive). 

## Dataset Acquisition
 The dataset comes from [[1]](#1). It contains customer reviews (text) and an indicator of whether they liked the restaurant or not.

## Evaluation Protocol
For the evaluation, the LM will be first run with normal fine-tuning, and then compared with RL fine-tuned model.
As a statistical baseline, majority voting will be used. Random forest classifier will be used as a simple machine learning baseline.
Given that sentiment analysis is essentially a binary classification problem, the models will be evaluated using a threshold-independent metric - AUROC. Moreover, accuracy, precision, recall, and F1-score can be used to assess the model's performance across different sentiment classes. 


## References
<a id="1">[1]</a>
A. Anwar, “Restaurant Reviews,” www.kaggle.com, 2021. https://www.kaggle.com/datasets/d4rklucif3r/restaurant-reviews?resource=download (accessed Mar. 17, 2024).
