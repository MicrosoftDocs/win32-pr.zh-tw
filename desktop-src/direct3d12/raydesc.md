---
description: 傳遞至 TraceRay 函式來定義光線的原點、方向和範圍。
ms.assetid: ''
title: RayDesc 結構
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
ms.openlocfilehash: a5fd6e041fc476c24ff926c9c8f99f05699f5e41
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971140"
---
# <a name="raydesc-structure"></a><span data-ttu-id="03676-103">RayDesc 結構</span><span class="sxs-lookup"><span data-stu-id="03676-103">RayDesc structure</span></span>

<span data-ttu-id="03676-104">傳遞至 [**TraceRay**](traceray-function.md) 函式來定義光線的原點、方向和範圍。</span><span class="sxs-lookup"><span data-stu-id="03676-104">Passed to the [**TraceRay**](traceray-function.md) function to define the origin, direction, and extents of the ray.</span></span>

## <a name="syntax"></a><span data-ttu-id="03676-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="03676-105">Syntax</span></span>


```
struct RayDesc
{
    float3 Origin;
    float  TMin;
    float3 Direction;
    float  TMax;
};

```



## <a name="fields"></a><span data-ttu-id="03676-106">欄位</span><span class="sxs-lookup"><span data-stu-id="03676-106">Fields</span></span>

<dl> <dt>

<span data-ttu-id="03676-107"><span id="Origin"></span><span id="origin"></span>**起源**</span><span class="sxs-lookup"><span data-stu-id="03676-107"><span id="Origin"></span><span id="origin"></span>**Origin**</span></span>
</dt> <dd>

<span data-ttu-id="03676-108">光線的原點。</span><span class="sxs-lookup"><span data-stu-id="03676-108">The origin of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="03676-109"><span id="TMin"></span><span id="tmin"></span>**TMin**</span><span class="sxs-lookup"><span data-stu-id="03676-109"><span id="TMin"></span><span id="tmin"></span>**TMin**</span></span>
</dt> <dd>

<span data-ttu-id="03676-110">光線的最小範圍。</span><span class="sxs-lookup"><span data-stu-id="03676-110">The minimum extent of the ray.</span></span>


</dd> <dt>

<span data-ttu-id="03676-111"><span id="Direction"></span><span id="direction"></span>**方向**</span><span class="sxs-lookup"><span data-stu-id="03676-111"><span id="Direction"></span><span id="direction"></span>**Direction**</span></span>
</dt> <dd>

<span data-ttu-id="03676-112">光線的方向。</span><span class="sxs-lookup"><span data-stu-id="03676-112">The direction of the ray.</span></span>


</dd> <dt>

<span data-ttu-id="03676-113"><span id="TMax"></span><span id="tmax"></span>**TMax**</span><span class="sxs-lookup"><span data-stu-id="03676-113"><span id="TMax"></span><span id="tmax"></span>**TMax**</span></span>
</dt> <dd>

<span data-ttu-id="03676-114">光線的最大範圍。</span><span class="sxs-lookup"><span data-stu-id="03676-114">The maximum extent of the ray.</span></span>


</dd>

## <a name="requirements"></a><span data-ttu-id="03676-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="03676-115">Requirements</span></span>



## <a name="see-also"></a><span data-ttu-id="03676-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="03676-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03676-117">Direct3D 12 Raytracing HLSL 參考</span><span class="sxs-lookup"><span data-stu-id="03676-117">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




