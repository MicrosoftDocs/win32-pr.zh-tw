---
title: " (Direct3D 11 圖形) 的磁片區磚資源"
description: 瞭解如何使用磁片區 (3D) 材質作為並排顯示的資源。 請注意，磚解析度是三維。
ms.assetid: B6BF22A2-EDA3-4765-B545-BF825043D4C4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bf9b3ed8b1db89d9718fa904eefd23ce2e871db
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335432"
---
# <a name="volume-tiled-resources"></a>磁片區磚資源

磁片區 (3D) 材質可以用來做為並排的資源，請注意磚解析度是三維。

-   [概觀](#overview)
-   [D3D 11.3 磚資源 Api](#d3d113-tiled-resource-apis)
-   [相關主題](#related-topics)

## <a name="overview"></a>概觀

並排顯示的資源會將 D3D 資源物件與其支援記憶體分離， (資源在過去具有與其支援記憶體) 的1:1 關聯性。 這可提供各種有趣的案例，例如在材質資料中串流處理，以及重複使用或減少記憶體使用量

D3D 11.2 支援2D 紋理磚資源。 D3D12 和 D3D 11.3 新增對3D 並排紋理的支援。

磚中所使用的一般資源維度是2D 紋理的 4 x 4 磚，以及3D 紋理的 4 x 4 x 4 個圖格。



| 位/圖元 (1 取樣/圖元)                             | 磚尺寸 (圖元，w x h x d)                                     |
|-----------------------------|-------------------------------------|
| 8                           | 64 x 32 x 32                            |
| 16                          | 32 x 32 x 32                            |
| 32                          | 32 x 32 x 16                            |
| 64                          | 32 x 16 x 16                            |
| 128                         | 16 x 16 x 16                            |
| BC 1、4                      | 128 x 64 x 16                           |
| BC 2、3、5、6、7                | 64 x 64 x 16                            |



 

請注意，磚式資源不支援下列格式：96bpp 格式、影片格式、R1 \_ UNORM、R8G8 \_ B8G8 \_ UNORM、R8R8 \_ G8B8 \_ UNORM。

在下列圖表中，暗灰色表示 Null 磚。

-   [紋理3D 將資源預設對應 (最詳細的 mip) ](#texture-3d-tiled-resource-default-mapping-most-detailed-mip)
-   [紋理3D 並排顯示的資源預設對應 (第二個最詳細的 mip) ](#texture-3d-tiled-resource-default-mapping-second-most-detailed-mip)
-   [紋理3D 並排顯示資源 (最詳細的 mip) ](#texture-3d-tiled-resource-most-detailed-mip)
-   [紋理3D 並排顯示資源 (第二個最詳細的 mip) ](#texture-3d-tiled-resource-second-most-detailed-mip)
-   [紋理3D 磚資源 (單一磚) ](#texture-3d-tiled-resource-single-tile)
-   [紋理3D 並排顯示資源 (統一方塊) ](#texture-3d-tiled-resource-uniform-box)

### <a name="texture-3d-tiled-resource-default-mapping-most-detailed-mip"></a>紋理3D 將資源預設對應 (最詳細的 mip) 

![最詳細 mip 的預設對應](images/vtr-tex3d-default-1.png)

### <a name="texture-3d-tiled-resource-default-mapping-second-most-detailed-mip"></a>紋理3D 並排顯示的資源預設對應 (第二個最詳細的 mip) 

![第二個最詳細 mip 的預設對應](images/vtr-tex3d-default-2.png)

### <a name="texture-3d-tiled-resource-most-detailed-mip"></a>紋理3D 並排顯示資源 (最詳細的 mip) 

下列程式碼會在最詳細的 mip 上設定3D 磚資源。

``` syntax
D3D11_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 1;
trCoord.Y = 0;
trCoord.Z = 0;
trCoord.Subresource = 0;

D3D11_TILE_REGION_SIZE trSize;
trSize.bUseBox = false;
trSize.NumTiles = 63;
```

![3d 磚資源的最詳細對應](images/vtr-tex3d-default-1b.png)

### <a name="texture-3d-tiled-resource-second-most-detailed-mip"></a>紋理3D 並排顯示資源 (第二個最詳細的 mip) 

下列程式碼會設定3D 並排顯示的資源，以及第二個最詳細的 mip：

``` syntax
D3D11_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 1;
trCoord.Y = 0;
trCoord.Z = 0;
trCoord.Subresource = 1;

D3D11_TILE_REGION_SIZE trSize;
trSize.bUseBox = false;
trSize.NumTiles = 6;
```

![3d 並排顯示資源的第二個最詳細對應](images/vtr-tex3d-default-2b.png)

### <a name="texture-3d-tiled-resource-single-tile"></a>紋理3D 磚資源 (單一磚) 

下列程式碼會設定單一磚資源：

``` syntax
D3D11_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 1;
trCoord.Y = 1;
trCoord.Z = 1;
trCoord.Subresource = 0;

D3D11_TILE_REGION_SIZE trSize;
trSize.bUseBox = true;
trSize.NumTiles = 27;
trSize.Width = 3;
trSize.Height = 3;
trSize.Depth = 3;
```

![單一磚](images/vtr-tex3d-single.png)

### <a name="texture-3d-tiled-resource-uniform-box"></a>紋理3D 並排顯示資源 (統一方塊) 

下列程式碼會設定並排顯示資源 (記下語句的統一方塊 `trSize.bUseBox = true;) :`

``` syntax
D3D11_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 0;
trCoord.Y = 1;
trCoord.Z = 0;
trCoord.Subresource = 0;

D3D11_TILE_REGION_SIZE trSize;
trSize.bUseBox = true;
trSize.NumTiles = 27;
trSize.Width = 3;
trSize.Height = 3;
trSize.Depth = 3;
```

![統一箱](images/vtr-tex3d-uniform.png)

## <a name="d3d113-tiled-resource-apis"></a>D3D 11.3 磚資源 Api

相同的 API 呼叫同時用於2D 和3D 並排顯示的資源：

列舉

-   [**D3D11 \_並排顯示的 \_ 資源 \_ 層**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) ：決定並排資源支援的層級。
-   [**D3D11 \_FORMAT \_ SUPPORT2**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) ：用來測試已並排的資源支援。
-   [**D3D11 \_檢查多取樣 \_ \_ 品質 \_ 層級 \_ 旗**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_check_multisample_quality_levels_flag) 標：判斷多取樣資源中的磚資源支援。
-   [**D3D11 \_磚 \_ 複製 \_ 旗標**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_copy_flag) ：保留在 swizzled 並排顯示的資源和線性緩衝區進行複製的旗標。

結構

-   [**D3D11 \_並排顯示的 \_ 資源 \_ 座標**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tiled_resource_coordinate) ：保留 x、y 和 z 座標，以及 subresource 參考。 請注意，有一個 helper 類別： CD3D11 並排的 \_ \_ 資源 \_ 座標。
-   [**D3D11 \_磚 \_ 區域 \_ 大小**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_region_size) ：指定並排顯示區域的大小和圖格數目。
-   [**D3D11 \_磚 \_ 圖形**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_shape) ：圖格圖形為材質中的寬度、高度和深度。
-   [**D3D11 \_FEATURE \_ DATA \_ D3D11 \_ OPTIONS1**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1)：保留支援的磚資源層級。

方法

-   [**ID3D11Device：： CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) ：用來判斷目前硬體所支援的功能和層級。
-   [**ID3D11DeviceCoNtext2：： CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) ：會從緩衝區將圖格複製到磚資源，反之亦然。
-   [**ID3D11DeviceCoNtext2：： UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) ：將並排顯示的資源中的磚位置對應更新為磚集區中的記憶體位置。
-   [**ID3D11DeviceCoNtext2：： CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) ：將對應從來源磚的資源複製到已並排顯示的資源。
-   [**ID3D11DeviceCoNtext2：： GetResourceTiling**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling) ：取得如何將磚的資源分成磚的相關資訊。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 11.3 功能](direct3d-11-3-features.md)
</dt> </dl>

 

 




