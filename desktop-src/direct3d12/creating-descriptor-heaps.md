---
title: 建立描述元堆積
description: 若要建立和設定描述元堆積，您必須選取描述項堆積類型、判斷它包含多少個描述元，以及設定旗標，指出它是否為 CPU 可見和/或著色器可見。
ms.assetid: 58677023-692C-4BA4-90B7-D568F3DD3F73
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e472a0749634d5cbaa9cbf1cde5e11202d4c4f9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548369"
---
# <a name="creating-descriptor-heaps"></a><span data-ttu-id="9bafd-103">建立描述元堆積</span><span class="sxs-lookup"><span data-stu-id="9bafd-103">Creating Descriptor Heaps</span></span>

<span data-ttu-id="9bafd-104">若要建立和設定描述元堆積，您必須選取描述項堆積類型、判斷它包含多少個描述元，以及設定旗標，指出它是否為 CPU 可見和/或著色器可見。</span><span class="sxs-lookup"><span data-stu-id="9bafd-104">To create and configure a descriptor heap, you must select a descriptor heap type, determine how many descriptors it contains, and set flags that indicate whether it is CPU visible and/or shader visible.</span></span>

-   [<span data-ttu-id="9bafd-105">描述元堆積類型</span><span class="sxs-lookup"><span data-stu-id="9bafd-105">Descriptor Heap types</span></span>](#descriptor-heap-types)
-   [<span data-ttu-id="9bafd-106">描述元堆積屬性</span><span class="sxs-lookup"><span data-stu-id="9bafd-106">Descriptor Heap Properties</span></span>](#descriptor-heap-properties)
-   [<span data-ttu-id="9bafd-107">描述項控制代碼</span><span class="sxs-lookup"><span data-stu-id="9bafd-107">Descriptor Handles</span></span>](#descriptor-handles)
-   [<span data-ttu-id="9bafd-108">描述元堆積方法</span><span class="sxs-lookup"><span data-stu-id="9bafd-108">Descriptor Heap Methods</span></span>](#descriptor-heap-methods)
-   [<span data-ttu-id="9bafd-109">基本描述項堆積包裝函式</span><span class="sxs-lookup"><span data-stu-id="9bafd-109">Minimal descriptor heap wrapper</span></span>](#minimal-descriptor-heap-wrapper)
-   [<span data-ttu-id="9bafd-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="9bafd-110">Related topics</span></span>](#related-topics)

## <a name="descriptor-heap-types"></a><span data-ttu-id="9bafd-111">描述元堆積類型</span><span class="sxs-lookup"><span data-stu-id="9bafd-111">Descriptor Heap types</span></span>

<span data-ttu-id="9bafd-112">堆積的類型取決於 [**D3D12 \_ 描述元 \_ 堆積 \_ 型**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type) 別列舉的一個成員：</span><span class="sxs-lookup"><span data-stu-id="9bafd-112">The type of heap is determined by one member of the [**D3D12\_DESCRIPTOR\_HEAP\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type) enum:</span></span>

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

## <a name="descriptor-heap-properties"></a><span data-ttu-id="9bafd-113">描述元堆積屬性</span><span class="sxs-lookup"><span data-stu-id="9bafd-113">Descriptor Heap Properties</span></span>

<span data-ttu-id="9bafd-114">堆積屬性是在 [**D3D12 描述元 \_ 堆積 \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc) 結構上設定，它會參考 [**D3D12 \_ 描述元 \_ 堆積 \_ 類型**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type) 和 [**D3D12 描述元 \_ \_ 堆積 \_ 旗標**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_flags) 列舉。</span><span class="sxs-lookup"><span data-stu-id="9bafd-114">Heap properties are set on the [**D3D12\_DESCRIPTOR\_HEAP\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc) structure, which references both the [**D3D12\_DESCRIPTOR\_HEAP\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type) and [**D3D12\_DESCRIPTOR\_HEAP\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_flags) enums.</span></span>

<span data-ttu-id="9bafd-115">您 \_ \_ \_ \_ 可以選擇性地在描述元堆積上設定旗標 D3D12 描述元堆積旗標著色器， \_ 以指出它會系結至命令清單以供著色器參考。</span><span class="sxs-lookup"><span data-stu-id="9bafd-115">The flag D3D12\_DESCRIPTOR\_HEAP\_FLAG\_SHADER\_VISIBLE can optionally be set on a descriptor heap to indicate it is be bound on a command list for reference by shaders.</span></span> <span data-ttu-id="9bafd-116">*未* 使用此旗標建立的描述元堆積，可讓應用程式在將描述項複製到著色器可見描述元堆積之前，將描述項暫存在 CPU 記憶體中，以方便使用。</span><span class="sxs-lookup"><span data-stu-id="9bafd-116">Descriptor heaps created *without* this flag allow applications the option to stage descriptors in CPU memory before copying them to a shader visible descriptor heap, as a convenience.</span></span> <span data-ttu-id="9bafd-117">但是，應用程式也可以直接將描述元直接建立至著色器可見的描述項堆積，而不需要在 CPU 上暫存任何程式。</span><span class="sxs-lookup"><span data-stu-id="9bafd-117">But it is also fine for applications to directly create descriptors into shader visible descriptor heaps with no requirement to stage anything on the CPU.</span></span>

<span data-ttu-id="9bafd-118">此旗標只適用于 CBV、SRV、UAV 和取樣器。</span><span class="sxs-lookup"><span data-stu-id="9bafd-118">This flag only applies to CBV, SRV, UAV and samplers.</span></span> <span data-ttu-id="9bafd-119">它不會套用到其他描述元堆積類型，因為著色器不會直接參考其他類型。</span><span class="sxs-lookup"><span data-stu-id="9bafd-119">It does not apply to other descriptor heap types since shaders do not directly reference the other types.</span></span>

<span data-ttu-id="9bafd-120">例如，描述並建立取樣器描述元堆積。</span><span class="sxs-lookup"><span data-stu-id="9bafd-120">For example, describe and create a sampler descriptor heap.</span></span>


```C++
// Describe and create a sampler descriptor heap.
D3D12_DESCRIPTOR_HEAP_DESC samplerHeapDesc = {};
samplerHeapDesc.NumDescriptors = 1;
samplerHeapDesc.Type = D3D12_DESCRIPTOR_HEAP_TYPE_SAMPLER;
samplerHeapDesc.Flags = D3D12_DESCRIPTOR_HEAP_FLAG_SHADER_VISIBLE;
ThrowIfFailed(m_device->CreateDescriptorHeap(&samplerHeapDesc, IID_PPV_ARGS(&m_samplerHeap)));
```



<span data-ttu-id="9bafd-121">描述和建立常數緩衝區視圖 (CBV) 、著色器資源查看 (SRV) 和未排序的存取視圖 (UAV) 描述元堆積。</span><span class="sxs-lookup"><span data-stu-id="9bafd-121">Describe and create a constant buffer view (CBV), Shader resource view (SRV), and unordered access view (UAV) descriptor heap.</span></span>


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



## <a name="descriptor-handles"></a><span data-ttu-id="9bafd-122">描述項控制代碼</span><span class="sxs-lookup"><span data-stu-id="9bafd-122">Descriptor Handles</span></span>

<span data-ttu-id="9bafd-123">[**D3D12 \_ GPU 描述 \_ 項 \_ 控制碼**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle)和 [**D3D12 \_ CPU \_ 描述項 \_ 控制碼**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle)結構會識別描述項堆積中的特定描述項。</span><span class="sxs-lookup"><span data-stu-id="9bafd-123">The [**D3D12\_GPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) and [**D3D12\_CPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) structures identify specific descriptors in a descriptor heap.</span></span> <span data-ttu-id="9bafd-124">控制碼有點類似指標，但應用程式不能手動取值;否則，行為會是未定義的。</span><span class="sxs-lookup"><span data-stu-id="9bafd-124">A handle is a bit like a pointer, but the application must not dereference it manually; otherwise, the behavior is undefined.</span></span> <span data-ttu-id="9bafd-125">使用控制碼必須經過 API。</span><span class="sxs-lookup"><span data-stu-id="9bafd-125">The use of the handles must go through the API.</span></span> <span data-ttu-id="9bafd-126">控制碼本身可以自由複製或傳遞到操作/使用描述項的 Api。</span><span class="sxs-lookup"><span data-stu-id="9bafd-126">A handle itself can be copied freely or passed into APIs that operate on/use descriptors.</span></span> <span data-ttu-id="9bafd-127">沒有任何 ref 計數，因此應用程式必須確保在刪除基礎描述元堆積之後，它不會使用控制碼。</span><span class="sxs-lookup"><span data-stu-id="9bafd-127">There is no ref counting, so the application must ensure that it does not use a handle after the underlying descriptor heap has been deleted.</span></span>

<span data-ttu-id="9bafd-128">應用程式可以找出指定之描述項堆積類型之描述項的遞增大小，以便從基底的控制碼開始，手動產生描述項堆積中任何位置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="9bafd-128">Applications can find out the increment size of the descriptors for a given descriptor heap type, so that they can generate handles to any location in a descriptor heap manually starting from the handle to the base.</span></span> <span data-ttu-id="9bafd-129">應用程式絕不能將描述項控制碼的遞增大小硬式編碼，而且應該一律針對指定的裝置實例進行查詢;否則，行為會是未定義的。</span><span class="sxs-lookup"><span data-stu-id="9bafd-129">Applications must never hardcode descriptor handle increment sizes, and should always query them for a given device instance; otherwise, the behavior is undefined.</span></span> <span data-ttu-id="9bafd-130">應用程式也必須使用遞增大小和控制碼來執行其本身的檢查或操作描述元堆積資料，因為這樣做的結果並未定義。</span><span class="sxs-lookup"><span data-stu-id="9bafd-130">Applications must also not use the increment sizes and handles to do their own examination or manipulation of descriptor heap data, as the results from doing so are undefined.</span></span> <span data-ttu-id="9bafd-131">控制碼實際上不能當做指標使用，而是做為指標的 proxy，以避免意外取值。</span><span class="sxs-lookup"><span data-stu-id="9bafd-131">The handles may not actually be used as pointers, but rather as proxies for pointers so as to avoid accidental dereferencing.</span></span>

> [!Note]
>
> <span data-ttu-id="9bafd-132">在 \_ 標頭 d3dx12 中定義的協助程式結構 CD3DX12 GPU \_ 描述元 \_ 控制碼，它會繼承 [**D3D12 \_ GPU 描述項 \_ \_ 控制碼**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) 結構，並提供初始化和其他有用的作業。</span><span class="sxs-lookup"><span data-stu-id="9bafd-132">There is a helper structure, CD3DX12\_GPU\_DESCRIPTOR\_HANDLE, defined in the header d3dx12.h, which inherits the [**D3D12\_GPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) structure and provides initialization and other useful operations.</span></span> <span data-ttu-id="9bafd-133">同樣地，CD3DX12 \_ cpu \_ 描述項 \_ 會針對 [**D3D12 \_ cpu 描述項 \_ \_ 控制碼**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) 結構定義協助程式結構。</span><span class="sxs-lookup"><span data-stu-id="9bafd-133">Similarly the CD3DX12\_CPU\_DESCRIPTOR\_HANDLE helper structure is defined for the [**D3D12\_CPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) structure.</span></span>

 

<span data-ttu-id="9bafd-134">填入命令清單時，會使用這兩個 helper 結構。</span><span class="sxs-lookup"><span data-stu-id="9bafd-134">Both of these helper structures are used when populating command lists.</span></span>


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



## <a name="descriptor-heap-methods"></a><span data-ttu-id="9bafd-135">描述元堆積方法</span><span class="sxs-lookup"><span data-stu-id="9bafd-135">Descriptor Heap Methods</span></span>

<span data-ttu-id="9bafd-136">描述元堆積 ([**ID3D12DescriptorHeap**](/windows/desktop/api/d3d12/nn-d3d12-id3d12descriptorheap)) 繼承自 [**ID3D12Pageable**](/windows/win32/api/d3d12/nn-d3d12-id3d12pageable)。</span><span class="sxs-lookup"><span data-stu-id="9bafd-136">Descriptor heaps ([**ID3D12DescriptorHeap**](/windows/desktop/api/d3d12/nn-d3d12-id3d12descriptorheap)) inherit from [**ID3D12Pageable**](/windows/win32/api/d3d12/nn-d3d12-id3d12pageable).</span></span> <span data-ttu-id="9bafd-137">這會對應用程式上的描述項堆積的常駐管理負責，就像資源堆積一樣。</span><span class="sxs-lookup"><span data-stu-id="9bafd-137">This imposes the responsibility for the residency management of descriptor heaps on applications, just like resource heaps.</span></span> <span data-ttu-id="9bafd-138">常駐管理方法只適用于著色器可見的堆積，因為未直接對 GPU 顯示非著色器可見的堆積。</span><span class="sxs-lookup"><span data-stu-id="9bafd-138">The residency management methods only apply to shader visible heaps since the non shader visible heaps are not visible to the GPU directly.</span></span>

<span data-ttu-id="9bafd-139">[**ID3D12Device：： GetDescriptorHandleIncrementSize**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize)方法可讓應用程式以手動方式將控制碼位移到堆積 (將控制碼產生到描述項堆積) 的任何位置。</span><span class="sxs-lookup"><span data-stu-id="9bafd-139">The [**ID3D12Device::GetDescriptorHandleIncrementSize**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize) method allows applications to manually offset handles into a heap (producing handles into anywhere in a descriptor heap).</span></span> <span data-ttu-id="9bafd-140">堆積開始位置的控制碼來自 [**ID3D12DescriptorHeap：： GetCPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart) / [**ID3D12DescriptorHeap：： GetGPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart)。</span><span class="sxs-lookup"><span data-stu-id="9bafd-140">The heap start location’s handle comes from [**ID3D12DescriptorHeap::GetCPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart)/[**ID3D12DescriptorHeap::GetGPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart).</span></span> <span data-ttu-id="9bafd-141">位移的完成方式是將遞增大小加入 \* 至描述項堆積開始的位移的描述元數目。</span><span class="sxs-lookup"><span data-stu-id="9bafd-141">Offsetting is done by adding the increment size \* the number of descriptors to offset to the descriptor heap start .</span></span> <span data-ttu-id="9bafd-142">請注意，遞增大小不能視為位元組大小，因為應用程式不能將控制碼視為記憶體，而是指的是具有非標準化配置的記憶體，而且甚至針對指定的裝置也可能有變化。</span><span class="sxs-lookup"><span data-stu-id="9bafd-142">Note that the increment size cannot be thought of as a byte size since applications must not dereference handles as if they are memory – the memory pointed to has a non-standardized layout and can vary even for a given device.</span></span>

<span data-ttu-id="9bafd-143">[**GetCPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart) 會傳回 cpu 可見描述項堆積的 cpu 控制碼。</span><span class="sxs-lookup"><span data-stu-id="9bafd-143">[**GetCPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart) returns a CPU handle for CPU visible descriptor heaps.</span></span> <span data-ttu-id="9bafd-144">它會傳回 Null 控制碼 (而且如果描述項堆積不會顯示錯誤，debug 層將會報告錯誤) 。</span><span class="sxs-lookup"><span data-stu-id="9bafd-144">It returns a NULL handle (and the debug layer will report an error) if the descriptor heap is not CPU visible.</span></span>

<span data-ttu-id="9bafd-145">[**GetGPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart) 會傳回著色器可見描述項堆積的 GPU 控制碼。</span><span class="sxs-lookup"><span data-stu-id="9bafd-145">[**GetGPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart) returns a GPU handle for shader visible descriptor heaps.</span></span> <span data-ttu-id="9bafd-146">它會傳回 Null 控制碼 (而且如果描述元堆積不是著色器，debug 層將會報告錯誤) 。</span><span class="sxs-lookup"><span data-stu-id="9bafd-146">It returns a NULL handle (and the debug layer will report an error) if the descriptor heap is not shader visible.</span></span>

<span data-ttu-id="9bafd-147">例如，使用11on12 裝置建立轉譯目標視圖，以顯示 D2D 文字。</span><span class="sxs-lookup"><span data-stu-id="9bafd-147">For example, creating render target views to display D2D text using an 11on12 device.</span></span>


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



## <a name="minimal-descriptor-heap-wrapper"></a><span data-ttu-id="9bafd-148">基本描述項堆積包裝函式</span><span class="sxs-lookup"><span data-stu-id="9bafd-148">Minimal descriptor heap wrapper</span></span>

<span data-ttu-id="9bafd-149">應用程式開發人員可能會想要建立自己的 helper 程式碼來管理描述項控制碼和堆積。</span><span class="sxs-lookup"><span data-stu-id="9bafd-149">Application developers will likely want to build their own helper code for managing descriptor handles and heaps.</span></span> <span data-ttu-id="9bafd-150">基本範例如下所示。</span><span class="sxs-lookup"><span data-stu-id="9bafd-150">A basic example is shown below.</span></span> <span data-ttu-id="9bafd-151">例如，更複雜的包裝函式可以追蹤哪些類型的描述項在堆積中的位置，並儲存描述項建立引數。</span><span class="sxs-lookup"><span data-stu-id="9bafd-151">More sophisticated wrappers could, for example, keep track of what types of descriptors are where in a heap and store the descriptor creation arguments.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="9bafd-152">相關主題</span><span class="sxs-lookup"><span data-stu-id="9bafd-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9bafd-153">描述元堆積</span><span class="sxs-lookup"><span data-stu-id="9bafd-153">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> </dl>

 

 