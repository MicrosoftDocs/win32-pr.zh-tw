---
description: 用來設定 SetPriority 中資源優先權的常數。
ms.assetid: 98886349-883f-41c3-870b-e4a639977760
title: 'D3D9_RESOURCE_PRIORITY (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3D9_RESOURCE_PRIORITY_MINIMUM
- D3D9_RESOURCE_PRIORITY_LOW
- D3D9_RESOURCE_PRIORITY_NORMAL
- D3D9_RESOURCE_PRIORITY_HIGH
- D3D9_RESOURCE_PRIORITY_MAXIMUM
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 1ae5a54c7645db63b1023c3571f8181f4ee2daec
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196209"
---
# <a name="d3d9_resource_priority"></a><span data-ttu-id="25e38-103">D3D9 \_ 資源 \_ 優先順序</span><span class="sxs-lookup"><span data-stu-id="25e38-103">D3D9\_RESOURCE\_PRIORITY</span></span>

<span data-ttu-id="25e38-104">用來設定 [**SetPriority**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dresource9-setpriority)中資源優先權的常數。</span><span class="sxs-lookup"><span data-stu-id="25e38-104">Constants used to set the priority of a resource in [**SetPriority**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dresource9-setpriority).</span></span>



| <span data-ttu-id="25e38-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="25e38-105">Constant/value</span></span>                                                                                                                                                                                                                                                                     | <span data-ttu-id="25e38-106">Description</span><span class="sxs-lookup"><span data-stu-id="25e38-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3D9_RESOURCE_PRIORITY_MINIMUM"></span><span id="d3d9_resource_priority_minimum"></span><dl> <span data-ttu-id="25e38-107"><dt>**D3D9 \_資源 \_ 優先順序 \_ 最小**</dt> <dt>0x28000000</dt></span><span class="sxs-lookup"><span data-stu-id="25e38-107"><dt>**D3D9\_RESOURCE\_PRIORITY\_MINIMUM**</dt> <dt>0x28000000</dt></span></span> </dl> | <span data-ttu-id="25e38-108">資源可能會有最低的優先順序。</span><span class="sxs-lookup"><span data-stu-id="25e38-108">The resource has the lowest priority possible.</span></span> <span data-ttu-id="25e38-109">這個常數會將資源標示為未使用和收回。</span><span class="sxs-lookup"><span data-stu-id="25e38-109">This constant marks the resource as unused and for eviction.</span></span> <span data-ttu-id="25e38-110">當另一個資源需要資源所佔用的記憶體空間時，就應該立即收回資源。</span><span class="sxs-lookup"><span data-stu-id="25e38-110">The resource should be evicted as soon as another resource requires the memory space that the resource occupies.</span></span><br/>                                                                                                                                                                                                              |
| <span id="D3D9_RESOURCE_PRIORITY_LOW"></span><span id="d3d9_resource_priority_low"></span><dl> <span data-ttu-id="25e38-111"><dt>**D3D9 \_資源 \_ 優先順序 \_ 低**</dt> <dt>0x50000000</dt></span><span class="sxs-lookup"><span data-stu-id="25e38-111"><dt>**D3D9\_RESOURCE\_PRIORITY\_LOW**</dt> <dt>0x50000000</dt></span></span> </dl>             | <span data-ttu-id="25e38-112">已排程低優先順序的資源。</span><span class="sxs-lookup"><span data-stu-id="25e38-112">The resource is scheduled with low priority.</span></span> <span data-ttu-id="25e38-113">資源的位置並不重要，而且作業系統會執行最少的工作來尋找資源的位置。</span><span class="sxs-lookup"><span data-stu-id="25e38-113">The placement of the resource is not critical, and the operating system performs minimal work to find a location for the resource.</span></span> <span data-ttu-id="25e38-114">將資源標示為低優先順序，可讓其他更重要的資源佔用更快速的記憶體。</span><span class="sxs-lookup"><span data-stu-id="25e38-114">Marking a resource as low priority allows other more critical resources to occupy the faster memory.</span></span><br/>                                                                                                                                                      |
| <span id="D3D9_RESOURCE_PRIORITY_NORMAL"></span><span id="d3d9_resource_priority_normal"></span><dl> <span data-ttu-id="25e38-115"><dt>**D3D9 \_資源 \_ 優先順序 \_ 一般**</dt> <dt>0x78000000</dt></span><span class="sxs-lookup"><span data-stu-id="25e38-115"><dt>**D3D9\_RESOURCE\_PRIORITY\_NORMAL**</dt> <dt>0x78000000</dt></span></span> </dl>    | <span data-ttu-id="25e38-116">資源會以一般優先順序排程。</span><span class="sxs-lookup"><span data-stu-id="25e38-116">The resource is scheduled with normal priority.</span></span> <span data-ttu-id="25e38-117">資源的位置對於效能而言很重要，但並不重要。</span><span class="sxs-lookup"><span data-stu-id="25e38-117">The placement of the resource is important for performance, but it is not critical.</span></span> <span data-ttu-id="25e38-118">作業系統應嘗試將標示為 normal 的資源放在資源的慣用位置，而非低優先順序的資源中。</span><span class="sxs-lookup"><span data-stu-id="25e38-118">The operating system should try to place the resource that is marked as normal in the resource's preferred location instead of a low-priority resource.</span></span> <span data-ttu-id="25e38-119">一般而言，紋理會標示為一般。</span><span class="sxs-lookup"><span data-stu-id="25e38-119">Typically, textures are marked as normal.</span></span><br/>                                                                                                     |
| <span id="D3D9_RESOURCE_PRIORITY_HIGH"></span><span id="d3d9_resource_priority_high"></span><dl> <span data-ttu-id="25e38-120"><dt>**D3D9 \_資源 \_ 優先順序 \_ 高**</dt> <dt>0xa0000000</dt></span><span class="sxs-lookup"><span data-stu-id="25e38-120"><dt>**D3D9\_RESOURCE\_PRIORITY\_HIGH**</dt> <dt>0xa0000000</dt></span></span> </dl>          | <span data-ttu-id="25e38-121">已排程高優先順序的資源。</span><span class="sxs-lookup"><span data-stu-id="25e38-121">The resource is scheduled with high priority.</span></span> <span data-ttu-id="25e38-122">資源的位置對於效能而言是不可或缺的。</span><span class="sxs-lookup"><span data-stu-id="25e38-122">The placement of the resource is critical for performance.</span></span> <span data-ttu-id="25e38-123">作業系統一律會嘗試將標示為「高」的資源放在資源的慣用位置，而非低優先順序或一般優先順序的資源。</span><span class="sxs-lookup"><span data-stu-id="25e38-123">The operating system always tries to place the resource that is marked as high in the resource's preferred location instead of a low-priority or normal-priority resource.</span></span> <span data-ttu-id="25e38-124">通常，轉譯目標會標示為高。</span><span class="sxs-lookup"><span data-stu-id="25e38-124">Typically, render targets are marked as high.</span></span><br/>                                                                                                         |
| <span id="D3D9_RESOURCE_PRIORITY_MAXIMUM"></span><span id="d3d9_resource_priority_maximum"></span><dl> <span data-ttu-id="25e38-125"><dt>**D3D9 \_資源 \_ 優先順序 \_ 最大**</dt> <dt>0xc8000000</dt></span><span class="sxs-lookup"><span data-stu-id="25e38-125"><dt>**D3D9\_RESOURCE\_PRIORITY\_MAXIMUM**</dt> <dt>0xc8000000</dt></span></span> </dl> | <span data-ttu-id="25e38-126">資源的最高優先順序可能。</span><span class="sxs-lookup"><span data-stu-id="25e38-126">The resource has the maximum priority possible.</span></span> <span data-ttu-id="25e38-127">這個常數會將資源的優先順序標示為已軟釘選。</span><span class="sxs-lookup"><span data-stu-id="25e38-127">This constant marks the priority of the resource as soft-pinned.</span></span> <span data-ttu-id="25e38-128">只有在沒有其他方法可解決 DMA 緩衝區的記憶體需求時，才會從記憶體中收回已進行軟釘釘的資源。</span><span class="sxs-lookup"><span data-stu-id="25e38-128">A soft-pinned resource is evicted from memory only if there is no other way of resolving the memory requirement of a DMA buffer.</span></span> <span data-ttu-id="25e38-129">作業系統會嘗試將 DMA 緩衝區分割成其大小下限，並收回未釘選且未在收回已軟釘選資源之前未進行軟釘選的所有其他資源。</span><span class="sxs-lookup"><span data-stu-id="25e38-129">The operating system attempts to split a DMA buffer to its minimum size and evict all other resources that are not pinned and not soft-pinned before it evicts a soft-pinned resource.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="25e38-130">備註</span><span class="sxs-lookup"><span data-stu-id="25e38-130">Remarks</span></span>

<span data-ttu-id="25e38-131">排程器會將 **D3D9 \_ 資源 \_ 優先順序 \_ 下限** 和 **D3D9 \_ 資源 \_ 優先順序 \_ 最大** 值以外的值視為提示。</span><span class="sxs-lookup"><span data-stu-id="25e38-131">Values other than **D3D9\_RESOURCE\_PRIORITY\_MINIMUM** and **D3D9\_RESOURCE\_PRIORITY\_MAXIMUM** are treated as hints by the scheduler.</span></span>

<span data-ttu-id="25e38-132">您可以使用本主題稍早所定義之值以外的優先權層級。</span><span class="sxs-lookup"><span data-stu-id="25e38-132">You can use priority levels other than the values defined earlier in this topic.</span></span> <span data-ttu-id="25e38-133">例如，將具有優先權層級0x78000001 的資源標記為，表示資源優先順序稍微高於一般。</span><span class="sxs-lookup"><span data-stu-id="25e38-133">For example, marking a resource with a priority level of 0x78000001 indicates that the resource priority is slightly above normal.</span></span>

## <a name="requirements"></a><span data-ttu-id="25e38-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="25e38-134">Requirements</span></span>



| <span data-ttu-id="25e38-135">需求</span><span class="sxs-lookup"><span data-stu-id="25e38-135">Requirement</span></span> | <span data-ttu-id="25e38-136">值</span><span class="sxs-lookup"><span data-stu-id="25e38-136">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="25e38-137">標頭</span><span class="sxs-lookup"><span data-stu-id="25e38-137">Header</span></span><br/> | <dl> <span data-ttu-id="25e38-138"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="25e38-138"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25e38-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="25e38-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25e38-140">Direct3D 常數</span><span class="sxs-lookup"><span data-stu-id="25e38-140">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
