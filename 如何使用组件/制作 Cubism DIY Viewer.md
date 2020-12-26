# 「Live2D Unity 文档翻译」制作 Cubism DIY Viewer

本文翻译自：https://docs.live2d.com/cubism-sdk-tutorials/use-cubismdiyviewer/

译者注：注意！这并不是一篇严谨的翻译，本人并不是翻译行业从业者，也根本不会日文。官网的中文翻译会连带代码一起翻译，而且还不如机翻日文，官网的英语翻译版本有的语法很奇怪，看起来也是机翻。本文主要来自日文机翻，然后再结合实际开发经验调整到通顺，修改不该翻译的东西并润色。

[最后更新日期: 2017/09/19] 译者注：这是这个日文原文的更新日期

by [Traitam](https://twitter.com/traitam)



在 Live2D 的 GitHub 上，您可以自己编译 Cubism DIY Viewer。

本节介绍如何创建该立体主义DIY查看器。

流程是在 Unity 上创建一个项目，对其进行构建，自定义，最后将其输出为应用程序。

## 为 Cubism DIY Viewer 创建 Unity 项目

首先，创建一个新的 Unity 项目，并将 SDK 的 unitypackage 添加到您的项目中。

有关导入 SDK 的信息，请参阅文章：[导入SDK](https://docs.live2d.com/cubism-sdk-tutorials/getting-started/)-放置模型中的 "将SDK导入项目"。



此外，需要最新版本的 SDK 组件才能处理此 Cubism DIY Viewer。

从下面的链接下载最新的 SDK 组件。

https://github.com/Live2D/CubismUnityComponents/tree/develop



在上一页中，在红色框中按 “Clone or download”，然后按 “Download ZIP” 来下载Zip压缩包。

![img](https://docs.live2d.com/wp-content/uploads/2017/08/2017-08-01_17h01_08-1.png)



下载并解压缩最新版本的 Cubism Unity Components。

把解压缩出来的 Assets 在资源管理器中覆盖上面创建的 Unity 项目的 Assets 文件夹

如果您在 Unity 中覆盖，那样文件夹名称将被重命名，因此请在资源管理器覆盖。

![img](https://docs.live2d.com/wp-content/uploads/2017/08/2017-08-02_10h47_23_02-1.png)

覆盖后，从下面的链接下载DIY Viewer。

https://github.com/Live2D/CubismViewer

就像下载最新的 SDK 一样，单击绿色按钮 “Clone or download”，然后单击 “Download ZIP” 开始下载。

下载后，解压缩并添加到 Unity。

将解压缩后文件夹中的 Assets 文件夹复制到与 Unity 中 Assets 文件夹相同的位置。

![img](https://docs.live2d.com/wp-content/uploads/2017/08/2017-08-02_10h51_29-1.png)

接下来是 Unity Editor 设置。 Unity Editor 中只有一项设置。

在 Unity 中选择 “Edit”→“Project Settings”→“Player”来打开 Player Settings 。

之后，打开 “Other Settings”，并将 “Configuration” 中的 “Api Compatibility Level“ 的  “.NET 2.0 Subset” 更改为 “ .NET 2.0”。

这样就完成了 Unity Editor 的设置。

![img](https://docs.live2d.com/wp-content/uploads/2017/08/2017-08-02_11h10_54-1.png)

![img](https://docs.live2d.com/wp-content/uploads/2017/08/2017-08-02_11h12_08-1.png)

## 添加所需的 DLL

添加 Viewer 时，我在 Unity 上遇到错误消息。可以复制并添加一个名为 System.Windows.Forms.dll 的文件来解决此错误。

如果 Unity 使用默认安装位置的话，这个文件位于 `C:/ProgramFiles/UnityEditor/Data/Mono/lib/mono2.0/System.Windows.Forms.dll`

在 Unity 上粘贴的位置是 “Assets/Live2D/Cubism/Viewer/Plugins/” 。

![img](https://docs.live2d.com/wp-content/uploads/2017/08/2017-08-02_10h57_22-1.png)

## 查看器场景创建

在当前项目中为 Viewer 创建一个场景。

右击 “Hierarchy” 窗口打开上下文菜单。

在菜单中单击 “Create Empty” 以创建一个空白的 Game Object。

将您创建的空 Game Object 对象重命名为 “CubismViewer”。

选择 "CubismViewer"，然后单击 'Inspector”>“Add Component”>“Cubism Viewer.cs”。之后，将添加的 CubismViewer 组件的 Camera 设置为 Main Camera 对象。

译注：先在 CubismViewer 上面附加 Cubism Viewer.cs，然后把 Main Camera 拖到 Camera 参数上

![img](https://docs.live2d.com/wp-content/uploads/2017/08/2017-08-03_10h58_50-1.png)

![img](https://docs.live2d.com/wp-content/uploads/2017/08/2017-08-09_15h10_40.png)



设置 Game Object 后，创建并设置按钮以调用场景中的进程。

右键单击 “Hierarchy” 窗口，然后选择 “UI”→“Button” 来创建按钮。

![img](https://docs.live2d.com/wp-content/uploads/2017/08/2017-08-02_11h22_12-1.png)

选择创建的按钮并设置 `OnClick()`。

在 `OnClick()` 上按 "+" 后，添加一个 `CubismViewer` 对象。

![img](https://docs.live2d.com/wp-content/uploads/2017/08/2017-08-02_11h24_26-1.png)



选择 `CubismViewer.ShowFileDialog`。

![img](https://docs.live2d.com/wp-content/uploads/2017/08/2017-08-02_11h28_30-1.png)





这样就完成了 "Cubism DIY Viewer" 项目的创建。

要显示模型，请按照以下步骤操作。

运行场景并按按钮来打开文件选择窗口。

然后选择 `.model3.json`。

![img](https://docs.live2d.com/wp-content/uploads/2017/08/2017-08-02_11h37_11-1.png)

## 定制 Gems

使用 model3.json 的动作时，将 `Gems/Animation/SimpleAnimator.cs` 添加到 `CubismViewer` 对象。

在加载 .model3.json 后，可以以相同方式加载 .motion3.json，这样运动将应用于显示的模型。

请参阅 GitHub 上关于 Built-in Gems，User Gems 的链接。

https://github.com/Live2D/CubismViewer#built-in-gems



## 导出为 exe 文件

最后，将此项目导出为 standalone（独立）的应用程序。

导出之前，请先保存上面创建的场景。



按 “File”→“Build Settings” 以配置构建设置。

按 “Add Open Scenes” 将刚刚保存的场景添加到 “Scenes In Build” 中。



最后，按 'Build' 或 “Build And Run”，然后输入要创建的 exe 的名称。

![img](https://docs.live2d.com/wp-content/uploads/2017/08/2017-08-02_11h45_18-1.png)



如果单击“生成并运行”，则在生成完成后，exe 将自动启动。

如果配置没有错误，则可以像在 Unity 上一样加载和显示模型。

![img](https://docs.live2d.com/wp-content/uploads/2017/08/2017-08-02_12h11_04-1.png)