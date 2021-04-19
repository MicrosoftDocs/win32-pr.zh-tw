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
# <a name="adding-frames-and-animations-direct3d-9"></a><span data-ttu-id="040f4-103"> (Direct3D 9) 加入框架和動畫</span><span class="sxs-lookup"><span data-stu-id="040f4-103">Adding Frames and Animations (Direct3D 9)</span></span>

<span data-ttu-id="040f4-104">本節說明如何將框架和動畫新增至簡單的 cube。</span><span class="sxs-lookup"><span data-stu-id="040f4-104">This section shows how to add frames and animations to a simple cube.</span></span>

## <a name="working-with-frames"></a><span data-ttu-id="040f4-105">使用框架</span><span class="sxs-lookup"><span data-stu-id="040f4-105">Working with Frames</span></span>

<span data-ttu-id="040f4-106">畫面格應該採用下列結構。</span><span class="sxs-lookup"><span data-stu-id="040f4-106">A frame is expected to take the following structure.</span></span>


```
Frame Aframe {        // The frame name is chosen for convenience.
FrameTransformMatrix {
...transform data...
}
[ Meshes ] and/or [ More frames]
}
```



<span data-ttu-id="040f4-107">將已定義的 cube 網格放在具有身分識別轉換的框架內。</span><span class="sxs-lookup"><span data-stu-id="040f4-107">Place the defined cube mesh inside a frame with an identity transform.</span></span> <span data-ttu-id="040f4-108">然後將動畫套用至此框架。</span><span class="sxs-lookup"><span data-stu-id="040f4-108">Then apply an animation to this frame.</span></span>


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



## <a name="working-with-animations"></a><span data-ttu-id="040f4-109">使用動畫</span><span class="sxs-lookup"><span data-stu-id="040f4-109">Working with Animations</span></span>

<span data-ttu-id="040f4-110">動畫是由一組按鍵定義。</span><span class="sxs-lookup"><span data-stu-id="040f4-110">An animation is defined by a set of keys.</span></span> <span data-ttu-id="040f4-111">索引鍵是與調整作業、方向或位置相關聯的時間值。</span><span class="sxs-lookup"><span data-stu-id="040f4-111">A key is a time value associated with a scaling operation, an orientation, or a position.</span></span>


```
Animation Animation0 {        // The name is chosen for convenience.
{ Frame that it applies to - normally a reference }
AnimationKey {
...animation key data...
}
{ ...more animation keys... }
}
```



<span data-ttu-id="040f4-112">動畫接著會分組為 AnimationSets：</span><span class="sxs-lookup"><span data-stu-id="040f4-112">Animations are then grouped into AnimationSets:</span></span>


```
AnimationSet AnimationSet0 { // The name is chosen for convenience.
{ an animation - could be inline or a reference }
{ ... more animations ... } 
} 
```



<span data-ttu-id="040f4-113">現在請透過動畫取得 cube。</span><span class="sxs-lookup"><span data-stu-id="040f4-113">Now take the cube through an animation.</span></span>


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



<span data-ttu-id="040f4-114">如需詳細資訊，請參閱 [**動畫**](animation.md) 和 [**AnimationSet**](animationset.md) 範本。</span><span class="sxs-lookup"><span data-stu-id="040f4-114">For more information, see the [**Animation**](animation.md) and [**AnimationSet**](animationset.md) templates.</span></span>

## <a name="related-topics"></a><span data-ttu-id="040f4-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="040f4-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="040f4-116">X 檔案 (舊版) </span><span class="sxs-lookup"><span data-stu-id="040f4-116">X Files (Legacy)</span></span>](x-files--legacy-.md)
</dt> </dl>

 

 



