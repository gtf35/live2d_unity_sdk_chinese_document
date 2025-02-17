# Live2D Cubism SDK 3 for Unity 文档中文翻译
⚡🚧⚡ 施工中，尚未翻译完毕

👉[点击此处查看目录在线阅读](https://blog.gtf35.top/tag/Live2D-Unity-%E6%96%87%E6%A1%A3%E7%BF%BB%E8%AF%91/)

## 为什么要创建这个仓库

纵览 Live2D SDK 的中文资料，数量真的是少之又少，其中是新版的(3.0以上)更是凤毛麟角，而其中系统完整的又是少之又少。

但是学习这个 SDK 的使用，最好的肯定是官方文档，虽然官网有中文，但是质量其实并不高，先不说相当一部分的话莫名其妙，甚至连代码都翻译了。

但这并不是问题，作为一名程序员，看英文文档已经是常规操作，但是我想说的是这个英文文档的语法也很神奇，不太能看。

举个栗子：

- 官方文档中文：通过使用转换后的AnimationClip， Unity不要使用上面的Live2D功能， Unity只有内置功能才能处理动画。

- 官方文档英文：By using the converted AnimationClip, Unity Do not use the function of Live2D above, Unity It is possible to handle animation with only built-in function.

- 官方文档日文：変換されたAnimationClipを用いることで、Unity上ではLive2Dの機能は使わず、Unityのビルトイン機能のみでアニメーションを扱うことが可能となっています。

- 基于日文机翻：通过使用转换后的 AnimationClip，可以仅使用 Unity 的内置函数处理动画，而无需在 Unity 上使用 Live2D 函数。

到这已经很明显了，中文和英文的含义直接变了（相信日文的原因是这是日本公司，日文是他们的母语，而且后续的文档里也有介绍在 Unity 上使用 Live2D 函数），所以有一个贴合实际的翻译很重要，于是我创建了这个仓库，既节约后人的时间，也方便我日后查看。不过有一点需要注意：

这并不是严谨的翻译，本人并不是翻译行业从业者，也根本不会日文。本文主要来自日文机翻，然后再结合实际开发经验调整到通顺，修改不该翻译的东西并润色。主要就是为了方便中国的开发者学习 「Live2d Cubism SDK for Unity」，只会竭力保证文章内容通顺且贴合实际开发情况。

## 翻译情况-SDK教程

完成部分：

- 入门
  - 导入SDK    [博客](https://blog.gtf35.top/cubism-sdk-tutorials-getting-started-sdk-import/) [Github](https://github.com/gtf35/live2d_unity_sdk_chinese_document/blob/main/%E5%85%A5%E9%97%A8/%E5%AF%BC%E5%85%A5SDK.md) [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/getting-started/)
  - 播放动画    [博客](https://blog.gtf35.top/cubism-sdk-tutorials-getting-started-animation/) [Github ](https://github.com/gtf35/live2d_unity_sdk_chinese_document/blob/main/%E5%85%A5%E9%97%A8/%E6%92%AD%E6%94%BE%E5%8A%A8%E7%94%BB.md) [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/animation/)
  - 更新导入的模型    [博客](https://blog.gtf35.top/cubism-sdk-tutorials-getting-started-reimportmodel/) [Github](https://github.com/gtf35/live2d_unity_sdk_chinese_document/blob/main/%E5%85%A5%E9%97%A8/%E6%9B%B4%E6%96%B0%E5%AF%BC%E5%85%A5%E7%9A%84%E6%A8%A1%E5%9E%8B.md) [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/reimportmodel/)
  - 在运行时加载模型    [博客](https://blog.gtf35.top/cubism-sdk-tutorials-getting-started-initializemodel/) [Github](https://github.com/gtf35/live2d_unity_sdk_chinese_document/blob/main/%E5%85%A5%E9%97%A8/%E5%9C%A8%E8%BF%90%E8%A1%8C%E6%97%B6%E5%8A%A0%E8%BD%BD%E6%A8%A1%E5%9E%8B.md) [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/initializemodel/)
  - 关于更新模型参数   [博客](https://blog.gtf35.top/cubism-sdk-tutorials-getting-started-about-parameterupdating-of-model/) [Github](https://github.com/gtf35/live2d_unity_sdk_chinese_document/blob/main/%E5%85%A5%E9%97%A8/%E5%85%B3%E4%BA%8E%E6%9B%B4%E6%96%B0%E6%A8%A1%E5%9E%8B%E5%8F%82%E6%95%B0.md) [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/about-parameterupdating-of-model/)
  - 更新 Cubism Components  [博客](https://blog.gtf35.top/cubism-sdk-tutorials-getting-started-update-components/) [Github](https://github.com/gtf35/live2d_unity_sdk_chinese_document/blob/main/%E5%85%A5%E9%97%A8/%E6%9B%B4%E6%96%B0%20Cubism%20Components.md) [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/update-components/)
- 如何使用组件
  - 设置命中判断    [博客](https://blog.gtf35.top/cubism-sdk-tutorials-how-to-use-hittest/) [Github](https://github.com/gtf35/live2d_unity_sdk_chinese_document/blob/main/%E5%A6%82%E4%BD%95%E4%BD%BF%E7%94%A8%E7%BB%84%E4%BB%B6/%E5%91%BD%E4%B8%AD%E5%88%A4%E6%96%AD.md) [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/hittest/)
  - 实现视线跟踪    [博客](https://blog.gtf35.top/cubism-sdk-tutorials-lookat/) [Github](https://github.com/gtf35/live2d_unity_sdk_chinese_document/blob/main/%E5%A6%82%E4%BD%95%E4%BD%BF%E7%94%A8%E7%BB%84%E4%BB%B6/%E5%AE%9E%E7%8E%B0%E8%A7%86%E7%BA%BF%E8%BF%BD%E8%B8%AA.md) [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/lookat/)
  - 实现自动眨眼    [博客](https://blog.gtf35.top/cubism-sdk-tutorials-eyeblink/) [Github](https://github.com/gtf35/live2d_unity_sdk_chinese_document/blob/main/%E5%A6%82%E4%BD%95%E4%BD%BF%E7%94%A8%E7%BB%84%E4%BB%B6/%E5%AE%9E%E7%8E%B0%E8%87%AA%E5%8A%A8%E7%9C%A8%E7%9C%BC.md) [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/eyeblink/)
  - 嘴唇同步设置   [博客](https://blog.gtf35.top/cubism-sdk-tutorials-lipsync/) [Github](https://github.com/gtf35/live2d_unity_sdk_chinese_document/blob/main/%E5%A6%82%E4%BD%95%E4%BD%BF%E7%94%A8%E7%BB%84%E4%BB%B6/%E5%AE%9E%E7%8E%B0%E5%8F%A3%E5%9E%8B%E5%90%8C%E6%AD%A5.md) [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/lipsync/)
  - 如何实现参数值周期变化    [博客](https://blog.gtf35.top/cubism-sdk-tutorials-harmonicmotion/) [Github](https://github.com/gtf35/live2d_unity_sdk_chinese_document/blob/main/%E5%A6%82%E4%BD%95%E4%BD%BF%E7%94%A8%E7%BB%84%E4%BB%B6/%E5%A6%82%E4%BD%95%E5%AE%9E%E7%8E%B0%E5%8F%82%E6%95%B0%E5%80%BC%E5%91%A8%E6%9C%9F%E5%8F%98%E5%8C%96.md) [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/harmonicmotion/)
  - 如何在模型的 Drawable 之间插入精灵    [博客](https://blog.gtf35.top/cubism-sdk-tutorials-betweendrawables/) [Github](https://github.com/gtf35/live2d_unity_sdk_chinese_document/blob/main/%E5%A6%82%E4%BD%95%E4%BD%BF%E7%94%A8%E7%BB%84%E4%BB%B6/%E5%A6%82%E4%BD%95%E5%9C%A8%E6%A8%A1%E5%9E%8B%E7%9A%84%20Drawable%20%E4%B9%8B%E9%97%B4%E6%8F%92%E5%85%A5%E7%B2%BE%E7%81%B5.md) [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/betweendrawables/)
  - 获取艺术网格中的用户数据    [博客](https://blog.gtf35.top/cubism-sdk-tutorials-userdata-drawable/) [Github](https://github.com/gtf35/live2d_unity_sdk_chinese_document/blob/main/%E5%A6%82%E4%BD%95%E4%BD%BF%E7%94%A8%E7%BB%84%E4%BB%B6/%E8%8E%B7%E5%8F%96%E8%89%BA%E6%9C%AF%E7%BD%91%E6%A0%BC%E4%B8%AD%E7%9A%84%E7%94%A8%E6%88%B7%E6%95%B0%E6%8D%AE.md) [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/userdata-drawable/)
  - 获取在 motion3.json 中设置的事件    [博客](https://blog.gtf35.top/cubism-sdk-tutorials-motion-event/) [Github](https://github.com/gtf35/live2d_unity_sdk_chinese_document/blob/main/%E5%A6%82%E4%BD%95%E4%BD%BF%E7%94%A8%E7%BB%84%E4%BB%B6/%E8%8E%B7%E5%8F%96%E5%9C%A8%20motion3.json%20%E4%B8%AD%E8%AE%BE%E7%BD%AE%E7%9A%84%E4%BA%8B%E4%BB%B6.md) [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/motion-event/)
  - 通过脚本播放动作    [博客](https://blog.gtf35.top/cubism-sdk-tutorials-motion-unity-ow/) [Github](https://github.com/gtf35/live2d_unity_sdk_chinese_document/blob/main/%E5%A6%82%E4%BD%95%E4%BD%BF%E7%94%A8%E7%BB%84%E4%BB%B6/%E4%BB%8E%E8%84%9A%E6%9C%AC%E6%92%AD%E6%94%BE%E5%8A%A8%E4%BD%9C.md) [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/motion-unity-ow/)
  - 如何自定义 Importer/Deleter    [博客](https://blog.gtf35.top/cubism-sdk-tutorials-customize-importer/) [Github](https://github.com/gtf35/live2d_unity_sdk_chinese_document/blob/main/%E5%A6%82%E4%BD%95%E4%BD%BF%E7%94%A8%E7%BB%84%E4%BB%B6/%E5%A6%82%E4%BD%95%E8%87%AA%E5%AE%9A%E4%B9%89ImporterDeleter.md) [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/customize-importer/)
  - 如何设置 UpdateController    [博客](https://blog.gtf35.top/cubism-sdk-tutorials-updatecontroller/) [Github](https://github.com/gtf35/live2d_unity_sdk_chinese_document/blob/main/%E5%A6%82%E4%BD%95%E4%BD%BF%E7%94%A8%E7%BB%84%E4%BB%B6/%E5%A6%82%E4%BD%95%E8%AE%BE%E7%BD%AE%20UpdateController.md) [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/updatecontroller/)
  - 在 Mecanim 中启用动作淡入淡出   [博客](https://blog.gtf35.top/cubism-sdk-tutorials-motionfade/) [Github](https://github.com/gtf35/live2d_unity_sdk_chinese_document/blob/main/%E5%A6%82%E4%BD%95%E4%BD%BF%E7%94%A8%E7%BB%84%E4%BB%B6/%E5%9C%A8%20Mecanim%20%E4%B8%AD%E5%90%AF%E7%94%A8%E5%8A%A8%E4%BD%9C%E6%B7%A1%E5%85%A5%E6%B7%A1%E5%87%BA.md) [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/motionfade/)
  - 使用表情功能    [博客](https://blog.gtf35.top/cubism-sdk-tutorials-expression/) [Github](https://github.com/gtf35/live2d_unity_sdk_chinese_document/blob/main/%E5%A6%82%E4%BD%95%E4%BD%BF%E7%94%A8%E7%BB%84%E4%BB%B6/%E4%BD%BF%E7%94%A8%E8%A1%A8%E6%83%85%E5%8A%9F%E8%83%BD.md) [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/expression/)
  - 使用 Pose 功能    [博客](https://blog.gtf35.top/cubism-sdk-tutorials-pose-unity/) [Github](https://github.com/gtf35/live2d_unity_sdk_chinese_document/blob/main/%E5%A6%82%E4%BD%95%E4%BD%BF%E7%94%A8%E7%BB%84%E4%BB%B6/%E4%BD%BF%E7%94%A8%20Pose%20%E5%8A%9F%E8%83%BD.md) [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/pose-unity/)
  - 保存/恢复要操作的值    [博客](https://blog.gtf35.top/cubism-sdk-tutorials-parameterstore/) [Github](https://github.com/gtf35/live2d_unity_sdk_chinese_document/blob/main/%E5%A6%82%E4%BD%95%E4%BD%BF%E7%94%A8%E7%BB%84%E4%BB%B6/%E4%BF%9D%E5%AD%98%E5%92%8C%E6%81%A2%E5%A4%8D%E5%8F%82%E6%95%B0%E5%80%BC.md) [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/parameterstore/)
  - 控制您自己的组件的执行顺序    [博客](https://blog.gtf35.top/cubism-sdk-tutorials-using-update-controller/) [Github](https://github.com/gtf35/live2d_unity_sdk_chinese_document/blob/main/%E5%A6%82%E4%BD%95%E4%BD%BF%E7%94%A8%E7%BB%84%E4%BB%B6/%E6%8E%A7%E5%88%B6%E6%82%A8%E8%87%AA%E5%B7%B1%E7%9A%84%E7%BB%84%E4%BB%B6%E7%9A%84%E6%89%A7%E8%A1%8C%E9%A1%BA%E5%BA%8F.md) [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/using-update-controller/)
  - 定制材料   [博客](https://blog.gtf35.top/cubism-sdk-tutorials-material-customization/) [Github](https://github.com/gtf35/live2d_unity_sdk_chinese_document/blob/main/%E5%A6%82%E4%BD%95%E4%BD%BF%E7%94%A8%E7%BB%84%E4%BB%B6/%E5%AE%9A%E5%88%B6%E6%9D%90%E6%96%99.md) [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/unity-material-customization/)
  - 制作 Cubism DIY Viewer    [博客](https://blog.gtf35.top/cubism-sdk-tutorials-use-cubismdiyviewer/) [Github](https://github.com/gtf35/live2d_unity_sdk_chinese_document/blob/main/%E5%A6%82%E4%BD%95%E4%BD%BF%E7%94%A8%E7%BB%84%E4%BB%B6/%E5%88%B6%E4%BD%9C%20Cubism%20DIY%20Viewer.md) [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/use-cubismdiyviewer/)

未完成：

- 故障排除
  - 使用 AssetBundle 中的模型时出现内存泄漏问题和解决方法    [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/issue-of-assetbundle/)
  - 使模型的绘制顺序正常    [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/sortrendering/)
  - 切换面部表情/姿势
    - 切换姿势时的注意事项    [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/attention-changepose/)
  - 组织多个模型的重叠    [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/orderinlayer/)
  - 运动循环播放期间淡入淡出
    - 启用淡入淡出以循环运动（动画状态机）    [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/loop-playback-with-fade-animator/)
    - 启用淡入淡出以循环运动（CubismMotionController）    [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/loop-playback-with-fade-cubism/)

## 翻译情况-SDK手册

等待教程翻译完成之后开始