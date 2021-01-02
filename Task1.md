###### functions I learned in 1230
- matplotlib.pyplot.scatter
- matplotlib.pyplot.xlim
Calling this function with no arguments (e.g. xlim()) is the pyplot equivalent of calling get_xlim on the current axes. Calling this function with arguments is the pyplot equivalent of calling set_xlim on the current axes. All arguments are passed though.
- matplotlib.pyplot.contour(*args, data=None, **kwargs)

- np.meshgrid
- np.linspace
- np.c_
- np.ravel()

- LogisticRegression.predict_proba
- LogisticRegression.predict
- https://zhuanlan.zhihu.com/p/28408516

###### notes in 1231
- what do targets mean? Names of the clusters?
- pandas.DataFrame( data, index, columns, dtype, copy) 很符合阅读习惯的可视化数据处理方式
- pd.Series(iris_target).value_counts() 利用value_counts函数查看每个类别数量
- iris_features.describe() 对于特征进行一些统计描述

###### notes in 0101
- iris_all['target'] = iris_target print(iris_all['target'] ) 是否是print one column, using the formal structure？具体怎么置换函数中的某一个参数还不会。
- sns.pairplot(data=iris_all,diag_kind='hist', hue= 'target') 
  hue: Variable in data to map plot aspects to different colors; 
  diag_kind: Kind of plot for the diagonal subplots. hist 直方图
- sns.boxplot(x='target', y=col, saturation=0.5,palette='pastel', data=iris_all) 
  箱形图（或盒须图）以一种利于变量之间比较或不同分类变量层次之间比较的方式来展示定量数据的分布。图中矩形框显示数据集的上下四分位数，而矩形框中延伸出的线段（触须）则用于显示其余数据的分布位置，剩下超过上下四分位间距的数据点则被视为“异常值”。
  saturation：控制用于绘制颜色的原始饱和度的比例。通常大幅填充在轻微不饱和的颜色下看起来更好，如果您希望绘图颜色与输入颜色规格完美匹配可将其设置为1。
  palette：调色板名称
- add_subplot *Add an Axes to the figure as part of a subplot arrangement.*
- kwargs and args: https://zhuanlan.zhihu.com/p/50804195
- iris_all_class0 = iris_all[iris_all['target']==0].values *在返回向量时多加了target维*
 
###### notes in 0102
- sklearn.model_selection.train_test_split(*arrays, test_size=None, train_size=None, random_state=None, shuffle=True, stratify=None) *Split arrays or matrices into random train and test subsets* 
*arrays：可以是lists,np.array,pd.DataFrame，下面是options的内容
test_size：float类型，必须是[0,1]之间，代表测试集占总数据集的比例。也可以是int类型，代表测试集的实际数量。如果给出的是None，则所有的集合都是训练集。默认是0.25
train_size：和上面一样
random_state：随机数种子。确保每次运行可以得到一样的结果。从反面来说，设为不同的值，得到不同的数据切分。
shuffle：是否重新洗牌，默认为True。即将你的数据集打乱，重新拍列。
stratify：按照一定的比例抽取样本。
- 数据选取 iloc loc ix：loc中的数据是列名，是字符串，所以前后都要取；iloc中数据是int整型，所以是Python默认的前闭后开。即loc[0:1]取第0列和第1列和iloc[0:1]取第0行
- 在LogisticRegression类中，fit(X,y)方法用于训练LR分类器，其中X是训练样本，y是对应的标记向量target
- sklearn.metrics.confusion_matrix(y_true, y_pred, *, labels=None, sample_weight=None, normalize=None) *Compute confusion matrix to evaluate the accuracy of a classification.* 在机器学习领域，混淆矩阵（confusion matrix），又称为可能性表格或是错误矩阵。它是一种特定的矩阵用来呈现算法性能的可视化效果，通常是监督学习（非监督学习，通常用匹配矩阵：matching matrix）。其每一列代表预测值，每一行代表的是实际的类别。这个名字来源于它可以非常容易的表明多个类别是否有混淆（也就是一个class被预测成另一个class）。https://blog.csdn.net/vesper305/article/details/44927047
- sklearn.metrics.accuracy_score(y_true, y_pred, *, normalize=True, sample_weight=None)
Accuracy classification score.
In multilabel classification, this function computes subset accuracy: the set of labels predicted for a sample must exactly match the corresponding set of labels in y_true.

