- ** Cross-Validation（交叉验证）** https://zhuanlan.zhihu.com/p/24825503
每次的测试集将不再只包含一个数据，而是多个，具体数目将根据K的选取决定。这个方法折中了LOOCV方法，即（Leave-one-out cross-validation）和The Validation Set Approach。
K的选取是一个Bias和Variance的trade-off。

- **为什么文本分类则倾向于使用余弦来计算相似度？** 因为向量空间模型在实际使用中取得了很好的效果，可能是因为高维度中求欧式距离没有内积简单（经过归一化后）
Euclidean distance is usually not good for sparse data (and more general case)?：https://stats.stackexchange.com/questions/29627/euclidean-distance-is-usually-not-good-for-sparse-data-and-more-general-case

了解：TF-IDF与余弦相似度 https://zhuanlan.zhihu.com/p/32826433

“找出相似文章”的一种算法：
1. 使⽤用TF-IDF算法，找出两篇文章的关键词；
2. 每篇文章各取出若干个关键词（比如20个），合并成一个集合，计算每篇文章对于这个集合中的词的词频（为了避免文章长度的差异，可以使用相对词频）；
3. 生成两篇文章各自的词频向量；
4. 计算两个向量的余弦相似度，值越大就表示越相似。




