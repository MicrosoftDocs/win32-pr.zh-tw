---
description: 表示光線目前參數起點的 float。
ms.assetid: ''
title: RayTMin
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RayTMin
api_type:
- NA
ms.openlocfilehash: 00db0eb46e8c011e5b31f773679e19ca6dd4a7a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970337"
---
# <a name="raytmin"></a><span data-ttu-id="9e88b-103">RayTMin</span><span class="sxs-lookup"><span data-stu-id="9e88b-103">RayTMin</span></span>

<span data-ttu-id="9e88b-104">表示光線目前參數起點的 float。</span><span class="sxs-lookup"><span data-stu-id="9e88b-104">A float representing the current parametric starting point for the ray.</span></span> 

## <a name="syntax"></a><span data-ttu-id="9e88b-105">語法</span><span class="sxs-lookup"><span data-stu-id="9e88b-105">Syntax</span></span>

```
float RayTMin();

```

## <a name="remarks"></a><span data-ttu-id="9e88b-106">備註</span><span class="sxs-lookup"><span data-stu-id="9e88b-106">Remarks</span></span>

<span data-ttu-id="9e88b-107">**RayTMin** 會根據下列公式來定義光線的起點：原點 + (方向 \* RayTMin) 。</span><span class="sxs-lookup"><span data-stu-id="9e88b-107">**RayTMin** defines the starting point of the ray according to the following formula: Origin + (Direction \* RayTMin).</span></span>  <span data-ttu-id="9e88b-108">*來源* 和 *方向* 可能位於世界或物件空間中，這會導致世界或物件空間的起點。</span><span class="sxs-lookup"><span data-stu-id="9e88b-108">*Origin* and *Direction* may be in either world or object space, which results in either a world or an object space starting point.</span></span>

<span data-ttu-id="9e88b-109">**RayTMin** 是在 [**TraceRay**](traceray-function.md)的呼叫中指定，並且在該呼叫的持續時間內是常數。</span><span class="sxs-lookup"><span data-stu-id="9e88b-109">**RayTMin** is specified in the call to [**TraceRay**](traceray-function.md), and is constant for the duration of that call.</span></span>




<span data-ttu-id="9e88b-110">您可以從下列 raytracing 著色器類型呼叫這個函數：</span><span class="sxs-lookup"><span data-stu-id="9e88b-110">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="9e88b-111">**任何命中著色器**</span><span class="sxs-lookup"><span data-stu-id="9e88b-111">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="9e88b-112">**最接近的點擊著色器**</span><span class="sxs-lookup"><span data-stu-id="9e88b-112">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="9e88b-113">**交集著色器**</span><span class="sxs-lookup"><span data-stu-id="9e88b-113">**Intersection Shader**</span></span>](intersection-shader.md)
* [<span data-ttu-id="9e88b-114">**遺漏著色器**</span><span class="sxs-lookup"><span data-stu-id="9e88b-114">**Miss Shader**</span></span>](miss-shader.md)





## <a name="see-also"></a><span data-ttu-id="9e88b-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9e88b-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e88b-116">Direct3D 12 Raytracing HLSL 參考</span><span class="sxs-lookup"><span data-stu-id="9e88b-116">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




