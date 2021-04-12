---
title: Stream-Output 階段
description: 資料流程輸出階段的目的是要持續輸出 (或串流) 頂點資料從幾何著色器階段 (或頂點著色器階段（如果幾何著色器階段非使用中) 至記憶體中的一或多個緩衝區） (請參閱開始使用階段 Stream-Output。
ms.assetid: f902dc93-9612-481b-a6bd-073e924a4c79
keywords:
- " (Direct3D 10) 的資料流程輸出階段"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0879cde2ba2f1bb3ed9cc6121aaf378cd4af312
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104463952"
---
# <a name="stream-output-stage"></a><span data-ttu-id="94f84-104">Stream-Output 階段</span><span class="sxs-lookup"><span data-stu-id="94f84-104">Stream-Output Stage</span></span>

<span data-ttu-id="94f84-105">資料流程輸出階段的目的是要持續輸出 (或串流) 頂點資料從幾何著色器階段 (或頂點著色器階段（如果幾何著色器階段非使用中) 至記憶體中的一或多個緩衝區） (請參閱開始使用 [階段](d3d10-graphics-programming-guide-output-stream-stage-getting-started.md) Stream-Output。</span><span class="sxs-lookup"><span data-stu-id="94f84-105">The purpose of the stream-output stage is to continuously output (or stream) vertex data from the geometry-shader stage (or the vertex-shader stage if the geometry-shader stage is inactive) to one or more buffers in memory (see [Getting Started with the Stream-Output Stage](d3d10-graphics-programming-guide-output-stream-stage-getting-started.md)).</span></span>

<span data-ttu-id="94f84-106">資料流程輸出階段 (所以) 位於幾何著色器階段之後，緊接在點陣化階段之前的管線中，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="94f84-106">The stream-output stage (SO) is located in the pipeline right after the geometry-shader stage and just before the rasterization stage, as shown in the following diagram.</span></span>

![在管線中資料流輸出階段的位置圖](images/d3d10-pipeline-stages-so.png)

<span data-ttu-id="94f84-108">串流輸出到記憶體的資料可在後續轉譯行程中讀回到管線，或者可以複製到預備環境資源（讓它可供 CPU 讀取）。</span><span class="sxs-lookup"><span data-stu-id="94f84-108">Data streamed out to memory can be read back into the pipeline in a subsequent rendering pass, or can be copied to a staging resource (so it can be read by the CPU).</span></span> <span data-ttu-id="94f84-109">資料流程處理的資料量可能不同; [**>id3d11devicecoNtext：:D rawauto**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawauto) API 是設計用來處理資料，而不需要對寫入的資料量 (的 GPU) 進行查詢。</span><span class="sxs-lookup"><span data-stu-id="94f84-109">The amount of data streamed out can vary; the [**ID3D11DeviceContext::DrawAuto**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawauto) API is designed to handle the data without the need to query (the GPU) about the amount of data written.</span></span>

<span data-ttu-id="94f84-110">當三角形或行帶系結至輸入組合語言階段時，每個區域會先轉換成清單，再進行資料流程處理。頂點一律會寫出做為完整的基本專案 (例如，一次有3個頂點用於三角形) ;未完成的基本專案永遠不會串流處理。具有相鄰性的基本型別會捨棄相鄰資料，然後再將資料串流。</span><span class="sxs-lookup"><span data-stu-id="94f84-110">When a triangle or line strip is bound to the input-assembler stage, each strip is converted into a list before they are streamed out. Vertices are always written out as complete primitives (for example, 3 vertices at a time for triangles); incomplete primitives are never streamed out. Primitive types with adjacency discard the adjacency data before streaming data out.</span></span>

<span data-ttu-id="94f84-111">有兩種方式可將資料流輸出資料饋送至管線：</span><span class="sxs-lookup"><span data-stu-id="94f84-111">There are two ways to feed stream-output data into the pipeline:</span></span>

-   <span data-ttu-id="94f84-112">資料流程-輸出資料可以回送至輸入組合語言階段。</span><span class="sxs-lookup"><span data-stu-id="94f84-112">Stream-output data can be fed back into the input-assembler stage.</span></span>
-   <span data-ttu-id="94f84-113">您可以使用載入函數 (（例如 [load](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-load)) ），利用可程式化的著色器來讀取資料流程輸出資料。</span><span class="sxs-lookup"><span data-stu-id="94f84-113">Stream-output data can be read by programmable shaders using load functions (such as [Load](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-load)).</span></span>

<span data-ttu-id="94f84-114">若要使用緩衝區作為資料流程輸出資源，請使用 D3D11 系結 [**\_ \_ 資料流程 \_ 輸出**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) 旗標建立緩衝區。</span><span class="sxs-lookup"><span data-stu-id="94f84-114">To use a buffer as a stream-output resource, create the buffer with the [**D3D11\_BIND\_STREAM\_OUTPUT**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) flag.</span></span> <span data-ttu-id="94f84-115">資料流輸出階段同時支援最多 4 個緩衝區。</span><span class="sxs-lookup"><span data-stu-id="94f84-115">The stream-output stage supports up to 4 buffers simultaneously.</span></span>

-   <span data-ttu-id="94f84-116">如果您要串流資料到多個緩衝區，每個緩衝區只可以擷取每個頂點資料的單一元素（最多 4 個元件），隱含的資料分散等於每個緩衝區中的元素寬度（相容於單一元素可繫結以供輸入到著色器階段的方式）。</span><span class="sxs-lookup"><span data-stu-id="94f84-116">If you are streaming data into multiple buffers, each buffer can only capture a single element (up to 4 components) of per-vertex data, with an implied data stride equal to the element width in each buffer (compatible with the way single element buffers can be bound for input into shader stages).</span></span> <span data-ttu-id="94f84-117">此外，如果緩衝區有不同的大小，其中一個緩衝區已滿時寫入會立即停止。</span><span class="sxs-lookup"><span data-stu-id="94f84-117">Furthermore, if the buffers have different sizes, writing stops as soon as any one of the buffers is full.</span></span>
-   <span data-ttu-id="94f84-118">如果您要串流資料到單一緩衝區，緩衝區可以擷取每個頂點資料最多 64 個純量元件 (256 位元組或更少)，或者頂點分散可能是 2048 位元組。</span><span class="sxs-lookup"><span data-stu-id="94f84-118">If you are streaming data into a single buffer, the buffer can capture up to 64 scalar components of per-vertex data (256 bytes or less) or the vertex stride can be up to 2048 bytes.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="94f84-119">本節內容</span><span class="sxs-lookup"><span data-stu-id="94f84-119">In this section</span></span>



| <span data-ttu-id="94f84-120">主題</span><span class="sxs-lookup"><span data-stu-id="94f84-120">Topic</span></span>                                                                                                                               | <span data-ttu-id="94f84-121">描述</span><span class="sxs-lookup"><span data-stu-id="94f84-121">Description</span></span>                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="94f84-122">使用 Stream-Output 階段開始使用</span><span class="sxs-lookup"><span data-stu-id="94f84-122">Getting Started with the Stream-Output Stage</span></span>](d3d10-graphics-programming-guide-output-stream-stage-getting-started.md)<br/> | <span data-ttu-id="94f84-123">本節說明如何搭配資料流程輸出階段使用幾何著色器。</span><span class="sxs-lookup"><span data-stu-id="94f84-123">This section describes how to use a geometry shader with the stream output stage.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="94f84-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="94f84-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94f84-125">圖形管線</span><span class="sxs-lookup"><span data-stu-id="94f84-125">Graphics Pipeline</span></span>](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[<span data-ttu-id="94f84-126"> (Direct3D 10) 的管線階段 </span><span class="sxs-lookup"><span data-stu-id="94f84-126">Pipeline Stages (Direct3D 10)</span></span>](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

