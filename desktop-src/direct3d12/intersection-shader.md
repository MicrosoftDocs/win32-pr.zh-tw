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
ms.openlocfilehash: d7f9f81fdedae0fc6f6aa0448e6771c331af9c0d8924ab0f091d281565e4cfa3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119850878"
---
# <a name="intersection-shader"></a>交集著色器

著色器，用來針對與關聯的周框方塊 (周框方塊) 相交的光線，執行自訂交集基本專案。 

交集著色器沒有光線承載的存取權，但會透過呼叫 [**ReportHit**](reporthit-function.md)來定義每個點擊的交集屬性。  如果「光線旗標」**光線 \_ 旗標 \_ \_ 先接受 \_ HIT_ \AND \_ \END \_ 搜尋** 已設定，或從任何點擊著色器呼叫 [**AcceptHitAndEndSearch**](accepthitandendsearch-function.md) ，則處理 **ReportHit** 可能會提早停止交集著色器。  否則，如果已接受命中，則會傳回 true，如果被拒，則傳回 false。  這表示，任何點擊著色器（如果有的話）都必須在控制項有條件地傳回交集著色器之前執行。

## <a name="shader-type-attribute"></a>著色器類型屬性


```
[shader("intersection")]
```



## <a name="example"></a>範例

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

 

 




