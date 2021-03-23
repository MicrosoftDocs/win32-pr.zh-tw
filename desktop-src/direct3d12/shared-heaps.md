---
title: 共用堆積
description: 共用適用于多進程和多介面卡架構。
ms.assetid: 67C6B1D4-BF76-45A9-BADC-7C9520C900EB
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f4271055f88e38484041c225b6b17c6d75f0d98
ms.sourcegitcommit: d6102d9e2b26368142fe5b006c65acb50c98be65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/26/2019
ms.locfileid: "74104113"
---
# <a name="shared-heaps"></a><span data-ttu-id="ed5d5-103">共用堆積</span><span class="sxs-lookup"><span data-stu-id="ed5d5-103">Shared Heaps</span></span>

<span data-ttu-id="ed5d5-104">共用適用于多進程和多介面卡架構。</span><span class="sxs-lookup"><span data-stu-id="ed5d5-104">Sharing is useful for multi-process and multi-adapter architectures.</span></span>

-   [<span data-ttu-id="ed5d5-105">共用總覽</span><span class="sxs-lookup"><span data-stu-id="ed5d5-105">Sharing overview</span></span>](#sharing-overview)
-   [<span data-ttu-id="ed5d5-106">跨進程共用堆積</span><span class="sxs-lookup"><span data-stu-id="ed5d5-106">Sharing heaps across processes</span></span>](#sharing-heaps-across-processes)
-   [<span data-ttu-id="ed5d5-107">跨介面卡共用堆積</span><span class="sxs-lookup"><span data-stu-id="ed5d5-107">Sharing heaps across adapters</span></span>](#sharing-heaps-across-adapters)
-   [<span data-ttu-id="ed5d5-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="ed5d5-108">Related topics</span></span>](#related-topics)

## <a name="sharing-overview"></a><span data-ttu-id="ed5d5-109">共用總覽</span><span class="sxs-lookup"><span data-stu-id="ed5d5-109">Sharing overview</span></span>

<span data-ttu-id="ed5d5-110">共用堆積有兩項功能：在一或多個進程之間共用堆積中的資料，以及針對堆積內的資源阻止不具決定性的非定義材質配置選項。</span><span class="sxs-lookup"><span data-stu-id="ed5d5-110">Shared heaps enable two things: sharing data in a heap across one or more processes, and precluding a non-deterministic choice of undefined texture layout for resources placed within the heap.</span></span> <span data-ttu-id="ed5d5-111">在介面卡之間共用堆積也可免除資料的 CPU 封送處理需求。</span><span class="sxs-lookup"><span data-stu-id="ed5d5-111">Sharing heaps across adapters also removes the need for CPU marshaling of the data.</span></span>

<span data-ttu-id="ed5d5-112">堆積和認可的資源都可以共用。</span><span class="sxs-lookup"><span data-stu-id="ed5d5-112">Both heaps and committed resources can be shared.</span></span> <span data-ttu-id="ed5d5-113">共用認可的資源實際上會與認可的資源描述共用隱含堆積，讓相容的資源描述可以對應到另一部裝置的堆積。</span><span class="sxs-lookup"><span data-stu-id="ed5d5-113">Sharing a committed resource actually shares the implicit heap along with the committed resource description, such that a compatible resource description can be mapped to the heap from another device.</span></span>

<span data-ttu-id="ed5d5-114">所有方法都可自由執行緒，並繼承 NT 控制碼共用設計的現有 D3D11 語義。</span><span class="sxs-lookup"><span data-stu-id="ed5d5-114">All methods are free-threaded and inherit the existing D3D11 semantics of the NT handle sharing design.</span></span>

-   [<span data-ttu-id="ed5d5-115">**ID3D12Device::CreateSharedHandle**</span><span class="sxs-lookup"><span data-stu-id="ed5d5-115">**ID3D12Device::CreateSharedHandle**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createsharedhandle)
-   [<span data-ttu-id="ed5d5-116">**ID3D12Device::OpenSharedHandle**</span><span class="sxs-lookup"><span data-stu-id="ed5d5-116">**ID3D12Device::OpenSharedHandle**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandle)
-   [<span data-ttu-id="ed5d5-117">**ID3D12Device::OpenSharedHandleByName**</span><span class="sxs-lookup"><span data-stu-id="ed5d5-117">**ID3D12Device::OpenSharedHandleByName**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandlebyname)

## <a name="sharing-heaps-across-processes"></a><span data-ttu-id="ed5d5-118">跨進程共用堆積</span><span class="sxs-lookup"><span data-stu-id="ed5d5-118">Sharing heaps across processes</span></span>

<span data-ttu-id="ed5d5-119">共用堆積會以 \_ \_ \_ [**D3D12 \_ 堆積 \_ 旗標**](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_flags) 列舉的 D3D12 堆積旗標共用成員來指定。</span><span class="sxs-lookup"><span data-stu-id="ed5d5-119">Shared heaps are specified with the D3D12\_HEAP\_FLAG\_SHARED member of the [**D3D12\_HEAP\_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_flags) enum.</span></span>

<span data-ttu-id="ed5d5-120">在可存取 CPU 的堆積上，不支援共用堆積： D3D12 \_ 堆積 \_ 類型 \_ 上傳、D3D12 \_ 堆積 \_ 類型 \_ READBACK 和 D3D12 \_ 堆積 \_ 類型 \_ 自訂，不含 D3D12 \_ CPU \_ 頁面 \_ 屬性 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="ed5d5-120">Shared heaps are not supported on CPU-accessible heaps: D3D12\_HEAP\_TYPE\_UPLOAD, D3D12\_HEAP\_TYPE\_READBACK, and D3D12\_HEAP\_TYPE\_CUSTOM without D3D12\_CPU\_PAGE\_PROPERTY\_NOT\_AVAILABLE.</span></span>

<span data-ttu-id="ed5d5-121">阻止不具決定性的未定義材質版面配置，可能會大幅影響某些 Gpu 上的延遲轉譯案例，因此它不是放置和認可資源的預設行為。</span><span class="sxs-lookup"><span data-stu-id="ed5d5-121">Precluding a non-deterministic choice of undefined texture layout can significantly impair deferred rendering scenarios on some GPUs, so it is not the default behavior for placed and committed resources.</span></span> <span data-ttu-id="ed5d5-122">某些 GPU 架構上的延遲轉譯受損，因為具決定性的材質版面配置會降低在轉譯為相同格式和大小的多個轉譯目標紋理時所達到的有效記憶體頻寬。</span><span class="sxs-lookup"><span data-stu-id="ed5d5-122">Deferred rendering is impaired on some GPU architectures because deterministic texture layouts decrease the effective memory bandwidth achieved when rendering simultaneously to multiple render target textures of the same format and size.</span></span> <span data-ttu-id="ed5d5-123">GPU 架構不斷演進，無法利用非決定性的材質配置來支援標準化的 swizzle 模式和標準化的版面配置，以進行延遲的呈現。</span><span class="sxs-lookup"><span data-stu-id="ed5d5-123">GPU architectures are evolving away from leveraging non-deterministic texture layouts in order to support standardized swizzle patterns and standardized layouts efficiently for deferred rendering.</span></span>

<span data-ttu-id="ed5d5-124">共用堆積也會伴隨其他小成本：</span><span class="sxs-lookup"><span data-stu-id="ed5d5-124">Shared heaps come with other minor costs as well:</span></span>

-   <span data-ttu-id="ed5d5-125">由於有資訊洩漏的問題，因此無法將共用堆積資料回收為彈性，因為同進程堆積會導致實體記憶體的 zero'ed 更頻繁。</span><span class="sxs-lookup"><span data-stu-id="ed5d5-125">Shared heap data cannot be recycled as flexibly as in-process heaps due to information disclosure concerns, so physical memory is zero'ed more often.</span></span>
-   <span data-ttu-id="ed5d5-126">在建立和終結共用堆積期間，會有額外的 CPU 額外負荷和系統記憶體使用量增加。</span><span class="sxs-lookup"><span data-stu-id="ed5d5-126">There is a minor additional CPU overhead and increased system memory usage during creation and destruction of shared heaps.</span></span>

## <a name="sharing-heaps-across-adapters"></a><span data-ttu-id="ed5d5-127">跨介面卡共用堆積</span><span class="sxs-lookup"><span data-stu-id="ed5d5-127">Sharing heaps across adapters</span></span>

<span data-ttu-id="ed5d5-128">您可以使用 \_ \_ \_ \_ \_ [**D3D12 \_ 堆積 \_ 旗標**](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_flags) 列舉的 D3D12 堆積旗標共用交叉配接器成員，指定跨介面卡的共用堆積。</span><span class="sxs-lookup"><span data-stu-id="ed5d5-128">Shared heaps across adapters is specified with the D3D12\_HEAP\_FLAG\_SHARED\_CROSS\_ADAPTER member of the [**D3D12\_HEAP\_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_flags) enum.</span></span>

<span data-ttu-id="ed5d5-129">跨介面卡共用堆積可讓多個介面卡共用資料，而不會在 CPU 之間將資料封送處理。</span><span class="sxs-lookup"><span data-stu-id="ed5d5-129">Cross adapter shared heaps enable multiple adapters to share data without the CPU marshaling the data between them.</span></span> <span data-ttu-id="ed5d5-130">雖然不同的介面卡功能會判斷介面卡在兩者之間傳遞資料的效率，但只是啟用 GPU 複本可增加達到的有效頻寬。</span><span class="sxs-lookup"><span data-stu-id="ed5d5-130">While varying adapter capabilities determine how efficient adapters can pass data between them, merely enabling GPU copies increases the effective bandwidth achieved.</span></span> <span data-ttu-id="ed5d5-131">即使不支援這類材質配置，跨介面卡堆積還是允許某些材質配置來支援材質資料的交換。</span><span class="sxs-lookup"><span data-stu-id="ed5d5-131">Some texture layouts are allowed on cross adapter heaps to support an interchange of texture data, even if such texture layouts are not otherwise supported.</span></span> <span data-ttu-id="ed5d5-132">某些限制可能適用于這類紋理，例如僅支援複製。</span><span class="sxs-lookup"><span data-stu-id="ed5d5-132">Certain restrictions may apply to such textures, such as only supporting copying.</span></span>

<span data-ttu-id="ed5d5-133">跨介面卡共用可搭配呼叫 [**ID3D12Device：： CreateHeap**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createheap)所建立的堆積運作。</span><span class="sxs-lookup"><span data-stu-id="ed5d5-133">Cross-adapter sharing works with heaps created by calling [**ID3D12Device::CreateHeap**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createheap).</span></span> <span data-ttu-id="ed5d5-134">然後，應用程式可以透過 [**CreatePlacedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createplacedresource)來建立資源。</span><span class="sxs-lookup"><span data-stu-id="ed5d5-134">Applications can then create resources via [**CreatePlacedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createplacedresource).</span></span> <span data-ttu-id="ed5d5-135">[**CreateCommittedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource)所建立的資源/堆積也會允許此功能，但只有資料列主要 D3D12 \_ 資源 \_ 維度 \_ TEXTURE2D 資源， (參閱 [**D3D12 \_ 資源 \_ 維度**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_dimension)) 。</span><span class="sxs-lookup"><span data-stu-id="ed5d5-135">It is also allowed by resources/heaps created by [**CreateCommittedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource) but only for row-major D3D12\_RESOURCE\_DIMENSION\_TEXTURE2D resources (refer to [**D3D12\_RESOURCE\_DIMENSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_dimension)).</span></span> <span data-ttu-id="ed5d5-136">跨介面卡共用無法與 [**CreateReservedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createreservedresource)搭配使用。</span><span class="sxs-lookup"><span data-stu-id="ed5d5-136">Cross-adapter sharing does not work with [**CreateReservedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createreservedresource).</span></span>

<span data-ttu-id="ed5d5-137">針對跨介面卡共用，所有一般的跨佇列資源分享規則仍然適用。</span><span class="sxs-lookup"><span data-stu-id="ed5d5-137">For cross-adapter sharing, all of the usual cross-queue resource sharing rules still apply.</span></span> <span data-ttu-id="ed5d5-138">應用程式必須發出適當的阻礙，以確保這兩張介面卡之間有適當的同步處理和連貫性。</span><span class="sxs-lookup"><span data-stu-id="ed5d5-138">Applications must issue the appropriate barriers to ensure proper synchronization and coherence between the two adapters.</span></span> <span data-ttu-id="ed5d5-139">應用程式應該使用跨介面卡的圍牆來協調提交給多個介面卡的命令清單排程。</span><span class="sxs-lookup"><span data-stu-id="ed5d5-139">Applications should use cross-adapter fences to coordinate the scheduling of command lists submitted to multiple adapters.</span></span> <span data-ttu-id="ed5d5-140">沒有任何機制可跨 D3D API 版本共用跨介面卡資源。</span><span class="sxs-lookup"><span data-stu-id="ed5d5-140">There is no mechanism to share cross-adapter resources across D3D API versions.</span></span> <span data-ttu-id="ed5d5-141">只有系統記憶體支援跨介面卡共用資源。</span><span class="sxs-lookup"><span data-stu-id="ed5d5-141">Cross-adapter shared resources are only supported in system memory.</span></span> <span data-ttu-id="ed5d5-142">D3D12 \_ 堆積 \_ 型別預設堆積 \_ 和 D3D12 \_ 堆積類型自訂堆積 (使用 L0 記憶體集區時，支援跨介面卡共用堆積/資源 \_ \_ ，) 的寫入合併 CPU 頁面屬性。</span><span class="sxs-lookup"><span data-stu-id="ed5d5-142">Cross-adapter shared heaps/resources are supported in D3D12\_HEAP\_TYPE\_DEFAULT heaps and D3D12\_HEAP\_TYPE\_CUSTOM heaps (with the L0 memory pool, and write-combine CPU page properties).</span></span> <span data-ttu-id="ed5d5-143">驅動程式必須確定跨介面卡共用堆積的 GPU 讀取/寫入作業與系統上的其他 Gpu 一致。</span><span class="sxs-lookup"><span data-stu-id="ed5d5-143">Drivers must be sure that GPU read/write operations to cross-adapter shared heaps are coherent with other GPUs on the system.</span></span> <span data-ttu-id="ed5d5-144">例如，驅動程式可能需要將堆積資料排除在 GPU 快取中，而當 CPU 無法直接存取堆積資料時，通常不需要清除這些資料。</span><span class="sxs-lookup"><span data-stu-id="ed5d5-144">For example, the driver may need to exclude the heap data from residing in GPU caches that typically don’t need to be flushed when the CPU cannot directly access the heap data.</span></span>

<span data-ttu-id="ed5d5-145">應用程式應該限制只有在需要所提供功能的情況下，才會使用跨介面卡堆積。</span><span class="sxs-lookup"><span data-stu-id="ed5d5-145">Applications should confine the usage of cross adapter heaps to only those scenarios which require the functionality they provide.</span></span> <span data-ttu-id="ed5d5-146">跨介面卡堆積位於 D3D12 \_ MEMORY \_ POOL L0 中 \_ ，這不一定是 [**GetCustomHeapProperties**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcustomheapproperties) 所建議的。</span><span class="sxs-lookup"><span data-stu-id="ed5d5-146">Cross-adapter heaps are located in D3D12\_MEMORY\_POOL\_L0, which is not always what [**GetCustomHeapProperties**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcustomheapproperties) suggests.</span></span> <span data-ttu-id="ed5d5-147">針對離散/NUMA 介面卡架構，該記憶體集區的效率不高。</span><span class="sxs-lookup"><span data-stu-id="ed5d5-147">That memory pool is not efficient for discrete/ NUMA adapter architectures.</span></span> <span data-ttu-id="ed5d5-148">而且，最有效率的材質版面配置不一定都可以使用。</span><span class="sxs-lookup"><span data-stu-id="ed5d5-148">And, the most efficient texture layouts are not always available.</span></span>

<span data-ttu-id="ed5d5-149">同時適用下列限制：</span><span class="sxs-lookup"><span data-stu-id="ed5d5-149">The following limitations also apply:</span></span>

-   <span data-ttu-id="ed5d5-150">堆積層的相關堆積旗標必須是 D3D12 \_ 堆積旗標，才能 \_ \_ 允許 \_ 所有 \_ 緩衝區 \_ 和 \_ 紋理。</span><span class="sxs-lookup"><span data-stu-id="ed5d5-150">The heap flags related to heap tiers must be D3D12\_HEAP\_FLAG\_ALLOW\_ALL\_BUFFERS\_AND\_TEXTURES.</span></span>
-   <span data-ttu-id="ed5d5-151">您 \_ \_ \_ 也必須設定共用的 D3D12 堆積旗標。</span><span class="sxs-lookup"><span data-stu-id="ed5d5-151">D3D12\_HEAP\_FLAG\_SHARED must also be set.</span></span>
-   <span data-ttu-id="ed5d5-152">您必須 \_ 設定 D3D12 堆積 \_ 類型 \_ 的預設值，或 D3D12 \_ \_ \_ 無法使用的 D3D12 記憶體集區 \_ \_ \_ L0 和 D3D12 \_ CPU \_ 頁面 \_ 屬性 \_ \_ 的自訂堆積類型。</span><span class="sxs-lookup"><span data-stu-id="ed5d5-152">Either D3D12\_HEAP\_TYPE\_DEFAULT must be set or D3D12\_HEAP\_TYPE\_CUSTOM with D3D12\_MEMORY\_POOL\_L0 and D3D12\_CPU\_PAGE\_PROPERTY\_NOT\_AVAILABLE must be set.</span></span>
-   <span data-ttu-id="ed5d5-153">只有具有 D3D12 資源旗標的資源 \_ \_ ，才能 \_ \_ \_ 在跨介面卡堆積上放置。</span><span class="sxs-lookup"><span data-stu-id="ed5d5-153">Only resources with D3D12\_RESOURCE\_FLAG\_ALLOW\_CROSS\_ADAPTER may be placed on cross-adapter heaps.</span></span>

<span data-ttu-id="ed5d5-154">如需使用多個介面卡的詳細資訊，請參閱 [多介面卡系統](multi-engine.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="ed5d5-154">For more information on using multiple adapters, refer to the [Multi-adapter systems](multi-engine.md) section.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ed5d5-155">相關主題</span><span class="sxs-lookup"><span data-stu-id="ed5d5-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed5d5-156">堆積中的子分配</span><span class="sxs-lookup"><span data-stu-id="ed5d5-156">Suballocation Within Heaps</span></span>](suballocation-within-heaps.md)
</dt> </dl>

 

 




