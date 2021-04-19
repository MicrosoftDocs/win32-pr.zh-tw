---
description: 在加速結構中將光線傳送到搜尋中。
ms.assetid: ''
title: TraceRay 函式
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TraceRay
api_type:
- NA
ms.openlocfilehash: faeed928b25acb4dac95e47a46a103daf87124e0
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "106992644"
---
# <a name="traceray-function"></a><span data-ttu-id="aad21-103">TraceRay 函式</span><span class="sxs-lookup"><span data-stu-id="aad21-103">TraceRay function</span></span>

<span data-ttu-id="aad21-104">在加速結構中將光線傳送到搜尋中。</span><span class="sxs-lookup"><span data-stu-id="aad21-104">Sends a ray into a search for hits in an acceleration structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="aad21-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="aad21-105">Syntax</span></span>
<span data-ttu-id="aad21-106">此內建函式定義相當於下列函式範本：</span><span class="sxs-lookup"><span data-stu-id="aad21-106">This intrinsic function definition is equivalent to the following function template:</span></span>

```
Template<payload_t>
void TraceRay(RaytracingAccelerationStructure AccelerationStructure,
              uint RayFlags,
              uint InstanceInclusionMask,
              uint RayContributionToHitGroupIndex,
              uint MultiplierForGeometryContributionToHitGroupIndex,
              uint MissShaderIndex,
              RayDesc Ray,
              inout payload_t Payload);

```



## <a name="parameters"></a><span data-ttu-id="aad21-107">參數</span><span class="sxs-lookup"><span data-stu-id="aad21-107">Parameters</span></span>

`AccelerationStructure`

<span data-ttu-id="aad21-108">要使用的最上層加速結構。</span><span class="sxs-lookup"><span data-stu-id="aad21-108">The top-level acceleration structure to use.</span></span> <span data-ttu-id="aad21-109">指定 Null 加速結構會強制遺漏。</span><span class="sxs-lookup"><span data-stu-id="aad21-109">Specifying a NULL acceleration structure forces a miss.</span></span>

`RayFlags`

<span data-ttu-id="aad21-110">[Ray_flag](ray_flag.md)值的有效組合。</span><span class="sxs-lookup"><span data-stu-id="aad21-110">Valid combination of [ray_flag](ray_flag.md) values.</span></span> <span data-ttu-id="aad21-111">系統只會傳播定義的光線旗標，也就是 [RayFlags](rayflags.md) 著色器內建可看見。</span><span class="sxs-lookup"><span data-stu-id="aad21-111">Only defined ray flags are propagated by the system, i.e. are visible to the [RayFlags](rayflags.md) shader intrinsic.</span></span>

`InstanceInclusionMask`

<span data-ttu-id="aad21-112">不帶正負號的整數，也就是用來根據每個實例中的 InstanceMask 來包含或拒絕幾何實例的最下方8位。</span><span class="sxs-lookup"><span data-stu-id="aad21-112">An unsigned integer, the bottom 8 bits of which are used to include or reject geometry instances based on the InstanceMask in each instance.</span></span> <span data-ttu-id="aad21-113">例如：</span><span class="sxs-lookup"><span data-stu-id="aad21-113">For example:</span></span>
```
if(!((InstanceInclusionMask & InstanceMask) & 0xff)) { //ignore intersection }
```

`RayContributionToHitGroupIndex`

<span data-ttu-id="aad21-114">不帶正負號的整數，指定要加入的位移，以針對點擊群組索引，在著色器資料表內進行計算。</span><span class="sxs-lookup"><span data-stu-id="aad21-114">An unsigned integer specifying the offset to add into addressing calculations within shader tables for hit group indexing.</span></span>  <span data-ttu-id="aad21-115">只會使用此值的底部4位。</span><span class="sxs-lookup"><span data-stu-id="aad21-115">Only the bottom 4 bits of this value are used.</span></span>

`MultiplierForGeometryContributionToHitGroupIndex`

<span data-ttu-id="aad21-116">不帶正負號的整數，指定要乘以 *GeometryContributionToHitGroupIndex* 的跨距，也就是以0為基底的索引，應用程式將幾何提供給其最底層的加速結構。</span><span class="sxs-lookup"><span data-stu-id="aad21-116">An unsigned integer specifying the stride to multiply by *GeometryContributionToHitGroupIndex*, which is just the 0 based index the geometry was supplied by the app into its bottom-level acceleration structure.</span></span> <span data-ttu-id="aad21-117">只會使用這個乘數值的下16位。</span><span class="sxs-lookup"><span data-stu-id="aad21-117">Only the bottom 16 bits of this multiplier value are used.</span></span>

`MissShaderIndex`

<span data-ttu-id="aad21-118">不帶正負號的整數，指定著色器資料表內遺漏著色器的索引。</span><span class="sxs-lookup"><span data-stu-id="aad21-118">An unsigned integer specifying the index of the miss shader within a shader table.</span></span>

`Ray`

<span data-ttu-id="aad21-119">[**RayDesc**](raydesc.md) ，表示要追蹤的光線。</span><span class="sxs-lookup"><span data-stu-id="aad21-119">A [**RayDesc**](raydesc.md) representing the ray to be traced.</span></span>

`Payload`

<span data-ttu-id="aad21-120">使用者定義的光線承載，可針對在 raytracing 期間叫用的著色器，同時存取輸入和輸出。</span><span class="sxs-lookup"><span data-stu-id="aad21-120">A user defined ray payload accessed both for both input and output by shaders invoked during raytracing.</span></span>  <span data-ttu-id="aad21-121">[**TraceRay**](traceray-function.md)完成後，呼叫端也可以存取承載。</span><span class="sxs-lookup"><span data-stu-id="aad21-121">After [**TraceRay**](traceray-function.md) completes, the caller can access the payload as well.</span></span>

## <a name="return-value"></a><span data-ttu-id="aad21-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="aad21-122">Return Value</span></span>

<span data-ttu-id="aad21-123">**void**</span><span class="sxs-lookup"><span data-stu-id="aad21-123">**void**</span></span>

## <a name="remarks"></a><span data-ttu-id="aad21-124">備註</span><span class="sxs-lookup"><span data-stu-id="aad21-124">Remarks</span></span>

<span data-ttu-id="aad21-125">您可以從下列 raytracing 著色器類型呼叫這個函數：</span><span class="sxs-lookup"><span data-stu-id="aad21-125">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="aad21-126">**最接近的點擊著色器**</span><span class="sxs-lookup"><span data-stu-id="aad21-126">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="aad21-127">**遺漏著色器**</span><span class="sxs-lookup"><span data-stu-id="aad21-127">**Miss Shader**</span></span>](miss-shader.md)
* [<span data-ttu-id="aad21-128">**光線產生著色器**</span><span class="sxs-lookup"><span data-stu-id="aad21-128">**Ray Generation Shader**</span></span>](ray-generation-shader.md)



## <a name="see-also"></a><span data-ttu-id="aad21-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aad21-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aad21-130">Direct3D 12 Raytracing HLSL 參考</span><span class="sxs-lookup"><span data-stu-id="aad21-130">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




