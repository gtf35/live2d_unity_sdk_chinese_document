# 「Live2D Unity 文档翻译」使用 Pose 功能

本文翻译自：https://docs.live2d.com/cubism-sdk-tutorials/pose-unity

译者注：注意！这并不是一篇严谨的翻译，本人并不是翻译行业从业者，也根本不会日文。官网的中文翻译会连带代码一起翻译，而且还不如机翻日文，官网的英语翻译版本有的语法很奇怪，看起来也是机翻。本文主要来自日文机翻，然后再结合实际开发经验调整到通顺，修改不该翻译的东西并润色。

[最后更新日期: 2020/01/30] 译者注：这是这个日文原文的更新日期



此页面描述如何控制 Cubism 零件的显示状态。

[ [导入 SDK-放置模型 ](https://docs.live2d.com/cubism-sdk-tutorials/getting-started/)] 假设模型已经放置到项目中。

[单击此处](https://docs.live2d.com/cubism-editor-manual/pose-setting/)了解如何配置 Pose（译注：指的是美术设计阶段），然后[单击此处](https://docs.live2d.com/cubism-sdk-manual/pose-unity/)了解 SDK 中的 Pose 相关内容。



## 摘要

如果在 Unity 编辑器菜单中选中「Live2D/Cubism/OrignalWorkflow/Should Import As Original Workflow」导入的模型的话，生成的`Prefab` 将自动设置 `pose`。

如果要将 `Pose` 功能应用于没有上述设置的模型，则可以按照本文中介绍的步骤进行设置。

1. 清除 `AnimationClip Curves`
2. 在 OW 模式下重新导入模型

 ※ 在 OW 模式下重新导入模型时，除 `Pose` 设置外，还同时添加了 OW 的 `Cubism Update Controller` ，`Cubism Parameter Store` 和 `Cubism Expression Controller`。

## 1.清除 `AnimationClip Curves`

1.在 Unity 编辑器菜单中，选中 「Live2D/Cubism/OrignalWorkflow/Should Import As Original Workflow」。

![img](https://docs.live2d.com/wp-content/uploads/2019/03/check_ow_import.png)

2.在 Unity 编辑器菜单中，选中「Live2D/Cubism/OrignalWorkflow/Should Clear Animation Curves」。

![img](https://docs.live2d.com/wp-content/uploads/2019/03/check_clear_curves.png)

3.在 `Project` 窗口中，右击要配置的模型的文件夹，然后单击 「Reimport/重新导入」

![img](https://docs.live2d.com/wp-content/uploads/2019/03/model_reimport.png)

## 在 OW 模式下重新导入模型

1.在 Unity 编辑器菜单中，取消选中「Live2D/Cubism/OrignalWorkflow/Should Import As Original Workflow」。

![img](https://docs.live2d.com/wp-content/uploads/2019/03/checkout_clear_curves.png)

2.在 `Project` 窗口中，右击要重新导入的模型的文件夹，然后单击 「Reimport/重新导入」

![img](https://docs.live2d.com/wp-content/uploads/2019/03/model_reimport.png)