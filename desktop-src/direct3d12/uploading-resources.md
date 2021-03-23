---
title: 上傳不同類型的資源
description: 示範如何使用一個緩衝區，將常數緩衝區資料和頂點緩衝區資料上傳至 GPU，以及如何適當地子配置和將資料放在緩衝區中。
ms.assetid: 255B0482-21D6-4276-8009-3F3891879CA1
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd2edca2cd9f4d3becf5036056a89f91c50f2c24
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104607"
---
# <a name="uploading-different-types-of-resources"></a><span data-ttu-id="55664-103">上傳不同類型的資源</span><span class="sxs-lookup"><span data-stu-id="55664-103">Uploading Different Types of Resources</span></span>

<span data-ttu-id="55664-104">示範如何使用一個緩衝區，將常數緩衝區資料和頂點緩衝區資料上傳至 GPU，以及如何適當地子配置和將資料放在緩衝區中。</span><span class="sxs-lookup"><span data-stu-id="55664-104">Shows how to use one buffer to upload both constant buffer data and vertex buffer data to the GPU, and how to properly sub-allocate and place data within buffers.</span></span> <span data-ttu-id="55664-105">使用單一緩衝區可增加記憶體使用量的彈性，並提供應用程式更緊密地控制記憶體使用量。</span><span class="sxs-lookup"><span data-stu-id="55664-105">The use of one single buffer increases memory usage flexibility and provides applications with tighter control of memory usage.</span></span> <span data-ttu-id="55664-106">也會顯示 D3D11 和 D3D12 模型之間的差異，以便上傳不同類型的資源。</span><span class="sxs-lookup"><span data-stu-id="55664-106">Also shows the differences between the D3D11 and D3D12 models for uploading different types of resources.</span></span>

-   [<span data-ttu-id="55664-107">上傳不同類型的資源</span><span class="sxs-lookup"><span data-stu-id="55664-107">Upload Different Types of Resources</span></span>](#upload-different-types-of-resources)
    -   [<span data-ttu-id="55664-108">程式碼範例： D3D11</span><span class="sxs-lookup"><span data-stu-id="55664-108">Code Example: D3D11</span></span>](#code-example-d3d11)
    -   [<span data-ttu-id="55664-109">程式碼範例： D3D12</span><span class="sxs-lookup"><span data-stu-id="55664-109">Code Example: D3D12</span></span>](#code-example-d3d12)
-   [<span data-ttu-id="55664-110">常數</span><span class="sxs-lookup"><span data-stu-id="55664-110">Constants</span></span>](#constants)
-   [<span data-ttu-id="55664-111">資源</span><span class="sxs-lookup"><span data-stu-id="55664-111">Resources</span></span>](#uploading-different-types-of-resources)
-   [<span data-ttu-id="55664-112">資源大小反映</span><span class="sxs-lookup"><span data-stu-id="55664-112">Resource size reflection</span></span>](#resource-size-reflection)
-   [<span data-ttu-id="55664-113">緩衝區對齊</span><span class="sxs-lookup"><span data-stu-id="55664-113">Buffer alignment</span></span>](#buffer-alignment)
-   [<span data-ttu-id="55664-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="55664-114">Related topics</span></span>](#related-topics)

## <a name="upload-different-types-of-resources"></a><span data-ttu-id="55664-115">上傳不同類型的資源</span><span class="sxs-lookup"><span data-stu-id="55664-115">Upload Different Types of Resources</span></span>

<span data-ttu-id="55664-116">在 D3D12 中，應用程式會建立一個緩衝區來容納不同類型的資源資料以進行上傳，並以類似的方式將資源資料複製到相同的緩衝區，以用於不同的資源資料。</span><span class="sxs-lookup"><span data-stu-id="55664-116">In D3D12, applications create one buffer to accommodate different types of resource data for uploading, and copy resource data to the same buffer in a similar way for different resource data.</span></span> <span data-ttu-id="55664-117">接著會建立個別的視圖，以將這些資源資料系結至新資源系結模型中的圖形管線。</span><span class="sxs-lookup"><span data-stu-id="55664-117">Individual views are then created to bind those resource data to the graphics pipeline in the new resource binding model.</span></span>

<span data-ttu-id="55664-118">在 D3D11 中，應用程式會針對不同類型的資源資料建立不同的緩衝區 (請注意 `BindFlags` 下列 D3D11 範例程式碼中所用的不同) 、將每個資源緩衝區明確系結至圖形管線，以及根據不同的資源類型，以不同的方法更新資源資料。</span><span class="sxs-lookup"><span data-stu-id="55664-118">In D3D11, applications create separate buffers for different types of resource data (note the different `BindFlags` used in the D3D11 sample code below), explicitly binding each resource buffer to the graphics pipeline, and update the resource data with different methods based on different resource types.</span></span>

<span data-ttu-id="55664-119">在 D3D12 和 D3D11 中，應用程式只應使用上傳資源，其中 CPU 會寫入資料一次，而且 GPU 會讀取一次。</span><span class="sxs-lookup"><span data-stu-id="55664-119">In both D3D12 and D3D11, applications should only use upload resources where the CPU will write the data once and the GPU will read it once.</span></span> <span data-ttu-id="55664-120">如果 GPU 會多次讀取資料，GPU 將不會以線性方式讀取資料，或轉譯已大幅限制 GPU。</span><span class="sxs-lookup"><span data-stu-id="55664-120">If the GPU will read the data multiple times, the GPU will not read the data linearly, or the rendering is significantly GPU-limited already.</span></span> <span data-ttu-id="55664-121">更好的選項可能是使用 [**ID3D12GraphicsCommandList：： CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) 或 [**ID3D12GraphicsCommandList：： CopyBufferRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion) 將上傳緩衝區資料複製到預設資源。</span><span class="sxs-lookup"><span data-stu-id="55664-121">The better option may be to use [**ID3D12GraphicsCommandList::CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) or [**ID3D12GraphicsCommandList::CopyBufferRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion) to copy the upload buffer data to a default resource.</span></span> <span data-ttu-id="55664-122">預設資源可以位於離散 Gpu 的實體視頻記憶體中。</span><span class="sxs-lookup"><span data-stu-id="55664-122">A default resource can reside in physical video memory on discrete GPUs.</span></span>

### <a name="code-example-d3d11"></a><span data-ttu-id="55664-123">程式碼範例： D3D11</span><span class="sxs-lookup"><span data-stu-id="55664-123">Code Example: D3D11</span></span>

``` syntax
// D3D11: Separate buffers for each resource type.

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

### <a name="code-example-d3d12"></a><span data-ttu-id="55664-124">程式碼範例： D3D12</span><span class="sxs-lookup"><span data-stu-id="55664-124">Code Example: D3D12</span></span>

``` syntax
// D3D12: One buffer to accommodate different types of resources

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

<span data-ttu-id="55664-125">請注意，使用 helper 結構 [**CD3DX12 \_ 堆積 \_ 屬性**](cd3dx12-heap-properties.md) 和 [**CD3DX12 \_ 資源 \_ DESC**](cd3dx12-resource-desc.md)。</span><span class="sxs-lookup"><span data-stu-id="55664-125">Note the use of the helper structures [**CD3DX12\_HEAP\_PROPERTIES**](cd3dx12-heap-properties.md) and [**CD3DX12\_RESOURCE\_DESC**](cd3dx12-resource-desc.md).</span></span>

## <a name="constants"></a><span data-ttu-id="55664-126">常數</span><span class="sxs-lookup"><span data-stu-id="55664-126">Constants</span></span>

<span data-ttu-id="55664-127">若要在上傳或 Readback 堆積內設定常數、頂點和索引，請使用下列 Api：</span><span class="sxs-lookup"><span data-stu-id="55664-127">To set constants, vertices and indexes within an Upload or Readback heap, use the following APIs:</span></span>

-   [<span data-ttu-id="55664-128">**ID3D12Device::CreateConstantBufferView**</span><span class="sxs-lookup"><span data-stu-id="55664-128">**ID3D12Device::CreateConstantBufferView**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview)
-   [<span data-ttu-id="55664-129">**ID3D12GraphicsCommandList::IASetVertexBuffers**</span><span class="sxs-lookup"><span data-stu-id="55664-129">**ID3D12GraphicsCommandList::IASetVertexBuffers**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers)
-   [<span data-ttu-id="55664-130">**ID3D12GraphicsCommandList::IASetIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="55664-130">**ID3D12GraphicsCommandList::IASetIndexBuffer**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetindexbuffer)

## <a name="resources"></a><span data-ttu-id="55664-131">資源</span><span class="sxs-lookup"><span data-stu-id="55664-131">Resources</span></span>

<span data-ttu-id="55664-132">資源是可抽象化 GPU 實體記憶體使用量的 D3D 概念。</span><span class="sxs-lookup"><span data-stu-id="55664-132">Resources are the D3D concept which abstracts the usage of GPU physical memory.</span></span> <span data-ttu-id="55664-133">資源需要 GPU 虛擬位址空間來存取實體記憶體。</span><span class="sxs-lookup"><span data-stu-id="55664-133">Resources require GPU virtual address space to access physical memory.</span></span> <span data-ttu-id="55664-134">資源建立是無限制執行緒。</span><span class="sxs-lookup"><span data-stu-id="55664-134">Resource creation is free-threaded.</span></span>

<span data-ttu-id="55664-135">有三種類型的資源與虛擬位址建立和 D3D12 的彈性有關：</span><span class="sxs-lookup"><span data-stu-id="55664-135">There are three types of resources with respect to virtual address creation and flexibility in D3D12:</span></span>

-   <span data-ttu-id="55664-136">認可的資源</span><span class="sxs-lookup"><span data-stu-id="55664-136">Committed resources</span></span>

    <span data-ttu-id="55664-137">認可的資源是在世代上最常見的 D3D 資源概念。</span><span class="sxs-lookup"><span data-stu-id="55664-137">Committed resources are the most common idea of D3D resources over the generations.</span></span> <span data-ttu-id="55664-138">建立這類資源會配置虛擬位址範圍、夠大的隱含堆積來容納整個資源，然後將虛擬位址範圍認可到堆積所封裝的實體記憶體。</span><span class="sxs-lookup"><span data-stu-id="55664-138">Creating such a resource allocates virtual address range, an implicit heap large enough to fit the whole resource, and commits the virtual address range to the physical memory encapsulated by the heap.</span></span> <span data-ttu-id="55664-139">必須傳遞隱含堆積屬性，以符合與舊版 D3D 的功能同位。</span><span class="sxs-lookup"><span data-stu-id="55664-139">The implicit heap properties must be passed to match functional parity with previous D3D versions.</span></span> <span data-ttu-id="55664-140">請參閱 [**ID3D12Device：： CreateCommittedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource)。</span><span class="sxs-lookup"><span data-stu-id="55664-140">Refer to [**ID3D12Device::CreateCommittedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).</span></span>

-   <span data-ttu-id="55664-141">保留的資源</span><span class="sxs-lookup"><span data-stu-id="55664-141">Reserved resources</span></span>

    <span data-ttu-id="55664-142">保留的資源相當於 D3D11 的磚資源。</span><span class="sxs-lookup"><span data-stu-id="55664-142">Reserved resources are equivalent to D3D11 tiled resources.</span></span> <span data-ttu-id="55664-143">建立時，只會配置虛擬位址範圍，而不會對應到任何堆積。</span><span class="sxs-lookup"><span data-stu-id="55664-143">On their creation, only a virtual address range is allocated and not mapped to any heap.</span></span> <span data-ttu-id="55664-144">應用程式會稍後將這類資源對應至堆積。</span><span class="sxs-lookup"><span data-stu-id="55664-144">The application will map such resources to heaps later.</span></span> <span data-ttu-id="55664-145">這類資源的功能目前在 D3D11 中是不變的，因為它們可以使用 [**UpdateTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings)對應至64kb 圖格的堆積。</span><span class="sxs-lookup"><span data-stu-id="55664-145">The capabilities of such resources are currently unchanged over D3D11, as they can be mapped to a heap at a 64KB tile granularity with [**UpdateTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings).</span></span> <span data-ttu-id="55664-146">請參閱 [ **ID3D12Device：： CreateReservedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createreservedresource)</span><span class="sxs-lookup"><span data-stu-id="55664-146">Refer to [**ID3D12Device::CreateReservedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createreservedresource)</span></span>

-   <span data-ttu-id="55664-147">放置的資源</span><span class="sxs-lookup"><span data-stu-id="55664-147">Placed resources</span></span>

    <span data-ttu-id="55664-148">新的 D3D12，應用程式可以建立與資源分開的堆積。</span><span class="sxs-lookup"><span data-stu-id="55664-148">New for D3D12, applications may create heaps separate from resources.</span></span> <span data-ttu-id="55664-149">之後，應用程式可能會在單一堆積中找到多個資源。</span><span class="sxs-lookup"><span data-stu-id="55664-149">Afterward, the application may locate multiple resources within a single heap.</span></span> <span data-ttu-id="55664-150">您可以在不建立並排或保留的資源的情況下完成這項工作，以啟用可直接由應用程式建立之所有資源類型的功能。</span><span class="sxs-lookup"><span data-stu-id="55664-150">This can be done without creating tiled or reserved resources, enabling the capabilities for all resource types able to be created directly by applications.</span></span> <span data-ttu-id="55664-151">多個資源可能會重迭，而且應用程式必須使用 `TiledResourceBarrier` 來正確地重新使用實體記憶體。</span><span class="sxs-lookup"><span data-stu-id="55664-151">Multiple resources may overlap, and the application must use the `TiledResourceBarrier` to re-use physical memory correctly.</span></span> <span data-ttu-id="55664-152">請參閱 [ **ID3D12Device：： CreatePlacedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource)</span><span class="sxs-lookup"><span data-stu-id="55664-152">Refer to [**ID3D12Device::CreatePlacedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource)</span></span>

## <a name="resource-size-reflection"></a><span data-ttu-id="55664-153">資源大小反映</span><span class="sxs-lookup"><span data-stu-id="55664-153">Resource size reflection</span></span>

<span data-ttu-id="55664-154">應用程式必須使用資源大小反映，以瞭解有未知材質配置在堆積中有多少房間紋理。</span><span class="sxs-lookup"><span data-stu-id="55664-154">Applications must use resource size reflection to understand how much room textures with unknown texture layouts require in heaps.</span></span> <span data-ttu-id="55664-155">緩衝區也受到支援，但大多是方便使用。</span><span class="sxs-lookup"><span data-stu-id="55664-155">Buffers are also supported, but mostly as a convenience.</span></span>

<span data-ttu-id="55664-156">應用程式應留意主要對齊差異，以協助封裝資源更密集。</span><span class="sxs-lookup"><span data-stu-id="55664-156">Applications should be aware of major alignment discrepancies, to help pack resources more densely.</span></span>

<span data-ttu-id="55664-157">例如，具有單一位元組緩衝區的單一元素陣列會傳回64KB 的大小和64的對齊，因為緩衝區目前只能對齊64KB。</span><span class="sxs-lookup"><span data-stu-id="55664-157">For example, a single-element array with a one-byte-buffer returns a Size of 64KB and an Alignment of 64KB, as buffers currently can only be 64KB aligned.</span></span>

<span data-ttu-id="55664-158">另外還有三個元素陣列，其中具有兩個單一材質64KB 對齊的紋理，以及一個材質4MB 對齊的材質，會根據陣列的順序來報告不同的大小。</span><span class="sxs-lookup"><span data-stu-id="55664-158">Also, a three element array with two single-texel 64KB aligned textures and a single-texel 4MB aligned texture reports differing sizes based on the order of the array.</span></span> <span data-ttu-id="55664-159">如果中間有4MB 對齊的紋理，則產生的大小為12MB。</span><span class="sxs-lookup"><span data-stu-id="55664-159">If the 4MB aligned textures is in the middle, the resulting Size is 12MB.</span></span> <span data-ttu-id="55664-160">否則，產生的大小為 8 MB。</span><span class="sxs-lookup"><span data-stu-id="55664-160">Otherwise, the resulting Size is 8MB.</span></span> <span data-ttu-id="55664-161">傳回的對齊一律為4MB，也就是資源陣列中所有對齊的超級集合。</span><span class="sxs-lookup"><span data-stu-id="55664-161">The Alignment returned would always be 4MB, the super-set of all alignments in the resource array.</span></span>

<span data-ttu-id="55664-162">參考下列 Api：</span><span class="sxs-lookup"><span data-stu-id="55664-162">Reference the following APIs:</span></span>

-   [<span data-ttu-id="55664-163">**D3D12 \_ 資源 \_ 分配 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="55664-163">**D3D12\_RESOURCE\_ALLOCATION\_INFO**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)
-   [<span data-ttu-id="55664-164">**GetResourceAllocationInfo**</span><span class="sxs-lookup"><span data-stu-id="55664-164">**GetResourceAllocationInfo**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo)

## <a name="buffer-alignment"></a><span data-ttu-id="55664-165">緩衝區對齊</span><span class="sxs-lookup"><span data-stu-id="55664-165">Buffer alignment</span></span>

<span data-ttu-id="55664-166">緩衝區對齊限制未變更 D3D11，特別是：</span><span class="sxs-lookup"><span data-stu-id="55664-166">Buffer alignment restrictions have not changed from D3D11, notably:</span></span>

-   <span data-ttu-id="55664-167">適用于多範例紋理的 4 MB。</span><span class="sxs-lookup"><span data-stu-id="55664-167">4 MB for multi-sample textures.</span></span>
-   <span data-ttu-id="55664-168">適用于單一範例紋理和緩衝區的 64 KB。</span><span class="sxs-lookup"><span data-stu-id="55664-168">64 KB for single-sample textures and buffers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="55664-169">相關主題</span><span class="sxs-lookup"><span data-stu-id="55664-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55664-170">在緩衝區內進行子分配</span><span class="sxs-lookup"><span data-stu-id="55664-170">Suballocation Within Buffers</span></span>](large-buffers.md)
</dt> </dl>

 

 




