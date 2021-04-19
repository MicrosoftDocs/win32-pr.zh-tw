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
# <a name="any-hit-shader"></a><span data-ttu-id="9855f-103">任何命中著色器</span><span class="sxs-lookup"><span data-stu-id="9855f-103">Any Hit Shader</span></span>

<span data-ttu-id="9855f-104">當光線交集不透明時，所叫用的著色器。</span><span class="sxs-lookup"><span data-stu-id="9855f-104">A shader that is invoked when ray intersections are not opaque.</span></span> 

<span data-ttu-id="9855f-105">任何點擊著色器都必須宣告承載參數，後面接著屬性參數。</span><span class="sxs-lookup"><span data-stu-id="9855f-105">Any hit shaders must declare a payload parameter followed by an attributes parameter.</span></span> <span data-ttu-id="9855f-106">這些參數都必須是使用者定義的結構類型，分別用於 [**TraceRay**](traceray-function.md) 和 [**ReportHit**](reporthit-function.md) ，或使用固定函式三角形交集時的 [**交集屬性結構**](intersection-attributes.md) 。</span><span class="sxs-lookup"><span data-stu-id="9855f-106">Each of these parameters must be a user-defined structure type matching types used for [**TraceRay**](traceray-function.md) and [**ReportHit**](reporthit-function.md) respectively, or the [**Intersection Attributes Structure**](intersection-attributes.md) when fixed function triangle intersection is used.</span></span>

<span data-ttu-id="9855f-107">任何點擊著色器都可以執行下列種類的作業：</span><span class="sxs-lookup"><span data-stu-id="9855f-107">Any hit shaders may perform the following kinds of operations:</span></span>

*   <span data-ttu-id="9855f-108">讀取和修改光線承載： (inout payload_t rayPayload) </span><span class="sxs-lookup"><span data-stu-id="9855f-108">Read and modify the ray payload: (inout payload_t rayPayload)</span></span>
*   <span data-ttu-id="9855f-109">讀取交集屬性： (attr_t 屬性) </span><span class="sxs-lookup"><span data-stu-id="9855f-109">Read the intersection attributes: (in attr_t attributes)</span></span>
*   <span data-ttu-id="9855f-110">呼叫 [**AcceptHitAndEndSearch**](accepthitandendsearch-function.md)，它會接受目前的點擊，結束 [任何命中的著色](any-hit-shader.md)器，結束 [交集著色器](intersection-shader.md) （如果有的話），並在最接近的點擊著色器在作用中時執行最接近的點擊 [著色器](closest-hit-shader.md) 。</span><span class="sxs-lookup"><span data-stu-id="9855f-110">Call [**AcceptHitAndEndSearch**](accepthitandendsearch-function.md), which accepts the current hit, ends the [any hit shader](any-hit-shader.md), ends the [intersection shader](intersection-shader.md) if one is present, and executes the [closest hit shader](closest-hit-shader.md) on the closest hit so far if it is active.</span></span>
*   <span data-ttu-id="9855f-111">呼叫 [**IgnoreHit**](ignorehit-function.md)，這會結束任何命中的著色器，並告知系統繼續搜尋命中，包括將控制權傳回給交集著色器（如果目前正在執行），並從 [**ReportHit**](reporthit-function.md)\* 呼叫位置傳回 false。</span><span class="sxs-lookup"><span data-stu-id="9855f-111">Call [**IgnoreHit**](ignorehit-function.md), which ends the any hit shader and tells the system to continue searching for hits, including returning control to an intersection shader, if it is currently executing, returning false from the [**ReportHit**](reporthit-function.md)\* call site.</span></span> 
*   <span data-ttu-id="9855f-112">傳回但不呼叫其中一個內建函式（可接受目前的點擊），並告知系統繼續搜尋命中，包括將控制權傳回給交集著色器（如果有的話），並在 [**ReportHit**](reporthit-function.md) 呼叫位置傳回 true，表示已接受點擊。</span><span class="sxs-lookup"><span data-stu-id="9855f-112">Return without calling either of these intrinsics, which accepts the current hit and tells the system to continue searching for hits, including returning control to the intersection shader if there is one, returning true at the [**ReportHit**](reporthit-function.md) call site to indicate that the hit was accepted.</span></span>

<span data-ttu-id="9855f-113">即使 [**IgnoreHit**](ignorehit-function.md) 或 [**AcceptHitAndEndSearch**](accepthitandendsearch-function.md)結束了任何叫用著色器調用，也必須保留對光線承載所做的任何修改。</span><span class="sxs-lookup"><span data-stu-id="9855f-113">Even if an any hit shader invocation is ended by [**IgnoreHit**](ignorehit-function.md) or [**AcceptHitAndEndSearch**](accepthitandendsearch-function.md), any modifications made to the ray payload so far must still be retained.</span></span>

## <a name="shader-type-attribute"></a><span data-ttu-id="9855f-114">著色器類型屬性</span><span class="sxs-lookup"><span data-stu-id="9855f-114">Shader Type attribute</span></span>

```
[shader("anyhit")]
```

## <a name="example"></a><span data-ttu-id="9855f-115">範例</span><span class="sxs-lookup"><span data-stu-id="9855f-115">Example</span></span>

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
