---
title: 使用 Direct3D 12 的管線和著色器
description: 相較于上一代圖形程式設計介面，Direct3D 12 程式化管線可大幅提高轉譯效能。
ms.assetid: 329882F5-D2A9-4D6D-AC3B-29F370D22C97
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e2c392b3915443da2f287a5511f3959cbb7179f
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/06/2021
ms.locfileid: "104548383"
---
# <a name="pipelines-and-shaders-with-direct3d-12"></a><span data-ttu-id="dd214-103">使用 Direct3D 12 的管線和著色器</span><span class="sxs-lookup"><span data-stu-id="dd214-103">Pipelines and Shaders with Direct3D 12</span></span>

<span data-ttu-id="dd214-104">相較于上一代圖形程式設計介面，Direct3D 12 程式化管線可大幅提高轉譯效能。</span><span class="sxs-lookup"><span data-stu-id="dd214-104">The Direct3D 12 programmable pipeline significantly increases rendering performance compared to previous generation graphics programming interfaces.</span></span>

-   [<span data-ttu-id="dd214-105">Direct3D 12 圖形管線</span><span class="sxs-lookup"><span data-stu-id="dd214-105">Direct3D 12 graphics pipeline</span></span>](#direct3d-12-graphics-pipeline)
-   [<span data-ttu-id="dd214-106">管線狀態物件</span><span class="sxs-lookup"><span data-stu-id="dd214-106">Pipeline state objects</span></span>](#pipeline-state-objects)
-   [<span data-ttu-id="dd214-107">Direct3D 12 計算管線</span><span class="sxs-lookup"><span data-stu-id="dd214-107">Direct3D 12 compute pipeline</span></span>](#direct3d-12-compute-pipeline)
-   [<span data-ttu-id="dd214-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="dd214-108">Related topics</span></span>](#related-topics)

## <a name="direct3d-12-graphics-pipeline"></a><span data-ttu-id="dd214-109">Direct3D 12 圖形管線</span><span class="sxs-lookup"><span data-stu-id="dd214-109">Direct3D 12 graphics pipeline</span></span>

<span data-ttu-id="dd214-110">下圖說明 Direct3D 12 圖形管線和狀態。</span><span class="sxs-lookup"><span data-stu-id="dd214-110">The following diagram illustrates the Direct3D 12 graphics pipeline and state.</span></span>

![說明 direct3d 12 管線和狀態的圖表](images/pipeline.png)

<span data-ttu-id="dd214-112">圖形管線是 GPU 轉譯畫面格時，資料輸入和輸出的連續流程。</span><span class="sxs-lookup"><span data-stu-id="dd214-112">A graphics pipeline is the sequential flow of data inputs and outputs as the GPU renders frames.</span></span> <span data-ttu-id="dd214-113">由於有管線狀態和輸入，GPU 會執行一連串的作業來建立產生的映射。</span><span class="sxs-lookup"><span data-stu-id="dd214-113">Given the pipeline state and inputs, the GPU performs a series of operations to create the resulting images.</span></span> <span data-ttu-id="dd214-114">圖形管線包含著色器，可執行可程式化的轉譯效果和計算，以及固定的函式作業。</span><span class="sxs-lookup"><span data-stu-id="dd214-114">A graphics pipeline contains shaders, which perform programmable rendering effects and calculations, and fixed function operations.</span></span>

<span data-ttu-id="dd214-115">參考管線狀態圖表時，請注意下列事項：</span><span class="sxs-lookup"><span data-stu-id="dd214-115">Note the following when referring to the pipeline state diagram:</span></span>

-   <span data-ttu-id="dd214-116">描述項資料表和堆積可以任意排列： SRVs、CBVs 和 UAVs 可依任何順序參考及配置。</span><span class="sxs-lookup"><span data-stu-id="dd214-116">The descriptor tables and heaps can be arbitrarily arranged: SRVs, CBVs and UAVs can be referenced and allocated in any order.</span></span>
-   <span data-ttu-id="dd214-117">管線的某些作業是可設定的。</span><span class="sxs-lookup"><span data-stu-id="dd214-117">Some operations of the pipeline are configurable.</span></span> <span data-ttu-id="dd214-118">例如，輸出合併通常會以「轉譯目標」和「深度」樣板視圖的讀取-修改-寫入為基礎運作。</span><span class="sxs-lookup"><span data-stu-id="dd214-118">For example, the output merger typically operates on a read-modify-write basis with the render target and depth stencil views.</span></span> <span data-ttu-id="dd214-119">不過，您可以設定管線，讓其中一個視圖為唯讀或僅限寫入。</span><span class="sxs-lookup"><span data-stu-id="dd214-119">However the pipeline can be configured so that either of these views are read-only or write-only.</span></span>
-   <span data-ttu-id="dd214-120">靜態取樣器不是根引數的一部分，因為它們是靜態引數。</span><span class="sxs-lookup"><span data-stu-id="dd214-120">Static samplers are not part of the root arguments since they are static.</span></span>

## <a name="pipeline-state-objects"></a><span data-ttu-id="dd214-121">管線狀態物件</span><span class="sxs-lookup"><span data-stu-id="dd214-121">Pipeline state objects</span></span>

<span data-ttu-id="dd214-122">Direct3D 12 引進 (PSO) 的管線狀態物件。</span><span class="sxs-lookup"><span data-stu-id="dd214-122">Direct3D 12 introduces the pipeline state object (PSO).</span></span> <span data-ttu-id="dd214-123">像輸入組合語言、轉譯器、圖元著色器和輸出合併等管線元件的狀態會儲存在 PSO 中，而不是儲存和表示大量高階物件的管線狀態。</span><span class="sxs-lookup"><span data-stu-id="dd214-123">Rather than storing and representing pipeline state across a large number of high-level objects, the states of pipeline components like the input assembler, rasterizer, pixel shader, and output merger are stored in a PSO.</span></span> <span data-ttu-id="dd214-124">PSO 是在建立之後不可變的整合管線狀態物件。</span><span class="sxs-lookup"><span data-stu-id="dd214-124">A PSO is a unified pipeline state object that is immutable after creation.</span></span> <span data-ttu-id="dd214-125">目前選取的 PSO 可以快速且動態地進行變更，而硬體和驅動程式可以直接將 PSO 轉換成原生硬體指示和狀態，讓 GPU 進行圖形處理。</span><span class="sxs-lookup"><span data-stu-id="dd214-125">The currently selected PSO can be changed quickly and dynamically, and the hardware and drivers can directly convert a PSO into native hardware instructions and state, readying the GPU for graphics processing.</span></span> <span data-ttu-id="dd214-126">為了套用 PSO，硬體會將最少量的預先計算狀態直接複製到硬體暫存器。</span><span class="sxs-lookup"><span data-stu-id="dd214-126">To apply a PSO, the hardware copies a minimal amount of pre-computed state directly to the hardware registers.</span></span> <span data-ttu-id="dd214-127">這會移除圖形驅動程式根據所有目前適用的轉譯和管線設定持續重新計算硬體狀態所造成的額外負荷。</span><span class="sxs-lookup"><span data-stu-id="dd214-127">This removes the overhead caused by the graphics driver continually recomputing hardware state based on all currently applicable rendering and pipeline settings.</span></span> <span data-ttu-id="dd214-128">結果會大幅減少繪製呼叫的額外負荷、提升效能，以及每個畫面格的繪製呼叫。</span><span class="sxs-lookup"><span data-stu-id="dd214-128">The result is significantly reduced draw call overhead, increased performance, and more draw calls per frame.</span></span>

<span data-ttu-id="dd214-129">目前套用的 PSO 會定義並連接轉譯管線中使用的所有著色器。</span><span class="sxs-lookup"><span data-stu-id="dd214-129">The currently applied PSO defines and connects all of the shaders being used in the rendering pipeline.</span></span> <span data-ttu-id="dd214-130">[Microsoft 高階著色器語言 (HLSL) ](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) 會預先編譯成著色器物件，然後在執行時間用來當做管線狀態物件的輸入。</span><span class="sxs-lookup"><span data-stu-id="dd214-130">[Microsoft High Level Shader Language (HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) is pre-compiled into shader objects, which are then used at run time as input for pipeline state objects.</span></span> <span data-ttu-id="dd214-131">如需有關如何在圖形管線內 PSO 函式的詳細資訊，請參閱 [在 Direct3D 12 中管理圖形管線狀態](managing-graphics-pipeline-state-in-direct3d-12.md)。</span><span class="sxs-lookup"><span data-stu-id="dd214-131">For more information about how the PSO functions within the graphics pipeline, see [Managing graphics pipeline state in Direct3D 12](managing-graphics-pipeline-state-in-direct3d-12.md).</span></span>

## <a name="direct3d-12-compute-pipeline"></a><span data-ttu-id="dd214-132">Direct3D 12 計算管線</span><span class="sxs-lookup"><span data-stu-id="dd214-132">Direct3D 12 compute pipeline</span></span>

<span data-ttu-id="dd214-133">下圖說明 Direct3D 12 計算管線和狀態。</span><span class="sxs-lookup"><span data-stu-id="dd214-133">The following diagram illustrates the Direct3D 12 compute pipeline and state.</span></span>

![顯示 Direct3D 12 計算管線的圖表。](images/compute-pipeline.png)

<span data-ttu-id="dd214-135">此管線中沒有固定的函式單位，不過，在計算中仍可使用描述元堆積、取樣器堆積和靜態取樣器。</span><span class="sxs-lookup"><span data-stu-id="dd214-135">There are no fixed function units in this pipeline, however descriptor heaps, sampler heaps and static samplers are still available in compute.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dd214-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="dd214-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd214-137">在 Direct3D 12 中提交工作</span><span class="sxs-lookup"><span data-stu-id="dd214-137">Work Submission in Direct3D 12</span></span>](command-queues-and-command-lists.md)
</dt> </dl>

 

 