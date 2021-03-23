---
title: 描述元堆積總覽
description: 描述元堆積包含許多不屬於管線狀態物件的物件類型 (PSO) ，例如著色器資源查看 (SRVs) 、未排序的存取視圖 (UAVs) 、常數緩衝區視圖 (CBVs) 和取樣器。
ms.assetid: 14561E77-44E0-4A58-8456-F40D59ECA175
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8bf720ebb71d016457fa4383a8d33aa62e2eee4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104444"
---
# <a name="descriptor-heaps-overview"></a><span data-ttu-id="3fb39-103">描述元堆積總覽</span><span class="sxs-lookup"><span data-stu-id="3fb39-103">Descriptor Heaps Overview</span></span>

<span data-ttu-id="3fb39-104">描述元堆積包含許多不屬於管線狀態物件的物件類型 (PSO) ，例如著色器資源查看 (SRVs) 、未排序的存取視圖 (UAVs) 、常數緩衝區視圖 (CBVs) 和取樣器。</span><span class="sxs-lookup"><span data-stu-id="3fb39-104">Descriptor heaps contain many object types that are not part of a Pipeline State Object (PSO), such as Shader Resource Views (SRVs), Unordered Access Views (UAVs), Constant Buffer Views (CBVs), and Samplers.</span></span>

-   [<span data-ttu-id="3fb39-105">描述元堆積的用途</span><span class="sxs-lookup"><span data-stu-id="3fb39-105">The Purpose of Descriptor Heaps</span></span>](#the-purpose-of-descriptor-heaps)
-   [<span data-ttu-id="3fb39-106">同步處理</span><span class="sxs-lookup"><span data-stu-id="3fb39-106">Synchronization</span></span>](#synchronization)
-   [<span data-ttu-id="3fb39-107">繫結</span><span class="sxs-lookup"><span data-stu-id="3fb39-107">Binding</span></span>](#binding)
-   [<span data-ttu-id="3fb39-108">切換堆積</span><span class="sxs-lookup"><span data-stu-id="3fb39-108">Switching heaps</span></span>](#switching-heaps)
-   [<span data-ttu-id="3fb39-109">束</span><span class="sxs-lookup"><span data-stu-id="3fb39-109">Bundles</span></span>](#bundles)
-   [<span data-ttu-id="3fb39-110">管理</span><span class="sxs-lookup"><span data-stu-id="3fb39-110">Management</span></span>](#management)
-   [<span data-ttu-id="3fb39-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="3fb39-111">Related topics</span></span>](#related-topics)

## <a name="the-purpose-of-descriptor-heaps"></a><span data-ttu-id="3fb39-112">描述元堆積的用途</span><span class="sxs-lookup"><span data-stu-id="3fb39-112">The Purpose of Descriptor Heaps</span></span>

<span data-ttu-id="3fb39-113">描述元堆積的主要目的是要包含在轉譯時，儲存著色器所參考的物件類型之描述項規格規格的大量記憶體配置， (理想的轉譯或更) 的整個框架。</span><span class="sxs-lookup"><span data-stu-id="3fb39-113">The primary purpose of a descriptor heap is to encompass the bulk of memory allocation required for storing the descriptor specifications of object types that shaders reference for as large of a window of rendering as possible (ideally an entire frame of rendering or more).</span></span> <span data-ttu-id="3fb39-114">如果應用程式正在切換管線從 API 快速看到的材質，描述項堆積中必須有空格，才能針對每個所需的狀態集合，即時定義描述中繼資料表。</span><span class="sxs-lookup"><span data-stu-id="3fb39-114">If an application is switching which textures the pipeline sees rapidly from the API, there has to be space in the descriptor heap to define descriptor tables on the fly for every set of state needed.</span></span> <span data-ttu-id="3fb39-115">例如，如果在另一個物件中再次使用資源，則應用程式可以選擇重複使用定義，或只在切換不同物件類型時依序指派堆積空間。</span><span class="sxs-lookup"><span data-stu-id="3fb39-115">The application can choose to reuse definitions if the resources are used again in another object, for example, or just assign the heap space sequentially as it switches various object types.</span></span>

<span data-ttu-id="3fb39-116">描述元堆積也允許個別的軟體元件分別管理描述項儲存。</span><span class="sxs-lookup"><span data-stu-id="3fb39-116">Descriptor heaps also allow individual software components to manage descriptor storage separately from each other.</span></span>

<span data-ttu-id="3fb39-117">CPU 可以看到所有堆積。</span><span class="sxs-lookup"><span data-stu-id="3fb39-117">All heaps are visible to the CPU.</span></span> <span data-ttu-id="3fb39-118">如果有任何) – write、回寫等等，應用程式也可以要求描述項堆積應該具有 (的 CPU 存取屬性。</span><span class="sxs-lookup"><span data-stu-id="3fb39-118">The application can also request which CPU access properties a descriptor heap should have (if any) – write combined, write back, and so on.</span></span> <span data-ttu-id="3fb39-119">應用程式可以視需要使用任何屬性來建立所需的描述項堆積數目。</span><span class="sxs-lookup"><span data-stu-id="3fb39-119">Apps can create as many descriptor heaps as desired with whatever properties are desired.</span></span> <span data-ttu-id="3fb39-120">應用程式一律會有選項，可讓您建立僅供未受限制之暫存用途的描述元堆積，並複製到視需要用於轉譯的描述元堆積。</span><span class="sxs-lookup"><span data-stu-id="3fb39-120">Apps always have the option to create descriptor heaps that are purely for staging purposes that are unconstrained in size, and copying to descriptor heaps that are used for rendering as necessary.</span></span>

<span data-ttu-id="3fb39-121">在相同的描述元堆積中，有一些限制。</span><span class="sxs-lookup"><span data-stu-id="3fb39-121">There are some restrictions in what can go in the same descriptor heap.</span></span> <span data-ttu-id="3fb39-122">CBV、UAV 和 SRV 專案可以位於相同的描述元堆積中。</span><span class="sxs-lookup"><span data-stu-id="3fb39-122">CBV, UAV and SRV entries can be in the same descriptor heap.</span></span> <span data-ttu-id="3fb39-123">不過，取樣器專案無法與 CBV、UAV 或 SRV 專案共用堆積。</span><span class="sxs-lookup"><span data-stu-id="3fb39-123">However, Samplers entries cannot share a heap with CBV, UAV or SRV entries.</span></span> <span data-ttu-id="3fb39-124">一般而言，有兩組描述項堆積，一個用於一般資源，第二個用於取樣器。</span><span class="sxs-lookup"><span data-stu-id="3fb39-124">Typically, there are two sets of descriptor heaps, one for the common resources and the second for Samplers.</span></span>

<span data-ttu-id="3fb39-125">使用 Direct3D 12 的描述項堆積時，會鏡像大部分的 GPU 硬體，也就是只需要在描述元堆積中存留描述項，或只在使用這些堆積時需要較少的定址位。</span><span class="sxs-lookup"><span data-stu-id="3fb39-125">The use of descriptor heaps by Direct3D 12 mirrors what most GPU hardware does, which is to either require descriptors live only in descriptor heaps, or simply that fewer addressing bits are needed if these heaps are used.</span></span> <span data-ttu-id="3fb39-126">Direct3D 12 的確需要使用描述元堆積，而且沒有任何選項可將描述項放在記憶體中的任何位置。</span><span class="sxs-lookup"><span data-stu-id="3fb39-126">Direct3D 12 does require the use of descriptor heaps, there is no option to put descriptors anywhere in memory.</span></span>

<span data-ttu-id="3fb39-127">描述元堆積只能由 CPU 立即進行編輯，而且沒有任何選項可依 GPU 編輯描述元堆積。</span><span class="sxs-lookup"><span data-stu-id="3fb39-127">Descriptor heaps can only be edited immediately by the CPU, there is no option to edit a descriptor heap by the GPU.</span></span>

## <a name="synchronization"></a><span data-ttu-id="3fb39-128">同步處理</span><span class="sxs-lookup"><span data-stu-id="3fb39-128">Synchronization</span></span>

<span data-ttu-id="3fb39-129">描述元堆積內容可以在記錄參考它的命令清單之前、期間和之後變更。</span><span class="sxs-lookup"><span data-stu-id="3fb39-129">Descriptor heap contents can be changed before, during and after recording command lists that reference it.</span></span> <span data-ttu-id="3fb39-130">不過，當提交要執行的命令清單可能會參考該位置時，無法變更描述項，因為這樣可能會叫用競爭條件。</span><span class="sxs-lookup"><span data-stu-id="3fb39-130">However, descriptors cannot be changed while a command list submitted for execution might reference that location, as this could invoke a race condition.</span></span>

## <a name="binding"></a><span data-ttu-id="3fb39-131">繫結</span><span class="sxs-lookup"><span data-stu-id="3fb39-131">Binding</span></span>

<span data-ttu-id="3fb39-132">最多一次只能系結一個 CBV/SRV/UAV 合併堆積和一個取樣器堆積。</span><span class="sxs-lookup"><span data-stu-id="3fb39-132">At most one CBV/SRV/UAV combined heap and one Sampler heap can be bound at any one time.</span></span> <span data-ttu-id="3fb39-133">這些堆積會在圖形和計算管線之間共用 (在其 Pso) 中所述。</span><span class="sxs-lookup"><span data-stu-id="3fb39-133">These heaps are shared between both the graphics and compute pipelines (described in their PSOs).</span></span>

## <a name="switching-heaps"></a><span data-ttu-id="3fb39-134">切換堆積</span><span class="sxs-lookup"><span data-stu-id="3fb39-134">Switching heaps</span></span>

<span data-ttu-id="3fb39-135">應用程式可接受使用 [**SetDescriptorHeaps**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps) 和 [**重設**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset) api，在相同的命令清單中或在不同的範圍內切換堆積。</span><span class="sxs-lookup"><span data-stu-id="3fb39-135">It is acceptable for an application to switch heaps within the same command list or in different ones using the [**SetDescriptorHeaps**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps) and [**Reset**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset) APIs.</span></span> <span data-ttu-id="3fb39-136">在某些硬體上，這可能是昂貴的作業，需要 GPU 延遲才能排清相依于目前系結描述項堆積的所有工作。</span><span class="sxs-lookup"><span data-stu-id="3fb39-136">On some hardware, this can be an expensive operation, requiring a GPU stall to flush all work that depends on the currently bound descriptor heap.</span></span> <span data-ttu-id="3fb39-137">如此一來，如果必須變更描述元堆積，則應用程式應該在 GPU 工作負載相對較淺時嘗試這麼做，這可能會限制命令清單的開頭變更。</span><span class="sxs-lookup"><span data-stu-id="3fb39-137">As a result, if descriptor heaps must be changed, applications should try to do so when the GPU workload is relatively light, perhaps limiting changes to the start of a command list.</span></span>

## <a name="bundles"></a><span data-ttu-id="3fb39-138">束</span><span class="sxs-lookup"><span data-stu-id="3fb39-138">Bundles</span></span>

<span data-ttu-id="3fb39-139">使用套件組合時，只能呼叫 [**SetDescriptorHeaps**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps) 方法，而描述項堆積集合必須完全符合呼叫組合的命令清單。</span><span class="sxs-lookup"><span data-stu-id="3fb39-139">With bundles there can only be one call to the [**SetDescriptorHeaps**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps) method, and the descriptor heaps set must match exactly those of the command list calling the bundle.</span></span> <span data-ttu-id="3fb39-140">如果組合未變更描述中繼資料表，則不需要設定描述元堆積。</span><span class="sxs-lookup"><span data-stu-id="3fb39-140">If the bundle does not change descriptor tables, it does not need to set the descriptor heaps.</span></span>

<span data-ttu-id="3fb39-141">如需無法搭配配套使用的 API 呼叫清單，請參閱 [建立和錄製命令清單和](recording-command-lists-and-bundles.md)組合。</span><span class="sxs-lookup"><span data-stu-id="3fb39-141">For a list of API calls that cannot be used with bundles, refer to [Creating and Recording Command Lists and Bundles](recording-command-lists-and-bundles.md).</span></span>

## <a name="management"></a><span data-ttu-id="3fb39-142">管理性</span><span class="sxs-lookup"><span data-stu-id="3fb39-142">Management</span></span>

<span data-ttu-id="3fb39-143">若要轉譯場景中的所有物件，將需要許多描述項，而且可以遵循一些不同的管理原則。</span><span class="sxs-lookup"><span data-stu-id="3fb39-143">To render all of the objects in a scene, many descriptors will be needed, and there are some different management strategies that can be followed.</span></span>

<span data-ttu-id="3fb39-144">最基本的策略是將下一個繪製呼叫的所有需求填入描述項堆積的新區域。</span><span class="sxs-lookup"><span data-stu-id="3fb39-144">The most basic strategy would be to fill in a fresh area of the descriptor heap with all of the requirements for the next draw call.</span></span> <span data-ttu-id="3fb39-145">因此，在對命令清單發出 draw 呼叫之前，會將描述項資料表指標設定為剛填入資料表的開頭。</span><span class="sxs-lookup"><span data-stu-id="3fb39-145">So, just before issuing the draw call on the command list, a descriptor table pointer would be set to the start of the freshly populated table.</span></span> <span data-ttu-id="3fb39-146">好處是，不需要記錄任何特定描述項在堆積中的位置。</span><span class="sxs-lookup"><span data-stu-id="3fb39-146">The upside is that there is no need to record where any particular descriptor is in the heap.</span></span>

<span data-ttu-id="3fb39-147">這項策略的缺點是，描述項堆積中可能會有很多重複的描述項，特別是當轉譯非常類似的場景時，以及將會快速使用描述項堆積空間的情況。</span><span class="sxs-lookup"><span data-stu-id="3fb39-147">The downside to this strategy is that there could be a lot of repetition of descriptors in the descriptor heap, especially when a very similar scene is being rendered, and that descriptor heap space is going to be used up quickly.</span></span> <span data-ttu-id="3fb39-148">針對在 GPU 上轉譯的描述元堆積，以及由 CPU 記錄的描述元堆積，可能需要避免發生衝突。</span><span class="sxs-lookup"><span data-stu-id="3fb39-148">Separate descriptor heaps for those being rendered on the GPU and for those being recorded by the CPU, would probably be necessary to avoid conflict.</span></span> <span data-ttu-id="3fb39-149">或者，您也可以使用子配置系統。</span><span class="sxs-lookup"><span data-stu-id="3fb39-149">Alternatively a sub-allocation system could be used.</span></span>

<span data-ttu-id="3fb39-150">此外，您可以藉由從下一次的繪製呼叫中仔細使用重迭的描述中繼資料表，以進一步優化基本系統，如此就只會加入所需的新描述項。</span><span class="sxs-lookup"><span data-stu-id="3fb39-150">Also, the basic system could be further optimized by careful use of overlapping descriptor tables from one draw call to the next, so that only the new descriptors required are added.</span></span>

<span data-ttu-id="3fb39-151">相較于基本的策略，更有效率的策略是預先填入描述項堆積，其中包含物件 (或資料) 的描述項，這些都是場景的一部分。</span><span class="sxs-lookup"><span data-stu-id="3fb39-151">A more efficient strategy than the basic one would be to pre-fill descriptor heaps with descriptors required for the objects (or materials) that are known to be part of the scene.</span></span> <span data-ttu-id="3fb39-152">此處的概念是，只有在繪製時才需要設定描述中繼資料表，因為描述項堆積會預先填入。</span><span class="sxs-lookup"><span data-stu-id="3fb39-152">The idea here is that it is only necessary to set the descriptor table at draw time, as the descriptor heap is populated ahead of time.</span></span>

<span data-ttu-id="3fb39-153">預先填入策略的變化是將描述元堆積視為一個大型陣列，包含固定已知位置中的所有必要描述項。</span><span class="sxs-lookup"><span data-stu-id="3fb39-153">A variation of the pre-filling strategy is to treat the descriptor heap as one huge array, containing all the required descriptors in fixed known locations.</span></span> <span data-ttu-id="3fb39-154">然後，繪製呼叫只需要接收一組常數，也就是需要使用描述項的陣列中的索引。</span><span class="sxs-lookup"><span data-stu-id="3fb39-154">Then the draw call needs only to receive a set of constants which are the indices into the array of where the descriptors are that need to be used.</span></span>

<span data-ttu-id="3fb39-155">進一步的優化是確保根常數和根描述元包含最常變更的，而不是將常數放置於描述元堆積中。</span><span class="sxs-lookup"><span data-stu-id="3fb39-155">A further optimization is to ensure root constants and root descriptors contain those that change most frequently, rather than place constants in the descriptor heap.</span></span> <span data-ttu-id="3fb39-156">在大部分的硬體中，這是處理常數的有效方式。</span><span class="sxs-lookup"><span data-stu-id="3fb39-156">For most hardware this is an efficient way of handling constants.</span></span>

<span data-ttu-id="3fb39-157">在實務上，圖形引擎可能會在不同的情況下使用不同的策略，並結合每個策略的元素，以符合特定的繪圖需求。</span><span class="sxs-lookup"><span data-stu-id="3fb39-157">In practice a graphics engine might use a different strategy in different situations, and combine elements of each strategy to suit the particular drawing requirements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3fb39-158">相關主題</span><span class="sxs-lookup"><span data-stu-id="3fb39-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3fb39-159">描述元堆積</span><span class="sxs-lookup"><span data-stu-id="3fb39-159">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> </dl>

 

 




