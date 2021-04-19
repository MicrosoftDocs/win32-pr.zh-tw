---
description: 當光線交集不透明時，所叫用的著色器。
ms.assetid: ''
title: 任何命中著色器
ms.date: 05/31/2018
ms.topic: reference
ms.localizationpriority: low
topic_type:
- APIRef
- kbSyntax
api_name:
- RAY_FLAG
api_type:
- NA
ms.openlocfilehash: aad2f8b94f6ea53d500d285cac3555f5ff8b95f4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970102"
---
# <a name="any-hit-shader"></a>任何命中著色器

當光線交集不透明時，所叫用的著色器。 

任何點擊著色器都必須宣告承載參數，後面接著屬性參數。 這些參數都必須是使用者定義的結構類型，分別用於 [**TraceRay**](traceray-function.md) 和 [**ReportHit**](reporthit-function.md) ，或使用固定函式三角形交集時的 [**交集屬性結構**](intersection-attributes.md) 。

任何點擊著色器都可以執行下列種類的作業：

*   讀取和修改光線承載： (inout payload_t rayPayload) 
*   讀取交集屬性： (attr_t 屬性) 
*   呼叫 [**AcceptHitAndEndSearch**](accepthitandendsearch-function.md)，它會接受目前的點擊，結束 [任何命中的著色](any-hit-shader.md)器，結束 [交集著色器](intersection-shader.md) （如果有的話），並在最接近的點擊著色器在作用中時執行最接近的點擊 [著色器](closest-hit-shader.md) 。
*   呼叫 [**IgnoreHit**](ignorehit-function.md)，這會結束任何命中的著色器，並告知系統繼續搜尋命中，包括將控制權傳回給交集著色器（如果目前正在執行），並從 [**ReportHit**](reporthit-function.md)* 呼叫位置傳回 false。 
*   傳回但不呼叫其中一個內建函式（可接受目前的點擊），並告知系統繼續搜尋命中，包括將控制權傳回給交集著色器（如果有的話），並在 [**ReportHit**](reporthit-function.md) 呼叫位置傳回 true，表示已接受點擊。

即使 [**IgnoreHit**](ignorehit-function.md) 或 [**AcceptHitAndEndSearch**](accepthitandendsearch-function.md)結束了任何叫用著色器調用，也必須保留對光線承載所做的任何修改。

## <a name="shader-type-attribute"></a>著色器類型屬性

```
[shader("anyhit")]
```

## <a name="example"></a>範例

```
[shader("anyhit")]
void anyhit_main( inout MyPayload payload, in MyAttributes attr )
{
    float3 hitLocation = ObjectRayOrigin() + ObjectRayDirection() * RayTCurrent();
    float alpha = computeAlpha(hitLocation, attr, ...);

    // Processing shadow and only care if a hit is registered?
    if (TerminateShadowRay(alpha))
        AcceptHitAndEndSearch(); // aborts function

    // Save alpha contribution and ignoring hit?
    if (SaveAndIgnore(payload, RayTCurrent(), alpha, attr, ...))
        IgnoreHit(); // aborts function

    // do something else
    // return to accept and update closest hit
}
```
