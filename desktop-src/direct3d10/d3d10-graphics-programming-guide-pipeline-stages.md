---
description: Direct3D 10 可程式化管線是設計用來產生即時遊戲應用程式的圖形。 下圖顯示透過每個可程式化階段輸入至輸出的資料流程。
ms.assetid: 3ead6c7c-c7cc-48f1-81d5-b4b67326d610
title: " (Direct3D 10) 的管線階段"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db78bf6e904051fcac255a5bf1b99ca0f7d43ca3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110540"
---
# <a name="pipeline-stages-direct3d-10"></a><span data-ttu-id="5d97a-104"> (Direct3D 10) 的管線階段</span><span class="sxs-lookup"><span data-stu-id="5d97a-104">Pipeline Stages (Direct3D 10)</span></span>

<span data-ttu-id="5d97a-105">Direct3D 10 可程式化管線是設計用來產生即時遊戲應用程式的圖形。</span><span class="sxs-lookup"><span data-stu-id="5d97a-105">The Direct3D 10 programmable pipeline is designed for generating graphics for realtime gaming applications.</span></span> <span data-ttu-id="5d97a-106">下圖顯示透過每個可程式化階段輸入至輸出的資料流程。</span><span class="sxs-lookup"><span data-stu-id="5d97a-106">The following diagram shows the data flow from input to output through each of the programmable stages.</span></span>

![direct3d 10 程式化管線中資料流程的圖表](images/d3d10-pipeline-stages.png)

<span data-ttu-id="5d97a-108">所有階段都可以使用 API 進行設定。</span><span class="sxs-lookup"><span data-stu-id="5d97a-108">All of the stages can be configured using the API.</span></span> <span data-ttu-id="5d97a-109">使用 HLSL 的程式設計語言，可使用的程式設計語言， (圓角矩形) 區塊的常見著色器核心階段。</span><span class="sxs-lookup"><span data-stu-id="5d97a-109">Stages featuring common shader cores (the rounded rectangular blocks) are programmable using the HLSL programming language.</span></span> <span data-ttu-id="5d97a-110">如您所見，這會讓管線極具彈性且更具彈性。</span><span class="sxs-lookup"><span data-stu-id="5d97a-110">As you will see, this makes the pipeline extremely flexible and adaptable.</span></span> <span data-ttu-id="5d97a-111">每個階段的用途如下所示。</span><span class="sxs-lookup"><span data-stu-id="5d97a-111">The purpose of each of the stages is listed below.</span></span>

-   <span data-ttu-id="5d97a-112">[輸入組合語言階段](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage.md) -輸入組合語言階段負責提供資料 (三角形、線條和點) 至管線。</span><span class="sxs-lookup"><span data-stu-id="5d97a-112">[Input-Assembler Stage](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage.md) - The input-assembler stage is responsible for supplying data (triangles, lines and points) to the pipeline.</span></span>
-   <span data-ttu-id="5d97a-113">[頂點著色器階段](https://www.bing.com/search?q=Vertex-Shader+Stage) - 頂點著色器階段處理頂點，通常執行轉換、貼圖與光照等作業。</span><span class="sxs-lookup"><span data-stu-id="5d97a-113">[Vertex-Shader Stage](https://www.bing.com/search?q=Vertex-Shader+Stage) - The vertex-shader stage processes vertices, typically performing operations such as transformations, skinning, and lighting.</span></span> <span data-ttu-id="5d97a-114">頂點著色器一律採用單一輸入頂點，並產生單一輸出頂點。</span><span class="sxs-lookup"><span data-stu-id="5d97a-114">A vertex shader always takes a single input vertex and produces a single output vertex.</span></span>
-   <span data-ttu-id="5d97a-115">[幾何-著色器階段](https://www.bing.com/search?q=Geometry-Shader+Stage) -幾何著色器階段會處理整個基本專案。</span><span class="sxs-lookup"><span data-stu-id="5d97a-115">[Geometry-Shader Stage](https://www.bing.com/search?q=Geometry-Shader+Stage) - The geometry-shader stage processes entire primitives.</span></span> <span data-ttu-id="5d97a-116">它的輸入是完整的基本 (，其為三角形的三個頂點、線條的兩個頂點，或點) 的單一頂點。</span><span class="sxs-lookup"><span data-stu-id="5d97a-116">Its input is a full primitive (which is three vertices for a triangle, two vertices for a line, or a single vertex for a point).</span></span> <span data-ttu-id="5d97a-117">此外，每個基本專案也可以包含任何邊緣相鄰基本專案的頂點資料。</span><span class="sxs-lookup"><span data-stu-id="5d97a-117">In addition, each primitive can also include the vertex data for any edge-adjacent primitives.</span></span> <span data-ttu-id="5d97a-118">這最多可以包含三角形的三個頂點或一行的額外兩個頂點。</span><span class="sxs-lookup"><span data-stu-id="5d97a-118">This could include at most an additional three vertices for a triangle or an additional two vertices for a line.</span></span> <span data-ttu-id="5d97a-119">幾何著色器也支援有限的幾何放大以及取消放大。</span><span class="sxs-lookup"><span data-stu-id="5d97a-119">The Geometry Shader also supports limited geometry amplification and de-amplification.</span></span> <span data-ttu-id="5d97a-120">即使有輸入基本類型，幾何著色器可捨棄基本類型，或發出一種或多種新的基本類型。</span><span class="sxs-lookup"><span data-stu-id="5d97a-120">Given an input primitive, the Geometry Shader can discard the primitive, or emit one or more new primitives.</span></span>
-   <span data-ttu-id="5d97a-121">[資料流程輸出階段](../direct3d11/d3d10-graphics-programming-guide-output-stream-stage.md) ：資料流程輸出階段是設計用來將管線中的基本資料串流處理至轉譯器的記憶體。</span><span class="sxs-lookup"><span data-stu-id="5d97a-121">[Stream-Output Stage](../direct3d11/d3d10-graphics-programming-guide-output-stream-stage.md) - The stream-output stage is designed for streaming primitive data from the pipeline to memory on its way to the rasterizer.</span></span> <span data-ttu-id="5d97a-122">資料可串流輸出及/或傳遞進入點陣化。</span><span class="sxs-lookup"><span data-stu-id="5d97a-122">Data can be streamed out and/or passed into the rasterizer.</span></span> <span data-ttu-id="5d97a-123">串流輸出到記憶體的資料可重新循環回管線，做為輸入資料或從 CPU 讀回。</span><span class="sxs-lookup"><span data-stu-id="5d97a-123">Data streamed out to memory can be recirculated back into the pipeline as input data or read-back from the CPU.</span></span>
-   <span data-ttu-id="5d97a-124">轉譯器[階段](../direct3d11/d3d10-graphics-programming-guide-rasterizer-stage.md)-轉譯器會負責裁剪基本專案、準備圖元著色器的基本專案，以及決定如何叫用圖元著色器。</span><span class="sxs-lookup"><span data-stu-id="5d97a-124">[Rasterizer Stage](../direct3d11/d3d10-graphics-programming-guide-rasterizer-stage.md) - The rasterizer is responsible for clipping primitives, preparing primitives for the pixel shader and determining how to invoke pixel shaders.</span></span>
-   <span data-ttu-id="5d97a-125">[像素著色器階段](https://www.bing.com/search?q=Pixel-Shader+Stage) - 像素著色器階段會接收基本型別的插補資料，並產生每一像素資料，如色彩。</span><span class="sxs-lookup"><span data-stu-id="5d97a-125">[Pixel-Shader Stage](https://www.bing.com/search?q=Pixel-Shader+Stage) - The pixel-shader stage receives interpolated data for a primitive and generates per-pixel data such as color.</span></span>
-   <span data-ttu-id="5d97a-126">[輸出合併階段](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md) -輸出合併階段負責將各種類型的輸出資料結合 (圖元著色器值、深度和樣板資訊) 與轉譯目標的內容和深度/樣板緩衝區，以產生最終的管線結果。</span><span class="sxs-lookup"><span data-stu-id="5d97a-126">[Output-Merger Stage](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md) - The output-merger stage is responsible for combining various types of output data (pixel shader values, depth and stencil information) with the contents of the render target and depth/stencil buffers to generate the final pipeline result.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5d97a-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="5d97a-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d97a-128">Direct3D 10 程式設計手冊</span><span class="sxs-lookup"><span data-stu-id="5d97a-128">Programming Guide for Direct3D 10</span></span>](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
