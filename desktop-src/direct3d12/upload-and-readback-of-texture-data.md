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
# <a name="uploading-texture-data-through-buffers"></a>透過緩衝區上傳材質資料

上傳2D 或3D 紋理資料與上傳1D 資料類似，不同之處在于應用程式必須特別注意與資料列間距相關的資料對齊。 您可以從圖形管線的多個部分 orthogonally 和並行使用緩衝區，而且非常有彈性。

-   [透過緩衝區上傳材質資料](#upload-texture-data-via-buffers)
-   [複製](#copying)
-   [對應和取消對應](#mapping-and-unmapping)
-   [緩衝區對齊](#buffer-alignment)
-   [相關主題](#related-topics)

## <a name="upload-texture-data-via-buffers"></a>透過緩衝區上傳材質資料

應用程式必須透過 [**ID3D12GraphicsCommandList：： CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) 或 [**ID3D12GraphicsCommandList：： CopyBufferRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)上傳資料。 紋理資料更可能更大、不斷地存取，並受益于比其他資源資料更快的非線性記憶體配置的快取一致性。 在 D3D12 中使用緩衝區時，只要滿足記憶體對齊需求，應用程式就可以完全掌控與複製資源資料相關聯的資料放置和相片順序。

此範例會反白顯示應用程式在將2D 資料放入緩衝區之前，直接將2D 資料壓平合併成1D。 在 mipmap 2D 案例中，應用程式可以將每個子資源分開簡維，並快速使用1D 子配置演算法，或使用更複雜的2D 子配置技術來將視訊記憶體的使用率降至最低。 第一個技巧應更頻繁地使用，因為它較為簡單。 當將資料封裝到磁片或網路上時，第二項技術可能會很有用。 無論是哪一種情況，應用程式仍必須呼叫每個子資源的複製 Api。

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

請注意，使用 helper 結構 [**CD3DX12 \_ 堆積 \_ 屬性**](cd3dx12-heap-properties.md) 和 [**CD3DX12 \_ 材質 \_ 複製 \_ 位置**](cd3dx12-texture-copy-location.md)，以及 [**CreateCommittedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource) 和 [**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)的方法。

## <a name="copying"></a>複製

D3D12 方法可讓應用程式取代 D3D11 [**UpdateSubresource**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-updatesubresource)、 [**CopySubresourceRegion**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-copysubresourceregion)和資源初始資料。 資料列主要紋理資料的單一 3D subresource 有可能位於緩衝區資源中。 [**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) 可以從緩衝區將該材質資料複製到具有未知材質配置的材質資源，反之亦然。 應用程式應該使用這種類型的技術來填入經常存取的 GPU 資源，方法是在沒有 CPU 存取的預設堆積中建立經常存取的 GPU 資源時，在上傳堆積中建立大型緩衝區。 這種技術可有效率地支援離散 Gpu 及其大量的 CPU 無法存取的記憶體，而不需要經常因而影響的 UMA 架構。

請注意下列兩個常數：

``` syntax
const UINT D3D12_TEXTURE_DATA_PITCH_ALIGNMENT = 256;
const UINT D3D12_TEXTURE_DATA_PLACEMENT_ALIGNMENT = 512;
```

-   [**D3D12 \_ SUBRESOURCE \_ 足跡**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint)
-   [**D3D12 \_ 放置的 \_ SUBRESOURCE \_ 足跡**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint)
-   [**D3D12 \_ 材質 \_ 複製 \_ 位置**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location)
-   [**D3D12 \_ 材質 \_ 複製 \_ 類型**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_copy_type)
-   [**ID3D12Device::GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints)
-   [**ID3D12GraphicsCommandList::CopyResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
-   [**ID3D12GraphicsCommandList::CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
-   [**ID3D12GraphicsCommandList::CopyBufferRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
-   [**ID3D12GraphicsCommandList::CopyTiles**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles)
-   [**ID3D12CommandQueue::UpdateTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings)

## <a name="mapping-and-unmapping"></a>對應和取消對應

您可以安全地呼叫多個執行緒的對應 [**和取消**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap)[**對應**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map)。 **對應** 的第一個呼叫會配置資源的 CPU 虛擬位址範圍。 取消對應的最後一個呼叫會解除配置 CPU 虛擬位址範圍。 CPU 虛擬位址通常會傳回給應用程式。

只要透過 readback 堆積中的資源，在 CPU 和 GPU 之間傳遞資料，就必須使用對應和取消 [**對應**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) [**，以**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) 支援在上支援 D3D12 的所有系統。 盡可能讓範圍盡可能緊密地保持最高效率， (參考 [**D3D12 \_ 範圍**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range)) 。

偵錯工具的效能不僅受益于所有 [**地圖取消對應**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map)呼叫上的精確使用範圍  /  [](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) ，也可讓應用程式在不再進行 CPU 修改時取消對應資源。

D3D12 不支援使用 [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) (搭配捨棄參數設定) 來重新命名資源的 D3D11 方法。 應用程式必須自行執行資源重新命名。 所有的 **對應** 呼叫都隱含地沒有 \_ 覆寫和多執行緒。 應用程式必須負責確保命令清單中包含的所有相關 GPU 工作都已完成，然後才能存取 CPU 的資料。 D3D12 的 **對應** 呼叫不會隱含地排清任何命令緩衝區，也不會封鎖等候 GPU 完成工作。 因此，在某些情況下 [**，可能甚至會將**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap)對應和取消 **對應** 優化。

## <a name="buffer-alignment"></a>緩衝區對齊

緩衝區對齊限制：

-   線性 subresource 複製必須對齊512個位元組 (資料列間距對齊 D3D12 \_ 材質 \_ 資料 \_ 間距 \_ 對齊位元組) 。
-   常數資料讀取必須是來自堆積開頭的256個位元組倍數 (也就是，只有來自256位元組對齊) 的位址。
-   索引資料讀取必須是索引資料類型大小的倍數 (亦即，僅來自針對資料) 自然對齊的位址。
-   [**ID3D12GraphicsCommandList：:D rawinstanced**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced) 和 [**ID3D12GraphicsCommandList：:D rawindexedinstanced**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawindexedinstanced) 資料必須是來自 (4 的倍數的位移，也就是只有來自以 DWORD 對齊) 的位址。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[在緩衝區內進行子分配](large-buffers.md)
</dt> </dl>

 

 