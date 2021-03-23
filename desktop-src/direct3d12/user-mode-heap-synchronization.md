---
title: 多引擎同步處理
description: 本主題討論如何同步處理在大部分新式 Gpu 中找到之多個獨立引擎的存取。
ms.assetid: 93903F50-A6CA-41C2-863D-68D645586B4C
ms.localizationpriority: high
ms.topic: article
ms.date: 09/25/2019
ms.openlocfilehash: d60704e411a1ba45dd4902ad9101a416391743dd
ms.sourcegitcommit: 622d149edf775af5a9633c2d12ccfddf7000b8fd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/31/2020
ms.locfileid: "104548345"
---
# <a name="multi-engine-synchronization"></a><span data-ttu-id="66912-103">多引擎同步處理</span><span class="sxs-lookup"><span data-stu-id="66912-103">Multi-engine synchronization</span></span>

<span data-ttu-id="66912-104">大部分新式 Gpu 包含多個可提供特殊功能的獨立引擎。</span><span class="sxs-lookup"><span data-stu-id="66912-104">Most modern GPUs contain multiple independent engines that provide specialized functionality.</span></span> <span data-ttu-id="66912-105">許多人都有一或多個專用的複製引擎和一個計算引擎，通常與3D 引擎不同。</span><span class="sxs-lookup"><span data-stu-id="66912-105">Many have one or more dedicated copy engines, and a compute engine, usually distinct from the 3D engine.</span></span> <span data-ttu-id="66912-106">這些引擎都可以彼此平行執行命令。</span><span class="sxs-lookup"><span data-stu-id="66912-106">Each of these engines can execute commands in parallel with each other.</span></span> <span data-ttu-id="66912-107">Direct3D 12 使用佇列和命令清單，可讓您更精細地存取3D、計算和複製引擎。</span><span class="sxs-lookup"><span data-stu-id="66912-107">Direct3D 12 provides fine-grained access to the 3D, compute, and copy engines, using queues and command lists.</span></span>

## <a name="gpu-engines"></a><span data-ttu-id="66912-108">GPU 引擎</span><span class="sxs-lookup"><span data-stu-id="66912-108">GPU engines</span></span>

<span data-ttu-id="66912-109">下圖顯示標題的 CPU 執行緒，每個執行緒都會填入一或多個複製、計算和3D 佇列。</span><span class="sxs-lookup"><span data-stu-id="66912-109">The following diagram shows a title's CPU threads, each populating one or more of the copy, compute, and 3D queues.</span></span> <span data-ttu-id="66912-110">3D 佇列可以驅動所有三個 GPU 引擎;計算佇列可以驅動計算和複製引擎;而複製佇列則只是複製引擎。</span><span class="sxs-lookup"><span data-stu-id="66912-110">The 3D queue can drive all three GPU engines; the compute queue can drive the compute and copy engines; and the copy queue simply the copy engine.</span></span>

<span data-ttu-id="66912-111">當不同的執行緒擴展佇列時，可能不會有任何簡單的保證執行順序，因此 &mdash; 當標題需要時，需要同步處理機制。</span><span class="sxs-lookup"><span data-stu-id="66912-111">As the different threads populate the queues, there can be no simple guarantee of the order of execution, hence the need for synchronization mechanisms&mdash;when the title requires them.</span></span>

![將命令傳送至三個佇列的四個執行緒](images/gpu-engines.png)

<span data-ttu-id="66912-113">下圖說明標題如何跨多個 GPU 引擎排程工作，包括在必要時進行引擎間同步處理：它會顯示具有引擎間相依性的每個引擎工作負載。</span><span class="sxs-lookup"><span data-stu-id="66912-113">The following image illustrate how a title might schedule work across multiple GPU engines, including inter-engine synchronization where necessary: it shows the per-engine workloads with inter-engine dependencies.</span></span> <span data-ttu-id="66912-114">在此範例中，複製引擎會先複製轉譯所需的一些幾何。</span><span class="sxs-lookup"><span data-stu-id="66912-114">In this example, the copy engine first copies some geometry necessary for rendering.</span></span> <span data-ttu-id="66912-115">3D 引擎會等候這些複本完成，並透過幾何呈現預先傳遞。</span><span class="sxs-lookup"><span data-stu-id="66912-115">The 3D engine waits for these copies to complete, and renders a pre-pass over the geometry.</span></span> <span data-ttu-id="66912-116">然後，計算引擎會使用此功能。</span><span class="sxs-lookup"><span data-stu-id="66912-116">This is then consumed by the compute engine.</span></span> <span data-ttu-id="66912-117">計算引擎 [**分派**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)的結果，以及複製引擎上的數個材質複製作業，都是由3d 引擎用來進行最終 [**繪製**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced) 呼叫。</span><span class="sxs-lookup"><span data-stu-id="66912-117">The results of the compute engine [**Dispatch**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch), along with several texture copy operations on the copy engine, are consumed by the 3D engine for the final [**Draw**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced) call.</span></span>

![複製、圖形和計算引擎通訊](images/gpu-sync.png)

<span data-ttu-id="66912-119">下列虛擬程式碼會說明標題如何提交這類工作負載。</span><span class="sxs-lookup"><span data-stu-id="66912-119">The following pseudo-code illustrates how a title might submit such a workload.</span></span>

``` syntax
// Get per-engine contexts. Note that multiple queues may be exposed
// per engine, however that design is not reflected here.
copyEngine = device->GetCopyEngineContext();
renderEngine = device->GetRenderEngineContext();
computeEngine = device->GetComputeEngineContext();
copyEngine->CopyResource(geometry, ...); // copy geometry
copyEngine->Signal(copyFence, 101);
copyEngine->CopyResource(tex1, ...); // copy textures
copyEngine->CopyResource(tex2, ...); // copy more textures
copyEngine->CopyResource(tex3, ...); // copy more textures
copyEngine->CopyResource(tex4, ...); // copy more textures
copyEngine->Signal(copyFence, 102);
renderEngine->Wait(copyFence, 101); // geometry copied
renderEngine->Draw(); // pre-pass using geometry only into rt1
renderEngine->Signal(renderFence, 201);
computeEngine->Wait(renderFence, 201); // prepass completed
computeEngine->Dispatch(); // lighting calculations on pre-pass (using rt1 as SRV)
computeEngine->Signal(computeFence, 301);
renderEngine->Wait(computeFence, 301); // lighting calculated into buf1
renderEngine->Wait(copyFence, 102); // textures copied
renderEngine->Draw(); // final render using buf1 as SRV, and tex[1-4] SRVs
```

<span data-ttu-id="66912-120">下列虛擬程式碼示範複製和3D 引擎之間的同步處理，以透過信號緩衝區完成類似堆積的記憶體配置。</span><span class="sxs-lookup"><span data-stu-id="66912-120">The following pseudo-code illustrates synchronization between the copy and 3D engines to accomplish heap-like memory allocation via a ring buffer.</span></span> <span data-ttu-id="66912-121">標題可讓您彈性地在最大化平行處理原則 (之間選擇適當的平衡) 並透過小型緩衝區) 減少記憶體耗用量和延遲 (。</span><span class="sxs-lookup"><span data-stu-id="66912-121">Titles have the flexibility to choose the right balance between maximizing parallelism (via a large buffer) and reducing memory consumption and latency (via a small buffer).</span></span>

``` syntax
device->CreateBuffer(&ringCB);
for(int i=1;i++){
  if(i > length) copyEngine->Wait(fence1, i - length);
  copyEngine->Map(ringCB, value%length, WRITE, pData); // copy new data
  copyEngine->Signal(fence2, i);
  renderEngine->Wait(fence2, i);
  renderEngine->Draw(); // draw using copied data
  renderEngine->Signal(fence1, i);
}

// example for length = 3:
// copyEngine->Map();
// copyEngine->Signal(fence2, 1); // fence2 = 1  
// copyEngine->Map();
// copyEngine->Signal(fence2, 2); // fence2 = 2
// copyEngine->Map();
// copyEngine->Signal(fence2, 3); // fence2 = 3
// copy engine has exhausted the ring buffer, so must wait for render to consume it
// copyEngine->Wait(fence1, 1); // fence1 == 0, wait
// renderEngine->Wait(fence2, 1); // fence2 == 3, pass
// renderEngine->Draw();
// renderEngine->Signal(fence1, 1); // fence1 = 1, copy engine now unblocked
// renderEngine->Wait(fence2, 2); // fence2 == 3, pass
// renderEngine->Draw();
// renderEngine->Signal(fence1, 2); // fence1 = 2
// renderEngine->Wait(fence2, 3); // fence2 == 3, pass
// renderEngine->Draw();
// renderEngine->Signal(fence1, 3); // fence1 = 3
// now render engine is starved, and so must wait for the copy engine
// renderEngine->Wait(fence2, 4); // fence2 == 3, wait
```

## <a name="multi-engine-scenarios"></a><span data-ttu-id="66912-122">多引擎案例</span><span class="sxs-lookup"><span data-stu-id="66912-122">Multi-engine scenarios</span></span>

<span data-ttu-id="66912-123">Direct3D 12 可讓您避免意外因非預期的同步處理延遲而發生低效率。</span><span class="sxs-lookup"><span data-stu-id="66912-123">Direct3D 12 allows you to avoid accidentally running into inefficiencies caused by unexpected synchronization delays.</span></span> <span data-ttu-id="66912-124">它也可讓您在較高的層級導入同步處理，在這種情況下，您可以更確定所需的同步處理。</span><span class="sxs-lookup"><span data-stu-id="66912-124">It also allows you to introduce synchronization at a higher level where the required synchronization can be determined with greater certainty.</span></span> <span data-ttu-id="66912-125">多重引擎定址的第二個問題是，更明確地進行昂貴的作業，包括在3D 和影片之間的轉換，因為在多個核心內容之間進行同步處理，所以傳統上會耗費大量的成本。</span><span class="sxs-lookup"><span data-stu-id="66912-125">A second issue that multi-engine addresses is to make expensive operations more explicit, which includes transitions between 3D and video that were traditionally costly because of synchronization between multiple kernel contexts.</span></span>

<span data-ttu-id="66912-126">特別是，下列案例可以透過 Direct3D 12 來解決。</span><span class="sxs-lookup"><span data-stu-id="66912-126">In particular, the following scenarios can be addressed with Direct3D 12.</span></span>

-   <span data-ttu-id="66912-127">非同步和低優先順序的 GPU 工作。</span><span class="sxs-lookup"><span data-stu-id="66912-127">Asynchronous and low priority GPU work.</span></span> <span data-ttu-id="66912-128">這可並存執行低優先順序的 GPU 工作和不可部分完成的作業，讓一個 GPU 執行緒在不封鎖的情況下，使用另一個未同步處理執行緒的結果。</span><span class="sxs-lookup"><span data-stu-id="66912-128">This enables concurrent execution of low priority GPU work and atomic operations that enable one GPU thread to consume the results of another unsynchronized thread without blocking.</span></span>
-   <span data-ttu-id="66912-129">高優先順序的計算工作。</span><span class="sxs-lookup"><span data-stu-id="66912-129">High priority compute work.</span></span> <span data-ttu-id="66912-130">使用背景計算，可以中斷3D 轉譯，以執行少量的高優先順序計算工作。</span><span class="sxs-lookup"><span data-stu-id="66912-130">With background compute it is possible to interrupt 3D rendering to do a small amount of high priority compute work.</span></span> <span data-ttu-id="66912-131">這項工作的結果可提早取得，以在 CPU 上進行額外的處理。</span><span class="sxs-lookup"><span data-stu-id="66912-131">The results of this work can be obtained early for additional processing on the CPU.</span></span>
-   <span data-ttu-id="66912-132">背景計算工作。</span><span class="sxs-lookup"><span data-stu-id="66912-132">Background compute work.</span></span> <span data-ttu-id="66912-133">計算工作負載的個別低優先順序佇列，可讓應用程式利用備用 GPU 迴圈來執行背景計算，而不會對主要轉譯 (或其他) 工作造成負面影響。</span><span class="sxs-lookup"><span data-stu-id="66912-133">A separate low priority queue for compute workloads allows an application to utilize spare GPU cycles to perform background computation without negative impact on the primary rendering (or other) tasks.</span></span> <span data-ttu-id="66912-134">背景工作可能包括解壓縮資源或更新模擬或加速結構。</span><span class="sxs-lookup"><span data-stu-id="66912-134">Background tasks may include decompression of resources or updating simulations or acceleration structures.</span></span> <span data-ttu-id="66912-135">背景工作應該不常在 CPU 上進行同步處理 (大約每個畫面) ，以避免拖延或減緩前景工作。</span><span class="sxs-lookup"><span data-stu-id="66912-135">Background tasks should be synchronized on the CPU infrequently (approximately once per frame) to avoid stalling or slowing foreground work.</span></span>
-   <span data-ttu-id="66912-136">串流和上傳資料。</span><span class="sxs-lookup"><span data-stu-id="66912-136">Streaming and uploading data.</span></span> <span data-ttu-id="66912-137">個別的複製佇列取代了初始資料和更新資源的 D3D11 概念。</span><span class="sxs-lookup"><span data-stu-id="66912-137">A separate copy queue replaces the D3D11 concepts of initial data and updating resources.</span></span> <span data-ttu-id="66912-138">雖然應用程式會負責 Direct3D 12 模型中的更多詳細資料，但這項責任具有強大的功能。</span><span class="sxs-lookup"><span data-stu-id="66912-138">Although the application is responsible for more details in the Direct3D 12 model, this responsibility comes with power.</span></span> <span data-ttu-id="66912-139">應用程式可以控制用來緩衝處理上傳資料的系統記憶體數量。</span><span class="sxs-lookup"><span data-stu-id="66912-139">The application can control how much system memory is devoted to buffering upload data.</span></span> <span data-ttu-id="66912-140">應用程式可以選擇 (CPU 與 GPU 的時機和方式、封鎖與非封鎖的) 同步處理，以及追蹤進度及控制已排入佇列的工作量。</span><span class="sxs-lookup"><span data-stu-id="66912-140">The app can choose when and how (CPU vs GPU, blocking vs non-blocking) to synchronize, and can track progress and control the amount of queued work.</span></span>
-   <span data-ttu-id="66912-141">提高的平行處理原則。</span><span class="sxs-lookup"><span data-stu-id="66912-141">Increased parallelism.</span></span> <span data-ttu-id="66912-142">應用程式可以針對背景工作負載使用更深入的佇列 (例如，當它們有個別的佇列可用於前景工作時，) 的影片解碼。</span><span class="sxs-lookup"><span data-stu-id="66912-142">Applications can use deeper queues for background workloads (e.g. video decode) when they have separate queues for foreground work.</span></span>

<span data-ttu-id="66912-143">在 Direct3D 12 中，命令佇列的概念是應用程式所提交之大約一連串序列工作的 API 標記法。</span><span class="sxs-lookup"><span data-stu-id="66912-143">In Direct3D 12 the concept of a command queue is the API representation of a roughly serial sequence of work submitted by the application.</span></span> <span data-ttu-id="66912-144">屏障和其他技術可讓您在管線中或依循序執行此工作，但應用程式只會看到單一完成時間軸。</span><span class="sxs-lookup"><span data-stu-id="66912-144">Barriers and other techniques allow this work to be executed in a pipeline or out of order, but the application only sees a single completion timeline.</span></span> <span data-ttu-id="66912-145">這會對應到 D3D11 中的直屬內容。</span><span class="sxs-lookup"><span data-stu-id="66912-145">This corresponds to the immediate context in D3D11.</span></span>

## <a name="synchronization-apis"></a><span data-ttu-id="66912-146">同步處理 Api</span><span class="sxs-lookup"><span data-stu-id="66912-146">Synchronization APIs</span></span>

### <a name="devices-and-queues"></a><span data-ttu-id="66912-147">裝置和佇列</span><span class="sxs-lookup"><span data-stu-id="66912-147">Devices and queues</span></span>

<span data-ttu-id="66912-148">Direct3D 12 裝置有方法可建立及取出不同類型和優先順序的命令佇列。</span><span class="sxs-lookup"><span data-stu-id="66912-148">The Direct3D 12 device has methods to create and retrieve command queues of different types and priorities.</span></span> <span data-ttu-id="66912-149">大部分的應用程式都應該使用預設的命令佇列，因為它們允許其他元件共用使用量。</span><span class="sxs-lookup"><span data-stu-id="66912-149">Most applications should use the default command queues because these allow for shared usage by other components.</span></span> <span data-ttu-id="66912-150">具有額外並行需求的應用程式可以建立額外的佇列。</span><span class="sxs-lookup"><span data-stu-id="66912-150">Applications with additional concurrency requirements can create additional queues.</span></span> <span data-ttu-id="66912-151">佇列是由其取用的命令清單類型所指定。</span><span class="sxs-lookup"><span data-stu-id="66912-151">Queues are specified by the command list type that they consume.</span></span>

<span data-ttu-id="66912-152">請參閱下列 [**ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device)的建立方法。</span><span class="sxs-lookup"><span data-stu-id="66912-152">Refer to the following creation methods of [**ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device).</span></span>

-   <span data-ttu-id="66912-153">[**CreateCommandQueue**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue) ：根據 [**Direct3D 12 \_ 命令 \_ 佇列 \_ DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc) 結構中的資訊建立命令佇列。</span><span class="sxs-lookup"><span data-stu-id="66912-153">[**CreateCommandQueue**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue) : creates a command queue based on information in a [**Direct3D 12\_COMMAND\_QUEUE\_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc) structure.</span></span>
-   <span data-ttu-id="66912-154">[**CreateCommandList**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist) ：建立 [**Direct3D 12 \_ 命令 \_ 清單 \_ 類型**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type)類型的命令清單。</span><span class="sxs-lookup"><span data-stu-id="66912-154">[**CreateCommandList**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist) : creates a command list of type [**Direct3D 12\_COMMAND\_LIST\_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type).</span></span>
-   <span data-ttu-id="66912-155">[**CreateFence**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence) ：建立一個範圍，並記下 [**Direct3D 12 \_ 隔離 \_ 旗標**](/windows/win32/api/d3d12/ne-d3d12-d3d12_fence_flags)中的旗標。</span><span class="sxs-lookup"><span data-stu-id="66912-155">[**CreateFence**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence) : creates a fence, noting the flags in [**Direct3D 12\_FENCE\_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_fence_flags).</span></span> <span data-ttu-id="66912-156">使用的是用來同步處理佇列。</span><span class="sxs-lookup"><span data-stu-id="66912-156">Fences are used to synchronize queues.</span></span>

<span data-ttu-id="66912-157">所有類型 (3D、計算和複製) 的佇列會共用相同的介面，並以所有命令清單為基礎。</span><span class="sxs-lookup"><span data-stu-id="66912-157">Queues of all types (3D, compute and copy) share the same interface and are all command-list based.</span></span>

<span data-ttu-id="66912-158">請參閱下列 [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue)方法。</span><span class="sxs-lookup"><span data-stu-id="66912-158">Refer to the following methods of [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue).</span></span>

-   <span data-ttu-id="66912-159">[**ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) ：提交要執行的命令清單陣列。</span><span class="sxs-lookup"><span data-stu-id="66912-159">[**ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) : submits an array of command lists for execution.</span></span> <span data-ttu-id="66912-160">每個命令清單都是由 [**ID3D12CommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist)所定義。</span><span class="sxs-lookup"><span data-stu-id="66912-160">Each command list being defined by [**ID3D12CommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist).</span></span>
-   <span data-ttu-id="66912-161">[**信號**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal) ：當 (在 GPU 上執行的佇列) 達到特定點時，設定隔離值。</span><span class="sxs-lookup"><span data-stu-id="66912-161">[**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal) : sets a fence value when the queue (running on the GPU) reaches a certain point.</span></span>
-   <span data-ttu-id="66912-162">[**等候**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait) ：佇列會等到指定的範圍達到指定的值為止。</span><span class="sxs-lookup"><span data-stu-id="66912-162">[**Wait**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait) : the queue waits until the specified fence reaches the specified value.</span></span>

<span data-ttu-id="66912-163">請注意，所有佇列都不會使用組合，因此不能使用此類型來建立佇列。</span><span class="sxs-lookup"><span data-stu-id="66912-163">Note that bundles are not consumed by any queues and therefore this type cannot be used to create a queue.</span></span>

### <a name="fences"></a><span data-ttu-id="66912-164">柵欄</span><span class="sxs-lookup"><span data-stu-id="66912-164">Fences</span></span>

<span data-ttu-id="66912-165">多引擎 API 提供明確的 Api，以使用圍牆來建立和同步處理。</span><span class="sxs-lookup"><span data-stu-id="66912-165">The multi-engine API provides explicit APIs to create and synchronize using fences.</span></span> <span data-ttu-id="66912-166">範圍是由 UINT64 值所控制的同步處理結構。</span><span class="sxs-lookup"><span data-stu-id="66912-166">A fence is a synchronization construct controlled by a UINT64 value.</span></span> <span data-ttu-id="66912-167">隔離值是由應用程式設定。</span><span class="sxs-lookup"><span data-stu-id="66912-167">Fence values are set by the application.</span></span> <span data-ttu-id="66912-168">信號作業會修改隔離值，而等候作業會封鎖，直到範圍達到要求的值或更高的值。</span><span class="sxs-lookup"><span data-stu-id="66912-168">A signal operation modifies the fence value and a wait operation blocks until the fence has reached the requested value or greater.</span></span> <span data-ttu-id="66912-169">當範圍達到特定值時，就會引發事件。</span><span class="sxs-lookup"><span data-stu-id="66912-169">An event can be fired when a fence reaches a certain value.</span></span>

<span data-ttu-id="66912-170">請參閱 [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) 介面的方法。</span><span class="sxs-lookup"><span data-stu-id="66912-170">Refer to the methods of the [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) interface.</span></span>

-   <span data-ttu-id="66912-171">[**GetCompletedValue**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue) ：傳回目前的範圍值。</span><span class="sxs-lookup"><span data-stu-id="66912-171">[**GetCompletedValue**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue) : returns the current value of the fence.</span></span>
-   <span data-ttu-id="66912-172">[**SetEventOnCompletion**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-seteventoncompletion) ：當範圍達到指定值時，就會引發事件。</span><span class="sxs-lookup"><span data-stu-id="66912-172">[**SetEventOnCompletion**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-seteventoncompletion) : causes an event to fire when the fence reaches a given value.</span></span>
-   <span data-ttu-id="66912-173">[**信號**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-signal) ：將範圍設定為指定的值。</span><span class="sxs-lookup"><span data-stu-id="66912-173">[**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-signal) : sets the fence to the given value.</span></span>

<span data-ttu-id="66912-174">範圍可讓 CPU 存取目前的隔離值，以及 CPU 等候和信號。</span><span class="sxs-lookup"><span data-stu-id="66912-174">Fences allow CPU access to the current fence value, and CPU waits and signals.</span></span>

<span data-ttu-id="66912-175">[**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence)介面上的 [**信號**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-signal)方法會更新 CPU 端的隔離。</span><span class="sxs-lookup"><span data-stu-id="66912-175">The [**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-signal) method on the [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) interface updates a fence from the CPU side.</span></span> <span data-ttu-id="66912-176">此更新會立即進行。</span><span class="sxs-lookup"><span data-stu-id="66912-176">This update occurs immediately.</span></span> <span data-ttu-id="66912-177">[**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue)上的 [**信號**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal)方法會更新 GPU 端的隔離。</span><span class="sxs-lookup"><span data-stu-id="66912-177">The [**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal) method on [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue) updates a fence from the GPU side.</span></span> <span data-ttu-id="66912-178">此更新會在命令佇列上的所有其他作業都已完成之後發生。</span><span class="sxs-lookup"><span data-stu-id="66912-178">This update occurs after all other operations on the command queue have been completed.</span></span>

<span data-ttu-id="66912-179">多引擎安裝程式中的所有節點都可以讀取和回應任何範圍，達到正確的值。</span><span class="sxs-lookup"><span data-stu-id="66912-179">All nodes in a multi-engine setup can read and react to any fence reaching the right value.</span></span>

<span data-ttu-id="66912-180">應用程式會設定自己的隔離值，好的起點可能會針對每個框架增加一次範圍。</span><span class="sxs-lookup"><span data-stu-id="66912-180">Applications set their own fence values, a good starting point might be increasing a fence once per frame.</span></span>

<span data-ttu-id="66912-181">*可* 倒轉的範圍 *。*</span><span class="sxs-lookup"><span data-stu-id="66912-181">A fence *may* be *rewound*.</span></span> <span data-ttu-id="66912-182">這表示，隔離值不需要單獨遞增。</span><span class="sxs-lookup"><span data-stu-id="66912-182">This means that the fence value does not need to solely increment.</span></span> <span data-ttu-id="66912-183">如果在兩個不同的命令佇列上將 **信號** 作業排入佇列，或兩個 CPU 執行緒都在一個範圍上呼叫 **信號** ，則可能會有一個競爭來判斷最後最後一個 **信號** 的完成，因此會保留哪一個隔離值。</span><span class="sxs-lookup"><span data-stu-id="66912-183">If a **Signal** operation is enqueued on two different command queues, or if two CPU threads are both calling **Signal** on a fence, there may be a race to determine which **Signal** completes last, and therefore which fence value is the one which will remain.</span></span> <span data-ttu-id="66912-184">如果已倒轉範圍，任何新的等候 (包括 **SetEventOnCompletion** 要求) 將會與新的較低範圍值進行比對，因此即使此範圍值之前夠高足以滿足這些要求，也可能不會對其感到滿意。</span><span class="sxs-lookup"><span data-stu-id="66912-184">If a fence is rewound, any new waits (including **SetEventOnCompletion** requests) will be compared against the new lower fence value, and therefore may not be satisfied, even if the fence value had previously been high enough to satisfy them.</span></span> <span data-ttu-id="66912-185">如果發生競爭情形，則在可滿足未完成等候的值與較低的值之間， *將會符合等候，* 而不考慮之後剩下的值。</span><span class="sxs-lookup"><span data-stu-id="66912-185">If a race does occur, between a value which will satisfy an outstanding wait, and a lower value which will not, the wait *will* be satisfied regardless of which value remains afterwards.</span></span>

<span data-ttu-id="66912-186">隔離 Api 提供功能強大的同步處理功能，但可能會導致難以偵測的問題。</span><span class="sxs-lookup"><span data-stu-id="66912-186">The fence APIs provide powerful synchronization functionality but can create potentially difficult to debug issues.</span></span> <span data-ttu-id="66912-187">建議您只使用每個隔離來指出某個時間軸上的進度，以防止 signalers 之間的競爭。</span><span class="sxs-lookup"><span data-stu-id="66912-187">It is recommended that each fence only be used to indicate progress on one timeline to prevent races between signalers.</span></span>

### <a name="copy-and-compute-command-lists"></a><span data-ttu-id="66912-188">複製和計算命令清單</span><span class="sxs-lookup"><span data-stu-id="66912-188">Copy and compute command lists</span></span>

<span data-ttu-id="66912-189">所有三種類型的命令清單都會使用 [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) 介面，不過複製和計算只支援方法的子集。</span><span class="sxs-lookup"><span data-stu-id="66912-189">All three types of command list use the [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) interface, however only a subset of the methods are supported for copy and compute.</span></span>

<span data-ttu-id="66912-190">複製和計算命令清單可以使用下列方法。</span><span class="sxs-lookup"><span data-stu-id="66912-190">Copy and compute command lists can use the following methods.</span></span>

-   [<span data-ttu-id="66912-191">**關閉**</span><span class="sxs-lookup"><span data-stu-id="66912-191">**Close**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)
-   [<span data-ttu-id="66912-192">**CopyBufferRegion**</span><span class="sxs-lookup"><span data-stu-id="66912-192">**CopyBufferRegion**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
-   [<span data-ttu-id="66912-193">**CopyResource**</span><span class="sxs-lookup"><span data-stu-id="66912-193">**CopyResource**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
-   [<span data-ttu-id="66912-194">**CopyTextureRegion**</span><span class="sxs-lookup"><span data-stu-id="66912-194">**CopyTextureRegion**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
-   [<span data-ttu-id="66912-195">**CopyTiles**</span><span class="sxs-lookup"><span data-stu-id="66912-195">**CopyTiles**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles)
-   [<span data-ttu-id="66912-196">**重設**</span><span class="sxs-lookup"><span data-stu-id="66912-196">**Reset**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset)
-   [<span data-ttu-id="66912-197">**ResourceBarrier**</span><span class="sxs-lookup"><span data-stu-id="66912-197">**ResourceBarrier**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)

<span data-ttu-id="66912-198">計算命令清單也可以使用下列方法。</span><span class="sxs-lookup"><span data-stu-id="66912-198">Compute command lists can also use the following methods.</span></span>

-   [<span data-ttu-id="66912-199">**ClearState**</span><span class="sxs-lookup"><span data-stu-id="66912-199">**ClearState**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearstate)
-   [<span data-ttu-id="66912-200">**ClearUnorderedAccessViewFloat**</span><span class="sxs-lookup"><span data-stu-id="66912-200">**ClearUnorderedAccessViewFloat**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat)
-   [<span data-ttu-id="66912-201">**ClearUnorderedAccessViewUint**</span><span class="sxs-lookup"><span data-stu-id="66912-201">**ClearUnorderedAccessViewUint**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint)
-   [<span data-ttu-id="66912-202">**DiscardResource**</span><span class="sxs-lookup"><span data-stu-id="66912-202">**DiscardResource**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource)
-   [<span data-ttu-id="66912-203">**分派**</span><span class="sxs-lookup"><span data-stu-id="66912-203">**Dispatch**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)
-   [<span data-ttu-id="66912-204">**ExecuteIndirect**</span><span class="sxs-lookup"><span data-stu-id="66912-204">**ExecuteIndirect**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect)
-   [<span data-ttu-id="66912-205">**SetComputeRoot32BitConstant**</span><span class="sxs-lookup"><span data-stu-id="66912-205">**SetComputeRoot32BitConstant**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstant)
-   [<span data-ttu-id="66912-206">**SetComputeRoot32BitConstants**</span><span class="sxs-lookup"><span data-stu-id="66912-206">**SetComputeRoot32BitConstants**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstants)
-   [<span data-ttu-id="66912-207">**SetComputeRootConstantBufferView**</span><span class="sxs-lookup"><span data-stu-id="66912-207">**SetComputeRootConstantBufferView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootconstantbufferview)
-   [<span data-ttu-id="66912-208">**SetComputeRootDescriptorTable**</span><span class="sxs-lookup"><span data-stu-id="66912-208">**SetComputeRootDescriptorTable**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable)
-   [<span data-ttu-id="66912-209">**SetComputeRootShaderResourceView**</span><span class="sxs-lookup"><span data-stu-id="66912-209">**SetComputeRootShaderResourceView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootshaderresourceview)
-   [<span data-ttu-id="66912-210">**SetComputeRootSignature**</span><span class="sxs-lookup"><span data-stu-id="66912-210">**SetComputeRootSignature**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature)
-   [<span data-ttu-id="66912-211">**SetComputeRootUnorderedAccessView**</span><span class="sxs-lookup"><span data-stu-id="66912-211">**SetComputeRootUnorderedAccessView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootunorderedaccessview)
-   [<span data-ttu-id="66912-212">**SetDescriptorHeaps**</span><span class="sxs-lookup"><span data-stu-id="66912-212">**SetDescriptorHeaps**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)
-   [<span data-ttu-id="66912-213">**SetPipelineState**</span><span class="sxs-lookup"><span data-stu-id="66912-213">**SetPipelineState**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate)
-   [<span data-ttu-id="66912-214">**SetPredication**</span><span class="sxs-lookup"><span data-stu-id="66912-214">**SetPredication**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication)

<span data-ttu-id="66912-215">在呼叫 [**SetPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate)時，計算命令清單必須設定計算 PSO。</span><span class="sxs-lookup"><span data-stu-id="66912-215">Compute command lists must set a compute PSO when calling [**SetPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate).</span></span>

<span data-ttu-id="66912-216">套件組合無法搭配計算或複製命令清單或佇列使用。</span><span class="sxs-lookup"><span data-stu-id="66912-216">Bundles cannot be used with compute or copy command lists or queues.</span></span>

## <a name="pipelined-compute-and-graphics-example"></a><span data-ttu-id="66912-217">管線計算和圖形範例</span><span class="sxs-lookup"><span data-stu-id="66912-217">Pipelined compute and graphics example</span></span>

<span data-ttu-id="66912-218">此範例示範如何使用範圍同步處理，在佇列上建立計算工作的管線 (由佇列中的 `pComputeQueue` 圖形工作所使用的) 所參考 `pGraphicsQueue` 。</span><span class="sxs-lookup"><span data-stu-id="66912-218">This example shows how fence synchronization can be used to create a pipeline of compute work on a queue (referenced by `pComputeQueue`) that's consumed by graphics work on queue `pGraphicsQueue`.</span></span> <span data-ttu-id="66912-219">計算和圖形工作會使用圖形佇列來進行管線處理，從數個畫面格取用計算工作的結果，而 CPU 事件則是用來節流整個佇列的總工作。</span><span class="sxs-lookup"><span data-stu-id="66912-219">The compute and graphics work is pipelined with the graphics queue consuming the result of compute work from several frames back, and a CPU event is used to throttle the total work queued overall.</span></span>

```cpp
void PipelinedComputeGraphics()
{
    const UINT CpuLatency = 3;
    const UINT ComputeGraphicsLatency = 2;

    HANDLE handle = CreateEvent(nullptr, FALSE, FALSE, nullptr);

    UINT64 FrameNumber = 0;

    while (1)
    {
        if (FrameNumber > ComputeGraphicsLatency)
        {
            pComputeQueue->Wait(pGraphicsFence,
                FrameNumber - ComputeGraphicsLatency);
        }

        if (FrameNumber > CpuLatency)
        {
            pComputeFence->SetEventOnFenceCompletion(
                FrameNumber - CpuLatency,
                handle);
            WaitForSingleObject(handle, INFINITE);
        }

        ++FrameNumber;

        pComputeQueue->ExecuteCommandLists(1, &pComputeCommandList);
        pComputeQueue->Signal(pComputeFence, FrameNumber);
        if (FrameNumber > ComputeGraphicsLatency)
        {
            UINT GraphicsFrameNumber = FrameNumber - ComputeGraphicsLatency;
            pGraphicsQueue->Wait(pComputeFence, GraphicsFrameNumber);
            pGraphicsQueue->ExecuteCommandLists(1, &pGraphicsCommandList);
            pGraphicsQueue->Signal(pGraphicsFence, GraphicsFrameNumber);
        }
    }
}
```

<span data-ttu-id="66912-220">若要支援此管線，必須有 `ComputeGraphicsLatency+1` 從計算佇列傳遞至圖形佇列的不同資料複本的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="66912-220">To support this pipelining, there must be a buffer of `ComputeGraphicsLatency+1` different copies of the data passing from the compute queue to the graphics queue.</span></span> <span data-ttu-id="66912-221">命令清單必須使用 UAVs 和間接取值，從緩衝區中資料的適當「版本」中讀取和寫入。</span><span class="sxs-lookup"><span data-stu-id="66912-221">The command lists must use UAVs and indirection to read and write from the appropriate “version” of the data in the buffer.</span></span> <span data-ttu-id="66912-222">計算佇列必須等到圖形佇列完成讀取畫面格 N 的資料後，才能寫入框架 `N+ComputeGraphicsLatency` 。</span><span class="sxs-lookup"><span data-stu-id="66912-222">The compute queue must wait until the graphics queue has finished reading from the data for frame N before it can write frame `N+ComputeGraphicsLatency`.</span></span>

<span data-ttu-id="66912-223">請注意，相對於 CPU 的計算佇列數量不會直接取決於所需的緩衝量，不過，將 GPU 的工作量超過可用的緩衝區空間量並不重要。</span><span class="sxs-lookup"><span data-stu-id="66912-223">Note that the amount of compute queue worked relative to the CPU does not depend directly on the amount of buffering required, however, queuing GPU work beyond the amount of buffer space available is less valuable.</span></span>

<span data-ttu-id="66912-224">避免間接取值的替代機制是建立多個對應到每個「重新命名」版本資料的命令清單。</span><span class="sxs-lookup"><span data-stu-id="66912-224">An alternative mechanism to avoid indirection would be to create multiple command lists corresponding to each of the “renamed” versions of the data.</span></span> <span data-ttu-id="66912-225">下一個範例會使用這項技術來擴充先前的範例，讓計算和圖形佇列以非同步方式執行。</span><span class="sxs-lookup"><span data-stu-id="66912-225">The next example uses this technique while extending the previous example to allow the compute and graphics queues to run more asynchronously.</span></span>

## <a name="asynchronous-compute-and-graphics-example"></a><span data-ttu-id="66912-226">非同步計算和圖形範例</span><span class="sxs-lookup"><span data-stu-id="66912-226">Asynchronous compute and graphics example</span></span>

<span data-ttu-id="66912-227">下一個範例可讓圖形從計算佇列以非同步方式呈現。</span><span class="sxs-lookup"><span data-stu-id="66912-227">This next example allows graphics to render asynchronously from the compute queue.</span></span> <span data-ttu-id="66912-228">這兩個階段之間仍有固定的緩衝資料量，但現在圖形工作會獨立執行，並使用在圖形工作排入佇列時 CPU 上已知的計算階段最新結果。</span><span class="sxs-lookup"><span data-stu-id="66912-228">There is still a fixed amount of buffered data between the two stages, however now graphics work proceeds independently and uses the most up-to-date result of the compute stage as known on the CPU when the graphics work is queued.</span></span> <span data-ttu-id="66912-229">如果圖形工作正在由其他來源（例如使用者輸入）進行更新，這將會很有用。</span><span class="sxs-lookup"><span data-stu-id="66912-229">This would be useful if the graphics work was being updated by another source, for example user input.</span></span> <span data-ttu-id="66912-230">必須要有多個命令清單，才能讓 `ComputeGraphicsLatency` 圖形工作的框架一次在飛行，而此函式 `UpdateGraphicsCommandList` 代表更新命令清單來包含最新的輸入資料，並從適當的緩衝區讀取計算資料。</span><span class="sxs-lookup"><span data-stu-id="66912-230">There must be multiple command lists to allow the `ComputeGraphicsLatency` frames of graphics work to be in flight at a time, and the function `UpdateGraphicsCommandList` represents updating the command list to include the most recent input data and read from the compute data from the appropriate buffer.</span></span>

<span data-ttu-id="66912-231">計算佇列仍然必須等待圖形佇列完成管道緩衝區，但導入了第三個範圍 () ， `pGraphicsComputeFence` 讓圖形讀取計算工作的進度和一般圖形進度都可以追蹤。</span><span class="sxs-lookup"><span data-stu-id="66912-231">The compute queue must still wait for the graphics queue to finish with the pipe buffers, but a third fence (`pGraphicsComputeFence`) is introduced so that the progress of graphics reading compute work versus graphics progress in general can be tracked.</span></span> <span data-ttu-id="66912-232">這會反映出現在連續圖形框架可以從相同計算結果讀取的事實，或可能略過計算結果。</span><span class="sxs-lookup"><span data-stu-id="66912-232">This reflects the fact that now consecutive graphics frames could read from the same compute result or could skip a compute result.</span></span> <span data-ttu-id="66912-233">更有效率但稍微複雜的設計只會使用單一圖形範圍，並將對應儲存至每個圖形框架所使用的計算框架。</span><span class="sxs-lookup"><span data-stu-id="66912-233">A more efficient but slightly more complicated design would use just the single graphics fence and store a mapping to the compute frames used by each graphics frame.</span></span>

```cpp
void AsyncPipelinedComputeGraphics()
{
    const UINT CpuLatency{ 3 };
    const UINT ComputeGraphicsLatency{ 2 };

    // The compute fence is at index 0; the graphics fence is at index 1.
    ID3D12Fence* rgpFences[]{ pComputeFence, pGraphicsFence };
    HANDLE handles[2];
    handles[0] = CreateEvent(nullptr, FALSE, TRUE, nullptr);
    handles[1] = CreateEvent(nullptr, FALSE, TRUE, nullptr);
    UINT FrameNumbers[]{ 0, 0 };

    ID3D12GraphicsCommandList* rgpGraphicsCommandLists[CpuLatency];
    CreateGraphicsCommandLists(ARRAYSIZE(rgpGraphicsCommandLists),
        rgpGraphicsCommandLists);

    // Graphics needs to wait for the first compute frame to complete; this is the
    // only wait that the graphics queue will perform.
    pGraphicsQueue->Wait(pComputeFence, 1);

    while (true)
    {
        for (auto i = 0; i < 2; ++i)
        {
            if (FrameNumbers[i] > CpuLatency)
            {
                rgpFences[i]->SetEventOnCompletion(
                    FrameNumbers[i] - CpuLatency,
                    handles[i]);
            }
            else
            {
                ::SetEvent(handles[i]);
            }
        }


        auto WaitResult = ::WaitForMultipleObjects(2, handles, FALSE, INFINITE);
        if (WaitResult > WAIT_OBJECT_0 + 1) continue;
        auto Stage = WaitResult - WAIT_OBJECT_0;
        ++FrameNumbers[Stage];

        switch (Stage)
        {
        case 0:
        {
            if (FrameNumbers[Stage] > ComputeGraphicsLatency)
            {
                pComputeQueue->Wait(pGraphicsComputeFence,
                    FrameNumbers[Stage] - ComputeGraphicsLatency);
            }
            pComputeQueue->ExecuteCommandLists(1, &pComputeCommandList);
            pComputeQueue->Signal(pComputeFence, FrameNumbers[Stage]);
            break;
        }
        case 1:
        {
            // Recall that the GPU queue started with a wait for pComputeFence, 1
            UINT64 CompletedComputeFrames = min(1,
                pComputeFence->GetCompletedValue());
            UINT64 PipeBufferIndex =
                (CompletedComputeFrames - 1) % ComputeGraphicsLatency;
            UINT64 CommandListIndex = (FrameNumbers[Stage] - 1) % CpuLatency;
            // Update graphics command list based on CPU input and using the appropriate
            // buffer index for data produced by compute.
            UpdateGraphicsCommandList(PipeBufferIndex,
                rgpGraphicsCommandLists[CommandListIndex]);

            // Signal *before* new rendering to indicate what compute work
            // the graphics queue is DONE with
            pGraphicsQueue->Signal(pGraphicsComputeFence, CompletedComputeFrames - 1);
            pGraphicsQueue->ExecuteCommandLists(1,
                rgpGraphicsCommandLists + PipeBufferIndex);
            pGraphicsQueue->Signal(pGraphicsFence, FrameNumbers[Stage]);
            break;
        }
        }
    }
}
```

## <a name="multi-queue-resource-access"></a><span data-ttu-id="66912-234">多佇列資源存取</span><span class="sxs-lookup"><span data-stu-id="66912-234">Multi-queue resource access</span></span>

<span data-ttu-id="66912-235">若要存取一個以上佇列的資源，應用程式必須遵守下列規則。</span><span class="sxs-lookup"><span data-stu-id="66912-235">To access a resource on more than one queue an application must adhere to the following rules.</span></span>

-   <span data-ttu-id="66912-236">資源存取 (請參閱 [**Direct3D 12 \_ 資源 \_ 狀態**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) ，) 由佇列類型類別非佇列物件所決定。</span><span class="sxs-lookup"><span data-stu-id="66912-236">Resource access (refer to [**Direct3D 12\_RESOURCE\_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states)) is determined by queue type class not queue object.</span></span> <span data-ttu-id="66912-237">佇列的類型有兩種：計算/3D 佇列是一種類型類別，Copy 是第二種類型類別。</span><span class="sxs-lookup"><span data-stu-id="66912-237">There are two type classes of queue: Compute/3D queue is one type class, Copy is a second type class.</span></span> <span data-ttu-id="66912-238">因此，在 \_ \_ 一個3d 佇列上具有非圖元著色器資源狀態之障礙的資源 \_ ，可以在任何3d 或計算佇列上以該狀態使用，受限於需要序列化大部分寫入的同步處理需求。</span><span class="sxs-lookup"><span data-stu-id="66912-238">So a resource that has a barrier to the NON\_PIXEL\_SHADER\_RESOURCE state on one 3D queue can be used in that state on any 3D or Compute queue, subject to synchronization requirements which require most writes to be serialized.</span></span> <span data-ttu-id="66912-239">在兩個類型類別之間共用的資源狀態 (複製 \_ 來源和複製 \_ 目的地) 會視為每個類型類別的不同狀態。</span><span class="sxs-lookup"><span data-stu-id="66912-239">The resource states that are shared between the two type classes (COPY\_SOURCE and COPY\_DEST) are considered different states for each type class.</span></span> <span data-ttu-id="66912-240">如此一來，如果資源轉換為複製 \_ 佇列上的目的地，則無法從3d 或計算佇列的複製目的地存取該資源，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="66912-240">So that if a resource transitions to COPY\_DEST on a Copy queue it is not accessible as a copy destination from 3D or Compute queues and vice versa.</span></span>

    <span data-ttu-id="66912-241">總結。</span><span class="sxs-lookup"><span data-stu-id="66912-241">To summarize.</span></span>

    -   <span data-ttu-id="66912-242">佇列「物件」是任何單一佇列。</span><span class="sxs-lookup"><span data-stu-id="66912-242">A queue "object" is any single queue.</span></span>
    -   <span data-ttu-id="66912-243">佇列「類型」是下列三種之一：計算、3D 和複製。</span><span class="sxs-lookup"><span data-stu-id="66912-243">A queue "type" is any one of these three: Compute, 3D, and Copy.</span></span>
    -   <span data-ttu-id="66912-244">佇列「類型類別」是下列其中一項：計算/3D 和複製。</span><span class="sxs-lookup"><span data-stu-id="66912-244">A queue "type class" is any one of these two: Compute/3D and Copy.</span></span>

-   <span data-ttu-id="66912-245">複製旗標 (複製 \_ 目的地和複製 \_ 來源) 當做初始狀態使用，代表 3D/計算類型類別中的狀態。</span><span class="sxs-lookup"><span data-stu-id="66912-245">The COPY flags (COPY\_DEST and COPY\_SOURCE) used as initial states represent states in the 3D/Compute type class.</span></span> <span data-ttu-id="66912-246">若要在一開始就在複製佇列上使用資源，它應該會在一般狀態中啟動。</span><span class="sxs-lookup"><span data-stu-id="66912-246">To use a resource initially on a Copy queue it should start in the COMMON state.</span></span> <span data-ttu-id="66912-247">您可以使用隱含狀態轉換，將一般狀態用於複製佇列上的所有使用量。</span><span class="sxs-lookup"><span data-stu-id="66912-247">The COMMON state can be used for all usages on a Copy queue using the implicit state transitions.</span></span> 
-   <span data-ttu-id="66912-248">雖然資源狀態會跨所有計算和3D 佇列共用，但不允許在不同佇列上同時寫入資源。</span><span class="sxs-lookup"><span data-stu-id="66912-248">Although resource state is shared across all Compute and 3D queues, it is not permitted to write to the resource simultaneously on different queues.</span></span> <span data-ttu-id="66912-249">這裡的「同時」表示未同步處理，請注意，在某些硬體上並不可能執行未同步執行。</span><span class="sxs-lookup"><span data-stu-id="66912-249">"Simultaneously" here means unsynchronized, noting unsynchronized execution is not possible on some hardware.</span></span> <span data-ttu-id="66912-250">適用下列規則。</span><span class="sxs-lookup"><span data-stu-id="66912-250">The following rules apply.</span></span>

    -   <span data-ttu-id="66912-251">一次只能有一個佇列寫入資源。</span><span class="sxs-lookup"><span data-stu-id="66912-251">Only one queue can write to a resource at a time.</span></span>
    -   <span data-ttu-id="66912-252">多個佇列可以從資源讀取，只要它們未讀取寫入器所修改的位元組 (讀取同時寫入的位元組會產生未定義的結果) 。</span><span class="sxs-lookup"><span data-stu-id="66912-252">Multiple queues can read from the resource as long as they don’t read the bytes being modified by the writer (reading bytes being simultaneously written produces undefined results).</span></span>
    -   <span data-ttu-id="66912-253">在寫入之前，必須先使用隔離來同步處理，另一個佇列可以讀取寫入的位元組或進行寫入存取。</span><span class="sxs-lookup"><span data-stu-id="66912-253">A fence must be used to synchronize after writing before another queue can read the written bytes or make any write access.</span></span>

-   <span data-ttu-id="66912-254">所呈現的背景緩衝區必須處於 Direct3D 12 \_ 資源 \_ 狀態的 \_ 一般狀態。</span><span class="sxs-lookup"><span data-stu-id="66912-254">Back buffers being presented must be in the Direct3D 12\_RESOURCE\_STATE\_COMMON state.</span></span> 

## <a name="related-topics"></a><span data-ttu-id="66912-255">相關主題</span><span class="sxs-lookup"><span data-stu-id="66912-255">Related topics</span></span>

[<span data-ttu-id="66912-256">Direct3D 12 程式設計指南</span><span class="sxs-lookup"><span data-stu-id="66912-256">Direct3D 12 programming guide</span></span>](directx-12-programming-guide.md)

[<span data-ttu-id="66912-257">在 Direct3D 12 中使用資源阻礙來同步處理資源狀態</span><span class="sxs-lookup"><span data-stu-id="66912-257">Using resource barriers to synchronize resource states in Direct3D 12</span></span>](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md)

[<span data-ttu-id="66912-258">Direct3D 12 中的記憶體管理</span><span class="sxs-lookup"><span data-stu-id="66912-258">Memory management in Direct3D 12</span></span>](memory-management.md)
