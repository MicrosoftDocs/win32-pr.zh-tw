---
title: 記憶體別名和資料繼承
description: 放置和保留的資源可能會在堆積內為實體記憶體加上別名。 當堆積已設定共用旗標，或當別名的資源有完整定義的記憶體配置時，放置的資源可提供比保留資源更多的資料繼承案例。
ms.assetid: 53C5804B-0F81-41AF-83D2-A96DCDFDC94A
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cace5b5997e2a460406ae72abb247224886f3926
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103614"
---
# <a name="memory-aliasing-and-data-inheritance"></a><span data-ttu-id="07c53-104">記憶體別名和資料繼承</span><span class="sxs-lookup"><span data-stu-id="07c53-104">Memory Aliasing and Data Inheritance</span></span>

<span data-ttu-id="07c53-105">放置和保留的資源可能會在堆積內為實體記憶體加上別名。</span><span class="sxs-lookup"><span data-stu-id="07c53-105">Placed and reserved resource may alias physical memory within a heap.</span></span> <span data-ttu-id="07c53-106">當堆積已設定共用旗標，或當別名的資源有完整定義的記憶體配置時，放置的資源可提供比保留資源更多的資料繼承案例。</span><span class="sxs-lookup"><span data-stu-id="07c53-106">Placed resources enable more data inheritance scenarios than reserved resources when the heap has the shared flag set or when the aliased resources have fully defined memory layouts.</span></span>

-   [<span data-ttu-id="07c53-107">鋸齒化</span><span class="sxs-lookup"><span data-stu-id="07c53-107">Aliasing</span></span>](#memory-aliasing-and-data-inheritance)
-   [<span data-ttu-id="07c53-108">資料繼承</span><span class="sxs-lookup"><span data-stu-id="07c53-108">Data Inheritance</span></span>](#data-inheritance)
-   [<span data-ttu-id="07c53-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="07c53-109">Related topics</span></span>](#related-topics)

## <a name="aliasing"></a><span data-ttu-id="07c53-110">別名</span><span class="sxs-lookup"><span data-stu-id="07c53-110">Aliasing</span></span>

<span data-ttu-id="07c53-111">即使您不想要資料繼承，也必須在共用相同實體記憶體的兩個資源的使用方式之間發出別名屏障。</span><span class="sxs-lookup"><span data-stu-id="07c53-111">An aliasing barrier must be issued between the usage of two resources that share the same physical memory, even if data inheritance is not desired.</span></span> <span data-ttu-id="07c53-112">簡單的使用模型至少必須代表與這類作業相關的目的地資源。</span><span class="sxs-lookup"><span data-stu-id="07c53-112">Simple usage models must denote, at least, the destination resource involved in such an operation.</span></span> <span data-ttu-id="07c53-113">如需更多詳細資料和先進的使用模型，請參閱 [**CreatePlacedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource) 。</span><span class="sxs-lookup"><span data-stu-id="07c53-113">See [**CreatePlacedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource) for more details and advanced usage models.</span></span>

<span data-ttu-id="07c53-114">存取資源之後，任何與該資源分享實體記憶體的資源都會變成無效，除非允許進行資料繼承。</span><span class="sxs-lookup"><span data-stu-id="07c53-114">After a resource is accessed, any resources which share physical memory with that resource become invalidated, unless data inheritance is allowed to occur.</span></span> <span data-ttu-id="07c53-115">讀取不正確資源會導致未定義的資源內容。</span><span class="sxs-lookup"><span data-stu-id="07c53-115">Reads of invalidated resources result in undefined resource contents.</span></span> <span data-ttu-id="07c53-116">寫入不正確資源也會產生未定義的資源內容，除非發生兩個狀況：</span><span class="sxs-lookup"><span data-stu-id="07c53-116">Writes to invalidated resources also result in undefined resource contents, unless two conditions occur:</span></span>

-   <span data-ttu-id="07c53-117">資源沒有 D3D12 \_ 資源 \_ 旗標 \_ 允許 \_ 呈現 \_ 目標或 D3D12 \_ 資源 \_ 旗標 \_ 允許深度樣板 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="07c53-117">The resource does not have either the D3D12\_RESOURCE\_FLAG\_ALLOW\_RENDER\_TARGET or D3D12\_RESOURCE\_FLAG\_ALLOW\_DEPTH\_STENCIL.</span></span>
-   <span data-ttu-id="07c53-118">寫入是整個 subresource 或磚的複製或清除操作。</span><span class="sxs-lookup"><span data-stu-id="07c53-118">The write is a copy or clear operation to an entire subresource or tile.</span></span> <span data-ttu-id="07c53-119">磚-初始化僅適用于具有 64KB \_ 磚 \_ 未定義 \_ SWIZZLE 和 64kb \_ 磚 \_ 標準 \_ SWIZZLE 的資源。</span><span class="sxs-lookup"><span data-stu-id="07c53-119">Tile-initialization is only available for resources with 64KB\_TILE\_UNDEFINED\_SWIZZLE and 64KB\_TILE\_STANDARD\_SWIZZLE.</span></span>

<span data-ttu-id="07c53-120">當版面配置提供有關材質資料位置位置的資訊，以及當資源處於某些轉換屏障狀態時，重迭的失效範圍會限定為較小的資料細微性。</span><span class="sxs-lookup"><span data-stu-id="07c53-120">Overlapping invalidations are scoped to smaller granularities, when layouts provide information on the location on the location of texel data and when resources are in certain transition barrier states.</span></span> <span data-ttu-id="07c53-121">但是，失效的大小不能小於資源對齊資料細微性。</span><span class="sxs-lookup"><span data-stu-id="07c53-121">But, invalidations cannot go any smaller than resource alignment granularities.</span></span>

<span data-ttu-id="07c53-122">緩衝區對齊細微性是64KB，較大的對齊細微性則優先。</span><span class="sxs-lookup"><span data-stu-id="07c53-122">A buffer alignment granularity is 64KB, and larger alignment granularity takes precedence.</span></span> <span data-ttu-id="07c53-123">這在考慮4KB 紋理時很重要，因為多個4KB 紋理可以位於64KB 區域，而不會彼此重迭。</span><span class="sxs-lookup"><span data-stu-id="07c53-123">This is important when considering 4KB textures, as multiple 4KB textures can reside in a 64KB region without overlapping each other.</span></span> <span data-ttu-id="07c53-124">但是，相同64KB 區域的緩衝區別名無法與其中任何4KB 紋理一起使用。</span><span class="sxs-lookup"><span data-stu-id="07c53-124">But, a buffer aliasing the same 64KB region cannot be used in conjunction with any of those 4KB textures.</span></span> <span data-ttu-id="07c53-125">應用程式無法可靠地將緩衝區的存取權與 4 KB 的材質分開，因為 Gpu 可在64KB 區域內以未定義模式 swizzle 4 KB 的材質資料。</span><span class="sxs-lookup"><span data-stu-id="07c53-125">The application cannot reliably keep the access to the buffer from intersecting the 4KB textures, as GPUs are allowed to swizzle 4KB texture data within the 64KB region in an undefined pattern.</span></span>

<span data-ttu-id="07c53-126">64KB \_ 圖格 \_ 未定義 \_ SWIZZLE、64kb \_ 磚 \_ 標準 \_ SWIZZLE 和資料列 \_ 主要材質版面配置會通知應用程式，對齊資料細微性的重迭對齊已失效。</span><span class="sxs-lookup"><span data-stu-id="07c53-126">64KB\_TILE\_UNDEFINED\_SWIZZLE, 64KB\_TILE\_STANDARD\_SWIZZLE, and ROW\_MAJOR texture layouts inform the application which overlapping alignment granularities have become invalid.</span></span> <span data-ttu-id="07c53-127">例如：應用程式可以建立2D 轉譯目標紋理陣列，其中包含2個數組配量、單一 mip 層級，以及 64KB \_ 磚 \_ 未定義的 \_ SWIZZLE 版面配置。</span><span class="sxs-lookup"><span data-stu-id="07c53-127">For example: An application can create a 2D render target texture array with 2 array slices, a single mip level, and the 64KB\_TILE\_UNDEFINED\_SWIZZLE layout.</span></span> <span data-ttu-id="07c53-128">假設應用程式瞭解每個陣列配量占 100 64KB 的圖格。</span><span class="sxs-lookup"><span data-stu-id="07c53-128">Assume the application understands each array slice occupies 100 64KB tiles.</span></span> <span data-ttu-id="07c53-129">應用程式可以使用陣列配量0放棄，並針對 ~ 6MB 緩衝區、~ 6MB 紋理（具有未定義的版面配置等等）重複使用該記憶體。接下來，假設應用程式不再需要陣列配量1的第一個圖格。</span><span class="sxs-lookup"><span data-stu-id="07c53-129">The application can forgo using array slice 0, and re-use that memory for either a ~6MB buffer, a ~6MB texture with undefined layout, etc. Going further, assume the application no longer required the first tile of array slice 1.</span></span> <span data-ttu-id="07c53-130">然後，應用程式也可以在該處找出64KB 緩衝區，直到轉譯再次需要陣列配量1的第一個圖格。</span><span class="sxs-lookup"><span data-stu-id="07c53-130">Then, the application could also locate a 64KB buffer there until rendering would again require the first tile of array slice 1.</span></span> <span data-ttu-id="07c53-131">應用程式必須執行完整的磚清除或複製，才能重新使用第一個具有材質陣列的磚。</span><span class="sxs-lookup"><span data-stu-id="07c53-131">The application would have to do a full tile clear or copy in order to re-use the first tile with the texture array again.</span></span>

<span data-ttu-id="07c53-132">但是，即使材質具有已定義的版面配置仍有問題的情況。</span><span class="sxs-lookup"><span data-stu-id="07c53-132">However, even textures with defined layouts still have problematic cases.</span></span> <span data-ttu-id="07c53-133">材質資源大小可能會與應用程式本身的計算方式有很大的不同，因為某些介面卡架構會為紋理配置額外的記憶體，以在一般轉譯案例期間減少有效的頻寬。</span><span class="sxs-lookup"><span data-stu-id="07c53-133">Texture resource sizes can significantly differ from what the application can calculate itself, because some adapter architectures allocate extra memory for textures to reduce the effective bandwidth during common rendering scenarios.</span></span> <span data-ttu-id="07c53-134">任何失效的額外記憶體區域都會導致整個資源失效。</span><span class="sxs-lookup"><span data-stu-id="07c53-134">Any invalidations into that extra memory region cause the entire resource to become invalidated.</span></span> <span data-ttu-id="07c53-135">如需詳細資訊，請參閱 [**GetResourceAllocationInfo**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo) 。</span><span class="sxs-lookup"><span data-stu-id="07c53-135">See [**GetResourceAllocationInfo**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo) for more details.</span></span>

## <a name="data-inheritance"></a><span data-ttu-id="07c53-136">資料繼承</span><span class="sxs-lookup"><span data-stu-id="07c53-136">Data Inheritance</span></span>

<span data-ttu-id="07c53-137">放置的資源會啟用最多紋理的資料繼承，即使是未定義的記憶體配置。</span><span class="sxs-lookup"><span data-stu-id="07c53-137">Placed resources enable the most data inheritance for textures, even with undefined memory layouts.</span></span> <span data-ttu-id="07c53-138">應用程式可以藉由在共用堆積的相同位移上找出兩個具有相同資源屬性的材質，來模擬共用認可資源所啟用的資料繼承功能。</span><span class="sxs-lookup"><span data-stu-id="07c53-138">Applications can mimic the data inheritance capabilities that shared committed resources enable by locating two textures with identical resource properties at the same offset in a shared heap.</span></span> <span data-ttu-id="07c53-139">整個資源描述必須完全相同，包括優化的純量值和資源建立方法的類型， (放置或保留) 。</span><span class="sxs-lookup"><span data-stu-id="07c53-139">The entire resource description must be identical, including the optimized clear value and type of resource creation method (placed or reserved).</span></span> <span data-ttu-id="07c53-140">但是，這兩個資源可能會有不同的初始轉換屏障狀態。</span><span class="sxs-lookup"><span data-stu-id="07c53-140">But, both resources may have had different initial transition barrier states.</span></span>

<span data-ttu-id="07c53-141">保留的資源可啟用個別圖格資料繼承;但是資源轉換屏障狀態通常會有限制。</span><span class="sxs-lookup"><span data-stu-id="07c53-141">Reserved resources enable per-tile data inheritance; but restrictions commonly exist for resource transition barrier states.</span></span>

<span data-ttu-id="07c53-142">若要繼承資料，這兩個資源必須處於相容的資源轉換屏障狀態：</span><span class="sxs-lookup"><span data-stu-id="07c53-142">To inherit data, both resources must be in a compatible resource transition barrier state:</span></span>

-   <span data-ttu-id="07c53-143">對於緩衝區、同時存取材質和跨介面卡材質，資源轉換狀態並不重要，而且所有狀態都是「相容」。</span><span class="sxs-lookup"><span data-stu-id="07c53-143">For buffers, simultaneous access textures, and cross-adapter textures, the resource transition state is not important and all states are “compatible”.</span></span>
-   <span data-ttu-id="07c53-144">針對沒有先前屬性的保留紋理或其他每個圖格的資料繼承到 64KB \_ 磚 \_ 未定義 \_ SWIZZLE 或 64kb \_ 圖格 \_ 標準 \_ SWIZZLE，資源轉換屏障狀態（包括磚）必須處於一般狀態。</span><span class="sxs-lookup"><span data-stu-id="07c53-144">For reserved textures without the previous properties or other per-tile data inheritance through 64KB\_TILE\_UNDEFINED\_SWIZZLE or 64KB\_TILE\_STANDARD\_SWIZZLE, the resource transition barrier state including the tile must be in the common state.</span></span>
-   <span data-ttu-id="07c53-145">對於資源描述完全相符的所有其他材質，每個對應子資源的資源轉換屏障狀態必須：</span><span class="sxs-lookup"><span data-stu-id="07c53-145">For all other textures, where the resource descriptions match exactly, the resource transition barrier state for each corresponding pair of subresources must:</span></span>
    -   <span data-ttu-id="07c53-146">處於一般狀態。</span><span class="sxs-lookup"><span data-stu-id="07c53-146">Be in the common state.</span></span>
    -   <span data-ttu-id="07c53-147">當狀態的 GPU 寫入旗標相同時，就等於。</span><span class="sxs-lookup"><span data-stu-id="07c53-147">Be equal when the state has the same GPU-write flag in them.</span></span>

<span data-ttu-id="07c53-148">當 GPU 支援標準 swizzle 時，緩衝區和標準 swizzle 材質可能會對相同的記憶體進行別名，並在兩者之間繼承資料。</span><span class="sxs-lookup"><span data-stu-id="07c53-148">When the GPU supports standard swizzle, buffers and standard swizzle textures may be aliased to the same memory and inherit data between them.</span></span> <span data-ttu-id="07c53-149">應用程式可以操控緩衝區標記法中的材質，因為標準 swizzle 模式描述材質在記憶體中的配置方式。</span><span class="sxs-lookup"><span data-stu-id="07c53-149">The application can manipulate texels from the buffer representation, because the standard swizzle pattern describes how texels are laid out in memory.</span></span> <span data-ttu-id="07c53-150">CPU 可見的 swizzle 模式相當於緩衝區中看到的 GPU 可見 swizzle 模式。</span><span class="sxs-lookup"><span data-stu-id="07c53-150">The CPU-visible swizzle pattern is equivalent to the GPU-visible swizzle pattern seen in buffers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="07c53-151">相關主題</span><span class="sxs-lookup"><span data-stu-id="07c53-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07c53-152">堆積中的子分配</span><span class="sxs-lookup"><span data-stu-id="07c53-152">Suballocation Within Heaps</span></span>](suballocation-within-heaps.md)
</dt> </dl>

 

 




