---
title: 描述元堆積
description: 描述元堆積是描述項連續配置的集合，每個描述項的一個配置。
ms.assetid: 04d3facf-21ec-45ca-ad9b-78fdcddc7136
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f19821cff5e8730c376e5c80fef07e67974d31d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104130"
---
# <a name="descriptor-heaps"></a><span data-ttu-id="9f460-103">描述元堆積</span><span class="sxs-lookup"><span data-stu-id="9f460-103">Descriptor Heaps</span></span>

<span data-ttu-id="9f460-104">描述元堆積是描述項連續配置的集合，每個描述項的一個配置。</span><span class="sxs-lookup"><span data-stu-id="9f460-104">A descriptor heap is a collection of contiguous allocations of descriptors, one allocation for every descriptor.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9f460-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="9f460-105">In this section</span></span>



| <span data-ttu-id="9f460-106">主題</span><span class="sxs-lookup"><span data-stu-id="9f460-106">Topic</span></span>                                                                                             | <span data-ttu-id="9f460-107">描述</span><span class="sxs-lookup"><span data-stu-id="9f460-107">Description</span></span>                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9f460-108">描述元堆積總覽</span><span class="sxs-lookup"><span data-stu-id="9f460-108">Descriptor Heaps Overview</span></span>](descriptor-heaps-overview.md)<br/>                             | <span data-ttu-id="9f460-109">描述元堆積包含許多不屬於管線狀態物件的物件類型 (PSO) ，例如著色器資源查看 (SRVs) 、未排序的存取視圖 (UAVs) 、常數緩衝區視圖 (CBVs) 和取樣器。</span><span class="sxs-lookup"><span data-stu-id="9f460-109">Descriptor heaps contain many object types that are not part of a Pipeline State Object (PSO), such as Shader Resource Views (SRVs), Unordered Access Views (UAVs), Constant Buffer Views (CBVs), and Samplers.</span></span> <br/>                |
| [<span data-ttu-id="9f460-110">硬體層</span><span class="sxs-lookup"><span data-stu-id="9f460-110">Hardware Tiers</span></span>](hardware-support.md)<br/>                                                 | <span data-ttu-id="9f460-111">第1層到第3層的硬體層級已增加管線的可用資源。</span><span class="sxs-lookup"><span data-stu-id="9f460-111">The levels of hardware from Tier 1 to Tier 3 have increasing resources available to the pipeline.</span></span> <br/>                                                                                                                              |
| [<span data-ttu-id="9f460-112">著色器可見的描述元堆積</span><span class="sxs-lookup"><span data-stu-id="9f460-112">Shader Visible Descriptor Heaps</span></span>](shader-visible-descriptor-heaps.md)<br/>                 | <span data-ttu-id="9f460-113">著色器可見的描述元堆積是可透過描述中繼資料表來參考著色器的描述元堆積。</span><span class="sxs-lookup"><span data-stu-id="9f460-113">Shader visible descriptor heaps, are descriptor heaps that can be referenced by shaders through descriptor tables.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="9f460-114">非著色器可見描述元堆積</span><span class="sxs-lookup"><span data-stu-id="9f460-114">Non Shader Visible Descriptor Heaps</span></span>](non-shader-visible-descriptor-heaps.md)<br/>         | <span data-ttu-id="9f460-115">部分描述元堆積無法透過描述項資料表來參考著色器，但存在於記錄命令清單之前，或因為不需要著色器可見的堆積，以協助應用程式暫存描述項。</span><span class="sxs-lookup"><span data-stu-id="9f460-115">Some descriptor heaps cannot be referenced by shaders through descriptor tables, but exist either to assist the app in staging the descriptors prior to recording a command list or because no shader-visible heap is required.</span></span><br/> |
| [<span data-ttu-id="9f460-116">建立描述元堆積</span><span class="sxs-lookup"><span data-stu-id="9f460-116">Creating Descriptor Heaps</span></span>](creating-descriptor-heaps.md)<br/>                             | <span data-ttu-id="9f460-117">若要建立和設定描述元堆積，您必須選取描述項堆積類型、判斷它包含多少個描述元，以及設定旗標，指出它是否為 CPU 可見和/或著色器可見。</span><span class="sxs-lookup"><span data-stu-id="9f460-117">To create and configure a descriptor heap, you must select a descriptor heap type, determine how many descriptors it contains, and set flags that indicate whether it is CPU visible and/or shader visible.</span></span> <br/>                    |
| [<span data-ttu-id="9f460-118">設定和填入描述元堆積</span><span class="sxs-lookup"><span data-stu-id="9f460-118">Setting and Populating Descriptor Heaps</span></span>](setting-descriptor-heaps.md)<br/>                | <span data-ttu-id="9f460-119">可以在命令清單上設定的描述項堆積型別，也就是包含描述項資料表的描述項，其中每一次最多隻能使用 (的描述中繼資料表) 。</span><span class="sxs-lookup"><span data-stu-id="9f460-119">The descriptor heap types that can be set on a command list are those that contain descriptors for which descriptor tables can be used (at most one of each at a time).</span></span> <br/>                                                        |
| [<span data-ttu-id="9f460-120">描述元堆積的配置摘要</span><span class="sxs-lookup"><span data-stu-id="9f460-120">Descriptor Heap Configurability Summary</span></span>](descriptor-heap-configurability-summary.md)<br/> | <span data-ttu-id="9f460-121">下表摘要說明著色器和非著色器可見堆積支援的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9f460-121">The following table summarizes information about Shader and non-Shader visible heap support.</span></span><br/>                                                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="9f460-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="9f460-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f460-123">描述項</span><span class="sxs-lookup"><span data-stu-id="9f460-123">Descriptors</span></span>](descriptors.md)
</dt> <dt>

[<span data-ttu-id="9f460-124">描述中繼資料表</span><span class="sxs-lookup"><span data-stu-id="9f460-124">Descriptor Tables</span></span>](descriptor-tables.md)
</dt> <dt>

[<span data-ttu-id="9f460-125">**ID3D12DescriptorHeap**</span><span class="sxs-lookup"><span data-stu-id="9f460-125">**ID3D12DescriptorHeap**</span></span>](/windows/desktop/api/d3d12/nn-d3d12-id3d12descriptorheap)
</dt> <dt>

[<span data-ttu-id="9f460-126">資源系結</span><span class="sxs-lookup"><span data-stu-id="9f460-126">Resource Binding</span></span>](resource-binding.md)
</dt> <dt>

[<span data-ttu-id="9f460-127">根簽章</span><span class="sxs-lookup"><span data-stu-id="9f460-127">Root Signatures</span></span>](root-signatures.md)
</dt> </dl>

 

 





