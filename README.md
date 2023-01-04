# Automated-Fake-News-Detection
Fake News Projection using Deep Learning  in Python

In this project, we will use Natural Language Processing Techniques alongside Machine & Deep Learning

The goal of this project is to compare the accuracy of deep learning models against machine learning models
Later-on, we will then ensemble these models for any accuracy increase

# Dataset
Data will be a combination of two datasets: [LIAR Dataset](https://aclanthology.org/P17-2067/) by William Yang & [Fake and real news dataset](https://www.kaggle.com/datasets/clmentbisaillon/fake-and-real-news-dataset?select=True.csv) by Clement Bisalliion


### LIAR Dataset
Introduced by Wang in "Liar, Liar Pants on Fire": A New Benchmark Dataset for Fake News Detection the dataset contains 13 variables/columns for train, test & validation:

- Column 1: the ID of the statement ([ID].json)
- Column 2: the label (Label class contains: True, Mostly-true, Half-true, Barely-true, FALSE, Pants-fire)
- Column 3: the statement
- Column 4: the subject(s)
- Column 5: the speaker
- Column 6: the speaker's job title
- Column 7: the state info
- Column 8: the party affiliation
- Columns 9-13: the total credit history count, including the current statement
  - 9: barely true counts
  - 10: false counts
  - 11: half true counts
  - 12: mostly true counts
  - 13: pants on fire counts
- Column 14: the context (venue / location of the speech or statement)
- Column 15: the extracted justification

To simplify things, 2 variables will be used for classification. These are:
- Column 3: the statement
- Column 2: the label

The problem with the label column is it's multi-labeled. We will simplify this into a binary-label using the methodology below:

1. Original = New
2. True = True
3. Mostly-true = True
4. Half-true = True
5. Barely-true = False
6. False = False
7. Pants-fire = False

#### Fake and real news dataset
Created by Clement Bisaillon the dataset contains 4 variables/columns split True & Fake dataset:
- Column 1: the title of the article
- Column 2: the text of the article
- Column 3: the subject of the article
- Column 4: the date the article was posted
