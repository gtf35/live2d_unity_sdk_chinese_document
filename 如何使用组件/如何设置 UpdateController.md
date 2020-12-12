# 「Live2D Unity 文档翻译」如何设置 UpdateController

本文翻译自：https://docs.live2d.com/cubism-sdk-tutorials/updatecontroller

译者注：注意！这并不是一篇严谨的翻译，本人并不是翻译行业从业者，也根本不会日文。官网的中文翻译会连带代码一起翻译，而且还不如机翻日文，官网的英语翻译版本有的语法很奇怪，看起来也是机翻。本文主要来自日文机翻，然后再结合实际开发经验调整到通顺，修改不该翻译的东西并润色。

[最后更新日期: 2019/03/28] 译者注：这是这个日文原文的更新日期



该页面描述了在 Unity 中控制 Cubism 每个组件的执行顺序的步骤。

[ [导入 SDK-放置模型 ](https://docs.live2d.com/cubism-sdk-tutorials/getting-started/)] 假设模型已经放置到项目中。

## 摘要

使用 `CubismUpdateController` 来控制每个组件的执行顺序。

如果您在 Unity 编辑器菜单中选中「Live2D/Cubism/OrignalWorkflow/Should Import As Original Workflow」之后导入模型，则将自动在生成的 Prefab 中设置该组件。

如果要控制不具有上述设置的模型中每个 Cubism 的组件的更新顺序，则可以按照本文中描述的过程进行设置。

要在您的 `Cubism` 模型上设置  `UpdateController`，请按照下列步骤操作：

1. 附加 `CubismUpdateController`

## 附加 `CubismUpdateController`

将控制组件更新顺序的 `CubismUpdateController` 附加到模型所在的 `GameObject`。

![img](https://docs.live2d.com/wp-content/uploads/2019/03/update_attach.png)