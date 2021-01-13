#### 0106
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

2. #### fit(X, y, sample_weight=None)
Fit Gaussian Naive Bayes according to X, y

Parameters
X: array-like of shape (n_samples, n_features) In here, n_samples=150, n_features=4
Training vectors, where n_samples is the number of samples and n_features is the number of features.

y: array-like of shape (n_samples,) In here, n_samples=150, one-dimension
Target values.

sample_weight: array-like of shape (n_samples,), default=None
Weights applied to individual samples (1. for unweighted).

Returns
self:object

3. #### predict(X)
Perform classification on an array of test vectors X.

Parameters
X: array-like of shape (n_samples, n_features)

Returns
C: ndarray of shape (n_samples,)
Predicted target values for X

4. #### x.shape = (10,1024), x[0].shape, and x.shape[0]

x is a 2D array, which can also be looked upon as an array of 1D arrays, having 10 rows and 1024 columns. x[0] is the first 1D sub-array which has 1024 elements (there are 10 such 1D sub-arrays in x), and x[0].shape gives the shape of that sub-array, which happens to be a 1-tuple - (1024, ).

On the other hand, x.shape is a 2-tuple which represents the shape of x, which in this case is (10, 1024). x.shape[0] gives the first element in that tuple, which is 10.

#### 0107
1. ##### np.random.RandomState(1)
It's a class, containing functions to create arrays with random numbers. The paramenter 1 means that the numbers will not change everytime it generates.

2. ##### What does [:,:-1] and [:,-1] mean?
[:,:-1]: This will take all rows and all but the last column.

[:,-1]: This will take all rows and the last column.

: denotes "all", and -1 in indexing means the last row/column.

3. ##### logistic 分类二元/大型，朴素贝叶斯分类多元/小型
