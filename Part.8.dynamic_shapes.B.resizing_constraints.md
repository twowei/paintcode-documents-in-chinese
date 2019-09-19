# 缩放约束条件

你可以定义一个形状的缩放行为，通过使用检查器里的缩放约束条件：

![](images/constraints.png)

这个约束条件定义了一个形状和它的 `Frame` 间的关系。有有六种约束条件：left, right, top, bottom, width 和 height。

![](images/usedconstraints.png)

在定义形状和它的 `Frame` 间的关系时，水平的约束条件（left, width, right）是完全独立于纵向的。为了清晰起见，我们将指描述水平约束条件的行为。

每个约束条件既可以是严格的，也可以是宽松的（ `rigid`和`flexible`）。

左边的约束代表形状的左边和包围它的 `Frame` 的左边的距离。当左边的约束是严格的，那么无论你怎么调整 `Frame` 的大小，这个距离都不会改变。而当这个左边的约束是宽松的，那么 PaintCode 会根据另外两个（width，right）条件来尽让这个距离相应变大。

`width` 和 `right` 约束也是类似。你可以通过严格和宽松条件的特定组合，来实现各种有用的行为。

## 将固定宽度的形状剧中

![](images/dynamics1.png)

使形状按比例调整大小

![](images/dynamics2.png)

两边有固定边距的形状

![](images/dynamics3.png)

吸附到右边的形状

![](images/dynamics4.png)

吸附到左侧而且大小成比例变化的幸好组啊姑娘

![](images/dynamics5.png)
