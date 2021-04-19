---
description: 浮點數，代表光線目前的參數結束點。
ms.assetid: ''
title: RayTCurrent
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RayTCurrent
api_type:
- NA
ms.openlocfilehash: 4f090bab88c6be671ca0614255fd7bdebb0d1549
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979714"
---
# <a name="raytcurrent"></a><span data-ttu-id="e60c0-103">RayTCurrent</span><span class="sxs-lookup"><span data-stu-id="e60c0-103">RayTCurrent</span></span>

<span data-ttu-id="e60c0-104">浮點數，代表光線目前的參數結束點。</span><span class="sxs-lookup"><span data-stu-id="e60c0-104">A float representing the current parametric ending point for the ray.</span></span>  

## <a name="syntax"></a><span data-ttu-id="e60c0-105">語法</span><span class="sxs-lookup"><span data-stu-id="e60c0-105">Syntax</span></span>

```
float RayTCurrent();

```


## <a name="remarks"></a><span data-ttu-id="e60c0-106">備註</span><span class="sxs-lookup"><span data-stu-id="e60c0-106">Remarks</span></span>

<span data-ttu-id="e60c0-107">**RayTCurrent** 會根據下列公式來定義光線的目前結束點：原點 + (方向 \* RayTCurrent) 。</span><span class="sxs-lookup"><span data-stu-id="e60c0-107">**RayTCurrent** defines the current ending point of the ray according to the following formula: Origin + (Direction \* RayTCurrent).</span></span>  <span data-ttu-id="e60c0-108">*原點* 和 *方向* 可能位於世界或物件空間中，這會導致世界或物件空間結束點。</span><span class="sxs-lookup"><span data-stu-id="e60c0-108">*Origin* and *Direction* may be in either world or object space, which results in either a world or an object space ending point.</span></span>

<span data-ttu-id="e60c0-109">**RayTCurrent** 會在具有 [**RayDesc：： TMax**](raydesc.md)值的呼叫 [**TraceRay**](traceray-function.md)呼叫中初始化，然後在追蹤查詢期間更新，以在任何點擊) 中回報交集 (，並接受。</span><span class="sxs-lookup"><span data-stu-id="e60c0-109">**RayTCurrent** is initialized in the call [**TraceRay**](traceray-function.md) call with the [**RayDesc::TMax**](raydesc.md) value and then is updated during the trace query as intersections are reported (in the any hit), and accepted.</span></span>

<span data-ttu-id="e60c0-110">在 [交集著色器](intersection-shader.md)中，它代表到目前為止最接近交集的距離。</span><span class="sxs-lookup"><span data-stu-id="e60c0-110">In the [intersection shader](intersection-shader.md), it represents the distance to the closest intersection found so far.</span></span>  <span data-ttu-id="e60c0-111">如果已接受叫用，則會在 () 至所提供的賦值值之後更新此值。</span><span class="sxs-lookup"><span data-stu-id="e60c0-111">It will be updated after () to the THit value provided if the hit was accepted.</span></span>

<span data-ttu-id="e60c0-112">在 [任何點擊著色器](any-hit-shader.md)中，它代表目前所報告交集的距離。</span><span class="sxs-lookup"><span data-stu-id="e60c0-112">In the [any hit shader](any-hit-shader.md), it represents the distance to the current intersection being reported.</span></span>

<span data-ttu-id="e60c0-113">在 [最接近的點擊著色器](closest-hit-shader.md)中，它代表已接受的最接近交集距離。</span><span class="sxs-lookup"><span data-stu-id="e60c0-113">In the [closest hit shader](closest-hit-shader.md), it represents the distance to the closest intersection accepted.</span></span>

<span data-ttu-id="e60c0-114">在 [遺漏著色器](miss-shader.md)中，它等於傳遞給 **TraceRay** 呼叫的 *TMax* 。</span><span class="sxs-lookup"><span data-stu-id="e60c0-114">In the [miss shader](miss-shader.md), it is equal to *TMax* passed to the **TraceRay** call.</span></span>


<span data-ttu-id="e60c0-115">您可以從下列 raytracing 著色器類型呼叫這個函數：</span><span class="sxs-lookup"><span data-stu-id="e60c0-115">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="e60c0-116">**任何命中著色器**</span><span class="sxs-lookup"><span data-stu-id="e60c0-116">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="e60c0-117">**最接近的點擊著色器**</span><span class="sxs-lookup"><span data-stu-id="e60c0-117">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="e60c0-118">**交集著色器**</span><span class="sxs-lookup"><span data-stu-id="e60c0-118">**Intersection Shader**</span></span>](intersection-shader.md)
* [<span data-ttu-id="e60c0-119">**遺漏著色器**</span><span class="sxs-lookup"><span data-stu-id="e60c0-119">**Miss Shader**</span></span>](miss-shader.md)





## <a name="see-also"></a><span data-ttu-id="e60c0-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e60c0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e60c0-121">Direct3D 12 Raytracing HLSL 參考</span><span class="sxs-lookup"><span data-stu-id="e60c0-121">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




