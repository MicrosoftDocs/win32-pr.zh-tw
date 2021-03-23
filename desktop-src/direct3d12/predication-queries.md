---
title: Predication 查詢
description: D3D12PredicationQueries 範例示範如何使用 DirectX 12 查詢堆積和 predication 來挑選遮蔽。 本逐步解說將說明擴充 HelloConstBuffer 範例以處理 predication 查詢所需的其他程式碼。
ms.assetid: F61817BB-45BC-4977-BE4A-EE0FDAFBCB57
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad14e55864ee8d568acc0c9eb46134834d27ff54
ms.sourcegitcommit: 4c00910ed754d7d0a68c9a833751d714c06e3b39
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "104548343"
---
# <a name="predication-queries"></a><span data-ttu-id="80ee2-104">Predication 查詢</span><span class="sxs-lookup"><span data-stu-id="80ee2-104">Predication queries</span></span>

<span data-ttu-id="80ee2-105">**D3D12PredicationQueries** 範例示範如何使用 DirectX 12 查詢堆積和 predication 來挑選遮蔽。</span><span class="sxs-lookup"><span data-stu-id="80ee2-105">The **D3D12PredicationQueries** sample demonstrates occlusion culling using DirectX 12 query heaps and predication.</span></span> <span data-ttu-id="80ee2-106">本逐步解說將說明擴充 **HelloConstBuffer** 範例以處理 predication 查詢所需的其他程式碼。</span><span class="sxs-lookup"><span data-stu-id="80ee2-106">The walkthrough describes the additional code needed to extend the **HelloConstBuffer** sample to handle predication queries.</span></span>

-   [<span data-ttu-id="80ee2-107">建立深度樣板描述元堆積和遮蔽查詢堆積</span><span class="sxs-lookup"><span data-stu-id="80ee2-107">Create a depth stencil descriptor heap and an occlusion query heap</span></span>](#create-a-depth-stencil-descriptor-heap-and-an-occlusion-query-heap)
-   [<span data-ttu-id="80ee2-108">啟用 Alpha 混色</span><span class="sxs-lookup"><span data-stu-id="80ee2-108">Enable alpha blending</span></span>](#enable-alpha-blending)
-   [<span data-ttu-id="80ee2-109">停用色彩和深度寫入</span><span class="sxs-lookup"><span data-stu-id="80ee2-109">Disable color and depth writes</span></span>](#disable-color-and-depth-writes)
-   [<span data-ttu-id="80ee2-110">建立緩衝區來儲存查詢的結果</span><span class="sxs-lookup"><span data-stu-id="80ee2-110">Create a buffer to store the results of the query</span></span>](#create-a-buffer-to-store-the-results-of-the-query)
-   [<span data-ttu-id="80ee2-111">繪製四邊形並執行和解決遮蔽查詢</span><span class="sxs-lookup"><span data-stu-id="80ee2-111">Draw the quads and perform and resolve the occlusion query</span></span>](#draw-the-quads-and-perform-and-resolve-the-occlusion-query)
-   [<span data-ttu-id="80ee2-112">執行範例</span><span class="sxs-lookup"><span data-stu-id="80ee2-112">Run the sample</span></span>](#run-the-sample)
-   [<span data-ttu-id="80ee2-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="80ee2-113">Related topics</span></span>](#related-topics)

## <a name="create-a-depth-stencil-descriptor-heap-and-an-occlusion-query-heap"></a><span data-ttu-id="80ee2-114">建立深度樣板描述元堆積和遮蔽查詢堆積</span><span class="sxs-lookup"><span data-stu-id="80ee2-114">Create a depth stencil descriptor heap and an occlusion query heap</span></span>

<span data-ttu-id="80ee2-115">在 **LoadPipeline** 方法中，建立深度樣板描述元堆積。</span><span class="sxs-lookup"><span data-stu-id="80ee2-115">In the **LoadPipeline** method create a depth stencil descriptor heap.</span></span>

``` syntax
              // Describe and create a depth stencil view (DSV) descriptor heap.
              D3D12_DESCRIPTOR_HEAP_DESC dsvHeapDesc = {};
              dsvHeapDesc.NumDescriptors = 1;
              dsvHeapDesc.Type = D3D12_DESCRIPTOR_HEAP_TYPE_DSV;
              dsvHeapDesc.Flags = D3D12_DESCRIPTOR_HEAP_FLAG_NONE;
              ThrowIfFailed(m_device->CreateDescriptorHeap(&dsvHeapDesc, IID_PPV_ARGS(&m_dsvHeap)));
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="80ee2-116">呼叫流程</span><span class="sxs-lookup"><span data-stu-id="80ee2-116">Call flow</span></span></th>
<th><span data-ttu-id="80ee2-117">參數</span><span class="sxs-lookup"><span data-stu-id="80ee2-117">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="80ee2-118"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc"><strong>D3D12_DESCRIPTOR_HEAP_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="80ee2-118"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc"><strong>D3D12_DESCRIPTOR_HEAP_DESC</strong></a></span></span></td>
<td><dl><span data-ttu-id="80ee2-119"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type"><strong>D3D12_DESCRIPTOR_HEAP_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="80ee2-119"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type"><strong>D3D12_DESCRIPTOR_HEAP_TYPE</strong></a></span></span><br />
<span data-ttu-id="80ee2-120">[<strong>D3D12_DESCRIPTOR_HEAP_FLAG</strong>] (/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_flags) </span><span class="sxs-lookup"><span data-stu-id="80ee2-120">[<strong>D3D12_DESCRIPTOR_HEAP_FLAG</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_flags)</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="80ee2-121"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap"><strong>CreateDescriptorHeap</strong></a></span><span class="sxs-lookup"><span data-stu-id="80ee2-121"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap"><strong>CreateDescriptorHeap</strong></a></span></span></td>

</tr>
</tbody>
</table>



 

<span data-ttu-id="80ee2-122">在 **LoadAssets** 方法中，建立遮蔽查詢的堆積。</span><span class="sxs-lookup"><span data-stu-id="80ee2-122">In the **LoadAssets** method create a heap for occlusion queries.</span></span>

``` syntax
     // Describe and create a heap for occlusion queries.
              D3D12_QUERY_HEAP_DESC queryHeapDesc = {};
              queryHeapDesc.Count = 1;
              queryHeapDesc.Type = D3D12_QUERY_HEAP_TYPE_OCCLUSION;
              ThrowIfFailed(m_device->CreateQueryHeap(&queryHeapDesc, IID_PPV_ARGS(&m_queryHeap)));
```



| <span data-ttu-id="80ee2-123">呼叫流程</span><span class="sxs-lookup"><span data-stu-id="80ee2-123">Call flow</span></span>                                                 | <span data-ttu-id="80ee2-124">參數</span><span class="sxs-lookup"><span data-stu-id="80ee2-124">Parameters</span></span>                                                |
|-----------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="80ee2-125">**D3D12 \_ 查詢 \_ 堆積 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="80ee2-125">**D3D12\_QUERY\_HEAP\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_query_heap_desc) | [<span data-ttu-id="80ee2-126">**D3D12 \_ 查詢 \_ 堆積 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="80ee2-126">**D3D12\_QUERY\_HEAP\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_heap_type) |
| [<span data-ttu-id="80ee2-127">**CreateQueryHeap**</span><span class="sxs-lookup"><span data-stu-id="80ee2-127">**CreateQueryHeap**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createqueryheap)   |                                                           |



 

## <a name="enable-alpha-blending"></a><span data-ttu-id="80ee2-128">啟用 Alpha 混色</span><span class="sxs-lookup"><span data-stu-id="80ee2-128">Enable alpha blending</span></span>

<span data-ttu-id="80ee2-129">此範例會繪製兩個四邊形，並說明二元遮蔽查詢。</span><span class="sxs-lookup"><span data-stu-id="80ee2-129">This sample draws two quads and illustrates a binary occlusion query.</span></span> <span data-ttu-id="80ee2-130">上面的四個視窗會在螢幕上以動畫顯示，而其中一個會偶爾 pixels occluded。</span><span class="sxs-lookup"><span data-stu-id="80ee2-130">The quad in front animates across the screen, and the one in back will occasionally be occluded.</span></span> <span data-ttu-id="80ee2-131">在 **LoadAssets** 方法中，會針對此範例啟用 Alpha 混合，讓我們可以看到，D3D 會將四個 pixels occluded 視為背面的四個點。</span><span class="sxs-lookup"><span data-stu-id="80ee2-131">In the **LoadAssets** method, alpha blending is enabled for this sample so that we can see at what point D3D considers the quad in back occluded.</span></span>

``` syntax
     // Enable alpha blending so we can visualize the occlusion query results.
              CD3DX12_BLEND_DESC blendDesc(CD3DX12_DEFAULT);
              blendDesc.RenderTarget[0] =
              {
                     TRUE, FALSE,
                     D3D12_BLEND_SRC_ALPHA, D3D12_BLEND_INV_SRC_ALPHA, D3D12_BLEND_OP_ADD,
                     D3D12_BLEND_ONE, D3D12_BLEND_ZERO, D3D12_BLEND_OP_ADD,
                     D3D12_LOGIC_OP_NOOP,
                     D3D12_COLOR_WRITE_ENABLE_ALL,
              };
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="80ee2-132">呼叫流程</span><span class="sxs-lookup"><span data-stu-id="80ee2-132">Call flow</span></span></th>
<th><span data-ttu-id="80ee2-133">參數</span><span class="sxs-lookup"><span data-stu-id="80ee2-133">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="80ee2-134"><a href="cd3dx12-blend-desc.md"><strong>CD3DX12_BLEND_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="80ee2-134"><a href="cd3dx12-blend-desc.md"><strong>CD3DX12_BLEND_DESC</strong></a></span></span></td>
<td><dl><span data-ttu-id="80ee2-135"><a href="cd3dx12-default.md"><strong>CD3DX12_DEFAULT</strong></a></span><span class="sxs-lookup"><span data-stu-id="80ee2-135"><a href="cd3dx12-default.md"><strong>CD3DX12_DEFAULT</strong></a></span></span><br />
<span data-ttu-id="80ee2-136">[<strong>D3D12_BLEND</strong>] (/windows/desktop/api/d3d12/ne-d3d12-d3d12_blend) </span><span class="sxs-lookup"><span data-stu-id="80ee2-136">[<strong>D3D12_BLEND</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_blend)</span></span><br />
<span data-ttu-id="80ee2-137">[<strong>D3D12_BLEND_OP</strong>] (/windows/desktop/api/d3d12/ne-d3d12-d3d12_blend_op) </span><span class="sxs-lookup"><span data-stu-id="80ee2-137">[<strong>D3D12_BLEND_OP</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_blend_op)</span></span><br />
<span data-ttu-id="80ee2-138">[<strong>D3D12_LOGIC_OP</strong>] (/windows/desktop/api/d3d12/ne-d3d12-d3d12_logic_op) </span><span class="sxs-lookup"><span data-stu-id="80ee2-138">[<strong>D3D12_LOGIC_OP</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_logic_op)</span></span><br />
<span data-ttu-id="80ee2-139">[<strong>D3D12_COLOR_WRITE_ENABLE</strong>] (/windows/desktop/api/d3d12/ne-d3d12-d3d12_color_write_enable) </span><span class="sxs-lookup"><span data-stu-id="80ee2-139">[<strong>D3D12_COLOR_WRITE_ENABLE</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_color_write_enable)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="disable-color-and-depth-writes"></a><span data-ttu-id="80ee2-140">停用色彩和深度寫入</span><span class="sxs-lookup"><span data-stu-id="80ee2-140">Disable color and depth writes</span></span>

<span data-ttu-id="80ee2-141">遮蔽查詢的執行方式是將四個部分的四個部分，涵蓋與我們想要測試可見度相同的區域。</span><span class="sxs-lookup"><span data-stu-id="80ee2-141">The occlusion query is performed by rendering a quad that covers the same area as the quad whose visibility we want to test.</span></span> <span data-ttu-id="80ee2-142">在更複雜的場景中，查詢可能是周框磁片區，而不是簡單的四個磁片區。</span><span class="sxs-lookup"><span data-stu-id="80ee2-142">In more complex scenes, the query would likely be a bounding volume, rather than a simple quad.</span></span> <span data-ttu-id="80ee2-143">無論是哪一種情況，都會建立新的管線狀態，以停用寫入轉譯目標和 z 緩衝區，讓遮蔽查詢本身不會影響轉譯行程的可見輸出。</span><span class="sxs-lookup"><span data-stu-id="80ee2-143">In either case, a new pipeline state is created that disables writing to the render target and the z buffer so that the occlusion query itself does not affect the visible output of the rendering pass.</span></span>

<span data-ttu-id="80ee2-144">在 **LoadAssets** 方法中，停用遮蔽查詢狀態的色彩寫入和深度寫入。</span><span class="sxs-lookup"><span data-stu-id="80ee2-144">In the **LoadAssets** method, disable color writes and depth writes for the occlusion query's state.</span></span>

``` syntax
 // Disable color writes and depth writes for the occlusion query's state.
              psoDesc.BlendState.RenderTarget[0].RenderTargetWriteMask = 0;
              psoDesc.DepthStencilState.DepthWriteMask = D3D12_DEPTH_WRITE_MASK_ZERO;

              ThrowIfFailed(m_device->CreateGraphicsPipelineState(&psoDesc, IID_PPV_ARGS(&m_queryState)));
```



| <span data-ttu-id="80ee2-145">呼叫流程</span><span class="sxs-lookup"><span data-stu-id="80ee2-145">Call flow</span></span>                                                                            | <span data-ttu-id="80ee2-146">參數</span><span class="sxs-lookup"><span data-stu-id="80ee2-146">Parameters</span></span>                                                  |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="80ee2-147">**D3D12 \_ 圖形 \_ 管線 \_ 狀態 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="80ee2-147">**D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) | [<span data-ttu-id="80ee2-148">**D3D12 \_ 深度 \_ 寫入 \_ 遮罩**</span><span class="sxs-lookup"><span data-stu-id="80ee2-148">**D3D12\_DEPTH\_WRITE\_MASK**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_depth_write_mask) |
| [<span data-ttu-id="80ee2-149">**CreateGraphicsPipelineState**</span><span class="sxs-lookup"><span data-stu-id="80ee2-149">**CreateGraphicsPipelineState**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate)      |                                                             |



 

## <a name="create-a-buffer-to-store-the-results-of-the-query"></a><span data-ttu-id="80ee2-150">建立緩衝區來儲存查詢的結果</span><span class="sxs-lookup"><span data-stu-id="80ee2-150">Create a buffer to store the results of the query</span></span>

<span data-ttu-id="80ee2-151">在 **LoadAssets** 方法中，必須建立緩衝區來儲存查詢的結果。</span><span class="sxs-lookup"><span data-stu-id="80ee2-151">In the **LoadAssets** method a buffer needs to be created to store the results of the query.</span></span> <span data-ttu-id="80ee2-152">每個查詢都需要在 GPU 記憶體中有8個位元組的空間。</span><span class="sxs-lookup"><span data-stu-id="80ee2-152">Each query requires 8 bytes of space in GPU memory.</span></span> <span data-ttu-id="80ee2-153">此範例只會執行一個查詢，為了簡單起見，可讀性會建立緩衝區大小 (，即使此函式呼叫將配置64K 的 GPU 記憶體頁面，大部分的實際應用程式都可能會建立較大的緩衝區) 。</span><span class="sxs-lookup"><span data-stu-id="80ee2-153">This sample only performs one query and for simplicity and readability creates a buffer exactly that size (even though this function call will allocate a 64K page of GPU memory - most real apps would likely create a larger buffer).</span></span>

``` syntax
 // Create the query result buffer.
              CD3DX12_HEAP_PROPERTIES heapProps(D3D12_HEAP_TYPE_DEFAULT);
              auto queryBufferDesc = CD3DX12_RESOURCE_DESC::Buffer(8);
              ThrowIfFailed(m_device->CreateCommittedResource(
                     &heapProps,
                     D3D12_HEAP_FLAG_NONE,
                     &queryBufferDesc,
                     D3D12_RESOURCE_STATE_GENERIC_READ,
                     nullptr,
                     IID_PPV_ARGS(&m_queryResult)
                     ));
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="80ee2-154">呼叫流程</span><span class="sxs-lookup"><span data-stu-id="80ee2-154">Call flow</span></span></th>
<th><span data-ttu-id="80ee2-155">參數</span><span class="sxs-lookup"><span data-stu-id="80ee2-155">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="80ee2-156"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>CreateCommittedResource</strong></a></span><span class="sxs-lookup"><span data-stu-id="80ee2-156"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>CreateCommittedResource</strong></a></span></span></td>
<td><dl><span data-ttu-id="80ee2-157"><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a></span><span class="sxs-lookup"><span data-stu-id="80ee2-157"><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a></span></span><br />
<span data-ttu-id="80ee2-158">[<strong>D3D12_HEAP_TYPE</strong>] (/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type) </span><span class="sxs-lookup"><span data-stu-id="80ee2-158">[<strong>D3D12_HEAP_TYPE</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)</span></span><br />
<span data-ttu-id="80ee2-159">[<strong>D3D12_HEAP_FLAG</strong>] (/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) </span><span class="sxs-lookup"><span data-stu-id="80ee2-159">[<strong>D3D12_HEAP_FLAG</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags)</span></span><br />
<span data-ttu-id="80ee2-160">[<strong>CD3DX12_RESOURCE_DESC</strong>] (cd3dx12-resource-desc.md) </span><span class="sxs-lookup"><span data-stu-id="80ee2-160">[<strong>CD3DX12_RESOURCE_DESC</strong>](cd3dx12-resource-desc.md)</span></span><br />
<span data-ttu-id="80ee2-161">[<strong>D3D12_RESOURCE_STATES</strong>] (/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) </span><span class="sxs-lookup"><span data-stu-id="80ee2-161">[<strong>D3D12_RESOURCE_STATES</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="draw-the-quads-and-perform-and-resolve-the-occlusion-query"></a><span data-ttu-id="80ee2-162">繪製四邊形並執行和解決遮蔽查詢</span><span class="sxs-lookup"><span data-stu-id="80ee2-162">Draw the quads and perform and resolve the occlusion query</span></span>

<span data-ttu-id="80ee2-163">完成設定之後，會在 **PopulateCommandLists** 方法中更新主要迴圈。</span><span class="sxs-lookup"><span data-stu-id="80ee2-163">Having done the setup, the main loop is updated in the **PopulateCommandLists** method.</span></span>

<dl> 1. <span data-ttu-id="80ee2-164">將四邊形從後到前繪製，讓透明效果能正常運作。</span><span class="sxs-lookup"><span data-stu-id="80ee2-164">Draw the quads from back to front to make the transparency effect work properly.</span></span> <span data-ttu-id="80ee2-165">將四個單元中的四個前提在上一個畫面格的查詢結果上，是相當常見的技巧。</span><span class="sxs-lookup"><span data-stu-id="80ee2-165">Drawing the quad in back to front is predicated on the result of the previous frame’s query and is a fairly common technique for this.</span></span>  
2. <span data-ttu-id="80ee2-166">變更 PSO 以停用轉譯目標和深度樣板寫入。</span><span class="sxs-lookup"><span data-stu-id="80ee2-166">Change the PSO to disable render target and depth stencil writes.</span></span>  
3. <span data-ttu-id="80ee2-167">執行遮蔽查詢。</span><span class="sxs-lookup"><span data-stu-id="80ee2-167">Perform the occlusion query.</span></span>  
4. <span data-ttu-id="80ee2-168">解析遮蔽查詢。</span><span class="sxs-lookup"><span data-stu-id="80ee2-168">Resolve the occlusion query.</span></span>  
</dl>

``` syntax
       // Draw the quads and perform the occlusion query.
       {
              CD3DX12_GPU_DESCRIPTOR_HANDLE cbvFarQuad(m_cbvHeap->GetGPUDescriptorHandleForHeapStart(), m_frameIndex * CbvCountPerFrame, m_cbvSrvDescriptorSize);
              CD3DX12_GPU_DESCRIPTOR_HANDLE cbvNearQuad(cbvFarQuad, m_cbvSrvDescriptorSize);

              m_commandList->IASetPrimitiveTopology(D3D_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP);
              m_commandList->IASetVertexBuffers(0, 1, &m_vertexBufferView);

              // Draw the far quad conditionally based on the result of the occlusion query
              // from the previous frame.
              m_commandList->SetGraphicsRootDescriptorTable(0, cbvFarQuad);
              m_commandList->SetPredication(m_queryResult.Get(), 0, D3D12_PREDICATION_OP_EQUAL_ZERO);
              m_commandList->DrawInstanced(4, 1, 0, 0);

              // Disable predication and always draw the near quad.
              m_commandList->SetPredication(nullptr, 0, D3D12_PREDICATION_OP_EQUAL_ZERO);
              m_commandList->SetGraphicsRootDescriptorTable(0, cbvNearQuad);
              m_commandList->DrawInstanced(4, 1, 4, 0);

              // Run the occlusion query with the bounding box quad.
              m_commandList->SetGraphicsRootDescriptorTable(0, cbvFarQuad);
              m_commandList->SetPipelineState(m_queryState.Get());
              m_commandList->BeginQuery(m_queryHeap.Get(), D3D12_QUERY_TYPE_BINARY_OCCLUSION, 0);
              m_commandList->DrawInstanced(4, 1, 8, 0);
              m_commandList->EndQuery(m_queryHeap.Get(), D3D12_QUERY_TYPE_BINARY_OCCLUSION, 0);

              // Resolve the occlusion query and store the results in the query result buffer
              // to be used on the subsequent frame.
              m_commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_queryResult.Get(), D3D12_RESOURCE_STATE_GENERIC_READ, D3D12_RESOURCE_STATE_COPY_DEST));
              m_commandList->ResolveQueryData(m_queryHeap.Get(), D3D12_QUERY_TYPE_BINARY_OCCLUSION, 0, 1, m_queryResult.Get(), 0);
              m_commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_queryResult.Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_GENERIC_READ));
       }
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="80ee2-169">呼叫流程</span><span class="sxs-lookup"><span data-stu-id="80ee2-169">Call flow</span></span></th>
<th><span data-ttu-id="80ee2-170">參數</span><span class="sxs-lookup"><span data-stu-id="80ee2-170">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="80ee2-171"><a href="cd3dx12-gpu-descriptor-handle.md"><strong>CD3DX12_GPU_DESCRIPTOR_HANDLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="80ee2-171"><a href="cd3dx12-gpu-descriptor-handle.md"><strong>CD3DX12_GPU_DESCRIPTOR_HANDLE</strong></a></span></span></td>
<td><span data-ttu-id="80ee2-172"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart"><strong>GetGPUDescriptorHandleForHeapStart</strong></a></span><span class="sxs-lookup"><span data-stu-id="80ee2-172"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart"><strong>GetGPUDescriptorHandleForHeapStart</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="80ee2-173"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetprimitivetopology"><strong>IASetPrimitiveTopology</strong></a></span><span class="sxs-lookup"><span data-stu-id="80ee2-173"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetprimitivetopology"><strong>IASetPrimitiveTopology</strong></a></span></span></td>
<td><span data-ttu-id="80ee2-174"><a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_primitive_topology"><strong>D3D_PRIMITIVE_TOPOLOGY</strong></a></span><span class="sxs-lookup"><span data-stu-id="80ee2-174"><a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_primitive_topology"><strong>D3D_PRIMITIVE_TOPOLOGY</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="80ee2-175"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers"><strong>IASetVertexBuffers</strong></a></span><span class="sxs-lookup"><span data-stu-id="80ee2-175"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers"><strong>IASetVertexBuffers</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="80ee2-176"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable"><strong>SetGraphicsRootDescriptorTable</strong></a></span><span class="sxs-lookup"><span data-stu-id="80ee2-176"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable"><strong>SetGraphicsRootDescriptorTable</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="80ee2-177"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication"><strong>SetPredication</strong></a></span><span class="sxs-lookup"><span data-stu-id="80ee2-177"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication"><strong>SetPredication</strong></a></span></span></td>
<td><span data-ttu-id="80ee2-178"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_predication_op"><strong>D3D12_PREDICATION_OP</strong></a></span><span class="sxs-lookup"><span data-stu-id="80ee2-178"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_predication_op"><strong>D3D12_PREDICATION_OP</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="80ee2-179"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced"><strong>DrawInstanced</strong></a></span><span class="sxs-lookup"><span data-stu-id="80ee2-179"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced"><strong>DrawInstanced</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="80ee2-180"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication"><strong>SetPredication</strong></a></span><span class="sxs-lookup"><span data-stu-id="80ee2-180"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication"><strong>SetPredication</strong></a></span></span></td>
<td><span data-ttu-id="80ee2-181"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_predication_op"><strong>D3D12_PREDICATION_OP</strong></a></span><span class="sxs-lookup"><span data-stu-id="80ee2-181"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_predication_op"><strong>D3D12_PREDICATION_OP</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="80ee2-182"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable"><strong>SetGraphicsRootDescriptorTable</strong></a></span><span class="sxs-lookup"><span data-stu-id="80ee2-182"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable"><strong>SetGraphicsRootDescriptorTable</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="80ee2-183"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced"><strong>DrawInstanced</strong></a></span><span class="sxs-lookup"><span data-stu-id="80ee2-183"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced"><strong>DrawInstanced</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="80ee2-184"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable"><strong>SetGraphicsRootDescriptorTable</strong></a></span><span class="sxs-lookup"><span data-stu-id="80ee2-184"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable"><strong>SetGraphicsRootDescriptorTable</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="80ee2-185"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate"><strong>SetPipelineState</strong></a></span><span class="sxs-lookup"><span data-stu-id="80ee2-185"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate"><strong>SetPipelineState</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="80ee2-186"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery"><strong>BeginQuery</strong></a></span><span class="sxs-lookup"><span data-stu-id="80ee2-186"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery"><strong>BeginQuery</strong></a></span></span></td>
<td><span data-ttu-id="80ee2-187"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type"><strong>D3D12_QUERY_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="80ee2-187"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type"><strong>D3D12_QUERY_TYPE</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="80ee2-188"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced"><strong>DrawInstanced</strong></a></span><span class="sxs-lookup"><span data-stu-id="80ee2-188"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced"><strong>DrawInstanced</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="80ee2-189"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery"><strong>EndQuery</strong></a></span><span class="sxs-lookup"><span data-stu-id="80ee2-189"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery"><strong>EndQuery</strong></a></span></span></td>
<td><span data-ttu-id="80ee2-190"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type"><strong>D3D12_QUERY_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="80ee2-190"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type"><strong>D3D12_QUERY_TYPE</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="80ee2-191"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></span><span class="sxs-lookup"><span data-stu-id="80ee2-191"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></span></span></td>
<td><dl><span data-ttu-id="80ee2-192"><a href="cd3dx12-resource-barrier.md"><strong>CD3DX12_RESOURCE_BARRIER</strong></a></span><span class="sxs-lookup"><span data-stu-id="80ee2-192"><a href="cd3dx12-resource-barrier.md"><strong>CD3DX12_RESOURCE_BARRIER</strong></a></span></span><br />
<span data-ttu-id="80ee2-193">[<strong>D3D12_RESOURCE_STATES</strong>] (/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) </span><span class="sxs-lookup"><span data-stu-id="80ee2-193">[<strong>D3D12_RESOURCE_STATES</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states)</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="80ee2-194"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata"><strong>ResolveQueryData</strong></a></span><span class="sxs-lookup"><span data-stu-id="80ee2-194"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata"><strong>ResolveQueryData</strong></a></span></span></td>
<td><span data-ttu-id="80ee2-195"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type"><strong>D3D12_QUERY_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="80ee2-195"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type"><strong>D3D12_QUERY_TYPE</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="80ee2-196"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></span><span class="sxs-lookup"><span data-stu-id="80ee2-196"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></span></span></td>
<td><dl><span data-ttu-id="80ee2-197"><a href="cd3dx12-resource-barrier.md"><strong>CD3DX12_RESOURCE_BARRIER</strong></a></span><span class="sxs-lookup"><span data-stu-id="80ee2-197"><a href="cd3dx12-resource-barrier.md"><strong>CD3DX12_RESOURCE_BARRIER</strong></a></span></span><br />
<span data-ttu-id="80ee2-198">[<strong>D3D12_RESOURCE_STATES</strong>] (/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) </span><span class="sxs-lookup"><span data-stu-id="80ee2-198">[<strong>D3D12_RESOURCE_STATES</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="run-the-sample"></a><span data-ttu-id="80ee2-199">執行範例</span><span class="sxs-lookup"><span data-stu-id="80ee2-199">Run the sample</span></span>

<span data-ttu-id="80ee2-200">未 pixels occluded：</span><span class="sxs-lookup"><span data-stu-id="80ee2-200">Not occluded:</span></span>

![兩個方塊未 pixels occluded](images/not-occluded.png)

<span data-ttu-id="80ee2-202">閉塞：</span><span class="sxs-lookup"><span data-stu-id="80ee2-202">Occluded:</span></span>

![一個 box 完全 pixels occluded](images/occluded.png)

<span data-ttu-id="80ee2-204">部分 pixels occluded：</span><span class="sxs-lookup"><span data-stu-id="80ee2-204">Partially occluded:</span></span>

![一個 box 部分 pixels occluded](images/partially-occluded.png)

## <a name="related-topics"></a><span data-ttu-id="80ee2-206">相關主題</span><span class="sxs-lookup"><span data-stu-id="80ee2-206">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80ee2-207">D3D12 程式碼逐步解說-解說</span><span class="sxs-lookup"><span data-stu-id="80ee2-207">D3D12 Code Walk-Throughs</span></span>](d3d12-code-walk-throughs.md)
</dt> <dt>

[<span data-ttu-id="80ee2-208">預測</span><span class="sxs-lookup"><span data-stu-id="80ee2-208">Predication</span></span>](predication.md)
</dt> <dt>

[<span data-ttu-id="80ee2-209">查詢</span><span class="sxs-lookup"><span data-stu-id="80ee2-209">Queries</span></span>](queries.md)
</dt> </dl>

 

 
