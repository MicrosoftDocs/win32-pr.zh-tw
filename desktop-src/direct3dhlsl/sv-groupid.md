---
title: SV_GroupID
description: 計算著色器在其中執行之執行緒群組的索引。
ms.assetid: 1b90ca74-a2b6-4a5f-aa4a-1ec879360593
keywords:
- SV_GroupID HLSL
topic_type:
- apiref
api_name:
- SV_GroupID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ab94cef0a9a33f23947e11b93a5487c65eee3890
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827037"
---
# <a name="sv_groupid"></a><span data-ttu-id="a2ae7-104">SV \_ GroupID</span><span class="sxs-lookup"><span data-stu-id="a2ae7-104">SV\_GroupID</span></span>

<span data-ttu-id="a2ae7-105">計算著色器在其中執行之執行緒群組的索引。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-105">Indices for which thread group a compute shader is executing in.</span></span> <span data-ttu-id="a2ae7-106">索引會指向整個群組，而不是個別的執行緒。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-106">The indices are to the whole group and not an individual thread.</span></span> <span data-ttu-id="a2ae7-107">可能的值會在以參數形式傳遞給 [**分派**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)的範圍內變更。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-107">Possible values vary across the range passed as parameters to [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch).</span></span> <span data-ttu-id="a2ae7-108">例如，呼叫分派 (2，1，1) 會產生可能的值0、0、0和1、0、0。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-108">For example calling Dispatch(2,1,1) results in possible values of 0,0,0 and 1,0,0.</span></span>

<span data-ttu-id="a2ae7-109">定義 [**分派呼叫**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) 內的群組位移，每個分派呼叫的維度。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-109">Defines the group offset within a [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) call, per dimension of the dispatch call.</span></span>

## <a name="type"></a><span data-ttu-id="a2ae7-110">類型</span><span class="sxs-lookup"><span data-stu-id="a2ae7-110">Type</span></span>



| <span data-ttu-id="a2ae7-111">類型</span><span class="sxs-lookup"><span data-stu-id="a2ae7-111">Type</span></span>      |
|-------|
| <span data-ttu-id="a2ae7-112">uint3</span><span class="sxs-lookup"><span data-stu-id="a2ae7-112">uint3</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a2ae7-113">備註</span><span class="sxs-lookup"><span data-stu-id="a2ae7-113">Remarks</span></span>

<span data-ttu-id="a2ae7-114">這個系統值是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-114">This system value is optional.</span></span>

<span data-ttu-id="a2ae7-115">下圖顯示傳遞給 [**分派**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)之參數的關聯性、分派 (5、3、2) 、 [numthreads](sm5-attributes-numthreads.md) 屬性中指定的值、numthreads (10、8、3) 和值，這些值會傳遞給執行緒相關系統值的計算著色器 ([SV \_ GroupIndex](sv-groupindex.md)、[sv \_ DispatchThreadID](sv-dispatchthreadid.md)、[sv \_ GroupThreadID](sv-groupthreadid.md)、sv \_ GroupID) 。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-115">The following illustration shows the relationship between the parameters passed to [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), the values specified in the [numthreads](sm5-attributes-numthreads.md) attribute, numthreads(10,8,3), and values that will passed to the compute shader for the thread-related system values ([SV\_GroupIndex](sv-groupindex.md),[SV\_DispatchThreadID](sv-dispatchthreadid.md),[SV\_GroupThreadID](sv-groupthreadid.md),SV\_GroupID).</span></span>

![分派、執行緒群組和執行緒之間關聯性的圖例](images/threadgroupids.png)

<span data-ttu-id="a2ae7-117">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="a2ae7-117">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="a2ae7-118">頂點</span><span class="sxs-lookup"><span data-stu-id="a2ae7-118">Vertex</span></span> | <span data-ttu-id="a2ae7-119">船體</span><span class="sxs-lookup"><span data-stu-id="a2ae7-119">Hull</span></span> | <span data-ttu-id="a2ae7-120">網域</span><span class="sxs-lookup"><span data-stu-id="a2ae7-120">Domain</span></span> | <span data-ttu-id="a2ae7-121">幾何</span><span class="sxs-lookup"><span data-stu-id="a2ae7-121">Geometry</span></span> | <span data-ttu-id="a2ae7-122">像素</span><span class="sxs-lookup"><span data-stu-id="a2ae7-122">Pixel</span></span> | <span data-ttu-id="a2ae7-123">計算</span><span class="sxs-lookup"><span data-stu-id="a2ae7-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="a2ae7-124">x</span><span class="sxs-lookup"><span data-stu-id="a2ae7-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="a2ae7-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a2ae7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2ae7-126">語意</span><span class="sxs-lookup"><span data-stu-id="a2ae7-126">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="a2ae7-127">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="a2ae7-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
