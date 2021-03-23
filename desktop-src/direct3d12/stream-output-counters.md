---
title: 串流輸出計數器
description: 資料流程輸出是 GPU 將頂點寫入緩衝區的能力。 資料流程輸出計數器會監視進度。
ms.assetid: 7342DA09-25E9-4154-83BA-B03ADBB8B671
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df4d2f3a823f5f4b5d2d5f365235d7e3f8817207
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103616"
---
# <a name="stream-output-counters"></a><span data-ttu-id="6bf92-104">串流輸出計數器</span><span class="sxs-lookup"><span data-stu-id="6bf92-104">Stream Output Counters</span></span>

<span data-ttu-id="6bf92-105">資料流程輸出是 GPU 將頂點寫入緩衝區的能力。</span><span class="sxs-lookup"><span data-stu-id="6bf92-105">Stream output is the ability of the GPU to write vertices to a buffer.</span></span> <span data-ttu-id="6bf92-106">資料流程輸出計數器會監視進度。</span><span class="sxs-lookup"><span data-stu-id="6bf92-106">The stream output counters monitor progress.</span></span>

-   [<span data-ttu-id="6bf92-107">從 Direct3D 11 到 Direct3D 12 的資料流程計數器差異</span><span class="sxs-lookup"><span data-stu-id="6bf92-107">Differences in Stream Counters from Direct3D 11 to Direct3D 12</span></span>](#differences-in-stream-counters-from-direct3d-11-to-direct3d-12)
-   [<span data-ttu-id="6bf92-108">BufferFilledSize</span><span class="sxs-lookup"><span data-stu-id="6bf92-108">BufferFilledSize</span></span>](#bufferfilledsize)
-   [<span data-ttu-id="6bf92-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="6bf92-109">Related topics</span></span>](#related-topics)

## <a name="differences-in-stream-counters-from-direct3d-11-to-direct3d-12"></a><span data-ttu-id="6bf92-110">從 Direct3D 11 到 Direct3D 12 的資料流程計數器差異</span><span class="sxs-lookup"><span data-stu-id="6bf92-110">Differences in Stream Counters from Direct3D 11 to Direct3D 12</span></span>

<span data-ttu-id="6bf92-111">在資料流程輸出流程中，GPU 必須知道其寫入緩衝區中的目前位置。</span><span class="sxs-lookup"><span data-stu-id="6bf92-111">As a part of the stream output process, the GPU has to know the current location in the buffer that it is writing to.</span></span> <span data-ttu-id="6bf92-112">在 Direct3D 11 中，用來儲存這個位置的記憶體是由驅動程式配置，而應用程式用來操作此值的唯一方法是透過 **SOSetTargets** 方法。</span><span class="sxs-lookup"><span data-stu-id="6bf92-112">In Direct3D 11, memory to store this location is allocated by the driver and the only way for applications to manipulate this value is via the **SOSetTargets** method.</span></span> <span data-ttu-id="6bf92-113">在 Direct3D 12 中，應用程式會配置記憶體來儲存這個目前的位置。</span><span class="sxs-lookup"><span data-stu-id="6bf92-113">In Direct3D 12, apps allocate memory to store this current location.</span></span> <span data-ttu-id="6bf92-114">沒有特殊的方法可以操作此值，而且應用程式可以自由地使用 CPU 或 GPU 來讀取/寫入值。</span><span class="sxs-lookup"><span data-stu-id="6bf92-114">There are no special ways to manipulate this value, and apps are free to read/write the value with the CPU or GPU.</span></span>

## <a name="bufferfilledsize"></a><span data-ttu-id="6bf92-115">BufferFilledSize</span><span class="sxs-lookup"><span data-stu-id="6bf92-115">BufferFilledSize</span></span>

<span data-ttu-id="6bf92-116">應用程式負責配置32位數量的儲存體（稱為 *BufferFilledSize*）。</span><span class="sxs-lookup"><span data-stu-id="6bf92-116">The application is responsible for allocating storage for a 32-bit quantity called the *BufferFilledSize*.</span></span> <span data-ttu-id="6bf92-117">這包含資料流程輸出緩衝區中的資料位元組數。</span><span class="sxs-lookup"><span data-stu-id="6bf92-117">This contains the number of bytes of data in the stream-output buffer.</span></span> <span data-ttu-id="6bf92-118">此儲存體可放置在與包含資料流程輸出資料的資源相同或不同的資源中。</span><span class="sxs-lookup"><span data-stu-id="6bf92-118">This storage can be placed in the same, or a different, resource as the one that contains the stream-output data.</span></span> <span data-ttu-id="6bf92-119">此值是由資料流程輸出階段中的 GPU 所存取，以決定要在緩衝區中附加新頂點資料的位置。</span><span class="sxs-lookup"><span data-stu-id="6bf92-119">This value is accessed by the GPU in the stream-output stage to determine where to append new vertex data in the buffer.</span></span> <span data-ttu-id="6bf92-120">此外，GPU 會存取此值以判斷何時發生溢位。</span><span class="sxs-lookup"><span data-stu-id="6bf92-120">Additionally, this value is accessed by the GPU to determine when overflow has occurred.</span></span>

<span data-ttu-id="6bf92-121">請參閱結構 [**D3D12 \_ 資料流程 \_ 輸出 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc)。</span><span class="sxs-lookup"><span data-stu-id="6bf92-121">Refer to the structure [**D3D12\_STREAM\_OUTPUT\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc).</span></span>

<span data-ttu-id="6bf92-122">Debug 層會驗證 [**ID3D12GraphicsCommandList：： SOSetTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-sosettargets)中的下列事項：</span><span class="sxs-lookup"><span data-stu-id="6bf92-122">The debug layer will validate the following in [**ID3D12GraphicsCommandList::SOSetTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-sosettargets):</span></span>

-   <span data-ttu-id="6bf92-123">如果指定了非 Null 的資源， *BufferFilledSize* 就會落在 {*OffsetInBytes*， *SizeInBytes*} 所隱含的範圍內。</span><span class="sxs-lookup"><span data-stu-id="6bf92-123">*BufferFilledSize* falls in the range implied by {*OffsetInBytes*, *SizeInBytes*}, if a non-NULL resource is specified.</span></span>
-   <span data-ttu-id="6bf92-124">*BufferFilledSizeOffsetInBytes* 是4的倍數。</span><span class="sxs-lookup"><span data-stu-id="6bf92-124">*BufferFilledSizeOffsetInBytes* is a multiple of 4.</span></span>
-   <span data-ttu-id="6bf92-125">*BufferFilledSizeOffsetInBytes* 在包含資源的範圍內。</span><span class="sxs-lookup"><span data-stu-id="6bf92-125">*BufferFilledSizeOffsetInBytes* is within the range of the containing resource.</span></span>
-   <span data-ttu-id="6bf92-126">指定的資源是緩衝區。</span><span class="sxs-lookup"><span data-stu-id="6bf92-126">The specified resource is a buffer.</span></span>

<span data-ttu-id="6bf92-127">執行時間不會驗證與資料流程輸出緩衝區相關聯的堆積型別，因為所有堆積類型都支援資料流程輸出。</span><span class="sxs-lookup"><span data-stu-id="6bf92-127">The runtime will not validate the heap type associated with the stream output buffer, as stream output is supported in all heap types.</span></span>

<span data-ttu-id="6bf92-128">根簽章必須使用 [**D3D12 根簽章 \_ \_ \_ 旗**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) 標旗標來指定是否要使用資料流程輸出。</span><span class="sxs-lookup"><span data-stu-id="6bf92-128">Root signatures must specify if stream output will be used, by using the [**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags.</span></span>

<span data-ttu-id="6bf92-129">D3D12 \_ 根簽章 \_ \_ 旗 \_ \_ 標允許串流 \_ 輸出可針對以 HLSL 撰寫的根簽章指定，其方式類似于指定其他旗標的方式。</span><span class="sxs-lookup"><span data-stu-id="6bf92-129">D3D12\_ROOT\_SIGNATURE\_FLAG\_ALLOW\_STREAM\_OUTPUT can be specified for root signatures authored in HLSL, in a manner similar to how the other flags are specified.</span></span>

<span data-ttu-id="6bf92-130">[](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate)如果幾何著色器包含資料流程輸出，但根簽章沒有 D3D12 的根簽章旗標 \_ \_ \_ \_ 允許 \_ 串流 \_ 輸出旗標，則 CreateGraphicsPipelineState 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="6bf92-130">[**CreateGraphicsPipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) will fail if the geometry shader contains stream-output but the root signature does not have the D3D12\_ROOT\_SIGNATURE\_FLAG\_ALLOW\_STREAM\_OUTPUT flag set.</span></span>

<span data-ttu-id="6bf92-131">當資源當做資料流程輸出目標使用時，使用的資源必須處於 D3D12 \_ 資源 \_ 狀態 \_ 資料流程輸出 \_ 狀態。</span><span class="sxs-lookup"><span data-stu-id="6bf92-131">When a resource is used as a stream-output target, the resources used must be in the D3D12\_RESOURCE\_STATE\_STREAM\_OUT state.</span></span> <span data-ttu-id="6bf92-132">這同時適用于頂點資料和 *BufferFilledSize* (，其可位於相同或不同的資源) 。</span><span class="sxs-lookup"><span data-stu-id="6bf92-132">This applies to both the vertex data and the *BufferFilledSize* (which can be in the same or separate resources).</span></span>

<span data-ttu-id="6bf92-133">沒有特殊的 Api 可設定資料流程輸出緩衝區位移，因為應用程式可以直接使用 CPU 或 GPU 寫入 *BufferFilledSize* 。</span><span class="sxs-lookup"><span data-stu-id="6bf92-133">There are no special APIs to set stream-output buffer offsets because applications can write to the *BufferFilledSize* with the CPU or GPU directly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6bf92-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="6bf92-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6bf92-135">計數器和查詢</span><span class="sxs-lookup"><span data-stu-id="6bf92-135">Counters and Queries</span></span>](counters-and-queries.md)
</dt> </dl>

 

 




