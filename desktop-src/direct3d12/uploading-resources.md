---
title: 上傳不同類型的資源
description: 示範如何使用一個緩衝區，將常數緩衝區資料和頂點緩衝區資料上傳至 GPU，以及如何適當地子配置和將資料放在緩衝區中。
ms.assetid: 255B0482-21D6-4276-8009-3F3891879CA1
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b03d4755124bbadcdd255a6e99739b710845ab14
ms.sourcegitcommit: a30d0436a84986234df673c6def6694d5a8579f6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "113563778"
---
# <a name="uploading-different-types-of-resources"></a><span data-ttu-id="77e32-103">上傳不同類型的資源</span><span class="sxs-lookup"><span data-stu-id="77e32-103">Uploading different types of resources</span></span>

<span data-ttu-id="77e32-104">示範如何使用一個緩衝區，將常數緩衝區資料和頂點緩衝區資料上傳至 GPU，以及如何適當地子配置和將資料放在緩衝區中。</span><span class="sxs-lookup"><span data-stu-id="77e32-104">Shows how to use one buffer to upload both constant buffer data and vertex buffer data to the GPU, and how to properly sub-allocate and place data within buffers.</span></span> <span data-ttu-id="77e32-105">使用單一緩衝區可增加記憶體使用量的彈性，並提供應用程式更嚴密地控制記憶體使用量。</span><span class="sxs-lookup"><span data-stu-id="77e32-105">The use of a single buffer increases memory usage flexibility, and provides applications with tighter control over memory usage.</span></span> <span data-ttu-id="77e32-106">另外也會顯示 Direct3D 11 和 Direct3D 12 模型之間的差異，以便上傳不同類型的資源。</span><span class="sxs-lookup"><span data-stu-id="77e32-106">Also shows the differences between the Direct3D 11 and Direct3D 12 models for uploading different types of resources.</span></span>

## <a name="upload-different-types-of-resources"></a><span data-ttu-id="77e32-107">Upload 不同類型的資源</span><span class="sxs-lookup"><span data-stu-id="77e32-107">Upload different types of resources</span></span>

<span data-ttu-id="77e32-108">在 Direct3D 12 中，您會建立一個緩衝區來容納不同類型的資源資料進行上傳，並以類似的方式將資源資料複製到相同的緩衝區，以用於不同的資源資料。</span><span class="sxs-lookup"><span data-stu-id="77e32-108">In Direct3D 12, you create one buffer to accommodate different types of resource data for uploading, and you copy resource data to the same buffer in a similar way for different resource data.</span></span> <span data-ttu-id="77e32-109">接著會建立個別的視圖，以將這些資源資料系結至 Direct3D 12 資源系結模型中的圖形管線。</span><span class="sxs-lookup"><span data-stu-id="77e32-109">Individual views are then created to bind those resource data to the graphics pipeline in the Direct3D 12 resource binding model.</span></span>

<span data-ttu-id="77e32-110">在 Direct3D 11 中，您可以針對不同類型的資源資料建立不同的緩衝區 (請注意 `BindFlags` 下列 Direct3D 11 範例程式碼中所用的不同) 、將每個資源緩衝區明確系結至圖形管線，以及根據不同的資源類型，以不同的方法更新資源資料。</span><span class="sxs-lookup"><span data-stu-id="77e32-110">In Direct3D 11, you create separate buffers for different types of resource data (note the different `BindFlags` used in the Direct3D 11 sample code below), explicitly binding each resource buffer to the graphics pipeline, and update the resource data with different methods based on different resource types.</span></span>

<span data-ttu-id="77e32-111">在 Direct3D 12 和 Direct3D 11 中，您應該只使用上傳資源，只要 CPU 寫入資料一次，GPU 就會讀取一次。</span><span class="sxs-lookup"><span data-stu-id="77e32-111">In both Direct3D 12 and Direct3D 11, you should use upload resources only where the CPU will write the data once, and the GPU will read it once.</span></span>

<span data-ttu-id="77e32-112">在某些情況下，</span><span class="sxs-lookup"><span data-stu-id="77e32-112">In some cases,</span></span>
* <span data-ttu-id="77e32-113">GPU 會多次讀取資料，或</span><span class="sxs-lookup"><span data-stu-id="77e32-113">the GPU will read the data multiple times, or</span></span>
* <span data-ttu-id="77e32-114">GPU 不會以線性方式讀取資料，或</span><span class="sxs-lookup"><span data-stu-id="77e32-114">the GPU won't read the data linearly, or</span></span>
* <span data-ttu-id="77e32-115">轉譯已大幅限制 GPU。</span><span class="sxs-lookup"><span data-stu-id="77e32-115">the rendering is significantly GPU-limited already.</span></span>

<span data-ttu-id="77e32-116">在這些情況下，較佳的選項可能是使用 [**ID3D12GraphicsCommandList：： CopyTextureRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) 或 [**ID3D12GraphicsCommandList：： CopyBufferRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion) ，將上傳緩衝區資料複製到預設資源。</span><span class="sxs-lookup"><span data-stu-id="77e32-116">In those cases, the better option might be to use [**ID3D12GraphicsCommandList::CopyTextureRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) or [**ID3D12GraphicsCommandList::CopyBufferRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion) to copy the upload buffer data to a default resource.</span></span>

<span data-ttu-id="77e32-117">預設資源可以位於離散 Gpu 的實體視頻記憶體中。</span><span class="sxs-lookup"><span data-stu-id="77e32-117">A default resource can reside in physical video memory on discrete GPUs.</span></span>

### <a name="code-example-direct3d-11"></a><span data-ttu-id="77e32-118">程式碼範例： Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="77e32-118">Code Example: Direct3D 11</span></span>

```cpp
// Direct3D 11: Separate buffers for each resource type.

void main()
{
    // ...

    // Create a constant buffer.
    float constantBufferData[] = ...;

    D3D11_BUFFER_DESC constantBufferDesc = {0};  
    constantBufferDesc.ByteWidth = sizeof(constantBufferData);  
    constantBufferDesc.Usage = D3D11_USAGE_DYNAMIC;  
    constantBufferDesc.BindFlags = D3D11_BIND_CONSTANT_BUFFER;  
    constantBufferDesc.CPUAccessFlags = D3D11_CPU_ACCESS_WRITE;  

    ComPtr<ID3D11Buffer> constantBuffer;
    d3dDevice->CreateBuffer(  
        &constantBufferDesc,  
        NULL,
        &constantBuffer  
        );

    // Create a vertex buffer.
    float vertexBufferData[] = ...;

    D3D11_BUFFER_DESC vertexBufferDesc = { 0 };
    vertexBufferDesc.ByteWidth = sizeof(vertexBufferData);
    vertexBufferDesc.Usage = D3D11_USAGE_DYNAMIC;
    vertexBufferDesc.BindFlags = D3D11_BIND_VERTEX_BUFFER;

    ComPtr<ID3D11Buffer> vertexBuffer;
    d3dDevice->CreateBuffer(
        &vertexBufferDesc,
        NULL,
        &vertexBuffer
        );

    // ...
}

void DrawFrame()
{
    // ...

    // Bind buffers to the graphics pipeline.
    d3dDeviceContext->VSSetConstantBuffers(0, 1, constantBuffer.Get());
    d3dDeviceContext->IASetVertexBuffers(0, 1, vertexBuffer.Get(), ...);

    // Update the constant buffer.
    D3D11_MAPPED_SUBRESOURCE mappedResource;  
    d3dDeviceContext->Map(
        constantBuffer.Get(),
        0, 
        D3D11_MAP_WRITE_DISCARD,
        0,
        &mappedResource
        );
    memcpy(mappedResource.pData, constantBufferData,
        sizeof(contatnBufferData));
    d3dDeviceContext->Unmap(constantBuffer.Get(), 0);  

    // Update the vertex buffer.
    d3dDeviceContext->UpdateSubresource(
        vertexBuffer.Get(),
        0,
        NULL,
        vertexBufferData,
        sizeof(vertexBufferData),
        0
    );

    // ...
}
```

### <a name="code-example-direct3d-12"></a><span data-ttu-id="77e32-119">程式碼範例： Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="77e32-119">Code Example: Direct3D 12</span></span>

```cpp
// Direct3D 12: One buffer to accommodate different types of resources

ComPtr<ID3D12Resource> m_spUploadBuffer;
UINT8* m_pDataBegin = nullptr;    // starting position of upload buffer
UINT8* m_pDataCur = nullptr;      // current position of upload buffer
UINT8* m_pDataEnd = nullptr;      // ending position of upload buffer

void main()
{
    //
    // Initialize an upload buffer
    //

    InitializeUploadBuffer(64 * 1024);

    // ...
}

void DrawFrame()
{
    // ...

    // Set vertices data to the upload buffer.

    float vertices[] = ...;
    UINT verticesOffset = 0;
    ThrowIfFailed(
        SetDataToUploadBuffer(
            vertices, sizeof(float), sizeof(vertices) / sizeof(float),
            sizeof(float), 
            verticesOffset
            ));

    // Set constant data to the upload buffer.

    float constants[] = ...;
    UINT constantsOffset = 0;
    ThrowIfFailed(
        SetDataToUploadBuffer(
            constants, sizeof(float), sizeof(constants) / sizeof(float), 
            D3D12_CONSTANT_BUFFER_DATA_PLACEMENT_ALIGNMENT, 
            constantsOffset
            ));

    // Create vertex buffer views for the new binding model.

    D3D12_VERTEX_BUFFER_VIEW vertexBufferViewDesc = {
        m_spUploadBuffer->GetGPUVirtualAddress() + verticesOffset,
        sizeof(vertices), // size
        sizeof(float) * 4,  // stride
    };

    commandList->IASetVertexBuffers( 
        0,
        1,
        &vertexBufferViewDesc,
        ));

    // Create constant buffer views for the new binding model.

    D3D12_CONSTANT_BUFFER_VIEW_DESC constantBufferViewDesc = {
        m_spUploadBuffer->GetGPUVirtualAddress() + constantsOffset,
        sizeof(constants) // size
         };

    d3dDevice->CreateConstantBufferView(
        &constantBufferViewDesc,
        ...
        ));

    // Continue command list building and execution ...
}

//
// Create an upload buffer and keep it always mapped.
//

HRESULT InitializeUploadBuffer(SIZE_T uSize)
{
    HRESULT hr = d3dDevice->CreateCommittedResource(
         &CD3DX12_HEAP_PROPERTIES( D3D12_HEAP_TYPE_UPLOAD ),    
               D3D12_HEAP_FLAG_NONE, 
               &CD3DX12_RESOURCE_DESC::Buffer( uSize ), 
               D3D12_RESOURCE_STATE_GENERIC_READ, nullptr,  
               IID_PPV_ARGS( &m_spUploadBuffer ) );

    if (SUCCEEDED(hr))
    {
        void* pData;
        //
        // No CPU reads will be done from the resource.
        //
        CD3DX12_RANGE readRange(0, 0);
        m_spUploadBuffer->Map( 0, &readRange, &pData ); 
        m_pDataCur = m_pDataBegin = reinterpret_cast< UINT8* >( pData );
        m_pDataEnd = m_pDataBegin + uSize;
    }
    return hr;
}

//
// Sub-allocate from the buffer, with offset aligned.
//

HRESULT SuballocateFromBuffer(SIZE_T uSize, UINT uAlign)
{
    m_pDataCur = reinterpret_cast< UINT8* >(
        Align(reinterpret_cast< SIZE_T >(m_pDataCur), uAlign)
        );

    return (m_pDataCur + uSize > m_pDataEnd) ? E_INVALIDARG : S_OK;
}

//
// Place and copy data to the upload buffer.
//

HRESULT SetDataToUploadBuffer(
    const void* pData, 
    UINT bytesPerData, 
    UINT dataCount, 
    UINT alignment, 
    UINT& byteOffset
    )
{
    SIZE_T byteSize = bytesPerData * dataCount;
    HRESULT hr = SuballocateFromBuffer(byteSize, alignment);
    if (SUCCEEDED(hr))
    {
        byteOffset = UINT(m_pDataCur - m_pDataBegin);
        memcpy(m_pDataCur, pData, byteSize); 
        m_pDataCur += byteSize;
    }
    return hr;
}

//
// Align uLocation to the next multiple of uAlign.
//

UINT Align(UINT uLocation, UINT uAlign)
{
    if ( (0 == uAlign) || (uAlign & (uAlign-1)) )
    {
        ThrowException("non-pow2 alignment");
    }

    return ( (uLocation + (uAlign-1)) & ~(uAlign-1) );
}
```

<span data-ttu-id="77e32-120">請注意， [**CD3DX12_HEAP_PROPERTIES**](cd3dx12-heap-properties.md) 和 [**CD3DX12_RESOURCE_DESC**](cd3dx12-resource-desc.md)使用 helper 結構。</span><span class="sxs-lookup"><span data-stu-id="77e32-120">Note the use of the helper structures [**CD3DX12_HEAP_PROPERTIES**](cd3dx12-heap-properties.md) and [**CD3DX12_RESOURCE_DESC**](cd3dx12-resource-desc.md).</span></span>

## <a name="constants"></a><span data-ttu-id="77e32-121">常數</span><span class="sxs-lookup"><span data-stu-id="77e32-121">Constants</span></span>

<span data-ttu-id="77e32-122">若要在上傳或 readback 堆積內設定常數、頂點和索引，請使用下列 Api。</span><span class="sxs-lookup"><span data-stu-id="77e32-122">To set constants, vertices, and indexes within an upload or readback heap, use the following APIs.</span></span>

-   [<span data-ttu-id="77e32-123">**ID3D12Device::CreateConstantBufferView**</span><span class="sxs-lookup"><span data-stu-id="77e32-123">**ID3D12Device::CreateConstantBufferView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview)
-   [<span data-ttu-id="77e32-124">**ID3D12GraphicsCommandList::IASetVertexBuffers**</span><span class="sxs-lookup"><span data-stu-id="77e32-124">**ID3D12GraphicsCommandList::IASetVertexBuffers**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers)
-   [<span data-ttu-id="77e32-125">**ID3D12GraphicsCommandList::IASetIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="77e32-125">**ID3D12GraphicsCommandList::IASetIndexBuffer**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetindexbuffer)

## <a name="resources"></a><span data-ttu-id="77e32-126">資源</span><span class="sxs-lookup"><span data-stu-id="77e32-126">Resources</span></span>

<span data-ttu-id="77e32-127">資源是可抽象化 GPU 實體記憶體使用量的 Direct3D 概念。</span><span class="sxs-lookup"><span data-stu-id="77e32-127">Resources are the Direct3D concept that abstracts the usage of GPU physical memory.</span></span> <span data-ttu-id="77e32-128">資源需要 GPU 虛擬位址空間來存取實體記憶體。</span><span class="sxs-lookup"><span data-stu-id="77e32-128">Resources require GPU virtual address space to access physical memory.</span></span> <span data-ttu-id="77e32-129">資源建立是無限制執行緒。</span><span class="sxs-lookup"><span data-stu-id="77e32-129">Resource creation is free-threaded.</span></span>

<span data-ttu-id="77e32-130">有三種類型的資源是在 Direct3D 12 中建立和彈性的虛擬位址。</span><span class="sxs-lookup"><span data-stu-id="77e32-130">There are three types of resources with respect to virtual address creation and flexibility in Direct3D 12.</span></span>

### <a name="committed-resources"></a><span data-ttu-id="77e32-131">認可的資源</span><span class="sxs-lookup"><span data-stu-id="77e32-131">Committed resources</span></span>

<span data-ttu-id="77e32-132">認可的資源是最常見的 Direct3D 資源在世代上的概念。</span><span class="sxs-lookup"><span data-stu-id="77e32-132">Committed resources are the most common idea of Direct3D resources over the generations.</span></span> <span data-ttu-id="77e32-133">建立這類資源會配置虛擬位址範圍、夠大的隱含堆積來容納整個資源，然後將虛擬位址範圍認可到堆積所封裝的實體記憶體。</span><span class="sxs-lookup"><span data-stu-id="77e32-133">Creating such a resource allocates virtual address range, an implicit heap large enough to fit the whole resource, and commits the virtual address range to the physical memory encapsulated by the heap.</span></span> <span data-ttu-id="77e32-134">必須傳遞隱含堆積屬性，以符合與舊版 Direct3D 版本的功能同位。</span><span class="sxs-lookup"><span data-stu-id="77e32-134">The implicit heap properties must be passed to match functional parity with previous Direct3D versions.</span></span> <span data-ttu-id="77e32-135">請參閱 [**ID3D12Device：： CreateCommittedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource)。</span><span class="sxs-lookup"><span data-stu-id="77e32-135">Refer to [**ID3D12Device::CreateCommittedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).</span></span>

### <a name="reserved-resources"></a><span data-ttu-id="77e32-136">保留的資源</span><span class="sxs-lookup"><span data-stu-id="77e32-136">Reserved resources</span></span>

<span data-ttu-id="77e32-137">保留的資源相當於 Direct3D 11 磚資源。</span><span class="sxs-lookup"><span data-stu-id="77e32-137">Reserved resources are equivalent to Direct3D 11 tiled resources.</span></span> <span data-ttu-id="77e32-138">在建立時，只會配置虛擬位址範圍，而不會對應到任何堆積。</span><span class="sxs-lookup"><span data-stu-id="77e32-138">On their creation, only a virtual address range is allocated, and not mapped to any heap.</span></span> <span data-ttu-id="77e32-139">應用程式會稍後將這類資源對應至堆積。</span><span class="sxs-lookup"><span data-stu-id="77e32-139">The application will map such resources to heaps later.</span></span> <span data-ttu-id="77e32-140">這類資源的功能目前與 Direct3D 11 的功能不一樣，因為它們可以使用 [**UpdateTileMappings**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings)對應至64kb 圖格的堆積。</span><span class="sxs-lookup"><span data-stu-id="77e32-140">The capabilities of such resources are currently unchanged from Direct3D 11, as they can be mapped to a heap at a 64KB tile granularity with [**UpdateTileMappings**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings).</span></span> <span data-ttu-id="77e32-141">請參閱 [**ID3D12Device：： CreateReservedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createreservedresource)。</span><span class="sxs-lookup"><span data-stu-id="77e32-141">Refer to [**ID3D12Device::CreateReservedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createreservedresource).</span></span>

### <a name="placed-resources"></a><span data-ttu-id="77e32-142">放置的資源</span><span class="sxs-lookup"><span data-stu-id="77e32-142">Placed resources</span></span>

<span data-ttu-id="77e32-143">針對 Direct3D 12 的新新，您可以建立與資源分開的堆積。</span><span class="sxs-lookup"><span data-stu-id="77e32-143">New for Direct3D 12, you can create heaps separate from resources.</span></span> <span data-ttu-id="77e32-144">之後，您可以在單一堆積中找到多個資源。</span><span class="sxs-lookup"><span data-stu-id="77e32-144">Afterward, you can locate multiple resources within a single heap.</span></span> <span data-ttu-id="77e32-145">您可以這麼做，而不需要建立並排或保留的資源，讓您的應用程式可以直接建立所有資源類型的功能。</span><span class="sxs-lookup"><span data-stu-id="77e32-145">You can do that without creating tiled or reserved resources, enabling the capabilities for all resource types able to be created directly by your application.</span></span> <span data-ttu-id="77e32-146">多個資源可能會重迭，您必須使用 [**ID3D12GraphicsCommandList：： ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) 正確地重新使用實體記憶體。</span><span class="sxs-lookup"><span data-stu-id="77e32-146">Multiple resources might overlap, and you must use the [**ID3D12GraphicsCommandList::ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) to re-use physical memory correctly.</span></span> <span data-ttu-id="77e32-147">請參閱 [**ID3D12Device：： CreatePlacedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createplacedresource)。</span><span class="sxs-lookup"><span data-stu-id="77e32-147">Refer to [**ID3D12Device::CreatePlacedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createplacedresource).</span></span>

## <a name="resource-size-reflection"></a><span data-ttu-id="77e32-148">資源大小反映</span><span class="sxs-lookup"><span data-stu-id="77e32-148">Resource size reflection</span></span>

<span data-ttu-id="77e32-149">您必須使用資源大小反映，以瞭解具有未知材質版面配置的材質紋理在堆積中需要多少空間。</span><span class="sxs-lookup"><span data-stu-id="77e32-149">You must use resource size reflection to understand how much space textures with unknown texture layouts require in heaps.</span></span> <span data-ttu-id="77e32-150">緩衝區也受到支援，但大多是方便使用。</span><span class="sxs-lookup"><span data-stu-id="77e32-150">Buffers are also supported, but mostly as a convenience.</span></span>

<span data-ttu-id="77e32-151">您應該留意主要對齊差異，以協助封裝資源更密集。</span><span class="sxs-lookup"><span data-stu-id="77e32-151">You should be aware of major alignment discrepancies, to help pack resources more densely.</span></span>

<span data-ttu-id="77e32-152">例如，具有單一位元組緩衝區的單一元素陣列會傳回64KB 的 *大小* ，以及64的 *對齊方式* ，因為緩衝區只能是64kb 對齊。</span><span class="sxs-lookup"><span data-stu-id="77e32-152">For example, a single-element array with a one-byte-buffer returns a *Size* of 64KB, and an *Alignment* of 64KB, because buffers can be only 64KB-aligned.</span></span>

<span data-ttu-id="77e32-153">另外還有三個元素陣列，其中具有兩個單一材質64KB 對齊的紋理，以及一個材質4MB 對齊的材質，會根據陣列的順序來報告不同的大小。</span><span class="sxs-lookup"><span data-stu-id="77e32-153">Also, a three element array with two single-texel 64KB aligned textures and a single-texel 4MB aligned texture reports differing sizes based on the order of the array.</span></span> <span data-ttu-id="77e32-154">如果中間有4MB 對齊的紋理，則產生的 *大小* 為12MB。</span><span class="sxs-lookup"><span data-stu-id="77e32-154">If the 4MB aligned textures is in the middle, then the resulting *Size* is 12MB.</span></span> <span data-ttu-id="77e32-155">否則，產生的大小為 8 MB。</span><span class="sxs-lookup"><span data-stu-id="77e32-155">Otherwise, the resulting Size is 8MB.</span></span> <span data-ttu-id="77e32-156">傳回的對齊一律為4MB，也就是資源陣列中所有對齊的超集合。</span><span class="sxs-lookup"><span data-stu-id="77e32-156">The Alignment returned would always be 4MB, the superset of all alignments in the resource array.</span></span>

<span data-ttu-id="77e32-157">參考下列 Api。</span><span class="sxs-lookup"><span data-stu-id="77e32-157">Reference the following APIs.</span></span>

- [<span data-ttu-id="77e32-158">**D3D12 \_ 資源 \_ 分配 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="77e32-158">**D3D12\_RESOURCE\_ALLOCATION\_INFO**</span></span>](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)
- [<span data-ttu-id="77e32-159">**GetResourceAllocationInfo**</span><span class="sxs-lookup"><span data-stu-id="77e32-159">**GetResourceAllocationInfo**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo)

## <a name="buffer-alignment"></a><span data-ttu-id="77e32-160">緩衝區對齊</span><span class="sxs-lookup"><span data-stu-id="77e32-160">Buffer alignment</span></span>

<span data-ttu-id="77e32-161">緩衝區對齊限制尚未從 Direct3D 11 變更，值得注意的是：</span><span class="sxs-lookup"><span data-stu-id="77e32-161">Buffer alignment restrictions have not changed from Direct3D 11, notably:</span></span>

- <span data-ttu-id="77e32-162">適用于多範例紋理的 4 MB。</span><span class="sxs-lookup"><span data-stu-id="77e32-162">4 MB for multi-sample textures.</span></span>
- <span data-ttu-id="77e32-163">適用于單一範例紋理和緩衝區的 64 KB。</span><span class="sxs-lookup"><span data-stu-id="77e32-163">64 KB for single-sample textures and buffers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="77e32-164">相關主題</span><span class="sxs-lookup"><span data-stu-id="77e32-164">Related topics</span></span>

* [<span data-ttu-id="77e32-165">在緩衝區內進行子分配</span><span class="sxs-lookup"><span data-stu-id="77e32-165">Suballocation within buffers</span></span>](large-buffers.md)
