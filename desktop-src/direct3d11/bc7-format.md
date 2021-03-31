---
title: BC7 格式
description: BC7 格式是用於高品質 RGB 和 RGBA 資料壓縮的紋理壓縮格式。
ms.assetid: DF333106-293E-4B3E-A1EB-B0BF0ADBAC72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b9b64c3d4a8b5e960077a9f33de82ff08cd4bbc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382458"
---
# <a name="bc7-format"></a><span data-ttu-id="a62e4-103">BC7 格式</span><span class="sxs-lookup"><span data-stu-id="a62e4-103">BC7 Format</span></span>

<span data-ttu-id="a62e4-104">BC7 格式是用於高品質 RGB 和 RGBA 資料壓縮的紋理壓縮格式。</span><span class="sxs-lookup"><span data-stu-id="a62e4-104">The BC7 format is a texture compression format used for high-quality compression of RGB and RGBA data.</span></span>

-   [<span data-ttu-id="a62e4-105">關於 BC7/DXGI \_ 格式 \_ BC7</span><span class="sxs-lookup"><span data-stu-id="a62e4-105">About BC7/DXGI\_FORMAT\_BC7</span></span>](/windows)
-   [<span data-ttu-id="a62e4-106">BC7 執行</span><span class="sxs-lookup"><span data-stu-id="a62e4-106">BC7 Implementation</span></span>](#bc7-implementation)
-   [<span data-ttu-id="a62e4-107">解碼 BC7 格式</span><span class="sxs-lookup"><span data-stu-id="a62e4-107">Decoding the BC7 Format</span></span>](#decoding-the-bc7-format)
-   [<span data-ttu-id="a62e4-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="a62e4-108">Related topics</span></span>](#related-topics)

<span data-ttu-id="a62e4-109">如需 BC7 格式的區塊模式資訊，請參閱 [BC7 格式模式參考](bc7-format-mode-reference.md) (英文)。</span><span class="sxs-lookup"><span data-stu-id="a62e4-109">For info about the block modes of the BC7 format, see [BC7 Format Mode Reference](bc7-format-mode-reference.md).</span></span>

## <a name="about-bc7dxgi_format_bc7"></a><span data-ttu-id="a62e4-110">關於 BC7/DXGI \_ 格式 \_ BC7</span><span class="sxs-lookup"><span data-stu-id="a62e4-110">About BC7/DXGI\_FORMAT\_BC7</span></span>

<span data-ttu-id="a62e4-111">BC7 是由下列 DXGI \_ 格式列舉值所指定：</span><span class="sxs-lookup"><span data-stu-id="a62e4-111">BC7 is specified by the following DXGI\_FORMAT enumeration values:</span></span>

-   <span data-ttu-id="a62e4-112">**DXGI \_格式化 \_ BC7 \_** 無別。</span><span class="sxs-lookup"><span data-stu-id="a62e4-112">**DXGI\_FORMAT\_BC7\_TYPELESS**.</span></span>
-   <span data-ttu-id="a62e4-113">**DXGI \_FORMAT \_ BC7 \_ UNORM**。</span><span class="sxs-lookup"><span data-stu-id="a62e4-113">**DXGI\_FORMAT\_BC7\_UNORM**.</span></span>
-   <span data-ttu-id="a62e4-114">**DXGI \_FORMAT \_ BC7 \_ UNORM \_ SRGB**。</span><span class="sxs-lookup"><span data-stu-id="a62e4-114">**DXGI\_FORMAT\_BC7\_UNORM\_SRGB**.</span></span>

<span data-ttu-id="a62e4-115">BC7 格式可用於 [Texture2D](/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures) (包括陣列)、Texture3D，或 TextureCube (包括陣列) 紋理資源。</span><span class="sxs-lookup"><span data-stu-id="a62e4-115">The BC7 format can be used for [Texture2D](/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures) (including arrays), Texture3D, or TextureCube (including arrays) texture resources.</span></span> <span data-ttu-id="a62e4-116">同樣地，此格式適用於任何與這些資源建立關聯的 Mipmap 表面。</span><span class="sxs-lookup"><span data-stu-id="a62e4-116">Similarly, this format applies to any MIP-map surfaces associated with these resources.</span></span>

<span data-ttu-id="a62e4-117">BC7 使用固定的 16 位元組 (128 位元) 區塊大小，以及固定之 4x4 材質的磚大小。</span><span class="sxs-lookup"><span data-stu-id="a62e4-117">BC7 uses a fixed block size of 16 bytes (128 bits) and a fixed tile size of 4x4 texels.</span></span> <span data-ttu-id="a62e4-118">與之前的 BC 格式一樣，大於支援之磚大小 (4x4) 的紋理影像，程式會使用多重區塊對其進行壓縮。</span><span class="sxs-lookup"><span data-stu-id="a62e4-118">As with previous BC formats, texture images larger than the supported tile size (4x4) are compressed by using multiple blocks.</span></span> <span data-ttu-id="a62e4-119">此位址身分識別也適用於 3D 圖片和 Mipmap、立方體貼圖，以及紋理陣列。</span><span class="sxs-lookup"><span data-stu-id="a62e4-119">This addressing identity also applies to three-dimensional images and MIP-maps, cubemaps, and texture arrays.</span></span> <span data-ttu-id="a62e4-120">所有影像磚都必須格式相同。</span><span class="sxs-lookup"><span data-stu-id="a62e4-120">All image tiles must be of the same format.</span></span>

<span data-ttu-id="a62e4-121">BC7 壓縮三通道 (RGB) 和四通道 (RGBA) 定點資料影像。</span><span class="sxs-lookup"><span data-stu-id="a62e4-121">BC7 compresses both three-channel (RGB) and four-channel (RGBA) fixed-point data images.</span></span> <span data-ttu-id="a62e4-122">一般而言，來源資料的每個色彩元件 (通道) 為 8 位元，但此格式可將來源資料的每個色彩元件編碼為較高位元。</span><span class="sxs-lookup"><span data-stu-id="a62e4-122">Typically, source data is 8 bits per color component (channel), although the format is capable of encoding source data with higher bits per color component.</span></span> <span data-ttu-id="a62e4-123">所有影像磚都必須格式相同。</span><span class="sxs-lookup"><span data-stu-id="a62e4-123">All image tiles must be of the same format.</span></span>

<span data-ttu-id="a62e4-124">BC7 解碼器在套用紋理篩選之前，會先執行解壓縮。</span><span class="sxs-lookup"><span data-stu-id="a62e4-124">The BC7 decoder performs decompression before texture filtering is applied.</span></span>

<span data-ttu-id="a62e4-125">BC7 解壓縮硬體必須為位元精確。也就是硬體傳回的結果，必須和本文中所述解碼器傳回的結果相同。</span><span class="sxs-lookup"><span data-stu-id="a62e4-125">BC7 decompression hardware must be bit accurate; that is, the hardware must return results that are identical to the results returned by the decoder described in this document.</span></span>

## <a name="bc7-implementation"></a><span data-ttu-id="a62e4-126">BC7 實作</span><span class="sxs-lookup"><span data-stu-id="a62e4-126">BC7 Implementation</span></span>

<span data-ttu-id="a62e4-127">BC7 實作可以指定 8 種模式中的一種，並具有在 16 位元組 (128 位元) 區塊之最低有效位元中指定的模式。</span><span class="sxs-lookup"><span data-stu-id="a62e4-127">A BC7 implementation can specify one of 8 modes, with the mode specified in the least significant bit of the 16 byte (128 bit) block.</span></span> <span data-ttu-id="a62e4-128">該模式的編碼，是由 0 或更多具有 0 值的位元，最後再加上一個 1 而成。</span><span class="sxs-lookup"><span data-stu-id="a62e4-128">The mode is encoded by zero or more bits with a value of 0 followed by a 1.</span></span>

<span data-ttu-id="a62e4-129">BC7 區塊可能包含多個端點配對。</span><span class="sxs-lookup"><span data-stu-id="a62e4-129">A BC7 block can contain multiple endpoint pairs.</span></span> <span data-ttu-id="a62e4-130">基於本檔的目的，對應至端點配對的一組索引可能稱為「子集」。</span><span class="sxs-lookup"><span data-stu-id="a62e4-130">For the purposes of this documentation, the set of indices that correspond to an endpoint pair may be referred to as a "subset."</span></span> <span data-ttu-id="a62e4-131">此外，在某些區塊模式中，端點標記法的編碼方式，也就是此檔的用途，也就是所謂的「RBGP」，其中「P」位代表端點之色彩元件的共用最少位。</span><span class="sxs-lookup"><span data-stu-id="a62e4-131">Also, in some block modes, the endpoint representation is encoded in a form that -- again, for the purposes of this documentation -- shall be referred to as "RBGP," where the "P" bit represents a shared least significant bit for the color components of the endpoint.</span></span> <span data-ttu-id="a62e4-132">例如，如果格式的端點表示法為 "RGB 5.5.5.1"，則端點會解譯為 RGB 6.6.6 值，其中 P 位元的狀態定義了每個元件的最低有效位元。</span><span class="sxs-lookup"><span data-stu-id="a62e4-132">For example, if the endpoint representation for the format is "RGB 5.5.5.1," then the endpoint is interpreted as an RGB 6.6.6 value, where the state of the P-bit defines the least significant bit of each component.</span></span> <span data-ttu-id="a62e4-133">同樣地，對於具有 Alpha 色板的來源資料，如果格式的表示為 "RGBAP 5.5.5.5.1"，則端點會 interepreted 為 RGBA 6.6.6.6。</span><span class="sxs-lookup"><span data-stu-id="a62e4-133">Similarly, for source data with an alpha channel, if the representation for the format is "RGBAP 5.5.5.5.1," then the endpoint is interepreted as RGBA 6.6.6.6.</span></span> <span data-ttu-id="a62e4-134">依區塊模式而定，您能為子集的兩個端點 (每一子集 2 個 P 位元) 個別指定共用最低有效位元，或讓子集的兩個端點 (每一子集 1 個 P 位元) 共用。</span><span class="sxs-lookup"><span data-stu-id="a62e4-134">Depending on the block mode, you can specify the shared least significant bit for either both endpoints of a subset individually (2 P-bits per subset), or shared between endpoints of a subset (1 P-bit per subset).</span></span>

<span data-ttu-id="a62e4-135">對於沒有明確編碼 Alpha 元件的 BC7 區塊，BC7 區塊包含模式位元、分割位元、壓縮端點、壓縮索引，和一個選擇性的 P 位元。</span><span class="sxs-lookup"><span data-stu-id="a62e4-135">For BC7 blocks that don't explicitly encode the alpha component, a BC7 block consists of mode bits, partition bits, compressed endpoints, compressed indices, and an optional P-bit.</span></span> <span data-ttu-id="a62e4-136">在這些區塊中，端點具有僅限 RGB 的表示法，且 Alpha 元件為來源資料中的所有材質都解碼為 1.0。</span><span class="sxs-lookup"><span data-stu-id="a62e4-136">In these blocks the endpoints have an RGB-only representation and the alpha component is decoded as 1.0 for all texels in the source data.</span></span>

<span data-ttu-id="a62e4-137">對於具有合併色彩和 Alpha 元件的 BC7 區塊，一個區塊包含模式位元、壓縮端點、壓縮索引，以及選用的分割位元和一個 P 位元。</span><span class="sxs-lookup"><span data-stu-id="a62e4-137">For BC7 blocks that have combined color and alpha components, a block consists of mode bits, compressed endpoints, compressed indices, and optional partition bits and a P-bit.</span></span> <span data-ttu-id="a62e4-138">在這些區塊中，端點色彩以 RGBA 格式表示，而且會插入 Alpha 元件值和色彩元件值。</span><span class="sxs-lookup"><span data-stu-id="a62e4-138">In these blocks, the endpoint colors are expressed in RGBA format, and alpha component values are interpolated alongside the color component values.</span></span>

<span data-ttu-id="a62e4-139">對於具有不同色彩與 Alpha 元件的 BC7 區塊，一個區塊包含模式位元、旋轉位元、壓縮端點、壓縮索引，和一個選擇性的索引選取器位元。</span><span class="sxs-lookup"><span data-stu-id="a62e4-139">For BC7 blocks that have separate color and alpha components, a block consists of mode bits, rotation bits, compressed endpoints, compressed indices, and an optional index selector bit.</span></span> <span data-ttu-id="a62e4-140">這些區塊具有有效的 RGB 向量 \[ R、G、B \] 和純量 Alpha 通道，而且會 \[ 另外進行 \] 編碼。</span><span class="sxs-lookup"><span data-stu-id="a62e4-140">These blocks have an effective RGB vector \[R, G, B\] and a scalar alpha channel \[A\] separately encoded.</span></span>

<span data-ttu-id="a62e4-141">下表列出每個區塊類型的元件。</span><span class="sxs-lookup"><span data-stu-id="a62e4-141">The following table lists the components of each block type.</span></span>



| <span data-ttu-id="a62e4-142">BC7 區塊包含...</span><span class="sxs-lookup"><span data-stu-id="a62e4-142">BC7 block contains...</span></span>     | <span data-ttu-id="a62e4-143">模式位元</span><span class="sxs-lookup"><span data-stu-id="a62e4-143">mode bits</span></span> | <span data-ttu-id="a62e4-144">旋轉位元</span><span class="sxs-lookup"><span data-stu-id="a62e4-144">rotation bits</span></span> | <span data-ttu-id="a62e4-145">索引選取器位元</span><span class="sxs-lookup"><span data-stu-id="a62e4-145">index selector bit</span></span> | <span data-ttu-id="a62e4-146">分割位元</span><span class="sxs-lookup"><span data-stu-id="a62e4-146">partition bits</span></span> | <span data-ttu-id="a62e4-147">壓縮端點</span><span class="sxs-lookup"><span data-stu-id="a62e4-147">compressed endpoints</span></span> | <span data-ttu-id="a62e4-148">P 位元</span><span class="sxs-lookup"><span data-stu-id="a62e4-148">P-bit</span></span>    | <span data-ttu-id="a62e4-149">壓縮索引</span><span class="sxs-lookup"><span data-stu-id="a62e4-149">compressed indices</span></span> |
|---------------------------|-----------|---------------|--------------------|----------------|----------------------|----------|--------------------|
| <span data-ttu-id="a62e4-150">僅限色彩元件</span><span class="sxs-lookup"><span data-stu-id="a62e4-150">color components only</span></span>     | <span data-ttu-id="a62e4-151">必要</span><span class="sxs-lookup"><span data-stu-id="a62e4-151">required</span></span>  | <span data-ttu-id="a62e4-152">N/A</span><span class="sxs-lookup"><span data-stu-id="a62e4-152">N/A</span></span>           | <span data-ttu-id="a62e4-153">N/A</span><span class="sxs-lookup"><span data-stu-id="a62e4-153">N/A</span></span>                | <span data-ttu-id="a62e4-154">必要</span><span class="sxs-lookup"><span data-stu-id="a62e4-154">required</span></span>       | <span data-ttu-id="a62e4-155">必要</span><span class="sxs-lookup"><span data-stu-id="a62e4-155">required</span></span>             | <span data-ttu-id="a62e4-156">選用</span><span class="sxs-lookup"><span data-stu-id="a62e4-156">optional</span></span> | <span data-ttu-id="a62e4-157">必要</span><span class="sxs-lookup"><span data-stu-id="a62e4-157">required</span></span>           |
| <span data-ttu-id="a62e4-158">色彩 + Alpha 合併</span><span class="sxs-lookup"><span data-stu-id="a62e4-158">color + alpha combined</span></span>    | <span data-ttu-id="a62e4-159">必要</span><span class="sxs-lookup"><span data-stu-id="a62e4-159">required</span></span>  | <span data-ttu-id="a62e4-160">N/A</span><span class="sxs-lookup"><span data-stu-id="a62e4-160">N/A</span></span>           | <span data-ttu-id="a62e4-161">N/A</span><span class="sxs-lookup"><span data-stu-id="a62e4-161">N/A</span></span>                | <span data-ttu-id="a62e4-162">選用</span><span class="sxs-lookup"><span data-stu-id="a62e4-162">optional</span></span>       | <span data-ttu-id="a62e4-163">必要</span><span class="sxs-lookup"><span data-stu-id="a62e4-163">required</span></span>             | <span data-ttu-id="a62e4-164">選用</span><span class="sxs-lookup"><span data-stu-id="a62e4-164">optional</span></span> | <span data-ttu-id="a62e4-165">必要</span><span class="sxs-lookup"><span data-stu-id="a62e4-165">required</span></span>           |
| <span data-ttu-id="a62e4-166">色彩和 Alpha 分隔</span><span class="sxs-lookup"><span data-stu-id="a62e4-166">color and alpha separated</span></span> | <span data-ttu-id="a62e4-167">必要</span><span class="sxs-lookup"><span data-stu-id="a62e4-167">required</span></span>  | <span data-ttu-id="a62e4-168">必要</span><span class="sxs-lookup"><span data-stu-id="a62e4-168">required</span></span>      | <span data-ttu-id="a62e4-169">選用</span><span class="sxs-lookup"><span data-stu-id="a62e4-169">optional</span></span>           | <span data-ttu-id="a62e4-170">N/A</span><span class="sxs-lookup"><span data-stu-id="a62e4-170">N/A</span></span>            | <span data-ttu-id="a62e4-171">必要</span><span class="sxs-lookup"><span data-stu-id="a62e4-171">required</span></span>             | <span data-ttu-id="a62e4-172">N/A</span><span class="sxs-lookup"><span data-stu-id="a62e4-172">N/A</span></span>      | <span data-ttu-id="a62e4-173">必要</span><span class="sxs-lookup"><span data-stu-id="a62e4-173">required</span></span>           |



 

<span data-ttu-id="a62e4-174">BC7 在兩個端點之間的大約行定義調色盤。</span><span class="sxs-lookup"><span data-stu-id="a62e4-174">BC7 defines a palette of colors on an approximate line between two endpoints.</span></span> <span data-ttu-id="a62e4-175">模式值判斷每個區塊的端點配對插入數量。</span><span class="sxs-lookup"><span data-stu-id="a62e4-175">The mode value determines the number of interpolating endpoint pairs per block.</span></span> <span data-ttu-id="a62e4-176">BC7 在每個材質上儲存一個調色盤索引。</span><span class="sxs-lookup"><span data-stu-id="a62e4-176">BC7 stores one palette index per texel.</span></span>

<span data-ttu-id="a62e4-177">對於每個對應至一組端點的索引子集，編碼器修正了該子集壓縮索引資料中一個位元的狀態。</span><span class="sxs-lookup"><span data-stu-id="a62e4-177">For each subset of indices that corresponds to a pair of endpoints, the encoder fixes the state of one bit of the compressed index data for that subset.</span></span> <span data-ttu-id="a62e4-178">它藉由選擇一個端點順序來完成此項工作，該端點順序可讓指定的「修正」索引之索引將其最高有效位元設為 0，之後便能捨棄該位元，為每個子集節省一個位元。</span><span class="sxs-lookup"><span data-stu-id="a62e4-178">It does so by choosing an endpoint order that allows the index for the designated "fix-up" index to set its most significant bit to 0, and which can then be discarded, saving one bit per subset.</span></span> <span data-ttu-id="a62e4-179">對於僅具有一個單一子集的區塊模式，修正索引一律為索引 0。</span><span class="sxs-lookup"><span data-stu-id="a62e4-179">For block modes with only a single subset, the fix-up index is always index 0.</span></span>

## <a name="decoding-the-bc7-format"></a><span data-ttu-id="a62e4-180">解碼 BC7 格式</span><span class="sxs-lookup"><span data-stu-id="a62e4-180">Decoding the BC7 Format</span></span>

<span data-ttu-id="a62e4-181">下列虛擬程式碼概述了於 16 位元組 BC7 區塊中，解壓縮位於 (x,y) 之像素的步驟。</span><span class="sxs-lookup"><span data-stu-id="a62e4-181">The following pseudocode outlines the steps to decompress the pixel at (x,y) given the 16 byte BC7 block.</span></span>

``` syntax
decompress_bc7(x, y, block)
{
    mode = extract_mode(block);
    
    //decode partition data from explicit partition bits
    subset_index = 0;
    num_subsets = 1;
    
    if (mode.type == 0 OR == 1 OR == 2 OR == 3 OR == 7)
    {
        num_subsets = get_num_subsets(mode.type);
        partition_set_id = extract_partition_set_id(mode, block);
        subset_index = get_partition_index(num_subsets, partition_set_id, x, y);
    }
    
    //extract raw, compressed endpoint bits
    UINT8 endpoint_array[num_subsets][4] = extract_endpoints(mode, block);
    
    //decode endpoint color and alpha for each subset
    fully_decode_endpoints(endpoint_array, mode, block);
    
    //endpoints are now complete.
    UINT8 endpoint_start[4] = endpoint_array[2 * subset_index];
    UINT8 endpoint_end[4]   = endpoint_array[2 * subset_index + 1];
        
    //Determine the palette index for this pixel
    alpha_index     = get_alpha_index(block, mode, x, y);
    alpha_bitcount  = get_alpha_bitcount(block, mode);
    color_index     = get_color_index(block, mode, x, y);
    color_bitcount  = get_color_bitcount(block, mode);

    //determine output
    UINT8 output[4];
    output.rgb = interpolate(endpoint_start.rgb, endpoint_end.rgb, color_index, color_bitcount);
    output.a   = interpolate(endpoint_start.a,   endpoint_end.a,   alpha_index, alpha_bitcount);
    
    if (mode.type == 4 OR == 5)
    {
        //Decode the 2 color rotation bits as follows:
        // 00 – Block format is Scalar(A) Vector(RGB) - no swapping
        // 01 – Block format is Scalar(R) Vector(AGB) - swap A and R
        // 10 – Block format is Scalar(G) Vector(RAB) - swap A and G
        // 11 - Block format is Scalar(B) Vector(RGA) - swap A and B
        rotation = extract_rot_bits(mode, block);
        output = swap_channels(output, rotation);
    }
    
}
```

<span data-ttu-id="a62e4-182">下列虛擬程式碼概述了於 16 位元組 BC7 區塊中，為每個子集完整解碼端點色彩和 Alpha 元件的步驟。</span><span class="sxs-lookup"><span data-stu-id="a62e4-182">The followoing pseudocode outlines the steps to fully decode endpoint color and alpha components for each subset given a 16-byte BC7 block.</span></span>

``` syntax
fully_decode_endpoints(endpoint_array, mode, block)
{
    //first handle modes that have P-bits
    if (mode.type == 0 OR == 1 OR == 3 OR == 6 OR == 7)
    {
        for each endpoint i
        {
            //component-wise left-shift
            endpoint_array[i].rgba = endpoint_array[i].rgba << 1;
        }
        
        //if P-bit is shared
        if (mode.type == 1) 
        {
            pbit_zero = extract_pbit_zero(mode, block);
            pbit_one = extract_pbit_one(mode, block);
            
            //rgb component-wise insert pbits
            endpoint_array[0].rgb |= pbit_zero;
            endpoint_array[1].rgb |= pbit_zero;
            endpoint_array[2].rgb |= pbit_one;
            endpoint_array[3].rgb |= pbit_one;  
        }
        else //unique P-bit per endpoint
        {  
            pbit_array = extract_pbit_array(mode, block);
            for each endpoint i
            {
                endpoint_array[i].rgba |= pbit_array[i];
            }
        }
    }

    for each endpoint i
    {
        // Color_component_precision & alpha_component_precision includes pbit
        // left shift endpoint components so that their MSB lies in bit 7
        endpoint_array[i].rgb = endpoint_array[i].rgb << (8 - color_component_precision(mode));
        endpoint_array[i].a = endpoint_array[i].a << (8 - alpha_component_precision(mode));

        // Replicate each component's MSB into the LSBs revealed by the left-shift operation above
        endpoint_array[i].rgb = endpoint_array[i].rgb | (endpoint_array[i].rgb >> color_component_precision(mode));
        endpoint_array[i].a = endpoint_array[i].a | (endpoint_array[i].a >> alpha_component_precision(mode));
    }
        
    //If this mode does not explicitly define the alpha component
    //set alpha equal to 1.0
    if (mode.type == 0 OR == 1 OR == 2 OR == 3)
    {
        for each endpoint i
        {
            endpoint_array[i].a = 255; //i.e. alpha = 1.0f
        }
    }
}
```

<span data-ttu-id="a62e4-183">若要為每個子集產生每個插入的元件，請使用下列演算法︰讓 "c" 成為產生的元件、讓 "e0" 成為該子集端點 0 的元件，並讓 "e1" 成為該子集端點 1 的元件。</span><span class="sxs-lookup"><span data-stu-id="a62e4-183">To generate each interpolated component for each subset, use the following algorithm: let "c" be the component to generate; let "e0" be that component of endpoint 0 of the subset; and let "e1" be that component of endpoint 1 of the subset.</span></span>

``` syntax
UINT16 aWeight2[] = {0, 21, 43, 64};
UINT16 aWeight3[] = {0, 9, 18, 27, 37, 46, 55, 64};
UINT16 aWeight4[] = {0, 4, 9, 13, 17, 21, 26, 30, 34, 38, 43, 47, 51, 55, 60, 64};

UINT8 interpolate(UINT8 e0, UINT8 e1, UINT8 index, UINT8 indexprecision)
{
    if(indexprecision == 2)
        return (UINT8) (((64 - aWeights2[index])*UINT16(e0) + aWeights2[index]*UINT16(e1) + 32) >> 6);
    else if(indexprecision == 3)
        return (UINT8) (((64 - aWeights3[index])*UINT16(e0) + aWeights3[index]*UINT16(e1) + 32) >> 6);
    else // indexprecision == 4
        return (UINT8) (((64 - aWeights4[index])*UINT16(e0) + aWeights4[index]*UINT16(e1) + 32) >> 6);
}
```

<span data-ttu-id="a62e4-184">下列虛擬程式碼示範如何為色彩和 Alpha 元件擷取索引及位元計數的方式。</span><span class="sxs-lookup"><span data-stu-id="a62e4-184">The following pseudocode illustrates how to extract indices and bit counts for color and alpha components.</span></span> <span data-ttu-id="a62e4-185">使用不同色彩和 Alpha 的區塊也有兩組索引資料︰一個用於向量通道，一個用於純量通道。</span><span class="sxs-lookup"><span data-stu-id="a62e4-185">Blocks with separate color and alpha also have two sets of index data: one for the vector channel, and one for the scalar channel.</span></span> <span data-ttu-id="a62e4-186">對於模式 4，這些索引有不同寬度 (2 或 3 位元)，而且有一個 1 位元選取器來指定向量或純量資料是否使用 3 位元索引。</span><span class="sxs-lookup"><span data-stu-id="a62e4-186">For Mode 4, these indices are of differing widths (2 or 3 bits), and there is a one-bit selector which specifies whether the vector or scalar data uses the 3-bit indices.</span></span> <span data-ttu-id="a62e4-187">(解壓縮 Alpha 位元計數類似於擷取色彩位元計數，但是具有以 **idxMode** 位元為基礎的反向行為。)</span><span class="sxs-lookup"><span data-stu-id="a62e4-187">(Extracting the alpha bit count is similar to extracting color bit count but with inverse behavior based on the **idxMode** bit.)</span></span>

``` syntax
bitcount get_color_bitcount(block, mode)
{
    if (mode.type == 0 OR == 1)
        return 3;
    
    if (mode.type == 2 OR == 3 OR == 5 OR == 7)
        return 2;
    
    if (mode.type == 6)
        return 4;
        
    //The only remaining case is Mode 4 with 1-bit index selector
    idxMode = extract_idxMode(block);
    if (idxMode == 0)
        return 2;
    else
        return 3;
}
```

## <a name="related-topics"></a><span data-ttu-id="a62e4-188">相關主題</span><span class="sxs-lookup"><span data-stu-id="a62e4-188">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a62e4-189">Direct3D 11 中的材質區塊壓縮</span><span class="sxs-lookup"><span data-stu-id="a62e4-189">Texture Block Compression in Direct3D 11</span></span>](texture-block-compression-in-direct3d-11.md)
</dt> </dl>

 

 