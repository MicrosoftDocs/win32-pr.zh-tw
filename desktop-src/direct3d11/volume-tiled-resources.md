---
title: " (Direct3D 11 圖形) 的磁片區磚資源"
description: 磁片區 (3D) 材質可以用來做為並排的資源，請注意磚解析度是三維。
ms.assetid: B6BF22A2-EDA3-4765-B545-BF825043D4C4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abb8b35e522ef3298abad1322d6fb7a2fe65bfcf
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/12/2019
ms.locfileid: "103679055"
---
# <a name="volume-tiled-resources"></a><span data-ttu-id="474d6-103">磁片區磚資源</span><span class="sxs-lookup"><span data-stu-id="474d6-103">Volume Tiled Resources</span></span>

<span data-ttu-id="474d6-104">磁片區 (3D) 材質可以用來做為並排的資源，請注意磚解析度是三維。</span><span class="sxs-lookup"><span data-stu-id="474d6-104">Volume (3D) textures can be used as tiled resources, noting that tile resolution is three-dimensional.</span></span>

-   [<span data-ttu-id="474d6-105">概觀</span><span class="sxs-lookup"><span data-stu-id="474d6-105">Overview</span></span>](#overview)
-   [<span data-ttu-id="474d6-106">D3D 11.3 磚資源 Api</span><span class="sxs-lookup"><span data-stu-id="474d6-106">D3D11.3 Tiled Resource APIs</span></span>](#d3d113-tiled-resource-apis)
-   [<span data-ttu-id="474d6-107">相關主題</span><span class="sxs-lookup"><span data-stu-id="474d6-107">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="474d6-108">概觀</span><span class="sxs-lookup"><span data-stu-id="474d6-108">Overview</span></span>

<span data-ttu-id="474d6-109">並排顯示的資源會將 D3D 資源物件與其支援記憶體分離， (資源在過去具有與其支援記憶體) 的1:1 關聯性。</span><span class="sxs-lookup"><span data-stu-id="474d6-109">Tiled resources decouple a D3D Resource object from its backing memory (resources in the past had a 1:1 relationship with their backing memory).</span></span> <span data-ttu-id="474d6-110">這可提供各種有趣的案例，例如在材質資料中串流處理，以及重複使用或減少記憶體使用量</span><span class="sxs-lookup"><span data-stu-id="474d6-110">This allows for a variety of interesting scenarios such as streaming in texture data and reusing or reducing memory usage</span></span>

<span data-ttu-id="474d6-111">D3D 11.2 支援2D 紋理磚資源。</span><span class="sxs-lookup"><span data-stu-id="474d6-111">2D texture tiled resources are supported in D3D11.2.</span></span> <span data-ttu-id="474d6-112">D3D12 和 D3D 11.3 新增對3D 並排紋理的支援。</span><span class="sxs-lookup"><span data-stu-id="474d6-112">D3D12 and D3D11.3 add support for 3D tiled textures.</span></span>

<span data-ttu-id="474d6-113">磚中所使用的一般資源維度是2D 紋理的 4 x 4 磚，以及3D 紋理的 4 x 4 x 4 個圖格。</span><span class="sxs-lookup"><span data-stu-id="474d6-113">The typical resource dimensions used in tiling are 4 x 4 tiles for 2D textures, and 4 x 4 x 4 tiles for 3D textures.</span></span>



|                             |                                     |
|-----------------------------|-------------------------------------|
| <span data-ttu-id="474d6-114">位/圖元 (1 取樣/圖元) </span><span class="sxs-lookup"><span data-stu-id="474d6-114">Bits/pixel (1 sample/pixel)</span></span> | <span data-ttu-id="474d6-115">磚尺寸 (圖元，w x h x d) </span><span class="sxs-lookup"><span data-stu-id="474d6-115">Tile dimensions (pixels, w x h x d)</span></span> |
| <span data-ttu-id="474d6-116">8</span><span class="sxs-lookup"><span data-stu-id="474d6-116">8</span></span>                           | <span data-ttu-id="474d6-117">64 x 32 x 32</span><span class="sxs-lookup"><span data-stu-id="474d6-117">64x32x32</span></span>                            |
| <span data-ttu-id="474d6-118">16</span><span class="sxs-lookup"><span data-stu-id="474d6-118">16</span></span>                          | <span data-ttu-id="474d6-119">32 x 32 x 32</span><span class="sxs-lookup"><span data-stu-id="474d6-119">32x32x32</span></span>                            |
| <span data-ttu-id="474d6-120">32</span><span class="sxs-lookup"><span data-stu-id="474d6-120">32</span></span>                          | <span data-ttu-id="474d6-121">32 x 32 x 16</span><span class="sxs-lookup"><span data-stu-id="474d6-121">32x32x16</span></span>                            |
| <span data-ttu-id="474d6-122">64</span><span class="sxs-lookup"><span data-stu-id="474d6-122">64</span></span>                          | <span data-ttu-id="474d6-123">32 x 16 x 16</span><span class="sxs-lookup"><span data-stu-id="474d6-123">32x16x16</span></span>                            |
| <span data-ttu-id="474d6-124">128</span><span class="sxs-lookup"><span data-stu-id="474d6-124">128</span></span>                         | <span data-ttu-id="474d6-125">16 x 16 x 16</span><span class="sxs-lookup"><span data-stu-id="474d6-125">16x16x16</span></span>                            |
| <span data-ttu-id="474d6-126">BC 1、4</span><span class="sxs-lookup"><span data-stu-id="474d6-126">BC 1,4</span></span>                      | <span data-ttu-id="474d6-127">128 x 64 x 16</span><span class="sxs-lookup"><span data-stu-id="474d6-127">128x64x16</span></span>                           |
| <span data-ttu-id="474d6-128">BC 2、3、5、6、7</span><span class="sxs-lookup"><span data-stu-id="474d6-128">BC 2,3,5,6,7</span></span>                | <span data-ttu-id="474d6-129">64 x 64 x 16</span><span class="sxs-lookup"><span data-stu-id="474d6-129">64x64x16</span></span>                            |



 

<span data-ttu-id="474d6-130">請注意，磚式資源不支援下列格式：96bpp 格式、影片格式、R1 \_ UNORM、R8G8 \_ B8G8 \_ UNORM、R8R8 \_ G8B8 \_ UNORM。</span><span class="sxs-lookup"><span data-stu-id="474d6-130">Note the following formats are not supported with tiled resources: 96bpp formats, video formats, R1\_UNORM, R8G8\_B8G8\_UNORM, R8R8\_G8B8\_UNORM.</span></span>

<span data-ttu-id="474d6-131">在下列圖表中，暗灰色表示 Null 磚。</span><span class="sxs-lookup"><span data-stu-id="474d6-131">In the diagrams below dark gray represents NULL tiles.</span></span>

-   [<span data-ttu-id="474d6-132">紋理3D 將資源預設對應 (最詳細的 mip) </span><span class="sxs-lookup"><span data-stu-id="474d6-132">Texture 3D Tiled Resource default mapping (most detailed mip)</span></span>](#texture-3d-tiled-resource-default-mapping-most-detailed-mip)
-   [<span data-ttu-id="474d6-133">紋理3D 並排顯示的資源預設對應 (第二個最詳細的 mip) </span><span class="sxs-lookup"><span data-stu-id="474d6-133">Texture 3D Tiled Resource default mapping (second most detailed mip)</span></span>](#texture-3d-tiled-resource-default-mapping-second-most-detailed-mip)
-   [<span data-ttu-id="474d6-134">紋理3D 並排顯示資源 (最詳細的 mip) </span><span class="sxs-lookup"><span data-stu-id="474d6-134">Texture 3D Tiled Resource (most detailed mip)</span></span>](#texture-3d-tiled-resource-most-detailed-mip)
-   [<span data-ttu-id="474d6-135">紋理3D 並排顯示資源 (第二個最詳細的 mip) </span><span class="sxs-lookup"><span data-stu-id="474d6-135">Texture 3D Tiled Resource (second most detailed mip)</span></span>](#texture-3d-tiled-resource-second-most-detailed-mip)
-   [<span data-ttu-id="474d6-136">紋理3D 磚資源 (單一磚) </span><span class="sxs-lookup"><span data-stu-id="474d6-136">Texture 3D Tiled Resource (Single Tile)</span></span>](#texture-3d-tiled-resource-single-tile)
-   [<span data-ttu-id="474d6-137">紋理3D 並排顯示資源 (統一方塊) </span><span class="sxs-lookup"><span data-stu-id="474d6-137">Texture 3D Tiled Resource (Uniform Box)</span></span>](#texture-3d-tiled-resource-uniform-box)

### <a name="texture-3d-tiled-resource-default-mapping-most-detailed-mip"></a><span data-ttu-id="474d6-138">紋理3D 將資源預設對應 (最詳細的 mip) </span><span class="sxs-lookup"><span data-stu-id="474d6-138">Texture 3D Tiled Resource default mapping (most detailed mip)</span></span>

![最詳細 mip 的預設對應](images/vtr-tex3d-default-1.png)

### <a name="texture-3d-tiled-resource-default-mapping-second-most-detailed-mip"></a><span data-ttu-id="474d6-140">紋理3D 並排顯示的資源預設對應 (第二個最詳細的 mip) </span><span class="sxs-lookup"><span data-stu-id="474d6-140">Texture 3D Tiled Resource default mapping (second most detailed mip)</span></span>

![第二個最詳細 mip 的預設對應](images/vtr-tex3d-default-2.png)

### <a name="texture-3d-tiled-resource-most-detailed-mip"></a><span data-ttu-id="474d6-142">紋理3D 並排顯示資源 (最詳細的 mip) </span><span class="sxs-lookup"><span data-stu-id="474d6-142">Texture 3D Tiled Resource (most detailed mip)</span></span>

<span data-ttu-id="474d6-143">下列程式碼會在最詳細的 mip 上設定3D 磚資源。</span><span class="sxs-lookup"><span data-stu-id="474d6-143">The following code sets up a 3D tiled resource at the most detailed mip.</span></span>

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

### <a name="texture-3d-tiled-resource-second-most-detailed-mip"></a><span data-ttu-id="474d6-145">紋理3D 並排顯示資源 (第二個最詳細的 mip) </span><span class="sxs-lookup"><span data-stu-id="474d6-145">Texture 3D Tiled Resource (second most detailed mip)</span></span>

<span data-ttu-id="474d6-146">下列程式碼會設定3D 並排顯示的資源，以及第二個最詳細的 mip：</span><span class="sxs-lookup"><span data-stu-id="474d6-146">The following code sets up a 3D tiled resource, and the second most detailed mip:</span></span>

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

### <a name="texture-3d-tiled-resource-single-tile"></a><span data-ttu-id="474d6-148">紋理3D 磚資源 (單一磚) </span><span class="sxs-lookup"><span data-stu-id="474d6-148">Texture 3D Tiled Resource (Single Tile)</span></span>

<span data-ttu-id="474d6-149">下列程式碼會設定單一磚資源：</span><span class="sxs-lookup"><span data-stu-id="474d6-149">The following code sets up a Single Tile resource:</span></span>

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

### <a name="texture-3d-tiled-resource-uniform-box"></a><span data-ttu-id="474d6-151">紋理3D 並排顯示資源 (統一方塊) </span><span class="sxs-lookup"><span data-stu-id="474d6-151">Texture 3D Tiled Resource (Uniform Box)</span></span>

<span data-ttu-id="474d6-152">下列程式碼會設定並排顯示資源 (記下語句的統一方塊 `trSize.bUseBox = true;) :`</span><span class="sxs-lookup"><span data-stu-id="474d6-152">The following code sets up a Uniform Box tiled resource (note the statement `trSize.bUseBox = true;) :`</span></span>

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

## <a name="d3d113-tiled-resource-apis"></a><span data-ttu-id="474d6-154">D3D 11.3 磚資源 Api</span><span class="sxs-lookup"><span data-stu-id="474d6-154">D3D11.3 Tiled Resource APIs</span></span>

<span data-ttu-id="474d6-155">相同的 API 呼叫同時用於2D 和3D 並排顯示的資源：</span><span class="sxs-lookup"><span data-stu-id="474d6-155">The same API calls are used for both 2D and 3D tiled resources:</span></span>

<span data-ttu-id="474d6-156">列舉</span><span class="sxs-lookup"><span data-stu-id="474d6-156">Enums</span></span>

-   <span data-ttu-id="474d6-157">[**D3D11 \_並排顯示的 \_ 資源 \_ 層**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) ：決定並排資源支援的層級。</span><span class="sxs-lookup"><span data-stu-id="474d6-157">[**D3D11\_TILED\_RESOURCES\_TIER**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) : determines the level of tiled resource support.</span></span>
-   <span data-ttu-id="474d6-158">[**D3D11 \_FORMAT \_ SUPPORT2**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) ：用來測試已並排的資源支援。</span><span class="sxs-lookup"><span data-stu-id="474d6-158">[**D3D11\_FORMAT\_SUPPORT2**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) : used to test for tiled resource support.</span></span>
-   <span data-ttu-id="474d6-159">[**D3D11 \_檢查多取樣 \_ \_ 品質 \_ 層級 \_ 旗**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_check_multisample_quality_levels_flag) 標：判斷多取樣資源中的磚資源支援。</span><span class="sxs-lookup"><span data-stu-id="474d6-159">[**D3D11\_CHECK\_MULTISAMPLE\_QUALITY\_LEVELS\_FLAG**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_check_multisample_quality_levels_flag) : determines tiled resource support in a multi-sampling resource.</span></span>
-   <span data-ttu-id="474d6-160">[**D3D11 \_磚 \_ 複製 \_ 旗標**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_copy_flag) ：保留在 swizzled 並排顯示的資源和線性緩衝區進行複製的旗標。</span><span class="sxs-lookup"><span data-stu-id="474d6-160">[**D3D11\_TILE\_COPY\_FLAGS**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_copy_flag) : holds flags for copying to and from swizzled tiled resources and linear buffers.</span></span>

<span data-ttu-id="474d6-161">結構</span><span class="sxs-lookup"><span data-stu-id="474d6-161">Structures</span></span>

-   <span data-ttu-id="474d6-162">[**D3D11 \_並排顯示的 \_ 資源 \_ 座標**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tiled_resource_coordinate) ：保留 x、y 和 z 座標，以及 subresource 參考。</span><span class="sxs-lookup"><span data-stu-id="474d6-162">[**D3D11\_TILED\_RESOURCE\_COORDINATE**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tiled_resource_coordinate) : holds the x, y, and z co-ordinate, and subresource reference.</span></span> <span data-ttu-id="474d6-163">請注意，有一個 helper 類別： CD3D11 並排的 \_ \_ 資源 \_ 座標。</span><span class="sxs-lookup"><span data-stu-id="474d6-163">Note there is a helper class: CD3D11\_TILED\_RESOURCE\_COORDINATE.</span></span>
-   <span data-ttu-id="474d6-164">[**D3D11 \_磚 \_ 區域 \_ 大小**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_region_size) ：指定並排顯示區域的大小和圖格數目。</span><span class="sxs-lookup"><span data-stu-id="474d6-164">[**D3D11\_TILE\_REGION\_SIZE**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_region_size) : specifies the size, and number of tiles, of the tiled region.</span></span>
-   <span data-ttu-id="474d6-165">[**D3D11 \_磚 \_ 圖形**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_shape) ：圖格圖形為材質中的寬度、高度和深度。</span><span class="sxs-lookup"><span data-stu-id="474d6-165">[**D3D11\_TILE\_SHAPE**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_shape) : the tile shape as a width, height and depth in texels.</span></span>
-   <span data-ttu-id="474d6-166">[**D3D11 \_FEATURE \_ DATA \_ D3D11 \_ OPTIONS1**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1)：保留支援的磚資源層級。</span><span class="sxs-lookup"><span data-stu-id="474d6-166">[**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS1**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1): holds the supported tile resource tier level.</span></span>

<span data-ttu-id="474d6-167">方法</span><span class="sxs-lookup"><span data-stu-id="474d6-167">Methods</span></span>

-   <span data-ttu-id="474d6-168">[**ID3D11Device：： CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) ：用來判斷目前硬體所支援的功能和層級。</span><span class="sxs-lookup"><span data-stu-id="474d6-168">[**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) : used to determine what features, and at what tier, are supported by the current hardware.</span></span>
-   <span data-ttu-id="474d6-169">[**ID3D11DeviceCoNtext2：： CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) ：會從緩衝區將圖格複製到磚資源，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="474d6-169">[**ID3D11DeviceContext2::CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) : copies tiles from buffer to tiled resource or vice versa.</span></span>
-   <span data-ttu-id="474d6-170">[**ID3D11DeviceCoNtext2：： UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) ：將並排顯示的資源中的磚位置對應更新為磚集區中的記憶體位置。</span><span class="sxs-lookup"><span data-stu-id="474d6-170">[**ID3D11DeviceContext2::UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) : updates mappings of tile locations in tiled resources to memory locations in a tile pool.</span></span>
-   <span data-ttu-id="474d6-171">[**ID3D11DeviceCoNtext2：： CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) ：將對應從來源磚的資源複製到已並排顯示的資源。</span><span class="sxs-lookup"><span data-stu-id="474d6-171">[**ID3D11DeviceContext2::CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) : copies mappings from a source tiled resource to a destination tiled resource.</span></span>
-   <span data-ttu-id="474d6-172">[**ID3D11DeviceCoNtext2：： GetResourceTiling**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling) ：取得如何將磚的資源分成磚的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="474d6-172">[**ID3D11DeviceContext2::GetResourceTiling**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling) : gets info about how a tiled resource is broken into tiles.</span></span>

## <a name="related-topics"></a><span data-ttu-id="474d6-173">相關主題</span><span class="sxs-lookup"><span data-stu-id="474d6-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="474d6-174">Direct3D 11.3 功能</span><span class="sxs-lookup"><span data-stu-id="474d6-174">Direct3D 11.3 Features</span></span>](direct3d-11-3-features.md)
</dt> </dl>

 

 




