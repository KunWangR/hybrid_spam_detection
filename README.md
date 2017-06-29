Hybrid Spam Detection
======================
feature importance
-----------------------------------

For the limit space, we haven't show the ranking of feature importance in our paper, so we put several files to describe feature selection in detail.

1. formula.pdf----the formula used tocompute the average impurity loss in GBDT
2. feaimp2.pdf----the figure of feature importance ranking in Module 2.
3. feaimp4.pdf----the figure of feature importance ranking in Module 4.

For instance, the average impurity loss of feature *j* on 10 subtrees of GBDT is calculated by formula as follow. Fig.1 exhibits the top 20 features.

![formula for feature importance](/imgs/formula1.png)

Where, *M* is the number of subtrees and particularly, *M=10* in our experiment. $\hat{L}_{j}^{2}(T_m)$ is the impurity loss of feature $j$ on subtree $m$ that can be figured as follow.

![formula for feature importance](/imgs/formula2.png)

Where, *N* is the number of nodes of tree and *N-1* is the number of non-leaf nodes. *v_t* represents features related to node $t$. $\hat{i}_{t}^{2}$ is the square of reduced impurity after splitting node *t*.

In feaimp2.pdf (or in Fig.1), the ranking of click ratio features and distinct count features is higher than time-related features. Feature of **average clicks on project** has the highest score, and **number of distinct IP** plays a vital role in classification. With observation of raw data, most cheating users click heavily on certain ad position or ad project averagely and their clicks are concentrated on a few of positions or projects, which means a higher click centrality. After feature selection, there are 11 time-related features in final classifier, which indicates that time-related features have great contribution to cheater detection.

![features in Module2](/imgs/feaimp2.png)

\*\*\*\*\*\*\*\*Fig.1 Importances of Features in Module 2\*\*\*\*\*\*\*

In feaimp4.pdf (or in Fig.2), 31 features are selected for classifier in Module 4, insists of 21 time related features, 6 click centrality features and 3 category features. **IP_previous_second_freq_var**, which means the variance of IP frequency among seconds in last minute, has the highest rank, while **frequency of cookie click on position** is the least important.  The multi-granularities window features contribute most to classification task and ** period window features** own the highest importance score. 

![features in Module2](/imgs/feaimp4.png)

\*\*\*\*\*\*\*\*Fig.2 Importances of Features in Module 4\*\*\*\*\*\*\*

<script type="text/javascript" async src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-MML-AM_CHTML"> </script>
formula1: $$n==x$$

formula2: $$n!=x$$

formula3: (m==y)

formula4: [m!=y]

formula5: \(k==z\)

formula6: \[k!=z\]

