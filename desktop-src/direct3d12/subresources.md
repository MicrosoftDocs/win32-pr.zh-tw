---
title: '子資源 (Direct3D 12 圖形) '
description: 說明如何將資源分割成子資源，以及如何參考子資源的單一、多重或配量。
ms.assetid: C4F92F8A-DBF0-412B-8707-CC4C1BF2D88F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2fc4478e71bbafb8a21897f838ee8091592024a4e3c761280911e395f8ae491
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117911964"
---
# <a name="subresources-direct3d-12-graphics"></a>子資源 (Direct3D 12 圖形) 

說明如何將資源分割成子資源，以及如何參考子資源的單一、多重或配量。

-   [範例子資源](#example-subresources)
    -   [Subresource 索引](#subresource-indexing)
    -   [Mip 配量](#mip-slice)
    -   [陣列配量](#array-slice)
    -   [平面配量](#plane-slice)
    -   [多個子資源](#multiple-subresources)
-   [Subresource Api](#subresource-apis)
-   [相關主題](#related-topics)

## <a name="example-subresources"></a>範例子資源

如果資源包含緩衝區，則它只會包含一個索引為0的 subresource。 如果資源包含材質 (或紋理陣列) ，則參考子資源會更複雜。

某些 Api 會存取整個資源 (例如 [**ID3D12GraphicsCommandList：： CopyResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource) 方法) ，其他人會存取一部分的資源 (例如 [**ID3D12Resource：： ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) 方法) 。 存取某個資源部分的方法通常會使用 view description (例如 [**D3D12 \_ TEX2D \_ ARRAY \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv) 結構) 指定要存取的子資源。 如需完整清單，請參閱 [Subresource api](#subresource-apis) 一節。

### <a name="subresource-indexing"></a>Subresource 索引

為了編制特定 subresource 的索引，會先編制 mip 層級的索引，因為每個陣列專案都已編制索引。

![subresource 索引](images/subresource-index.png)

### <a name="mip-slice"></a>Mip 配量

Mip 配量包含陣列中每個材質的一個 mipmap 層級，如下圖所示。

![subresource mip 配量](images/subresource-mip-slice.png)

### <a name="array-slice"></a>陣列配量

根據紋理的陣列，每個材質都有 mipmap，陣列配量包含一個材質和其所有 mip 層級，如下圖所示。

![subresource 陣列配量](images/subresource-array-slices.png)

### <a name="plane-slice"></a>平面配量

平面格式通常不會用來儲存 RGBA 資料，但如果 (可能 24bpp RGB 資料) ，則一個平面可以代表紅色影像、一個綠色，以及一個藍色的影像。 不過，一個平面不一定是一種色彩，可以將兩個或更多的色彩組合成一個平面。 通常會使用平面資料來進行子樣本 YCbCr 和 Depth-Stencil 資料。 Depth-Stencil 是唯一支援 mipmap、陣列和多個平面的格式 (通常是深度的平面0和樣板) 的平面1。

針對兩個 Depth-Stencil 映射的陣列編制索引 subresource，每個影像都有三個 mip 層級，如下所示。

![深度樣板索引編制](images/depth-stencil-indexing.png)

子樣本 YCbCr 支援陣列且具有平面，但不支援 mipmap。 YCbCr 影像有兩個平面，一個適用于每個平面的亮度 (Y) ，其中一個適用于人類眼最敏感的亮度，另一個用於色度，也就是一種 (，也就是「Cb」和「Cr」交錯) ，人類眼睛較不敏感 此格式可讓您壓縮色度值，以便在不影響亮度的情況下壓縮影像，而且這是一種常見的影片壓縮格式，但它可用來壓縮靜止影像。 下圖顯示 NV12 格式，請注意色度已壓縮成一季的亮度解析度，這表示每個平面的寬度都相同，而色度平面是亮度平面高度的一半。 平面會以子資源的方式，以與上述 Depth-Stencil 範例相同的方式來編制索引。

![nv12 格式](images/ycbcr.png)

在 Direct3D 11 中存在平面格式，但無法個別定址個別的平面，例如複製或對應作業。 這已在 Direct3D 12 中變更，因此每個平面都會收到自己的 subresource 識別碼。 比較下列兩個方法來計算 subresource 識別碼。

Direct3D 11

``` syntax
inline UINT D3D11CalcSubresource( UINT MipSlice, UINT ArraySlice, UINT MipLevels )
{
    return MipSlice + (ArraySlice * MipLevels); 
}
```

Direct3D 12

``` syntax
inline UINT D3D12CalcSubresource( UINT MipSlice, UINT ArraySlice, UINT PlaneSlice, UINT MipLevels, UINT ArraySize )
{ 
    return MipSlice + (ArraySlice * MipLevels) + (PlaneSlice * MipLevels * ArraySize); 
}
```

大部分的硬體都會假設平面 N 的記憶體一律會在平面 N-1 之後立即配置。

使用子資源的替代方案是，應用程式可以為每個平面配置完全不同的資源。 在此情況下，應用程式瞭解資料是平面的，並使用多個資源來代表它。

### <a name="multiple-subresources"></a>多個子資源

著色器資源檢視可以選取子資源的任何矩形區域，並使用上述其中一個配量，併合理使用 view (結構中的欄位，例如 [**D3D12 \_ TEX2D \_ ARRAY \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)) ，如影像中所示。

![多重 subresource 選取專案](images/subresource-multiple.png)

轉譯目標視圖只能使用單一 subresource 或 mip 配量，且不能包含來自一個以上 mip 配量的子資源。 也就是說，轉譯目標視圖中的每個材質都必須是相同的大小。 著色器資源檢視可以選取子資源的任何矩形區域，如下圖所示。

## <a name="subresource-apis"></a>Subresource Api

下列 Api 參考和使用子資源：

枚舉：

-   [**D3D12 \_ 材質 \_ 複製 \_ 類型**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_copy_type)

下列結構包含 *PlaneSlice* 索引，最多包含 *MipSlice* 索引。

-   [**D3D12 \_ TEX2D \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_rtv)
-   [**D3D12 \_ TEX2D \_ 陣列 \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_rtv)
-   [**D3D12 \_ TEX2D \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_srv)
-   [**D3D12 \_ TEX2D \_ 陣列 \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)
-   [**D3D12 \_ TEX2D \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_uav)
-   [**D3D12 \_ TEX2D \_ 陣列 \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_uav)

下列結構包含 *ArraySlice* 索引，最多包含 *MipSlice* 索引。

-   [**D3D12 \_ TEX1D \_ 陣列 \_ DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_dsv)
-   [**D3D12 \_ TEX2D \_ 陣列 \_ DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_dsv)
-   [**D3D12 \_ TEX2DMS \_ 陣列 \_ DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_dsv)
-   [**D3D12 \_ TEX1D \_ 陣列 \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_rtv)
-   [**D3D12 \_ TEX2D \_ 陣列 \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_rtv)
-   [**D3D12 \_ TEX2DMS \_ 陣列 \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_rtv)
-   [**D3D12 \_ TEX1D \_ 陣列 \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_srv)
-   [**D3D12 \_ TEX2D \_ 陣列 \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)
-   [**D3D12 \_ TEX2DMS \_ 陣列 \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_srv)
-   [**D3D12 \_ TEX1D \_ 陣列 \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_uav)
-   [**D3D12 \_ TEX2D \_ 陣列 \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_uav)

下列結構包含 *MipSlice* 索引，但不包含 *ArraySlice* 和 *PlaneSlice* 索引。

-   [**D3D12 \_ TEX1D \_ DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_dsv)
-   [**D3D12 \_ TEX2D \_ DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_dsv)
-   [**D3D12 \_ TEX1D \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_rtv)
-   [**D3D12 \_ TEX3D \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_rtv)
-   [**D3D12 \_ TEX1D \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_uav)
-   [**D3D12 \_ TEX3D \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_uav)

下列結構也會參考子資源：

-   [**D3D12 \_捨棄 \_ 區域**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_discard_region) ：用於準備捨棄資源的結構。
-   [**D3D12 \_放置 \_ 的 \_ SUBRESOURCE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint) 使用量：將位移新增至基本使用量的資源。
-   [**D3D12 \_資源 \_ 轉換 \_ 屏障**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier) ：描述不同使用方式 (著色器資源、轉譯目標等 ) 之間的子資源轉換。
-   [**D3D12 \_SUBRESOURCE \_ 資料**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) ： SUBRESOURCE 資料包含資料本身，以及資料列和配量的間距。
-   [**D3D12 \_SUBRESOURCE \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) 使用量：使用量包括 SUBRESOURCE 的格式、寬度、高度、深度和資料列的間距。
-   [**D3D12 \_SUBRESOURCE \_ 資訊**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_info) ：包含 SUBRESOURCE 的位移、資料列間距和深度音調。
-   [**D3D12 \_SUBRESOURCE \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) 圖格：描述已並排的 SUBRESOURCE 音量 (請參閱) 的 [磁片區磚資源](volume-tiled-resources.md) 。
-   [**D3D12 \_材質 \_ 複製 \_ 位置**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) ：描述材質的一部分，以供複製之用。
-   [**D3D12 \_並排顯示的 \_ 資源 \_ 座標**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) ：描述已並排資源的座標。

方法:

-   [**ID3D12Device：： GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints) ：取得資源的資訊，以啟用複製。
-   [**ID3D12Device：： GetResourceTiling**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourcetiling) ：取得如何將磚的資源分成磚的相關資訊。
-   [**ID3D12GraphicsCommandList：： ResolveSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource) ：將多取樣的 subresource 複製到非多重取樣的 subresource 中。
-   [**ID3D12Resource：： Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) ：傳回資源中指定資料的指標，並拒絕 SUBRESOURCE 的 GPU 存取。
-   [**ID3D12Resource：： ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) ：從 subresource 或 subresource 的矩形區域複製資料。
-   [**ID3D12Resource：：**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) 取消對應： unmaps 指定的記憶體範圍，並使資源的指標失效。 掉 GPU 對 subresource 的存取。
-   [**ID3D12Resource：： WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) ：將資料複製到 subresource 或 subresource 的矩形區域。

紋理必須處於 [**D3D12 \_ 資源狀態的 \_ \_ 一般**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) 狀態，才能透過 [**WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) 和 [**ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) 進行 CPU 存取，但緩衝區則否。 資源的 CPU 存取通常是透過對應取消 [**對應**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map)來完成 / [****](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[資源系結](resource-binding.md)
</dt> </dl>

 

 




