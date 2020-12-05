# 「Live2D Unity 文档翻译」如何在模型的 Drawable 之间插入精灵

本文翻译自：https://docs.live2d.com/cubism-sdk-tutorials/betweendrawables/

译者注：注意！这并不是一篇严谨的翻译，本人并不是翻译行业从业者，也根本不会日文。官网的中文翻译会连带代码一起翻译，而且还不如机翻日文，官网的英语翻译版本有的语法很奇怪，看起来也是机翻。本文主要来自日文机翻，然后再结合实际开发经验调整到通顺，修改不该翻译的东西并润色。

[最后更新日期: 2020/01/30] 译者注：这是这个日文原文的更新日期	



本节将说明如何在模型 drawable 之间放置另一个精灵。

## 概览

如果您想在模型的图层之间绘制，则可以通过配置模型的 Cubism Renderer 来更改 drawable 的绘制顺序。

可以通过修改「Local Order」的数值来控制绘图顺序。

当将子图形放置在模型的固定零件之间时，可以在子图形的前面绘制一些 Drawable ，并在子图形的背面绘制其他Drawable。

## 步骤

首先，更改附加到模型根目录的 CubismRenderController 组件的 Order In Layer 编号。

然后更改每个 Drawable 上附加的 CubismRenderer 组件上 LocalOrder 中设置的数字。

模型根部的 CubismRenderController 的 Order In Layer 也会影响 /Drawables/ 下所有对象的 Local Order。



例如，如果在图层中的顺序为 "0" 时将 "Local Order" 设置为 "1"，则设置的 Drawable 的绘制顺序将为 1。

此外，如果在图层中的顺序为 "3" 时将 "Local Order" 设置为 "2"，则设置的 Drawable 的绘制顺序将为 5。

如果在图层中的顺序为 "5" 时将 "Local Order" 设置为 "-2"，则 Drawable 的绘制顺序将为 3。

有关图层绘制的详细说明，请参见下面的链接。

[Unity - 手册: Sprite Renderer](https://docs.unity3d.com/Manual/class-SpriteRenderer.html)





如果要在 Drawable 和 Drawble 之间放置另一个精灵，如下所示，请更改 CubismRenderer 组件的 Local Order 值。 

[drawable] [精灵] [drawable]

![img](https://docs.live2d.com/wp-content/uploads/2017/08/2017-08-17_15h45_12.png)

## 示例：使模型容纳精灵

例如，创建一个新的精灵，并将模型摆放在侧面。

![img](https://docs.live2d.com/wp-content/uploads/2017/09/2017-09-07_10h49_39.png)



首先，配置 Sprite。在 "层级(Hierarchy)" 窗口中右键，然后选择 "2D对象(2D Object)">"精灵(Sprite)" 来创建一个新的 Sprite。

然后单击您创建的 Sprite，并将 "检查器(Inspector)" 窗口中的 "Sprite Renderer> 精灵(Sprite)" 项设置为 UI Sprite。

另外，将 "Sprite Renderer">"图层顺序(Order In Layer)" 设置 "1"。

![img](https://docs.live2d.com/wp-content/uploads/2017/08/2017-08-17_17h40_16.png)



接下来，设置模型。

将模型左手和左前臂的 Local Order 值设置为 "2"。

这样，将按此顺序绘制：数值已更改的左手/左前臂→Sprite→未设置数值的模型。

![img](https://docs.live2d.com/wp-content/uploads/2017/08/2017-08-17_17h58_21.png)

![img](https://docs.live2d.com/wp-content/uploads/2017/08/2017-08-17_15h30_55.png)

