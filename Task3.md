##### 0109
- **Cross-Validation（交叉验证** https://zhuanlan.zhihu.com/p/24825503

  每次的测试集将不再只包含一个数据，而是多个，具体数目将根据K的选取决定。这个方法折中了LOOCV方法，即（Leave-one-out cross-validation）和The Validation Set Approach。
  K的选取是一个Bias和Variance的trade-off。

- **为什么文本分类则倾向于使用余弦来计算相似度？** 因为向量空间模型在实际使用中取得了很好的效果，可能是因为高维度中求欧式距离没有内积简单（经过归一化后）
  Euclidean distance is usually not good for sparse data (and more general case)?：https://stats.stackexchange.com/questions/29627/euclidean-distance-is-usually-not-good-for-sparse-data-and-more-general-case

**了解：TF-IDF与余弦相似度** https://zhuanlan.zhihu.com/p/32826433

*“找出相似文章”的一种算法：*
1. 使⽤用TF-IDF算法，找出两篇文章的关键词；
2. 每篇文章各取出若干个关键词（比如20个），合并成一个集合，计算每篇文章对于这个集合中的词的词频（为了避免文章长度的差异，可以使用相对词频）；
3. 生成两篇文章各自的词频向量；
4. 计算两个向量的余弦相似度，值越大就表示越相似。

后面的作图方式和task1，2类似，无需赘述。
##### 0110
- **iris dataset**: divided into "data" (four dimension, 150 datas) and "target" (every data has a corresponding target)

- knn, naive bayes, and logistic regressions... the methods are radically different but the procedures, dividing the dataset to a training set and a testing set,     are the same. 

- **a small serendipity about the parameter random_state** https://www.cnblogs.com/Yanjy-OnlyOne/p/11288098.html
When I compared three different way, including KNN, LR, and NB, strange things happened. Sometimes, in LR, an error occurred, saying "lbfgs failed to converge (status=1): STOP: TOTAL NO. of ITERATIONS REACHED LIMIT.", sometimes there was no error. Also, the probability of the prediction varies. The results are 1.0, 0.967 or 0.933. I wondered which parameter affected the probability. After changing some parameters, I discovered that random_state is the one that disturbs the result. Here is its definition:
> random_state: *int, RandomState instance or None, default=None*
> Controls the shuffling applied to the data before applying the split. Pass an int for reproducible output across multiple function calls. 

It means that if *random_state=None*, then everytime I run the codes, the data will be shuffled in different ways. But if I give an integrator to *random_state*, the way that shuffles the data will not change. So, I set a number, and steady the result. 

See more on https://scikit-learn.org/stable/glossary.html#term-random_state and https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.train_test_split.html?highlight=train_test_split#sklearn.model_selection.train_test_split

##### 0111
\> a = np.array([[1,4],[3,1]])

\> np.sort(a)                # sort along the last axis

array([[1, 4],

   [1, 3]])

\> np.sort(a, axis=None)     # sort the flattened array

array([1, 1, 3, 4])

\> np.sort(a, axis=0)        # sort along the first axis

array([[1, 1],

   [3, 4]])

numpy.newaxis: A convenient alias for None, useful for indexing arrays.

**An example here**      
https://github.com/Xiyu-Serena-Wan/datascience_workshop/issues/1#issuecomment-757886581

**numpy.sin(x)**

x:array_like  Angle, in radians (2 \pi rad equals 360 degrees).

**enumerate**  https://www.runoob.com/python/python-func-enumerate.html

enumerate() 函数用于将一个可遍历的数据对象(如列表、元组或字符串)组合为一个索引序列，同时列出数据和数据下标，一般用在 for 循环当中。

**KNeighborsRegressor** https://scikit-learn.org/stable/modules/generated/sklearn.neighbors.KNeighborsRegressor.html?highlight=kneighborsregressor#sklearn.neighbors.KNeighborsRegressor

之前是**KNeighborsClassifer**https://scikit-learn.org/stable/modules/generated/sklearn.neighbors.KNeighborsClassifier.html?highlight=kneighborsregressor

vs: https://stackoverflow.com/questions/52794075/sklearn-kneighborsregressor-vs-kneighborsclassifer

**matplotlib.pyplot.axis**https://matplotlib.org/3.3.3/api/_as_gen/matplotlib.pyplot.axis.html?highlight=axis%20tight

**matplotlib.tight_layout**https://matplotlib.org/3.3.3/api/tight_layout_api.html?highlight=tight_layout#module-matplotlib.tight_layout
