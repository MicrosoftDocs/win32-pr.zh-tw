---
description: 當它已啟用，且已判定最接近的點擊，或光線交集搜尋結束時，即會叫用著色器。
ms.assetid: ''
title: 最接近的點擊著色器
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RAY_FLAG
api_type:
- NA
ms.openlocfilehash: 347ad66dce0a81b929d5dc3c82051bf84226e723
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972573"
---
# <a name="closest-hit-shader"></a><span data-ttu-id="853c4-103">最接近的點擊著色器</span><span class="sxs-lookup"><span data-stu-id="853c4-103">Closest Hit Shader</span></span>

<span data-ttu-id="853c4-104">當它已啟用，且已判定最接近的點擊，或光線交集搜尋結束時，即會叫用著色器。</span><span class="sxs-lookup"><span data-stu-id="853c4-104">A shader that is invoked when it is enabled and the closest hit has been determined or ray intersection search ended.</span></span> <span data-ttu-id="853c4-105">此著色器是通常會發生表面陰影和產生額外光線的位置。</span><span class="sxs-lookup"><span data-stu-id="853c4-105">This shader is where surface shading and additional ray generation will typically occur.</span></span>  <span data-ttu-id="853c4-106">最接近的點擊著色器必須宣告承載參數，後面接著屬性參數。</span><span class="sxs-lookup"><span data-stu-id="853c4-106">Closest hit shaders must declare a payload parameter, followed by an attributes parameter.</span></span>  <span data-ttu-id="853c4-107">每個都必須是使用者定義的結構類型，分別用於 [**TraceRay**](traceray-function.md) 和 [**ReportHit**](reporthit-function.md) ，或使用固定函數三角形交集時的 [**交集屬性結構**](intersection-attributes.md) 。</span><span class="sxs-lookup"><span data-stu-id="853c4-107">Each must be a user-defined structure type matching types used for [**TraceRay**](traceray-function.md) and [**ReportHit**](reporthit-function.md) respectively, or the [**Intersection Attributes Structure**](intersection-attributes.md) when fixed-function triangle intersection is used.</span></span>

## <a name="shader-type-attribute"></a><span data-ttu-id="853c4-108">著色器類型屬性</span><span class="sxs-lookup"><span data-stu-id="853c4-108">Shader Type attribute</span></span>


```
[shader("closesthit")]
```



## <a name="example"></a><span data-ttu-id="853c4-109">範例</span><span class="sxs-lookup"><span data-stu-id="853c4-109">Example</span></span>

```
[shader("closesthit")]
void closesthit_main(inout MyPayload payload, in MyAttributes attr)
{
    CallShader( ... );  // maybe
    // update payload for surface
    // trace reflection
    float3 worldRayOrigin = WorldRayOrigin() + WorldRayDirection() * RayTCurrent();
    float3 worldNormal = mul(attr.normal, (float3x3)ObjectToWorld3x4());
    RayDesc reflectedRay = { worldRayOrigin, SceneConstants.Epsilon,
                             ReflectRay(WorldRayDirection(), worldNormal),
                             SceneConstants.TMax };
    TraceRay(MyAccelerationStructure,
             SceneConstants.RayFlags,
             SceneConstants.InstanceInclusionMask,
             SceneConstants.RayContributionToHitGroupIndex,
             SceneConstants.MultiplierForGeometryContributionToHitGroupIndex,
             SceneConstants.MissShaderIndex,
             reflectedRay,
             payload);
    // Combine final contributions into ray payload
    // this ray query is now complete.
    // Alternately, could look at data in payload result based on that make other TraceRay
    // calls.  No constraints on the code structure.
}

```

 

 




