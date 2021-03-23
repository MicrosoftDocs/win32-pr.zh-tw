---
title: Direct3D 12 詞彙
description: 這些詞彙是 Direct3D 12 的特色。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 46B0F055-7E4F-4F8D-9915-3D195FD695B7
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a84b4b2e5a993b33b4c322b91682c8f9b5499bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548447"
---
# <a name="direct3d-12-glossary"></a><span data-ttu-id="28821-103">Direct3D 12 詞彙</span><span class="sxs-lookup"><span data-stu-id="28821-103">Direct3D 12 glossary</span></span>

<span data-ttu-id="28821-104">這些詞彙是 Direct3D 12 的特色。</span><span class="sxs-lookup"><span data-stu-id="28821-104">These terms are distinctive of Direct3D 12.</span></span>

<dl> <dt>

<span data-ttu-id="28821-105"><span id="direct3d12.directx_12_glossary_binding"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BINDING"></span>**綁定**</span><span class="sxs-lookup"><span data-stu-id="28821-105"><span id="direct3d12.directx_12_glossary_binding"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BINDING"></span>**binding**</span></span>
</dt> <dd>

<span data-ttu-id="28821-106">將記憶體連接至圖形管線的程式。</span><span class="sxs-lookup"><span data-stu-id="28821-106">The process of attaching memory to the graphics pipeline.</span></span> <span data-ttu-id="28821-107">例如，資源系結牽涉到將材質之類的資源系結至管線，以用於呈現物件。</span><span class="sxs-lookup"><span data-stu-id="28821-107">Resource binding, for example, involves the binding of a resource such as a texture to the pipeline, for use in rendering an object.</span></span>

</dd> <dt>

<span data-ttu-id="28821-108"><span id="direct3d12.directx_12_glossary_buffer"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BUFFER"></span>**緩衝區**</span><span class="sxs-lookup"><span data-stu-id="28821-108"><span id="direct3d12.directx_12_glossary_buffer"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BUFFER"></span>**buffer**</span></span>
</dt> <dd>

<span data-ttu-id="28821-109">D3D 資源的類型，與連續的記憶體配置同義。</span><span class="sxs-lookup"><span data-stu-id="28821-109">A type of D3D resource that is synonymous with a contiguous memory allocation.</span></span>

</dd> <dt>

<span data-ttu-id="28821-110"><span id="direct3d12.directx_12_glossary_bundle"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BUNDLE"></span>**束**</span><span class="sxs-lookup"><span data-stu-id="28821-110"><span id="direct3d12.directx_12_glossary_bundle"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BUNDLE"></span>**bundle**</span></span>
</dt> <dd>

<span data-ttu-id="28821-111">圖形處理單位 (GPU) 的命令緩衝區只能透過 *直接命令清單* 來執行。</span><span class="sxs-lookup"><span data-stu-id="28821-111">A command buffer that the graphics processing unit (GPU) can execute only directly via a *direct command list*.</span></span> <span data-ttu-id="28821-112">組合會繼承所有 GPU 狀態 (但目前設定的 *管線狀態物件* 和基本拓撲) 除外。</span><span class="sxs-lookup"><span data-stu-id="28821-112">A bundle inherits all GPU state (except for the currently set *pipeline state object* and primitive topology).</span></span>

</dd> <dt>

<span data-ttu-id="28821-113"><span id="direct3d12.directx_12_glossary_command_allocator"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_ALLOCATOR"></span>**命令配置器**</span><span class="sxs-lookup"><span data-stu-id="28821-113"><span id="direct3d12.directx_12_glossary_command_allocator"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_ALLOCATOR"></span>**command allocator**</span></span>
</dt> <dd>

<span data-ttu-id="28821-114">儲存 GPU 命令的基礎記憶體配置。</span><span class="sxs-lookup"><span data-stu-id="28821-114">The underlying memory allocations in which GPU commands are stored.</span></span> <span data-ttu-id="28821-115">命令配置器 *物件同時適用* 于 *直接命令清單* 和組合。</span><span class="sxs-lookup"><span data-stu-id="28821-115">The command allocator object applies to both *direct command lists* and *bundles*.</span></span>

</dd> <dt>

<span data-ttu-id="28821-116"><span id="direct3d12.directx_12_glossary_command_list"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_LIST"></span>**命令清單**</span><span class="sxs-lookup"><span data-stu-id="28821-116"><span id="direct3d12.directx_12_glossary_command_list"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_LIST"></span>**command list**</span></span>
</dt> <dd>

<span data-ttu-id="28821-117">命令清單會對應至 GPU 執行的一組命令。</span><span class="sxs-lookup"><span data-stu-id="28821-117">A command list corresponds to a set of commands which the GPU executes.</span></span> <span data-ttu-id="28821-118">這些包括設定狀態、繪製、清除和複製等命令。</span><span class="sxs-lookup"><span data-stu-id="28821-118">These include commands such as to set state, draw, clear, and copy.</span></span> <span data-ttu-id="28821-119">D3D12 命令清單介面明顯不同于 D3D11 命令清單介面。</span><span class="sxs-lookup"><span data-stu-id="28821-119">The D3D12 command list interface is significantly different than the D3D11 command list interface.</span></span> <span data-ttu-id="28821-120">D3D12 命令清單介面包含類似于 D3D11 裝置內容轉譯 Api 的 Api。</span><span class="sxs-lookup"><span data-stu-id="28821-120">The D3D12 command list interface contains APIs similar to the D3D11 device context rendering APIs.</span></span>

<span data-ttu-id="28821-121">D3D12 命令清單不會對應或取消對應資源、變更磚對應、調整磚集區大小、取得查詢資料，也不會以隱含方式將命令提交至 GPU 進行執行。</span><span class="sxs-lookup"><span data-stu-id="28821-121">A D3D12 command list does not map or unmap resources, change tile mappings, resize tile pools, get query data, nor does it ever implicitly submit commands to the GPU for execution.</span></span>

<span data-ttu-id="28821-122">不同于 D3D11 延遲的內容，D3D12 命令清單只支援兩個層級的間接取值。</span><span class="sxs-lookup"><span data-stu-id="28821-122">Unlike D3D11 deferred contexts, D3D12 command lists only support two levels of indirection.</span></span> <span data-ttu-id="28821-123">*直接命令清單* 對應至 GPU 可執行檔命令緩衝區。</span><span class="sxs-lookup"><span data-stu-id="28821-123">A *direct command list* corresponds to a command buffer which the GPU can execute.</span></span> <span data-ttu-id="28821-124">組合 *只能透過* 直接命令清單來執行。</span><span class="sxs-lookup"><span data-stu-id="28821-124">A *bundle* can be executed only directly via a direct command list.</span></span>

<span data-ttu-id="28821-125">直接命令清單不會繼承任何 GPU 狀態。</span><span class="sxs-lookup"><span data-stu-id="28821-125">A direct command list does not inherit any GPU state.</span></span> <span data-ttu-id="28821-126">組合會繼承所有 GPU 狀態 (但目前設定的管線狀態物件和基本拓撲) 除外。</span><span class="sxs-lookup"><span data-stu-id="28821-126">A bundle inherits all GPU state (except for the currently set pipeline state object and primitive topology).</span></span>

<span data-ttu-id="28821-127">命令配置器會設定命令清單的記憶體 *。*</span><span class="sxs-lookup"><span data-stu-id="28821-127">Memory for a command list is set by the *command allocator*.</span></span> <span data-ttu-id="28821-128">命令清單的目的是它們可以提交至 GPU 作為單一轉譯要求。</span><span class="sxs-lookup"><span data-stu-id="28821-128">The purpose of command lists is that they can be submitted to a GPU as a single rendering request.</span></span>

</dd> <dt>

<span data-ttu-id="28821-129"><span id="direct3d12.directx_12_glossary_command_queue"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_QUEUE"></span>**命令佇列**</span><span class="sxs-lookup"><span data-stu-id="28821-129"><span id="direct3d12.directx_12_glossary_command_queue"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_QUEUE"></span>**command queue**</span></span>
</dt> <dd>

<span data-ttu-id="28821-130">GPU 會連續執行的 *命令清單* 佇列。</span><span class="sxs-lookup"><span data-stu-id="28821-130">A queue of *command lists* that the GPU executes in succession.</span></span> <span data-ttu-id="28821-131">應用程式必須明確地將 *命令清單* 提交到命令佇列以供執行。</span><span class="sxs-lookup"><span data-stu-id="28821-131">Applications must explicitly submit *command lists* to a command queue for execution.</span></span> <span data-ttu-id="28821-132">通常有三個命令佇列：3D 圖形、計算和複製，對應至 GPU 上的3D 圖形管線、計算引擎，以及一或多個複製引擎。</span><span class="sxs-lookup"><span data-stu-id="28821-132">Typically there are three command queues: 3D graphics, compute and copy, corresponding to the 3D graphics pipeline, the compute engine, and one or more copy engines, on the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="28821-133"><span id="direct3d12.directx_12_glossary_conservative_rasterization"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_CONSERVATIVE_RASTERIZATION"></span>**保守的點陣化**</span><span class="sxs-lookup"><span data-stu-id="28821-133"><span id="direct3d12.directx_12_glossary_conservative_rasterization"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_CONSERVATIVE_RASTERIZATION"></span>**conservative rasterization**</span></span>
</dt> <dd>

<span data-ttu-id="28821-134">保守的點陣化是適用于 Direct3D 圖形管線之轉譯器階段的操作模式。</span><span class="sxs-lookup"><span data-stu-id="28821-134">Conservative rasterization is a mode of operation for the rasterizer stage of the Direct3D graphics pipeline.</span></span> <span data-ttu-id="28821-135">它會停用標準以範例為基礎的點陣化，並改為以基本型別來點陣化任何數量所涵蓋的圖元。</span><span class="sxs-lookup"><span data-stu-id="28821-135">It disables the standard sample-based rasterization, and will instead rasterize a pixel that is covered by any amount by a primitive.</span></span> <span data-ttu-id="28821-136">其中一項重要的區別是，雖然任何涵蓋範圍都會產生柵格化圖元，但該涵蓋範圍不能以硬體為特性，因此涵蓋範圍一律會以二進位呈現給圖元著色器：完全涵蓋或未涵蓋。</span><span class="sxs-lookup"><span data-stu-id="28821-136">One important distinction is that, while any coverage at all produces a rasterized pixel, that coverage cannot be characterized by the hardware, so coverage always appears binary to a pixel shader: either fully covered or not covered.</span></span> <span data-ttu-id="28821-137">它會保留給圖元著色器程式碼，以 analytically 判斷實際的涵蓋範圍。</span><span class="sxs-lookup"><span data-stu-id="28821-137">It is left to the pixel shader code to analytically determine the actual coverage.</span></span>

<span data-ttu-id="28821-138">保守的點陣化有助於解決衝突和點擊偵測、分類收納和遮蔽剔除等問題，其中圖元的色彩更特定且可以消除邊緣案例。</span><span class="sxs-lookup"><span data-stu-id="28821-138">Conservative rasterization can help with such problems as collision and hit detection, binning, and occlusion culling, where the color of a pixel is more certain and edge cases can be eliminated.</span></span> <span data-ttu-id="28821-139">請參閱 [保守的光柵](conservative-rasterization.md)化。</span><span class="sxs-lookup"><span data-stu-id="28821-139">See [Conservative Rasterization](conservative-rasterization.md).</span></span>

</dd> <dt>

<span data-ttu-id="28821-140"><span id="direct3d12.directx_12_glossary_cbv"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_CBV"></span>**常數緩衝區視圖 (CBV)**</span><span class="sxs-lookup"><span data-stu-id="28821-140"><span id="direct3d12.directx_12_glossary_cbv"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_CBV"></span>**Constant Buffer View (CBV)**</span></span>
</dt> <dd>

<span data-ttu-id="28821-141">常數緩衝區包含著色器常數資料，例如相機視圖、投射矩陣和世界矩陣。</span><span class="sxs-lookup"><span data-stu-id="28821-141">Constant buffers contain shader constant data, such as a camera view, projection matrices, and world matrices.</span></span> <span data-ttu-id="28821-142">「常數緩衝區視圖」是圖形管線所見之緩衝區的格式特定視圖。</span><span class="sxs-lookup"><span data-stu-id="28821-142">A "constant buffer view" is the format-specific view of the buffer as seen by the graphics pipeline.</span></span>

</dd> <dt>

<span data-ttu-id="28821-143"><span id="direct3d12.directx_12_glossary_default_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DEFAULT_HEAP"></span>**預設堆積**</span><span class="sxs-lookup"><span data-stu-id="28821-143"><span id="direct3d12.directx_12_glossary_default_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DEFAULT_HEAP"></span>**default heap**</span></span>
</dt> <dd>

<span data-ttu-id="28821-144">使用者模式堆積，著重于支援持續性 GPU 資源類型，包括 GPU 寫入的資源。</span><span class="sxs-lookup"><span data-stu-id="28821-144">A user-mode heap that is focused on supporting persistent GPU resource types, including GPU-written resources.</span></span>

</dd> <dt>

<span data-ttu-id="28821-145"><span id="direct3d12.directx_12_glossary_descriptor"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR"></span>**描述 符**</span><span class="sxs-lookup"><span data-stu-id="28821-145"><span id="direct3d12.directx_12_glossary_descriptor"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR"></span>**descriptor**</span></span>
</dt> <dd>

<span data-ttu-id="28821-146">描述項是 D3D12 中單一資源的系結主要單位。</span><span class="sxs-lookup"><span data-stu-id="28821-146">Descriptors are the primary unit of binding for a single resource in D3D12.</span></span> <span data-ttu-id="28821-147">描述項是相當小的資料區塊，可完整描述 gpu 特定格式的 GPU 物件。</span><span class="sxs-lookup"><span data-stu-id="28821-147">A descriptor is a relatively small block of data that fully describes an object to the GPU, in a GPU specific format.</span></span> <span data-ttu-id="28821-148">有許多不同類型的描述項：著色器資源檢視 (SRVs) 、未排序的存取視圖 (UAVs) 、常數緩衝區視圖 (CBVs) 和取樣器是一些範例。</span><span class="sxs-lookup"><span data-stu-id="28821-148">There are many different types of descriptors: Shader Resource Views (SRVs), Unordered Access Views (UAVs), Constant Buffer Views (CBVs), and Samplers are a few examples.</span></span>

</dd> <dt>

<span data-ttu-id="28821-149"><span id="direct3d12.directx_12_glossary_descriptor_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR_HEAP"></span>**描述元堆積**</span><span class="sxs-lookup"><span data-stu-id="28821-149"><span id="direct3d12.directx_12_glossary_descriptor_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR_HEAP"></span>**descriptor heap**</span></span>
</dt> <dd>

<span data-ttu-id="28821-150">描述元堆積是描述項連續配置的集合，每個描述項的一個配置。</span><span class="sxs-lookup"><span data-stu-id="28821-150">A descriptor heap is a collection of contiguous allocations of descriptors, one allocation for every descriptor.</span></span> <span data-ttu-id="28821-151">描述元堆積的主要點是為了將著色器參考最大的物件類型描述項規格，儲存在轉譯時所需的大量記憶體配置， (理想的轉譯或更) 的整個框架。</span><span class="sxs-lookup"><span data-stu-id="28821-151">The primary point of a descriptor heap is to encompass the bulk of memory allocation required for storing the descriptor specifications of object types that shaders reference for as large of a window of rendering as possible (ideally an entire frame of rendering or more).</span></span>

</dd> <dt>

<span data-ttu-id="28821-152"><span id="direct3d12.directx_12_glossary_descriptor_table"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR_TABLE"></span>**描述項資料表**</span><span class="sxs-lookup"><span data-stu-id="28821-152"><span id="direct3d12.directx_12_glossary_descriptor_table"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR_TABLE"></span>**descriptor table**</span></span>
</dt> <dd>

<span data-ttu-id="28821-153">描述項資料表在邏輯上是描述項的陣列。</span><span class="sxs-lookup"><span data-stu-id="28821-153">A descriptor table is logically an array of descriptors.</span></span> <span data-ttu-id="28821-154">每個描述中繼資料表都會儲存一或多個類型的描述項，包括 SRVs、UAVe、CBVs 和取樣器。</span><span class="sxs-lookup"><span data-stu-id="28821-154">Each descriptor table stores descriptors of one or more types, including SRVs, UAVe, CBVs, and Samplers.</span></span> <span data-ttu-id="28821-155">描述項資料表不是記憶體的配置，它只是描述項堆積中的位移和長度。</span><span class="sxs-lookup"><span data-stu-id="28821-155">A descriptor table is not an allocation of memory, it is simply an offset and length into a descriptor heap.</span></span>

</dd> <dt>

<span data-ttu-id="28821-156"><span id="direct3d12.directx_12_glossary_direct_command_list"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DIRECT_COMMAND_LIST"></span>**直接命令清單**</span><span class="sxs-lookup"><span data-stu-id="28821-156"><span id="direct3d12.directx_12_glossary_direct_command_list"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DIRECT_COMMAND_LIST"></span>**direct command list**</span></span>
</dt> <dd>

<span data-ttu-id="28821-157">GPU 可執行檔命令緩衝區。</span><span class="sxs-lookup"><span data-stu-id="28821-157">A command buffer that the GPU can execute.</span></span> <span data-ttu-id="28821-158">直接命令清單不會繼承任何 GPU 狀態。</span><span class="sxs-lookup"><span data-stu-id="28821-158">A direct command list doesn't inherit any GPU state.</span></span>

</dd> <dt>

<span data-ttu-id="28821-159"><span id="direct3d12.directx_12_glossary_fence"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_FENCE"></span>**柵欄**</span><span class="sxs-lookup"><span data-stu-id="28821-159"><span id="direct3d12.directx_12_glossary_fence"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_FENCE"></span>**fence**</span></span>
</dt> <dd>

<span data-ttu-id="28821-160">用來同步處理 GPU 和 CPU 的機制。</span><span class="sxs-lookup"><span data-stu-id="28821-160">A mechanism to synchronize the GPU and CPU.</span></span> <span data-ttu-id="28821-161">您可以指示 GPU 和 CPU 等待範圍，等候其他處理器趕上的作用。</span><span class="sxs-lookup"><span data-stu-id="28821-161">Both the GPU and CPU can be instructed to wait at a fence, waiting in effect for the other processor to catch up.</span></span> <span data-ttu-id="28821-162">請參閱 [多重引擎同步](./user-mode-heap-synchronization.md)處理。</span><span class="sxs-lookup"><span data-stu-id="28821-162">See [Multi-engine synchronization](./user-mode-heap-synchronization.md).</span></span>

</dd> <dt>

<span data-ttu-id="28821-163"><span id="direct3d12.directx_12_glossary_hazard"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_HAZARD"></span>**危險，危險追蹤**</span><span class="sxs-lookup"><span data-stu-id="28821-163"><span id="direct3d12.directx_12_glossary_hazard"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_HAZARD"></span>**hazard, hazard tracking**</span></span>
</dt> <dd>

<span data-ttu-id="28821-164">當資源已用於一個用途，且應用程式打算將它用於其他用途時，會發生危險。</span><span class="sxs-lookup"><span data-stu-id="28821-164">A hazard occurs when a resource has been used for one purpose, and the app intends to reuse it for another purpose.</span></span> <span data-ttu-id="28821-165">若要再次使用資源，必須將中繼快取排清或失效，壓縮需求必須與第二次使用一致，而且資源應該處於所需的狀態，以避免在寫入資源之後讀取資源，並基於預期目的而使其失效。</span><span class="sxs-lookup"><span data-stu-id="28821-165">In order to use the resource again, intermediate caches will need to be flushed or invalidated, compression requirements will need to be consistent with the second use, and the resource should be in the required state to avoid reading the resource after it has been written to and invalidated for the intended purpose.</span></span>

<span data-ttu-id="28821-166">維護資源和避免這些同步處理問題的程式稱為「危險追蹤」。</span><span class="sxs-lookup"><span data-stu-id="28821-166">The process of maintaining resources and avoiding these sync issues is known as hazard tracking.</span></span> <span data-ttu-id="28821-167">如果驅動程式沒有風險追蹤，則應用程式會負責這項工作。</span><span class="sxs-lookup"><span data-stu-id="28821-167">If there is no hazard tracking by the driver, then the app is responsible for this.</span></span> <span data-ttu-id="28821-168">在大部分舊版的 DirectX 中，風險追蹤是由驅動程式處理。</span><span class="sxs-lookup"><span data-stu-id="28821-168">In most earlier versions of DirectX, hazard tracking was handled by the driver.</span></span> <span data-ttu-id="28821-169">為了改善效能，DirectX 12 提供沒有危險追蹤的方法。</span><span class="sxs-lookup"><span data-stu-id="28821-169">To improve performance, methods without hazard tracking are available in DirectX 12.</span></span>

</dd> <dt>

<span data-ttu-id="28821-170"><span id="direct3d12.directx_12_glossary_hlsl"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_HLSL"></span>**高階著色器語言 (HLSL)**</span><span class="sxs-lookup"><span data-stu-id="28821-170"><span id="direct3d12.directx_12_glossary_hlsl"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_HLSL"></span>**High-Level Shader Language (HLSL)**</span></span>
</dt> <dd>

<span data-ttu-id="28821-171">一種電腦語言，類似于 C 的許多方式，用於撰寫著色器程式碼。</span><span class="sxs-lookup"><span data-stu-id="28821-171">A computer language, similar but distinct in many ways from C, that is used to write shader code.</span></span> <span data-ttu-id="28821-172">頂點、圖元、幾何、計算、網域和輪廓著色器全都使用 HLSL 撰寫。</span><span class="sxs-lookup"><span data-stu-id="28821-172">Vertex, pixel, geometry, compute, domain, and hull shaders are all written using HLSL.</span></span> <span data-ttu-id="28821-173">編譯器會將 HLSL 來源轉換成二進位格式，以供 GPU 取用。</span><span class="sxs-lookup"><span data-stu-id="28821-173">A compiler converts the HLSL source into a binary format for the GPU to consume.</span></span>

</dd> <dt>

<span data-ttu-id="28821-174"><span id="direct3d12.directx_12_glossary_multiengine"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_MULTIENGINE"></span>**multiengine**</span><span class="sxs-lookup"><span data-stu-id="28821-174"><span id="direct3d12.directx_12_glossary_multiengine"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_MULTIENGINE"></span>**multiengine**</span></span>
</dt> <dd>

<span data-ttu-id="28821-175">單一 GPU 中不同的引擎實例和類型。</span><span class="sxs-lookup"><span data-stu-id="28821-175">The different instances and types of engines in a single GPU.</span></span> <span data-ttu-id="28821-176">引擎的類型包括：圖形、計算和複製。</span><span class="sxs-lookup"><span data-stu-id="28821-176">The types of engines include: graphics, compute, and copy.</span></span>

</dd> <dt>

<span data-ttu-id="28821-177"><span id="direct3d12.directx_12_glossary_multigpu"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_MULTIGPU"></span>**MultiGPU**</span><span class="sxs-lookup"><span data-stu-id="28821-177"><span id="direct3d12.directx_12_glossary_multigpu"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_MULTIGPU"></span>**MultiGPU**</span></span>
</dt> <dd>

<span data-ttu-id="28821-178">一種硬體設定，其中有一個以上的圖形配接器。</span><span class="sxs-lookup"><span data-stu-id="28821-178">A hardware configuration where there is more than one graphics adapter.</span></span> <span data-ttu-id="28821-179">不同的介面卡有時也稱為節點。</span><span class="sxs-lookup"><span data-stu-id="28821-179">The separate adapters are sometimes referred to as nodes.</span></span> <span data-ttu-id="28821-180">擁有多個 Gpu 可以使其與 CPU 進行同步處理，而彼此的工作則比使用單一 GPU 更為複雜。</span><span class="sxs-lookup"><span data-stu-id="28821-180">Having multiple GPUs can make the task of synchronizing them with the CPU, and each other, considerably more complex than with a single GPU.</span></span>

</dd> <dt>

<span data-ttu-id="28821-181"><span id="direct3d12.directx_12_glossary_pipeline_state_object"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_PIPELINE_STATE_OBJECT"></span>**管線狀態物件 (PSO)**</span><span class="sxs-lookup"><span data-stu-id="28821-181"><span id="direct3d12.directx_12_glossary_pipeline_state_object"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_PIPELINE_STATE_OBJECT"></span>**Pipeline State object (PSO)**</span></span>
</dt> <dd>

<span data-ttu-id="28821-182">GPU 狀態的重要部分。</span><span class="sxs-lookup"><span data-stu-id="28821-182">A significant portion of the state of the GPU.</span></span> <span data-ttu-id="28821-183">此狀態包括目前設定的著色器和特定的固定函式狀態物件。</span><span class="sxs-lookup"><span data-stu-id="28821-183">This state includes all currently set shaders and certain fixed-function state objects.</span></span> <span data-ttu-id="28821-184">變更管線物件內所包含之狀態的唯一方式，就是變更目前系結的管線物件。</span><span class="sxs-lookup"><span data-stu-id="28821-184">The only way to change states contained within the pipeline object is to change the currently bound pipeline object.</span></span>

</dd> <dt>

<span data-ttu-id="28821-185"><span id="direct3d12.directx_12_glossary_predication"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_PREDICATION"></span>**預測**</span><span class="sxs-lookup"><span data-stu-id="28821-185"><span id="direct3d12.directx_12_glossary_predication"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_PREDICATION"></span>**predication**</span></span>
</dt> <dd>

<span data-ttu-id="28821-186">Predication 是一項功能，可啟用 GPU 而非 CPU 來決定不繪製、複製或分派物件。</span><span class="sxs-lookup"><span data-stu-id="28821-186">Predication is a feature that enables the GPU rather than the CPU to determine to not draw, copy or dispatch an object.</span></span> <span data-ttu-id="28821-187">比方說，如果物件的周框方塊是由另一個物件完全 pixels occluded，或是將物件減少為小於圖元的大小，則根本不會嘗試繪製隱藏的物件。</span><span class="sxs-lookup"><span data-stu-id="28821-187">For example, if a bounding box of an object is totally occluded by another object or perspective has reduced the object to less than the size of a pixel, there may be no point in attempting to draw the hidden object at all.</span></span> <span data-ttu-id="28821-188">請參閱 [Predication](predication.md)。</span><span class="sxs-lookup"><span data-stu-id="28821-188">See [Predication](predication.md).</span></span>

</dd> <dt>

<span data-ttu-id="28821-189"><span id="direct3d12.directx_12_glossary_rov"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_ROV"></span>**(ROV) 的轉譯器訂單視圖**</span><span class="sxs-lookup"><span data-stu-id="28821-189"><span id="direct3d12.directx_12_glossary_rov"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_ROV"></span>**Rasterizer Order View (ROV)**</span></span>
</dt> <dd>

<span data-ttu-id="28821-190">標準圖形管線可能無法正確地將多個包含透明度的材質組合在一起。</span><span class="sxs-lookup"><span data-stu-id="28821-190">Standard graphics pipelines may have trouble correctly compositing together multiple textures that contain transparency.</span></span> <span data-ttu-id="28821-191">網路圍牆、冒煙、火、植被指數和彩色玻璃等物件會使用透明效果來取得所需的效果。</span><span class="sxs-lookup"><span data-stu-id="28821-191">Objects such as wire fences, smoke, fire, vegetation, and colored glass use transparency to get the desired effect.</span></span> <span data-ttu-id="28821-192">如果多個包含透明度的材質 (在包含植被指數的半透明大樓前方的範圍前面，有多個材質出現問題，就會發生問題，例如) 。</span><span class="sxs-lookup"><span data-stu-id="28821-192">Problems arise when multiple textures that contain transparency are in line with each other (smoke in front of a fence in front of a glass building containing vegetation, as an example).</span></span> <span data-ttu-id="28821-193">以轉譯器排序的視圖 (ROVs) 啟用基礎順序獨立透明度 (OIT) 演算法來使用硬體的功能，以嘗試正確地解析透明度順序。</span><span class="sxs-lookup"><span data-stu-id="28821-193">Rasterizer ordered views (ROVs) enable the underlying Order Independent Transparency (OIT) algorithms to use features of the hardware to try to resolve the transparency order correctly.</span></span> <span data-ttu-id="28821-194">透明度是由圖元著色器所處理。</span><span class="sxs-lookup"><span data-stu-id="28821-194">Transparency is handled by the pixel shader.</span></span>

<span data-ttu-id="28821-195">以轉譯器排序的視圖 (ROVs) 允許圖元著色器程式碼將未排序的存取視圖標記 (UAV) 系結，以及改變 UAVs 圖形管線結果順序的一般需求。</span><span class="sxs-lookup"><span data-stu-id="28821-195">Rasterizer Ordered Views (ROVs) allow pixel shader code to mark Unordered Access View (UAV) bindings with a declaration that alters the normal requirements for the order of graphics pipeline results for UAVs.</span></span>

</dd> <dt>

<span data-ttu-id="28821-196"><span id="direct3d12.directx_12_glossary_readback_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_READBACK_HEAP"></span>**readback 堆積**</span><span class="sxs-lookup"><span data-stu-id="28821-196"><span id="direct3d12.directx_12_glossary_readback_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_READBACK_HEAP"></span>**readback heap**</span></span>
</dt> <dd>

<span data-ttu-id="28821-197">將焦點放在從 GPU 傳輸回 CPU 的資料的使用者模式堆積。</span><span class="sxs-lookup"><span data-stu-id="28821-197">A user-mode heap that is focused on data transfer from the GPU back to the CPU.</span></span>

</dd> <dt>

<span data-ttu-id="28821-198"><span id="direct3d12.directx_12_glossary_resource"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE"></span>**資源**</span><span class="sxs-lookup"><span data-stu-id="28821-198"><span id="direct3d12.directx_12_glossary_resource"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE"></span>**resource**</span></span>
</dt> <dd>

<span data-ttu-id="28821-199">提供資料給管線，並定義在場景中呈現內容的實體。</span><span class="sxs-lookup"><span data-stu-id="28821-199">An entity that provides data to the pipeline and defines what is rendered during your scene.</span></span> <span data-ttu-id="28821-200">從您的遊戲媒體載入或在執行階段動態建立資源。</span><span class="sxs-lookup"><span data-stu-id="28821-200">Resources can be loaded from your game media or created dynamically at run time.</span></span> <span data-ttu-id="28821-201">通常，資源包括紋理資料、頂點資料和著色器資料。</span><span class="sxs-lookup"><span data-stu-id="28821-201">Typically, resources include texture data, vertex data, and shader data.</span></span> <span data-ttu-id="28821-202">大部分的 Direct3D 應用程式會在其存留期內廣泛地建立和終結資源。</span><span class="sxs-lookup"><span data-stu-id="28821-202">Most Direct3D applications create and destroy resources extensively throughout their lifespan.</span></span>

</dd> <dt>

<span data-ttu-id="28821-203"><span id="direct3d12.directx_12_glossary_resource_barrier"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_BARRIER"></span>**資源屏障**</span><span class="sxs-lookup"><span data-stu-id="28821-203"><span id="direct3d12.directx_12_glossary_resource_barrier"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_BARRIER"></span>**resource barrier**</span></span>
</dt> <dd>

<span data-ttu-id="28821-204">資源關卡會通知驅動程式，可能需要對單一資源進行多個存取的同步處理，例如讀取和寫入相同的材質。</span><span class="sxs-lookup"><span data-stu-id="28821-204">A resource barrier notifies the driver that synchronization of multiple accesses to a single resource may be required, for example, reading and writing to the same texture.</span></span>

</dd> <dt>

<span data-ttu-id="28821-205"><span id="direct3d12.directx_12_glossary_resource_binding"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_BINDING"></span>**資源系結**</span><span class="sxs-lookup"><span data-stu-id="28821-205"><span id="direct3d12.directx_12_glossary_resource_binding"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_BINDING"></span>**resource binding**</span></span>
</dt> <dd>

<span data-ttu-id="28821-206">資源系結是將資源 (紋理、頂點緩衝區、索引緩衝區等) 上連結至圖形管線的程式，可讓管線的著色器處理正確的資源。</span><span class="sxs-lookup"><span data-stu-id="28821-206">Resource binding is the process of linking resources (textures, vertex buffers, index buffers, and so on), to the graphics pipeline, enabling the shaders of the pipeline to process the correct resource.</span></span>

</dd> <dt>

<span data-ttu-id="28821-207"><span id="direct3d12.directx_12_glossary_resource_heaps"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_HEAPS"></span>**資源堆積**</span><span class="sxs-lookup"><span data-stu-id="28821-207"><span id="direct3d12.directx_12_glossary_resource_heaps"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_HEAPS"></span>**resource heaps**</span></span>
</dt> <dd>

<span data-ttu-id="28821-208">資源堆積是堆積的一般詞彙，記憶體緩衝區會保留這些資源，因為它們會在 GPU 之間傳輸。</span><span class="sxs-lookup"><span data-stu-id="28821-208">Resource heaps is a generic term for the heaps that are memory buffers set aside to hold resources as they are transferred to and from the GPU.</span></span> <span data-ttu-id="28821-209">傳送至 GPU 需要一個上傳堆積，從 GPU 到 CPU 都需要 Readback 堆積，而 GPU 的持續性堆積會在多個轉譯畫面上維持，稱為預設堆積。</span><span class="sxs-lookup"><span data-stu-id="28821-209">A transfer to the GPU requires an Upload Heap, from the GPU to the CPU requires a Readback Heap, and a persistent heap for the GPU to maintain over multiple rendering frames is called a Default Heap.</span></span>

</dd> <dt>

<span data-ttu-id="28821-210"><span id="direct3d12.directx_12_glossary_root_signature"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_ROOT_SIGNATURE"></span>**根簽章**</span><span class="sxs-lookup"><span data-stu-id="28821-210"><span id="direct3d12.directx_12_glossary_root_signature"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_ROOT_SIGNATURE"></span>**root signature**</span></span>
</dt> <dd>

<span data-ttu-id="28821-211">根簽章會定義要系結至圖形或計算管線的所有資源。</span><span class="sxs-lookup"><span data-stu-id="28821-211">Root signatures define all the resources that are to be bound to the graphics, or compute, pipelines.</span></span> <span data-ttu-id="28821-212">根簽章是由應用程式設定，並將命令清單連結至著色器通常需要的資源，每個應用程式都有一個圖形和一個計算根簽章。</span><span class="sxs-lookup"><span data-stu-id="28821-212">A root signature is configured by the app and links command lists to the resources that the shaders require Typically, there is one graphics and one compute root signature per app.</span></span>

</dd> <dt>

<span data-ttu-id="28821-213"><span id="direct3d12.directx_12_glossary_sampler"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SAMPLER"></span>**採樣**</span><span class="sxs-lookup"><span data-stu-id="28821-213"><span id="direct3d12.directx_12_glossary_sampler"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SAMPLER"></span>**sampler**</span></span>
</dt> <dd>

<span data-ttu-id="28821-214">取樣器是從材質讀取的程式碼。</span><span class="sxs-lookup"><span data-stu-id="28821-214">A sampler is code that reads from a texture.</span></span>

</dd> <dt>

<span data-ttu-id="28821-215"><span id="direct3d12.directx_12_glossary_srv"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SRV"></span>**(SRV) 的著色器資源檢視**</span><span class="sxs-lookup"><span data-stu-id="28821-215"><span id="direct3d12.directx_12_glossary_srv"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SRV"></span>**Shader Resource View (SRV)**</span></span>
</dt> <dd>

<span data-ttu-id="28821-216">在著色器資源中查看資料的格式特定方式，例如紋理。</span><span class="sxs-lookup"><span data-stu-id="28821-216">A format-specific way to look at the data in a shader resource, such as a texture.</span></span>

</dd> <dt>

<span data-ttu-id="28821-217"><span id="direct3d12.directx_12_glossary_static_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_STATIC_HEAP"></span>**靜態堆積**</span><span class="sxs-lookup"><span data-stu-id="28821-217"><span id="direct3d12.directx_12_glossary_static_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_STATIC_HEAP"></span>**static heap**</span></span>
</dt> <dd>

<span data-ttu-id="28821-218">將焦點放在多個 GPU 唯讀資源的使用者模式堆積，通常會同時使用，且不會經常變更。</span><span class="sxs-lookup"><span data-stu-id="28821-218">A user-mode heap that is focused on multiple GPU-read-only resources that are typically used at the same time and are not changed frequently.</span></span>

</dd> <dt>

<span data-ttu-id="28821-219"><span id="direct3d12.directx_12_glossary_swap_chain"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SWAP_CHAIN"></span>**交換鏈**</span><span class="sxs-lookup"><span data-stu-id="28821-219"><span id="direct3d12.directx_12_glossary_swap_chain"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SWAP_CHAIN"></span>**swap chain**</span></span>
</dt> <dd>

<span data-ttu-id="28821-220">交換鏈會控制背景的緩衝區旋轉，形成圖形動畫的基礎。</span><span class="sxs-lookup"><span data-stu-id="28821-220">Swap chains control the back buffer rotation, forming the basis of graphics animation.</span></span> <span data-ttu-id="28821-221">交換鏈是由低層級的 API set DXGI 所處理 (請參閱 [DXGI 總覽](../direct3ddxgi/d3d10-graphics-programming-guide-dxgi.md)) 。</span><span class="sxs-lookup"><span data-stu-id="28821-221">Swap chains are handled by the low level API set DXGI (see [DXGI Overview](../direct3ddxgi/d3d10-graphics-programming-guide-dxgi.md)).</span></span>

</dd> <dt>

<span data-ttu-id="28821-222"><span id="direct3d12.directx_12_glossary_swizzle"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SWIZZLE"></span>**swizzle**</span><span class="sxs-lookup"><span data-stu-id="28821-222"><span id="direct3d12.directx_12_glossary_swizzle"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SWIZZLE"></span>**swizzle**</span></span>
</dt> <dd>

<span data-ttu-id="28821-223">在記憶體中找出多維度資料的技巧，讓鄰近維度的資料通常會有鄰近的位址。</span><span class="sxs-lookup"><span data-stu-id="28821-223">A technique of locating multidimensional data in memory such that data of nearby dimensionality tends to have nearby addresses.</span></span> <span data-ttu-id="28821-224">尤其是，一個資料列的所有資料，在下一個資料列的資料之前不會連續找出。</span><span class="sxs-lookup"><span data-stu-id="28821-224">In particular, all the data for one row is not located contiguously before the data for the next row.</span></span> <span data-ttu-id="28821-225">「參數化 Swizzle」描述描述 Swizzle 模式的標準化方式。</span><span class="sxs-lookup"><span data-stu-id="28821-225">A "Parameterized Swizzle" describes a standardized way to describe swizzle patterns.</span></span>

</dd> <dt>

<span data-ttu-id="28821-226"><span id="direct3d12.directx_12_glossary_static_texture"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_STATIC_TEXTURE"></span>**紋理**</span><span class="sxs-lookup"><span data-stu-id="28821-226"><span id="direct3d12.directx_12_glossary_static_texture"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_STATIC_TEXTURE"></span>**texture**</span></span>
</dt> <dd>

<span data-ttu-id="28821-227">一種類型的 D3D 資源，其為多維度，且具有已針對 GPU 的多維度存取優化的記憶體配置。</span><span class="sxs-lookup"><span data-stu-id="28821-227">A type of D3D resource that is multi-dimensional and has a memory layout that is optimized for multi-dimensional access from the GPU.</span></span> <span data-ttu-id="28821-228">紋理通常會包含轉譯至表面上所需的原始影像，以進行光源和混色，但可以包含其他形式的資料，例如色彩漸層和參考色彩。</span><span class="sxs-lookup"><span data-stu-id="28821-228">Textures often contain the raw image required to render onto a surface, before lighting and blending takes place, but can contain other forms of data such as color gradients and reference colors.</span></span> <span data-ttu-id="28821-229">Direct3D 12 支援一、二和三個維度紋理。</span><span class="sxs-lookup"><span data-stu-id="28821-229">Direct3D 12 supports one, two, and three dimensional textures.</span></span>

</dd> <dt>

<span data-ttu-id="28821-230"><span id="direct3d12.directx_12_glossary_tile"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_TILE"></span>**瓦**</span><span class="sxs-lookup"><span data-stu-id="28821-230"><span id="direct3d12.directx_12_glossary_tile"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_TILE"></span>**tile**</span></span>
</dt> <dd>

<span data-ttu-id="28821-231">視訊記憶體的頁面，類似于記憶體的 CPU/系統分頁。</span><span class="sxs-lookup"><span data-stu-id="28821-231">A page of video memory, similar to a CPU/System page of memory.</span></span> <span data-ttu-id="28821-232">磚標記法有助於區別 GPU 虛擬記憶體子系統與 CPU 虛擬記憶體子系統。</span><span class="sxs-lookup"><span data-stu-id="28821-232">The tile notation helps to distinguish the GPU virtual memory subsystem from the CPU virtual memory subsystem.</span></span> <span data-ttu-id="28821-233">Gpu 提供的虛擬記憶體功能與系統虛擬記憶體類似。</span><span class="sxs-lookup"><span data-stu-id="28821-233">GPUs provide similar virtual memory capabilities as system virtual memory.</span></span> <span data-ttu-id="28821-234">某些 Gpu 具有共用的虛擬記憶體功能，可讓您以 CPU 和 GPU 共用虛擬記憶體子系統的一些頁面。</span><span class="sxs-lookup"><span data-stu-id="28821-234">Some GPUs have shared virtual memory capabilities, which allow for the sharing of some pages of the virtual memory subsystem with both the CPU and GPU.</span></span>

</dd> <dt>

<span data-ttu-id="28821-235"><span id="direct3d12.directx_12_glossary_tiled_resources"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_TILED_RESOURCES"></span>**磚資源**</span><span class="sxs-lookup"><span data-stu-id="28821-235"><span id="direct3d12.directx_12_glossary_tiled_resources"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_TILED_RESOURCES"></span>**tiled resources**</span></span>
</dt> <dd>

<span data-ttu-id="28821-236">需要有並排的資源，因此不會浪費較少的 GPU 記憶體來儲存應用程式知道將無法存取的介面區域，而且硬體可以瞭解如何在連續的磚之間進行篩選。</span><span class="sxs-lookup"><span data-stu-id="28821-236">Tiled resources are needed so less GPU memory is wasted storing regions of surfaces that the application knows will not be accessed, and the hardware can understand how to filter across adjacent tiles.</span></span> <span data-ttu-id="28821-237">磚的資源是大型邏輯資源，但需要少量的實體記憶體。</span><span class="sxs-lookup"><span data-stu-id="28821-237">Tiled resources are large logical resources, but requiring small amounts of physical memory.</span></span>

</dd> <dt>

<span data-ttu-id="28821-238"><span id="direct3d12.directx_12_glossary_uav"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_UAV"></span>**未排序的存取視圖 (UAV)**</span><span class="sxs-lookup"><span data-stu-id="28821-238"><span id="direct3d12.directx_12_glossary_uav"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_UAV"></span>**Unordered Access View (UAV)**</span></span>
</dt> <dd>

<span data-ttu-id="28821-239">未排序的存取權會在資源 (中包含緩衝區、紋理和材質陣列，而不需要多取樣) ，可讓您從多個執行緒暫時未排序的讀取/寫入存取。</span><span class="sxs-lookup"><span data-stu-id="28821-239">An unordered access view into a resource (which includes buffers, textures, and texture arrays - without multi-sampling), allows temporally unordered read/write access from multiple threads.</span></span> <span data-ttu-id="28821-240">這表示此資源類型可以由多個執行緒同時讀取/寫入，而不會產生記憶體衝突。</span><span class="sxs-lookup"><span data-stu-id="28821-240">This means that this resource type can be read/written simultaneously by multiple threads without generating memory conflicts.</span></span>

</dd> <dt>

<span data-ttu-id="28821-241"><span id="direct3d12.directx_12_glossary_upload_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_UPLOAD_HEAP"></span>**上傳堆積**</span><span class="sxs-lookup"><span data-stu-id="28821-241"><span id="direct3d12.directx_12_glossary_upload_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_UPLOAD_HEAP"></span>**upload heap**</span></span>
</dt> <dd>

<span data-ttu-id="28821-242">使用者模式堆積，著重于從 CPU 到 GPU 的資料傳輸。</span><span class="sxs-lookup"><span data-stu-id="28821-242">A user-mode heap that is focused on data transfer from the CPU to the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="28821-243"><span id="direct3d12.directx_12_glossary_user_mode_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_USER_MODE_HEAP"></span>**使用者模式堆積**</span><span class="sxs-lookup"><span data-stu-id="28821-243"><span id="direct3d12.directx_12_glossary_user_mode_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_USER_MODE_HEAP"></span>**user-mode heap**</span></span>
</dt> <dd>

<span data-ttu-id="28821-244">在沒有任何核心元件感知的情況下回收的大型、連續記憶體組態集合：配置和終結方法不會在穩定狀態下呼叫核心配置和銷毀方法。</span><span class="sxs-lookup"><span data-stu-id="28821-244">A collection of large, contiguous memory allocations that are recycled without any kernel component's awareness: the allocation and destruction methods do not call kernel allocation and destruction methods during steady state.</span></span> <span data-ttu-id="28821-245">Upload、Readback 和 Default 堆積是使用者模式堆積的變體。</span><span class="sxs-lookup"><span data-stu-id="28821-245">Upload, Readback, and Default heaps are variants of user mode heaps.</span></span>

</dd> <dt>

<span data-ttu-id="28821-246"><span id="direct3d12.directx_12_glossary_volume_tiled_resources"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_VOLUME_TILED_RESOURCES"></span>**磁片區磚資源**</span><span class="sxs-lookup"><span data-stu-id="28821-246"><span id="direct3d12.directx_12_glossary_volume_tiled_resources"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_VOLUME_TILED_RESOURCES"></span>**volume tiled resources**</span></span>
</dt> <dd>

<span data-ttu-id="28821-247">三維並排顯示的 [資源](/windows)。</span><span class="sxs-lookup"><span data-stu-id="28821-247">Three-dimensional [tiled resources](/windows).</span></span>

</dd> </dl>

 

 