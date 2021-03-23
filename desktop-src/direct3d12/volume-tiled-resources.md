---
title: " (Direct3D 12) 的磁片區磚資源"
description: 磁片區 (3D) 材質可以用來做為並排的資源，請注意磚解析度是三維。
ms.assetid: F670D15D-BC0F-4F90-99C1-A35192FE8980
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42679155bbd8dc2cec560d2724e430c860f54bc0
ms.sourcegitcommit: 05e7efd3d8de6926d08802669f37e825a2fa2f46
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/12/2020
ms.locfileid: "104548360"
---
# <a name="volume-tiled-resources-direct3d-12"></a><span data-ttu-id="0e3b5-103"> (Direct3D 12) 的磁片區磚資源</span><span class="sxs-lookup"><span data-stu-id="0e3b5-103">Volume tiled resources (Direct3D 12)</span></span>

<span data-ttu-id="0e3b5-104">磁片區 (3D) 材質可以用來做為並排的資源，請注意磚解析度是三維。</span><span class="sxs-lookup"><span data-stu-id="0e3b5-104">Volume (3D) textures can be used as tiled resources, noting that tile resolution is three-dimensional.</span></span>

-   [<span data-ttu-id="0e3b5-105">概觀</span><span class="sxs-lookup"><span data-stu-id="0e3b5-105">Overview</span></span>](#overview)
-   [<span data-ttu-id="0e3b5-106">磚資源 Api</span><span class="sxs-lookup"><span data-stu-id="0e3b5-106">Tiled Resource APIs</span></span>](#tiled-resource-apis)
-   [<span data-ttu-id="0e3b5-107">相關主題</span><span class="sxs-lookup"><span data-stu-id="0e3b5-107">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="0e3b5-108">概觀</span><span class="sxs-lookup"><span data-stu-id="0e3b5-108">Overview</span></span>

<span data-ttu-id="0e3b5-109">並排顯示的資源會將 D3D 資源物件與其支援記憶體分離， (資源在過去具有與其支援記憶體) 的1:1 關聯性。</span><span class="sxs-lookup"><span data-stu-id="0e3b5-109">Tiled resources decouple a D3D Resource object from its backing memory (resources in the past had a 1:1 relationship with their backing memory).</span></span> <span data-ttu-id="0e3b5-110">這可提供各種有趣的案例，例如在材質資料中串流處理，以及重複使用或減少記憶體使用量。</span><span class="sxs-lookup"><span data-stu-id="0e3b5-110">This allows for a variety of interesting scenarios such as streaming in texture data and reusing or reducing memory usage.</span></span>

<span data-ttu-id="0e3b5-111">D3D 11.2 支援2D 紋理磚資源。</span><span class="sxs-lookup"><span data-stu-id="0e3b5-111">2D texture tiled resources are supported in D3D11.2.</span></span> <span data-ttu-id="0e3b5-112">D3D12 和 D3D 11.3 可選擇性支援3D 並排顯示的材質 (請參閱 D3D12 並排顯示的 [**\_ \_ 資源 \_ 層級**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier)) 。</span><span class="sxs-lookup"><span data-stu-id="0e3b5-112">Optional support for 3D tiled textures is available for D3D12 and D3D11.3 (refer to [**D3D12\_TILED\_RESOURCES\_TIER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier)).</span></span>

<span data-ttu-id="0e3b5-113">磚中所使用的一般資源維度是2D 紋理的 4 x 4 磚，以及3D 紋理的 4 x 4 x 4 個圖格。</span><span class="sxs-lookup"><span data-stu-id="0e3b5-113">The typical resource dimensions used in tiling are 4 x 4 tiles for 2D textures, and 4 x 4 x 4 tiles for 3D textures.</span></span>



| <span data-ttu-id="0e3b5-114">位/圖元 (1 取樣/圖元) </span><span class="sxs-lookup"><span data-stu-id="0e3b5-114">Bits/pixel (1 sample/pixel)</span></span> | <span data-ttu-id="0e3b5-115">磚尺寸 (圖元，w x h x d) </span><span class="sxs-lookup"><span data-stu-id="0e3b5-115">Tile dimensions (pixels, w x h x d)</span></span> |
|-----------------------------|-------------------------------------|
| <span data-ttu-id="0e3b5-116">8</span><span class="sxs-lookup"><span data-stu-id="0e3b5-116">8</span></span>                           | <span data-ttu-id="0e3b5-117">64 x 32 x 32</span><span class="sxs-lookup"><span data-stu-id="0e3b5-117">64x32x32</span></span>                            |
| <span data-ttu-id="0e3b5-118">16</span><span class="sxs-lookup"><span data-stu-id="0e3b5-118">16</span></span>                          | <span data-ttu-id="0e3b5-119">32 x 32 x 32</span><span class="sxs-lookup"><span data-stu-id="0e3b5-119">32x32x32</span></span>                            |
| <span data-ttu-id="0e3b5-120">32</span><span class="sxs-lookup"><span data-stu-id="0e3b5-120">32</span></span>                          | <span data-ttu-id="0e3b5-121">32 x 32 x 16</span><span class="sxs-lookup"><span data-stu-id="0e3b5-121">32x32x16</span></span>                            |
| <span data-ttu-id="0e3b5-122">64</span><span class="sxs-lookup"><span data-stu-id="0e3b5-122">64</span></span>                          | <span data-ttu-id="0e3b5-123">32 x 16 x 16</span><span class="sxs-lookup"><span data-stu-id="0e3b5-123">32x16x16</span></span>                            |
| <span data-ttu-id="0e3b5-124">128</span><span class="sxs-lookup"><span data-stu-id="0e3b5-124">128</span></span>                         | <span data-ttu-id="0e3b5-125">16 x 16 x 16</span><span class="sxs-lookup"><span data-stu-id="0e3b5-125">16x16x16</span></span>                            |
| <span data-ttu-id="0e3b5-126">BC 1、4</span><span class="sxs-lookup"><span data-stu-id="0e3b5-126">BC 1,4</span></span>                      | <span data-ttu-id="0e3b5-127">128 x 64 x 16</span><span class="sxs-lookup"><span data-stu-id="0e3b5-127">128x64x16</span></span>                           |
| <span data-ttu-id="0e3b5-128">BC 2、3、5、6、7</span><span class="sxs-lookup"><span data-stu-id="0e3b5-128">BC 2,3,5,6,7</span></span>                | <span data-ttu-id="0e3b5-129">64 x 64 x 16</span><span class="sxs-lookup"><span data-stu-id="0e3b5-129">64x64x16</span></span>                            |

<span data-ttu-id="0e3b5-130">請注意，磚式資源不支援下列格式：96bpp 格式、影片格式、R1 \_ UNORM、R8G8 \_ B8G8 \_ UNORM、R8R8 \_ G8B8 \_ UNORM。</span><span class="sxs-lookup"><span data-stu-id="0e3b5-130">Note the following formats are not supported with tiled resources: 96bpp formats, video formats, R1\_UNORM, R8G8\_B8G8\_UNORM, R8R8\_G8B8\_UNORM.</span></span>

<span data-ttu-id="0e3b5-131">在下列圖表中，暗灰色表示 Null 磚。</span><span class="sxs-lookup"><span data-stu-id="0e3b5-131">In the diagrams below dark gray represents NULL tiles.</span></span>

-   [<span data-ttu-id="0e3b5-132">紋理3D 將資源預設對應 (最詳細的 mip) </span><span class="sxs-lookup"><span data-stu-id="0e3b5-132">Texture 3D Tiled Resource default mapping (most detailed mip)</span></span>](#texture-3d-tiled-resource-default-mapping-most-detailed-mip)
-   [<span data-ttu-id="0e3b5-133">紋理3D 並排顯示的資源預設對應 (第二個最詳細的 mip) </span><span class="sxs-lookup"><span data-stu-id="0e3b5-133">Texture 3D Tiled Resource default mapping (second most detailed mip)</span></span>](#texture-3d-tiled-resource-default-mapping-second-most-detailed-mip)
-   [<span data-ttu-id="0e3b5-134">紋理3D 並排顯示資源 (最詳細的 mip) </span><span class="sxs-lookup"><span data-stu-id="0e3b5-134">Texture 3D Tiled Resource (most detailed mip)</span></span>](#texture-3d-tiled-resource-most-detailed-mip)
-   [<span data-ttu-id="0e3b5-135">紋理3D 並排顯示資源 (第二個最詳細的 mip) </span><span class="sxs-lookup"><span data-stu-id="0e3b5-135">Texture 3D Tiled Resource (second most detailed mip)</span></span>](#texture-3d-tiled-resource-second-most-detailed-mip)
-   [<span data-ttu-id="0e3b5-136">紋理3D 磚資源 (單一磚) </span><span class="sxs-lookup"><span data-stu-id="0e3b5-136">Texture 3D Tiled Resource (Single Tile)</span></span>](#texture-3d-tiled-resource-single-tile)
-   [<span data-ttu-id="0e3b5-137">紋理3D 並排顯示資源 (統一方塊) </span><span class="sxs-lookup"><span data-stu-id="0e3b5-137">Texture 3D Tiled Resource (Uniform Box)</span></span>](#texture-3d-tiled-resource-uniform-box)

### <a name="texture-3d-tiled-resource-default-mapping-most-detailed-mip"></a><span data-ttu-id="0e3b5-138">紋理3D 將資源預設對應 (最詳細的 mip) </span><span class="sxs-lookup"><span data-stu-id="0e3b5-138">Texture 3D Tiled Resource default mapping (most detailed mip)</span></span>

![並排顯示的3維度資源預設對應](images/vtr-tex3d-default-1.png)

### <a name="texture-3d-tiled-resource-default-mapping-second-most-detailed-mip"></a><span data-ttu-id="0e3b5-140">紋理3D 並排顯示的資源預設對應 (第二個最詳細的 mip) </span><span class="sxs-lookup"><span data-stu-id="0e3b5-140">Texture 3D Tiled Resource default mapping (second most detailed mip)</span></span>

![顯示第二個最詳細的 mip](images/vtr-tex3d-default-2.png)

### <a name="texture-3d-tiled-resource-most-detailed-mip"></a><span data-ttu-id="0e3b5-142">紋理3D 並排顯示資源 (最詳細的 mip) </span><span class="sxs-lookup"><span data-stu-id="0e3b5-142">Texture 3D Tiled Resource (most detailed mip)</span></span>

<span data-ttu-id="0e3b5-143">下列程式碼會在最詳細的 mip 上設定3D 磚資源。</span><span class="sxs-lookup"><span data-stu-id="0e3b5-143">The following code sets up a 3D tiled resource at the most detailed mip.</span></span>

``` syntax
D3D12_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 1;
trCoord.Y = 0;
trCoord.Z = 0;
trCoord.Subresource = 0;

D3D12_TILE_REGION_SIZE trSize;
trSize.bUseBox = false;
trSize.NumTiles = 63;
```

![三維度材質最詳細的 mip](images/vtr-tex3d-default-1b.png)

### <a name="texture-3d-tiled-resource-second-most-detailed-mip"></a><span data-ttu-id="0e3b5-145">紋理3D 並排顯示資源 (第二個最詳細的 mip) </span><span class="sxs-lookup"><span data-stu-id="0e3b5-145">Texture 3D Tiled Resource (second most detailed mip)</span></span>

<span data-ttu-id="0e3b5-146">下列程式碼會設定3D 並排顯示的資源，以及第二個最詳細的 mip：</span><span class="sxs-lookup"><span data-stu-id="0e3b5-146">The following code sets up a 3D tiled resource, and the second most detailed mip:</span></span>

``` syntax
D3D12_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 1;
trCoord.Y = 0;
trCoord.Z = 0;
trCoord.Subresource = 1;

D3D12_TILE_REGION_SIZE trSize;
trSize.bUseBox = false;
trSize.NumTiles = 6;
```

![三維度材質的第二個最詳細 mip](images/vtr-tex3d-default-2b.png)

### <a name="texture-3d-tiled-resource-single-tile"></a><span data-ttu-id="0e3b5-148">紋理3D 磚資源 (單一磚) </span><span class="sxs-lookup"><span data-stu-id="0e3b5-148">Texture 3D Tiled Resource (Single Tile)</span></span>

<span data-ttu-id="0e3b5-149">下列程式碼會設定單一磚資源：</span><span class="sxs-lookup"><span data-stu-id="0e3b5-149">The following code sets up a Single Tile resource:</span></span>

``` syntax
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

![一個並排顯示的三維度資源](images/vtr-tex3d-single.png)

### <a name="texture-3d-tiled-resource-uniform-box"></a><span data-ttu-id="0e3b5-151">紋理3D 並排顯示資源 (統一方塊) </span><span class="sxs-lookup"><span data-stu-id="0e3b5-151">Texture 3D Tiled Resource (Uniform Box)</span></span>

<span data-ttu-id="0e3b5-152">下列程式碼會設定並排顯示資源 (記下語句的統一方塊 `trSize.bUseBox = true;) :`</span><span class="sxs-lookup"><span data-stu-id="0e3b5-152">The following code sets up a Uniform Box tiled resource (note the statement `trSize.bUseBox = true;) :`</span></span>

``` syntax
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

## <a name="tiled-resource-apis"></a><span data-ttu-id="0e3b5-154">磚資源 Api</span><span class="sxs-lookup"><span data-stu-id="0e3b5-154">Tiled Resource APIs</span></span>

<span data-ttu-id="0e3b5-155">相同的 API 呼叫同時用於2D 和3D 並排顯示的資源：</span><span class="sxs-lookup"><span data-stu-id="0e3b5-155">The same API calls are used for both 2D and 3D tiled resources:</span></span>

<span data-ttu-id="0e3b5-156">列舉</span><span class="sxs-lookup"><span data-stu-id="0e3b5-156">Enums</span></span>

-   <span data-ttu-id="0e3b5-157">[**D3D12 \_並排顯示的 \_ 資源 \_ 層**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier) ：決定並排資源支援的層級。</span><span class="sxs-lookup"><span data-stu-id="0e3b5-157">[**D3D12\_TILED\_RESOURCES\_TIER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier) : determines the level of tiled resource support.</span></span>
-   <span data-ttu-id="0e3b5-158">[**D3D12 \_FORMAT \_ SUPPORT2**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2) ：用來測試已並排的資源支援。</span><span class="sxs-lookup"><span data-stu-id="0e3b5-158">[**D3D12\_FORMAT\_SUPPORT2**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2) : used to test for tiled resource support.</span></span>
-   <span data-ttu-id="0e3b5-159">[**D3D12 \_多型 \_ 品質 \_ 層級 \_ 旗標**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_multisample_quality_level_flags) ：決定多取樣資源中的磚資源支援。</span><span class="sxs-lookup"><span data-stu-id="0e3b5-159">[**D3D12\_MULTISAMPLE\_QUALITY\_LEVEL\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_multisample_quality_level_flags) : determines tiled resource support in a multi-sampling resource.</span></span>
-   <span data-ttu-id="0e3b5-160">[**D3D12 \_磚 \_ 複製 \_ 旗標**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tile_copy_flags) ：保留在 swizzled 並排顯示的資源和線性緩衝區進行複製的旗標。</span><span class="sxs-lookup"><span data-stu-id="0e3b5-160">[**D3D12\_TILE\_COPY\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tile_copy_flags) : holds flags for copying to and from swizzled tiled resources and linear buffers.</span></span>

<span data-ttu-id="0e3b5-161">結構</span><span class="sxs-lookup"><span data-stu-id="0e3b5-161">Structs</span></span>

-   <span data-ttu-id="0e3b5-162">[**D3D12 \_並排顯示的 \_ 資源 \_ 座標**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) ：保留 x、y 和 z 座標，以及 subresource 參考。</span><span class="sxs-lookup"><span data-stu-id="0e3b5-162">[**D3D12\_TILED\_RESOURCE\_COORDINATE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) : holds the x, y, and z co-ordinate, and subresource reference.</span></span> <span data-ttu-id="0e3b5-163">請注意，有一個協助程式結構： [**CD3DX12 平並排的 \_ \_ 資源 \_ 座標**](cd3dx12-tiled-resource-coordinate.md)。</span><span class="sxs-lookup"><span data-stu-id="0e3b5-163">Note there is a helper structure: [**CD3DX12\_TILED\_RESOURCE\_COORDINATE**](cd3dx12-tiled-resource-coordinate.md).</span></span>
-   <span data-ttu-id="0e3b5-164">[**D3D12 \_磚 \_ 區域 \_ 大小**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) ：指定並排顯示區域的大小和圖格數目。</span><span class="sxs-lookup"><span data-stu-id="0e3b5-164">[**D3D12\_TILE\_REGION\_SIZE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) : specifies the size, and number of tiles, of the tiled region.</span></span>
-   <span data-ttu-id="0e3b5-165">[**D3D12 \_磚 \_ 圖形**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape) ：圖格圖形為材質中的寬度、高度和深度。</span><span class="sxs-lookup"><span data-stu-id="0e3b5-165">[**D3D12\_TILE\_SHAPE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape) : the tile shape as a width, height and depth in texels.</span></span>
-   <span data-ttu-id="0e3b5-166">[**D3D12 \_功能 \_ 資料 \_ D3D12 \_ 選項**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) ：保留支援的磚資源層級和布林值 *VolumeTiledResourcesSupported*，指出是否支援磁片區並排顯示的資源。</span><span class="sxs-lookup"><span data-stu-id="0e3b5-166">[**D3D12\_FEATURE\_DATA\_D3D12\_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) : holds the supported tile resource tier level and a boolean, *VolumeTiledResourcesSupported*, indicated whether volume tiled resources are supported.</span></span>

<span data-ttu-id="0e3b5-167">方法</span><span class="sxs-lookup"><span data-stu-id="0e3b5-167">Methods</span></span>

-   <span data-ttu-id="0e3b5-168">[**ID3D12Device：： CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) ：用來判斷目前硬體所支援的功能和層級。</span><span class="sxs-lookup"><span data-stu-id="0e3b5-168">[**ID3D12Device::CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) : used to determine what features, and at what tier, are supported by the current hardware.</span></span>
-   <span data-ttu-id="0e3b5-169">[**ID3D12GraphcisCommandList：： CopyTiles**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles) ：會從緩衝區將圖格複製到磚資源，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="0e3b5-169">[**ID3D12GraphcisCommandList::CopyTiles**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles) : copies tiles from buffer to tiled resource or vice versa.</span></span>
-   <span data-ttu-id="0e3b5-170">[**ID3D12CommandQueue：： UpdateTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings) ：將並排顯示的資源中的磚位置對應更新為資源堆積中的記憶體位置。</span><span class="sxs-lookup"><span data-stu-id="0e3b5-170">[**ID3D12CommandQueue::UpdateTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings) : updates mappings of tile locations in tiled resources to memory locations in a resource heap.</span></span>
-   <span data-ttu-id="0e3b5-171">[**ID3D12CommandQueue：： CopyTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-copytilemappings) ：將對應從來源磚的資源複製到已並排顯示的資源。</span><span class="sxs-lookup"><span data-stu-id="0e3b5-171">[**ID3D12CommandQueue::CopyTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-copytilemappings) : copies mappings from a source tiled resource to a destination tiled resource.</span></span>
-   <span data-ttu-id="0e3b5-172">[**ID3D12Device：： GetResourceTiling**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourcetiling) ：取得如何將磚的資源分成磚的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0e3b5-172">[**ID3D12Device::GetResourceTiling**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourcetiling) : gets info about how a tiled resource is broken into tiles.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0e3b5-173">相關主題</span><span class="sxs-lookup"><span data-stu-id="0e3b5-173">Related topics</span></span>
* [<span data-ttu-id="0e3b5-174">資源系結</span><span class="sxs-lookup"><span data-stu-id="0e3b5-174">Resource Binding</span></span>](resource-binding.md)
