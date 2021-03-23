---
title: 透過緩衝區上傳材質資料
description: 上傳2D 或3D 紋理資料與上傳1D 資料類似，不同之處在于應用程式必須特別注意與資料列間距相關的資料對齊。
ms.assetid: 22A25A94-A45C-482D-853A-FA6860EE7E4E
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aadbd1e71b3c9895b75c973397488472b57f8eb1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548456"
---
# <a name="uploading-texture-data-through-buffers"></a><span data-ttu-id="86894-103">透過緩衝區上傳材質資料</span><span class="sxs-lookup"><span data-stu-id="86894-103">Uploading Texture Data Through Buffers</span></span>

<span data-ttu-id="86894-104">上傳2D 或3D 紋理資料與上傳1D 資料類似，不同之處在于應用程式必須特別注意與資料列間距相關的資料對齊。</span><span class="sxs-lookup"><span data-stu-id="86894-104">Uploading 2D or 3D texture data is similar to uploading 1D data, except that applications need to pay closer attention to data alignment related to row pitch.</span></span> <span data-ttu-id="86894-105">您可以從圖形管線的多個部分 orthogonally 和並行使用緩衝區，而且非常有彈性。</span><span class="sxs-lookup"><span data-stu-id="86894-105">Buffers can be used orthogonally and concurrently from multiple parts of the graphics pipeline, and are very flexible.</span></span>

-   [<span data-ttu-id="86894-106">透過緩衝區上傳材質資料</span><span class="sxs-lookup"><span data-stu-id="86894-106">Upload Texture Data via Buffers</span></span>](#upload-texture-data-via-buffers)
-   [<span data-ttu-id="86894-107">複製</span><span class="sxs-lookup"><span data-stu-id="86894-107">Copying</span></span>](#copying)
-   [<span data-ttu-id="86894-108">對應和取消對應</span><span class="sxs-lookup"><span data-stu-id="86894-108">Mapping and unmapping</span></span>](#mapping-and-unmapping)
-   [<span data-ttu-id="86894-109">緩衝區對齊</span><span class="sxs-lookup"><span data-stu-id="86894-109">Buffer alignment</span></span>](#buffer-alignment)
-   [<span data-ttu-id="86894-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="86894-110">Related topics</span></span>](#related-topics)

## <a name="upload-texture-data-via-buffers"></a><span data-ttu-id="86894-111">透過緩衝區上傳材質資料</span><span class="sxs-lookup"><span data-stu-id="86894-111">Upload Texture Data via Buffers</span></span>

<span data-ttu-id="86894-112">應用程式必須透過 [**ID3D12GraphicsCommandList：： CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) 或 [**ID3D12GraphicsCommandList：： CopyBufferRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)上傳資料。</span><span class="sxs-lookup"><span data-stu-id="86894-112">Applications must upload data via [**ID3D12GraphicsCommandList::CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) or [**ID3D12GraphicsCommandList::CopyBufferRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion).</span></span> <span data-ttu-id="86894-113">紋理資料更可能更大、不斷地存取，並受益于比其他資源資料更快的非線性記憶體配置的快取一致性。</span><span class="sxs-lookup"><span data-stu-id="86894-113">Texture data is much more likely to be larger, accessed repeatedly, and benefit from the improved cache-coherency of non-linear memory layouts than other resource data.</span></span> <span data-ttu-id="86894-114">在 D3D12 中使用緩衝區時，只要滿足記憶體對齊需求，應用程式就可以完全掌控與複製資源資料相關聯的資料放置和相片順序。</span><span class="sxs-lookup"><span data-stu-id="86894-114">When buffers are used in D3D12, applications have full control on data placement and arrangement associated with copying resource data around, as long as the memory alignment requirements are satisfied.</span></span>

<span data-ttu-id="86894-115">此範例會反白顯示應用程式在將2D 資料放入緩衝區之前，直接將2D 資料壓平合併成1D。</span><span class="sxs-lookup"><span data-stu-id="86894-115">The sample highlights where the application simply flattens 2D data into 1D before placing it in the buffer.</span></span> <span data-ttu-id="86894-116">在 mipmap 2D 案例中，應用程式可以將每個子資源分開簡維，並快速使用1D 子配置演算法，或使用更複雜的2D 子配置技術來將視訊記憶體的使用率降至最低。</span><span class="sxs-lookup"><span data-stu-id="86894-116">For the mipmap 2D scenario, the application can either flatten each sub-resource discretely and quickly use a 1D sub-allocation algorithm, or, use a more complicated 2D sub-allocation technique to minimize video memory utilization.</span></span> <span data-ttu-id="86894-117">第一個技巧應更頻繁地使用，因為它較為簡單。</span><span class="sxs-lookup"><span data-stu-id="86894-117">The first technique is expected to be used more often as it is simpler.</span></span> <span data-ttu-id="86894-118">當將資料封裝到磁片或網路上時，第二項技術可能會很有用。</span><span class="sxs-lookup"><span data-stu-id="86894-118">The second technique may be useful when packing data onto a disk or across a network.</span></span> <span data-ttu-id="86894-119">無論是哪一種情況，應用程式仍必須呼叫每個子資源的複製 Api。</span><span class="sxs-lookup"><span data-stu-id="86894-119">In either case, the application must still call the copy APIs for each sub-resource.</span></span>

``` syntax
// Prepare a pBitmap in memory, with bitmapWidth, bitmapHeight, and pixel format of DXGI_FORMAT_B8G8R8A8_UNORM. 
//
// Sub-allocate from the buffer for texture data.
//

D3D12_SUBRESOURCE_FOOTPRINT pitchedDesc = { 0 };
pitchedDesc.Format = DXGI_FORMAT_B8G8R8A8_UNORM;
pitchedDesc.Width = bitmapWidth;
pitchedDesc.Height = bitmapHeight;
pitchedDesc.Depth = 1;
pitchedDesc.RowPitch = Align(bitmapWidth * sizeof(DWORD), D3D12_TEXTURE_DATA_PITCH_ALIGNMENT);

//
// Note that the helper function UpdateSubresource in D3DX12.h, and ID3D12Device::GetCopyableFootprints 
// can help applications fill out D3D12_SUBRESOURCE_FOOTPRINT and D3D12_PLACED_SUBRESOURCE_FOOTPRINT structures.
//
// Refer to the D3D12 Code example for the previous section "Uploading Different Types of Resources"
// for the code for SuballocateFromBuffer.
//

SuballocateFromBuffer(
    pitchedDesc.Height * pitchedDesc.RowPitch,
    D3D12_TEXTURE_DATA_PLACEMENT_ALIGNMENT
    );

D3D12_PLACED_SUBRESOURCE_FOOTPRINT placedTexture2D = { 0 };
placedTexture2D.Offset = m_pDataCur – m_pDataBegin;
placedTexture2D.Footprint = pitchedDesc;

//
// Copy texture data from DWORD* pBitmap->pixels to the buffer
//

for (UINT y = 0; y < bitmapHeight; y++)
{
  UINT8 *pScan = m_pDataBegin + placedTexture2D.Offset + y * pitchedDesc.RowPitch;
  memcpy( pScan, &(pBitmap->pixels[y * bitmapWidth]), sizeof(DWORD) * bitmapWidth );
}

//
// Create default texture2D resource.
//

D3D12_RESOURCE_DESC  textureDesc { ... };

CComPtr<ID3D12Resource> texture2D;
d3dDevice->CreateCommittedResource( 
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT), 
        D3D12_HEAP_FLAG_NONE, &textureDesc, 
        D3D12_RESOURCE_STATE_COPY_DEST, 
        nullptr, 
        IID_PPV_ARGS(&texture2D) );

//
// Copy heap data to texture2D.
//

commandList->CopyTextureRegion( 
        &CD3DX12_TEXTURE_COPY_LOCATION( texture2D, 0 ), 
        0, 0, 0, 
        &CD3DX12_TEXTURE_COPY_LOCATION( m_spUploadHeap, placedTexture2D ), 
        nullptr );
```

<span data-ttu-id="86894-120">請注意，使用 helper 結構 [**CD3DX12 \_ 堆積 \_ 屬性**](cd3dx12-heap-properties.md) 和 [**CD3DX12 \_ 材質 \_ 複製 \_ 位置**](cd3dx12-texture-copy-location.md)，以及 [**CreateCommittedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource) 和 [**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)的方法。</span><span class="sxs-lookup"><span data-stu-id="86894-120">Note the use of the helper structures [**CD3DX12\_HEAP\_PROPERTIES**](cd3dx12-heap-properties.md) and [**CD3DX12\_TEXTURE\_COPY\_LOCATION**](cd3dx12-texture-copy-location.md), and the methods [**CreateCommittedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource) and [**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion).</span></span>

## <a name="copying"></a><span data-ttu-id="86894-121">複製</span><span class="sxs-lookup"><span data-stu-id="86894-121">Copying</span></span>

<span data-ttu-id="86894-122">D3D12 方法可讓應用程式取代 D3D11 [**UpdateSubresource**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-updatesubresource)、 [**CopySubresourceRegion**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-copysubresourceregion)和資源初始資料。</span><span class="sxs-lookup"><span data-stu-id="86894-122">D3D12 methods enable applications to replace D3D11 [**UpdateSubresource**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-updatesubresource), [**CopySubresourceRegion**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-copysubresourceregion), and resource initial data.</span></span> <span data-ttu-id="86894-123">資料列主要紋理資料的單一 3D subresource 有可能位於緩衝區資源中。</span><span class="sxs-lookup"><span data-stu-id="86894-123">A single 3D subresource worth of row-major texture data may be located in buffer resources.</span></span> <span data-ttu-id="86894-124">[**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) 可以從緩衝區將該材質資料複製到具有未知材質配置的材質資源，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="86894-124">[**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) can copy that texture data from the buffer to a texture resource with an unknown texture layout, and vice versa.</span></span> <span data-ttu-id="86894-125">應用程式應該使用這種類型的技術來填入經常存取的 GPU 資源，方法是在沒有 CPU 存取的預設堆積中建立經常存取的 GPU 資源時，在上傳堆積中建立大型緩衝區。</span><span class="sxs-lookup"><span data-stu-id="86894-125">Applications should prefer this type of technique to populate frequently accessed GPU resources, by creating large buffers in an UPLOAD heap while creating the frequently accessed GPU resources in a DEFAULT heap that has no CPU access.</span></span> <span data-ttu-id="86894-126">這種技術可有效率地支援離散 Gpu 及其大量的 CPU 無法存取的記憶體，而不需要經常因而影響的 UMA 架構。</span><span class="sxs-lookup"><span data-stu-id="86894-126">Such a technique efficiently supports discrete GPUs and their large amounts of CPU-inaccessible memory, without commonly impairing UMA architectures.</span></span>

<span data-ttu-id="86894-127">請注意下列兩個常數：</span><span class="sxs-lookup"><span data-stu-id="86894-127">Note the following two constants:</span></span>

``` syntax
const UINT D3D12_TEXTURE_DATA_PITCH_ALIGNMENT = 256;
const UINT D3D12_TEXTURE_DATA_PLACEMENT_ALIGNMENT = 512;
```

-   [<span data-ttu-id="86894-128">**D3D12 \_ SUBRESOURCE \_ 足跡**</span><span class="sxs-lookup"><span data-stu-id="86894-128">**D3D12\_SUBRESOURCE\_FOOTPRINT**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint)
-   [<span data-ttu-id="86894-129">**D3D12 \_ 放置的 \_ SUBRESOURCE \_ 足跡**</span><span class="sxs-lookup"><span data-stu-id="86894-129">**D3D12\_PLACED\_SUBRESOURCE\_FOOTPRINT**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint)
-   [<span data-ttu-id="86894-130">**D3D12 \_ 材質 \_ 複製 \_ 位置**</span><span class="sxs-lookup"><span data-stu-id="86894-130">**D3D12\_TEXTURE\_COPY\_LOCATION**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location)
-   [<span data-ttu-id="86894-131">**D3D12 \_ 材質 \_ 複製 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="86894-131">**D3D12\_TEXTURE\_COPY\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_copy_type)
-   [<span data-ttu-id="86894-132">**ID3D12Device::GetCopyableFootprints**</span><span class="sxs-lookup"><span data-stu-id="86894-132">**ID3D12Device::GetCopyableFootprints**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints)
-   [<span data-ttu-id="86894-133">**ID3D12GraphicsCommandList::CopyResource**</span><span class="sxs-lookup"><span data-stu-id="86894-133">**ID3D12GraphicsCommandList::CopyResource**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
-   [<span data-ttu-id="86894-134">**ID3D12GraphicsCommandList::CopyTextureRegion**</span><span class="sxs-lookup"><span data-stu-id="86894-134">**ID3D12GraphicsCommandList::CopyTextureRegion**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
-   [<span data-ttu-id="86894-135">**ID3D12GraphicsCommandList::CopyBufferRegion**</span><span class="sxs-lookup"><span data-stu-id="86894-135">**ID3D12GraphicsCommandList::CopyBufferRegion**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
-   [<span data-ttu-id="86894-136">**ID3D12GraphicsCommandList::CopyTiles**</span><span class="sxs-lookup"><span data-stu-id="86894-136">**ID3D12GraphicsCommandList::CopyTiles**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles)
-   [<span data-ttu-id="86894-137">**ID3D12CommandQueue::UpdateTileMappings**</span><span class="sxs-lookup"><span data-stu-id="86894-137">**ID3D12CommandQueue::UpdateTileMappings**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings)

## <a name="mapping-and-unmapping"></a><span data-ttu-id="86894-138">對應和取消對應</span><span class="sxs-lookup"><span data-stu-id="86894-138">Mapping and unmapping</span></span>

<span data-ttu-id="86894-139">您可以安全地呼叫多個執行緒的對應 [**和取消**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap)[**對應**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map)。</span><span class="sxs-lookup"><span data-stu-id="86894-139">[**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) and [**Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) can be called by multiple threads safely.</span></span> <span data-ttu-id="86894-140">**對應** 的第一個呼叫會配置資源的 CPU 虛擬位址範圍。</span><span class="sxs-lookup"><span data-stu-id="86894-140">The first call to **Map** allocates a CPU virtual address range for the resource.</span></span> <span data-ttu-id="86894-141">取消對應的最後一個呼叫會解除配置 CPU 虛擬位址範圍。</span><span class="sxs-lookup"><span data-stu-id="86894-141">The last call to **Unmap** deallocates the CPU virtual address range.</span></span> <span data-ttu-id="86894-142">CPU 虛擬位址通常會傳回給應用程式。</span><span class="sxs-lookup"><span data-stu-id="86894-142">The CPU virtual address is commonly returned to the application.</span></span>

<span data-ttu-id="86894-143">只要透過 readback 堆積中的資源，在 CPU 和 GPU 之間傳遞資料，就必須使用對應和取消 [**對應**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) [**，以**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) 支援在上支援 D3D12 的所有系統。</span><span class="sxs-lookup"><span data-stu-id="86894-143">Whenever data is passed between the CPU and GPU through resources in readback heaps, [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) and [**Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) must be used to support all systems D3D12 is supported on.</span></span> <span data-ttu-id="86894-144">盡可能讓範圍盡可能緊密地保持最高效率， (參考 [**D3D12 \_ 範圍**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range)) 。</span><span class="sxs-lookup"><span data-stu-id="86894-144">Keeping the ranges as tight as possible maximizes efficiency on the systems that require ranges (refer to [**D3D12\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range)).</span></span>

<span data-ttu-id="86894-145">偵錯工具的效能不僅受益于所有 [**地圖取消對應**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map)呼叫上的精確使用範圍  /  [](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) ，也可讓應用程式在不再進行 CPU 修改時取消對應資源。</span><span class="sxs-lookup"><span data-stu-id="86894-145">The performance of debugging tools benefit not only from the accurate usage of ranges on all [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) / [**Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) calls, but also from applications unmapping resources when CPU modifications will no longer be made.</span></span>

<span data-ttu-id="86894-146">D3D12 不支援使用 [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) (搭配捨棄參數設定) 來重新命名資源的 D3D11 方法。</span><span class="sxs-lookup"><span data-stu-id="86894-146">The D3D11 method of using [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) (with the DISCARD parameter set) to rename resources is not supported in D3D12.</span></span> <span data-ttu-id="86894-147">應用程式必須自行執行資源重新命名。</span><span class="sxs-lookup"><span data-stu-id="86894-147">Applications must implement resource renaming themselves.</span></span> <span data-ttu-id="86894-148">所有的 **對應** 呼叫都隱含地沒有 \_ 覆寫和多執行緒。</span><span class="sxs-lookup"><span data-stu-id="86894-148">All **Map** calls are implicitly NO\_OVERWRITE and multi-threaded.</span></span> <span data-ttu-id="86894-149">應用程式必須負責確保命令清單中包含的所有相關 GPU 工作都已完成，然後才能存取 CPU 的資料。</span><span class="sxs-lookup"><span data-stu-id="86894-149">It is the application’s responsibility to ensure that any relevant GPU work contained in command lists is finished before the accessing data with the CPU.</span></span> <span data-ttu-id="86894-150">D3D12 的 **對應** 呼叫不會隱含地排清任何命令緩衝區，也不會封鎖等候 GPU 完成工作。</span><span class="sxs-lookup"><span data-stu-id="86894-150">D3D12 calls to **Map** do not implicitly flush any command buffers, nor do they block waiting for the GPU to finish work.</span></span> <span data-ttu-id="86894-151">因此，在某些情況下 [**，可能甚至會將**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap)對應和取消 **對應** 優化。</span><span class="sxs-lookup"><span data-stu-id="86894-151">As a result, **Map** and [**Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) may even be optimized out in some scenarios.</span></span>

## <a name="buffer-alignment"></a><span data-ttu-id="86894-152">緩衝區對齊</span><span class="sxs-lookup"><span data-stu-id="86894-152">Buffer alignment</span></span>

<span data-ttu-id="86894-153">緩衝區對齊限制：</span><span class="sxs-lookup"><span data-stu-id="86894-153">Buffer alignment restrictions:</span></span>

-   <span data-ttu-id="86894-154">線性 subresource 複製必須對齊512個位元組 (資料列間距對齊 D3D12 \_ 材質 \_ 資料 \_ 間距 \_ 對齊位元組) 。</span><span class="sxs-lookup"><span data-stu-id="86894-154">Linear subresource copying must be aligned to 512 bytes (with the row pitch aligned to D3D12\_TEXTURE\_DATA\_PITCH\_ALIGNMENT bytes).</span></span>
-   <span data-ttu-id="86894-155">常數資料讀取必須是來自堆積開頭的256個位元組倍數 (也就是，只有來自256位元組對齊) 的位址。</span><span class="sxs-lookup"><span data-stu-id="86894-155">Constant data reads must be a multiple of 256 bytes from the beginning of the heap (i.e. only from addresses that are 256-byte aligned).</span></span>
-   <span data-ttu-id="86894-156">索引資料讀取必須是索引資料類型大小的倍數 (亦即，僅來自針對資料) 自然對齊的位址。</span><span class="sxs-lookup"><span data-stu-id="86894-156">Index data reads must be a multiple of the index data type size (i.e. only from addresses that are naturally aligned for the data).</span></span>
-   <span data-ttu-id="86894-157">[**ID3D12GraphicsCommandList：:D rawinstanced**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced) 和 [**ID3D12GraphicsCommandList：:D rawindexedinstanced**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawindexedinstanced) 資料必須是來自 (4 的倍數的位移，也就是只有來自以 DWORD 對齊) 的位址。</span><span class="sxs-lookup"><span data-stu-id="86894-157">[**ID3D12GraphicsCommandList::DrawInstanced**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced) and [**ID3D12GraphicsCommandList::DrawIndexedInstanced**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawindexedinstanced) data must be from offsets that are multiples of 4 (i.e. only from addresses that are DWORD aligned).</span></span>

## <a name="related-topics"></a><span data-ttu-id="86894-158">相關主題</span><span class="sxs-lookup"><span data-stu-id="86894-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86894-159">在緩衝區內進行子分配</span><span class="sxs-lookup"><span data-stu-id="86894-159">Suballocation Within Buffers</span></span>](large-buffers.md)
</dt> </dl>

 

 