---
description: 著色器，用來針對與關聯的周框方塊 (周框方塊) 相交的光線，執行自訂交集基本專案。
ms.assetid: ''
title: 交集著色器
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
ms.openlocfilehash: f20d9ceb90b716ca5e5c04fb796a8b20f535825d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970546"
---
# <a name="intersection-shader"></a><span data-ttu-id="61d90-103">交集著色器</span><span class="sxs-lookup"><span data-stu-id="61d90-103">Intersection Shader</span></span>

<span data-ttu-id="61d90-104">著色器，用來針對與關聯的周框方塊 (周框方塊) 相交的光線，執行自訂交集基本專案。</span><span class="sxs-lookup"><span data-stu-id="61d90-104">A shader that is used to implement custom intersection primitives for rays intersecting an associated bounding volume (bounding box).</span></span> 

<span data-ttu-id="61d90-105">交集著色器沒有光線承載的存取權，但會透過呼叫 [**ReportHit**](reporthit-function.md)來定義每個點擊的交集屬性。</span><span class="sxs-lookup"><span data-stu-id="61d90-105">The intersection shader does not have access to the ray payload, but defines the intersection attributes for each hit through a call to [**ReportHit**](reporthit-function.md).</span></span>  <span data-ttu-id="61d90-106">如果「光線旗標」**光線 \_ 旗標 \_ \_ 先接受 \_ HIT_ \AND \_ \END \_ 搜尋** 已設定，或從任何點擊著色器呼叫 [**AcceptHitAndEndSearch**](accepthitandendsearch-function.md) ，則處理 **ReportHit** 可能會提早停止交集著色器。</span><span class="sxs-lookup"><span data-stu-id="61d90-106">The handling of **ReportHit** may stop the intersection shader early, if the ray flag **RAY\_FLAG\_ACCEPT\_FIRST\_HIT_\AND\_\END\_SEARCH** is set, or [**AcceptHitAndEndSearch**](accepthitandendsearch-function.md) is called from an any hit shader.</span></span>  <span data-ttu-id="61d90-107">否則，如果已接受命中，則會傳回 true，如果被拒，則傳回 false。</span><span class="sxs-lookup"><span data-stu-id="61d90-107">Otherwise, it returns true if the hit was accepted or false if the hit was rejected.</span></span>  <span data-ttu-id="61d90-108">這表示，任何點擊著色器（如果有的話）都必須在控制項有條件地傳回交集著色器之前執行。</span><span class="sxs-lookup"><span data-stu-id="61d90-108">This means that an any hit shader, if present, must execute before control conditionally returns to the intersection shader.</span></span>

## <a name="shader-type-attribute"></a><span data-ttu-id="61d90-109">著色器類型屬性</span><span class="sxs-lookup"><span data-stu-id="61d90-109">Shader Type attribute</span></span>


```
[shader("intersection")]
```



## <a name="example"></a><span data-ttu-id="61d90-110">範例</span><span class="sxs-lookup"><span data-stu-id="61d90-110">Example</span></span>

```
struct CustomPrimitiveDef { ... };
struct MyAttributes { ... };
struct CustomIntersectionIterator {...};
void InitCustomIntersectionIterator(CustomIntersectionIterator it) {...}
bool IntersectCustomPrimitiveFrontToBack(
    CustomPrimitiveDef prim,
    inout CustomIntersectionIterator it,
    float3 origin, float3 dir,
    float rayTMin, inout float curT,
    out MyAttributes attr);

[shader("intersection")]
void intersection_main()
{
    float THit = RayTCurrent();
    MyAttributes attr;
    CustomIntersectionIterator it;
    InitCustomIntersectionIterator(it); 
    while(IntersectCustomPrimitiveFrontToBack(
            CustomPrimitiveDefinitions[LocalConstants.PrimitiveIndex],
            it, ObjectRayOrigin(), ObjectRayDirection(), 
            RayTMin(), THit, attr))
    {
        // Exit on the first hit.  Note that if the ray has
        // RAY_FLAG_ACCEPT_FIRST_HIT_AND_END_SEARCH or an
        // anyhit shader is used and calls AcceptHitAndEndSearch(),
        // that would also fully exit this intersection shader (making
        // the “break” below moot in that case).        
        if (ReportHit(THit, /*hitKind*/ 0, attr) && (RayFlags() &  RAY_FLAG_FORCE_OPAQUE))
            break;
    }
}
```

 

 




