---
title: SV_GroupIndex
description: '\ 0034; 壓平合併 \ 0034;執行緒群組中計算著色器執行緒的索引，會將多維度的 SV GroupThreadID 變成 \_ 1d 值。 SV \_ GroupIndex 從0變化 (numthreadsX \ numthreadsY \ numThreadsZ) \ 8211;單.'
ms.assetid: e793be10-7c83-478c-859a-4b0a2c537570
keywords:
- SV_GroupIndex HLSL
topic_type:
- apiref
api_name:
- SV_GroupIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 952a94378a0570d5bb7bc4f08959074bc8a4da4d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682577"
---
# <a name="sv_groupindex"></a><span data-ttu-id="fb575-105">SV \_ GroupIndex</span><span class="sxs-lookup"><span data-stu-id="fb575-105">SV\_GroupIndex</span></span>

<span data-ttu-id="fb575-106">執行緒群組中計算著色器執行緒的「壓平合併」索引，可將多維度的 SV \_ GroupThreadID 變成1d 值。</span><span class="sxs-lookup"><span data-stu-id="fb575-106">The "flattened" index of a compute shader thread within a thread group, which turns the multi-dimensional SV\_GroupThreadID into a 1D value.</span></span> <span data-ttu-id="fb575-107">SV \_ GroupIndex 從0變化 (numthreadsX \* numthreadsY \* numThreadsZ) –1。</span><span class="sxs-lookup"><span data-stu-id="fb575-107">SV\_GroupIndex varies from 0 to (numthreadsX \* numthreadsY \* numThreadsZ) – 1.</span></span>

## <a name="type"></a><span data-ttu-id="fb575-108">類型</span><span class="sxs-lookup"><span data-stu-id="fb575-108">Type</span></span>



| <span data-ttu-id="fb575-109">類型</span><span class="sxs-lookup"><span data-stu-id="fb575-109">Type</span></span> |
|------|
| <span data-ttu-id="fb575-110">uint</span><span class="sxs-lookup"><span data-stu-id="fb575-110">uint</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="fb575-111">備註</span><span class="sxs-lookup"><span data-stu-id="fb575-111">Remarks</span></span>


```
SV_GroupIndex = SV_GroupThreadID.z*dimx*dimy + 
                      SV_GroupThreadID.y*dimx + 
                      SV_GroupThreadID.x
```



<span data-ttu-id="fb575-112">其中 dimx 和 dimy 是進入點的 [numthreads](sm5-attributes-numthreads.md) 屬性所指定的維度。</span><span class="sxs-lookup"><span data-stu-id="fb575-112">where dimx and dimy are the dimensions specified in the [numthreads](sm5-attributes-numthreads.md) attribute for the entry point.</span></span>

<span data-ttu-id="fb575-113">這個系統值是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="fb575-113">This system value is optional.</span></span> <span data-ttu-id="fb575-114">不過，其用途可確保執行緒只會寫入至其在 groupshared 變數中指派的記憶體區域。</span><span class="sxs-lookup"><span data-stu-id="fb575-114">However, its use ensures that a thread only writes to its assigned region of memory in the groupshared variable.</span></span>

<span data-ttu-id="fb575-115">下圖顯示傳遞至 >id3d11devicecoNtext 的參數之間的關聯性 [**：:D ispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)、分派 (5、3、2) 、 [numthreads](sm5-attributes-numthreads.md) 屬性中所指定的值、numthreads (10、8、3) ，以及將傳遞給執行緒相關系統值的計算著色器的值 (SV \_ GroupIndex、[sv \_ DispatchThreadID](sv-dispatchthreadid.md)、[sv \_ GroupThreadID](sv-groupthreadid.md)、[sv \_ GroupID](sv-groupid.md)) 。</span><span class="sxs-lookup"><span data-stu-id="fb575-115">The following illustration shows the relationship between the parameters passed to [**ID3D11DeviceContext::Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), the values specified in the [numthreads](sm5-attributes-numthreads.md) attribute, numthreads(10,8,3), and values that will passed to the compute shader for the thread-related system values (SV\_GroupIndex,[SV\_DispatchThreadID](sv-dispatchthreadid.md),[SV\_GroupThreadID](sv-groupthreadid.md),[SV\_GroupID](sv-groupid.md)).</span></span>

![分派、執行緒群組和執行緒之間關聯性的圖例](images/threadgroupids.png)

<span data-ttu-id="fb575-117">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="fb575-117">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="fb575-118">頂點</span><span class="sxs-lookup"><span data-stu-id="fb575-118">Vertex</span></span> | <span data-ttu-id="fb575-119">船體</span><span class="sxs-lookup"><span data-stu-id="fb575-119">Hull</span></span> | <span data-ttu-id="fb575-120">網域</span><span class="sxs-lookup"><span data-stu-id="fb575-120">Domain</span></span> | <span data-ttu-id="fb575-121">幾何</span><span class="sxs-lookup"><span data-stu-id="fb575-121">Geometry</span></span> | <span data-ttu-id="fb575-122">像素</span><span class="sxs-lookup"><span data-stu-id="fb575-122">Pixel</span></span> | <span data-ttu-id="fb575-123">計算</span><span class="sxs-lookup"><span data-stu-id="fb575-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="fb575-124">x</span><span class="sxs-lookup"><span data-stu-id="fb575-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="fb575-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fb575-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb575-126">語意</span><span class="sxs-lookup"><span data-stu-id="fb575-126">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="fb575-127">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="fb575-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 