# Donors-Choose-Classification
Task is to classify the projects for the approval for donation.

## Description:
DonorsChoose.org receives hundreds of thousands of project proposals each year for classroom projects in need of funding. Right now, a large number of volunteers is needed to manually screen each submission before it's approved to be posted on the DonorsChoose.org website.

The goal of the competition is to predict whether or not a DonorsChoose.org project proposal submitted by a teacher will be approved, using the text of project descriptions which are processed by NLP techniques as well as additional metadata about the project, teacher, and school(nominal features). DonorsChoose.org can then use this information to identify projects most likely to need further review before approval.

#### Dataset link: https://www.kaggle.com/c/donorschoose-application-screening/overview

### Metrics: ROC_AUC Curve, AUC score.

## Results:
| Vectorizer | Model  |test AUC|
|------------|--------|-------|
|    BOW   |    NB  |0.6904 |
|    TFIDF |    DT  | 0.8297 |
|    TFIDFW2V |    GBDT  | 0.8825 |
|    - |    LSTM + Conv1D  | 0.7705 |

Gradient Boosted Decision Tress with TFIDFW2V gives the AUC score of 0.8825 on Test data.

## Contains 6 files:
1) EDA.ipynb – Exploratory Data Analysis on Data.
2) Preprocessing.ipynb – Pre-processing the Nominal features and Text data.
3) NB.ipynb – Naive Bayes on processed data.
4) DT.ipynb – Decision Tress on processed data.
5) GBDT.ipynb – Gradient Boosted Trees(XGBoost) on processed data.
6) LSTM.ipynb - LSTM and Conv1D on processed data.

