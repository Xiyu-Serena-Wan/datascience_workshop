1. #### 为什么有了logistic regression，还要学习朴素贝叶斯？ 

Source: https://www.cs.cmu.edu/~tom/mlbook/NBayesLogReg.pdf
> ##### Relationship Between Naive Bayes Classifiers and Logistic Regression
> To summarize, Logistic Regression directly estimates the parameters of P(Y|X), whereas Naive Bayes directly estimates parameters for P(Y) and P(X|Y). 
> The assumptions of one variant of a Gaussian Naive Bayes classifier imply the parametric form of P(Y|X) used in Logistic Regression. Furthermore, the parameters wi in Logistic Regression can be expressed in terms of the Gaussian Naive Bayes parameters. 
> In fact, if the GNB assumptions hold, then asymptotically the GNB and Logistic Regression converge toward **identical classifiers**.

> The two algorithms also differ in interesting ways:
> - When the GNB modeling assumptions do not hold, Logistic Regression and GNB typically learn different classifier functions. In this case, the **asymptotic classification accuracy** for Logistic Regression is often better than the asymptotic accuracy of GNB. Although Logistic Regression is consistent with the Naive
Bayes assumption that the input features Xi are conditionally independent given Y, it is not **rigidly tied to this assumption** as is Naive Bayes. Given
data that disobeys this assumption, the conditional likelihood maximization algorithm for Logistic Regression will **adjust its parameters to maximize the
fit to (the conditional likelihood of) the data**, even if the resulting parameters > are inconsistent with the Naive Bayes parameter estimates.
> - GNB and Logistic Regression converge toward their asymptotic accuracies at different rates. As Ng & Jordan (2002) show, GNB parameter estimates converge toward their asymptotic values in order **logn** examples, where n is the dimension of X. In contrast, Logistic Regression parameter estimates converge more slowly, requiring order **n** examples. 
> - The authors also show that in several data sets Logistic Regression outperforms GNB when many training examples are available, but GNB outperforms Logistic Regression when training data is scarce.

2. #### 
