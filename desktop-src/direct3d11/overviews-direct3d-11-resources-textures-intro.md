---
title: Direct3D 11 中的材質簡介
description: 紋理資源是設計來儲存紋素的結構化資料集合。
ms.assetid: d745093e-2d51-4d45-a88a-caa0ca58b2ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71fcafdfb9caf53a27e60956c8182ae3ef95008e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840307"
---
# <a name="introduction-to-textures-in-direct3d-11"></a><span data-ttu-id="d4110-103">Direct3D 11 中的材質簡介</span><span class="sxs-lookup"><span data-stu-id="d4110-103">Introduction To Textures in Direct3D 11</span></span>

<span data-ttu-id="d4110-104">紋理資源是設計來儲存紋素的結構化資料集合。</span><span class="sxs-lookup"><span data-stu-id="d4110-104">A texture resource is a structured collection of data designed to store texels.</span></span> <span data-ttu-id="d4110-105">紋素代表管線可讀取或寫入的最小紋理單位。</span><span class="sxs-lookup"><span data-stu-id="d4110-105">A texel represents the smallest unit of a texture that can be read or written to by the pipeline.</span></span> <span data-ttu-id="d4110-106">和緩衝區不同的是，紋理可依紋理樣本篩選，由著色器單位讀取。</span><span class="sxs-lookup"><span data-stu-id="d4110-106">Unlike buffers, textures can be filtered by texture samplers as they are read by shader units.</span></span> <span data-ttu-id="d4110-107">紋理類型會影響篩選紋理的方式。</span><span class="sxs-lookup"><span data-stu-id="d4110-107">The type of texture impacts how the texture is filtered.</span></span> <span data-ttu-id="d4110-108">每個材質都包含1至4個元件，以 DXGI 格式列舉所定義的其中一個 DXGI 格式來排列 \_ 。</span><span class="sxs-lookup"><span data-stu-id="d4110-108">Each texel contains 1 to 4 components, arranged in one of the DXGI formats defined by the DXGI\_FORMAT enumeration.</span></span>

<span data-ttu-id="d4110-109">建立具已知大小的紋理為結構化資源。</span><span class="sxs-lookup"><span data-stu-id="d4110-109">Textures are created as a structured resource with a known size.</span></span> <span data-ttu-id="d4110-110">不過，每個紋理在建立資源之後可能有型別或無型別，只要當紋理與管線繫結時使用檢視完全指定型別。</span><span class="sxs-lookup"><span data-stu-id="d4110-110">However, each texture may be typed or typeless when the resource is created as long as the type is fully specified using a view when the texture is bound to the pipeline.</span></span>

## <a name="texture-types"></a><span data-ttu-id="d4110-111">材質類型</span><span class="sxs-lookup"><span data-stu-id="d4110-111">Texture Types</span></span>

<span data-ttu-id="d4110-112">有數種紋理類型︰1D、2D、3D，每一個都可使用或不使用 Mipmap 建立。</span><span class="sxs-lookup"><span data-stu-id="d4110-112">There are several types of textures: 1D, 2D, 3D, each of which can be created with or without mipmaps.</span></span> <span data-ttu-id="d4110-113">Direct3D 11 也支援材質陣列和多重取樣材質。</span><span class="sxs-lookup"><span data-stu-id="d4110-113">Direct3D 11 also supports texture arrays and multisampled textures.</span></span>

-   [<span data-ttu-id="d4110-114">1D 紋理</span><span class="sxs-lookup"><span data-stu-id="d4110-114">1D Textures</span></span>](#1d-textures)
-   [<span data-ttu-id="d4110-115">1D 紋理陣列</span><span class="sxs-lookup"><span data-stu-id="d4110-115">1D Texture Arrays</span></span>](#1d-texture-arrays)
-   [<span data-ttu-id="d4110-116">2D 材質和2D 材質陣列</span><span class="sxs-lookup"><span data-stu-id="d4110-116">2D Textures and 2D Texture Arrays</span></span>](#2d-textures-and-2d-texture-arrays)
-   [<span data-ttu-id="d4110-117">3D 紋理</span><span class="sxs-lookup"><span data-stu-id="d4110-117">3D Textures</span></span>](#3d-textures)

### <a name="1d-textures"></a><span data-ttu-id="d4110-118">1D 紋理</span><span class="sxs-lookup"><span data-stu-id="d4110-118">1D Textures</span></span>

<span data-ttu-id="d4110-119">最簡單形式的 1D 紋理所包含的紋理資料，可以使用單一紋理座標處理，它可以視覺化為紋素陣列，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="d4110-119">A 1D texture in its simplest form contains texture data that can be addressed with a single texture coordinate; it can be visualized as an array of texels, as shown in the following illustration.</span></span> <span data-ttu-id="d4110-120">1D 紋理會以 [**ID3D11Texture1D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture1d) 介面表示。</span><span class="sxs-lookup"><span data-stu-id="d4110-120">1D textures are represented by the [**ID3D11Texture1D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture1d) interface.</span></span>

![1D 紋理的圖例](images/d3d10-1d-texture.png)

<span data-ttu-id="d4110-122">每個紋素根據所儲存的資料格式包含許多色彩元件。</span><span class="sxs-lookup"><span data-stu-id="d4110-122">Each texel contains a number of color components depending on the format of the data stored.</span></span> <span data-ttu-id="d4110-123">增加更多複雜度，您可以使用 Mipmap 層次建立 1D 紋理，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="d4110-123">Adding more complexity, you can create a 1D texture with mipmap levels, as shown in the following illustration.</span></span>

![具有 Mipmap 層次之 1D 紋理的圖例](images/d3d10-resource-texture1d.png)

<span data-ttu-id="d4110-125">Mipmap 層次是比上層小二的 n 次方的紋理。</span><span class="sxs-lookup"><span data-stu-id="d4110-125">A mipmap level is a texture that is a power-of-two smaller than the level above it.</span></span> <span data-ttu-id="d4110-126">最上層包含大部分的細節，每個後續的層次較小。</span><span class="sxs-lookup"><span data-stu-id="d4110-126">The topmost level contains the most detail, each subsequent level is smaller.</span></span> <span data-ttu-id="d4110-127">對於 1D Mipmap，最小層級包含一個紋素。</span><span class="sxs-lookup"><span data-stu-id="d4110-127">For a 1D mipmap, the smallest level contains one texel.</span></span> <span data-ttu-id="d4110-128">此外，MIP 層級一律降至 1:1。</span><span class="sxs-lookup"><span data-stu-id="d4110-128">Furthermore, MIP levels always reduce down to 1:1.</span></span> <span data-ttu-id="d4110-129">當專為特別尺寸紋理產生 Mipmap， 下一個較低層次一律為均勻大小 (除了最低層到達 1 以外)。</span><span class="sxs-lookup"><span data-stu-id="d4110-129">When mipmaps are generated for an odd sized texture, the next lower level is always even size (except when the lowest level reaches 1).</span></span> <span data-ttu-id="d4110-130">例如，圖表顯示 5x1 紋理，其下一個最低層為 2x1 紋理，其下一個 (和上一個) MIP 層是 1x1 大小的紋理。</span><span class="sxs-lookup"><span data-stu-id="d4110-130">For example, the diagram illustrates a 5x1 texture whose next lowest level is a 2x1 texture, whose next (and last) mip level is a 1x1 sized texture.</span></span> <span data-ttu-id="d4110-131">由稱為 LOD (細節層次) 的索引識別的層次，會在呈現不是那麼靠近相機的幾何圖形時，用於存取較小的紋理。</span><span class="sxs-lookup"><span data-stu-id="d4110-131">The levels are identified by an index called a LOD (level-of-detail) which is used to access the smaller texture when rendering geometry that is not as close to the camera.</span></span>

### <a name="1d-texture-arrays"></a><span data-ttu-id="d4110-132">1D 紋理陣列</span><span class="sxs-lookup"><span data-stu-id="d4110-132">1D Texture Arrays</span></span>

<span data-ttu-id="d4110-133">Direct3D 11 也支援材質的陣列。</span><span class="sxs-lookup"><span data-stu-id="d4110-133">Direct3D 11 also supports arrays of textures.</span></span> <span data-ttu-id="d4110-134">一維紋理陣列也會以 [**ID3D11Texture1D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture1d) 介面表示。</span><span class="sxs-lookup"><span data-stu-id="d4110-134">A 1D texture array is also represented by the [**ID3D11Texture1D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture1d) interface.</span></span> <span data-ttu-id="d4110-135">1D 紋理陣列概念上看起來像下圖。</span><span class="sxs-lookup"><span data-stu-id="d4110-135">An array of 1D textures looks conceptually like the following illustration.</span></span>

![1d 紋理陣列的圖例](images/d3d10-resource-texture1darray.png)

<span data-ttu-id="d4110-137">這個紋理陣列包含三種紋理。</span><span class="sxs-lookup"><span data-stu-id="d4110-137">This texture array contains three textures.</span></span> <span data-ttu-id="d4110-138">三個紋理的每一個都具有紋理寬度 5 (也就是第一層的元素數目)。</span><span class="sxs-lookup"><span data-stu-id="d4110-138">Each of the three textures has a texture width of 5 (which is the number of elements in the first layer).</span></span> <span data-ttu-id="d4110-139">每個紋理也包含 3 層 Mipmap。</span><span class="sxs-lookup"><span data-stu-id="d4110-139">Each texture also contains a 3 layer mipmap.</span></span>

<span data-ttu-id="d4110-140">在 Direct3D 中的所有紋理陣列都是同質紋理陣列，這表示紋理陣列中的每種紋理必須有相同資料格式和大小 (包括紋理寬度和 Mipmap 層次數目)。</span><span class="sxs-lookup"><span data-stu-id="d4110-140">All texture arrays in Direct3D are a homogeneous array of textures; this means that every texture in a texture array must have the same data format and size (including texture width and number of mipmap levels).</span></span> <span data-ttu-id="d4110-141">只要每一個紋理陣列中的所有紋理大小都相符，您可以建立不同大小的紋理陣列。</span><span class="sxs-lookup"><span data-stu-id="d4110-141">You may create texture arrays of different sizes, as long as all the textures in each array match in size.</span></span>

### <a name="2d-textures-and-2d-texture-arrays"></a><span data-ttu-id="d4110-142">2D 紋理和 2D 紋理陣列</span><span class="sxs-lookup"><span data-stu-id="d4110-142">2D Textures and 2D Texture Arrays</span></span>

<span data-ttu-id="d4110-143">Texture2D 資源包含 2D 紋格。</span><span class="sxs-lookup"><span data-stu-id="d4110-143">A Texture2D resource contains a 2D grid of texels.</span></span> <span data-ttu-id="d4110-144">每個紋素是由 u、v 向量定位。</span><span class="sxs-lookup"><span data-stu-id="d4110-144">Each texel is addressable by a u, v vector.</span></span> <span data-ttu-id="d4110-145">因為是紋理資源，它可能包含 mipmap 層次和子資源。</span><span class="sxs-lookup"><span data-stu-id="d4110-145">Since it is a texture resource, it may contain mipmap levels, and subresources.</span></span> <span data-ttu-id="d4110-146">2D 紋理會以 [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) 介面表示。</span><span class="sxs-lookup"><span data-stu-id="d4110-146">2D textures are represented by the [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) interface.</span></span> <span data-ttu-id="d4110-147">完全填充的 2D 紋理資源看起來如下圖。</span><span class="sxs-lookup"><span data-stu-id="d4110-147">A fully populated 2D texture resource looks like the following illustration.</span></span>

![2D 紋理資源的圖例](images/d3d10-resource-texture2d.png)

<span data-ttu-id="d4110-149">這個紋理資源包含具三個 Mipmap 層次的單一 3x5 紋理。</span><span class="sxs-lookup"><span data-stu-id="d4110-149">This texture resource contains a single 3x5 texture with three mipmap levels.</span></span>

<span data-ttu-id="d4110-150">2D 紋理陣列資源是同質 2D 紋理陣列，也就是每個紋理都有相同的資料格式和尺寸 (包括 Mipmap 層次)。</span><span class="sxs-lookup"><span data-stu-id="d4110-150">A 2D texture array resource is a homogeneous array of 2D textures; that is, each texture has the same data format and dimensions (including mipmap levels).</span></span> <span data-ttu-id="d4110-151">2D 材質陣列也會以 [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) 介面表示。</span><span class="sxs-lookup"><span data-stu-id="d4110-151">A 2D texture array is also represented by the [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) interface.</span></span> <span data-ttu-id="d4110-152">它有類似 1D 紋理的版面配置，現在包含 2D 資料的紋理除外，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="d4110-152">It has a similar layout as the 1D texture array except that the textures now contain 2D data, as shown in the following illustration.</span></span>

![2d 材質陣列的圖例](images/d3d10-resource-texture2darray.png)

<span data-ttu-id="d4110-154">這個紋理包含三個紋理，每個紋理為 3x5 含兩個 Mipmap 層次。</span><span class="sxs-lookup"><span data-stu-id="d4110-154">This texture array contains three textures; each texture is 3x5 with two mipmap levels.</span></span>

### <a name="using-a-2d-texture-array-as-a-texture-cube"></a><span data-ttu-id="d4110-155">使用 2D 紋理陣列做為立體紋理</span><span class="sxs-lookup"><span data-stu-id="d4110-155">Using a 2D Texture Array as a Texture Cube</span></span>

<span data-ttu-id="d4110-156">紋理立方體是包含 6 個紋理的 2D 紋理陣列，每個立方體表面一個紋理。</span><span class="sxs-lookup"><span data-stu-id="d4110-156">A texture cube is a 2D texture array that contains 6 textures, one for each face of the cube.</span></span> <span data-ttu-id="d4110-157">完全填充的紋理立方體如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="d4110-157">A fully populated texture cube looks like the following illustration.</span></span>

![代表材質 cube 之2d 材質陣列的圖例](images/d3d10-resource-texturecube.png)

<span data-ttu-id="d4110-159">包含 6 個紋理的 2D 紋理陣列，在使用立方體紋理視圖結合管線後，可使用立方體內建功能從著色器內讀取。</span><span class="sxs-lookup"><span data-stu-id="d4110-159">A 2D texture array that contains 6 textures may be read from within shaders with the cube map intrinsic functions, after they are bound to the pipeline with a cube-texture view.</span></span> <span data-ttu-id="d4110-160">使用從紋理立方體中心指出的 3D 向量，從著色器處理紋理。</span><span class="sxs-lookup"><span data-stu-id="d4110-160">Texture cubes are addressed from the shader with a 3D vector pointing out from the center of the texture cube.</span></span>

> [!Note]  
> <span data-ttu-id="d4110-161">您使用 [**10 個 \_ 功能等級**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) （含）以上建立的裝置可以支援材質 cube 的陣列，其中紋理數目等於陣列中的材質 cube 數目（以六為限）。</span><span class="sxs-lookup"><span data-stu-id="d4110-161">Devices that you create with [**10\_1 feature level**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) and above can support arrays of texture cubes in which the number of textures is equal to the number of texture cubes in an array times six.</span></span> <span data-ttu-id="d4110-162">您使用 [**10 個 \_ 功能層級**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) 建立的裝置僅支援六個臉部的單一紋理 cube。</span><span class="sxs-lookup"><span data-stu-id="d4110-162">Devices that you create with [**10\_0 feature level**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) support only a single texture cube of six faces.</span></span> <span data-ttu-id="d4110-163">此外，Direct3D 11 不支援部分 cubemaps。</span><span class="sxs-lookup"><span data-stu-id="d4110-163">Also, Direct3D 11 does not support partial cubemaps.</span></span>

 

### <a name="3d-textures"></a><span data-ttu-id="d4110-164">3D 紋理</span><span class="sxs-lookup"><span data-stu-id="d4110-164">3D Textures</span></span>

<span data-ttu-id="d4110-165">3D 紋理資源 (也稱為容體紋理) 包含 3D 紋理元素量。</span><span class="sxs-lookup"><span data-stu-id="d4110-165">A 3D texture resource (also known as a volume texture) contains a 3D volume of texels.</span></span> <span data-ttu-id="d4110-166">因為是紋理資源，所以可會包含 mipmap 層次。</span><span class="sxs-lookup"><span data-stu-id="d4110-166">Because it is a texture resource, it may contain mipmap levels.</span></span> <span data-ttu-id="d4110-167">3D 紋理會以 [**ID3D11Texture3D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture3d) 介面表示。</span><span class="sxs-lookup"><span data-stu-id="d4110-167">3D textures are represented by the [**ID3D11Texture3D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture3d) interface.</span></span> <span data-ttu-id="d4110-168">完全填充的 3D 紋理外觀如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="d4110-168">A fully populated 3D texture looks like the following illustration.</span></span>

![3D 紋理資源的圖例](images/d3d10-resource-texture3d.png)

<span data-ttu-id="d4110-170">3D 紋理 Mipmap 切片繫結為描繪目標輸出 (描繪目標視圖) 時，3D 紋理行為等同於具 n 切片的 2D 紋理陣列。</span><span class="sxs-lookup"><span data-stu-id="d4110-170">When a 3D texture mipmap slice is bound as a render target output (with a render-target view), the 3D texture behaves identically to a 2D texture array with n slices.</span></span> <span data-ttu-id="d4110-171">您可以透過將輸出資料的純量元件宣告為 SV RenderTargetArrayIndex 系統值，從 [幾何著色器] 階段選擇特定轉譯配量 \_ 。</span><span class="sxs-lookup"><span data-stu-id="d4110-171">The particular render slice is chosen from the geometry-shader stage, by declaring a scalar component of output data as the SV\_RenderTargetArrayIndex system-value.</span></span>

<span data-ttu-id="d4110-172">沒有 3D 紋理陣列概念，因此 3D 紋理子資源是單一 Mipmap 層次。</span><span class="sxs-lookup"><span data-stu-id="d4110-172">There is no concept of a 3D texture array; therefore a 3D texture subresource is a single mipmap level.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d4110-173">相關主題</span><span class="sxs-lookup"><span data-stu-id="d4110-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4110-174">紋理</span><span class="sxs-lookup"><span data-stu-id="d4110-174">Textures</span></span>](overviews-direct3d-11-resources-textures.md)
</dt> </dl>

 

 




