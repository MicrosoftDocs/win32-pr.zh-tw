---
title: SV_GroupThreadID
description: 在中執行計算著色器之執行緒群組內個別執行緒的索引。
ms.assetid: be944592-c4ea-43c9-88bc-98a9a190a437
keywords:
- SV_GroupThreadID HLSL
topic_type:
- apiref
api_name:
- SV_GroupThreadID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3d4d35766bdbdc2d69c98983a85f336ab784d24d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316267"
---
# <a name="sv_groupthreadid"></a><span data-ttu-id="ac91f-104">SV \_ GroupThreadID</span><span class="sxs-lookup"><span data-stu-id="ac91f-104">SV\_GroupThreadID</span></span>

<span data-ttu-id="ac91f-105">在中執行計算著色器之執行緒群組內個別執行緒的索引。</span><span class="sxs-lookup"><span data-stu-id="ac91f-105">Indices for which an individual thread within a thread group a compute shader is executing in.</span></span> <span data-ttu-id="ac91f-106">SV \_ GroupThreadID 在 [numthreads](sm5-attributes-numthreads.md) 屬性中為計算著色器指定的範圍內會有所不同。</span><span class="sxs-lookup"><span data-stu-id="ac91f-106">SV\_GroupThreadID varies across the range specified for the compute shader in the [numthreads](sm5-attributes-numthreads.md) attribute.</span></span> <span data-ttu-id="ac91f-107">例如，如果 numthreads (3，2，1) 指定了 SV GroupThreadID 輸入值的可能值， \_ 就會有此範圍的值 (0-2、0-1、0) 。</span><span class="sxs-lookup"><span data-stu-id="ac91f-107">For example if numthreads(3,2,1) was specified possible values for the SV\_GroupThreadID input value have this range of values (0-2,0-1,0).</span></span>

## <a name="type"></a><span data-ttu-id="ac91f-108">類型</span><span class="sxs-lookup"><span data-stu-id="ac91f-108">Type</span></span>



|       |
|-------|
| <span data-ttu-id="ac91f-109">類型</span><span class="sxs-lookup"><span data-stu-id="ac91f-109">Type</span></span>  |
| <span data-ttu-id="ac91f-110">uint3</span><span class="sxs-lookup"><span data-stu-id="ac91f-110">uint3</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ac91f-111">備註</span><span class="sxs-lookup"><span data-stu-id="ac91f-111">Remarks</span></span>

<span data-ttu-id="ac91f-112">這個系統值是選擇性的，且一律在傳遞至 [numthreads](sm5-attributes-numthreads.md) 屬性的值範圍內。</span><span class="sxs-lookup"><span data-stu-id="ac91f-112">This system value is optional, and is always within the bounds of the values passed into the [numthreads](sm5-attributes-numthreads.md) attribute.</span></span>

<span data-ttu-id="ac91f-113">下圖顯示傳遞給 [**分派**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)之參數的關聯性、分派 (5、3、2) 、 [numthreads](sm5-attributes-numthreads.md) 屬性中指定的值、numthreads (10、8、3) 和值，這些值會傳遞給執行緒相關系統值的計算著色器 ([SV \_ GroupIndex](sv-groupindex.md)、[sv \_ DispatchThreadID](sv-dispatchthreadid.md)、sv \_ GroupThreadID、[sv \_ GroupID](sv-groupid.md)) 。</span><span class="sxs-lookup"><span data-stu-id="ac91f-113">The following illustration shows the relationship between the parameters passed to [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), the values specified in the [numthreads](sm5-attributes-numthreads.md) attribute, numthreads(10,8,3), and values that will passed to the compute shader for the thread-related system values ([SV\_GroupIndex](sv-groupindex.md),[SV\_DispatchThreadID](sv-dispatchthreadid.md),SV\_GroupThreadID,[SV\_GroupID](sv-groupid.md)).</span></span>

![分派、執行緒群組和執行緒之間關聯性的圖例](images/threadgroupids.png)

<span data-ttu-id="ac91f-115">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="ac91f-115">This function is supported in the following types of shaders:</span></span>



|        |      |        |          |       |         |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ac91f-116">頂點</span><span class="sxs-lookup"><span data-stu-id="ac91f-116">Vertex</span></span> | <span data-ttu-id="ac91f-117">船體</span><span class="sxs-lookup"><span data-stu-id="ac91f-117">Hull</span></span> | <span data-ttu-id="ac91f-118">網域</span><span class="sxs-lookup"><span data-stu-id="ac91f-118">Domain</span></span> | <span data-ttu-id="ac91f-119">幾何</span><span class="sxs-lookup"><span data-stu-id="ac91f-119">Geometry</span></span> | <span data-ttu-id="ac91f-120">像素</span><span class="sxs-lookup"><span data-stu-id="ac91f-120">Pixel</span></span> | <span data-ttu-id="ac91f-121">計算</span><span class="sxs-lookup"><span data-stu-id="ac91f-121">Compute</span></span> |
|        |      |        |          |       | <span data-ttu-id="ac91f-122">x</span><span class="sxs-lookup"><span data-stu-id="ac91f-122">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="ac91f-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ac91f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac91f-124">語意</span><span class="sxs-lookup"><span data-stu-id="ac91f-124">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="ac91f-125">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="ac91f-125">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 