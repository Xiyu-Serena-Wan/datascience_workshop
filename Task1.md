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

###### notes in 1231
- what do targets mean? Names of the clusters?
- pandas.DataFrame( data, index, columns, dtype, copy) 很符合阅读习惯的可视化数据处理方式
- pd.Series(iris_target).value_counts() 利用value_counts函数查看每个类别数量
- iris_features.describe() 对于特征进行一些统计描述

##### notes in 0101
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
 
