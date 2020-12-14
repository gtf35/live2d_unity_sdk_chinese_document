# 「Live2D Unity 文档翻译」在 Mecanim 中启用动作淡入淡出

本文翻译自：https://docs.live2d.com/cubism-sdk-tutorials/motionfade/

译者注：注意！这并不是一篇严谨的翻译，本人并不是翻译行业从业者，也根本不会日文。官网的中文翻译会连带代码一起翻译，而且还不如机翻日文，官网的英语翻译版本有的语法很奇怪，看起来也是机翻。本文主要来自日文机翻，然后再结合实际开发经验调整到通顺，修改不该翻译的东西并润色。

[最后更新日期: 2020/01/30] 译者注：这是这个日文原文的更新日期



该页面描述了在 Unity 中控制 Cubism 每个组件的执行顺序的步骤。

[ [导入 SDK-放置模型 ](https://docs.live2d.com/cubism-sdk-tutorials/getting-started/)] 假设模型已经放置到项目中。

## 摘要

要使用淡入淡出功能，例如在 Unity 的 `motion3.json` 中设置了淡入淡出和运动淡入淡出功能，请在 Cubism SDK for Unity 中启用 「`MotionFade`」。

使用 `Cubism` 的淡入淡出功能，您可以更改在切换动作时动作单独和淡出的函数曲线，或者在仅更改特定参数的淡入淡出时间。

[单击此处](https://docs.live2d.com/cubism-editor-manual/fade-setting/)了解淡入淡出功能的详细信息。



在 Unity 编辑器菜单中选中「`Live2D/Cubism/OrignalWorkflow/Should Import As Original Workflow`」之后导入的模型。

这样会自动在模型上设置 `MotionFade`。



要在没有上述设置的型号上使用 `MotionFade`，请执行以下步骤。

1. 附加 `CubismFadeController`
2. 设置「模型名称.fadeMotionList」
3. 将 `CubismFadeStateObserver` 附加到 `AnimatorController` 的每一层

## 1.附加 CubismFadeController

将控制淡入淡出的 `CubismFadeController` 附加到模型的 `GameObject` 上。

![img](https://docs.live2d.com/wp-content/uploads/2019/03/fade_attach.png)

![img](https://docs.live2d.com/wp-content/uploads/2019/03/fade_attached.png)

- Cubism Fade Motion List：设置「模型名称.fadeMotionList」。详细信息将在步骤2中进行说明。

# 2. 设置「模型名称.fadeMotionList」

选择模型，然后将 `Modelname.fadeMotionList` 从「Inspector/层级」视图拖放到 `Cubism Fade Controller` 的 `Cubism Fade Motion List`。

![img](https://docs.live2d.com/wp-content/uploads/2019/03/set_fadeMotionList.png)

※ 选择 `AnimatiorController` 并将 `CubismFadeStateObserver` 附加到 `Animator` 窗口中每个图层的 `Inspector` 视图。

※ ".fade" 是存储运动数据的文件。它是从 motion3.json 自动生成的。

## 3. 将 `CubismFadeStateObserver` 附加到 `AnimatorController` 的每一层

选择 `AnimatiorController` 并将 `CubismFadeStateObserver` 附加到 `Animator` 窗口中每个图层的 `Inspector` 中。

![img](https://docs.live2d.com/wp-content/uploads/2019/03/fadeStateObserver_attach.png)

这样就完成了使用 `MotionFade` 控制淡入淡出。



如果在此状态下运行场景，则动画淡入时将会使用在 `CubismEditor` 中设置的淡入值。



以下是在有或没有 `MotionFade` 的情况下将 `Animator Controller` 的`MotionFade` 值设置为 0。

在左侧，由于未设置 MotionFade，因此它将在过渡设置的 0 秒处结束。

在右侧，设置了 MotionFade， Animator 过渡方式为 Cubism 的运动淡入淡出， 原有的参数值设置的淡入淡出将被覆盖。

![img](https://docs.live2d.com/wp-content/uploads/2019/09/Fade.gif)

*未附加 `CubismFadeStateObserver` 的图层将使用在 “Transition” 中设置的淡入淡出值。

