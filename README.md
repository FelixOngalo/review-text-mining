# Customer Review Text Mining in R

## Overview

This project applies **text mining and natural language processing techniques in R** to analyse customer review text and extract meaningful patterns from unstructured data.

The analysis combines three complementary approaches:

- **TF-IDF** for identifying terms that are particularly important within individual reviews.
- **Lexicon-based sentiment analysis** for measuring positive and negative sentiment.
- **Latent Dirichlet Allocation (LDA)** for discovering underlying topics across the collection of reviews.

The results are then **validated against engineered ground truth**, providing a way to evaluate whether the text-based methods produce results consistent with known or constructed expectations.

## Objectives

The project aims to answer three main questions:

1. **Which words are most important within individual customer reviews?**
2. **What sentiment is expressed in the reviews?**
3. **What underlying themes or topics appear across the reviews?**

Rather than relying on a single text-mining technique, the project compares different representations of the same textual data.

## Methods

### 1. TF-IDF

Term Frequency–Inverse Document Frequency (TF-IDF) is used to identify terms that are relatively important within a document while reducing the influence of words that occur frequently across the entire corpus.

The analysis considers:

- Term frequency
- Document frequency
- Inverse document frequency
- TF-IDF weighting
- Ranking terms by their TF-IDF scores

This provides a quantitative representation of the importance of words within individual reviews.

### 2. Lexicon-Based Sentiment Analysis

Customer reviews are analysed using a sentiment lexicon to identify words associated with positive and negative sentiment.

The workflow includes:

- Tokenising review text
- Removing stop words and irrelevant terms
- Matching tokens against a sentiment lexicon
- Calculating sentiment scores
- Classifying reviews according to their resulting sentiment

The sentiment results are subsequently compared with the engineered ground truth.

### 3. LDA Topic Modeling

**Latent Dirichlet Allocation (LDA)** is used to identify latent topics within the review corpus.

The model treats each document as a mixture of topics and each topic as a probability distribution over words.

The analysis examines:

- Topic-word probabilities
- Document-topic probabilities
- Dominant topics
- Highly associated terms
- Interpretability of discovered topics

The objective is to determine whether the automatically discovered topics correspond to meaningful themes within the customer reviews.

## Validation Against Engineered Ground Truth

A key feature of the project is the use of **engineered ground truth**.

Instead of evaluating the results only through visual inspection, known patterns are deliberately incorporated into the data so that the performance of the text-mining methods can be assessed against an expected outcome.

The validation examines whether:

- TF-IDF identifies intentionally important terms;
- sentiment analysis correctly distinguishes positive and negative reviews;
- LDA recovers the underlying themes embedded within the review corpus.

This provides a controlled way of evaluating the methods and understanding their limitations.

## Workflow

```text
Customer Reviews
       │
       ▼
Text Cleaning & Tokenisation
       │
       ├───────────────┐
       ▼               ▼
     TF-IDF       Sentiment Analysis
       │               │
       ▼               ▼
Important Terms   Sentiment Scores
       │               │
       └───────┬───────┘
               │
               ▼
          LDA Topic Model
               │
               ▼
        Discovered Topics
               │
               ▼
      Validation Against
       Engineered Ground Truth
```

## R Implementation

The analysis is implemented in **R**, with the workflow designed to make the underlying text-processing steps explicit rather than relying entirely on high-level black-box functions.

The project covers:

- Data preparation
- Text cleaning
- Tokenisation
- Stop-word removal
- Term-frequency calculations
- TF-IDF transformation
- Lexicon-based sentiment scoring
- Document-term matrices
- LDA topic modeling
- Model interpretation
- Ground-truth validation
- Visualisation of results

## Key Concepts

### Text Mining
- Tokenisation
- Corpus construction
- Stop words
- Term frequency
- Document frequency
- TF-IDF

### Sentiment Analysis
- Sentiment lexicons
- Positive and negative word associations
- Sentiment scoring
- Classification
- Validation

### Topic Modeling
- Latent Dirichlet Allocation
- Topic-word distributions
- Document-topic distributions
- Topic interpretation
- Unsupervised learning

### Validation
- Engineered ground truth
- Expected versus observed results
- Method evaluation
- Error analysis

## Key Learning Outcomes

This project demonstrates the ability to:

- Transform unstructured text into analysable data.
- Apply statistical representations to textual information.
- Extract informative features using TF-IDF.
- Perform lexicon-based sentiment analysis.
- Apply an unsupervised topic-modeling method.
- Interpret probabilistic topic distributions.
- Validate analytical methods against known expectations.
- Identify limitations in automated text analysis.
- Implement a reproducible text-mining workflow in R.

## Limitations

Text mining methods have important limitations.

Lexicon-based sentiment analysis can struggle with:

- sarcasm;
- context-dependent meanings;
- negation;
- domain-specific language;
- mixed sentiment within a single review.

Similarly, LDA topics require interpretation and may produce topics that are mathematically coherent but difficult to label meaningfully.

The engineered ground truth provides a useful controlled validation framework, but it does not fully reproduce the complexity of real-world customer reviews.

## Purpose

This project forms part of an **R data analytics portfolio** and demonstrates how unstructured customer feedback can be transformed into quantitative information.

The central workflow is:

> **Extract → Represent → Model → Interpret → Validate**

The project therefore focuses not only on obtaining results, but also on evaluating whether those results are supported by evidence from a controlled validation framework.

## Technologies

- **R**
- Text mining
- Natural language processing
- TF-IDF
- Sentiment analysis
- LDA
- Data visualisation
- Statistical validation
