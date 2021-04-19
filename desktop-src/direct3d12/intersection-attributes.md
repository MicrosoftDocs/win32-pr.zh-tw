---
title: 交集屬性結構
description: 在 HLSL 中宣告的結構，代表固定函式三角形交集的點擊屬性，或程式性基本交集的軸對齊周框方塊。
ms.assetid: ''
ms.localizationpriority: low
ms.topic: language-reference
ms.date: 05/31/2018
ms.openlocfilehash: b2f1dd8fee7371f81dd538b6ea6622f22e3bfd3d
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/12/2021
ms.locfileid: "106986663"
---
# <a name="intersection-attributes-structure"></a>交集屬性結構 

在 HLSL 中宣告的結構，代表固定函式三角形交集的點擊屬性，或程式性基本交集的軸對齊周框方塊。

## <a name="fixed-function-triangle-intersection"></a>Fixed 函數三角形交集

下列結構會在 HLSL 中宣告，以代表固定函式三角形交集的點擊屬性：


```
struct BuiltInTriangleIntersectionAttributes
{
    float2 barycentrics;
};
```

使用固定函式三角形交集叫用的[任何點擊](any-hit-shader.md)和[最接近點擊](closest-hit-shader.md)著色器，都必須使用此結構來取得點擊屬性。 針對三角形的3個頂點指定屬性 a0、a1 和 a2，barycentrics 是 a1 和 barycentrics 的加權。 y 是 a2 的加權。  例如，應用程式可以藉由執行下列動作來進行插補： a = a0 + barycentrics. x * (a1-a0) + barycentrics. y * (a2 – a0) 。

## <a name="axis-aligned-bounding-box-for-procedural-primitive-intersection"></a>程式性基本交集的軸對齊周框方塊

當軸對齊的周框方塊用於與程式性基本專案的交集時，會觸發交集著色器。  該著色器會提供使用者定義的交集屬性結構給 [**ReportHit**](reporthit-function.md) 呼叫。  在相同的點擊群組中，與此交集著色器系結的任何點擊和最接近的點擊著色器都必須使用相同的結構來進行點擊屬性，即使未參考屬性也一樣。  屬性結構的最大值為32個位元組，定義為 **D3D12 \_ RAYTRACING \_ MAX \_ 屬性 \_ 大小（ \_ 以 \_ 位元組為單位**）。


