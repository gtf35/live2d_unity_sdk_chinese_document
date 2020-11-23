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

## 翻译情况

完成部分：

- 入门
  - 导入SDK    [博客](https://blog.gtf35.top/cubism-sdk-tutorials-getting-started-sdk-import/) [Github](https://github.com/gtf35/live2d_unity_sdk_chinese_document/blob/main/%E5%85%A5%E9%97%A8/%E5%AF%BC%E5%85%A5SDK.md) [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/getting-started/)
  - 播放动画    [博客](https://blog.gtf35.top/cubism-sdk-tutorials-getting-started-animation/) [Github ](https://github.com/gtf35/live2d_unity_sdk_chinese_document/blob/main/%E5%85%A5%E9%97%A8/%E6%92%AD%E6%94%BE%E5%8A%A8%E7%94%BB.md) [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/animation/)
  - 更新导入的模型    [博客](https://blog.gtf35.top/cubism-sdk-tutorials-getting-started-reimportmodel/) [Github](https://github.com/gtf35/live2d_unity_sdk_chinese_document/blob/main/%E5%85%A5%E9%97%A8/%E6%9B%B4%E6%96%B0%E5%AF%BC%E5%85%A5%E7%9A%84%E6%A8%A1%E5%9E%8B.md) [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/reimportmodel/)
  - 在运行时加载模型    [博客](https://blog.gtf35.top/cubism-sdk-tutorials-getting-started-initializemodel/) [Github](https://github.com/gtf35/live2d_unity_sdk_chinese_document/blob/main/%E5%85%A5%E9%97%A8/%E5%9C%A8%E8%BF%90%E8%A1%8C%E6%97%B6%E5%8A%A0%E8%BD%BD%E6%A8%A1%E5%9E%8B.md) [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/initializemodel/)
  - 关于更新模型参数   [博客](https://blog.gtf35.top/cubism-sdk-tutorials-getting-started-about-parameterupdating-of-model/) [Github](https://github.com/gtf35/live2d_unity_sdk_chinese_document/blob/main/%E5%85%A5%E9%97%A8/%E5%85%B3%E4%BA%8E%E6%9B%B4%E6%96%B0%E6%A8%A1%E5%9E%8B%E5%8F%82%E6%95%B0.md) [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/about-parameterupdating-of-model/)

未完成：

- 入门
  - 更新 Cubism Components    [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/update-components/)
- 如何使用组件
  - 命中判断设置    [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/hittest/)
  - 视线跟踪设置    [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/lookat/)
  - 自动眨眼设置    [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/eyeblink/)
  - 嘴唇同步设置    [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/lipsync/)
  - 如何使参数定期工作    [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/harmonicmotion/)
  - 在模型的 Drawables 之间放置另一个精灵    [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/betweendrawables/)
  - 获取艺术网格中的用户数据集    [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/userdata-drawable/)
  - 获取在 motion3.json 中设置的事件    [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/motion-event/)
  - 通过脚本播放动作    [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/motion-unity-ow/)
  - 如何自定义 Importer/Deleter    [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/customize-importer/)
  - Original Workflow
    - 如何设置 UpdateController    [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/updatecontroller/)
    - 在 Mecanim 中启用运动淡入    [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/motionfade/)
    - 使用面部特征    [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/expression/)
    - 使用 Pose 功能    [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/pose-unity/)
    - 保存/恢复要操作的值    [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/parameterstore/)
    - 控制您自己的组件的执行顺序    [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/using-update-controller/)
- 定制
  - 定制材料    [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/unity-material-customization/)
  - 制作 Cubism DIY Viewer    [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/use-cubismdiyviewer/)
- 故障排除
  - 使用 AssetBundle 中的模型时出现内存泄漏问题和解决方法    [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/issue-of-assetbundle/)
  - 使模型的绘制顺序正常    [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/sortrendering/)
  - 切换面部表情/姿势
    - 切换姿势时的注意事项    [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/attention-changepose/)
  - 组织多个模型的重叠    [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/orderinlayer/)
  - 运动循环播放期间淡入淡出
    - 启用淡入淡出以循环运动（动画状态机）    [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/loop-playback-with-fade-animator/)
    - 启用淡入淡出以循环运动（CubismMotionController）    [官方文档](https://docs.live2d.com/cubism-sdk-tutorials/loop-playback-with-fade-cubism/)
