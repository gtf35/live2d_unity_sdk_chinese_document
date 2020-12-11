# 「Live2D Unity 文档翻译」如何自定义Importer/Deleter

本文翻译自：https://docs.live2d.com/cubism-sdk-tutorials/customize-importer/

译者注：注意！这并不是一篇严谨的翻译，本人并不是翻译行业从业者，也根本不会日文。官网的中文翻译会连带代码一起翻译，而且还不如机翻日文，官网的英语翻译版本有的语法很奇怪，看起来也是机翻。本文主要来自日文机翻，然后再结合实际开发经验调整到通顺，修改不该翻译的东西并润色。

[最后更新日期: 2020/01/30] 译者注：这是这个日文原文的更新日期



这篇文章提供了自定义 Importer/Deleter 的步骤。

[ [导入 SDK-放置模型 ](https://docs.live2d.com/cubism-sdk-tutorials/getting-started/)] 假设模型已经放置到项目中。



## 摘要

Importer/Deleter 是在导入或删除具有指定扩展名的文件时回调的功能。

若要创建和自定义自己的 Importer/Deleter，请按照下列步骤操作：

1. 创建继承自 `CubismImporterBase/CubismDeleterBase` 的 `Importer/Deleter` 脚本
2. 注册要由 `Importer/Deleter`  处理的文件的拓展名
3. 创建 `Import()/Delete()`，在导入或删除时将对其进行回调

## 创建继承自 `CubismImporterBase/CubismDeleterBase` 的 `Importer/Deleter` 脚本

创建一个 `ImporterCustomization` 脚本。

```c#
using Live2D.Cubism.Editor.Importers;

public sealed class ImporterCustomization : CubismImporterBase
{
    /*省略*/
}
```

创建一个`DeleterCustomization`脚本。

```c#
using Live2D.Cubism.Editor.Deleters;

public sealed class DeleterCustomization : CubismDeleterBase
{
    /*省略*/
}
```

※该脚本是 `Unity` 编辑器的扩展，因此您需要在 `Editor` 文件夹下创建它。

## 注册要由 `Importer/Deleter`  处理的文件的拓展名

注册要由 `Importer` 处理的文件的扩展名。

```c#
public sealed class ImporterCustomization : CubismImporterBase
{
    [UnityEditor.InitializeOnLoadMethod]
    private static void RegisterImporter()
    {
        CubismImporter.RegisterImporter<ImporterCustomization>(".asset");
    }
}
```

注册要由 `Deleter` 处理的文件的扩展名。

```c#
public sealed class ImporterCustomization : CubismImporterBase
{
    [UnityEditor.InitializeOnLoadMethod]
    private static void RegisterDeleter()
    {
        CubismDeleter.RegisterDeleter<DeleterCustomization>(".asset");
    }
}
```

## 创建 `Import()/Delete()`，在导入或删除时将对其进行回调

重写 `Import()`，在导入要处理的目标文件时将对其进行回调。

```c#
public sealed class ImporterCustomization : CubismImporterBase
{
    public override void Import()
    {
        UnityEngine.Debug.Log("Asset Import as path : " + AssetPath);
    }
}
```

重写 `Delete()`，在删除要处理的目标文件时将对其进行回调。

```c#
public sealed class ImporterCustomization : CubismImporterBase
{
    public override void Delete()
    {
        UnityEngine.Debug.Log("Asset deleted as path : " + AssetPath);
    }
}
```

