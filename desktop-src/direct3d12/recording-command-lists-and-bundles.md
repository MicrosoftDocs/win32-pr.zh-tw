---
title: 建立和記錄命令清單和組合
description: 本主題說明如何在 Direct3D 12 應用程式中錄製命令清單和組合。 命令清單和套件組合都可讓應用程式記錄繪圖或狀態變更呼叫，以供稍後在圖形處理單元上執行 (GPU) 。
ms.assetid: 0074B796-33A4-4AA1-A4E7-48A2A63F25B7
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5ef2b54138cf3a08b85e3e8cc31f97cbe66abf6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548427"
---
# <a name="creating-and-recording-command-lists-and-bundles"></a>建立和記錄命令清單和組合

本主題說明如何在 Direct3D 12 應用程式中錄製命令清單和組合。 命令清單和套件組合都可讓應用程式記錄繪圖或狀態變更呼叫，以供稍後在圖形處理單元上執行 (GPU) 。

除了命令清單之外，GPU 硬體中的 API 惡意探索功能會藉由新增第二個層級的命令清單（稱為 *配套）來提供。* 套件組合的目的是要讓應用程式將少量的 API 命令群組在一起，以供稍後執行。 在建立套件組合時，驅動程式將會盡可能地執行最多預先處理，以使這些成本在稍後執行。 組合是設計來使用並重複使用任何次數。 另一方面，命令清單通常只會執行一次。 不過，只要應用程式先確認先前的執行已完成，然後再) 提交新的執行，命令清單 *就可以* (執行多次。

一般情況下，下圖顯示在套件組合中進行 API 呼叫，以及將 API 呼叫和套件組合到單一畫面格的組建，如下圖所示，在 **命令清單 1** 和 **命令清單 2** 中，請注意組合 **1** 的重複使用，而且圖表中的 api 方法名稱就像範例一樣，可以使用許多不同的 api 呼叫。

![在框架中建立命令、組合和命令清單](images/gpu-workitems.png)

建立和執行組合和直接命令清單有不同的限制，而這些差異會在本主題中注明。

## <a name="creating-command-lists"></a>建立命令清單

直接命令清單和組合是藉由呼叫 [**ID3D12Device：： CreateCommandList**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist) 或 [**ID3D12Device4：： CreateCommandList1**](/windows/win32/api/d3d12/nf-d3d12-id3d12device4-createcommandlist1)所建立。

使用 [**ID3D12Device4：： CreateCommandList1**](/windows/win32/api/d3d12/nf-d3d12-id3d12device4-createcommandlist1) 建立已關閉的命令清單，而不是建立新的清單並立即將其關閉。 這可避免建立具有配置器和 PSO 的清單，而不是使用它們的效率。

[**ID3D12Device：： CreateCommandList**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist) 接受下列參數作為輸入：

### <a name="d3d12_command_list_type"></a>D3D12 \_ 命令 \_ 清單 \_ 類型

[**D3D12 \_ 命令 \_ 清單 \_ 類型**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type)列舉指出正在建立的命令清單類型。 它可以是直接命令清單、配套、計算命令清單或複製命令清單。

### <a name="id3d12commandallocator"></a>ID3D12CommandAllocator

命令配置器可讓應用程式管理配置給命令清單的記憶體。 命令配置器會藉由呼叫 [**CreateCommandAllocator**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandallocator)來建立。 建立命令清單時，配置器的命令清單類型（由 [**D3D12 \_ 命令 \_ 清單 \_ 類型**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type)指定）必須符合所建立的命令清單類型。 指定的配置器一次只能與一個以上的 *目前記錄* 命令清單相關聯，不過一個命令配置器可以用來建立任意數目的 [**GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) 物件。

為了回收命令配置器所配置的記憶體，應用程式會呼叫 [**ID3D12CommandAllocator：： Reset**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandallocator-reset)。 這可讓配置器針對新的命令重複使用，但不會減少其基礎大小。 但在這樣做之前，應用程式必須確定 GPU 不再執行與配置器相關聯的任何命令清單;否則，呼叫會失敗。 另請注意，此 API 不是無限制執行緒，因此無法同時從多個執行緒呼叫相同的配置器。

### <a name="id3d12pipelinestate"></a>ID3D12PipelineState

命令清單的初始管線狀態。 在 Microsoft Direct3D 12 中，大部分圖形管線狀態都是使用 [**ID3D12PipelineState**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinestate) 物件在命令清單中設定。 應用程式會在應用程式初始化期間建立大量的應用程式，然後藉由使用 [**ID3D12GraphicsCommandList：： SetPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate)變更目前系結的狀態物件來更新狀態。 如需有關管線狀態物件的詳細資訊，請參閱 [在 Direct3D 12 中管理圖形管線狀態](managing-graphics-pipeline-state-in-direct3d-12.md)。

請注意，套件組合不會繼承其父代直接命令清單中先前呼叫所設定的管線狀態。

如果此參數為 Null，則會使用預設狀態。

## <a name="recording-command-lists"></a>錄製命令清單

建立之後，命令清單會立即處於錄製狀態。 您也可以呼叫 I [**D3D12GraphicsCommandList：： Reset**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset)來重複使用現有的命令清單，這也會讓命令清單處於 [錄製中] 狀態。 不同于 [**ID3D12CommandAllocator：： Reset**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandallocator-reset)，當命令清單仍在執行時，您可以呼叫 **Reset** 。 一般模式是提交命令清單，然後立即將其重設為針對另一個命令清單重複使用配置的記憶體。 請注意，每個命令配置器只會有一個相關聯的命令清單，且一次只能處於錄製狀態。

當命令清單處於錄製狀態之後，您只要呼叫 [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) 介面的方法，即可將命令新增至清單。 其中許多方法都能提供 Microsoft Direct3D 11 開發人員熟悉的常用 Direct3D 功能;其他 Api 是 Direct3D 12 的新 Api。

將命令加入至命令清單之後，您可以藉由呼叫 [**Close**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)，將命令清單從錄製狀態轉換。

命令配置器可以成長，但不會壓縮和重複使用配置器，因此應考慮將應用程式的效率發揮到最大。 在重設之前，您可以將多個清單記錄到相同的配置器中，前提是一次只有一個清單會記錄到指定的配置器。 您可以將每個清單 visualise 為擁有配置器的一部分，以指出將執行的 [**ID3D12CommandQueue：： ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) 。

簡單的配置器共用策略應以大約 `numCommandLists * MaxFrameLatency` 配置器為目標。 例如，如果您記錄6個清單並允許最多3個潛在的框架，您可以合理地預期18-20 配置器。 更先進的共用策略，這會在相同的執行緒上重複使用多個清單的配置器，可能會以配置器為目標 `numRecordingThreads * MaxFrameLatency` 。 使用先前的範例，如果2個清單記錄線上程 A 上，2個線上程 B 上，1個線上程 C 上，1線上程 D 上，您實際上可以針對12-14 配置器。

使用隔離來決定何時可以重複使用指定的配置器。

因為命令清單可以在執行後立即重設，所以可以完整集區，並在每次呼叫 [**ID3D12CommandQueue：： ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)之後，將它們加回集區。

## <a name="example"></a>範例

下列程式碼片段說明如何建立和錄製命令清單。 請注意，此範例包含下列 Direct3D 12 功能：

-   管線狀態物件-這些物件是用來從命令清單內設定轉譯管線的大部分狀態參數。 如需詳細資訊，請參閱 [管理 Direct3D 12 中的圖形管線狀態](managing-graphics-pipeline-state-in-direct3d-12.md)。
-   描述元堆積-應用程式會使用描述元堆積來管理記憶體資源的管線系結。
-   資源屏障-這可用來管理從某個狀態到另一個狀態的資源轉換，例如從轉譯目標視圖到著色器資源檢視。 如需詳細資訊，請參閱 [使用資源阻礙來同步處理資源狀態](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md)。

例如，


```C++
void D3D12HelloTriangle::LoadAssets()
{
    // Create an empty root signature.
    {
        CD3DX12_ROOT_SIGNATURE_DESC rootSignatureDesc;
        rootSignatureDesc.Init(0, nullptr, 0, nullptr, D3D12_ROOT_SIGNATURE_FLAG_ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT);

        ComPtr<ID3DBlob> signature;
        ComPtr<ID3DBlob> error;
        ThrowIfFailed(D3D12SerializeRootSignature(&rootSignatureDesc, D3D_ROOT_SIGNATURE_VERSION_1, &signature, &error));
        ThrowIfFailed(m_device->CreateRootSignature(0, signature->GetBufferPointer(), signature->GetBufferSize(), IID_PPV_ARGS(&m_rootSignature)));
    }

    // Create the pipeline state, which includes compiling and loading shaders.
    {
        ComPtr<ID3DBlob> vertexShader;
        ComPtr<ID3DBlob> pixelShader;

#if defined(_DEBUG)
        // Enable better shader debugging with the graphics debugging tools.
        UINT compileFlags = D3DCOMPILE_DEBUG | D3DCOMPILE_SKIP_OPTIMIZATION;
#else
        UINT compileFlags = 0;
#endif

        ThrowIfFailed(D3DCompileFromFile(GetAssetFullPath(L"shaders.hlsl").c_str(), nullptr, nullptr, "VSMain", "vs_5_0", compileFlags, 0, &vertexShader, nullptr));
        ThrowIfFailed(D3DCompileFromFile(GetAssetFullPath(L"shaders.hlsl").c_str(), nullptr, nullptr, "PSMain", "ps_5_0", compileFlags, 0, &pixelShader, nullptr));

        // Define the vertex input layout.
        D3D12_INPUT_ELEMENT_DESC inputElementDescs[] =
        {
            { "POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT, 0, 0, D3D12_INPUT_CLASSIFICATION_PER_VERTEX_DATA, 0 },
            { "COLOR", 0, DXGI_FORMAT_R32G32B32A32_FLOAT, 0, 12, D3D12_INPUT_CLASSIFICATION_PER_VERTEX_DATA, 0 }
        };

        // Describe and create the graphics pipeline state object (PSO).
        D3D12_GRAPHICS_PIPELINE_STATE_DESC psoDesc = {};
        psoDesc.InputLayout = { inputElementDescs, _countof(inputElementDescs) };
        psoDesc.pRootSignature = m_rootSignature.Get();
        psoDesc.VS = { reinterpret_cast<UINT8*>(vertexShader->GetBufferPointer()), vertexShader->GetBufferSize() };
        psoDesc.PS = { reinterpret_cast<UINT8*>(pixelShader->GetBufferPointer()), pixelShader->GetBufferSize() };
        psoDesc.RasterizerState = CD3DX12_RASTERIZER_DESC(D3D12_DEFAULT);
        psoDesc.BlendState = CD3DX12_BLEND_DESC(D3D12_DEFAULT);
        psoDesc.DepthStencilState.DepthEnable = FALSE;
        psoDesc.DepthStencilState.StencilEnable = FALSE;
        psoDesc.SampleMask = UINT_MAX;
        psoDesc.PrimitiveTopologyType = D3D12_PRIMITIVE_TOPOLOGY_TYPE_TRIANGLE;
        psoDesc.NumRenderTargets = 1;
        psoDesc.RTVFormats[0] = DXGI_FORMAT_R8G8B8A8_UNORM;
        psoDesc.SampleDesc.Count = 1;
        ThrowIfFailed(m_device->CreateGraphicsPipelineState(&psoDesc, IID_PPV_ARGS(&m_pipelineState)));
    }

    // Create the command list.
    ThrowIfFailed(m_device->CreateCommandList(0, D3D12_COMMAND_LIST_TYPE_DIRECT, m_commandAllocator.Get(), m_pipelineState.Get(), IID_PPV_ARGS(&m_commandList)));

    // Command lists are created in the recording state, but there is nothing
    // to record yet. The main loop expects it to be closed, so close it now.
    ThrowIfFailed(m_commandList->Close());

    // Create the vertex buffer.
    {
        // Define the geometry for a triangle.
        Vertex triangleVertices[] =
        {
            { { 0.0f, 0.25f * m_aspectRatio, 0.0f }, { 1.0f, 0.0f, 0.0f, 1.0f } },
            { { 0.25f, -0.25f * m_aspectRatio, 0.0f }, { 0.0f, 1.0f, 0.0f, 1.0f } },
            { { -0.25f, -0.25f * m_aspectRatio, 0.0f }, { 0.0f, 0.0f, 1.0f, 1.0f } }
        };

        const UINT vertexBufferSize = sizeof(triangleVertices);

        // Note: using upload heaps to transfer static data like vert buffers is not 
        // recommended. Every time the GPU needs it, the upload heap will be marshalled 
        // over. Please read up on Default Heap usage. An upload heap is used here for 
        // code simplicity and because there are very few verts to actually transfer.
        ThrowIfFailed(m_device->CreateCommittedResource(
            &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
            D3D12_HEAP_FLAG_NONE,
            &CD3DX12_RESOURCE_DESC::Buffer(vertexBufferSize),
            D3D12_RESOURCE_STATE_GENERIC_READ,
            nullptr,
            IID_PPV_ARGS(&m_vertexBuffer)));

        // Copy the triangle data to the vertex buffer.
        UINT8* pVertexDataBegin;
        CD3DX12_RANGE readRange(0, 0);        // We do not intend to read from this resource on the CPU.
        ThrowIfFailed(m_vertexBuffer->Map(0, &readRange, reinterpret_cast<void**>(&pVertexDataBegin)));
        memcpy(pVertexDataBegin, triangleVertices, sizeof(triangleVertices));
        m_vertexBuffer->Unmap(0, nullptr);

        // Initialize the vertex buffer view.
        m_vertexBufferView.BufferLocation = m_vertexBuffer->GetGPUVirtualAddress();
        m_vertexBufferView.StrideInBytes = sizeof(Vertex);
        m_vertexBufferView.SizeInBytes = vertexBufferSize;
    }

    // Create synchronization objects and wait until assets have been uploaded to the GPU.
    {
        ThrowIfFailed(m_device->CreateFence(0, D3D12_FENCE_FLAG_NONE, IID_PPV_ARGS(&m_fence)));
        m_fenceValue = 1;

        // Create an event handle to use for frame synchronization.
        m_fenceEvent = CreateEvent(nullptr, FALSE, FALSE, nullptr);
        if (m_fenceEvent == nullptr)
        {
            ThrowIfFailed(HRESULT_FROM_WIN32(GetLastError()));
        }

        // Wait for the command list to execute; we are reusing the same command 
        // list in our main loop but for now, we just want to wait for setup to 
        // complete before continuing.
        WaitForPreviousFrame();
    }
}
```



建立並記錄命令清單之後，就可以使用命令佇列來執行它。 如需詳細資訊，請參閱 [執行和同步處理命令清單](executing-and-synchronizing-command-lists.md)。

## <a name="reference-counting"></a>參考計數

大部分 D3D12 Api 都會繼續使用參考計數（遵循 COM 慣例）。 有個值得注意的例外狀況是 D3D12 graphics 命令清單 Api。 [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist)上的所有 api 都不會保留傳遞至這些 api 之物件的參考。 這表示應用程式會負責確保永遠不會提交命令清單來執行參考損毀資源的執行。

## <a name="command-list-errors"></a>命令清單錯誤

[**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist)上大部分的 api 不會傳回錯誤。 命令清單建立期間發生的錯誤會延後，直到 [**ID3D12GraphicsCommandList：： Close**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)。 其中一個例外狀況是 \_ \_ 已移除 DXGI 錯誤裝置 \_ ，並會更進一步地延後。 請注意，這不同于 D3D11，其中許多參數驗證錯誤會以無訊息方式卸載，而且永遠不會傳回給呼叫端。

應用程式可能預期會 \_ \_ 在下列 API 呼叫中看到 DXGI 裝置已移除錯誤：

-   任何資源建立方法
-   [**ID3D12Resource：： Map**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-map)
-   [**IDXGISwapChain1::Present1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1)
-   [**GetDeviceRemovedReason**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdeviceremovedreason)

## <a name="command-list-api-restrictions"></a>命令清單 API 限制

某些命令清單 Api 只能針對特定類型的命令清單來呼叫。 下表顯示哪些命令清單 Api 適用于每種類型的命令清單。 它也會顯示哪些 Api 在 [**D3D12 轉譯階段**](./direct3d-12-render-passes.md)中為有效的呼叫。 

| API 名稱                                         | 圖形 | 計算 | 複製 | 套件組合 | 在轉譯階段中 |
|--------------------------------------------------|:--------:|:-------:|:----:|:------:|:--------------:|
| AtomicCopyBufferUINT                             | ✓        | ✓       | ✓    |        |                |
| AtomicCopyBufferUINT64                           | ✓        | ✓       | ✓    |        |                |
| BeginQuery                                       | ✓        |         |      |        | ✓              |
| BeginRenderPass                                  | ✓        |         |      |        |                |
| BuildRaytracingAccelerationStructure             | ✓        | ✓       |      |        |                |
| ClearDepthStencilView                            | ✓        |         |      |        |                |
| ClearRenderTargetView                            | ✓        |         |      |        |                |
| ClearState                                       | ✓        | ✓       |      |        |                |
| ClearUnorderedAccessViewFloat                    | ✓        | ✓       |      |        |                |
| ClearUnorderedAccessViewUint                     | ✓        | ✓       |      |        |                |
| CopyBufferRegion                                 | ✓        | ✓       | ✓    |        |                |
| CopyRaytracingAccelerationStructure              | ✓        | ✓       |      |        |                |
| CopyResource                                     | ✓        | ✓       | ✓    |        |                |
| CopyTextureRegion                                | ✓        | ✓       | ✓    |        |                |
| CopyTiles                                        | ✓        | ✓       | ✓    |        |                |
| DiscardResource                                  | ✓        | ✓       |      |        |                |
| 分派                                         | ✓        | ✓       |      | ✓      |                |
| DispatchRays                                     | ✓        | ✓       |      | ✓      |                |
| DrawIndexedInstanced                             | ✓        |         |      | ✓      | ✓              |
| DrawInstanced                                    | ✓        |         |      | ✓      | ✓              |
| EmitRaytracingAccelerationStructurePostbuildInfo | ✓        | ✓       |      |        |                |
| EndQuery                                         | ✓        | ✓       | ✓    |        | ✓              |
| EndRenderPass                                    | ✓        |         |      |        | ✓              |
| ExecuteBundle                                    | ✓        |         |      |        | ✓              |
| ExecuteIndirect                                  | ✓        | ✓       |      | ✓      | ✓              |
| ExecuteMetaCommand                               | ✓        | ✓       |      |        |                |
| IASetIndexBuffer                                 | ✓        |         |      | ✓      | ✓              |
| IASetPrimitiveTopology                           | ✓        |         |      | ✓      | ✓              |
| IASetVertexBuffers                               | ✓        |         |      | ✓      | ✓              |
| InitializeMetaCommand                            | ✓        | ✓       |      |        |                |
| OMSetBlendFactor                                 | ✓        |         |      | ✓      | ✓              |
| OMSetDepthBounds                                 | ✓        |         |      | ✓      | ✓              |
| OMSetRenderTargets                               | ✓        |         |      |        |                |
| OMSetStencilRef                                  | ✓        |         |      | ✓      | ✓              |
| ResolveQueryData                                 | ✓        | ✓       | ✓    |        |                |
| ResolveSubresource                               | ✓        |         |      |        |                |
| ResolveSubresourceRegion                         | ✓        |         |      |        |                |
| ResourceBarrier                                  | ✓        | ✓       | ✓    |        | ✓              |
| RSSetScissorRects                                | ✓        |         |      |        | ✓              |
| RSSetShadingRate                                 | ✓        |         |      | ✓      | ✓              |
| RSSetShadingRateImage                            | ✓        |         |      | ✓      | ✓              |
| RSSetViewports                                   | ✓        |         |      |        | ✓              |
| SetComputeRoot32BitConstant                      | ✓        | ✓       |      | ✓      | ✓              |
| SetComputeRoot32BitConstants                     | ✓        | ✓       |      | ✓      | ✓              |
| SetComputeRootConstantBufferView                 | ✓        | ✓       |      | ✓      | ✓              |
| SetComputeRootDescriptorTable                    | ✓        | ✓       |      | ✓      | ✓              |
| SetComputeRootShaderResourceView                 | ✓        | ✓       |      | ✓      | ✓              |
| SetComputeRootSignature                          | ✓        | ✓       |      | ✓      | ✓              |
| SetComputeRootUnorderedAccessView                | ✓        | ✓       |      | ✓      | ✓              |
| SetDescriptorHeaps                               | ✓        | ✓       |      | ✓      | ✓              |
| SetGraphicsRoot32BitConstant                     | ✓        |         |      | ✓      | ✓              |
| SetGraphicsRoot32BitConstants                    | ✓        |         |      | ✓      | ✓              |
| SetGraphicsRootConstantBufferView                | ✓        |         |      | ✓      | ✓              |
| SetGraphicsRootDescriptorTable                   | ✓        |         |      | ✓      | ✓              |
| SetGraphicsRootShaderResourceView                | ✓        |         |      | ✓      | ✓              |
| SetGraphicsRootSignature                         | ✓        |         |      | ✓      | ✓              |
| SetGraphicsRootUnorderedAccessView               | ✓        |         |      | ✓      | ✓              |
| SetPipelineState                                 | ✓        | ✓       |      | ✓      | ✓              |
| SetPipelineState1                                | ✓        | ✓       |      | ✓      |                |
| SetPredication                                   | ✓        | ✓       |      |        | ✓              |
| SetProtectedResourceSession                      | ✓        | ✓       | ✓    |        |                |
| SetSamplePositions                               | ✓        |         |      | ✓      | ✓              |
| SetViewInstanceMask                              | ✓        |         |      | ✓      | ✓              |
| SOSetTargets                                     | ✓        |         |      |        | ✓              |
| WriteBufferImmediate                             | ✓        | ✓       | ✓    | ✓      | ✓              |

## <a name="bundle-restrictions"></a>組合限制

限制可讓 Direct3D 12 驅動程式在記錄時執行與組合相關聯的大部分工作，進而讓 [**ExecuteBundle**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executebundle) API 以低額外負荷執行。 組合所參考的所有管線狀態物件都必須具有相同的轉譯目標格式、深度緩衝區格式和範例描述。

使用類型： D3D12 \_ 命令清單類型套件組合建立的命令清單上，不允許下列命令清單 API 呼叫 \_ \_ \_ ：

-   任何明確的方法
-   任何複製方法
-   [**DiscardResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource)
-   [**ExecuteBundle**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executebundle)
-   [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)
-   [**ResolveSubresource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource)
-   [**SetPredication**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication)
-   [**BeginQuery**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery)
-   [**EndQuery**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery)
-   [**SOSetTargets**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-sosettargets)
-   [**OMSetRenderTargets**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)
-   [**RSSetViewports**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetviewports)
-   [**RSSetScissorRects**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetscissorrects)

您可以針對組合呼叫 [**SetDescriptorHeaps**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps) ，但套件組合描述元堆積必須符合呼叫的命令清單描述元堆積。

如果在組合上呼叫這些 Api 的任何一個，則執行時間會捨棄呼叫。 每次發生這種情況時，debug 層都會發出錯誤。

## <a name="related-topics"></a>相關主題

[在 Direct3D 12 中提交工作](command-queues-and-command-lists.md)