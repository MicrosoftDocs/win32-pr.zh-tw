---
title: 建立描述元堆積
description: 若要建立和設定描述元堆積，您必須選取描述項堆積類型、判斷它包含多少個描述元，以及設定旗標，指出它是否為 CPU 可見和/或著色器可見。
ms.assetid: 58677023-692C-4BA4-90B7-D568F3DD3F73
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 218d21d462dd393360e9ebfcb07ab5b35524b9d8d8c01c8ab1ef28ef90166eb2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857988"
---
# <a name="creating-descriptor-heaps"></a>建立描述元堆積

若要建立和設定描述元堆積，您必須選取描述項堆積類型、判斷它包含多少個描述元，以及設定旗標，指出它是否為 CPU 可見和/或著色器可見。

-   [描述元堆積類型](#descriptor-heap-types)
-   [描述元堆積屬性](#descriptor-heap-properties)
-   [描述項控制代碼](#descriptor-handles)
-   [描述元堆積方法](#descriptor-heap-methods)
-   [基本描述項堆積包裝函式](#minimal-descriptor-heap-wrapper)
-   [相關主題](#related-topics)

## <a name="descriptor-heap-types"></a>描述元堆積類型

堆積的類型取決於 [**D3D12 \_ 描述元 \_ 堆積 \_ 型**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type) 別列舉的一個成員：

``` syntax
typedef enum D3D12_DESCRIPTOR_HEAP_TYPE
{
    D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV,    // Constant buffer/Shader resource/Unordered access views
    D3D12_DESCRIPTOR_HEAP_TYPE_SAMPLER,        // Samplers
    D3D12_DESCRIPTOR_HEAP_TYPE_RTV,            // Render target view
    D3D12_DESCRIPTOR_HEAP_TYPE_DSV,            // Depth stencil view
    D3D12_DESCRIPTOR_HEAP_TYPE_NUM_TYPES       // Simply the number of descriptor heap types
} D3D12_DESCRIPTOR_HEAP_TYPE;
```

## <a name="descriptor-heap-properties"></a>描述元堆積屬性

堆積屬性是在 [**D3D12 描述元 \_ 堆積 \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc) 結構上設定，它會參考 [**D3D12 \_ 描述元 \_ 堆積 \_ 類型**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type) 和 [**D3D12 描述元 \_ \_ 堆積 \_ 旗標**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_flags) 列舉。

您 \_ \_ \_ \_ 可以選擇性地在描述元堆積上設定旗標 D3D12 描述元堆積旗標著色器， \_ 以指出它會系結至命令清單以供著色器參考。 *未* 使用此旗標建立的描述元堆積，可讓應用程式在將描述項複製到著色器可見描述元堆積之前，將描述項暫存在 CPU 記憶體中，以方便使用。 但是，應用程式也可以直接將描述元直接建立至著色器可見的描述項堆積，而不需要在 CPU 上暫存任何程式。

此旗標只適用于 CBV、SRV、UAV 和取樣器。 它不會套用到其他描述元堆積類型，因為著色器不會直接參考其他類型。

例如，描述並建立取樣器描述元堆積。


```C++
// Describe and create a sampler descriptor heap.
D3D12_DESCRIPTOR_HEAP_DESC samplerHeapDesc = {};
samplerHeapDesc.NumDescriptors = 1;
samplerHeapDesc.Type = D3D12_DESCRIPTOR_HEAP_TYPE_SAMPLER;
samplerHeapDesc.Flags = D3D12_DESCRIPTOR_HEAP_FLAG_SHADER_VISIBLE;
ThrowIfFailed(m_device->CreateDescriptorHeap(&samplerHeapDesc, IID_PPV_ARGS(&m_samplerHeap)));
```



描述和建立常數緩衝區視圖 (CBV) 、著色器資源查看 (SRV) 和未排序的存取視圖 (UAV) 描述元堆積。


```C++
// Describe and create a shader resource view (SRV) and unordered
// access view (UAV) descriptor heap.
D3D12_DESCRIPTOR_HEAP_DESC srvUavHeapDesc = {};
srvUavHeapDesc.NumDescriptors = DescriptorCount;
srvUavHeapDesc.Type = D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV;
srvUavHeapDesc.Flags = D3D12_DESCRIPTOR_HEAP_FLAG_SHADER_VISIBLE;
ThrowIfFailed(m_device->CreateDescriptorHeap(&srvUavHeapDesc, IID_PPV_ARGS(&m_srvUavHeap)));

m_rtvDescriptorSize = m_device->GetDescriptorHandleIncrementSize(D3D12_DESCRIPTOR_HEAP_TYPE_RTV);
m_srvUavDescriptorSize = m_device->GetDescriptorHandleIncrementSize(D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV);
```



## <a name="descriptor-handles"></a>描述項控制代碼

[**D3D12 \_ GPU 描述 \_ 項 \_ 控制碼**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle)和 [**D3D12 \_ CPU \_ 描述項 \_ 控制碼**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle)結構會識別描述項堆積中的特定描述項。 控制碼有點類似指標，但應用程式不能手動取值;否則，行為會是未定義的。 使用控制碼必須經過 API。 控制碼本身可以自由複製或傳遞到操作/使用描述項的 Api。 沒有任何 ref 計數，因此應用程式必須確保在刪除基礎描述元堆積之後，它不會使用控制碼。

應用程式可以找出指定之描述項堆積類型之描述項的遞增大小，以便從基底的控制碼開始，手動產生描述項堆積中任何位置的控制碼。 應用程式絕不能將描述項控制碼的遞增大小硬式編碼，而且應該一律針對指定的裝置實例進行查詢;否則，行為會是未定義的。 應用程式也必須使用遞增大小和控制碼來執行其本身的檢查或操作描述元堆積資料，因為這樣做的結果並未定義。 控制碼實際上不能當做指標使用，而是做為指標的 proxy，以避免意外取值。

> [!Note]
>
> 在 \_ 標頭 d3dx12 中定義的協助程式結構 CD3DX12 GPU \_ 描述元 \_ 控制碼，它會繼承 [**D3D12 \_ GPU 描述項 \_ \_ 控制碼**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) 結構，並提供初始化和其他有用的作業。 同樣地，CD3DX12 \_ cpu \_ 描述項 \_ 會針對 [**D3D12 \_ cpu 描述項 \_ \_ 控制碼**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) 結構定義協助程式結構。

 

填入命令清單時，會使用這兩個 helper 結構。


```C++
// Fill the command list with all the render commands and dependent state.
void D3D12nBodyGravity::PopulateCommandList()
{
    // Command list allocators can only be reset when the associated
    // command lists have finished execution on the GPU; apps should use
    // fences to determine GPU execution progress.
    ThrowIfFailed(m_commandAllocators[m_frameIndex]->Reset());

    // However, when ExecuteCommandList() is called on a particular command
    // list, that command list can then be reset at any time and must be before
    // re-recording.
    ThrowIfFailed(m_commandList->Reset(m_commandAllocators[m_frameIndex].Get(), m_pipelineState.Get()));

    // Set necessary state.
    m_commandList->SetPipelineState(m_pipelineState.Get());
    m_commandList->SetGraphicsRootSignature(m_rootSignature.Get());

    m_commandList->SetGraphicsRootConstantBufferView(RootParameterCB, m_constantBufferGS->GetGPUVirtualAddress() + m_frameIndex * sizeof(ConstantBufferGS));

    ID3D12DescriptorHeap* ppHeaps[] = { m_srvUavHeap.Get() };
    m_commandList->SetDescriptorHeaps(_countof(ppHeaps), ppHeaps);

    m_commandList->IASetVertexBuffers(0, 1, &m_vertexBufferView);
    m_commandList->IASetPrimitiveTopology(D3D_PRIMITIVE_TOPOLOGY_POINTLIST);
    m_commandList->RSSetScissorRects(1, &m_scissorRect);

    // Indicate that the back buffer will be used as a render target.
    m_commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_PRESENT, D3D12_RESOURCE_STATE_RENDER_TARGET));

    CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart(), m_frameIndex, m_rtvDescriptorSize);
    m_commandList->OMSetRenderTargets(1, &rtvHandle, FALSE, nullptr);

    // Record commands.
    const float clearColor[] = { 0.0f, 0.0f, 0.1f, 0.0f };
    m_commandList->ClearRenderTargetView(rtvHandle, clearColor, 0, nullptr);

    // Render the particles.
    float viewportHeight = static_cast<float>(static_cast<UINT>(m_viewport.Height) / m_heightInstances);
    float viewportWidth = static_cast<float>(static_cast<UINT>(m_viewport.Width) / m_widthInstances);
    for (UINT n = 0; n < ThreadCount; n++)
    {
        const UINT srvIndex = n + (m_srvIndex[n] == 0 ? SrvParticlePosVelo0 : SrvParticlePosVelo1);

        D3D12_VIEWPORT viewport;
        viewport.TopLeftX = (n % m_widthInstances) * viewportWidth;
        viewport.TopLeftY = (n / m_widthInstances) * viewportHeight;
        viewport.Width = viewportWidth;
        viewport.Height = viewportHeight;
        viewport.MinDepth = D3D12_MIN_DEPTH;
        viewport.MaxDepth = D3D12_MAX_DEPTH;
        m_commandList->RSSetViewports(1, &viewport);

        CD3DX12_GPU_DESCRIPTOR_HANDLE srvHandle(m_srvUavHeap->GetGPUDescriptorHandleForHeapStart(), srvIndex, m_srvUavDescriptorSize);
        m_commandList->SetGraphicsRootDescriptorTable(RootParameterSRV, srvHandle);

        m_commandList->DrawInstanced(ParticleCount, 1, 0, 0);
    }

    m_commandList->RSSetViewports(1, &m_viewport);

    // Indicate that the back buffer will now be used to present.
    m_commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_RENDER_TARGET, D3D12_RESOURCE_STATE_PRESENT));

    ThrowIfFailed(m_commandList->Close());
}
```



## <a name="descriptor-heap-methods"></a>描述元堆積方法

描述元堆積 ([**ID3D12DescriptorHeap**](/windows/desktop/api/d3d12/nn-d3d12-id3d12descriptorheap)) 繼承自 [**ID3D12Pageable**](/windows/win32/api/d3d12/nn-d3d12-id3d12pageable)。 這會對應用程式上的描述項堆積的常駐管理負責，就像資源堆積一樣。 常駐管理方法只適用于著色器可見的堆積，因為未直接對 GPU 顯示非著色器可見的堆積。

[**ID3D12Device：： GetDescriptorHandleIncrementSize**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize)方法可讓應用程式以手動方式將控制碼位移到堆積 (將控制碼產生到描述項堆積) 的任何位置。 堆積開始位置的控制碼來自 [**ID3D12DescriptorHeap：： GetCPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart) / [**ID3D12DescriptorHeap：： GetGPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart)。 位移的完成方式是將遞增大小加入 \* 至描述項堆積開始的位移的描述元數目。 請注意，遞增大小不能視為位元組大小，因為應用程式不能將控制碼視為記憶體，而是指的是具有非標準化配置的記憶體，而且甚至針對指定的裝置也可能有變化。

[**GetCPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart) 會傳回 cpu 可見描述項堆積的 cpu 控制碼。 它會傳回 Null 控制碼 (而且如果描述項堆積不會顯示錯誤，debug 層將會報告錯誤) 。

[**GetGPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart) 會傳回著色器可見描述項堆積的 GPU 控制碼。 它會傳回 Null 控制碼 (而且如果描述元堆積不是著色器，debug 層將會報告錯誤) 。

例如，使用11on12 裝置建立轉譯目標視圖，以顯示 D2D 文字。


```C++
    // Create descriptor heaps.
    {
        // Describe and create a render target view (RTV) descriptor heap.
        D3D12_DESCRIPTOR_HEAP_DESC rtvHeapDesc = {};
        rtvHeapDesc.NumDescriptors = FrameCount;
        rtvHeapDesc.Type = D3D12_DESCRIPTOR_HEAP_TYPE_RTV;
        rtvHeapDesc.Flags = D3D12_DESCRIPTOR_HEAP_FLAG_NONE;
        ThrowIfFailed(m_d3d12Device->CreateDescriptorHeap(&rtvHeapDesc, IID_PPV_ARGS(&m_rtvHeap)));

        m_rtvDescriptorSize = m_d3d12Device->GetDescriptorHandleIncrementSize(D3D12_DESCRIPTOR_HEAP_TYPE_RTV);
    }

    // Create frame resources.
    {
        CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart());

        // Create a RTV, D2D render target, and a command allocator for each frame.
        for (UINT n = 0; n < FrameCount; n++)
        {
            ThrowIfFailed(m_swapChain->GetBuffer(n, IID_PPV_ARGS(&m_renderTargets[n])));
            m_d3d12Device->CreateRenderTargetView(m_renderTargets[n].Get(), nullptr, rtvHandle);

            // Create a wrapped 11On12 resource of this back buffer. Since we are 
            // rendering all D3D12 content first and then all D2D content, we specify 
            // the In resource state as RENDER_TARGET - because D3D12 will have last 
            // used it in this state - and the Out resource state as PRESENT. When 
            // ReleaseWrappedResources() is called on the 11On12 device, the resource 
            // will be transitioned to the PRESENT state.
            D3D11_RESOURCE_FLAGS d3d11Flags = { D3D11_BIND_RENDER_TARGET };
            ThrowIfFailed(m_d3d11On12Device->CreateWrappedResource(
                m_renderTargets[n].Get(),
                &d3d11Flags,
                D3D12_RESOURCE_STATE_RENDER_TARGET,
                D3D12_RESOURCE_STATE_PRESENT,
                IID_PPV_ARGS(&m_wrappedBackBuffers[n])
                ));

            // Create a render target for D2D to draw directly to this back buffer.
            ComPtr<IDXGISurface> surface;
            ThrowIfFailed(m_wrappedBackBuffers[n].As(&surface));
            ThrowIfFailed(m_d2dDeviceContext->CreateBitmapFromDxgiSurface(
                surface.Get(),
                &bitmapProperties,
                &m_d2dRenderTargets[n]
                ));

            rtvHandle.Offset(1, m_rtvDescriptorSize);

            ThrowIfFailed(m_d3d12Device->CreateCommandAllocator(D3D12_COMMAND_LIST_TYPE_DIRECT, IID_PPV_ARGS(&m_commandAllocators[n])));
        }
    
    }
```



## <a name="minimal-descriptor-heap-wrapper"></a>基本描述項堆積包裝函式

應用程式開發人員可能會想要建立自己的 helper 程式碼來管理描述項控制碼和堆積。 基本範例如下所示。 例如，更複雜的包裝函式可以追蹤哪些類型的描述項在堆積中的位置，並儲存描述項建立引數。

``` syntax
class CDescriptorHeapWrapper
{
public:
    CDescriptorHeapWrapper() { memset(this, 0, sizeof(*this)); }

    HRESULT Create(
        ID3D12Device* pDevice, 
        D3D12_DESCRIPTOR_HEAP_TYPE Type, 
        UINT NumDescriptors, 
        bool bShaderVisible = false)
    {
        D3D12_DESCRIPTOR_HEAP_DESC Desc;
        Desc.Type = Type;
        Desc.NumDescriptors = NumDescriptors;
        Desc.Flags = (bShaderVisible ? D3D12_DESCRIPTOR_HEAP_FLAG_SHADER_VISIBLE : D3D12_DESCRIPTOR_HEAP_FLAG_NONE);
       
        HRESULT hr = pDevice->CreateDescriptorHeap(&Desc, 
                               __uuidof(ID3D12DescriptorHeap), 
                               (void**)&pDH);
        if (FAILED(hr)) return hr;

        hCPUHeapStart = pDH->GetCPUDescriptorHandleForHeapStart();
        hGPUHeapStart = pDH->GetGPUDescriptorHandleForHeapStart();

        HandleIncrementSize = pDevice->GetDescriptorHandleIncrementSize(Desc.Type);
        return hr;
    }
    operator ID3D12DescriptorHeap*() { return pDH; }

    D3D12_CPU_DESCRIPTOR_HANDLE hCPU(UINT index)
    {
        return hCPUHeapStart.MakeOffsetted(index,HandleIncrementSize); 
    }
    D3D12_GPU_DESCRIPTOR_HANDLE hGPU(UINT index) 
    {
        assert(Desc.Flags&D3D12_DESCRIPTOR_HEAP_FLAG_SHADER_VISIBLE); 
        return hGPUHeapStart.MakeOffsetted(index,HandleIncrementSize); 
    }
    D3D12_DESCRIPTOR_HEAP_DESC Desc;
    CComPtr<ID3D12DescriptorHeap> pDH;
    D3D12_CPU_DESCRIPTOR_HANDLE hCPUHeapStart;
    D3D12_GPU_DESCRIPTOR_HANDLE hGPUHeapStart;
    UINT HandleIncrementSize;
};
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[描述元堆積](descriptor-heaps.md)
</dt> </dl>

 

 