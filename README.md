
# Complex Word Classification

> Kaggle Community Prediction Competition for the AI Course

## Table of Contents
* [Overview](#overview)
* [Evaluation](#evaluation)
* [Data Description](#data-description)
* [Status](#status)
* [License](#license)

## Overview

Predicting which words are considered hard to understand for a given target population is a vital step in many Natural Language Processing applications such as text simplification. A system could simplify texts for second language learners, native speakers with low literacy levels, and people with reading disabilities. 
This task is commonly referred to as Complex Word Identification. Usually, this task is approached as a binary classification task in which systems predict a complexity value (complex vs. non-complex) for a set of target words in a text. In this challenge, the task is to predict the lexical complexity of a word in a sentence. 
A word which is considered to be complex has label 1, a word is considered to be simple (non-complex) has label 0.

## Evaluation

The evaluation metric for this competition is balanced accuracy score. This is a proper metric to compute the accuracy in binary classification problems where the dataset is imbalanced. It is defined as the average of recall obtained on each class:

**balanced_accuracy** = $\frac{sensitivity + specificity}{2}$

where

**sensitivity**  = **true positive rate** =  $\frac{TP}{TP + FN}$

**specificity** = **true negative rate** = $\frac{TN}{FP + TN}$

### Data Description
The data comes from three sources: biblical text, biomedical articles and proceedings of the European Parliament. These sources were selected as they contain a natural mixture of common language and difficult to understand expressions, whilst each containing vastly different domain-specific vocabulary. 
The training data consists of 7662 training examples, each training example is a row of the form (id, corpus, sentence, token, complex). The testing data consists of 1338 test examples, each test example is a row of the form (id, corpus, sentence, token). 
Notice that you have to infer the label 0 (the token is not complex) or 1 (the token is complex).

-   **train.xlsx**  - the training set
-   **test.xlsx**  - the test set
-   **sample_submission.csv**  - a sample submission file in the correct format, with some labels equal to 0, and some labels equal to 1.

*Use the Kaggle API to download the dataset:*

    kaggle competitions download -c ub-fmi-cti-2021-2022
    
## Status
Project is: *finished*. 

## License
>You can check out the full license [here](https://github.com/MaximTiberiu/New-Employee-Best-Match/blob/main/LICENSE).

This project is licensed under the terms of the **MIT** license.