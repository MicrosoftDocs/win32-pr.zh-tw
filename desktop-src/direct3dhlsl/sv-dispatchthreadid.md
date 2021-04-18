---
title: SV_DispatchThreadID
description: 計算著色器所執行之合併執行緒和執行緒群組的索引。
ms.assetid: bad697f6-26d9-47cd-93e5-127621a161e8
keywords:
- SV_DispatchThreadID HLSL
topic_type:
- apiref
api_name:
- SV_DispatchThreadID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d55fcf7e291c561ecb51dd32dfac135c563974c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104559695"
---
# <a name="sv_dispatchthreadid"></a><span data-ttu-id="817c0-104">SV \_ DispatchThreadID</span><span class="sxs-lookup"><span data-stu-id="817c0-104">SV\_DispatchThreadID</span></span>

<span data-ttu-id="817c0-105">計算著色器所執行之合併執行緒和執行緒群組的索引。</span><span class="sxs-lookup"><span data-stu-id="817c0-105">Indices for which combined thread and thread group a compute shader is executing in.</span></span> <span data-ttu-id="817c0-106">SV \_ DispatchThreadID 是 sv \_ GroupID \* numthreads 和 GroupThreadID 的總和。</span><span class="sxs-lookup"><span data-stu-id="817c0-106">SV\_DispatchThreadID is the sum of SV\_GroupID \* numthreads and GroupThreadID.</span></span> <span data-ttu-id="817c0-107">它會隨著 [**分派**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) 與 [numthreads](sm5-attributes-numthreads.md)中指定的範圍而有所不同。</span><span class="sxs-lookup"><span data-stu-id="817c0-107">It varies across the range specified in [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) and [numthreads](sm5-attributes-numthreads.md).</span></span> <span data-ttu-id="817c0-108">例如，如果分派 (2，2，2) 在具有 numthreads (3，3，3) SV DispatchThreadID 的計算著色器上呼叫，則 \_ 每個維度的範圍為0到5。</span><span class="sxs-lookup"><span data-stu-id="817c0-108">For example if Dispatch(2,2,2) is called on a compute shader with numthreads(3,3,3) SV\_DispatchThreadID will have a range of 0..5 for each dimension.</span></span>

## <a name="type"></a><span data-ttu-id="817c0-109">類型</span><span class="sxs-lookup"><span data-stu-id="817c0-109">Type</span></span>



|       |
|-------|
| <span data-ttu-id="817c0-110">類型</span><span class="sxs-lookup"><span data-stu-id="817c0-110">Type</span></span>  |
| <span data-ttu-id="817c0-111">uint3</span><span class="sxs-lookup"><span data-stu-id="817c0-111">uint3</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="817c0-112">備註</span><span class="sxs-lookup"><span data-stu-id="817c0-112">Remarks</span></span>

<span data-ttu-id="817c0-113">這個系統值是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="817c0-113">This system value is optional.</span></span>

<span data-ttu-id="817c0-114">下圖顯示傳遞給 [**分派**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)之參數的關聯性、分派 (5、3、2) 、 [numthreads](sm5-attributes-numthreads.md) 屬性中指定的值、numthreads (10、8、3) 和值，這些值會傳遞給執行緒相關系統值的計算著色器 ([SV \_ GroupIndex](sv-groupindex.md)、sv \_ DispatchThreadID、[sv \_ GroupThreadID](sv-groupthreadid.md)、[sv \_ GroupID](sv-groupid.md)) 。</span><span class="sxs-lookup"><span data-stu-id="817c0-114">The following illustration shows the relationship between the parameters passed to [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), the values specified in the [numthreads](sm5-attributes-numthreads.md) attribute, numthreads(10,8,3), and values that will passed to the compute shader for the thread-related system values ([SV\_GroupIndex](sv-groupindex.md),SV\_DispatchThreadID,[SV\_GroupThreadID](sv-groupthreadid.md),[SV\_GroupID](sv-groupid.md)).</span></span>

![分派、執行緒群組和執行緒之間關聯性的圖例](images/threadgroupids.png)

<span data-ttu-id="817c0-116">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="817c0-116">This function is supported in the following types of shaders:</span></span>



|        |      |        |          |       |         |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="817c0-117">頂點</span><span class="sxs-lookup"><span data-stu-id="817c0-117">Vertex</span></span> | <span data-ttu-id="817c0-118">船體</span><span class="sxs-lookup"><span data-stu-id="817c0-118">Hull</span></span> | <span data-ttu-id="817c0-119">網域</span><span class="sxs-lookup"><span data-stu-id="817c0-119">Domain</span></span> | <span data-ttu-id="817c0-120">幾何</span><span class="sxs-lookup"><span data-stu-id="817c0-120">Geometry</span></span> | <span data-ttu-id="817c0-121">像素</span><span class="sxs-lookup"><span data-stu-id="817c0-121">Pixel</span></span> | <span data-ttu-id="817c0-122">計算</span><span class="sxs-lookup"><span data-stu-id="817c0-122">Compute</span></span> |
|        |      |        |          |       | <span data-ttu-id="817c0-123">x</span><span class="sxs-lookup"><span data-stu-id="817c0-123">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="817c0-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="817c0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="817c0-125">語意</span><span class="sxs-lookup"><span data-stu-id="817c0-125">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="817c0-126">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="817c0-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 