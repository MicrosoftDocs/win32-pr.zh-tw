---
title: 在 Direct3D 12 中使用資源阻礙來同步處理資源狀態
description: 為了降低整體 CPU 使用率並啟用驅動程式多執行緒處理和預先處理，Direct3D 12 會將每個資源狀態管理的責任從圖形驅動程式移至應用程式。
ms.assetid: 3AB3BF34-433C-400B-921A-55B23CCDA44F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c766f18e85ab8acc2ed0afad8e680d566a723a68
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104548453"
---
# <a name="using-resource-barriers-to-synchronize-resource-states-in-direct3d-12"></a><span data-ttu-id="bd009-103">在 Direct3D 12 中使用資源阻礙來同步處理資源狀態</span><span class="sxs-lookup"><span data-stu-id="bd009-103">Using Resource Barriers to Synchronize Resource States in Direct3D 12</span></span>

<span data-ttu-id="bd009-104">為了降低整體 CPU 使用率並啟用驅動程式多執行緒處理和預先處理，Direct3D 12 會將每個資源狀態管理的責任從圖形驅動程式移至應用程式。</span><span class="sxs-lookup"><span data-stu-id="bd009-104">To reduce overall CPU usage and enable driver multi-threading and pre-processing, Direct3D 12 moves the responsibility of per-resource state management from the graphics driver to the application.</span></span> <span data-ttu-id="bd009-105">每個資源狀態的範例，是目前是否正在透過著色器資源檢視或轉譯目標視圖來存取材質資源。</span><span class="sxs-lookup"><span data-stu-id="bd009-105">An example of per-resource state is whether a texture resource is currently being accessed as through a Shader Resource View or as a Render Target View.</span></span> <span data-ttu-id="bd009-106">在 Direct3D 11 中，需要有驅動程式，才能在背景中追蹤此狀態。</span><span class="sxs-lookup"><span data-stu-id="bd009-106">In Direct3D 11, drivers were required to track this state in the background.</span></span> <span data-ttu-id="bd009-107">從 CPU 的角度來看，這是很耗費資源的，而且會大幅使多執行緒的設計變得更複雜。</span><span class="sxs-lookup"><span data-stu-id="bd009-107">This is expensive from a CPU perspective and significantly complicates any sort of multi-threaded design.</span></span> <span data-ttu-id="bd009-108">在 Microsoft Direct3D 12 中，大部分的每個資源狀態都是由應用程式使用單一 API （ [**ID3D12GraphicsCommandList：： ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)）來管理。</span><span class="sxs-lookup"><span data-stu-id="bd009-108">In Microsoft Direct3D 12, most per-resource state is managed by the application with a single API, [**ID3D12GraphicsCommandList::ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).</span></span>

-   [<span data-ttu-id="bd009-109">使用 ResourceBarrier API 來管理每個資源的狀態</span><span class="sxs-lookup"><span data-stu-id="bd009-109">Using the ResourceBarrier API to manage per-resource state</span></span>](#using-the-resourcebarrier-api-to-manage-per-resource-state)
    -   [<span data-ttu-id="bd009-110">資源狀態</span><span class="sxs-lookup"><span data-stu-id="bd009-110">Resource states</span></span>](#using-resource-barriers-to-synchronize-resource-states-in-direct3d-12)
    -   [<span data-ttu-id="bd009-111">資源的初始狀態</span><span class="sxs-lookup"><span data-stu-id="bd009-111">Initial states for resources</span></span>](#initial-states-for-resources)
    -   [<span data-ttu-id="bd009-112">讀取/寫入資源狀態限制</span><span class="sxs-lookup"><span data-stu-id="bd009-112">Read/write resource state restrictions</span></span>](#readwrite-resource-state-restrictions)
    -   [<span data-ttu-id="bd009-113">用來呈現回緩衝區的資源狀態</span><span class="sxs-lookup"><span data-stu-id="bd009-113">Resource states for presenting back buffers</span></span>](#resource-states-for-presenting-back-buffers)
    -   [<span data-ttu-id="bd009-114">捨棄資源</span><span class="sxs-lookup"><span data-stu-id="bd009-114">Discarding resources</span></span>](#discarding-resources)
-   [<span data-ttu-id="bd009-115">隱含狀態轉換</span><span class="sxs-lookup"><span data-stu-id="bd009-115">Implicit State Transitions</span></span>](#implicit-state-transitions)
    -   [<span data-ttu-id="bd009-116">一般狀態提升</span><span class="sxs-lookup"><span data-stu-id="bd009-116">Common state promotion</span></span>](#common-state-promotion)
    -   [<span data-ttu-id="bd009-117">狀態衰減至一般</span><span class="sxs-lookup"><span data-stu-id="bd009-117">State decay to common</span></span>](#state-decay-to-common)
    -   [<span data-ttu-id="bd009-118">效能影響</span><span class="sxs-lookup"><span data-stu-id="bd009-118">Performance implications</span></span>](#performance-implications)
-   [<span data-ttu-id="bd009-119">分割阻礙</span><span class="sxs-lookup"><span data-stu-id="bd009-119">Split Barriers</span></span>](#split-barriers)
-   [<span data-ttu-id="bd009-120">資源屏障範例案例</span><span class="sxs-lookup"><span data-stu-id="bd009-120">Resource barrier example scenario</span></span>](#resource-barrier-example-scenario)
-   [<span data-ttu-id="bd009-121">一般狀態提升和衰減範例</span><span class="sxs-lookup"><span data-stu-id="bd009-121">Common state promotion and decay sample</span></span>](#common-state-promotion-and-decay-sample)
-   [<span data-ttu-id="bd009-122">分割障礙的範例</span><span class="sxs-lookup"><span data-stu-id="bd009-122">Example of split barriers</span></span>](#example-of-split-barriers)
-   [<span data-ttu-id="bd009-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="bd009-123">Related topics</span></span>](#related-topics)

## <a name="using-the-resourcebarrier-api-to-manage-per-resource-state"></a><span data-ttu-id="bd009-124">使用 ResourceBarrier API 來管理每個資源的狀態</span><span class="sxs-lookup"><span data-stu-id="bd009-124">Using the ResourceBarrier API to manage per-resource state</span></span>

<span data-ttu-id="bd009-125">[**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) 會通知圖形驅動程式，其中驅動程式可能需要將多個存取與儲存資源的記憶體進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="bd009-125">[**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) notifies the graphics driver of situations in which the driver may need to synchronize multiple accesses to the memory in which a resource is stored.</span></span> <span data-ttu-id="bd009-126">呼叫方法時，會使用一或多個資源關卡描述結構，指出所宣告的資源屏障類型。</span><span class="sxs-lookup"><span data-stu-id="bd009-126">The method is called with one or more resource barrier description structures indicating the type of resource barrier being declared.</span></span>

<span data-ttu-id="bd009-127">有三種類型的資源阻礙：</span><span class="sxs-lookup"><span data-stu-id="bd009-127">There are three types of resource barriers:</span></span>

-   <span data-ttu-id="bd009-128">**轉換屏障** -轉換屏障指出不同使用方式之間的一組子資源轉換。</span><span class="sxs-lookup"><span data-stu-id="bd009-128">**Transition barrier** - A transition barrier indicates that a set of subresources transition between different usages.</span></span> <span data-ttu-id="bd009-129">[**D3D12 \_ 資源 \_ 轉換 \_ 屏障**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier)結構是用來指定正在轉換的 subresource，以及 subresource *之前* 和 *之後* 的狀態。</span><span class="sxs-lookup"><span data-stu-id="bd009-129">A [**D3D12\_RESOURCE\_TRANSITION\_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier) structure is used to specify the subresource that is transitioning as well as the *before* and *after* states of the subresource.</span></span>

    <span data-ttu-id="bd009-130">系統會確認命令清單中的 subresource 轉換與先前的轉換在相同的命令清單中是一致的。</span><span class="sxs-lookup"><span data-stu-id="bd009-130">The system verifies that subresource transitions in a command list are consistent with previous transitions in the same command list.</span></span> <span data-ttu-id="bd009-131">Debug 層會進一步追蹤 subresource 狀態以找出其他錯誤，不過這項驗證很保守且不詳盡。</span><span class="sxs-lookup"><span data-stu-id="bd009-131">The debug layer further tracks subresource state to find other errors however this validation is conservative and not exhaustive.</span></span>

    <span data-ttu-id="bd009-132">請注意，您可以使用 D3D12 \_ 資源 \_ 關卡 \_ 所有 \_ 子資源旗標，指定要轉換資源內的所有子資源。</span><span class="sxs-lookup"><span data-stu-id="bd009-132">Note that you can use the D3D12\_RESOURCE\_BARRIER\_ALL\_SUBRESOURCES flag to specify that all subresources within a resource are being transitioned.</span></span>

-   <span data-ttu-id="bd009-133">**別名屏障** -別名屏障表示兩個不同資源的使用方式之間的轉換，這些資源在相同堆積中有重迭的對應。</span><span class="sxs-lookup"><span data-stu-id="bd009-133">**Aliasing barrier** - An aliasing barrier indicates a transition between usages of two different resources which have overlapping mappings into the same heap.</span></span> <span data-ttu-id="bd009-134">這同時適用于保留和放置的資源。</span><span class="sxs-lookup"><span data-stu-id="bd009-134">This applies to both reserved and placed resources.</span></span> <span data-ttu-id="bd009-135">[**D3D12 \_ 資源 \_ 別名 \_ 屏障**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_aliasing_barrier)結構是用來同時指定資源和 *之後\*\*資源。*</span><span class="sxs-lookup"><span data-stu-id="bd009-135">A [**D3D12\_RESOURCE\_ALIASING\_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_aliasing_barrier) structure is used to specify both the *before* resource and the *after* resource.</span></span>

    <span data-ttu-id="bd009-136">請注意，其中一個或兩個資源可以是 Null，這表示任何已並排顯示的資源可能會造成別名。</span><span class="sxs-lookup"><span data-stu-id="bd009-136">Note that one or both resources can be NULL, which indicates that any tiled resource could cause aliasing.</span></span> <span data-ttu-id="bd009-137">如需使用並排顯示資源的詳細資訊， [請參閱並排顯示的資源和](../direct3d11/tiled-resources.md) 磁片區並排顯示的 [資源](volume-tiled-resources.md)。</span><span class="sxs-lookup"><span data-stu-id="bd009-137">For more information about using tiled resources, see [Tiled resources](../direct3d11/tiled-resources.md) and [Volume Tiled Resources](volume-tiled-resources.md).</span></span>

-   <span data-ttu-id="bd009-138">未 **排序的存取視圖 (UAV) 屏障**-UAV 屏障指出任何未來的 UAV 存取（讀取或寫入）之間的所有 UAV 存取（讀取或寫入）都必須完成。</span><span class="sxs-lookup"><span data-stu-id="bd009-138">**Unordered access view (UAV) barrier** - A UAV barrier indicates that all UAV accesses, both read or write, to a particular resource must complete between any future UAV accesses, both read or write.</span></span> <span data-ttu-id="bd009-139">應用程式不需要在唯讀取 UAV 的兩個繪製或分派呼叫之間放置 UAV 關卡。</span><span class="sxs-lookup"><span data-stu-id="bd009-139">It's not necessary for an app to put a UAV barrier between two draw or dispatch calls that only read from a UAV.</span></span> <span data-ttu-id="bd009-140">此外，如果應用程式知道可以安全地以任何循序執行 UAV 存取，就不需要在兩個繪製或分派呼叫之間放置 UAV 關卡，以寫入相同的 UAV。</span><span class="sxs-lookup"><span data-stu-id="bd009-140">Also, it's not necessary to put a UAV barrier between two draw or dispatch calls that write to the same UAV if the application knows that it is safe to execute the UAV access in any order.</span></span> <span data-ttu-id="bd009-141">[**D3D12 \_ 資源 \_ UAV \_ 屏障**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_uav_barrier)結構是用來指定要套用關卡的 UAV 資源。</span><span class="sxs-lookup"><span data-stu-id="bd009-141">A [**D3D12\_RESOURCE\_UAV\_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_uav_barrier) structure is used to specify the UAV resource to which the barrier applies.</span></span> <span data-ttu-id="bd009-142">應用程式可以針對關卡的 UAV 指定 Null，這表示任何 UAV 存取都可能需要關卡。</span><span class="sxs-lookup"><span data-stu-id="bd009-142">The application can specify NULL for the barrier's UAV, which indicates that any UAV access could require the barrier.</span></span>

<span data-ttu-id="bd009-143">使用資源屏障描述的陣列來呼叫 [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) 時，API 的行為就像是針對每個專案呼叫一次一樣，依照提供的順序。</span><span class="sxs-lookup"><span data-stu-id="bd009-143">When [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) is called with an array of resource barrier descriptions, the API behaves as if it was called once for each element, in the order in which they were supplied.</span></span>

<span data-ttu-id="bd009-144">在任何指定的時間，subresource 都只會在一種狀態中，取決於提供給 [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)的一組 [**D3D12 \_ 資源 \_ 狀態**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states)旗標。</span><span class="sxs-lookup"><span data-stu-id="bd009-144">At any given time, a subresource is in exactly one state, determined by the set of [**D3D12\_RESOURCE\_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) flags supplied to [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).</span></span> <span data-ttu-id="bd009-145">應用程式必須確定連續呼叫 **ResourceBarrier** 的 *前後\*\*狀態同意*。</span><span class="sxs-lookup"><span data-stu-id="bd009-145">The application must ensure that the *before* and *after* states of consecutive calls to **ResourceBarrier** agree.</span></span>

> [!TIP]
>
> <span data-ttu-id="bd009-146">應用程式應該盡可能將多個轉換批次處理成一個 API 呼叫。</span><span class="sxs-lookup"><span data-stu-id="bd009-146">Applications should batch multiple transitions into one API call wherever possible.</span></span>

 

### <a name="resource-states"></a><span data-ttu-id="bd009-147">資源狀態</span><span class="sxs-lookup"><span data-stu-id="bd009-147">Resource states</span></span>

<span data-ttu-id="bd009-148">如需資源可在其之間轉換的資源狀態完整清單，請參閱 [**D3D12 \_ 資源 \_ 狀態**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) 列舉的參考主題。</span><span class="sxs-lookup"><span data-stu-id="bd009-148">For the complete list of resource states that a resource can transition between, see the reference topic for the [**D3D12\_RESOURCE\_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) enumeration.</span></span>

<span data-ttu-id="bd009-149">針對分割資源阻礙，也請參閱 [**D3D12 \_ 資源 \_ 屏障 \_ 旗標**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags)。</span><span class="sxs-lookup"><span data-stu-id="bd009-149">For split resource barriers, also refer to [**D3D12\_RESOURCE\_BARRIER\_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags).</span></span>

### <a name="initial-states-for-resources"></a><span data-ttu-id="bd009-150">資源的初始狀態</span><span class="sxs-lookup"><span data-stu-id="bd009-150">Initial states for resources</span></span>

<span data-ttu-id="bd009-151">您可以使用任何使用者指定的初始狀態來建立資源 (適用于資源描述) ，但有下列例外狀況：</span><span class="sxs-lookup"><span data-stu-id="bd009-151">Resources may be created with any user-specified initial state (valid for the resource description), with the following exceptions:</span></span>

-   <span data-ttu-id="bd009-152">上傳堆積必須在狀態 D3D12 \_ 資源 \_ 狀態一般讀取中開始， \_ \_ 它是的位 or 組合：</span><span class="sxs-lookup"><span data-stu-id="bd009-152">Upload heaps must start out in the state D3D12\_RESOURCE\_STATE\_GENERIC\_READ which is a bitwise OR combination of:</span></span>
    -   <span data-ttu-id="bd009-153">D3D12 \_ 資源 \_ 狀態 \_ 頂點 \_ 和 \_ 常數 \_ 緩衝區</span><span class="sxs-lookup"><span data-stu-id="bd009-153">D3D12\_RESOURCE\_STATE\_VERTEX\_AND\_CONSTANT\_BUFFER</span></span>
    -   <span data-ttu-id="bd009-154">D3D12 \_ 資源 \_ 狀態 \_ 索引 \_ 緩衝區</span><span class="sxs-lookup"><span data-stu-id="bd009-154">D3D12\_RESOURCE\_STATE\_INDEX\_BUFFER</span></span>
    -   <span data-ttu-id="bd009-155">D3D12 \_ 資源 \_ 狀態 \_ 複製 \_ 來源</span><span class="sxs-lookup"><span data-stu-id="bd009-155">D3D12\_RESOURCE\_STATE\_COPY\_SOURCE</span></span>
    -   <span data-ttu-id="bd009-156">D3D12 \_ 資源 \_ 狀態 \_ 非 \_ 圖元 \_ 著色器 \_ 資源</span><span class="sxs-lookup"><span data-stu-id="bd009-156">D3D12\_RESOURCE\_STATE\_NON\_PIXEL\_SHADER\_RESOURCE</span></span>
    -   <span data-ttu-id="bd009-157">D3D12 \_ 資源 \_ 狀態 \_ 圖元 \_ 著色器 \_ 資源</span><span class="sxs-lookup"><span data-stu-id="bd009-157">D3D12\_RESOURCE\_STATE\_PIXEL\_SHADER\_RESOURCE</span></span>
    -   <span data-ttu-id="bd009-158">D3D12 \_ 資源 \_ 狀態 \_ 間接 \_ 引數</span><span class="sxs-lookup"><span data-stu-id="bd009-158">D3D12\_RESOURCE\_STATE\_INDIRECT\_ARGUMENT</span></span>
-   <span data-ttu-id="bd009-159">Readback 堆積必須以 D3D12 \_ 資源 \_ 狀態 \_ 複製 \_ 目的地狀態開始。</span><span class="sxs-lookup"><span data-stu-id="bd009-159">Readback heaps must start out in the D3D12\_RESOURCE\_STATE\_COPY\_DEST state.</span></span>
-   <span data-ttu-id="bd009-160">交換鏈回緩衝區會自動以 D3D12 \_ 資源狀態的 \_ \_ 常見狀態開始。</span><span class="sxs-lookup"><span data-stu-id="bd009-160">Swap chain back buffers automatically start out in the D3D12\_RESOURCE\_STATE\_COMMON state.</span></span>

<span data-ttu-id="bd009-161">在堆積可以成為 GPU 複製作業的目標之前，通常必須先將堆積轉換成 D3D12 \_ 資源 \_ 狀態 \_ 複製 \_ 目的地狀態。</span><span class="sxs-lookup"><span data-stu-id="bd009-161">Before a heap can be the target of a GPU copy operation, normally the heap must first be transitioned to the D3D12\_RESOURCE\_STATE\_COPY\_DEST state.</span></span> <span data-ttu-id="bd009-162">不過，在上傳堆積上建立的資源必須以開始，而且無法從一般 \_ 讀取狀態變更，因為只有 CPU 會進行寫入。</span><span class="sxs-lookup"><span data-stu-id="bd009-162">However, resources created on UPLOAD heaps must start in and cannot change from the GENERIC\_READ state since only the CPU will be doing writing.</span></span> <span data-ttu-id="bd009-163">相反地，在 READBACK 堆積中建立的認可資源必須在中開始，而且無法從複製 \_ 目的地狀態變更。</span><span class="sxs-lookup"><span data-stu-id="bd009-163">Conversely, committed resources created in READBACK heaps must start in and cannot change from the COPY\_DEST state.</span></span>

### <a name="readwrite-resource-state-restrictions"></a><span data-ttu-id="bd009-164">讀取/寫入資源狀態限制</span><span class="sxs-lookup"><span data-stu-id="bd009-164">Read/write resource state restrictions</span></span>

<span data-ttu-id="bd009-165">用來描述資源狀態的資源狀態使用位會分成隻讀和讀取/寫入狀態。</span><span class="sxs-lookup"><span data-stu-id="bd009-165">The resource state usage bits that are used to describe a resource state are divided into read-only and read/write states.</span></span> <span data-ttu-id="bd009-166">[**D3D12 \_ 資源 \_ 狀態**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states)的參考主題指出列舉中每個位的讀取/寫入存取層級。</span><span class="sxs-lookup"><span data-stu-id="bd009-166">The reference topic for the [**D3D12\_RESOURCE\_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) indicates the read/write access level for each bit in the enumeration.</span></span>

<span data-ttu-id="bd009-167">最多隻能為任何資源設定一個讀取/寫入位。</span><span class="sxs-lookup"><span data-stu-id="bd009-167">At most, only one read/write bit can be set for any resource.</span></span> <span data-ttu-id="bd009-168">如果已設定寫入位，則可能不會針對該資源設定唯讀位。</span><span class="sxs-lookup"><span data-stu-id="bd009-168">If a write bit is set, then no read-only bit may be set for that resource.</span></span> <span data-ttu-id="bd009-169">如果未設定寫入位，則可能會設定任何數目的讀取位。</span><span class="sxs-lookup"><span data-stu-id="bd009-169">If no write bit is set, then any number of read bits may be set.</span></span>

### <a name="resource-states-for-presenting-back-buffers"></a><span data-ttu-id="bd009-170">用來呈現回緩衝區的資源狀態</span><span class="sxs-lookup"><span data-stu-id="bd009-170">Resource states for presenting back buffers</span></span>

<span data-ttu-id="bd009-171">在顯示背景緩衝區之前，它必須處於 D3D12 \_ 資源 \_ 狀態的 \_ 一般狀態。</span><span class="sxs-lookup"><span data-stu-id="bd009-171">Before a back buffer is presented, it must be in the D3D12\_RESOURCE\_STATE\_COMMON state.</span></span> <span data-ttu-id="bd009-172">請注意，目前的資源狀態 D3D12 \_ 資源 \_ 狀態 \_ 是 D3D12 \_ 資源狀態的 \_ 同義字 \_ ，而且兩者的值都是0。</span><span class="sxs-lookup"><span data-stu-id="bd009-172">Note, the resource state D3D12\_RESOURCE\_STATE\_PRESENT is a synonym for D3D12\_RESOURCE\_STATE\_COMMON, and they both have a value of 0.</span></span> <span data-ttu-id="bd009-173">如果 [**IDXGISwapChain：:P**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present) 重新傳送 (或 [**IDXGISwapChain1：:P resent1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1)) 是在目前非此狀態的資源上呼叫，則會發出 debug layer 警告。</span><span class="sxs-lookup"><span data-stu-id="bd009-173">If [**IDXGISwapChain::Present**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present) (or [**IDXGISwapChain1::Present1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1)) is called on a resource that is not currently in this state, a debug layer warning is emitted.</span></span>

### <a name="discarding-resources"></a><span data-ttu-id="bd009-174">捨棄資源</span><span class="sxs-lookup"><span data-stu-id="bd009-174">Discarding resources</span></span>

<span data-ttu-id="bd009-175">資源中的所有子資源都必須分別在轉譯 \_ 目標/深度寫入狀態中，以轉譯目標/深度樣板資源，同時也會在 \_ 呼叫 [**ID3D12GraphicsCommandList：:D iscardresource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource) 。</span><span class="sxs-lookup"><span data-stu-id="bd009-175">All subresources in a resource must be in the RENDER\_TARGET state, or DEPTH\_WRITE state, for render targets/depth-stencil resources respectively, when [**ID3D12GraphicsCommandList::DiscardResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource) is called.</span></span>

## <a name="implicit-state-transitions"></a><span data-ttu-id="bd009-176">隱含狀態轉換</span><span class="sxs-lookup"><span data-stu-id="bd009-176">Implicit State Transitions</span></span>

<span data-ttu-id="bd009-177">資源只能「升級」超出 D3D12 的 \_ 資源 \_ 狀態 \_ 。</span><span class="sxs-lookup"><span data-stu-id="bd009-177">Resources can only be "promoted" out of D3D12\_RESOURCE\_STATE\_COMMON.</span></span> <span data-ttu-id="bd009-178">同樣地，資源只會「衰減」以 D3D12 \_ 資源 \_ 狀態 \_ 。</span><span class="sxs-lookup"><span data-stu-id="bd009-178">Similarly, resources will only "decay" to D3D12\_RESOURCE\_STATE\_COMMON.</span></span>

### <a name="common-state-promotion"></a><span data-ttu-id="bd009-179">一般狀態提升</span><span class="sxs-lookup"><span data-stu-id="bd009-179">Common state promotion</span></span>

<span data-ttu-id="bd009-180">所有緩衝區資源以及具有 D3D12 資源旗標的 \_ 材質 \_ \_ ，都可讓您 \_ \_ \_ \_ \_ 在第一次 GPU 存取時，以隱含的方式從 D3D12 資源狀態（包括一般 \_ 讀取來涵蓋任何讀取案例），將同時存取旗標設定為隱含地升級為相關狀態。</span><span class="sxs-lookup"><span data-stu-id="bd009-180">All buffer resources as well as textures with the D3D12\_RESOURCE\_FLAG\_ALLOW\_SIMULTANEOUS\_ACCESS flag set are implicitly promoted from D3D12\_RESOURCE\_STATE\_COMMON to the relevant state on first GPU access, including GENERIC\_READ to cover any read scenario.</span></span> <span data-ttu-id="bd009-181">任何處于一般狀態的資源都可以透過其在單一狀態中進行存取，</span><span class="sxs-lookup"><span data-stu-id="bd009-181">Any resource in the COMMON state can be accessed as through it were in a single state with</span></span>

<dl> <span data-ttu-id="bd009-182">1寫入旗標，或</span><span class="sxs-lookup"><span data-stu-id="bd009-182">1 WRITE flag, or</span></span>  
<span data-ttu-id="bd009-183">1或多個讀取旗標</span><span class="sxs-lookup"><span data-stu-id="bd009-183">1 or more READ flags</span></span>  
</dl>

<span data-ttu-id="bd009-184">您可以根據下表，從一般狀態升級資源：</span><span class="sxs-lookup"><span data-stu-id="bd009-184">Resources can be promoted from the COMMON state based on the following table:</span></span>



| <span data-ttu-id="bd009-185">狀態旗標</span><span class="sxs-lookup"><span data-stu-id="bd009-185">State flag</span></span>                    | <span data-ttu-id="bd009-186">可提升狀態</span><span class="sxs-lookup"><span data-stu-id="bd009-186">Promotable State</span></span>                             |                                      |
|-------------------------------|----------------------------------------------|--------------------------------------|
|                               | <span data-ttu-id="bd009-187">**緩衝區和 Simultaneous-Access 紋理**</span><span class="sxs-lookup"><span data-stu-id="bd009-187">**Buffers and Simultaneous-Access Textures**</span></span> | <span data-ttu-id="bd009-188">**非同時存取的材質**</span><span class="sxs-lookup"><span data-stu-id="bd009-188">**Non-Simultaneous-Access Textures**</span></span> |
| <span data-ttu-id="bd009-189">頂點 \_ 和 \_ 常數 \_ 緩衝區</span><span class="sxs-lookup"><span data-stu-id="bd009-189">VERTEX\_AND\_CONSTANT\_BUFFER</span></span> | <span data-ttu-id="bd009-190">是</span><span class="sxs-lookup"><span data-stu-id="bd009-190">Yes</span></span>                                          | <span data-ttu-id="bd009-191">否</span><span class="sxs-lookup"><span data-stu-id="bd009-191">No</span></span>                                   |
| <span data-ttu-id="bd009-192">索引 \_ 緩衝區</span><span class="sxs-lookup"><span data-stu-id="bd009-192">INDEX\_BUFFER</span></span>                 | <span data-ttu-id="bd009-193">是</span><span class="sxs-lookup"><span data-stu-id="bd009-193">Yes</span></span>                                          | <span data-ttu-id="bd009-194">否</span><span class="sxs-lookup"><span data-stu-id="bd009-194">No</span></span>                                   |
| <span data-ttu-id="bd009-195">呈現 \_ 目標</span><span class="sxs-lookup"><span data-stu-id="bd009-195">RENDER\_TARGET</span></span>                | <span data-ttu-id="bd009-196">是</span><span class="sxs-lookup"><span data-stu-id="bd009-196">Yes</span></span>                                          | <span data-ttu-id="bd009-197">否</span><span class="sxs-lookup"><span data-stu-id="bd009-197">No</span></span>                                   |
| <span data-ttu-id="bd009-198">未排序的 \_ 存取</span><span class="sxs-lookup"><span data-stu-id="bd009-198">UNORDERED\_ACCESS</span></span>             | <span data-ttu-id="bd009-199">是</span><span class="sxs-lookup"><span data-stu-id="bd009-199">Yes</span></span>                                          | <span data-ttu-id="bd009-200">否</span><span class="sxs-lookup"><span data-stu-id="bd009-200">No</span></span>                                   |
| <span data-ttu-id="bd009-201">深度 \_ 寫入</span><span class="sxs-lookup"><span data-stu-id="bd009-201">DEPTH\_WRITE</span></span>                  | <span data-ttu-id="bd009-202">不<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="bd009-202">No<sup>\*</sup></span></span>                              | <span data-ttu-id="bd009-203">No</span><span class="sxs-lookup"><span data-stu-id="bd009-203">No</span></span>                                   |
| <span data-ttu-id="bd009-204">深度 \_ 讀取</span><span class="sxs-lookup"><span data-stu-id="bd009-204">DEPTH\_READ</span></span>                   | <span data-ttu-id="bd009-205">不<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="bd009-205">No<sup>\*</sup></span></span>                              | <span data-ttu-id="bd009-206">No</span><span class="sxs-lookup"><span data-stu-id="bd009-206">No</span></span>                                   |
| <span data-ttu-id="bd009-207">非 \_ 圖元 \_ 著色器 \_ 資源</span><span class="sxs-lookup"><span data-stu-id="bd009-207">NON\_PIXEL\_SHADER\_RESOURCE</span></span>  | <span data-ttu-id="bd009-208">是</span><span class="sxs-lookup"><span data-stu-id="bd009-208">Yes</span></span>                                          | <span data-ttu-id="bd009-209">是</span><span class="sxs-lookup"><span data-stu-id="bd009-209">Yes</span></span>                                  |
| <span data-ttu-id="bd009-210">圖元 \_ 著色器 \_ 資源</span><span class="sxs-lookup"><span data-stu-id="bd009-210">PIXEL\_SHADER\_RESOURCE</span></span>       | <span data-ttu-id="bd009-211">是</span><span class="sxs-lookup"><span data-stu-id="bd009-211">Yes</span></span>                                          | <span data-ttu-id="bd009-212">是</span><span class="sxs-lookup"><span data-stu-id="bd009-212">Yes</span></span>                                  |
| <span data-ttu-id="bd009-213">串流 \_ 輸出</span><span class="sxs-lookup"><span data-stu-id="bd009-213">STREAM\_OUT</span></span>                   | <span data-ttu-id="bd009-214">是</span><span class="sxs-lookup"><span data-stu-id="bd009-214">Yes</span></span>                                          | <span data-ttu-id="bd009-215">否</span><span class="sxs-lookup"><span data-stu-id="bd009-215">No</span></span>                                   |
| <span data-ttu-id="bd009-216">間接 \_ 引數</span><span class="sxs-lookup"><span data-stu-id="bd009-216">INDIRECT\_ARGUMENT</span></span>            | <span data-ttu-id="bd009-217">是</span><span class="sxs-lookup"><span data-stu-id="bd009-217">Yes</span></span>                                          | <span data-ttu-id="bd009-218">否</span><span class="sxs-lookup"><span data-stu-id="bd009-218">No</span></span>                                   |
| <span data-ttu-id="bd009-219">複製 \_ 目的地</span><span class="sxs-lookup"><span data-stu-id="bd009-219">COPY\_DEST</span></span>                    | <span data-ttu-id="bd009-220">是</span><span class="sxs-lookup"><span data-stu-id="bd009-220">Yes</span></span>                                          | <span data-ttu-id="bd009-221">是</span><span class="sxs-lookup"><span data-stu-id="bd009-221">Yes</span></span>                                  |
| <span data-ttu-id="bd009-222">複製 \_ 來源</span><span class="sxs-lookup"><span data-stu-id="bd009-222">COPY\_SOURCE</span></span>                  | <span data-ttu-id="bd009-223">是</span><span class="sxs-lookup"><span data-stu-id="bd009-223">Yes</span></span>                                          | <span data-ttu-id="bd009-224">是</span><span class="sxs-lookup"><span data-stu-id="bd009-224">Yes</span></span>                                  |
| <span data-ttu-id="bd009-225">解析 \_ 目的地</span><span class="sxs-lookup"><span data-stu-id="bd009-225">RESOLVE\_DEST</span></span>                 | <span data-ttu-id="bd009-226">是</span><span class="sxs-lookup"><span data-stu-id="bd009-226">Yes</span></span>                                          | <span data-ttu-id="bd009-227">否</span><span class="sxs-lookup"><span data-stu-id="bd009-227">No</span></span>                                   |
| <span data-ttu-id="bd009-228">解析 \_ 來源</span><span class="sxs-lookup"><span data-stu-id="bd009-228">RESOLVE\_SOURCE</span></span>               | <span data-ttu-id="bd009-229">是</span><span class="sxs-lookup"><span data-stu-id="bd009-229">Yes</span></span>                                          | <span data-ttu-id="bd009-230">否</span><span class="sxs-lookup"><span data-stu-id="bd009-230">No</span></span>                                   |
| <span data-ttu-id="bd009-231">預測</span><span class="sxs-lookup"><span data-stu-id="bd009-231">PREDICATION</span></span>                   | <span data-ttu-id="bd009-232">是</span><span class="sxs-lookup"><span data-stu-id="bd009-232">Yes</span></span>                                          | <span data-ttu-id="bd009-233">否</span><span class="sxs-lookup"><span data-stu-id="bd009-233">No</span></span>                                   |



 

<span data-ttu-id="bd009-234"><sup>\*</sup>深度樣板資源必須是不可同時存取的材質，因此永遠不會隱含地升級。</span><span class="sxs-lookup"><span data-stu-id="bd009-234"><sup>\*</sup>Depth-stencil resources must be non-simultaneous-access textures and thus can never be implicitly promoted.</span></span>

<span data-ttu-id="bd009-235">當此存取進行時，升級的作用就像是隱含的資源屏障。</span><span class="sxs-lookup"><span data-stu-id="bd009-235">When this access occurs the promotion acts like an implicit resource barrier.</span></span> <span data-ttu-id="bd009-236">針對後續的存取，必要時，資源屏障將需要變更資源狀態。</span><span class="sxs-lookup"><span data-stu-id="bd009-236">For subsequent accesses, resource barriers will be required to change the resource state if necessary.</span></span> <span data-ttu-id="bd009-237">請注意，從一個已升級的讀取狀態升階為多個讀取狀態是有效的，但這不是寫入狀態的情況。</span><span class="sxs-lookup"><span data-stu-id="bd009-237">Note that promotion from one promoted read state into multiple read state is valid, but this is not the case for write states.</span></span>  
<span data-ttu-id="bd009-238">例如，如果在繪製呼叫中將共通狀態的資源升級為圖元 \_ 著色器 \_ 資源，它仍然可以升級為 NON_PIXEL \_ 著色器 \_ 資源 |\_ \_ 另一個繪製呼叫中的圖元著色器資源。</span><span class="sxs-lookup"><span data-stu-id="bd009-238">For example, if a resource in the common state is promoted to PIXEL\_SHADER\_RESOURCE in a Draw call, it can still be promoted to NON_PIXEL\_SHADER\_RESOURCE | PIXEL\_SHADER\_RESOURCE in another Draw call.</span></span> <span data-ttu-id="bd009-239">但是，如果在寫入作業（例如複製目的地）中使用它，則資源狀態轉換會從合併的已升級讀取狀態中阻礙，此處 NON_PIXEL \_ 著色器 \_ 資源 |\_ \_ 需要複製目的地的圖元著色器資源 \_ 。</span><span class="sxs-lookup"><span data-stu-id="bd009-239">However, if it is used in a write operation, such as a copy destination, a resource state transition barrier from the combined promoted read states, here NON_PIXEL\_SHADER\_RESOURCE | PIXEL\_SHADER\_RESOURCE, to COPY\_DEST is needed.</span></span>  
<span data-ttu-id="bd009-240">同樣地，如果從共通升級為複製 \_ 目的地，仍然需要關卡從複製目的地轉換 \_ 成轉譯 \_ 目標。</span><span class="sxs-lookup"><span data-stu-id="bd009-240">Similarly, if promoted from COMMON to COPY\_DEST, a barrier is still required to transition from COPY\_DEST to RENDER\_TARGET.</span></span>

<span data-ttu-id="bd009-241">請注意，一般狀態提升為「免費」，因為 GPU 不需要執行任何同步處理等候。</span><span class="sxs-lookup"><span data-stu-id="bd009-241">Note that common state promotion is "free" in that there is no need for the GPU to perform any synchronization waits.</span></span> <span data-ttu-id="bd009-242">此促銷代表一般狀態中的資源應該不需要額外的 GPU 工作或驅動程式追蹤來支援特定存取。</span><span class="sxs-lookup"><span data-stu-id="bd009-242">The promotion represents the fact that resources in the COMMON state should not require additional GPU work or driver tracking to support certain accesses.</span></span>

### <a name="state-decay-to-common"></a><span data-ttu-id="bd009-243">狀態衰減至一般</span><span class="sxs-lookup"><span data-stu-id="bd009-243">State decay to common</span></span>

<span data-ttu-id="bd009-244">一般狀態升級的翻轉端會衰減回 D3D12 的 \_ 資源 \_ 狀態 \_ 。</span><span class="sxs-lookup"><span data-stu-id="bd009-244">The flip-side of common state promotion is decay back to D3D12\_RESOURCE\_STATE\_COMMON.</span></span> <span data-ttu-id="bd009-245">符合特定需求的資源會被視為無狀態，而且在 GPU 完成執行 [**ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) 作業時，會有效地回到一般狀態。</span><span class="sxs-lookup"><span data-stu-id="bd009-245">Resources that meet certain requirements are considered to be stateless and effectively return to the common state when the GPU finishes execution of an [**ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) operation.</span></span> <span data-ttu-id="bd009-246">在相同的 **ExecuteCommandLists** 呼叫中一起執行的命令清單之間，不會發生衰減。</span><span class="sxs-lookup"><span data-stu-id="bd009-246">Decay does not occur between command lists executed together in the same **ExecuteCommandLists** call.</span></span>

<span data-ttu-id="bd009-247">當 GPU 上的 [**ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) 作業完成時，下列資源將會衰減：</span><span class="sxs-lookup"><span data-stu-id="bd009-247">The following resources will decay when an [**ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) operation is completed on the GPU:</span></span>

-   <span data-ttu-id="bd009-248">在複製佇列上存取的資源， *或*</span><span class="sxs-lookup"><span data-stu-id="bd009-248">Resources being accessed on a Copy queue, *or*</span></span>
-   <span data-ttu-id="bd009-249">任何佇列類型上的緩衝區資源， *或*</span><span class="sxs-lookup"><span data-stu-id="bd009-249">Buffer resources on any queue type, *or*</span></span>
-   <span data-ttu-id="bd009-250">具有 D3D12 資源旗標之任何佇列類型上的材質資源 \_ \_ \_ 允許 \_ 同時 \_ 存取旗標， *或*</span><span class="sxs-lookup"><span data-stu-id="bd009-250">Texture resources on any queue type that have the D3D12\_RESOURCE\_FLAG\_ALLOW\_SIMULTANEOUS\_ACCESS flag set, *or*</span></span>
-   <span data-ttu-id="bd009-251">任何以隱含方式升級為唯讀狀態的資源。</span><span class="sxs-lookup"><span data-stu-id="bd009-251">Any resource implicitly promoted to a read-only state.</span></span>

<span data-ttu-id="bd009-252">如同一般狀態升級，衰減是免費的，不需要額外的同步處理。</span><span class="sxs-lookup"><span data-stu-id="bd009-252">Like common state promotion, the decay is free in that no additional synchronization is needed.</span></span> <span data-ttu-id="bd009-253">結合一般狀態升階和衰減有助於消除許多不必要的 [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) 轉換。</span><span class="sxs-lookup"><span data-stu-id="bd009-253">Combining common state promotion and decay can help to eliminate many unnecessary [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) transitions.</span></span> <span data-ttu-id="bd009-254">在某些情況下，這可提供顯著的效能改進。</span><span class="sxs-lookup"><span data-stu-id="bd009-254">In some cases, this can provide significant performance improvements.</span></span>

<span data-ttu-id="bd009-255">緩衝區和 Simultaneous-Access 資源將會衰減至一般狀態，而不論它們是使用資源阻礙明確轉換或隱含地升級。</span><span class="sxs-lookup"><span data-stu-id="bd009-255">Buffers and Simultaneous-Access resources will decay to the common state regardless of whether they were explicitly transitioned using resource barriers or implicitly promoted.</span></span>

### <a name="performance-implications"></a><span data-ttu-id="bd009-256">效能影響</span><span class="sxs-lookup"><span data-stu-id="bd009-256">Performance implications</span></span>

<span data-ttu-id="bd009-257">在一般狀態的資源上記錄明確的 [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)轉換時，請正確地使用 D3D12 \_ 資源 \_ 狀態 \_ 一般或任何可提升狀態，作為 D3D12 資源 \_ \_ 轉換屏障結構中的 BeforeState 值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="bd009-257">When recording explicit [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) transitions on resources in the common state, it is correct to use either D3D12\_RESOURCE\_STATE\_COMMON or any promotable state as the *BeforeState* value in the D3D12\_RESOURCE\_TRANSITION\_BARRIER structure.</span></span> <span data-ttu-id="bd009-258">這可讓傳統的狀態管理忽略自動衰減的緩衝區和同時存取的材質。</span><span class="sxs-lookup"><span data-stu-id="bd009-258">This allows traditional state management that ignores automatic decay of buffers and simultaneous-access textures.</span></span> <span data-ttu-id="bd009-259">不過，這可能不是理想的做法，因為避免使用已知處於一般狀態之資源的轉換 **ResourceBarrier** 呼叫，可大幅提升效能。</span><span class="sxs-lookup"><span data-stu-id="bd009-259">This may not be desirable though, as avoiding transition **ResourceBarrier** calls with resources known to be in the common state can significantly improve performance.</span></span> <span data-ttu-id="bd009-260">資源障礙的成本可能很高。</span><span class="sxs-lookup"><span data-stu-id="bd009-260">Resource barriers can be expensive.</span></span> <span data-ttu-id="bd009-261">它們是設計來強制快取排清、記憶體配置變更，以及對已處於一般狀態的資源而言，可能不需要的其他同步處理。</span><span class="sxs-lookup"><span data-stu-id="bd009-261">They are designed to force cache flushes, memory layout changes and other synchronization that may not be necessary for resources already in the common state.</span></span> <span data-ttu-id="bd009-262">在目前處於一般狀態的資源上使用資源屏障的命令清單，可能會造成許多不必要的額外負荷。</span><span class="sxs-lookup"><span data-stu-id="bd009-262">A command list that uses a resource barrier from a non-common state to another non-common state on a resource currently in the common state can introduce a lot of unneeded overhead.</span></span>

<span data-ttu-id="bd009-263">此外，除非絕對必要 (，否則請避免明確的 [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) 轉換 D3D12 \_ 資源 \_ 狀態， \_ 例如，下一次存取是在需要在一般) 狀態下啟動資源的複製命令佇列。</span><span class="sxs-lookup"><span data-stu-id="bd009-263">Also, avoid explicit [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) transitions to D3D12\_RESOURCE\_STATE\_COMMON unless absolutely necessary (e.g. the next access is on a COPY command queue which requires a resources begin in the common state).</span></span> <span data-ttu-id="bd009-264">過度轉換成常見狀態可能會大幅降低 GPU 效能。</span><span class="sxs-lookup"><span data-stu-id="bd009-264">Excessive transitions to the common state can dramatically slow down GPU performance.</span></span>

<span data-ttu-id="bd009-265">總而言之，您可以在不發出 [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) 呼叫的情況下，嘗試依賴一般狀態提升和衰減。</span><span class="sxs-lookup"><span data-stu-id="bd009-265">In summary, try to rely on common state promotion and decay whenever its semantics let you get away without issuing [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) calls.</span></span>

## <a name="split-barriers"></a><span data-ttu-id="bd009-266">分割阻礙</span><span class="sxs-lookup"><span data-stu-id="bd009-266">Split Barriers</span></span>

<span data-ttu-id="bd009-267">具有 D3D12 資源屏障旗標「僅限開始」旗標的資源轉換屏障會 \_ \_ \_ \_ \_ 開始分割關卡，而「轉換」關卡則稱為「擱置中」。</span><span class="sxs-lookup"><span data-stu-id="bd009-267">A resource transition barrier with the D3D12\_RESOURCE\_BARRIER\_FLAG\_BEGIN\_ONLY flag begins a split barrier and the transition barrier is said to be pending.</span></span> <span data-ttu-id="bd009-268">當屏障暫止時，GPU 無法讀取或寫入 (子) 資源。</span><span class="sxs-lookup"><span data-stu-id="bd009-268">While the barrier is pending the (sub)resource cannot be read or written by the GPU.</span></span> <span data-ttu-id="bd009-269">唯一可套用至具有暫止屏障之 (子) 資源的合法轉換屏障是具有相同 *之前* 和 *之後* 狀態的資源，以及 D3D12 \_ 資源 \_ 關卡旗標 \_ \_ 結束旗標 \_ ，這會阻礙完成暫止的轉換。</span><span class="sxs-lookup"><span data-stu-id="bd009-269">The only legal transition barrier that can be applied to a (sub)resource with a pending barrier is one with the same *before* and *after* states and the D3D12\_RESOURCE\_BARRIER\_FLAG\_END\_ONLY flag, which barrier completes the pending transition.</span></span>

<span data-ttu-id="bd009-270">分割屏障提供提示給 GPU，之後狀態 *a* 中的資源將在稍後於狀態 *B* 中使用。</span><span class="sxs-lookup"><span data-stu-id="bd009-270">Split barriers provide hints to the GPU that a resource in state *A* will next be used in state *B* sometime later.</span></span> <span data-ttu-id="bd009-271">這會提供 GPU 優化轉換工作負載的選項，可能會減少或避免執行停止。</span><span class="sxs-lookup"><span data-stu-id="bd009-271">This gives the GPU the option to optimize the transition workload, possibly reducing or eliminating execution stalls.</span></span> <span data-ttu-id="bd009-272">發出僅限結束的屏障可保證所有 GPU 轉換工作完成後，再移至下一個命令。</span><span class="sxs-lookup"><span data-stu-id="bd009-272">Issuing the end-only barrier guarantees that all GPU transition work is finished before moving onto the next command.</span></span>

<span data-ttu-id="bd009-273">使用分割關卡有助於改善效能，特別是在多重引擎案例中，或是資源在一或多個命令清單中的讀取/寫入更稀疏的轉換。</span><span class="sxs-lookup"><span data-stu-id="bd009-273">Using split barriers can help to improve performance, especially in multi-engine scenarios or where resources are read/write transitioned sparsely throughout one or more command lists.</span></span>

## <a name="resource-barrier-example-scenario"></a><span data-ttu-id="bd009-274">資源屏障範例案例</span><span class="sxs-lookup"><span data-stu-id="bd009-274">Resource barrier example scenario</span></span>

<span data-ttu-id="bd009-275">下列程式碼片段示範如何在多執行緒範例中使用 [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) 方法。</span><span class="sxs-lookup"><span data-stu-id="bd009-275">The following snippets show the use of the [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) method in a multi-threading sample.</span></span>

<span data-ttu-id="bd009-276">建立深度樣板視圖，並將其轉換為可寫入狀態。</span><span class="sxs-lookup"><span data-stu-id="bd009-276">Creating the depth stencil view, transitioning it to a writeable state.</span></span>


```C++
// Create the depth stencil.
{
    CD3DX12_RESOURCE_DESC shadowTextureDesc(
        D3D12_RESOURCE_DIMENSION_TEXTURE2D,
        0,
        static_cast<UINT>(m_viewport.Width), 
        static_cast<UINT>(m_viewport.Height), 
        1,
        1,
        DXGI_FORMAT_D32_FLOAT,
        1, 
        0,
        D3D12_TEXTURE_LAYOUT_UNKNOWN,
        D3D12_RESOURCE_FLAG_ALLOW_DEPTH_STENCIL | D3D12_RESOURCE_FLAG_DENY_SHADER_RESOURCE);

    D3D12_CLEAR_VALUE clearValue;    // Performance tip: Tell the runtime at resource creation the desired clear value.
    clearValue.Format = DXGI_FORMAT_D32_FLOAT;
    clearValue.DepthStencil.Depth = 1.0f;
    clearValue.DepthStencil.Stencil = 0;

    ThrowIfFailed(m_device->CreateCommittedResource(
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
        D3D12_HEAP_FLAG_NONE,
        &shadowTextureDesc,
        D3D12_RESOURCE_STATE_DEPTH_WRITE,
        &clearValue,
        IID_PPV_ARGS(&m_depthStencil)));

    // Create the depth stencil view.
    m_device->CreateDepthStencilView(m_depthStencil.Get(), nullptr, m_dsvHeap->GetCPUDescriptorHandleForHeapStart());
}
```



<span data-ttu-id="bd009-277">建立頂點緩衝區視圖，先將它從一般狀態變更為目的地，然後從目的地變更為一般可讀取的狀態。</span><span class="sxs-lookup"><span data-stu-id="bd009-277">Creating the vertex buffer view, first changing it from a common state to a destination, then from a destination to a generic readable state.</span></span>


```C++
// Create the vertex buffer.
{
    ThrowIfFailed(m_device->CreateCommittedResource(
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
        D3D12_HEAP_FLAG_NONE,
        &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::VertexDataSize),
        D3D12_RESOURCE_STATE_COPY_DEST,
        nullptr,
        IID_PPV_ARGS(&m_vertexBuffer)));

    {
        ThrowIfFailed(m_device->CreateCommittedResource(
            &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
            D3D12_HEAP_FLAG_NONE,
            &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::VertexDataSize),
            D3D12_RESOURCE_STATE_GENERIC_READ,
            nullptr,
            IID_PPV_ARGS(&m_vertexBufferUpload)));

        // Copy data to the upload heap and then schedule a copy 
        // from the upload heap to the vertex buffer.
        D3D12_SUBRESOURCE_DATA vertexData = {};
        vertexData.pData = pAssetData + SampleAssets::VertexDataOffset;
        vertexData.RowPitch = SampleAssets::VertexDataSize;
        vertexData.SlicePitch = vertexData.RowPitch;

        PIXBeginEvent(commandList.Get(), 0, L"Copy vertex buffer data to default resource...");

        UpdateSubresources<1>(commandList.Get(), m_vertexBuffer.Get(), m_vertexBufferUpload.Get(), 0, 0, 1, &vertexData);
        commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_vertexBuffer.Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_VERTEX_AND_CONSTANT_BUFFER));

        PIXEndEvent(commandList.Get());
    }
```



<span data-ttu-id="bd009-278">建立索引緩衝區視圖，先將它從一般狀態變更為目的地，然後從目的地變更為一般可讀取的狀態。</span><span class="sxs-lookup"><span data-stu-id="bd009-278">Creating the index buffer view, first changing it from a common state to a destination, then from a destination to a generic readable state.</span></span>


```C++
// Create the index buffer.
{
    ThrowIfFailed(m_device->CreateCommittedResource(
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
        D3D12_HEAP_FLAG_NONE,
        &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::IndexDataSize),
        D3D12_RESOURCE_STATE_COPY_DEST,
        nullptr,
        IID_PPV_ARGS(&m_indexBuffer)));

    {
        ThrowIfFailed(m_device->CreateCommittedResource(
            &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
            D3D12_HEAP_FLAG_NONE,
            &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::IndexDataSize),
            D3D12_RESOURCE_STATE_GENERIC_READ,
            nullptr,
            IID_PPV_ARGS(&m_indexBufferUpload)));

        // Copy data to the upload heap and then schedule a copy 
        // from the upload heap to the index buffer.
        D3D12_SUBRESOURCE_DATA indexData = {};
        indexData.pData = pAssetData + SampleAssets::IndexDataOffset;
        indexData.RowPitch = SampleAssets::IndexDataSize;
        indexData.SlicePitch = indexData.RowPitch;

        PIXBeginEvent(commandList.Get(), 0, L"Copy index buffer data to default resource...");

        UpdateSubresources<1>(commandList.Get(), m_indexBuffer.Get(), m_indexBufferUpload.Get(), 0, 0, 1, &indexData);
        commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_indexBuffer.Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_INDEX_BUFFER));

        PIXEndEvent(commandList.Get());
    }

    // Initialize the index buffer view.
    m_indexBufferView.BufferLocation = m_indexBuffer->GetGPUVirtualAddress();
    m_indexBufferView.SizeInBytes = SampleAssets::IndexDataSize;
    m_indexBufferView.Format = SampleAssets::StandardIndexFormat;
}
```



<span data-ttu-id="bd009-279">建立紋理和著色器資源檢視。</span><span class="sxs-lookup"><span data-stu-id="bd009-279">Creating textures and shader resource views.</span></span> <span data-ttu-id="bd009-280">材質會從一般狀態變更為目的地，然後從目的地變更為圖元著色器資源。</span><span class="sxs-lookup"><span data-stu-id="bd009-280">The texture is changed from a common state to a destination, and then from a destination to a pixel shader resource.</span></span>


```C++
    // Create each texture and SRV descriptor.
    const UINT srvCount = _countof(SampleAssets::Textures);
    PIXBeginEvent(commandList.Get(), 0, L"Copy diffuse and normal texture data to default resources...");
    for (int i = 0; i < srvCount; i++)
    {
        // Describe and create a Texture2D.
        const SampleAssets::TextureResource &tex = SampleAssets::Textures[i];
        CD3DX12_RESOURCE_DESC texDesc(
            D3D12_RESOURCE_DIMENSION_TEXTURE2D,
            0,
            tex.Width, 
            tex.Height, 
            1,
            static_cast<UINT16>(tex.MipLevels),
            tex.Format,
            1, 
            0,
            D3D12_TEXTURE_LAYOUT_UNKNOWN,
            D3D12_RESOURCE_FLAG_NONE);

        ThrowIfFailed(m_device->CreateCommittedResource(
            &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
            D3D12_HEAP_FLAG_NONE,
            &texDesc,
            D3D12_RESOURCE_STATE_COPY_DEST,
            nullptr,
            IID_PPV_ARGS(&m_textures[i])));

        {
            const UINT subresourceCount = texDesc.DepthOrArraySize * texDesc.MipLevels;
            UINT64 uploadBufferSize = GetRequiredIntermediateSize(m_textures[i].Get(), 0, subresourceCount);
            ThrowIfFailed(m_device->CreateCommittedResource(
                &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
                D3D12_HEAP_FLAG_NONE,
                &CD3DX12_RESOURCE_DESC::Buffer(uploadBufferSize),
                D3D12_RESOURCE_STATE_GENERIC_READ,
                nullptr,
                IID_PPV_ARGS(&m_textureUploads[i])));

            // Copy data to the intermediate upload heap and then schedule a copy 
            // from the upload heap to the Texture2D.
            D3D12_SUBRESOURCE_DATA textureData = {};
            textureData.pData = pAssetData + tex.Data->Offset;
            textureData.RowPitch = tex.Data->Pitch;
            textureData.SlicePitch = tex.Data->Size;

            UpdateSubresources(commandList.Get(), m_textures[i].Get(), m_textureUploads[i].Get(), 0, 0, subresourceCount, &textureData);
            commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_textures[i].Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE));
        }

        // Describe and create an SRV.
        D3D12_SHADER_RESOURCE_VIEW_DESC srvDesc = {};
        srvDesc.ViewDimension = D3D12_SRV_DIMENSION_TEXTURE2D;
        srvDesc.Shader4ComponentMapping = D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING;
        srvDesc.Format = tex.Format;
        srvDesc.Texture2D.MipLevels = tex.MipLevels;
        srvDesc.Texture2D.MostDetailedMip = 0;
        srvDesc.Texture2D.ResourceMinLODClamp = 0.0f;
        m_device->CreateShaderResourceView(m_textures[i].Get(), &srvDesc, cbvSrvHandle);

        // Move to the next descriptor slot.
        cbvSrvHandle.Offset(cbvSrvDescriptorSize);
    }
```



<span data-ttu-id="bd009-281">開始畫面格;這並不只會使用 [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) 來指出要使用背景緩衝區做為轉譯目標，也會初始化框架資源 (在深度樣板緩衝區) 上呼叫 **ResourceBarrier** 。</span><span class="sxs-lookup"><span data-stu-id="bd009-281">Beginning a frame; this not only uses [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) to indicate that the backbuffer is to be used as a render target, but also initializes the frame resource (which calls **ResourceBarrier** on the depth stencil buffer).</span></span>


```C++
// Assemble the CommandListPre command list.
void D3D12Multithreading::BeginFrame()
{
    m_pCurrentFrameResource->Init();

    // Indicate that the back buffer will be used as a render target.
    m_pCurrentFrameResource->m_commandLists[CommandListPre]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_PRESENT, D3D12_RESOURCE_STATE_RENDER_TARGET));

    // Clear the render target and depth stencil.
    const float clearColor[] = { 0.0f, 0.0f, 0.0f, 1.0f };
    CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart(), m_frameIndex, m_rtvDescriptorSize);
    m_pCurrentFrameResource->m_commandLists[CommandListPre]->ClearRenderTargetView(rtvHandle, clearColor, 0, nullptr);
    m_pCurrentFrameResource->m_commandLists[CommandListPre]->ClearDepthStencilView(m_dsvHeap->GetCPUDescriptorHandleForHeapStart(), D3D12_CLEAR_FLAG_DEPTH, 1.0f, 0, 0, nullptr);

    ThrowIfFailed(m_pCurrentFrameResource->m_commandLists[CommandListPre]->Close());
}

// Assemble the CommandListMid command list.
void D3D12Multithreading::MidFrame()
{
    // Transition our shadow map from the shadow pass to readable in the scene pass.
    m_pCurrentFrameResource->SwapBarriers();

    ThrowIfFailed(m_pCurrentFrameResource->m_commandLists[CommandListMid]->Close());
}
```



<span data-ttu-id="bd009-282">結束畫面格，表示現在會使用背景緩衝區來呈現。</span><span class="sxs-lookup"><span data-stu-id="bd009-282">Ending a frame, indicating the back buffer is now used to present.</span></span>


```C++
// Assemble the CommandListPost command list.
void D3D12Multithreading::EndFrame()
{
    m_pCurrentFrameResource->Finish();

    // Indicate that the back buffer will now be used to present.
    m_pCurrentFrameResource->m_commandLists[CommandListPost]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_RENDER_TARGET, D3D12_RESOURCE_STATE_PRESENT));

    ThrowIfFailed(m_pCurrentFrameResource->m_commandLists[CommandListPost]->Close());
}
```



<span data-ttu-id="bd009-283">初始化框架資源，在開始畫面格時呼叫，會將深度樣板緩衝區轉換為可寫入。</span><span class="sxs-lookup"><span data-stu-id="bd009-283">Initializing a frame resource, called when beginning a frame, transitions the depth stencil buffer to writeable.</span></span>


```C++
void FrameResource::Init()
{
    // Reset the command allocators and lists for the main thread.
    for (int i = 0; i < CommandListCount; i++)
    {
        ThrowIfFailed(m_commandAllocators[i]->Reset());
        ThrowIfFailed(m_commandLists[i]->Reset(m_commandAllocators[i].Get(), m_pipelineState.Get()));
    }

    // Clear the depth stencil buffer in preparation for rendering the shadow map.
    m_commandLists[CommandListPre]->ClearDepthStencilView(m_shadowDepthView, D3D12_CLEAR_FLAG_DEPTH, 1.0f, 0, 0, nullptr);

    // Reset the worker command allocators and lists.
    for (int i = 0; i < NumContexts; i++)
    {
        ThrowIfFailed(m_shadowCommandAllocators[i]->Reset());
        ThrowIfFailed(m_shadowCommandLists[i]->Reset(m_shadowCommandAllocators[i].Get(), m_pipelineStateShadowMap.Get()));

        ThrowIfFailed(m_sceneCommandAllocators[i]->Reset());
        ThrowIfFailed(m_sceneCommandLists[i]->Reset(m_sceneCommandAllocators[i].Get(), m_pipelineState.Get()));
    }
}
```



<span data-ttu-id="bd009-284">阻礙會在框架中交換，將陰影地圖從可寫入轉換為可讀取。</span><span class="sxs-lookup"><span data-stu-id="bd009-284">Barriers are swapped mid-frame, transitioning the shadow map from writeable to readable.</span></span>


```C++
void FrameResource::SwapBarriers()
{
    // Transition the shadow map from writeable to readable.
    m_commandLists[CommandListMid]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_shadowTexture.Get(), D3D12_RESOURCE_STATE_DEPTH_WRITE, D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE));
}
```



<span data-ttu-id="bd009-285">當框架結束時，會呼叫 Finish，將陰影對應轉換為一般狀態。</span><span class="sxs-lookup"><span data-stu-id="bd009-285">Finish is called when a frame is ended, transitioning the shadow map to a common state.</span></span>


```C++
void FrameResource::Finish()
{
    m_commandLists[CommandListPost]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_shadowTexture.Get(), D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE, D3D12_RESOURCE_STATE_DEPTH_WRITE));
}
```



## <a name="common-state-promotion-and-decay-sample"></a><span data-ttu-id="bd009-286">一般狀態提升和衰減範例</span><span class="sxs-lookup"><span data-stu-id="bd009-286">Common state promotion and decay sample</span></span>

``` syntax
    // Create a buffer resource using D3D12_RESOURCE_STATE_COMMON as the init state
    ID3D12Resource *pResource;
    CreateCommittedVertexBufferInCommonState(1024, &pResource);

    // Copy data to the buffer without the need for a barrier.
    // Promotes pResource state to D3D12_RESOURCE_STATE_COPY_DEST.
    pCommandList->CopyBufferRegion(pResource, 0, pOtherResource, 0, 1024); 

    // To use pResource as a vertex buffer a transition barrier is needed.
    // Note the StateBefore is D3D12_RESOURCE_STATE_COPY_DEST.
    D3D12_RESOURCE_BARRIER BarrierDesc = {};
    BarrierDesc.Type = D3D12_RESOURCE_BARRIER_TYPE_TRANSITION;
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_FLAG_NONE;
    BarrierDesc.Transition.pResource = pResource;
    BarrierDesc.Transition.Subresource = 0;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_COPY_DEST;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_VERTEX_AND_CONSTANT_BUFFER;
    pCommandList->ResourceBarrier( 1, &BarrierDesc );

    // Use pResource as a vertex buffer
    D3D12_VERTEX_BUFFER_VIEW vbView;
    vbView.BufferLocation = pResource->GetGPUVirtualAddress();
    vbView.SizeInBytes = 1024;
    vbView.StrideInBytes = sizeof(MyVertex);

    pCommandList->IASetVertexBuffers(0, 1, &vbView);
    pCommandList->Draw();

    pCommandQueue->ExecuteCommandLists(1, &pCommandList); 
    pCommandList->Reset(pAllocator, pPipelineState);

    // Since the reset command list will be executed in a separate call to 
    // ExecuteCommandLists, the previous state of pResource
    // will have decayed to D3D12_RESOURCE_STATE_COMMON so, again, no barrier is needed
    pCommandList->CopyBufferRegion(pResource, 0, pDifferentResource, 0, 1024);

    FinishRecordingCommandList(pCommandList);
    pCommandQueue->ExecuteCommandLists(1, &pCommandList); 

    WaitForQueue(pCommandQueue);

    // The previous ExecuteCommandLists call has finished so 
    // pResource has decayed to D3D12_RESOURCE_STATE_COMMON
```

## <a name="example-of-split-barriers"></a><span data-ttu-id="bd009-287">分割障礙的範例</span><span class="sxs-lookup"><span data-stu-id="bd009-287">Example of split barriers</span></span>

<span data-ttu-id="bd009-288">下列範例示範如何使用分割關卡來減少管線的停止。</span><span class="sxs-lookup"><span data-stu-id="bd009-288">The following example shows how to use a split barrier to reduce pipeline stalls.</span></span> <span data-ttu-id="bd009-289">接下來的程式碼不會使用分割障礙：</span><span class="sxs-lookup"><span data-stu-id="bd009-289">The code that follows does not use split barriers:</span></span>

``` syntax
 D3D12_RESOURCE_BARRIER BarrierDesc = {};
    BarrierDesc.Type = D3D12_RESOURCE_BARRIER_TRANSITION;
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_NONE;
    BarrierDesc.Transition.pResource = pResource;
    BarrierDesc.Transition.Subresource = 0;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_COMMON;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_RENDER_TARGET;

    pCommandList->ResourceBarrier( 1, &BarrierDesc );
    
    Write(pResource); // ... render to pResource
    OtherStuff(); // .. other gpu work

    // Transition pResource to PIXEL_SHADER_RESOURCE
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_RENDER_TARGET;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE;
    
    pCommandList->ResourceBarrier( 1, &BarrierDesc );

    Read(pResource); // ... read from pResource
```

<span data-ttu-id="bd009-290">下列程式碼會使用分割障礙：</span><span class="sxs-lookup"><span data-stu-id="bd009-290">The following code uses split barriers:</span></span>

``` syntax
D3D12_RESOURCE_BARRIER BarrierDesc = {};
    BarrierDesc.Type = D3D12_RESOURCE_BARRIER_TRANSITION;
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_NONE;
    BarrierDesc.Transition.pResource = pResource;
    BarrierDesc.Transition.Subresource = 0;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_COMMON;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_RENDER_TARGET;

    pCommandList->ResourceBarrier( 1, &BarrierDesc );
    
    Write(pResource); // ... render to pResource

    // Done writing to pResource. Start barrier to PIXEL_SHADER_RESOURCE and
    // then do other work
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_BEGIN_ONLY;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_RENDER_TARGET;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE;
    pCommandList->ResourceBarrier( 1, &BarrierDesc );

    OtherStuff(); // .. other gpu work

    // Need to read from pResource so end barrier
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_END_ONLY;

    pCommandList->ResourceBarrier( 1, &BarrierDesc );
    Read(pResource); // ... read from pResource
```

## <a name="related-topics"></a><span data-ttu-id="bd009-291">相關主題</span><span class="sxs-lookup"><span data-stu-id="bd009-291">Related topics</span></span>

[<span data-ttu-id="bd009-292">DirectX advanced learning 影片教學課程：資源阻礙和狀態追蹤</span><span class="sxs-lookup"><span data-stu-id="bd009-292">DirectX advanced learning video tutorials : Resource Barriers and State Tracking</span></span>](https://www.youtube.com/watch?v=nmB2XMasz2o)

[<span data-ttu-id="bd009-293">多引擎同步處理</span><span class="sxs-lookup"><span data-stu-id="bd009-293">Multi-engine synchronization</span></span>](./user-mode-heap-synchronization.md)

[<span data-ttu-id="bd009-294">在 Direct3D 12 中提交工作</span><span class="sxs-lookup"><span data-stu-id="bd009-294">Work Submission in Direct3D 12</span></span>](command-queues-and-command-lists.md)

[<span data-ttu-id="bd009-295">深入瞭解 D3D12 資源狀態的障礙</span><span class="sxs-lookup"><span data-stu-id="bd009-295">A Look Inside D3D12 Resource State Barriers</span></span>](https://devblogs.microsoft.com/directx/a-look-inside-d3d12-resource-state-barriers/)

