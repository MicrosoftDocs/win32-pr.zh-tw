---
title: " (Direct3D 12) 的磁片區磚資源"
description: 磁片區 (3D) 材質可以用來做為並排的資源，請注意磚解析度是三維。
ms.assetid: F670D15D-BC0F-4F90-99C1-A35192FE8980
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b8d6e9b4d7ae9ad4b93bae5cf29749c293bf7f55ea7fa35a1e1ca71040218e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123498"
---
# <a name="volume-tiled-resources-direct3d-12"></a> (Direct3D 12) 的磁片區磚資源

磁片區 (3D) 材質可以用來做為並排的資源，請注意磚解析度是三維。

## <a name="overview"></a>概觀

並排顯示的資源會將 Direct3D 資源物件與其支援記憶體分離， (資源在過去具有與其支援記憶體) 的1:1 關聯性。 這可提供各種有趣的案例，例如在材質資料中串流處理，以及重複使用或減少記憶體使用量。

Direct3D 11.2 支援2D 材質並排顯示的資源。 適用于 Direct3D 12 和 Direct3D 11.3 的選擇性支援3D 並排顯示的材質 (請參閱 [**D3D12_TILED_RESOURCES_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier)) 。

磚中所使用的一般資源維度是2D 紋理的 4 x 4 磚，以及3D 紋理的 4 x 4 x 4 個圖格。

| 位/圖元 (1 取樣/圖元)  | 磚尺寸 (圖元，w x h x d)  |
|-----------------------------|-------------------------------------|
| 8                           | 64 x 32 x 32                            |
| 16                          | 32 x 32 x 32                            |
| 32                          | 32 x 32 x 16                            |
| 64                          | 32 x 16 x 16                            |
| 128                         | 16 x 16 x 16                            |
| BC 1、4                      | 128 x 64 x 16                           |
| BC 2、3、5、6、7                | 64 x 64 x 16                            |

請注意，磚資源不支援下列格式：96bpp 格式、影片格式、 **R1_UNORM**、 **R8G8_B8G8_UNORM**、 **R8R8_G8B8_UNORM**。

在下圖中，暗灰色表示 Null 磚。

* [紋理3D 將資源預設對應 (最詳細的 mip) ](#texture-3d-tiled-resource-default-mapping-most-detailed-mip)
* [紋理3D 並排顯示的資源預設對應 (第二個最詳細的 mip) ](#texture-3d-tiled-resource-default-mapping-second-most-detailed-mip)
* [紋理3D 並排顯示資源 (最詳細的 mip) ](#texture-3d-tiled-resource-most-detailed-mip)
* [紋理3D 並排顯示資源 (第二個最詳細的 mip) ](#texture-3d-tiled-resource-second-most-detailed-mip)
* [紋理3D 磚資源 (單一磚) ](#texture-3d-tiled-resource-single-tile)
* [紋理3D 並排顯示資源 (統一方塊) ](#texture-3d-tiled-resource-uniform-box)

### <a name="texture-3d-tiled-resource-default-mapping-most-detailed-mip"></a>紋理3D 並排顯示資源預設對應 (最詳細的 mip) 

![並排顯示的3d 資源預設對應](images/vtr-tex3d-default-1.png)

### <a name="texture-3d-tiled-resource-default-mapping-second-most-detailed-mip"></a>紋理3D 並排顯示資源預設對應 (第二個最詳細的 mip) 

![顯示第二個最詳細的 mip](images/vtr-tex3d-default-2.png)

### <a name="texture-3d-tiled-resource-most-detailed-mip"></a>紋理3D 磚資源 (最詳細的 mip) 

下列程式碼會在最詳細的 mip 上設定3D 磚資源。

```cpp
D3D12_TILED_RESOURCE_COORDINATE trCoord{};
trCoord.X = 1;
trCoord.Y = 0;
trCoord.Z = 0;
trCoord.Subresource = 0;

D3D12_TILE_REGION_SIZE trSize{};
trSize.bUseBox = false;
trSize.NumTiles = 63;
```

![三維材質的最詳細 mip](images/vtr-tex3d-default-1b.png)

### <a name="texture-3d-tiled-resource-second-most-detailed-mip"></a>紋理3D 並排顯示資源 (第二個-最詳細的 mip) 

下列程式碼會設定3D 並排顯示的資源，以及第二個最詳細的 mip。

```cpp
D3D12_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 1;
trCoord.Y = 0;
trCoord.Z = 0;
trCoord.Subresource = 1;

D3D12_TILE_REGION_SIZE trSize;
trSize.bUseBox = false;
trSize.NumTiles = 6;
```

![三維材質的第二個最詳細 mip](images/vtr-tex3d-default-2b.png)

### <a name="texture-3d-tiled-resource-single-tile"></a>紋理3D 磚資源 (單一磚) 

下列程式碼會設定單一圖格資源。

```cpp
D3D12_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 1;
trCoord.Y = 1;
trCoord.Z = 1;
trCoord.Subresource = 0;

D3D12_TILE_REGION_SIZE trSize;
trSize.bUseBox = true;
trSize.NumTiles = 27;
trSize.Width = 3;
trSize.Height = 3;
trSize.Depth = 3;
```

![單一磚的立體資源](images/vtr-tex3d-single.png)

### <a name="texture-3d-tiled-resource-uniform-box"></a>紋理3D 並排顯示資源 (統一方塊) 

下列程式碼會設定並排顯示資源 (記下語句的統一方塊 `trSize.bUseBox = true;) :`

```cpp
D3D12_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 0;
trCoord.Y = 1;
trCoord.Z = 0;
trCoord.Subresource = 0;

D3D12_TILE_REGION_SIZE trSize;
trSize.bUseBox = true;
trSize.NumTiles = 27;
trSize.Width = 3;
trSize.Height = 3;
trSize.Depth = 3;
```

![統一箱](images/vtr-tex3d-uniform.png)

## <a name="tiled-resource-apis"></a>磚資源 Api

相同的 API 呼叫會用於2D 和3D 並排顯示的資源。

列舉

* [**D3D12_TILED_RESOURCES_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier) ：決定並排資源支援的層級。
* [**D3D12_FORMAT_SUPPORT2**](/windows/win32/api/d3d12/ne-d3d12-d3d12_format_support2) ：用來測試已平鋪的資源支援。
* [**D3D12_MULTISAMPLE_QUALITY_LEVEL_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_multisample_quality_level_flags) ：判斷多取樣資源中的磚資源支援。
* [**D3D12_TILE_COPY_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tile_copy_flags) ：保留旗標，以便在 swizzled 並排顯示的資源和線性緩衝區進行複製。

結構

* [**D3D12_TILED_RESOURCE_COORDINATE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) ：保留 x、y 和 z 座標，以及 subresource 參考。 請注意，有一個 helper 結構： [**CD3DX12_TILED_RESOURCE_COORDINATE**](cd3dx12-tiled-resource-coordinate.md)。
* [**D3D12_TILE_REGION_SIZE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tile_region_size) ：指定並排顯示區域的大小和圖格數目。
* [**D3D12_TILE_SHAPE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tile_shape) ：磚圖形為材質中的寬度、高度和深度。
* [**D3D12_FEATURE_DATA_D3D12_OPTIONS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) ：保留支援的磚資源層級和布林值 *VolumeTiledResourcesSupported*，指出是否支援磁片區磚資源。

方法

* [**ID3D12Device：： CheckFeatureSupport**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) ：用來判斷目前硬體所支援的功能和層級。
* [**ID3D12GraphicsCommandList：： CopyTiles**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles) ：會從緩衝區將圖格複製到磚資源，反之亦然。
* [**ID3D12CommandQueue：： UpdateTileMappings**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings) ：將並排顯示的資源中的磚位置對應更新為資源堆積中的記憶體位置。
* [**ID3D12CommandQueue：： CopyTileMappings**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-copytilemappings) ：將對應從來源磚的資源複製到已並排顯示的資源。
* [**ID3D12Device：： GetResourceTiling**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getresourcetiling) ：取得如何將磚的資源分成磚的相關資訊。

## <a name="related-topics"></a>相關主題

* [資源系結](resource-binding.md)
