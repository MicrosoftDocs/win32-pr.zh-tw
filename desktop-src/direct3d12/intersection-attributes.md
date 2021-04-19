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
# <a name="intersection-attributes-structure"></a><span data-ttu-id="bf2f8-103">交集屬性結構</span><span class="sxs-lookup"><span data-stu-id="bf2f8-103">Intersection attributes structure</span></span> 

<span data-ttu-id="bf2f8-104">在 HLSL 中宣告的結構，代表固定函式三角形交集的點擊屬性，或程式性基本交集的軸對齊周框方塊。</span><span class="sxs-lookup"><span data-stu-id="bf2f8-104">A structure declared in HLSL to represent hit attributes for fixed-function triangle intersection or axis-aligned bounding box for procedural primitive intersection.</span></span>

## <a name="fixed-function-triangle-intersection"></a><span data-ttu-id="bf2f8-105">Fixed 函數三角形交集</span><span class="sxs-lookup"><span data-stu-id="bf2f8-105">Fixed-function triangle intersection</span></span>

<span data-ttu-id="bf2f8-106">下列結構會在 HLSL 中宣告，以代表固定函式三角形交集的點擊屬性：</span><span class="sxs-lookup"><span data-stu-id="bf2f8-106">The following structure is declared in HLSL to represent hit attributes for fixed-function triangle intersection:</span></span>


```
struct BuiltInTriangleIntersectionAttributes
{
    float2 barycentrics;
};
```

<span data-ttu-id="bf2f8-107">使用固定函式三角形交集叫用的[任何點擊](any-hit-shader.md)和[最接近點擊](closest-hit-shader.md)著色器，都必須使用此結構來取得點擊屬性。</span><span class="sxs-lookup"><span data-stu-id="bf2f8-107">[Any hit](any-hit-shader.md) and [closest hit](closest-hit-shader.md) shaders invoked using fixed-function triangle intersection must use this structure for hit attributes.</span></span> <span data-ttu-id="bf2f8-108">針對三角形的3個頂點指定屬性 a0、a1 和 a2，barycentrics 是 a1 和 barycentrics 的加權。 y 是 a2 的加權。</span><span class="sxs-lookup"><span data-stu-id="bf2f8-108">Given attributes a0, a1 and a2 for the 3 vertices of a triangle, barycentrics.x is the weight for a1 and barycentrics.y is the weight for a2.</span></span>  <span data-ttu-id="bf2f8-109">例如，應用程式可以藉由執行下列動作來進行插補： a = a0 + barycentrics. x \* (a1-a0) + barycentrics. y \* (a2 – a0) 。</span><span class="sxs-lookup"><span data-stu-id="bf2f8-109">For example, the app can interpolate by doing:  a = a0 + barycentrics.x \* (a1-a0) + barycentrics.y\* (a2 – a0).</span></span>

## <a name="axis-aligned-bounding-box-for-procedural-primitive-intersection"></a><span data-ttu-id="bf2f8-110">程式性基本交集的軸對齊周框方塊</span><span class="sxs-lookup"><span data-stu-id="bf2f8-110">Axis-aligned bounding box for procedural primitive intersection</span></span>

<span data-ttu-id="bf2f8-111">當軸對齊的周框方塊用於與程式性基本專案的交集時，會觸發交集著色器。</span><span class="sxs-lookup"><span data-stu-id="bf2f8-111">When axis-aligned bounding boxes are used for intersection with procedural primitives, an intersection shader is triggered.</span></span>  <span data-ttu-id="bf2f8-112">該著色器會提供使用者定義的交集屬性結構給 [**ReportHit**](reporthit-function.md) 呼叫。</span><span class="sxs-lookup"><span data-stu-id="bf2f8-112">That shader provides a user-defined intersection attribute structure to the [**ReportHit**](reporthit-function.md) call.</span></span>  <span data-ttu-id="bf2f8-113">在相同的點擊群組中，與此交集著色器系結的任何點擊和最接近的點擊著色器都必須使用相同的結構來進行點擊屬性，即使未參考屬性也一樣。</span><span class="sxs-lookup"><span data-stu-id="bf2f8-113">The any hit and closest hit shaders bound in the same hit group with this intersection shader must use the same structure for hit attributes, even if the attributes are not referenced.</span></span>  <span data-ttu-id="bf2f8-114">屬性結構的最大值為32個位元組，定義為 **D3D12 \_ RAYTRACING \_ MAX \_ 屬性 \_ 大小（ \_ 以 \_ 位元組為單位**）。</span><span class="sxs-lookup"><span data-stu-id="bf2f8-114">The maximum attribute structure size is 32 bytes, defined as **D3D12\_RAYTRACING\_MAX\_ATTRIBUTE\_SIZE\_IN\_BYTES**.</span></span>


