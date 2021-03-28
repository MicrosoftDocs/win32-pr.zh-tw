---
title: numthreads
description: 定義在分派計算著色器時，要在單一線程群組中執行的執行緒數目 (查看 >id3d11devicecoNtext 分派) 。
ms.assetid: ec6b751c-d81c-4221-ae80-166d2a3707fe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: abcca751b58bc88ba984ac5c2210a563591d592e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382737"
---
# <a name="numthreads"></a><span data-ttu-id="28877-103">numthreads</span><span class="sxs-lookup"><span data-stu-id="28877-103">numthreads</span></span>

<span data-ttu-id="28877-104">定義在分派計算著色器時，要在單一線程群組中執行的執行緒數目 (請參閱 [**>id3d11devicecoNtext：:D ispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)) 。</span><span class="sxs-lookup"><span data-stu-id="28877-104">Defines the number of threads to be executed in a single thread group when a compute shader is dispatched (see [**ID3D11DeviceContext::Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)).</span></span>


```
numthreads(X, Y, Z)    
```



<span data-ttu-id="28877-105">X、Y 和 Z 值表示特定方向的執行緒群組大小，X Y z 的總計會 \* \* 提供群組中的執行緒數目。</span><span class="sxs-lookup"><span data-stu-id="28877-105">The X, Y and Z values indicate the size of the thread group in a particular direction and the total of X\*Y\*Z gives the number of threads in the group.</span></span> <span data-ttu-id="28877-106">在三個維度上指定執行緒群組大小的功能，可讓您以邏輯2D 和3D 資料結構的方式存取個別的執行緒。</span><span class="sxs-lookup"><span data-stu-id="28877-106">The ability to specify the size of the thread group across three dimensions allows individual threads to be accessed in a manner that logically 2D and 3D data structures.</span></span>

<span data-ttu-id="28877-107">例如，如果計算著色器正在進行4x4 矩陣加法，則 numthreads 可以設定為 numthreads (4，4，1) 而且個別執行緒中的索引會自動符合矩陣專案。</span><span class="sxs-lookup"><span data-stu-id="28877-107">For example, if a compute shader is doing 4x4 matrix addition then numthreads could be set to numthreads(4,4,1) and the indexing in the individual threads would automatically match the matrix entries.</span></span> <span data-ttu-id="28877-108">計算著色器也可以使用 numthreads (16，1，1) ，宣告具有相同執行緒數目 (16) 的執行緒群組，不過它接著必須根據目前的執行緒編號來計算目前的矩陣專案。</span><span class="sxs-lookup"><span data-stu-id="28877-108">The compute shader could also declare a thread group with the same number of threads (16) using numthreads(16,1,1), however it would then have to calculate the current matrix entry based on the current thread number.</span></span>

<span data-ttu-id="28877-109">**Numthreads** 可允許的參數值取決於計算著色器版本。</span><span class="sxs-lookup"><span data-stu-id="28877-109">The allowable parameter values for **numthreads** depends on the compute shader version.</span></span>



| <span data-ttu-id="28877-110">計算著色器</span><span class="sxs-lookup"><span data-stu-id="28877-110">Compute Shader</span></span> | <span data-ttu-id="28877-111">最大 Z</span><span class="sxs-lookup"><span data-stu-id="28877-111">Maximum Z</span></span> | <span data-ttu-id="28877-112">最大執行緒 (X \* Y \* Z) </span><span class="sxs-lookup"><span data-stu-id="28877-112">Maximum Threads (X\*Y\*Z)</span></span> |
|----------------|-----------|---------------------------|
| <span data-ttu-id="28877-113">cs \_ 4 \_ x</span><span class="sxs-lookup"><span data-stu-id="28877-113">cs\_4\_x</span></span>       | <span data-ttu-id="28877-114">1</span><span class="sxs-lookup"><span data-stu-id="28877-114">1</span></span>         | <span data-ttu-id="28877-115">768</span><span class="sxs-lookup"><span data-stu-id="28877-115">768</span></span>                       |
| <span data-ttu-id="28877-116">cs \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="28877-116">cs\_5\_0</span></span>       | <span data-ttu-id="28877-117">64</span><span class="sxs-lookup"><span data-stu-id="28877-117">64</span></span>        | <span data-ttu-id="28877-118">1024</span><span class="sxs-lookup"><span data-stu-id="28877-118">1024</span></span>                      |



 

<span data-ttu-id="28877-119">下圖顯示傳遞至 >id3d11devicecoNtext 的參數之間的關聯性 [**：:D ispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)、分派 (5、3、2) 、numthreads 屬性中指定的值、numthreads (10、8、3) 以及將傳遞給執行緒相關系統值的計算著色器的值 ([SV \_ GroupIndex](sv-groupindex.md)、[sv \_ DispatchThreadID](sv-dispatchthreadid.md)、[sv \_ GroupThreadID](sv-groupthreadid.md)、[sv \_ GroupID](sv-groupid.md)) 。</span><span class="sxs-lookup"><span data-stu-id="28877-119">The following illustration shows the relationship between the parameters passed to [**ID3D11DeviceContext::Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), the values specified in the numthreads attribute, numthreads(10,8,3), and values that will passed to the compute shader for the thread related system values ([SV\_GroupIndex](sv-groupindex.md),[SV\_DispatchThreadID](sv-dispatchthreadid.md),[SV\_GroupThreadID](sv-groupthreadid.md),[SV\_GroupID](sv-groupid.md)).</span></span>

![分派、執行緒群組和執行緒之間關聯性的圖例](images/threadgroupids.png)

<span data-ttu-id="28877-121">下列著色器類型支援此屬性：</span><span class="sxs-lookup"><span data-stu-id="28877-121">This attribute is supported in the following types of shaders:</span></span>



| <span data-ttu-id="28877-122">頂點</span><span class="sxs-lookup"><span data-stu-id="28877-122">Vertex</span></span> | <span data-ttu-id="28877-123">船體</span><span class="sxs-lookup"><span data-stu-id="28877-123">Hull</span></span> | <span data-ttu-id="28877-124">網域</span><span class="sxs-lookup"><span data-stu-id="28877-124">Domain</span></span> | <span data-ttu-id="28877-125">幾何</span><span class="sxs-lookup"><span data-stu-id="28877-125">Geometry</span></span> | <span data-ttu-id="28877-126">像素</span><span class="sxs-lookup"><span data-stu-id="28877-126">Pixel</span></span> | <span data-ttu-id="28877-127">計算</span><span class="sxs-lookup"><span data-stu-id="28877-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="28877-128">x</span><span class="sxs-lookup"><span data-stu-id="28877-128">x</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="28877-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="28877-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28877-130">著色器模型5屬性</span><span class="sxs-lookup"><span data-stu-id="28877-130">Shader Model 5 Attributes</span></span>](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[<span data-ttu-id="28877-131">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="28877-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 