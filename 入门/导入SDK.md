# 「Live2D Unity 文档翻译」导入 SDK

本文翻译自：https://docs.live2d.com/cubism-sdk-tutorials/getting-started/

译者注：注意！这并不是一篇严谨的翻译，本人并不是翻译行业从业者，也根本不会日文。官网的中文翻译会连带代码一起翻译，而且还不如机翻日文，官网的英语翻译版本有的语法很奇怪，看起来也是机翻。本文主要来自日文机翻，然后再结合实际开发经验调整到通顺，修改不该翻译的东西并润色。

[最后更新日期: 2020/01/30] 译者注：这是这个文档日文原文的更新日期

这是一个教你把从 Cubism Editor 导出的动作档模型文件导入 Unity 项目并在屏幕上显示的教程。

## 需要提前准备

「Cubism 3」 及更高版本的 「Cubism SDK for Unity」 支持 [Unity](https://unity3d.com/) 版本是 2019.x。

如果低于 2018.3 版本，则 SDK 的 assets （.mat等）中序列化的信息将被丢弃。

了解有关安装 Unity 的更多信息请参考[这里](https://docs.unity3d.com/ja/Manual/InstallingUnity.html)。



另外， [Cubism SDK for Unity](https://www.live2d.com/download/cubism-sdk/) 也请提前下载好。

这是以 unity package 格式分发的。

Github 上也提供了 SDK，但是它不包含库，因此在嵌入模型时使用上述包。



在 SDK 中使用 Live2D 模型时，您需要将其导出为「动作档（.moc3）」，而不是 .cmo3 或 .can3。

点击[这里](https://docs.live2d.com/cubism-editor-manual/moc3-file/)了解如何导出。

导出的文件夹包括 .moc3 文件，.model3.json 文件和纹理。

请将它们放在同一个文件夹中。

## 将 SDK 导入项目

在 2D 模式下创建一个新的 Unity 项目，然后将 Cubism SDK for Unity（.unitypackage文件）拖放到「project」视图中以将其导入。

[点击](https://docs.unity3d.com/Manual/GettingStarted.html)了解如何新建 Unity 项目。

![img](https://docs.live2d.com/wp-content/uploads/2017/06/import01-e1497264949420.png)

![img](https://docs.live2d.com/wp-content/uploads/2017/06/import02.png)

导入完成后，关闭 Unity 并重新打开您的项目。

> Tips：
>
> 另外，如果在导入下述模型时发生错误，请在此时更新 Cubism Components。 有关更新 Cubism Components 的说明，请参见[此处](https://docs.live2d.com/cubism-sdk-tutorials/update-components/)。

## 导入模型

将从 Cubism Editor 导出的动作档模型集的文件夹拖放到「project」视图中。

![img](https://docs.live2d.com/wp-content/uploads/2017/06/import03.png)

如果导入成功，SDK 中包含的 Cubism Importer 将自动生成一个 Prefab（预制体）。生成的 Prefab 是一个 Live2D 模型的载体，可以与 Unity 一起使用。 在此之后，可以从 「Hierarchy」 视图中修改参数和零件的显示状态。

您可以通过将生成的 Prefab 添加到「Hierarchy」或「Scene」视图来放置模型并运行场景。

> Tips：
>
> 导入 Prefab 后，即使将其放置在场景中也不会立即显示在屏幕上。 这是因为 Cubism SDK for Unity 在每个帧更新过程中都会设置网格。 放置预制件后，请通过执行一次场景来显示它。

## 关于 Original Workflow 方式

[2019/01/31 追加]

使用从 R11 添加的 Original Workflow 方法导入模型时，将其拖放到 「project」 窗口中之前，在菜单栏上选择 「 Live2D>Cubism>Original Workflow>Should Import As Original Workflow」

![img](https://docs.live2d.com/wp-content/uploads/2017/06/2019-01-29_17h38_33.png)

如果您选中此复选框，则 OW 方法组件将附加到生成的 Prefab 当中。

![img](https://docs.live2d.com/wp-content/uploads/2017/06/2019-01-29_19h20_12.png)

> Tips
>
> 在上述过程中生成的 Prefab 的中心将是导出 moc3 时设置的 [模型中心X] 和 [模型中心Y] 的坐标。 另外，对于默认尺寸，在 [画布宽度 ]和 [画布高度] 中设置的值被视为 Unity 的单位。 点击[此处](https://docs.live2d.com/cubism-editor-manual/moc3-file/)了解更多。
>
> 另外，如果在控制台视图中显示 DllNotFoundException ，则由于尚未加载库而无法转换模型。
>
> ![img](https://docs.live2d.com/wp-content/uploads/2017/06/DllNotFoundException-1.png)
>
> 在不重新启动Unity的情况下导入模型时出现此错误。
>
> 但是，如果重新启动后仍然出现错误，则可能是使用该库的平台设置已更改。
>
> 在 Inspector 视图中，修改库平台设置。
>
> 库文件位于：
>
> *Assets/Live2D/Cubism/Core/[平台]/LibLive2DCubismCore*
>
> ![img](https://docs.live2d.com/wp-content/uploads/2017/06/dllsettings-e1497591722692.png)