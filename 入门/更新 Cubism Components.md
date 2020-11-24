# 「Live2D Unity 文档翻译」更新 Cubism Components

本文翻译自：https://docs.live2d.com/cubism-sdk-tutorials/update-components/

译者注：注意！这并不是一篇严谨的翻译，本人并不是翻译行业从业者，也根本不会日文。官网的中文翻译会连带代码一起翻译，而且还不如机翻日文，官网的英语翻译版本有的语法很奇怪，看起来也是机翻。本文主要来自日文机翻，然后再结合实际开发经验调整到通顺，修改不该翻译的东西并润色。

[最后更新日期: 2019/01/30] 译者注：这是这个日文原文的更新日期

本节描述如何用最新的软件包替换已经[[导入SDK-放置模型](https://docs.live2d.com/cubism-sdk-tutorials/getting-started/)]的Unity项目。

## 概要

有两种获取 Cubism SDK 的方法：发布的软件包和 GitHub。

该软件包包含发布时最新的 Core 库和 Cubism Components，以及使用它们的示例。

请按照以下步骤将您 Unity 项目中的 Cubism SDK 更新。

如果您不熟悉 Unity，请在更新之前对项目进行备份。

## 获取最新版

从 [Cubism SDK 下载页面](https://www.live2d.com/download/cubism-sdk/)获取最新的软件包。

## 您的 Unity 项目更新到最新版

将新版本覆盖到现有的 Unity 项目时，可能无法继续在 Unity 端使用 Cubism Core。（译注：应该就是有报错的意思）

在这种情况下，请按照以下步骤进行更新。

1. 保存当前正在使用的所有场景。
2. 保存完后，用 “ Ctrl + N” 等创建一个新场景。
3. 用创建的新场景重新启动 Unity。
4. Unity启动后，覆盖最新的软件包。

覆盖后，如果没有编译错误，则当前 Unity 项目的 Cubism SDK 已经更新完成。

如果此时发生编译错误，则可能是以下原因。

- 项目中可能自定义了包含在上述软件包中的类
- 项目中已经存在同名的类

**Tips**

从 2019 年 8 月 1 日发布的 Cubism 4 SDK for Unity beta13 起，Cubism SDK 与 Cubism 4.0 兼容。

与以前一样，从Cubism 4编辑器导出的嵌入数据的格式为 .moc3，但是由于添加的功能（如掩码反转）不向下兼容，因此 Cubism 3 SDK 无法使用 Cubism 4 导出的 .moc3。

相反，Cubism 4 SDK 可以读取 Cubism 3 格式的 .moc3。

根据上面的内容，我们建议您从现在开始创建项目时使用 Cubism 4 SDK。

|            |          | Cubism SDK ver | Cubism SDK ver |
| ---------- | -------- | -------------- | -------------- |
|            |          | Cubism 3       | Cubism 4       |
| .moc3 版本 | Cubism 3 | ◯              | ◯              |
| .moc3 版本 | Cubism 4 | ×              | ◯              |

