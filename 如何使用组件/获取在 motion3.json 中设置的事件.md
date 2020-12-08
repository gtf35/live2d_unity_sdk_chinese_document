# 「Live2D Unity 文档翻译」获取在 motion3.json 中设置的事件

本文翻译自：https://docs.live2d.com/cubism-sdk-tutorials/motion-event

译者注：注意！这并不是一篇严谨的翻译，本人并不是翻译行业从业者，也根本不会日文。官网的中文翻译会连带代码一起翻译，而且还不如机翻日文，官网的英语翻译版本有的语法很奇怪，看起来也是机翻。本文主要来自日文机翻，然后再结合实际开发经验调整到通顺，修改不该翻译的东西并润色。

[最后更新日期: 2017/11/21] 译者注：这是这个日文原文的更新日期



本节介绍如何从自动生成的 AnimationClip 发出的事件中获取 motion3.json 中设置的事件的信息。

译者注：意思就是教你如何获取 motion3.json 里面事件的具体信息，然后因为 motion3.json 在导入 Unity 的时候会被转换成 AnimationClip ，所以要从 AnimationClip  里面获取。

## 摘要

[UserData] 是从 3.1 开始添加的功能，用户可以在运动的任意时刻发布事件。

在 Unity 中，事件是从 AnimationClip 触发的。而 AnimationClip  是从 motion3.json 转换而来的。

根据事件处理方式的不同，可以将其用于各种目的，例如从动作中间播放声音或更改零件的显示状态。

请参阅 [此处](https://docs.live2d.com/cubism-editor-manual/userdata/)，了解如何在 motion3.json 中设置事件。



要获取事件，请执行以下步骤。

1. 创建一个接收事件的组件
2. 向 CubismMotion3Json 添加描述
3. 在场景中放置模型和

## 创建一个接收事件的组件

在 “Project/项目” 窗口中单击 “Create”，然后单击 “C＃脚本” 来创建一个 C＃脚本。

这次名称写 UserDataTest。

![img](https://docs.live2d.com/wp-content/uploads/2017/11/userdatamodel01.png)

![img](https://docs.live2d.com/wp-content/uploads/2017/11/userdatamodel02.png)

在 UserDataTest 中编写如下代码：

```c#
using UnityEngine;

public class UserDataTest : MonoBehaviour
{
	public void UserDataEventListener(string value)
	{
        var currentState = GetComponent<Animator>().GetCurrentAnimatorStateInfo(0);


        Debug.Log("Time : " + (currentState.length / currentState.speed) + "\n" +
            "Value : " + value);
	}
}
```

## 向 CubismMotion3Json 添加描述

打开 CubismMotion3Json 类，并在 ToAnimationClip() 的 AnimationEvent 的部分添加描述，如下所示。

译注：这个文件在`Assets/Live2D/Cubism/Framework/Json/CubismMotion3Json.cs` 中，打开之后搜索`time = UserData[i].Time` 即可找到

```c#
                    var animationEvent = new AnimationEvent
                    {
                        time = UserData[i].Time,
                        functionName = "UserDataEventListener",    // 添加这行
                        stringParameter = UserData[i].Value,
                    };
```

对于 functionName ，设置为上一节中创建的 UserDataTest 类中事件的方法名

。

## 在场景中放置模型和运动

导入或重新导入带有事件集的 motion3.json。

有关导入和重新导入，请参见相关教程。

将模型 Prefab 放置在 “Hierarchy/层级” 窗口中，然后将 UserDataTest 组件附加到 Prefab 根目录。

![img](https://docs.live2d.com/wp-content/uploads/2017/11/01_t2.png)

将从 motion3.json 生成的 AnimationClip 拖放到 「Hierarchy/层级」 面板的 Prefab 中。

![img](https://docs.live2d.com/wp-content/uploads/2017/11/02-3.png)

配置完成！

如果在此状态下运行场景，则会在特定时间从正在播放的动画中发出事件，并且为该事件而设置的字符串将输出到控制台窗口。

![img](https://docs.live2d.com/wp-content/uploads/2017/11/03-2.png)

