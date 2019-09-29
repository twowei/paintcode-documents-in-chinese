# [颜色](_cover.md)

PaintCode 里有 3 种类型的颜色：

- 系统色
- 基础色（用户定义）
- 衍生色（用户定义）

**系统色**有黑色、白色、透明、红色、绿色、蓝色和几个深浅不一的灰色。你不能定义新的系统色，而且它们不会显示在库里。不过，你可以通过将颜色添加到库里，来创建你自己的颜色，它们可以是基本色和衍生色。

![Colors](./images/colors.png)

## 基础色

**基础色**是不依赖于任何其它颜色的简单色，你可以随时调整它，所有直接或间接与它相关的图形和库项（渐变、阴影……）都会相应地更新。

## 衍生色

[▶️衍生色视频，位于 Youbute](https://youtu.be/-WQNE_xyHNg)

**衍生色**是动态依赖于其他颜色的颜色。它是通过使用一些**内置颜色运算**从父颜色中衍生出来的：

- 改变透明度
- 改变色相
- 改变明度
- 改变饱和度
- 应用阴影
- 应用高亮
- 拷贝

![内置颜色运算](./images/built-in_operation.png)

当父颜色改变了，所有直接和间接的（通过其他颜色）衍生色都将自动更新。库中显示的颜色以层级树形式排列 —— 衍生色是基础色的子颜色。

## 使用颜色

有三种在你的**形状**中设置颜色的方式。

第一种，你可以通过**拖拽连接点**到一个画板中的形状，然后选择一个你想要连接该颜色的属性。**连接点**的位置是在库中颜色的旁边。如果一个颜色没有实际在文件中使用到，就会显示一个空心圆。

![Assign Color Connection](./images/assign_color_connection.png)

另一种使用颜色的方式是使用检查器里的 **Stroke** 或 **Fill** 按钮槽。当按钮槽是空的时候，意味着它的属性（描边或填充）还未被设置。当你点击按钮槽，会出现一个菜单来供你选择想要使用的颜色。这个菜单里同步了库里边的项，在菜单顶部还有系统色。

![Assign Color Well](./images/assign_color_well.png)

顺便一提，当你不想在你的**形状**中中使用颜色，只需要点击按钮槽左侧的紫色圆形 'X'。

第三种使用颜色的方式是在颜色**弹出按钮菜单**中选择颜色。

![Assign Color Popup](./images/assign_color_popup.png)

![Assign Color Popup Context](./images/assign_color_popup_context.png)

上面的三种设置颜色的方式效果都是一样的 —— 选择你觉得最方便的那个就好。

## 添加新颜色

有几种添加新颜色的方式：

- 点击库里颜色列表的最上边的 '+' 按钮
- 点击颜色弹出菜单上的 `'Add new color...'` 选项。这种方式会在这个弹出按钮中使用这个新创建的颜色。
- 按住 `'Command'` ，并单击检查器里的已经设置好颜色的按钮槽。通过这种方式可以在库中复制一份这个颜色。

当你在库中添加一个颜色，会出现一个颜色**编辑弹框**。（需要注意，你可以通过从别的文件里复制粘贴的带颜色的形状的方式来添加颜色，还可以通过双击一个[渐变](./Part.2.library.C.gradients.md)控件来添加）。

## 编辑颜色

你可以在库里双击一个颜色来编辑它。或者你也可以在检查器中点击按钮槽来显示颜色编辑弹框。

![Basic Color](./images/basiccolor.png)

文字输入框里的是颜色的名字。PaintCode 会为你生成所有的颜色名，不过你可以随时重命名让名字更具描述性。

有两种类型的颜色：“基础的” 和 “衍生的”。 基础色是 `'Base Color '` 设置为 `'None'` 的颜色。对于基础色，你只需要在颜色选择器里选择一个特定的颜色。你还可以用不同颜色格式设置精确的值，调整颜色球，或者使用弹窗右下角的取色器来吸取屏幕上的任意颜色。

通过给 `'Base Color'` 设置颜色，你就能得到一个“衍生的”色。对于衍生色，你需要为它进一步设置你想要的 **运算** 和 **数值**。例如，你可以将颜色设置为与库中已有的颜色相同，但不透明度设为 50%。这是一个极其有用的功能。

![Derived Color](./images/derivedcolor.png)

衍生色会随着它的父颜色的改变而自动更新。

## 删除颜色

当你试图删除一个已经在你的绘图里使用的颜色时，会弹出一个确认删除表，它会告知你如果你删除这个颜色，哪些形状和库项会受到影响。

![Delete Sheet](./images/delete_sheet.png)

当你删除了一个颜色时，在所有使用到它的形状、渐变、阴影和变量里会被替换成默认的红色。所有直接衍生于被删除颜色的颜色，会被转成基础色，但在视觉上会保持不变。

## 使颜色在生成代码和 Symbol 中表现为参数

要了解更多关于如何配置颜色和其他库项为参数，请阅读“[库项行为](./Part.2.library.A.core-concepts.md)”。