---
title: BC6H 格式
description: BC6H 格式為一種設計用來支援來源資料中高動態範圍 (HDR) 色彩空間的紋理壓縮格式。
ms.assetid: D6A1A729-5023-4A94-A8DB-5954D453E136
keywords:
- BC6H
- DXGI_FORMAT_BC6H
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92ea15e0275bc478c0708ce08f531d8888a3c84d
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335222"
---
# <a name="bc6h-format"></a><span data-ttu-id="19d86-105">BC6H 格式</span><span class="sxs-lookup"><span data-stu-id="19d86-105">BC6H Format</span></span>

<span data-ttu-id="19d86-106">BC6H 格式為一種設計用來支援來源資料中高動態範圍 (HDR) 色彩空間的紋理壓縮格式。</span><span class="sxs-lookup"><span data-stu-id="19d86-106">The BC6H format is a texture compression format designed to support high-dynamic range (HDR) color spaces in source data.</span></span>

-   [<span data-ttu-id="19d86-107">關於 BC6H/DXGI \_ 格式 \_ BC6H</span><span class="sxs-lookup"><span data-stu-id="19d86-107">About BC6H/DXGI\_FORMAT\_BC6H</span></span>](/windows)
-   [<span data-ttu-id="19d86-108">BC6H 執行</span><span class="sxs-lookup"><span data-stu-id="19d86-108">BC6H Implementation</span></span>](#bc6h-implementation)
-   [<span data-ttu-id="19d86-109">解碼 BC6H 格式</span><span class="sxs-lookup"><span data-stu-id="19d86-109">Decoding the BC6H Format</span></span>](#decoding-the-bc6h-format)
-   [<span data-ttu-id="19d86-110">BC6H 壓縮的端點格式</span><span class="sxs-lookup"><span data-stu-id="19d86-110">BC6H Compressed Endpoint Format</span></span>](#bc6h-compressed-endpoint-format)
-   [<span data-ttu-id="19d86-111">端點值的正負號延伸</span><span class="sxs-lookup"><span data-stu-id="19d86-111">Sign Extension for Endpoint Values</span></span>](#sign-extension-for-endpoint-values)
-   [<span data-ttu-id="19d86-112">端點值的轉換反轉</span><span class="sxs-lookup"><span data-stu-id="19d86-112">Transform Inversion for Endpoint Values</span></span>](#transform-inversion-for-endpoint-values)
-   [<span data-ttu-id="19d86-113">色彩端點的 Unquantization</span><span class="sxs-lookup"><span data-stu-id="19d86-113">Unquantization of Color Endpoints</span></span>](#unquantization-of-color-endpoints)
-   [<span data-ttu-id="19d86-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="19d86-114">Related topics</span></span>](#related-topics)

## <a name="about-bc6hdxgi_format_bc6h"></a><span data-ttu-id="19d86-115">關於 BC6H/DXGI \_ 格式 \_ BC6H</span><span class="sxs-lookup"><span data-stu-id="19d86-115">About BC6H/DXGI\_FORMAT\_BC6H</span></span>

<span data-ttu-id="19d86-116">BC6H 格式針對使用了三個 HDR 色彩通道的影像，透過賦予每個值為 (16:16:16) 的色彩通道一個 16 位元值，提供高品質的壓縮。</span><span class="sxs-lookup"><span data-stu-id="19d86-116">The BC6H format provides high-quality compression for images that use three HDR color channels, with a 16-bit value for each color channel of the value (16:16:16).</span></span> <span data-ttu-id="19d86-117">目前仍不支援 Alpha 色板。</span><span class="sxs-lookup"><span data-stu-id="19d86-117">There is no support for an alpha channel.</span></span>

<span data-ttu-id="19d86-118">BC6H 是由下列 DXGI \_ 格式列舉值所指定：</span><span class="sxs-lookup"><span data-stu-id="19d86-118">BC6H is specified by the following DXGI\_FORMAT enumeration values:</span></span>

-   <span data-ttu-id="19d86-119">**DXGI \_格式化 \_ BC6H \_** 無別。</span><span class="sxs-lookup"><span data-stu-id="19d86-119">**DXGI\_FORMAT\_BC6H\_TYPELESS**.</span></span>
-   <span data-ttu-id="19d86-120">**DXGI \_FORMAT \_ BC6H \_ UF16**。</span><span class="sxs-lookup"><span data-stu-id="19d86-120">**DXGI\_FORMAT\_BC6H\_UF16**.</span></span> <span data-ttu-id="19d86-121">此 BC6H 格式在 16 位元浮點數的色彩通道數值中，不會使用正負號位元。</span><span class="sxs-lookup"><span data-stu-id="19d86-121">This BC6H format does not use a sign bit in the 16-bit floating point color channel values.</span></span>
-   <span data-ttu-id="19d86-122">**DXGI \_FORMAT \_ BC6H \_ SF16**。這個 BC6H 格式會在16位浮點色彩通道值中使用正負號位。</span><span class="sxs-lookup"><span data-stu-id="19d86-122">**DXGI\_FORMAT\_BC6H\_SF16**.This BC6H format uses a sign bit in the 16-bit floating point color channel values.</span></span>

> [!Note]  
> <span data-ttu-id="19d86-123">色彩通道的16位浮點數格式通常稱為「半」浮點數格式。</span><span class="sxs-lookup"><span data-stu-id="19d86-123">The 16 bit floating point format for color channels is often referred to as a "half" floating point format.</span></span> <span data-ttu-id="19d86-124">此格式以下列位元配置︰</span><span class="sxs-lookup"><span data-stu-id="19d86-124">This format has the following bit layout:</span></span>
>
> |  <span data-ttu-id="19d86-125">格式</span><span class="sxs-lookup"><span data-stu-id="19d86-125">Format</span></span>                     | <span data-ttu-id="19d86-126">位配置</span><span class="sxs-lookup"><span data-stu-id="19d86-126">Bit layout</span></span>                                                |
> |-----------------------|-------------------------------------------------|
> | <span data-ttu-id="19d86-127">UF16 (不帶正負號的浮點數)</span><span class="sxs-lookup"><span data-stu-id="19d86-127">UF16 (unsigned float)</span></span> | <span data-ttu-id="19d86-128">5 個指數位元 + 11 個尾數位元</span><span class="sxs-lookup"><span data-stu-id="19d86-128">5 exponent bits + 11 mantissa bits</span></span>              |
> | <span data-ttu-id="19d86-129">SF16 (帶正負號的浮點數)</span><span class="sxs-lookup"><span data-stu-id="19d86-129">SF16 (signed float)</span></span>   | <span data-ttu-id="19d86-130">1 個正負號位元 + 5 個指數位元 + 10 個尾數位元</span><span class="sxs-lookup"><span data-stu-id="19d86-130">1 sign bit + 5 exponent bits + 10 mantissa bits</span></span> |
>
> 
>
>  

 

<span data-ttu-id="19d86-131">BC6H 格式可用於 [Texture2D](/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures) (包括陣列)、Texture3D，或 TextureCube (包括陣列) 紋理資源。</span><span class="sxs-lookup"><span data-stu-id="19d86-131">The BC6H format can be used for [Texture2D](/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures) (including arrays), Texture3D, or TextureCube (including arrays) texture resources.</span></span> <span data-ttu-id="19d86-132">同樣地，此格式適用於任何與這些資源建立關聯的 Mipmap 表面。</span><span class="sxs-lookup"><span data-stu-id="19d86-132">Similarly, this format applies to any MIP-map surfaces associated with these resources.</span></span>

<span data-ttu-id="19d86-133">BC6H 使用固定的 16 位元組 (128 位元) 區塊大小，以及固定之 4x4 材質的磚大小。</span><span class="sxs-lookup"><span data-stu-id="19d86-133">BC6H uses a fixed block size of 16 bytes (128 bits) and a fixed tile size of 4x4 texels.</span></span> <span data-ttu-id="19d86-134">與之前的 BC 格式一樣，大於支援之磚大小 (4x4) 的紋理影像，程式會使用多重區塊對其進行壓縮。</span><span class="sxs-lookup"><span data-stu-id="19d86-134">As with previous BC formats, texture images larger than the supported tile size (4x4) are compressed by using multiple blocks.</span></span> <span data-ttu-id="19d86-135">此定址身分識別也適用于三維影像、MIP 對應、cubemaps 和材質陣列。</span><span class="sxs-lookup"><span data-stu-id="19d86-135">This addressing identity applies also to three-dimensional images, MIP-maps, cubemaps, and texture arrays.</span></span> <span data-ttu-id="19d86-136">所有影像磚都必須格式相同。</span><span class="sxs-lookup"><span data-stu-id="19d86-136">All image tiles must be of the same format.</span></span>

<span data-ttu-id="19d86-137">關於 BC6H 格式的一些重要注意事項：</span><span class="sxs-lookup"><span data-stu-id="19d86-137">Some important notes about the BC6H format:</span></span>

-   <span data-ttu-id="19d86-138">BC6H 支援浮點數反正規化，但不支援 INF (無限大) 和 NAN (不是數字)。</span><span class="sxs-lookup"><span data-stu-id="19d86-138">BC6H supports floating point denormalization, but does not support INF (infinity) and NaN (not a number).</span></span> <span data-ttu-id="19d86-139">例外狀況是 BC6H (DXGI \_ FORMAT \_ BC6H SF16) 的簽署模式 \_ ，它支援-INF (負無限大) 。</span><span class="sxs-lookup"><span data-stu-id="19d86-139">The exception is the signed mode of BC6H (DXGI\_FORMAT\_BC6H\_SF16), which supports -INF (negative infinity).</span></span> <span data-ttu-id="19d86-140">請注意，這項對-INF 的支援只是格式本身的成品，而且此格式的編碼器不會特別支援。</span><span class="sxs-lookup"><span data-stu-id="19d86-140">Note that this support for -INF is merely an artifact of the format itself, and is not specifically supported by encoders for this format.</span></span> <span data-ttu-id="19d86-141">一般而言，當編碼器遇到 INF (正面或負面) 或 NaN 輸入資料時，它們應該 \\ 將該資料轉換成允許的最大非 INF 表示值，並在壓縮之前將 NaN 對應至0。</span><span class="sxs-lookup"><span data-stu-id="19d86-141">In general, when encoders encounter INF (positive or negative) or NaN input data, they should \\ convert that data to the maximum allowable non-INF representation value, and map NaN to 0 prior to compression.</span></span>
-   <span data-ttu-id="19d86-142">BC6H 不支援 Alpha 色板。</span><span class="sxs-lookup"><span data-stu-id="19d86-142">BC6H does not support an alpha channel.</span></span>
-   <span data-ttu-id="19d86-143">BC6H 解碼器在執行紋理篩選之前，會先執行解壓縮。</span><span class="sxs-lookup"><span data-stu-id="19d86-143">The BC6H decoder performs decompression before it performs texture filtering.</span></span>
-   <span data-ttu-id="19d86-144">BC6H 解壓縮必須是精確的;也就是說，硬體必須傳回與本檔中所述的解碼器相同的結果。</span><span class="sxs-lookup"><span data-stu-id="19d86-144">BC6H decompression must be bit accurate; that is, the hardware must return results that are identical to the decoder described in this documentation.</span></span>

## <a name="bc6h-implementation"></a><span data-ttu-id="19d86-145">BC6H 執行</span><span class="sxs-lookup"><span data-stu-id="19d86-145">BC6H Implementation</span></span>

<span data-ttu-id="19d86-146">BC6H 區塊由模式位元、壓縮端點、壓縮索引，以及選用的分割索引組成。</span><span class="sxs-lookup"><span data-stu-id="19d86-146">A BC6H block consists of mode bits, compressed endpoints, compressed indices, and an optional partition index.</span></span> <span data-ttu-id="19d86-147">此格式指定了 14 種不同的模式。</span><span class="sxs-lookup"><span data-stu-id="19d86-147">This format specifies 14 different modes.</span></span>

<span data-ttu-id="19d86-148">端點色彩以 RGB 三元組儲存。</span><span class="sxs-lookup"><span data-stu-id="19d86-148">An endpoint color is stored as an RGB triplet.</span></span> <span data-ttu-id="19d86-149">BC6H 透過一條通過數個使用者設定色彩端點的估計線，以決定色彩調色盤。</span><span class="sxs-lookup"><span data-stu-id="19d86-149">BC6H defines a palette of colors on an approximate line across a number of defined color endpoints.</span></span> <span data-ttu-id="19d86-150">此外，根據模式的不同，磚可分割成兩個區域或視為單一區域。其中，分割成兩個區域的磚，針對每個區域皆會有其個別的色彩端點組。</span><span class="sxs-lookup"><span data-stu-id="19d86-150">Also, depending on the mode, a tile can be divided into two regions or treated as a single region, where a two-region tile has a separate set of color endpoints for each region.</span></span> <span data-ttu-id="19d86-151">BC6H 在每個材質上儲存一個調色盤索引。</span><span class="sxs-lookup"><span data-stu-id="19d86-151">BC6H stores one palette index per texel.</span></span>

<span data-ttu-id="19d86-152">在兩個區域的案例中，總共會有 32 種可能的分割。</span><span class="sxs-lookup"><span data-stu-id="19d86-152">In the two-region case, there are 32 possible partitions.</span></span>

## <a name="decoding-the-bc6h-format"></a><span data-ttu-id="19d86-153">解碼 BC6H 格式</span><span class="sxs-lookup"><span data-stu-id="19d86-153">Decoding the BC6H Format</span></span>

<span data-ttu-id="19d86-154">下列虛擬程式碼描述於 16 位元組 BC6H 區塊中，解壓縮位於 (x,y) 點之像素的步驟。</span><span class="sxs-lookup"><span data-stu-id="19d86-154">The pseudocode below shows the steps to decompress the pixel at (x,y) given the 16 byte BC6H block.</span></span>

``` syntax
decompress_bc6h(x, y, block)
{
    mode = extract_mode(block);
    endpoints;
    index;
    
    if(mode.type == ONE)
    {
        endpoints = extract_compressed_endpoints(mode, block);
        index = extract_index_ONE(x, y, block);
    }
    else //mode.type == TWO
    {
        partition = extract_partition(block);
        region = get_region(partition, x, y);
        endpoints = extract_compressed_endpoints(mode, region, block);
        index = extract_index_TWO(x, y, partition, block);
    }
    
    unquantize(endpoints);
    color = interpolate(index, endpoints);
    finish_unquantize(color);
}
```

<span data-ttu-id="19d86-155">下表包含了 BC6H 區塊中 14 種可能格式個別的位元計數及其數值。</span><span class="sxs-lookup"><span data-stu-id="19d86-155">The following table contains the bit count and values for each of the 14 possible formats for BC6H blocks.</span></span> 

| <span data-ttu-id="19d86-156">模式</span><span class="sxs-lookup"><span data-stu-id="19d86-156">Mode</span></span> | <span data-ttu-id="19d86-157">分割索引</span><span class="sxs-lookup"><span data-stu-id="19d86-157">Partition Indices</span></span> | <span data-ttu-id="19d86-158">資料分割</span><span class="sxs-lookup"><span data-stu-id="19d86-158">Partition</span></span> | <span data-ttu-id="19d86-159">色彩端點</span><span class="sxs-lookup"><span data-stu-id="19d86-159">Color Endpoints</span></span>                  | <span data-ttu-id="19d86-160">模式位元</span><span class="sxs-lookup"><span data-stu-id="19d86-160">Mode Bits</span></span>      |
|------|-------------------|-----------|----------------------------------|----------------|
| <span data-ttu-id="19d86-161">1</span><span class="sxs-lookup"><span data-stu-id="19d86-161">1</span></span>    | <span data-ttu-id="19d86-162">46 個位元</span><span class="sxs-lookup"><span data-stu-id="19d86-162">46 bits</span></span>           | <span data-ttu-id="19d86-163">5 個位元</span><span class="sxs-lookup"><span data-stu-id="19d86-163">5 bits</span></span>    | <span data-ttu-id="19d86-164">75 個位元 (10.555, 10.555, 10.555)</span><span class="sxs-lookup"><span data-stu-id="19d86-164">75 bits (10.555, 10.555, 10.555)</span></span> | <span data-ttu-id="19d86-165">2 個位元 (00)</span><span class="sxs-lookup"><span data-stu-id="19d86-165">2 bits (00)</span></span>    |
| <span data-ttu-id="19d86-166">2</span><span class="sxs-lookup"><span data-stu-id="19d86-166">2</span></span>    | <span data-ttu-id="19d86-167">46 個位元</span><span class="sxs-lookup"><span data-stu-id="19d86-167">46 bits</span></span>           | <span data-ttu-id="19d86-168">5 個位元</span><span class="sxs-lookup"><span data-stu-id="19d86-168">5 bits</span></span>    | <span data-ttu-id="19d86-169">75 個位元 (7666, 7666, 7666)</span><span class="sxs-lookup"><span data-stu-id="19d86-169">75 bits (7666, 7666, 7666)</span></span>       | <span data-ttu-id="19d86-170">2 個位元 (01)</span><span class="sxs-lookup"><span data-stu-id="19d86-170">2 bits (01)</span></span>    |
| <span data-ttu-id="19d86-171">3</span><span class="sxs-lookup"><span data-stu-id="19d86-171">3</span></span>    | <span data-ttu-id="19d86-172">46 個位元</span><span class="sxs-lookup"><span data-stu-id="19d86-172">46 bits</span></span>           | <span data-ttu-id="19d86-173">5 個位元</span><span class="sxs-lookup"><span data-stu-id="19d86-173">5 bits</span></span>    | <span data-ttu-id="19d86-174">72 個位元 (11.555, 11.444, 11.444)</span><span class="sxs-lookup"><span data-stu-id="19d86-174">72 bits (11.555, 11.444, 11.444)</span></span> | <span data-ttu-id="19d86-175">5 個位元 (00010)</span><span class="sxs-lookup"><span data-stu-id="19d86-175">5 bits (00010)</span></span> |
| <span data-ttu-id="19d86-176">4</span><span class="sxs-lookup"><span data-stu-id="19d86-176">4</span></span>    | <span data-ttu-id="19d86-177">46 個位元</span><span class="sxs-lookup"><span data-stu-id="19d86-177">46 bits</span></span>           | <span data-ttu-id="19d86-178">5 個位元</span><span class="sxs-lookup"><span data-stu-id="19d86-178">5 bits</span></span>    | <span data-ttu-id="19d86-179">72 個位元 (11.444, 11.555, 11.444)</span><span class="sxs-lookup"><span data-stu-id="19d86-179">72 bits (11.444, 11.555, 11.444)</span></span> | <span data-ttu-id="19d86-180">5 個位元 (00110)</span><span class="sxs-lookup"><span data-stu-id="19d86-180">5 bits (00110)</span></span> |
| <span data-ttu-id="19d86-181">5</span><span class="sxs-lookup"><span data-stu-id="19d86-181">5</span></span>    | <span data-ttu-id="19d86-182">46 個位元</span><span class="sxs-lookup"><span data-stu-id="19d86-182">46 bits</span></span>           | <span data-ttu-id="19d86-183">5 個位元</span><span class="sxs-lookup"><span data-stu-id="19d86-183">5 bits</span></span>    | <span data-ttu-id="19d86-184">72 個位元 (11.444, 11.444, 11.555)</span><span class="sxs-lookup"><span data-stu-id="19d86-184">72 bits (11.444, 11.444, 11.555)</span></span> | <span data-ttu-id="19d86-185">5 個位元 (01010)</span><span class="sxs-lookup"><span data-stu-id="19d86-185">5 bits (01010)</span></span> |
| <span data-ttu-id="19d86-186">6</span><span class="sxs-lookup"><span data-stu-id="19d86-186">6</span></span>    | <span data-ttu-id="19d86-187">46 個位元</span><span class="sxs-lookup"><span data-stu-id="19d86-187">46 bits</span></span>           | <span data-ttu-id="19d86-188">5 個位元</span><span class="sxs-lookup"><span data-stu-id="19d86-188">5 bits</span></span>    | <span data-ttu-id="19d86-189">72 個位元 (9555, 9555, 9555)</span><span class="sxs-lookup"><span data-stu-id="19d86-189">72 bits (9555, 9555, 9555)</span></span>       | <span data-ttu-id="19d86-190">5 個位元 (01110)</span><span class="sxs-lookup"><span data-stu-id="19d86-190">5 bits (01110)</span></span> |
| <span data-ttu-id="19d86-191">7</span><span class="sxs-lookup"><span data-stu-id="19d86-191">7</span></span>    | <span data-ttu-id="19d86-192">46 個位元</span><span class="sxs-lookup"><span data-stu-id="19d86-192">46 bits</span></span>           | <span data-ttu-id="19d86-193">5 個位元</span><span class="sxs-lookup"><span data-stu-id="19d86-193">5 bits</span></span>    | <span data-ttu-id="19d86-194">72 個位元 (8666, 8555, 8555)</span><span class="sxs-lookup"><span data-stu-id="19d86-194">72 bits (8666, 8555, 8555)</span></span>       | <span data-ttu-id="19d86-195">5 個位元 (10010)</span><span class="sxs-lookup"><span data-stu-id="19d86-195">5 bits (10010)</span></span> |
| <span data-ttu-id="19d86-196">8</span><span class="sxs-lookup"><span data-stu-id="19d86-196">8</span></span>    | <span data-ttu-id="19d86-197">46 個位元</span><span class="sxs-lookup"><span data-stu-id="19d86-197">46 bits</span></span>           | <span data-ttu-id="19d86-198">5 個位元</span><span class="sxs-lookup"><span data-stu-id="19d86-198">5 bits</span></span>    | <span data-ttu-id="19d86-199">72 個位元 (8555, 8666, 8555)</span><span class="sxs-lookup"><span data-stu-id="19d86-199">72 bits (8555, 8666, 8555)</span></span>       | <span data-ttu-id="19d86-200">5 個位元 (10110)</span><span class="sxs-lookup"><span data-stu-id="19d86-200">5 bits (10110)</span></span> |
| <span data-ttu-id="19d86-201">9</span><span class="sxs-lookup"><span data-stu-id="19d86-201">9</span></span>    | <span data-ttu-id="19d86-202">46 個位元</span><span class="sxs-lookup"><span data-stu-id="19d86-202">46 bits</span></span>           | <span data-ttu-id="19d86-203">5 個位元</span><span class="sxs-lookup"><span data-stu-id="19d86-203">5 bits</span></span>    | <span data-ttu-id="19d86-204">72 個位元 (8555, 8555, 8666)</span><span class="sxs-lookup"><span data-stu-id="19d86-204">72 bits (8555, 8555, 8666)</span></span>       | <span data-ttu-id="19d86-205">5 個位元 (11010)</span><span class="sxs-lookup"><span data-stu-id="19d86-205">5 bits (11010)</span></span> |
| <span data-ttu-id="19d86-206">10</span><span class="sxs-lookup"><span data-stu-id="19d86-206">10</span></span>   | <span data-ttu-id="19d86-207">46 個位元</span><span class="sxs-lookup"><span data-stu-id="19d86-207">46 bits</span></span>           | <span data-ttu-id="19d86-208">5 個位元</span><span class="sxs-lookup"><span data-stu-id="19d86-208">5 bits</span></span>    | <span data-ttu-id="19d86-209">72 個位元 (6666, 6666, 6666)</span><span class="sxs-lookup"><span data-stu-id="19d86-209">72 bits (6666, 6666, 6666)</span></span>       | <span data-ttu-id="19d86-210">5 個位元 (11110)</span><span class="sxs-lookup"><span data-stu-id="19d86-210">5 bits (11110)</span></span> |
| <span data-ttu-id="19d86-211">11</span><span class="sxs-lookup"><span data-stu-id="19d86-211">11</span></span>   | <span data-ttu-id="19d86-212">63 個位元</span><span class="sxs-lookup"><span data-stu-id="19d86-212">63 bits</span></span>           | <span data-ttu-id="19d86-213">0 個位元</span><span class="sxs-lookup"><span data-stu-id="19d86-213">0 bits</span></span>    | <span data-ttu-id="19d86-214">60 個位元 (10.10, 10.10, 10.10)</span><span class="sxs-lookup"><span data-stu-id="19d86-214">60 bits (10.10, 10.10, 10.10)</span></span>    | <span data-ttu-id="19d86-215">5 個位元 (00011)</span><span class="sxs-lookup"><span data-stu-id="19d86-215">5 bits (00011)</span></span> |
| <span data-ttu-id="19d86-216">12</span><span class="sxs-lookup"><span data-stu-id="19d86-216">12</span></span>   | <span data-ttu-id="19d86-217">63 個位元</span><span class="sxs-lookup"><span data-stu-id="19d86-217">63 bits</span></span>           | <span data-ttu-id="19d86-218">0 個位元</span><span class="sxs-lookup"><span data-stu-id="19d86-218">0 bits</span></span>    | <span data-ttu-id="19d86-219">60 個位元 (11.9, 11.9, 11.9)</span><span class="sxs-lookup"><span data-stu-id="19d86-219">60 bits (11.9, 11.9, 11.9)</span></span>       | <span data-ttu-id="19d86-220">5 個位元 (00111)</span><span class="sxs-lookup"><span data-stu-id="19d86-220">5 bits (00111)</span></span> |
| <span data-ttu-id="19d86-221">13</span><span class="sxs-lookup"><span data-stu-id="19d86-221">13</span></span>   | <span data-ttu-id="19d86-222">63 個位元</span><span class="sxs-lookup"><span data-stu-id="19d86-222">63 bits</span></span>           | <span data-ttu-id="19d86-223">0 個位元</span><span class="sxs-lookup"><span data-stu-id="19d86-223">0 bits</span></span>    | <span data-ttu-id="19d86-224">60 個位元 (12.8, 12.8, 12.8)</span><span class="sxs-lookup"><span data-stu-id="19d86-224">60 bits (12.8, 12.8, 12.8)</span></span>       | <span data-ttu-id="19d86-225">5 個位元 (01011)</span><span class="sxs-lookup"><span data-stu-id="19d86-225">5 bits (01011)</span></span> |
| <span data-ttu-id="19d86-226">14</span><span class="sxs-lookup"><span data-stu-id="19d86-226">14</span></span>   | <span data-ttu-id="19d86-227">63 個位元</span><span class="sxs-lookup"><span data-stu-id="19d86-227">63 bits</span></span>           | <span data-ttu-id="19d86-228">0 個位元</span><span class="sxs-lookup"><span data-stu-id="19d86-228">0 bits</span></span>    | <span data-ttu-id="19d86-229">60 個位元 (16.4, 16.4, 16.4)</span><span class="sxs-lookup"><span data-stu-id="19d86-229">60 bits (16.4, 16.4, 16.4)</span></span>       | <span data-ttu-id="19d86-230">5 個位元 (01111)</span><span class="sxs-lookup"><span data-stu-id="19d86-230">5 bits (01111)</span></span> |



 

<span data-ttu-id="19d86-231">此表格中的每個格式皆可利用其模式位元進行識別。</span><span class="sxs-lookup"><span data-stu-id="19d86-231">Each format in this table can be uniquely identified by the mode bits.</span></span> <span data-ttu-id="19d86-232">前 10 個模式使用於分割為兩個區域的磚，並且其模式位元欄位之長度可為二或五。</span><span class="sxs-lookup"><span data-stu-id="19d86-232">The first ten modes are used for two-region tiles, and the mode bit field can be either two or five bits long.</span></span> <span data-ttu-id="19d86-233">這些區塊也包含了壓縮色彩端點 (72 或 75 個位元)、分割 (5 個位元)，以及分割索引 (46 個位元) 的欄位。</span><span class="sxs-lookup"><span data-stu-id="19d86-233">These blocks also have fields for the compressed color endpoints (72 or 75 bits), the partition (5 bits), and the partition indices (46 bits).</span></span>

<span data-ttu-id="19d86-234">針對壓縮色彩端點，上表中的數值標示了儲存 RGB 色彩端點的精確度，及每個色彩值所使用到的位元數。</span><span class="sxs-lookup"><span data-stu-id="19d86-234">For the compressed color endpoints, the values in the preceding table note the precision of the stored RGB endpoints, and the number of bits used for each color value.</span></span> <span data-ttu-id="19d86-235">例如：模式 3 指定了色彩端點精確度為 11，以及儲存轉換過後紅色、藍色，及綠色色彩端點差異值所需要的位元數。(分別為 5, 4, 4。)</span><span class="sxs-lookup"><span data-stu-id="19d86-235">For example, mode 3 specifies a color endpoint precision level of 11, and the number of bits used to store the delta values of the transformed endpoints for the red, blue and green colors (5, 4, and 4 respectively).</span></span> <span data-ttu-id="19d86-236">模式 10 則並未使用 delta 壓縮，而是明確的儲存所有四個色彩端點。</span><span class="sxs-lookup"><span data-stu-id="19d86-236">Mode 10 does not use delta compression, and instead stores all four color endpoints explicitly.</span></span>

<span data-ttu-id="19d86-237">最後四個區塊模式，則適用於單一區域的磚，其模式欄位為 5 個位元。</span><span class="sxs-lookup"><span data-stu-id="19d86-237">The last four block modes are used for one-region tiles, where the mode field is 5 bits.</span></span> <span data-ttu-id="19d86-238">這些區塊都具備了端點 (60 個位元) 及壓縮索引 (63 個位元) 的欄位。</span><span class="sxs-lookup"><span data-stu-id="19d86-238">These blocks have fields for the endpoints (60 bits) and the compressed indices (63 bits).</span></span> <span data-ttu-id="19d86-239">模式 11 (與模式 10 類似) 並未使用 delta 壓縮，而是將兩個色彩端點都明確儲存。</span><span class="sxs-lookup"><span data-stu-id="19d86-239">Mode 11 (like Mode 10) does not use delta compression, and instead stores both color endpoints explicitly.</span></span>

<span data-ttu-id="19d86-240">模式 10011、10111、11011，以及 11111 (未顯示) 目前則作為保留用途使用。</span><span class="sxs-lookup"><span data-stu-id="19d86-240">Modes 10011, 10111, 11011, and 11111 (not shown) are reserved.</span></span> <span data-ttu-id="19d86-241">請勿將這些運用在您的編碼器中。</span><span class="sxs-lookup"><span data-stu-id="19d86-241">Do not use these in your encoder.</span></span> <span data-ttu-id="19d86-242">如果硬體接收到了明確指定為這些模式當中其中一種的區塊，最後解壓縮的結果區塊必須在除 Alpha 色板之外全部的通道中包含所有的 0。</span><span class="sxs-lookup"><span data-stu-id="19d86-242">If the hardware is passed blocks with one of these modes specified, the resulting decompressed block must contain all zeroes in all channels except for the alpha channel.</span></span>

<span data-ttu-id="19d86-243">針對 BC6H，無論模式為何，Alpha 色板都必須傳回 1.0。</span><span class="sxs-lookup"><span data-stu-id="19d86-243">For BC6H, the alpha channel must always return 1.0 regardless of the mode.</span></span>

### <a name="bc6h-partition-set"></a><span data-ttu-id="19d86-244">BC6H 分割集</span><span class="sxs-lookup"><span data-stu-id="19d86-244">BC6H Partition Set</span></span>

<span data-ttu-id="19d86-245">兩個區域的磚共有 32 種可能的分割組合，其定義如下表。</span><span class="sxs-lookup"><span data-stu-id="19d86-245">There are 32 possible partition sets for a two-region tile, and which are defined in the table below.</span></span> <span data-ttu-id="19d86-246">每個 4x4 的區塊代表了單一圖形。</span><span class="sxs-lookup"><span data-stu-id="19d86-246">Each 4x4 block represents a single shape.</span></span>

![BC6H 分割組合列表](images/bc6h-partition-sets.png)

<span data-ttu-id="19d86-248">在此表格中的分割組合，以粗體及底線標示的項目，即為其子集 1 固定索引的位置 (以少於其母集 1 個位元表示)。</span><span class="sxs-lookup"><span data-stu-id="19d86-248">In this table of partition sets, the bolded and underlined entry is the location of the fix-up index for subset 1 (which is specified with one less bit).</span></span> <span data-ttu-id="19d86-249">子集 0 的固定索引一律都是索引 0，因為分割一律會進行排列，使得索引 0 一律會位於子集 0。</span><span class="sxs-lookup"><span data-stu-id="19d86-249">The fix-up index for subset 0 is always index 0, as the partitioning is always arranged such that index 0 is always in subset 0.</span></span> <span data-ttu-id="19d86-250">分割的順序為：由左上至右下，由左移至右，再由上至下。</span><span class="sxs-lookup"><span data-stu-id="19d86-250">Partition order goes from top-left to bottom-right, moving left to right and then top to bottom.</span></span>

## <a name="bc6h-compressed-endpoint-format"></a><span data-ttu-id="19d86-251">BC6H 壓縮的端點格式</span><span class="sxs-lookup"><span data-stu-id="19d86-251">BC6H Compressed Endpoint Format</span></span>

![BC6H 壓縮端點格式的位元欄位](images/bc6h-headers-med.png)

<span data-ttu-id="19d86-253">此表格將壓縮端點的位元欄位以端點格式的功能呈現。每一欄都指定了一種編碼方式，每一列都指定了一個位元欄位。</span><span class="sxs-lookup"><span data-stu-id="19d86-253">This table shows the bit fields for the compressed endpoints as a function of the endpoint format, with each column specifying an encoding and each row specifying a bit field.</span></span> <span data-ttu-id="19d86-254">利用此種方法，兩個區域的磚會使用到 82 個位元，單一區域的磚則會使用到 65 個位元。</span><span class="sxs-lookup"><span data-stu-id="19d86-254">This approach takes up 82 bits for two-region tiles and 65 bits for one-region tiles.</span></span> <span data-ttu-id="19d86-255">例如，上述的單一區域 16 4 編碼的前5位 \[ \] (特別是最右邊的資料行) 為位 m \[ 4:0 \] ，接下來的10個位是位 rw \[ 9:0 \] ，依此類推，最後包含 bw 10:15 的6位 \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="19d86-255">As an example, the first 5 bits for the one-region \[16 4\] encoding above (specifically the right-most column) are bits m\[4:0\], the next 10 bits are bits rw\[9:0\], and so on with the last 6 bits containing bw\[10:15\].</span></span>

<span data-ttu-id="19d86-256">上述表格中的欄位名稱定義如下︰</span><span class="sxs-lookup"><span data-stu-id="19d86-256">The field names in the table above are defined as follows:</span></span>

| <span data-ttu-id="19d86-257">欄位</span><span class="sxs-lookup"><span data-stu-id="19d86-257">Field</span></span> | <span data-ttu-id="19d86-258">變數</span><span class="sxs-lookup"><span data-stu-id="19d86-258">Variable</span></span>          |
|-------|-------------------|
| <span data-ttu-id="19d86-259">m</span><span class="sxs-lookup"><span data-stu-id="19d86-259">m</span></span>     | <span data-ttu-id="19d86-260">mode</span><span class="sxs-lookup"><span data-stu-id="19d86-260">mode</span></span>              |
| <span data-ttu-id="19d86-261">d</span><span class="sxs-lookup"><span data-stu-id="19d86-261">d</span></span>     | <span data-ttu-id="19d86-262">圖形索引</span><span class="sxs-lookup"><span data-stu-id="19d86-262">shape index</span></span>       |
| <span data-ttu-id="19d86-263">rw</span><span class="sxs-lookup"><span data-stu-id="19d86-263">rw</span></span>    | <span data-ttu-id="19d86-264">endpt \[ 0 \] 。\[0\]</span><span class="sxs-lookup"><span data-stu-id="19d86-264">endpt\[0\].A\[0\]</span></span> |
| <span data-ttu-id="19d86-265">rx</span><span class="sxs-lookup"><span data-stu-id="19d86-265">rx</span></span>    | <span data-ttu-id="19d86-266">endpt \[ 0 \] 。B \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="19d86-266">endpt\[0\].B\[0\]</span></span> |
| <span data-ttu-id="19d86-267">ry</span><span class="sxs-lookup"><span data-stu-id="19d86-267">ry</span></span>    | <span data-ttu-id="19d86-268">endpt \[ 1 \] 。\[0\]</span><span class="sxs-lookup"><span data-stu-id="19d86-268">endpt\[1\].A\[0\]</span></span> |
| <span data-ttu-id="19d86-269">rz</span><span class="sxs-lookup"><span data-stu-id="19d86-269">rz</span></span>    | <span data-ttu-id="19d86-270">endpt \[ 1 \] 。B \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="19d86-270">endpt\[1\].B\[0\]</span></span> |
| <span data-ttu-id="19d86-271">gw</span><span class="sxs-lookup"><span data-stu-id="19d86-271">gw</span></span>    | <span data-ttu-id="19d86-272">endpt \[ 0 \] 。\[1\]</span><span class="sxs-lookup"><span data-stu-id="19d86-272">endpt\[0\].A\[1\]</span></span> |
| <span data-ttu-id="19d86-273">gx</span><span class="sxs-lookup"><span data-stu-id="19d86-273">gx</span></span>    | <span data-ttu-id="19d86-274">endpt \[ 0 \] 。B \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="19d86-274">endpt\[0\].B\[1\]</span></span> |
| <span data-ttu-id="19d86-275">gy</span><span class="sxs-lookup"><span data-stu-id="19d86-275">gy</span></span>    | <span data-ttu-id="19d86-276">endpt \[ 1 \] 。\[1\]</span><span class="sxs-lookup"><span data-stu-id="19d86-276">endpt\[1\].A\[1\]</span></span> |
| <span data-ttu-id="19d86-277">gz</span><span class="sxs-lookup"><span data-stu-id="19d86-277">gz</span></span>    | <span data-ttu-id="19d86-278">endpt \[ 1 \] 。B \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="19d86-278">endpt\[1\].B\[1\]</span></span> |
| <span data-ttu-id="19d86-279">bw</span><span class="sxs-lookup"><span data-stu-id="19d86-279">bw</span></span>    | <span data-ttu-id="19d86-280">endpt \[ 0 \] 。A \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="19d86-280">endpt\[0\].A\[2\]</span></span> |
| <span data-ttu-id="19d86-281">bx</span><span class="sxs-lookup"><span data-stu-id="19d86-281">bx</span></span>    | <span data-ttu-id="19d86-282">endpt \[ 0 \] 。B \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="19d86-282">endpt\[0\].B\[2\]</span></span> |
| <span data-ttu-id="19d86-283">by</span><span class="sxs-lookup"><span data-stu-id="19d86-283">by</span></span>    | <span data-ttu-id="19d86-284">endpt \[ 1 \] 。A \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="19d86-284">endpt\[1\].A\[2\]</span></span> |
| <span data-ttu-id="19d86-285">bz</span><span class="sxs-lookup"><span data-stu-id="19d86-285">bz</span></span>    | <span data-ttu-id="19d86-286">endpt \[ 1 \] 。B \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="19d86-286">endpt\[1\].B\[2\]</span></span> |



 

<span data-ttu-id="19d86-287">Endpt \[ i \] （0或1）分別是指第0個或第一組端點。</span><span class="sxs-lookup"><span data-stu-id="19d86-287">Endpt\[i\], where i is either 0 or 1, refers to the 0th or 1st set of endpoints respectively.</span></span>

## <a name="sign-extension-for-endpoint-values"></a><span data-ttu-id="19d86-288">端點值的正負號延伸</span><span class="sxs-lookup"><span data-stu-id="19d86-288">Sign Extension for Endpoint Values</span></span>

<span data-ttu-id="19d86-289">針對兩個區域的磚，總共有四個端點數值可進行正負號擴充。</span><span class="sxs-lookup"><span data-stu-id="19d86-289">For two-region tiles, there are four endpoint values that can be sign extended.</span></span> <span data-ttu-id="19d86-290">Endpt \[ 0 \] 。只有當格式為帶正負號的格式時，才會簽署。只有當端點已轉換，或者格式為簽署格式時，其他端點才會簽署。</span><span class="sxs-lookup"><span data-stu-id="19d86-290">Endpt\[0\].A is signed only if the format is a signed format; the other endpoints are signed only if the endpoint was transformed, or if the format is a signed format.</span></span> <span data-ttu-id="19d86-291">下方的程式碼示範了將兩個區域端點數值的正負號擴充的演算法。</span><span class="sxs-lookup"><span data-stu-id="19d86-291">The code below demonstrates the algorithm for extending the sign of two-region endpoint values.</span></span>

``` syntax
static void sign_extend_two_region(Pattern &p, IntEndpts endpts[NREGIONS_TWO])
{
    for (int i=0; i<NCHANNELS; ++i)
    {
      if (BC6H::FORMAT == SIGNED_F16)
        endpts[0].A[i] = SIGN_EXTEND(endpts[0].A[i], p.chan[i].prec);
      if (p.transformed || BC6H::FORMAT == SIGNED_F16)
      {
        endpts[0].B[i] = SIGN_EXTEND(endpts[0].B[i], p.chan[i].delta[0]);
        endpts[1].A[i] = SIGN_EXTEND(endpts[1].A[i], p.chan[i].delta[1]);
        endpts[1].B[i] = SIGN_EXTEND(endpts[1].B[i], p.chan[i].delta[2]);
      }
    }
}
```

<span data-ttu-id="19d86-292">針對單一區域磚，行為會相同，只會 \[ 移除 endpt 1 \] 。</span><span class="sxs-lookup"><span data-stu-id="19d86-292">For one-region tiles, the behavior is the same, only with endpt\[1\] removed.</span></span>

``` syntax
static void sign_extend_one_region(Pattern &p, IntEndpts endpts[NREGIONS_ONE])
{
    for (int i=0; i<NCHANNELS; ++i)
    {
    if (BC6H::FORMAT == SIGNED_F16)
        endpts[0].A[i] = SIGN_EXTEND(endpts[0].A[i], p.chan[i].prec);
    if (p.transformed || BC6H::FORMAT == SIGNED_F16) 
        endpts[0].B[i] = SIGN_EXTEND(endpts[0].B[i], p.chan[i].delta[0]);
    }
}
```

## <a name="transform-inversion-for-endpoint-values"></a><span data-ttu-id="19d86-293">端點值的轉換反轉</span><span class="sxs-lookup"><span data-stu-id="19d86-293">Transform Inversion for Endpoint Values</span></span>

<span data-ttu-id="19d86-294">針對兩個區域的磚，轉換會套用相異編碼的反向，並在 endpt 0 新增基底 \[ 值 \] 。總共9個新增作業的其他三個專案。</span><span class="sxs-lookup"><span data-stu-id="19d86-294">For two-region tiles, the transform applies the inverse of the difference encoding, adding the base value at endpt\[0\].A to the three other entries for a total of 9 add operations.</span></span> <span data-ttu-id="19d86-295">在下列影像中，基底值表示為「A0」，並且有著最高的浮點數精確度。</span><span class="sxs-lookup"><span data-stu-id="19d86-295">In the image below, the base value is represented as "A0" and has the highest floating point precision.</span></span> <span data-ttu-id="19d86-296">「A1」、「B0」，以及「B1」都是從錨點值計算而來的差異值，並且都以較低的精確度表示。</span><span class="sxs-lookup"><span data-stu-id="19d86-296">"A1," "B0," and "B1" are all deltas calculated from the anchor value, and these delta values are represented with lower precision.</span></span> <span data-ttu-id="19d86-297"> (A0 對應至 endpt \[ 0 \] 。A，B0 對應于 endpt \[ 0 \] 。B，A1 對應到 endpt \[ 1 \] 。和 B1 對應于 endpt \[ 1 \] . b. ) </span><span class="sxs-lookup"><span data-stu-id="19d86-297">(A0 corresponds to endpt\[0\].A, B0 corresponds to endpt\[0\].B, A1 corresponds to endpt\[1\].A, and B1 corresponds to endpt\[1\].B.)</span></span>

![端點數值反向轉換的計算](images/bc6h-transform-inverse.png)

<span data-ttu-id="19d86-299">針對單一區域的磚，由於只有一個 delta 位移，因此只會有 3 個新增運算。</span><span class="sxs-lookup"><span data-stu-id="19d86-299">For one-region tiles there is only one delta offset, and therefore only 3 add operations.</span></span>

<span data-ttu-id="19d86-300">解壓縮程式必須確定反向轉換的結果不會溢位 endpt 0 的有效位數 \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="19d86-300">The decompressor must ensure that that the results of the inverse transform will not overflow the precision of endpt\[0\].a.</span></span> <span data-ttu-id="19d86-301">一旦溢位發生，反向轉換的結果值必須包裝於相同數量的位元中。</span><span class="sxs-lookup"><span data-stu-id="19d86-301">In the case of an overflow, the values resulting from the inverse transform must wrap within the same number of bits.</span></span> <span data-ttu-id="19d86-302">如果 A0 的精確度為「p」個位元，其轉換演算法為︰</span><span class="sxs-lookup"><span data-stu-id="19d86-302">If the precision of A0 is "p" bits, then the transform algorithm is:</span></span>

`B0 = (B0 + A0) & ((1 << p) - 1)`

<span data-ttu-id="19d86-303">針對帶正負號的格式，delta 計算的結果也必須要進行正負號擴充。</span><span class="sxs-lookup"><span data-stu-id="19d86-303">For signed formats, the results of the delta calculation must be sign extended as well.</span></span> <span data-ttu-id="19d86-304">若正負號擴充運算意圖擴充兩種符號，而 0 代表正向，1 代表負向時，則 0 的正負號擴充會負責處理上述限制。</span><span class="sxs-lookup"><span data-stu-id="19d86-304">If the sign extension operation considers extending both signs, where 0 is positive and 1 is negative, then the sign extension of 0 takes care of the clamp above.</span></span> <span data-ttu-id="19d86-305">同樣的，在上述限制之後，只有數值為 1 (負向) 的才需要進行正負號擴充。</span><span class="sxs-lookup"><span data-stu-id="19d86-305">Equivalently, after the clamp above, only a value of 1 (negative) needs to be sign extended.</span></span>

## <a name="unquantization-of-color-endpoints"></a><span data-ttu-id="19d86-306">色彩端點的 Unquantization</span><span class="sxs-lookup"><span data-stu-id="19d86-306">Unquantization of Color Endpoints</span></span>

<span data-ttu-id="19d86-307">若給予未壓縮的端點，下一個步驟即是對色彩端點進行初步的取消量化。</span><span class="sxs-lookup"><span data-stu-id="19d86-307">Given the uncompressed endpoints, the next step is to perform an initial unquantization of the color endpoints.</span></span> <span data-ttu-id="19d86-308">這牽涉到三個步驟：</span><span class="sxs-lookup"><span data-stu-id="19d86-308">This involves three steps:</span></span>

-   <span data-ttu-id="19d86-309">取消量化色彩調色盤</span><span class="sxs-lookup"><span data-stu-id="19d86-309">An unquantization of the color palettes</span></span>
-   <span data-ttu-id="19d86-310">插補調色盤</span><span class="sxs-lookup"><span data-stu-id="19d86-310">Interpolation of the palettes</span></span>
-   <span data-ttu-id="19d86-311">完成取消量化</span><span class="sxs-lookup"><span data-stu-id="19d86-311">Unquantization finalization</span></span>

<span data-ttu-id="19d86-312">將取消量化的程序分成兩個部分 (插補調色盤前的取消量化色彩調色盤，及插補之後的完成取消量化)，相較於插補調色盤前就進行完整的取消量化程序，可以減少需要進行的乘法運算次數。</span><span class="sxs-lookup"><span data-stu-id="19d86-312">Separating the unquantization process into two parts (color palette unquantization before interpolation and final unquantization after interpolation) reduces the number of multiplication operations required when compared to a full unquantization process before palette interpolation.</span></span>

<span data-ttu-id="19d86-313">下方的程式碼示範了擷取原始 16 位元色彩的估計值，並且利用提供的權數值將 6 個額外的色彩值新增至調色盤中的程序。</span><span class="sxs-lookup"><span data-stu-id="19d86-313">The code below illustrates the process for retrieving estimates of the original 16-bit color values, and then using the supplied weight values to add 6 additional color values to the palette.</span></span> <span data-ttu-id="19d86-314">每個通道都會執行相同的作業。</span><span class="sxs-lookup"><span data-stu-id="19d86-314">The same operation is performed on each channel.</span></span>

``` syntax
int aWeight3[] = {0, 9, 18, 27, 37, 46, 55, 64};
int aWeight4[] = {0, 4, 9, 13, 17, 21, 26, 30, 34, 38, 43, 47, 51, 55, 60, 64};

// c1, c2: endpoints of a component
void generate_palette_unquantized(UINT8 uNumIndices, int c1, int c2, int prec, UINT16 palette[NINDICES])
{
    int* aWeights;
    if(uNumIndices == 8)
        aWeights = aWeight3;
    else  // uNumIndices == 16
        aWeights = aWeight4;

    int a = unquantize(c1, prec); 
    int b = unquantize(c2, prec);

    // interpolate
    for(int i = 0; i < uNumIndices; ++i)
        palette[i] = finish_unquantize((a * (64 - aWeights[i]) + b * aWeights[i] + 32) >> 6);
}
```

<span data-ttu-id="19d86-315">下一個程式碼範例示範了插補的程序，請觀察下列過程︰</span><span class="sxs-lookup"><span data-stu-id="19d86-315">The next code sample demonstrates the interpolation process, with the following observations:</span></span>

-   <span data-ttu-id="19d86-316">由於 **unquantize** 函式 (請參閱下方程式碼) 的色彩值完整範圍是從 -32768 到 65535，插補器即透過 17 位元帶正負號的算術進行實作。</span><span class="sxs-lookup"><span data-stu-id="19d86-316">Since the full range of color values for the **unquantize** function (below) are from -32768 to 65535, the interpolator is implemented using 17-bit signed arithmetic.</span></span>
-   <span data-ttu-id="19d86-317">在插補之後，會將這些值傳遞至 **finish \_ unquantize** 函式 (本節的第三個範例中所述) ，它會套用最後的調整。</span><span class="sxs-lookup"><span data-stu-id="19d86-317">After interpolation, the values are passed to the **finish\_unquantize** function (described in the third sample in this section), which applies the final scaling.</span></span>
-   <span data-ttu-id="19d86-318">所有硬體解壓縮程式在利用這些函式時，都必須傳回在位元上正確無誤的結果。</span><span class="sxs-lookup"><span data-stu-id="19d86-318">All hardware decompressors are required to return bit-accurate results with these functions.</span></span>

``` syntax
int unquantize(int comp, int uBitsPerComp)
{
    int unq, s = 0;
    switch(BC6H::FORMAT)
    {
    case UNSIGNED_F16:
        if(uBitsPerComp >= 15)
            unq = comp;
        else if(comp == 0)
            unq = 0;
        else if(comp == ((1 << uBitsPerComp) - 1))
            unq = 0xFFFF;
        else
            unq = ((comp << 16) + 0x8000) >> uBitsPerComp;
        break;

    case SIGNED_F16:
        if(uBitsPerComp >= 16)
            unq = comp;
        else
        {
            if(comp < 0)
            {
                s = 1;
                comp = -comp;
            }

            if(comp == 0)
                unq = 0;
            else if(comp >= ((1 << (uBitsPerComp - 1)) - 1))
                unq = 0x7FFF;
            else
                unq = ((comp << 15) + 0x4000) >> (uBitsPerComp-1);

            if(s)
                unq = -unq;
        }
        break;
    }
    return unq;
}
```

<span data-ttu-id="19d86-319">**完成 \_ unquantize** 是在調色板插補之後呼叫。</span><span class="sxs-lookup"><span data-stu-id="19d86-319">**finish\_unquantize** is called after palette interpolation.</span></span> <span data-ttu-id="19d86-320">**unquantize** 函式會針對帶正負號及不帶正負號的對象，分別以 31/32 及 31/64 延遲其縮放。</span><span class="sxs-lookup"><span data-stu-id="19d86-320">The **unquantize** function postpones the scaling by 31/32 for signed, 31/64 for unsigned.</span></span> <span data-ttu-id="19d86-321">為了在插補調色盤完成之後使最終數值落入一半的有效範圍 (-0x7BFF ~ 0x7BFF)，並且減少需要進行的乘法運算次數，此行為是必要的。</span><span class="sxs-lookup"><span data-stu-id="19d86-321">This behavior is required to get the final value into valid half range(-0x7BFF ~ 0x7BFF) after the palette interpolation is completed in order to reduce the number of necessary multiplications.</span></span> <span data-ttu-id="19d86-322">**finish \_ unquantize** 會套用最後的調整，並傳回不 **帶正負** 號的短值，讓重新解譯成為 **半**。</span><span class="sxs-lookup"><span data-stu-id="19d86-322">**finish\_unquantize** applies the final scaling and returns an **unsigned short** value that gets reinterpreted into **half**.</span></span>

``` syntax
unsigned short finish_unquantize(int comp)
{
    if(BC6H::FORMAT == UNSIGNED_F16)
    {
        comp = (comp * 31) >> 6;                                         // scale the magnitude by 31/64
        return (unsigned short) comp;
    }
    else // (BC6H::FORMAT == SIGNED_F16)
    {
        comp = (comp < 0) ? -(((-comp) * 31) >> 5) : (comp * 31) >> 5;   // scale the magnitude by 31/32
        int s = 0;
        if(comp < 0)
        {
            s = 0x8000;
            comp = -comp;
        }
        return (unsigned short) (s | comp);
    }
}
```

## <a name="related-topics"></a><span data-ttu-id="19d86-323">相關主題</span><span class="sxs-lookup"><span data-stu-id="19d86-323">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19d86-324">Direct3D 11 中的材質區塊壓縮</span><span class="sxs-lookup"><span data-stu-id="19d86-324">Texture Block Compression in Direct3D 11</span></span>](texture-block-compression-in-direct3d-11.md)
</dt> </dl>

 

 