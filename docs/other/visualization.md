# 模型可视化

```keras.utils.visualize_util```模块提供了画出Keras模型的函数（利用graphviz）

该函数将画出模型结构图，并保存成图片：

```python
from keras.utils.visualize_util import plot
plot(model, to_file='model.png')
```

```plot```接收两个可选参数：

* ```show_shapes```：指定是否显示输出数据的形状，默认为```False```
* ```show_layer_names```:指定是否显示层名称,默认为```True```

我们也可以直接获取一个```pydot.Graph```对象，然后按照自己的需要配置它，例如，如果要在ipython中展示图片
```python
from IPython.display import SVG
from keras.utils.visualize_util import model_to_dot

SVG(model_to_dot(model).create(prog='dot', format='svg'))
```
