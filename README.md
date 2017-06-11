README.md
******************************************
For the limit space, we haven't show the ranking of feature importance
in our paper, so we put several files to describe feature selection in detail.

1) formula.pdf----the formula used tocompute the average impurity loss in GBDT
2) feaimp2.pdf----the figure of feature importance ranking in Module 2.
3) feaimp4.pdf----the figure of feature importance ranking in Module 4.

In feaimp2.pdf, the ranking of click ratio features and distinct count features
is higher than time-related features. Feature of \emph{average clicks on project}
has the highest score, and \emph{number of distinct IP} plays a vital role in 
classification. With observation of raw data, most cheating users click heavily on 
certain ad position or ad project averagely and their clicks are concentrated on 
a few of positions or projects, which means a higher click centrality. After feature 
selection, there are 11 time-related features in final classifier, which indicates that
time-related features have great contribution to cheater detection.

*******************************************