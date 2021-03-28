---
title: '子資源 (Direct3D 11 圖形) '
description: 本主題說明紋理子資源或資源的部分。
ms.assetid: 57444cb5-6c8b-4dac-8d6b-ca2b45eafac9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a432dbfbcbf08c4359ea436a3e8fa025c801d12
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104024396"
---
# <a name="subresources-direct3d-11-graphics"></a><span data-ttu-id="20f91-103">子資源 (Direct3D 11 圖形) </span><span class="sxs-lookup"><span data-stu-id="20f91-103">Subresources (Direct3D 11 Graphics)</span></span>

<span data-ttu-id="20f91-104">本主題說明紋理子資源或資源的部分。</span><span class="sxs-lookup"><span data-stu-id="20f91-104">This topic describes texture subresources, or portions of a resource.</span></span>

<span data-ttu-id="20f91-105">Direct3D 可以參考整個資源，或參考資源的子集。</span><span class="sxs-lookup"><span data-stu-id="20f91-105">Direct3D can reference an entire resource or it can reference subsets of a resource.</span></span> <span data-ttu-id="20f91-106">子資源這個詞彙指的是資源的子集。</span><span class="sxs-lookup"><span data-stu-id="20f91-106">The term subresource refers to a subset of a resource.</span></span>

<span data-ttu-id="20f91-107">緩衝區定義為單一的子資源。</span><span class="sxs-lookup"><span data-stu-id="20f91-107">A buffer is defined as a single subresource.</span></span> <span data-ttu-id="20f91-108">紋理稍微複雜一點，因為有數種不同的材質類型 (1D、2D 等等，) 某些支援 mipmap 層級和/或材質陣列的部分。</span><span class="sxs-lookup"><span data-stu-id="20f91-108">Textures are a little more complicated because there are several different texture types (1D, 2D, etc.) some of which support mipmap levels and/or texture arrays.</span></span> <span data-ttu-id="20f91-109">從最簡單的案例開始，1D 紋理定義為單一子資源，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="20f91-109">Beginning with the simplest case, a 1D texture is defined as a single subresource, as shown in the following illustration.</span></span>

![1D 紋理的圖例](images/d3d10-1d-texture.png)

<span data-ttu-id="20f91-111">這表示組成 1D 紋理的紋理陣列包含在單一子資源中。</span><span class="sxs-lookup"><span data-stu-id="20f91-111">This means that the array of texels that make up a 1D texture are contained in a single subresource.</span></span>

<span data-ttu-id="20f91-112">如果您展開有三個 mipmap 層級的一維紋理，就可以像下圖一樣視覺化。</span><span class="sxs-lookup"><span data-stu-id="20f91-112">If you expand a 1D texture with three mipmap levels, it can be visualized like the following illustration.</span></span>

![包含三個 mipmap 層級的1d 材質圖例](images/d3d10-resource-texture1d.png)

<span data-ttu-id="20f91-114">將此視為由三個子資源組成的單一材質。</span><span class="sxs-lookup"><span data-stu-id="20f91-114">Think of this as a single texture that is made up of three subresources.</span></span> <span data-ttu-id="20f91-115">您可以使用單一材質的詳細層級 (」 LOD) 來編制 subresource 索引。</span><span class="sxs-lookup"><span data-stu-id="20f91-115">A subresource can be indexed using the level-of-detail (LOD) for a single texture.</span></span> <span data-ttu-id="20f91-116">使用紋理的陣列時，存取特定的 subresource 需要」 LOD 和特定的材質。</span><span class="sxs-lookup"><span data-stu-id="20f91-116">When using an array of textures, accessing a particular subresource requires both the LOD and the particular texture.</span></span> <span data-ttu-id="20f91-117">此外，API 會將這兩項資訊合併為單一以零為基礎的 subresource 索引，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="20f91-117">Alternately, the API combines these two pieces of information into a single zero-based subresource index, as shown in the following illustration.</span></span>

![以零起始的子資源索引的圖例](images/d3d10-resource-texture1darray-sub-indexing.png)

## <a name="selecting-subresources"></a><span data-ttu-id="20f91-119">選取子資源</span><span class="sxs-lookup"><span data-stu-id="20f91-119">Selecting Subresources</span></span>

<span data-ttu-id="20f91-120">某些 Api 會存取整個資源 (例如 [**>id3d11devicecoNtext：： CopyResource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) 方法) ，其他人會存取一部分的資源 (例如 [**>id3d11devicecoNtext：： UpdateSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) 方法或 [**>id3d11devicecoNtext：： CopySubresourceRegion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) 方法) 。</span><span class="sxs-lookup"><span data-stu-id="20f91-120">Some APIs access an entire resource (for example the [**ID3D11DeviceContext::CopyResource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) method), others access a portion of a resource (for example the [**ID3D11DeviceContext::UpdateSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) method or the [**ID3D11DeviceContext::CopySubresourceRegion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) method).</span></span> <span data-ttu-id="20f91-121">存取某個資源部分的方法通常會使用 view description (例如 [**D3D11 \_ TEX2D \_ ARRAY \_ DSV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_dsv) structure) 來指定要存取的子資源。</span><span class="sxs-lookup"><span data-stu-id="20f91-121">The methods that access a portion of a resource generally use a view description (such as the [**D3D11\_TEX2D\_ARRAY\_DSV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_dsv) structure) to specify the subresources to access.</span></span>

<span data-ttu-id="20f91-122">下列各節中的圖例顯示存取材質陣列時，視圖描述所使用的詞彙。</span><span class="sxs-lookup"><span data-stu-id="20f91-122">The illustrations in the following sections show the terms used by a view description when accessing an array of textures.</span></span>

### <a name="array-slice"></a><span data-ttu-id="20f91-123">陣列切片</span><span class="sxs-lookup"><span data-stu-id="20f91-123">Array Slice</span></span>

<span data-ttu-id="20f91-124">根據紋理的陣列，每個使用 mipmap 的材質（ *陣列* 配量 (以白色矩形表示）) 包含一個材質和其所有的子資源，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="20f91-124">Given an array of textures, each texture with mipmaps, an *array slice* (represented by the white rectangle) includes one texture and all of its subresources, as shown in the following illustration.</span></span>

![陣列配量的圖例](images/d3d10-resource-array-slice.png)

### <a name="mip-slice"></a><span data-ttu-id="20f91-126">Mip 切片</span><span class="sxs-lookup"><span data-stu-id="20f91-126">Mip Slice</span></span>

<span data-ttu-id="20f91-127"> (由白色矩形表示的 *mip* 配量，) 為數組中的每個材質包含一個 mipmap 層級，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="20f91-127">A *mip slice* (represented by the white rectangle) includes one mipmap level for every texture in an array, as shown in the following illustration.</span></span>

![mip 配量的圖例](images/d3d10-resource-mip-slice.png)

### <a name="selecting-a-single-subresource"></a><span data-ttu-id="20f91-129">選取單一子資源</span><span class="sxs-lookup"><span data-stu-id="20f91-129">Selecting a Single Subresource</span></span>

<span data-ttu-id="20f91-130">您可以使用這兩種切片來選擇單一子資源，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="20f91-130">You can use these two types of slices to choose a single subresource, as shown in the following illustration.</span></span>

![使用陣列配量和 mip 配量來選擇 subresource 的圖例](images/d3d10-resource-subresources-1.png)

### <a name="selecting-multiple-subresources"></a><span data-ttu-id="20f91-132">選取多個子資源</span><span class="sxs-lookup"><span data-stu-id="20f91-132">Selecting Multiple Subresources</span></span>

<span data-ttu-id="20f91-133">或者，您可以使用這兩種類型的配量來搭配 mipmap 層級和/或紋理數目，以選擇多個子資源，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="20f91-133">Or you can use these two types of slices with the number of mipmap levels and/or number of textures, to choose multiple subresources, as shown in the following illustration.</span></span>

![選擇多個 subresource 的圖例](images/d3d10-resource-subresources-2.png)

> [!Note]  
> <span data-ttu-id="20f91-135">轉譯 [**目標視圖**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_render_target_view_desc) 只能使用單一 subresource 或 mip 配量，且不能包含來自一個以上 mip 配量的子資源。</span><span class="sxs-lookup"><span data-stu-id="20f91-135">A [**render-target view**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_render_target_view_desc) can only use a single subresource or mip slice and cannot include subresources from more than one mip slice.</span></span> <span data-ttu-id="20f91-136">也就是說，轉譯目標視圖中的每個材質都必須是相同的大小。</span><span class="sxs-lookup"><span data-stu-id="20f91-136">That is, every texture in a render-target view must be the same size.</span></span> <span data-ttu-id="20f91-137">[**著色器資源檢視**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc)可以選取子資源的任何矩形區域，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="20f91-137">A [**shader-resource view**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc) can select any rectangular region of subresources, as shown in the figure.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="20f91-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="20f91-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20f91-139">資源</span><span class="sxs-lookup"><span data-stu-id="20f91-139">Resources</span></span>](overviews-direct3d-11-resources.md)
</dt> </dl>

 

 




