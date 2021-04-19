---
description: 本節說明如何將框架和動畫新增至簡單的 cube。
ms.assetid: a909b1f1-b54d-469c-8689-003db41a8f25
title: " (Direct3D 9) 加入框架和動畫"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da88cf431825797943ed33df94742360f7629787
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973765"
---
# <a name="adding-frames-and-animations-direct3d-9"></a> (Direct3D 9) 加入框架和動畫

本節說明如何將框架和動畫新增至簡單的 cube。

## <a name="working-with-frames"></a>使用框架

畫面格應該採用下列結構。


```
Frame Aframe {        // The frame name is chosen for convenience.
FrameTransformMatrix {
...transform data...
}
[ Meshes ] and/or [ More frames]
}
```



將已定義的 cube 網格放在具有身分識別轉換的框架內。 然後將動畫套用至此框架。


```
Frame CubeFrame {
FrameTransformMatrix {
1.000000, 0.000000, 0.000000, 0.000000,
0.000000, 1.000000, 0.000000, 0.000000,
0.000000, 0.000000, 1.000000, 0.000000,
0.000000, 0.000000, 0.000000, 1.000000;;
}
{CubeMesh}        // You could have the mesh inline, but this 
                  // uses an object reference instead.
}
```



## <a name="working-with-animations"></a>使用動畫

動畫是由一組按鍵定義。 索引鍵是與調整作業、方向或位置相關聯的時間值。


```
Animation Animation0 {        // The name is chosen for convenience.
{ Frame that it applies to - normally a reference }
AnimationKey {
...animation key data...
}
{ ...more animation keys... }
}
```



動畫接著會分組為 AnimationSets：


```
AnimationSet AnimationSet0 { // The name is chosen for convenience.
{ an animation - could be inline or a reference }
{ ... more animations ... } 
} 
```



現在請透過動畫取得 cube。


```
AnimationSet AnimationSet0 {
Animation Animation0 {
{CubeFrame}    // Use the frame containing the cube.
AnimationKey {
2;             // Position keys
9;             // 9 keys
10; 3; -100.000000, 0.000000, 0.000000;;,
20; 3; -75.000000, 0.000000, 0.000000;;,
30; 3; -50.000000, 0.000000, 0.000000;;,
40; 3; -25.500000, 0.000000, 0.000000;;,
50; 3; 0.000000, 0.000000, 0.000000;;,
60; 3; 25.500000, 0.000000, 0.000000;;,
70; 3; 50.000000, 0.000000, 0.000000;;,
80; 3; 75.500000, 0.000000, 0.000000;;,
90; 3; 100.000000, 0.000000, 0.000000;;;
}
}
}
```



如需詳細資訊，請參閱 [**動畫**](animation.md) 和 [**AnimationSet**](animationset.md) 範本。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[X 檔案 (舊版) ](x-files--legacy-.md)
</dt> </dl>

 

 



