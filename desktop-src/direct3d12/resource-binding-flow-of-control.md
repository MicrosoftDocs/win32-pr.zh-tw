---
title: 資源系結總覽
description: DirectX 12 中資源系結的關鍵是描述項、描述中繼資料表、描述元堆積和根簽章的概念。
ms.assetid: 92E100CA-822D-46B1-BD37-FF57C3FB703D
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bc7e78255c123777716eddb43d9443e19113b34
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103617"
---
# <a name="resource-binding-overview"></a><span data-ttu-id="6489f-103">資源系結總覽</span><span class="sxs-lookup"><span data-stu-id="6489f-103">Resource Binding Overview</span></span>

<span data-ttu-id="6489f-104">DirectX 12 中資源系結的關鍵是 *描述* 項、 *描述中繼資料表*、 *描述* 元堆積和 *根* 簽章的概念。</span><span class="sxs-lookup"><span data-stu-id="6489f-104">The key to resource binding in DirectX 12 are the concepts of a *descriptor*, *descriptor tables*, *descriptor heaps*, and a *root signature*.</span></span>

-   [<span data-ttu-id="6489f-105">資源和圖形管線</span><span class="sxs-lookup"><span data-stu-id="6489f-105">Resources and the Graphics Pipeline</span></span>](#resources-and-the-graphics-pipeline)
-   [<span data-ttu-id="6489f-106">資源類型和視圖</span><span class="sxs-lookup"><span data-stu-id="6489f-106">Resource types and views</span></span>](#resource-types-and-views)
-   [<span data-ttu-id="6489f-107">控制項的資源系結流程</span><span class="sxs-lookup"><span data-stu-id="6489f-107">Resource Binding Flow of Control</span></span>](#resource-binding-overview)
-   [<span data-ttu-id="6489f-108">子</span><span class="sxs-lookup"><span data-stu-id="6489f-108">Suballocation</span></span>](#suballocation)
-   [<span data-ttu-id="6489f-109">釋放資源</span><span class="sxs-lookup"><span data-stu-id="6489f-109">Freeing Resources</span></span>](#freeing-resources)
-   [<span data-ttu-id="6489f-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="6489f-110">Related topics</span></span>](#related-topics)

## <a name="resources-and-the-graphics-pipeline"></a><span data-ttu-id="6489f-111">資源和圖形管線</span><span class="sxs-lookup"><span data-stu-id="6489f-111">Resources and the Graphics Pipeline</span></span>

<span data-ttu-id="6489f-112">著色器資源 (例如紋理、常數資料表、影像、緩衝區等等) 不會直接系結至著色器管線;相反地，它們是透過 *描述* 項參考。</span><span class="sxs-lookup"><span data-stu-id="6489f-112">Shader resources (such as textures, constant tables, images, buffers and so on) are not bound directly to the shader pipeline; instead, they are referenced through a *descriptor*.</span></span> <span data-ttu-id="6489f-113">描述項是一個小型物件，其中包含一個資源的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6489f-113">A descriptor is a small object that contains information about one resource.</span></span>

<span data-ttu-id="6489f-114">描述項會群組在一起，以形成 *描述中繼資料表*。</span><span class="sxs-lookup"><span data-stu-id="6489f-114">Descriptors are grouped together to form *descriptor tables*.</span></span> <span data-ttu-id="6489f-115">每個描述中繼資料表都會儲存某個資源類型範圍的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6489f-115">Each descriptor table stores information about one range of types of resource.</span></span> <span data-ttu-id="6489f-116">有許多不同類型的資源。</span><span class="sxs-lookup"><span data-stu-id="6489f-116">There are many different types of resources.</span></span> <span data-ttu-id="6489f-117">最常見的資源包括：</span><span class="sxs-lookup"><span data-stu-id="6489f-117">The most common resources are:</span></span>

-   <span data-ttu-id="6489f-118">常數緩衝區視圖 (CBVs) </span><span class="sxs-lookup"><span data-stu-id="6489f-118">Constant buffer views (CBVs)</span></span>
-   <span data-ttu-id="6489f-119">未排序的存取視圖 (UAVs) </span><span class="sxs-lookup"><span data-stu-id="6489f-119">Unordered access views (UAVs)</span></span>
-   <span data-ttu-id="6489f-120">著色器資源檢視 (SRVs) </span><span class="sxs-lookup"><span data-stu-id="6489f-120">Shader resource views (SRVs)</span></span>
-   <span data-ttu-id="6489f-121">取樣器</span><span class="sxs-lookup"><span data-stu-id="6489f-121">Samplers</span></span>

<span data-ttu-id="6489f-122">SRV、UAV 和 CBVs 描述元可以合併到相同的描述中繼資料表中。</span><span class="sxs-lookup"><span data-stu-id="6489f-122">SRV, UAV, and CBVs descriptors can be combined into the same descriptor table.</span></span>

<span data-ttu-id="6489f-123">圖形和計算管線藉由依索引參考描述中繼資料表來取得資源的存取權。</span><span class="sxs-lookup"><span data-stu-id="6489f-123">The graphics and compute pipelines gain access to resources by referencing into descriptor tables by index.</span></span>

<span data-ttu-id="6489f-124">描述中繼資料表會儲存在 *描述元堆積* 中。</span><span class="sxs-lookup"><span data-stu-id="6489f-124">Descriptor tables are stored in a *descriptor heap*.</span></span> <span data-ttu-id="6489f-125">描述項堆積在理想的情況下，會包含描述項資料表中 (的所有描述元，) 用於轉譯一或多個框架。</span><span class="sxs-lookup"><span data-stu-id="6489f-125">Descriptor heaps will ideally contain all the descriptors (in descriptor tables) for one or more frames to be rendered.</span></span> <span data-ttu-id="6489f-126">所有資源都會儲存在使用者模式堆積中。</span><span class="sxs-lookup"><span data-stu-id="6489f-126">All the resources will be stored in user mode heaps.</span></span>

<span data-ttu-id="6489f-127">另一個概念是 *根* 簽章的概念。</span><span class="sxs-lookup"><span data-stu-id="6489f-127">Another concept is that of a *root signature*.</span></span> <span data-ttu-id="6489f-128">根簽章是由應用程式定義的系結慣例，可供著色器用來找出需要存取的資源。</span><span class="sxs-lookup"><span data-stu-id="6489f-128">The root signature is a binding convention, defined by the application, that is used by shaders to locate the resources that they need access to.</span></span> <span data-ttu-id="6489f-129">根簽章可以存放：</span><span class="sxs-lookup"><span data-stu-id="6489f-129">The root signature can store:</span></span>

-   <span data-ttu-id="6489f-130">描述項堆積中描述項資料表的索引，其中已預先定義描述中繼資料表的配置。</span><span class="sxs-lookup"><span data-stu-id="6489f-130">Indexes to descriptor tables in a descriptor heap, where the layout of the descriptor table has been pre-defined.</span></span>
-   <span data-ttu-id="6489f-131">因此，應用程式可以系結使用者定義的常數 (稱為 *根常數*) 直接到著色器，而不需要經過描述元和描述中繼資料表。</span><span class="sxs-lookup"><span data-stu-id="6489f-131">Constants, so apps can bind user-defined constants (known as *root constants*) directly to shaders without having to go through descriptors and descriptor tables.</span></span>
-   <span data-ttu-id="6489f-132">緊接在根簽章內的描述項很少，例如常數緩衝區視圖 (CBV 每一次繪製的) ，因此儲存應用程式不需要將這些描述項放在描述元堆積中。</span><span class="sxs-lookup"><span data-stu-id="6489f-132">A very small number of descriptors directly inside the root signature, such as a constant buffer view (CBV) that changes per draw, thereby saving the application from needing to put those descriptors in a descriptor heap.</span></span>

<span data-ttu-id="6489f-133">換句話說，根簽章會針對每個繪製變更的少量資料，提供適合的效能優化。</span><span class="sxs-lookup"><span data-stu-id="6489f-133">In other words, the root signature provides performance optimizations suitable for small amounts of data that change per draw.</span></span>

<span data-ttu-id="6489f-134">適用于系結的 Direct3D 12 設計會將它與其他工作（例如記憶體管理、物件存留期管理、狀態追蹤和記憶體同步處理）分開， (指 [的是來自 Direct3D 11) 的系結模型差異](binding-model.md) 。</span><span class="sxs-lookup"><span data-stu-id="6489f-134">The Direct3D 12 design for binding separates it from other tasks, such as memory management, object lifetime management, state tracking, and memory synchronization (refer to [Differences in the Binding Model from Direct3D 11](binding-model.md)).</span></span> <span data-ttu-id="6489f-135">Direct3D 12 系結的設計是為了降低負荷，並針對最常進行的 API 呼叫優化。</span><span class="sxs-lookup"><span data-stu-id="6489f-135">Direct3D 12 binding is designed to be low overhead and optimized for the API calls that are made most frequently.</span></span> <span data-ttu-id="6489f-136">它也可在低端到高階硬體之間進行調整，並可從舊版 (更線性的 Direct3D 11 管線) 至較新 (更平行) 圖形引擎程式設計的方法。</span><span class="sxs-lookup"><span data-stu-id="6489f-136">It is also scalable across low end to high end hardware, and scalable from older (the more linear Direct3D 11 pipeline) to the newer (more parallel) approaches to graphics engine programming.</span></span>

## <a name="resource-types-and-views"></a><span data-ttu-id="6489f-137">資源類型和視圖</span><span class="sxs-lookup"><span data-stu-id="6489f-137">Resource types and views</span></span>

<span data-ttu-id="6489f-138">資源類型與 Direct3D 11 相同，亦即：</span><span class="sxs-lookup"><span data-stu-id="6489f-138">Resource types are the same as Direct3D 11, namely:</span></span>

-   <span data-ttu-id="6489f-139">Texture1D 和 Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="6489f-139">Texture1D, and Texture1DArray</span></span>
-   <span data-ttu-id="6489f-140">Texture2D，以及 Texture2DArray、Texture2DMS、Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="6489f-140">Texture2D, and Texture2DArray, Texture2DMS, Texture2DMSArray</span></span>
-   <span data-ttu-id="6489f-141">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6489f-141">Texture3D</span></span>
-   <span data-ttu-id="6489f-142">緩衝區 (具類型、結構化和原始) </span><span class="sxs-lookup"><span data-stu-id="6489f-142">Buffers (typed, structured and raw)</span></span>

<span data-ttu-id="6489f-143">資源檢視類似于 Direct3D 11、頂點和索引緩衝區視圖的加入。</span><span class="sxs-lookup"><span data-stu-id="6489f-143">Resource views are similar but slightly different from Direct3D 11, vertex and index buffer views have been added.</span></span>

-   <span data-ttu-id="6489f-144">常數緩衝區檢視 (CBV)</span><span class="sxs-lookup"><span data-stu-id="6489f-144">Constant buffer view (CBV)</span></span>
-   <span data-ttu-id="6489f-145">未排序的存取視圖 (UAV) </span><span class="sxs-lookup"><span data-stu-id="6489f-145">Unordered access view (UAV)</span></span>
-   <span data-ttu-id="6489f-146">著色器資源檢視 (SRV)</span><span class="sxs-lookup"><span data-stu-id="6489f-146">Shader resource view (SRV)</span></span>
-   <span data-ttu-id="6489f-147">取樣器</span><span class="sxs-lookup"><span data-stu-id="6489f-147">Samplers</span></span>
-   <span data-ttu-id="6489f-148">轉譯目標視圖 (RTV) </span><span class="sxs-lookup"><span data-stu-id="6489f-148">Render Target View (RTV)</span></span>
-   <span data-ttu-id="6489f-149"> (DSV) 的深度樣板視圖</span><span class="sxs-lookup"><span data-stu-id="6489f-149">Depth Stencil View (DSV)</span></span>
-   <span data-ttu-id="6489f-150">索引緩衝區視圖 (IBV) </span><span class="sxs-lookup"><span data-stu-id="6489f-150">Index Buffer View (IBV)</span></span>
-   <span data-ttu-id="6489f-151">頂點緩衝區視圖 (VBV) </span><span class="sxs-lookup"><span data-stu-id="6489f-151">Vertex Buffer View (VBV)</span></span>
-   <span data-ttu-id="6489f-152">串流輸出視圖 (SOV) </span><span class="sxs-lookup"><span data-stu-id="6489f-152">Stream Output View (SOV)</span></span>

<span data-ttu-id="6489f-153">只有著色器可以看到這些視圖的前四個，請參閱 [著色器可見的描述](shader-visible-descriptor-heaps.md) 項堆積和 [非著色器可見的描述](non-shader-visible-descriptor-heaps.md)元堆積。</span><span class="sxs-lookup"><span data-stu-id="6489f-153">Only the first four of these views are actually visible to shaders, refer to [Shader Visible Descriptor Heaps](shader-visible-descriptor-heaps.md) and [Non Shader Visible Descriptor Heaps](non-shader-visible-descriptor-heaps.md).</span></span>

## <a name="resource-binding-flow-of-control"></a><span data-ttu-id="6489f-154">控制項的資源系結流程</span><span class="sxs-lookup"><span data-stu-id="6489f-154">Resource Binding Flow of Control</span></span>

<span data-ttu-id="6489f-155">只著重于根簽章、根描述元、根常數、描述中繼資料表和描述元堆積，應用程式的轉譯邏輯流程應如下所示：</span><span class="sxs-lookup"><span data-stu-id="6489f-155">Focusing just on root signatures, root descriptors, root constants, descriptor tables, and descriptor heaps, the flow of rendering logic for an app should be similar to the following:</span></span>

-   <span data-ttu-id="6489f-156">建立一或多個根簽章物件–應用程式所需的每個不同系結設定一個。</span><span class="sxs-lookup"><span data-stu-id="6489f-156">Create one or more root signature objects – one for every different binding configuration an application needs.</span></span>
-   <span data-ttu-id="6489f-157">使用將用來搭配使用的根簽章物件來建立著色器和管線狀態。</span><span class="sxs-lookup"><span data-stu-id="6489f-157">Create shaders and pipeline state with the root signature objects they will be used with.</span></span>
-   <span data-ttu-id="6489f-158">如果有需要，請建立一個 (或（如有需要）更) 的描述元堆積，其中將包含每個轉譯畫面格的所有 SRV、UAV 和 CBV 描述項。</span><span class="sxs-lookup"><span data-stu-id="6489f-158">Create one (or, if necessary, more) descriptor heaps that will contain all the SRV, UAV, and CBV descriptors for each frame of rendering.</span></span>
-   <span data-ttu-id="6489f-159">針對將在許多框架中重複使用的描述項集合，將描述項堆積 (s) 具有描述項。</span><span class="sxs-lookup"><span data-stu-id="6489f-159">Initialize the descriptor heap(s) with descriptors where possible for sets of descriptors that will be reused across many frames.</span></span>
-   <span data-ttu-id="6489f-160">針對要呈現的每個框架：</span><span class="sxs-lookup"><span data-stu-id="6489f-160">For each frame to be rendered:</span></span>
    -   <span data-ttu-id="6489f-161">針對每個命令清單：</span><span class="sxs-lookup"><span data-stu-id="6489f-161">For each command list:</span></span>
        -   <span data-ttu-id="6489f-162">將目前的根簽章設定為使用 (，並在轉譯期間視需要變更（這很少需要) 。</span><span class="sxs-lookup"><span data-stu-id="6489f-162">Set the current root signature to use (and change if needed during rendering – which is rarely required).</span></span>
        -   <span data-ttu-id="6489f-163">針對新的 view (更新一些根簽章的常數及/或根簽章描述項，例如世界/視野投影) 。</span><span class="sxs-lookup"><span data-stu-id="6489f-163">Update some root signature’s constants and/or root signature descriptors for the new view (such as world/view projections).</span></span>
        -   <span data-ttu-id="6489f-164">針對要繪製的每個專案：</span><span class="sxs-lookup"><span data-stu-id="6489f-164">For each item to draw:</span></span>
            -   <span data-ttu-id="6489f-165">根據每個物件轉譯的需要，在描述元堆積中定義任何新的描述項。</span><span class="sxs-lookup"><span data-stu-id="6489f-165">Define any new descriptors in descriptor heaps as needed for per-object rendering.</span></span> <span data-ttu-id="6489f-166">針對著色器可見的描述元堆積，應用程式必須確定使用可能正在進行轉譯的描述項堆積空間，例如，在轉譯期間透過描述元堆積以線性方式配置空間。</span><span class="sxs-lookup"><span data-stu-id="6489f-166">For shader-visible descriptor heaps, the app must make sure to use descriptor heap space that isn’t already being referenced by rendering that could be in flight – for example, linearly allocating space through the descriptor heap during rendering.</span></span>
            -   <span data-ttu-id="6489f-167">使用描述項堆積所需區域的指標來更新根簽章。</span><span class="sxs-lookup"><span data-stu-id="6489f-167">Update the root signature with pointers to the required regions of the descriptor heaps.</span></span> <span data-ttu-id="6489f-168">例如，一個描述中繼資料表可能會指向某些靜態 (不變的) 描述項稍早初始化的描述項，而另一個描述中繼資料表則可能指向針對目前轉譯所設定的一些動態描述項。</span><span class="sxs-lookup"><span data-stu-id="6489f-168">For example, one descriptor table might point to some static (unchanging) descriptors initialized earlier, while another descriptor table might point to some dynamic descriptors configured for the current rendering.</span></span>
            -   <span data-ttu-id="6489f-169">針對每個專案轉譯更新一些根簽章的常數及/或根簽章描述項。</span><span class="sxs-lookup"><span data-stu-id="6489f-169">Update some root signature’s constants and/or root signature descriptors for per-item rendering.</span></span>
            -   <span data-ttu-id="6489f-170">將專案的管線狀態設定為只在需要變更時才繪製 () ，與目前系結的根簽章相容。</span><span class="sxs-lookup"><span data-stu-id="6489f-170">Set the pipeline state for the item to draw (only if change needed), compatible with the currently bound root signature.</span></span>
            -   <span data-ttu-id="6489f-171">Draw</span><span class="sxs-lookup"><span data-stu-id="6489f-171">Draw</span></span>
        -   <span data-ttu-id="6489f-172">重複 (下一個專案) </span><span class="sxs-lookup"><span data-stu-id="6489f-172">Repeat (next item)</span></span>
    -   <span data-ttu-id="6489f-173">重複 (下一個命令清單) </span><span class="sxs-lookup"><span data-stu-id="6489f-173">Repeat (next command list)</span></span>
    -   <span data-ttu-id="6489f-174">嚴格地說，當 GPU 已完成，且將不再使用任何記憶體時，就可以釋出。</span><span class="sxs-lookup"><span data-stu-id="6489f-174">Strictly when the GPU has finished with any memory that will no longer be used, it can be released.</span></span> <span data-ttu-id="6489f-175">如果未提交使用這些描述項的其他轉譯，則不需要刪除描述項的參考。</span><span class="sxs-lookup"><span data-stu-id="6489f-175">Descriptors' references to it do not need to be deleted if additional rendering that uses those descriptors is not submitted.</span></span> <span data-ttu-id="6489f-176">因此，後續轉譯可指向描述項堆積中的其他區域，或使用有效的描述元覆寫過時的描述元，以重複使用描述項堆積空間。</span><span class="sxs-lookup"><span data-stu-id="6489f-176">So, subsequent rendering can point to other areas in descriptor heaps, or stale descriptors can be overwritten with valid descriptors to reuse the descriptor heap space.</span></span>
-   <span data-ttu-id="6489f-177">重複 (下一個畫面格) </span><span class="sxs-lookup"><span data-stu-id="6489f-177">Repeat (next frame)</span></span>

<span data-ttu-id="6489f-178">請注意，其他描述項類型、轉譯目標視圖 (RTVs) 、深度樣板視圖 (DSV) 、索引緩衝區視圖 (IBVs) 、頂點緩衝區視圖 (VBVs) ，以及著色器物件檢視 (SOV) ）的管理方式不同。</span><span class="sxs-lookup"><span data-stu-id="6489f-178">Note that other descriptor types, render target views (RTVs), depth stencil views (DSV), index buffer views (IBVs), vertex buffer views (VBVs), and shader object views (SOV), are managed differently.</span></span> <span data-ttu-id="6489f-179">驅動程式會處理在記錄命令清單期間，針對每個繪製所系結之描述項集的版本設定， (類似于硬體/驅動程式) 如何設定根簽章系結的版本。</span><span class="sxs-lookup"><span data-stu-id="6489f-179">The driver handles the versioning of the set of descriptors bound for each draw during recording of the command list (similar to how the root signature bindings are versioned by the hardware/driver).</span></span> <span data-ttu-id="6489f-180">這與著色器可見描述項堆積的內容不同，因為應用程式在參考繪圖之間的不同描述項時，必須透過堆積手動設定。</span><span class="sxs-lookup"><span data-stu-id="6489f-180">This is different from the contents of shader-visible descriptor heaps, for which the application must manually allocate through the heap as it references different descriptors between draws.</span></span> <span data-ttu-id="6489f-181">將著色器可見之堆積內容的版本控制保留在應用程式中，因為它可讓應用程式執行一些動作，例如不變更的重複專案描述項，或使用大量的靜態描述項，並使用著色器的索引 (例如依材質識別碼) 從描述項堆積選取要使用的描述項，或針對不同的描述項組合使用技術組合。</span><span class="sxs-lookup"><span data-stu-id="6489f-181">Versioning of heap content that is shader-visible is left to the application because it allows applications to do things like reuse descriptors that don’t change, or use large static sets of descriptors and use shader indexing (such as by material ID) to select descriptors to use from the descriptor heap, or use combinations of techniques for different sets of descriptors.</span></span> <span data-ttu-id="6489f-182">硬體尚未配備其他描述項類型的彈性， (RTV、DSV、IBV、VBV、SOV) 。</span><span class="sxs-lookup"><span data-stu-id="6489f-182">The hardware isn’t equipped to handle this type of flexibility for the other descriptor types (RTV, DSV, IBV, VBV, SOV).</span></span>

## <a name="suballocation"></a><span data-ttu-id="6489f-183">子</span><span class="sxs-lookup"><span data-stu-id="6489f-183">Suballocation</span></span>

<span data-ttu-id="6489f-184">在 Direct3D 12 中，應用程式對記憶體管理具有低層級的控制。</span><span class="sxs-lookup"><span data-stu-id="6489f-184">In Direct3D 12, the app has low-level control over memory management.</span></span> <span data-ttu-id="6489f-185">在舊版 Direct3D （包括 Direct3D 11）中，每個資源都會有一個配置。</span><span class="sxs-lookup"><span data-stu-id="6489f-185">In earlier versions of Direct3D, including Direct3D 11, there would be one allocation per resource.</span></span> <span data-ttu-id="6489f-186">在 Direct3D 12 中，應用程式可以使用 API 來配置大型記憶體區塊，而不是任何單一物件都需要。</span><span class="sxs-lookup"><span data-stu-id="6489f-186">In Direct3D 12, the app can use the API to allocate a large block of memory, larger than any single object would need.</span></span> <span data-ttu-id="6489f-187">完成這項操作之後，應用程式就可以建立描述元來指向該大型記憶體區塊的區段。</span><span class="sxs-lookup"><span data-stu-id="6489f-187">After this is done, the app can create descriptors to point to sections of that large memory block.</span></span> <span data-ttu-id="6489f-188">這項程式決定在大型) 區塊內 (較社區塊的位置，也就是所謂的子 *分配*。</span><span class="sxs-lookup"><span data-stu-id="6489f-188">This process of deciding what to put where (smaller blocks inside the large block) is known as *suballocation*.</span></span> <span data-ttu-id="6489f-189">讓應用程式執行這項作業，可以有效率地使用計算和記憶體。</span><span class="sxs-lookup"><span data-stu-id="6489f-189">Enabling the app to do this can yield gains in efficient use of computation and memory.</span></span> <span data-ttu-id="6489f-190">例如，資源重新命名會呈現為過時。</span><span class="sxs-lookup"><span data-stu-id="6489f-190">For example, resource renaming is rendered obsolete.</span></span> <span data-ttu-id="6489f-191">為了取代這項功能，應用程式可以使用圍牆來決定何時使用特定資源，以及當命令清單執行時，不受限於命令清單執行需要使用該特定資源的情況。</span><span class="sxs-lookup"><span data-stu-id="6489f-191">In place of this, apps can use fences to determine when a particular resource is being used and when it's not by fencing on command list executions where the command list requires the use of that particular resource.</span></span>

## <a name="freeing-resources"></a><span data-ttu-id="6489f-192">釋放資源</span><span class="sxs-lookup"><span data-stu-id="6489f-192">Freeing Resources</span></span>

<span data-ttu-id="6489f-193">在任何已系結至管線的記憶體可以釋出之前，GPU 必須已完成。</span><span class="sxs-lookup"><span data-stu-id="6489f-193">Before any memory that has been bound to the pipeline can be freed, the GPU must be finished with it.</span></span>

<span data-ttu-id="6489f-194">等候畫面格轉譯可能是確定 GPU 已完成的最粗略方式。</span><span class="sxs-lookup"><span data-stu-id="6489f-194">Waiting for frame rendering is probably the coarsest way to be certain that the GPU has finished.</span></span> <span data-ttu-id="6489f-195">更精細的一點是，您可以再次使用範圍：當命令記錄到您要追蹤完成的命令清單時，請在它之後立即插入一個範圍。</span><span class="sxs-lookup"><span data-stu-id="6489f-195">At a finer grain, you can again use fences—when a command is recorded into a command list that you want to track the completion of, insert a fence immediately after it.</span></span> <span data-ttu-id="6489f-196">然後，您可以使用隔離來進行各種同步處理作業。</span><span class="sxs-lookup"><span data-stu-id="6489f-196">Then, you can do various synchronization operations with the fence.</span></span> <span data-ttu-id="6489f-197">您會將新的工作提交 (的命令清單) 等候在 GPU 上傳遞指定的範圍為止（指出完成之前的所有專案），或您可以要求當您在應用程式可透過睡眠執行緒) 等待的 (時引發 CPU 事件。</span><span class="sxs-lookup"><span data-stu-id="6489f-197">You submit new work (command lists) that waits until a specified fence has passed on the GPU, which indicates that everything before it is complete, or you can request that a CPU event be raised when the fence has passed (which the app can be waiting on with a sleeping thread).</span></span> <span data-ttu-id="6489f-198">在 Direct3D 11 中，這是 `EnqueueSetEvent` () 。</span><span class="sxs-lookup"><span data-stu-id="6489f-198">In Direct3D 11, this was `EnqueueSetEvent`().</span></span>

## <a name="related-topics"></a><span data-ttu-id="6489f-199">相關主題</span><span class="sxs-lookup"><span data-stu-id="6489f-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6489f-200">資源系結</span><span class="sxs-lookup"><span data-stu-id="6489f-200">Resource Binding</span></span>](resource-binding.md)
</dt> </dl>

 

 




