---
title: D3D12 程式碼 Walk-Throughs
description: 本節提供範例案例的程式碼。 許多解說都提供詳細資料，說明如何將程式碼新增至基本範例，以避免針對每個案例重複基本的元件程式碼。
ms.assetid: 1F37FD3A-385C-4DD5-B04C-980F078D90D0
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fdea9b519e2a0adac9dc346d6bee455af0018da
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104963"
---
# <a name="d3d12-code-walk-throughs"></a><span data-ttu-id="37a42-104">D3D12 程式碼 Walk-Throughs</span><span class="sxs-lookup"><span data-stu-id="37a42-104">D3D12 Code Walk-Throughs</span></span>

<span data-ttu-id="37a42-105">本節提供範例案例的程式碼。</span><span class="sxs-lookup"><span data-stu-id="37a42-105">This section provides code for sample scenarios.</span></span> <span data-ttu-id="37a42-106">許多解說都提供詳細資料，說明如何將程式碼新增至基本範例，以避免針對每個案例重複基本的元件程式碼。</span><span class="sxs-lookup"><span data-stu-id="37a42-106">Many of the walk-throughs provide details on what coding is required to be added to a basic sample, to avoid repeating the basic component code for each scenario.</span></span>

<span data-ttu-id="37a42-107">如需最基本的元件，請參閱 [建立基本的 Direct3D 12 元件](creating-a-basic-direct3d-12-component.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="37a42-107">For the most basic component, refer to the [Creating a Basic Direct3D 12 Component](creating-a-basic-direct3d-12-component.md) section.</span></span> <span data-ttu-id="37a42-108">下列逐步解說解說說明更先進的案例。</span><span class="sxs-lookup"><span data-stu-id="37a42-108">The following walk-throughs describe more advanced scenarios.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="37a42-109">本節內容</span><span class="sxs-lookup"><span data-stu-id="37a42-109">In this section</span></span>



| <span data-ttu-id="37a42-110">主題</span><span class="sxs-lookup"><span data-stu-id="37a42-110">Topic</span></span>                                                                                           | <span data-ttu-id="37a42-111">描述</span><span class="sxs-lookup"><span data-stu-id="37a42-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="37a42-112">使用 D3D11on12 的 D2D</span><span class="sxs-lookup"><span data-stu-id="37a42-112">D2D using D3D11on12</span></span>](d2d-using-d3d11on12.md)<br/>                                       | <span data-ttu-id="37a42-113">**D3D1211on12** 範例示範如何藉由在11型裝置與12部裝置之間共用資源，來呈現 D3D12 內容的 D2D 內容。</span><span class="sxs-lookup"><span data-stu-id="37a42-113">The **D3D1211on12** sample demonstrates how to render D2D content over D3D12 content by sharing resources between an 11 based device and a 12 based device.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="37a42-114">多引擎 n-內文重力模擬</span><span class="sxs-lookup"><span data-stu-id="37a42-114">Multi-engine n-body gravity simulation</span></span>](multi-engine-n-body-gravity-simulation.md)<br/> | <span data-ttu-id="37a42-115">**D3D12nBodyGravity** 範例會示範如何以非同步方式執行計算工作。</span><span class="sxs-lookup"><span data-stu-id="37a42-115">The **D3D12nBodyGravity** sample demonstrates how to do compute work asynchronously.</span></span> <span data-ttu-id="37a42-116">此範例會使用計算命令佇列來旋轉多個執行緒，並在執行 n 主體引力模擬的 GPU 上排程計算工作。</span><span class="sxs-lookup"><span data-stu-id="37a42-116">The sample spins up a number of threads each with a compute command queue and schedules compute work on the GPU that performs an n-body gravity simulation.</span></span> <span data-ttu-id="37a42-117">每個執行緒會在已滿位置和速度資料的兩個緩衝區上運作。</span><span class="sxs-lookup"><span data-stu-id="37a42-117">Each thread operates on two buffers full of position and velocity data.</span></span> <span data-ttu-id="37a42-118">在每個反復專案中，計算著色器會從一個緩衝區讀取目前的位置和速度資料，然後將下一個反覆運算寫入至另一個緩衝區。</span><span class="sxs-lookup"><span data-stu-id="37a42-118">With each iteration, the compute shader reads the current position and velocity data from one buffer and writes the next iteration into the other buffer.</span></span> <span data-ttu-id="37a42-119">當反復專案完成時，計算著色器會交換哪個緩衝區是讀取位置/速度資料的 SRV，以及藉由變更每個緩衝區上的資源狀態來寫入位置/速度更新的 UAV。</span><span class="sxs-lookup"><span data-stu-id="37a42-119">When the iteration completes, the compute shader swaps which buffer is the SRV for reading position/velocity data and which is the UAV for writing position/velocity updates by changing the resource state on each buffer.</span></span><br/> |
| [<span data-ttu-id="37a42-120">Predication 查詢</span><span class="sxs-lookup"><span data-stu-id="37a42-120">Predication queries</span></span>](predication-queries.md)<br/>                                       | <span data-ttu-id="37a42-121">**D3D12PredicationQueries** 範例示範如何使用 DirectX 12 查詢堆積和 predication 來挑選遮蔽。</span><span class="sxs-lookup"><span data-stu-id="37a42-121">The **D3D12PredicationQueries** sample demonstrates occlusion culling using DirectX 12 query heaps and predication.</span></span> <span data-ttu-id="37a42-122">本逐步解說將說明擴充 **HelloConstBuffer** 範例以處理 predication 查詢所需的其他程式碼。</span><span class="sxs-lookup"><span data-stu-id="37a42-122">The walkthrough describes the additional code needed to extend the **HelloConstBuffer** sample to handle predication queries.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="37a42-123">使用 HLSL 5.1 的動態索引</span><span class="sxs-lookup"><span data-stu-id="37a42-123">Dynamic Indexing using HLSL 5.1</span></span>](dynamic-indexing-using-hlsl-5-1.md)<br/>               | <span data-ttu-id="37a42-124">**D3D12DynamicIndexing** 範例示範一些可在著色器模型5.1 中使用的新 HLSL 功能（特別是動態索引和未系結的陣列），以轉譯相同的網格多次，每次轉譯時都有動態選取的材質。</span><span class="sxs-lookup"><span data-stu-id="37a42-124">The **D3D12DynamicIndexing** sample demonstrates some of the new HLSL features available in Shader Model 5.1 - particularly dynamic indexing and unbounded arrays - to render the same mesh multiple times, each time rendering it with a dynamically selected material.</span></span> <span data-ttu-id="37a42-125">使用動態索引時，著色器現在可以在陣列中編制索引，而不需要在編譯時期知道索引的值。</span><span class="sxs-lookup"><span data-stu-id="37a42-125">With dynamic indexing, shaders can now index into an array without knowing the value of the index at compile time.</span></span> <span data-ttu-id="37a42-126">當結合未系結的陣列時，這會為著色器作者和美工圖案增加另一層間接取值和彈性。</span><span class="sxs-lookup"><span data-stu-id="37a42-126">When combined with unbounded arrays, this adds another level of indirection and flexibility for shader authors and art pipelines.</span></span><br/>                                                                                                                                                                                  |
| [<span data-ttu-id="37a42-127">間接繪圖和 GPU 剔除</span><span class="sxs-lookup"><span data-stu-id="37a42-127">Indirect drawing and GPU culling</span></span>](indirect-drawing-and-gpu-culling-.md)<br/>            | <span data-ttu-id="37a42-128">D3D12ExecuteIndirect 範例會示範如何使用間接命令來繪製內容。</span><span class="sxs-lookup"><span data-stu-id="37a42-128">The D3D12ExecuteIndirect sample demonstrates how to use indirect commands to draw content.</span></span> <span data-ttu-id="37a42-129">它也會示範如何在發行之前，在計算著色器中的 GPU 上操作這些命令。</span><span class="sxs-lookup"><span data-stu-id="37a42-129">It also demonstrates how these commands can be manipulated on the GPU in a compute shader before they are issued.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="37a42-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="37a42-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37a42-131">Direct3D 12 程式設計指南</span><span class="sxs-lookup"><span data-stu-id="37a42-131">Direct3D 12 Programming Guide</span></span>](directx-12-programming-guide.md)
</dt> <dt>

[<span data-ttu-id="37a42-132">DirectX advanced learning 影片教學課程</span><span class="sxs-lookup"><span data-stu-id="37a42-132">DirectX advanced learning video tutorials</span></span>](https://www.youtube.com/channel/UCiaX2B8XiXR70jaN7NK-FpA)
</dt> <dt>

[<span data-ttu-id="37a42-133">D3D12 參考中的範例程式碼</span><span class="sxs-lookup"><span data-stu-id="37a42-133">Example Code in the D3D12 Reference</span></span>](notes-on-example-code.md)
</dt> <dt>

[<span data-ttu-id="37a42-134">工作範例</span><span class="sxs-lookup"><span data-stu-id="37a42-134">Working Samples</span></span>](working-samples.md)
</dt> </dl>

 

 





