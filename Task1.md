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
