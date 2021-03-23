---
title: '子資源 (Direct3D 12 圖形) '
description: 說明如何將資源分割成子資源，以及如何參考子資源的單一、多重或配量。
ms.assetid: C4F92F8A-DBF0-412B-8707-CC4C1BF2D88F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e8fa8ea0d48fea7ee8e192d9dcf1fe5e3d22423
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104548408"
---
# <a name="subresources-direct3d-12-graphics"></a><span data-ttu-id="b540e-103">子資源 (Direct3D 12 圖形) </span><span class="sxs-lookup"><span data-stu-id="b540e-103">Subresources (Direct3D 12 Graphics)</span></span>

<span data-ttu-id="b540e-104">說明如何將資源分割成子資源，以及如何參考子資源的單一、多重或配量。</span><span class="sxs-lookup"><span data-stu-id="b540e-104">Describes how a resource is divided into subresources, and how to reference a single, multiple or slice of subresources.</span></span>

-   [<span data-ttu-id="b540e-105">範例子資源</span><span class="sxs-lookup"><span data-stu-id="b540e-105">Example subresources</span></span>](#example-subresources)
    -   [<span data-ttu-id="b540e-106">Subresource 索引</span><span class="sxs-lookup"><span data-stu-id="b540e-106">Subresource indexing</span></span>](#subresource-indexing)
    -   [<span data-ttu-id="b540e-107">Mip 配量</span><span class="sxs-lookup"><span data-stu-id="b540e-107">Mip slice</span></span>](#mip-slice)
    -   [<span data-ttu-id="b540e-108">陣列配量</span><span class="sxs-lookup"><span data-stu-id="b540e-108">Array slice</span></span>](#array-slice)
    -   [<span data-ttu-id="b540e-109">平面配量</span><span class="sxs-lookup"><span data-stu-id="b540e-109">Plane slice</span></span>](#plane-slice)
    -   [<span data-ttu-id="b540e-110">多個子資源</span><span class="sxs-lookup"><span data-stu-id="b540e-110">Multiple subresources</span></span>](#multiple-subresources)
-   [<span data-ttu-id="b540e-111">Subresource Api</span><span class="sxs-lookup"><span data-stu-id="b540e-111">Subresource APIs</span></span>](#subresource-apis)
-   [<span data-ttu-id="b540e-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="b540e-112">Related topics</span></span>](#related-topics)

## <a name="example-subresources"></a><span data-ttu-id="b540e-113">範例子資源</span><span class="sxs-lookup"><span data-stu-id="b540e-113">Example subresources</span></span>

<span data-ttu-id="b540e-114">如果資源包含緩衝區，則它只會包含一個索引為0的 subresource。</span><span class="sxs-lookup"><span data-stu-id="b540e-114">If a resource contains a buffer, then it simply contains one subresource with an index of 0.</span></span> <span data-ttu-id="b540e-115">如果資源包含材質 (或紋理陣列) ，則參考子資源會更複雜。</span><span class="sxs-lookup"><span data-stu-id="b540e-115">If the resource contains a texture (or texture array), then referencing the subresources is more complex.</span></span>

<span data-ttu-id="b540e-116">某些 Api 會存取整個資源 (例如 [**ID3D12GraphicsCommandList：： CopyResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource) 方法) ，其他人會存取一部分的資源 (例如 [**ID3D12Resource：： ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) 方法) 。</span><span class="sxs-lookup"><span data-stu-id="b540e-116">Some APIs access an entire resource (such as the [**ID3D12GraphicsCommandList::CopyResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource) method), others access a portion of a resource (for example the [**ID3D12Resource::ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) method).</span></span> <span data-ttu-id="b540e-117">存取某個資源部分的方法通常會使用 view description (例如 [**D3D12 \_ TEX2D \_ ARRAY \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv) 結構) 指定要存取的子資源。</span><span class="sxs-lookup"><span data-stu-id="b540e-117">The methods that access a portion of a resource generally use a view description (such as the [**D3D12\_TEX2D\_ARRAY\_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv) structure) to specify the subresources to access.</span></span> <span data-ttu-id="b540e-118">如需完整清單，請參閱 [Subresource api](#subresource-apis) 一節。</span><span class="sxs-lookup"><span data-stu-id="b540e-118">Refer to the [Subresource APIs](#subresource-apis) section for a complete list.</span></span>

### <a name="subresource-indexing"></a><span data-ttu-id="b540e-119">Subresource 索引</span><span class="sxs-lookup"><span data-stu-id="b540e-119">Subresource indexing</span></span>

<span data-ttu-id="b540e-120">為了編制特定 subresource 的索引，會先編制 mip 層級的索引，因為每個陣列專案都已編制索引。</span><span class="sxs-lookup"><span data-stu-id="b540e-120">To index a particular subresource, the mip levels are indexed first as each array entry is indexed.</span></span>

![subresource 索引](images/subresource-index.png)

### <a name="mip-slice"></a><span data-ttu-id="b540e-122">Mip 配量</span><span class="sxs-lookup"><span data-stu-id="b540e-122">Mip slice</span></span>

<span data-ttu-id="b540e-123">Mip 配量包含陣列中每個材質的一個 mipmap 層級，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="b540e-123">A mip slice includes one mipmap level for every texture in an array, as shown in the following image.</span></span>

![subresource mip 配量](images/subresource-mip-slice.png)

### <a name="array-slice"></a><span data-ttu-id="b540e-125">陣列配量</span><span class="sxs-lookup"><span data-stu-id="b540e-125">Array slice</span></span>

<span data-ttu-id="b540e-126">根據紋理的陣列，每個材質都有 mipmap，陣列配量包含一個材質和其所有 mip 層級，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="b540e-126">Given an array of textures, each texture with mipmaps, an array slice includes one texture and all of its mip levels, as shown in the following image.</span></span>

![subresource 陣列配量](images/subresource-array-slices.png)

### <a name="plane-slice"></a><span data-ttu-id="b540e-128">平面配量</span><span class="sxs-lookup"><span data-stu-id="b540e-128">Plane slice</span></span>

<span data-ttu-id="b540e-129">平面格式通常不會用來儲存 RGBA 資料，但如果 (可能 24bpp RGB 資料) ，則一個平面可以代表紅色影像、一個綠色，以及一個藍色的影像。</span><span class="sxs-lookup"><span data-stu-id="b540e-129">Typically planar formats are not used to store RGBA data, but in the cases where it is (perhaps 24bpp RGB data), one plane could represent the red image, one the green, and one the blue image.</span></span> <span data-ttu-id="b540e-130">不過，一個平面不一定是一種色彩，可以將兩個或更多的色彩組合成一個平面。</span><span class="sxs-lookup"><span data-stu-id="b540e-130">One plane though is not necessarily one color, two or more colors could be combined into one plane.</span></span> <span data-ttu-id="b540e-131">通常會使用平面資料來進行子樣本 YCbCr 和 Depth-Stencil 資料。</span><span class="sxs-lookup"><span data-stu-id="b540e-131">More typically planar data is used for sub-sampled YCbCr and Depth-Stencil data.</span></span> <span data-ttu-id="b540e-132">Depth-Stencil 是唯一支援 mipmap、陣列和多個平面的格式 (通常是深度的平面0和樣板) 的平面1。</span><span class="sxs-lookup"><span data-stu-id="b540e-132">Depth-Stencil is the only format that fully supports mipmaps, arrays, and multiple planes (often plane 0 for Depth and plane 1 for Stencil).</span></span>

<span data-ttu-id="b540e-133">針對兩個 Depth-Stencil 映射的陣列編制索引 subresource，每個影像都有三個 mip 層級，如下所示。</span><span class="sxs-lookup"><span data-stu-id="b540e-133">The subresource indexing for an array of two Depth-Stencil images, each with three mip levels, is shown below.</span></span>

![深度樣板索引編制](images/depth-stencil-indexing.png)

<span data-ttu-id="b540e-135">子樣本 YCbCr 支援陣列且具有平面，但不支援 mipmap。</span><span class="sxs-lookup"><span data-stu-id="b540e-135">Sub-sampled YCbCr supports arrays and has planes, but does not support mipmaps.</span></span> <span data-ttu-id="b540e-136">YCbCr 影像有兩個平面，一個適用于每個平面的亮度 (Y) ，其中一個適用于人類眼最敏感的亮度，另一個用於色度，也就是一種 (，也就是「Cb」和「Cr」交錯) ，人類眼睛較不敏感</span><span class="sxs-lookup"><span data-stu-id="b540e-136">YCbCr images have two planes, one for the luminance (Y) that the human eye is most sensitive to, and one for the chrominance (both Cb, and Cr, interleaved) which the human eye is less sensitive to.</span></span> <span data-ttu-id="b540e-137">此格式可讓您壓縮色度值，以便在不影響亮度的情況下壓縮影像，而且這是一種常見的影片壓縮格式，但它可用來壓縮靜止影像。</span><span class="sxs-lookup"><span data-stu-id="b540e-137">This format enables compression of the chrominance values in order to compress an image without affecting the luminance, and is a common video compression format for that reason, although it is used to compress still images.</span></span> <span data-ttu-id="b540e-138">下圖顯示 NV12 格式，請注意色度已壓縮成一季的亮度解析度，這表示每個平面的寬度都相同，而色度平面是亮度平面高度的一半。</span><span class="sxs-lookup"><span data-stu-id="b540e-138">The image below shows the NV12 format, noting the chrominance has been compressed to one quarter of the resolution of the luminance, meaning the width of each plane is identical, and the chrominance plane is half the height of the luminance plane.</span></span> <span data-ttu-id="b540e-139">平面會以子資源的方式，以與上述 Depth-Stencil 範例相同的方式來編制索引。</span><span class="sxs-lookup"><span data-stu-id="b540e-139">The planes would be indexed as subresources in an identical way to the Depth-Stencil example above.</span></span>

![nv12 格式](images/ycbcr.png)

<span data-ttu-id="b540e-141">在 Direct3D 11 中存在平面格式，但無法個別定址個別的平面，例如複製或對應作業。</span><span class="sxs-lookup"><span data-stu-id="b540e-141">Planar formats existed in Direct3D 11, but individual planes could not be addressed individually, say for copy or mapping operations.</span></span> <span data-ttu-id="b540e-142">這已在 Direct3D 12 中變更，因此每個平面都會收到自己的 subresource 識別碼。</span><span class="sxs-lookup"><span data-stu-id="b540e-142">This was changed in Direct3D 12 so that each plane received its own subresource ID.</span></span> <span data-ttu-id="b540e-143">比較下列兩個方法來計算 subresource 識別碼。</span><span class="sxs-lookup"><span data-stu-id="b540e-143">Compare the following two methods for calculating the subresource ID.</span></span>

<span data-ttu-id="b540e-144">Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="b540e-144">Direct3D 11</span></span>

``` syntax
inline UINT D3D11CalcSubresource( UINT MipSlice, UINT ArraySlice, UINT MipLevels )
{
    return MipSlice + (ArraySlice * MipLevels); 
}
```

<span data-ttu-id="b540e-145">Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="b540e-145">Direct3D 12</span></span>

``` syntax
inline UINT D3D12CalcSubresource( UINT MipSlice, UINT ArraySlice, UINT PlaneSlice, UINT MipLevels, UINT ArraySize )
{ 
    return MipSlice + (ArraySlice * MipLevels) + (PlaneSlice * MipLevels * ArraySize); 
}
```

<span data-ttu-id="b540e-146">大部分的硬體都會假設平面 N 的記憶體一律會在平面 N-1 之後立即配置。</span><span class="sxs-lookup"><span data-stu-id="b540e-146">Most hardware assumes that the memory for plane N is always immediately allocated after plane N-1.</span></span>

<span data-ttu-id="b540e-147">使用子資源的替代方案是，應用程式可以為每個平面配置完全不同的資源。</span><span class="sxs-lookup"><span data-stu-id="b540e-147">An alternative to using subresources is that an app could allocate a completely separate resource per plane.</span></span> <span data-ttu-id="b540e-148">在此情況下，應用程式瞭解資料是平面的，並使用多個資源來代表它。</span><span class="sxs-lookup"><span data-stu-id="b540e-148">In this case, the application understands the data is planar and uses multiple resources to represent it.</span></span>

### <a name="multiple-subresources"></a><span data-ttu-id="b540e-149">多個子資源</span><span class="sxs-lookup"><span data-stu-id="b540e-149">Multiple subresources</span></span>

<span data-ttu-id="b540e-150">著色器資源檢視可以選取子資源的任何矩形區域，並使用上述其中一個配量，併合理使用 view (結構中的欄位，例如 [**D3D12 \_ TEX2D \_ ARRAY \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)) ，如影像中所示。</span><span class="sxs-lookup"><span data-stu-id="b540e-150">A shader-resource view can select any rectangular region of subresources, using one of the slices described above and judicious use of fields in the view structures (such as [**D3D12\_TEX2D\_ARRAY\_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)), as shown in the image.</span></span>

![多重 subresource 選取專案](images/subresource-multiple.png)

<span data-ttu-id="b540e-152">轉譯目標視圖只能使用單一 subresource 或 mip 配量，且不能包含來自一個以上 mip 配量的子資源。</span><span class="sxs-lookup"><span data-stu-id="b540e-152">A render-target view can only use a single subresource or mip slice and cannot include subresources from more than one mip slice.</span></span> <span data-ttu-id="b540e-153">也就是說，轉譯目標視圖中的每個材質都必須是相同的大小。</span><span class="sxs-lookup"><span data-stu-id="b540e-153">That is, every texture in a render-target view must be the same size.</span></span> <span data-ttu-id="b540e-154">著色器資源檢視可以選取子資源的任何矩形區域，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="b540e-154">A shader-resource view can select any rectangular region of subresources, as shown in the image.</span></span>

## <a name="subresource-apis"></a><span data-ttu-id="b540e-155">Subresource Api</span><span class="sxs-lookup"><span data-stu-id="b540e-155">Subresource APIs</span></span>

<span data-ttu-id="b540e-156">下列 Api 參考和使用子資源：</span><span class="sxs-lookup"><span data-stu-id="b540e-156">The following APIs reference and work with subresources:</span></span>

<span data-ttu-id="b540e-157">枚舉：</span><span class="sxs-lookup"><span data-stu-id="b540e-157">Enumerations:</span></span>

-   [<span data-ttu-id="b540e-158">**D3D12 \_ 材質 \_ 複製 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="b540e-158">**D3D12\_TEXTURE\_COPY\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_copy_type)

<span data-ttu-id="b540e-159">下列結構包含 *PlaneSlice* 索引，最多包含 *MipSlice* 索引。</span><span class="sxs-lookup"><span data-stu-id="b540e-159">The following structures contain *PlaneSlice* indexes, most contain *MipSlice* indexes.</span></span>

-   [<span data-ttu-id="b540e-160">**D3D12 \_ TEX2D \_ RTV**</span><span class="sxs-lookup"><span data-stu-id="b540e-160">**D3D12\_TEX2D\_RTV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_rtv)
-   [<span data-ttu-id="b540e-161">**D3D12 \_ TEX2D \_ 陣列 \_ RTV**</span><span class="sxs-lookup"><span data-stu-id="b540e-161">**D3D12\_TEX2D\_ARRAY\_RTV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_rtv)
-   [<span data-ttu-id="b540e-162">**D3D12 \_ TEX2D \_ SRV**</span><span class="sxs-lookup"><span data-stu-id="b540e-162">**D3D12\_TEX2D\_SRV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_srv)
-   [<span data-ttu-id="b540e-163">**D3D12 \_ TEX2D \_ 陣列 \_ SRV**</span><span class="sxs-lookup"><span data-stu-id="b540e-163">**D3D12\_TEX2D\_ARRAY\_SRV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)
-   [<span data-ttu-id="b540e-164">**D3D12 \_ TEX2D \_ UAV**</span><span class="sxs-lookup"><span data-stu-id="b540e-164">**D3D12\_TEX2D\_UAV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_uav)
-   [<span data-ttu-id="b540e-165">**D3D12 \_ TEX2D \_ 陣列 \_ UAV**</span><span class="sxs-lookup"><span data-stu-id="b540e-165">**D3D12\_TEX2D\_ARRAY\_UAV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_uav)

<span data-ttu-id="b540e-166">下列結構包含 *ArraySlice* 索引，最多包含 *MipSlice* 索引。</span><span class="sxs-lookup"><span data-stu-id="b540e-166">The following structures contain *ArraySlice* indexes, most contain *MipSlice* indexes.</span></span>

-   [<span data-ttu-id="b540e-167">**D3D12 \_ TEX1D \_ 陣列 \_ DSV**</span><span class="sxs-lookup"><span data-stu-id="b540e-167">**D3D12\_TEX1D\_ARRAY\_DSV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_dsv)
-   [<span data-ttu-id="b540e-168">**D3D12 \_ TEX2D \_ 陣列 \_ DSV**</span><span class="sxs-lookup"><span data-stu-id="b540e-168">**D3D12\_TEX2D\_ARRAY\_DSV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_dsv)
-   [<span data-ttu-id="b540e-169">**D3D12 \_ TEX2DMS \_ 陣列 \_ DSV**</span><span class="sxs-lookup"><span data-stu-id="b540e-169">**D3D12\_TEX2DMS\_ARRAY\_DSV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_dsv)
-   [<span data-ttu-id="b540e-170">**D3D12 \_ TEX1D \_ 陣列 \_ RTV**</span><span class="sxs-lookup"><span data-stu-id="b540e-170">**D3D12\_TEX1D\_ARRAY\_RTV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_rtv)
-   [<span data-ttu-id="b540e-171">**D3D12 \_ TEX2D \_ 陣列 \_ RTV**</span><span class="sxs-lookup"><span data-stu-id="b540e-171">**D3D12\_TEX2D\_ARRAY\_RTV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_rtv)
-   [<span data-ttu-id="b540e-172">**D3D12 \_ TEX2DMS \_ 陣列 \_ RTV**</span><span class="sxs-lookup"><span data-stu-id="b540e-172">**D3D12\_TEX2DMS\_ARRAY\_RTV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_rtv)
-   [<span data-ttu-id="b540e-173">**D3D12 \_ TEX1D \_ 陣列 \_ SRV**</span><span class="sxs-lookup"><span data-stu-id="b540e-173">**D3D12\_TEX1D\_ARRAY\_SRV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_srv)
-   [<span data-ttu-id="b540e-174">**D3D12 \_ TEX2D \_ 陣列 \_ SRV**</span><span class="sxs-lookup"><span data-stu-id="b540e-174">**D3D12\_TEX2D\_ARRAY\_SRV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)
-   [<span data-ttu-id="b540e-175">**D3D12 \_ TEX2DMS \_ 陣列 \_ SRV**</span><span class="sxs-lookup"><span data-stu-id="b540e-175">**D3D12\_TEX2DMS\_ARRAY\_SRV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_srv)
-   [<span data-ttu-id="b540e-176">**D3D12 \_ TEX1D \_ 陣列 \_ UAV**</span><span class="sxs-lookup"><span data-stu-id="b540e-176">**D3D12\_TEX1D\_ARRAY\_UAV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_uav)
-   [<span data-ttu-id="b540e-177">**D3D12 \_ TEX2D \_ 陣列 \_ UAV**</span><span class="sxs-lookup"><span data-stu-id="b540e-177">**D3D12\_TEX2D\_ARRAY\_UAV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_uav)

<span data-ttu-id="b540e-178">下列結構包含 *MipSlice* 索引，但不包含 *ArraySlice* 和 *PlaneSlice* 索引。</span><span class="sxs-lookup"><span data-stu-id="b540e-178">The following structures contain *MipSlice* indexes, but neither *ArraySlice* nor *PlaneSlice* indexes.</span></span>

-   [<span data-ttu-id="b540e-179">**D3D12 \_ TEX1D \_ DSV**</span><span class="sxs-lookup"><span data-stu-id="b540e-179">**D3D12\_TEX1D\_DSV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_dsv)
-   [<span data-ttu-id="b540e-180">**D3D12 \_ TEX2D \_ DSV**</span><span class="sxs-lookup"><span data-stu-id="b540e-180">**D3D12\_TEX2D\_DSV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_dsv)
-   [<span data-ttu-id="b540e-181">**D3D12 \_ TEX1D \_ RTV**</span><span class="sxs-lookup"><span data-stu-id="b540e-181">**D3D12\_TEX1D\_RTV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_rtv)
-   [<span data-ttu-id="b540e-182">**D3D12 \_ TEX3D \_ RTV**</span><span class="sxs-lookup"><span data-stu-id="b540e-182">**D3D12\_TEX3D\_RTV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_rtv)
-   [<span data-ttu-id="b540e-183">**D3D12 \_ TEX1D \_ UAV**</span><span class="sxs-lookup"><span data-stu-id="b540e-183">**D3D12\_TEX1D\_UAV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_uav)
-   [<span data-ttu-id="b540e-184">**D3D12 \_ TEX3D \_ UAV**</span><span class="sxs-lookup"><span data-stu-id="b540e-184">**D3D12\_TEX3D\_UAV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_uav)

<span data-ttu-id="b540e-185">下列結構也會參考子資源：</span><span class="sxs-lookup"><span data-stu-id="b540e-185">The following structures also reference subresources:</span></span>

-   <span data-ttu-id="b540e-186">[**D3D12 \_捨棄 \_ 區域**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_discard_region) ：用於準備捨棄資源的結構。</span><span class="sxs-lookup"><span data-stu-id="b540e-186">[**D3D12\_DISCARD\_REGION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_discard_region) : a structure used in preparation for discarding a resource.</span></span>
-   <span data-ttu-id="b540e-187">[**D3D12 \_放置 \_ 的 \_ SUBRESOURCE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint) 使用量：將位移新增至基本使用量的資源。</span><span class="sxs-lookup"><span data-stu-id="b540e-187">[**D3D12\_PLACED\_SUBRESOURCE\_FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint) : adds an offset into a resource to the basic footprint.</span></span>
-   <span data-ttu-id="b540e-188">[**D3D12 \_資源 \_ 轉換 \_ 屏障**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier) ：描述不同使用方式 (著色器資源、轉譯目標等 ) 之間的子資源轉換。</span><span class="sxs-lookup"><span data-stu-id="b540e-188">[**D3D12\_RESOURCE\_TRANSITION\_BARRIER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier) : describes the transition of subresources between different usages (shader resource, render target, etc.).</span></span>
-   <span data-ttu-id="b540e-189">[**D3D12 \_SUBRESOURCE \_ 資料**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) ： SUBRESOURCE 資料包含資料本身，以及資料列和配量的間距。</span><span class="sxs-lookup"><span data-stu-id="b540e-189">[**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) : subresource data includes the data itself, and the row and slice pitch.</span></span>
-   <span data-ttu-id="b540e-190">[**D3D12 \_SUBRESOURCE \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) 使用量：使用量包括 SUBRESOURCE 的格式、寬度、高度、深度和資料列的間距。</span><span class="sxs-lookup"><span data-stu-id="b540e-190">[**D3D12\_SUBRESOURCE\_FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) : a footprint includes the format, width, height, depth and row-pitch of the subresource.</span></span>
-   <span data-ttu-id="b540e-191">[**D3D12 \_SUBRESOURCE \_ 資訊**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_info) ：包含 SUBRESOURCE 的位移、資料列間距和深度音調。</span><span class="sxs-lookup"><span data-stu-id="b540e-191">[**D3D12\_SUBRESOURCE\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_info) : contains the offset, row pitch and depth pitch of the subresource.</span></span>
-   <span data-ttu-id="b540e-192">[**D3D12 \_SUBRESOURCE \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) 圖格：描述已並排的 SUBRESOURCE 音量 (請參閱) 的 [磁片區磚資源](volume-tiled-resources.md) 。</span><span class="sxs-lookup"><span data-stu-id="b540e-192">[**D3D12\_SUBRESOURCE\_TILING**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) : describes a tiled subresource volume (refer to [Volume Tiled Resources](volume-tiled-resources.md)).</span></span>
-   <span data-ttu-id="b540e-193">[**D3D12 \_材質 \_ 複製 \_ 位置**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) ：描述材質的一部分，以供複製之用。</span><span class="sxs-lookup"><span data-stu-id="b540e-193">[**D3D12\_TEXTURE\_COPY\_LOCATION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) : describes a portion of a texture for the purpose of copying.</span></span>
-   <span data-ttu-id="b540e-194">[**D3D12 \_並排顯示的 \_ 資源 \_ 座標**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) ：描述已並排資源的座標。</span><span class="sxs-lookup"><span data-stu-id="b540e-194">[**D3D12\_TILED\_RESOURCE\_COORDINATE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) : describes the coordinates of a tiled resource.</span></span>

<span data-ttu-id="b540e-195">方法:</span><span class="sxs-lookup"><span data-stu-id="b540e-195">Methods:</span></span>

-   <span data-ttu-id="b540e-196">[**ID3D12Device：： GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints) ：取得資源的資訊，以啟用複製。</span><span class="sxs-lookup"><span data-stu-id="b540e-196">[**ID3D12Device::GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints) : gets information on a resource, to enable a copy to be made.</span></span>
-   <span data-ttu-id="b540e-197">[**ID3D12Device：： GetResourceTiling**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourcetiling) ：取得如何將磚的資源分成磚的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b540e-197">[**ID3D12Device::GetResourceTiling**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourcetiling) : gets info about how a tiled resource is broken into tiles.</span></span>
-   <span data-ttu-id="b540e-198">[**ID3D12GraphicsCommandList：： ResolveSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource) ：將多取樣的 subresource 複製到非多重取樣的 subresource 中。</span><span class="sxs-lookup"><span data-stu-id="b540e-198">[**ID3D12GraphicsCommandList::ResolveSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource) : copies a multi-sampled subresource into a non-multi-sampled subresource.</span></span>
-   <span data-ttu-id="b540e-199">[**ID3D12Resource：： Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) ：傳回資源中指定資料的指標，並拒絕 SUBRESOURCE 的 GPU 存取。</span><span class="sxs-lookup"><span data-stu-id="b540e-199">[**ID3D12Resource::Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) : returns a pointer to the specified data in the resource, and denies the GPU access to the subresource.</span></span>
-   <span data-ttu-id="b540e-200">[**ID3D12Resource：： ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) ：從 subresource 或 subresource 的矩形區域複製資料。</span><span class="sxs-lookup"><span data-stu-id="b540e-200">[**ID3D12Resource::ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) : copies data from a subresource, or a rectangular region of a subresource.</span></span>
-   <span data-ttu-id="b540e-201">[**ID3D12Resource：：**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) 取消對應： unmaps 指定的記憶體範圍，並使資源的指標失效。</span><span class="sxs-lookup"><span data-stu-id="b540e-201">[**ID3D12Resource::Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) : unmaps the specified range of memory and invalidates the pointer to the resource.</span></span> <span data-ttu-id="b540e-202">掉 GPU 對 subresource 的存取。</span><span class="sxs-lookup"><span data-stu-id="b540e-202">Reinstates GPU access to the subresource.</span></span>
-   <span data-ttu-id="b540e-203">[**ID3D12Resource：： WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) ：將資料複製到 subresource 或 subresource 的矩形區域。</span><span class="sxs-lookup"><span data-stu-id="b540e-203">[**ID3D12Resource::WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) : copies data to a subresource, or a rectangular region of a subresource.</span></span>

<span data-ttu-id="b540e-204">紋理必須處於 [**D3D12 \_ 資源狀態的 \_ \_ 一般**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) 狀態，才能透過 [**WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) 和 [**ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) 進行 CPU 存取，但緩衝區則否。</span><span class="sxs-lookup"><span data-stu-id="b540e-204">Textures must be in the [**D3D12\_RESOURCE\_STATE\_COMMON**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) state for CPU access through [**WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) and [**ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) to be legal; but buffers do not.</span></span> <span data-ttu-id="b540e-205">資源的 CPU 存取通常是透過對應取消 [**對應**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map)來完成 / [\*\*\*\*](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap)。</span><span class="sxs-lookup"><span data-stu-id="b540e-205">CPU access to a resource is typically done through [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map)/[**Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b540e-206">相關主題</span><span class="sxs-lookup"><span data-stu-id="b540e-206">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b540e-207">資源系結</span><span class="sxs-lookup"><span data-stu-id="b540e-207">Resource Binding</span></span>](resource-binding.md)
</dt> </dl>

 

 




