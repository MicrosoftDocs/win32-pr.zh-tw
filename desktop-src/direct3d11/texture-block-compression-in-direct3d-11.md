---
title: Direct3D 11 中的材質區塊壓縮
description: 紋理的區塊壓縮 (BC) 支援在 Direct3D 11 中已進行擴充，內含 BC6H 和 BC7 演算法。
ms.assetid: E0735D4E-9C0F-45DC-854A-C27EB8367D86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f80a22c97c8a706a3825abfb4ac2b5133c1a9beb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092775"
---
# <a name="texture-block-compression-in-direct3d-11"></a><span data-ttu-id="68bb5-103">Direct3D 11 中的材質區塊壓縮</span><span class="sxs-lookup"><span data-stu-id="68bb5-103">Texture Block Compression in Direct3D 11</span></span>

<span data-ttu-id="68bb5-104">紋理的區塊壓縮 (BC) 支援在 Direct3D 11 中已進行擴充，內含 BC6H 和 BC7 演算法。</span><span class="sxs-lookup"><span data-stu-id="68bb5-104">Block Compression (BC) support for textures has been extended in Direct3D 11 to include the BC6H and BC7 algorithms.</span></span> <span data-ttu-id="68bb5-105">BC6H 支援高動態範圍色彩來源資料，而 BC7 使用較少的標準 RGB 來源資料成品，提供高於平均品質的壓縮。</span><span class="sxs-lookup"><span data-stu-id="68bb5-105">BC6H supports high-dynamic range color source data, and BC7 provides better-than-average quality compression with less artifacts for standard RGB source data.</span></span>

<span data-ttu-id="68bb5-106">如需關於 Direct3D 11 之前區塊壓縮演算法支援 (包括 BC1 到 BC5 格式的支援) 的相關詳細資訊，請參閱[區塊壓縮 (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression)。</span><span class="sxs-lookup"><span data-stu-id="68bb5-106">For more specific information about block compression algorithm support prior to Direct3D 11, including support for the BC1 through BC5 formats, see [Block Compression (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression).</span></span>

<span data-ttu-id="68bb5-107">**檔案格式的注意事項：** BC6H 和 BC7 材質壓縮格式會使用 DDS 檔案格式來儲存壓縮的材質資料。</span><span class="sxs-lookup"><span data-stu-id="68bb5-107">**Note about File Formats:** The BC6H and BC7 texture compression formats use the DDS file format for storing the compressed texture data.</span></span> <span data-ttu-id="68bb5-108">如需詳細資訊，請參閱[DDS 程式設計指南](/windows/desktop/direct3ddds/dx-graphics-dds-pguide)。</span><span class="sxs-lookup"><span data-stu-id="68bb5-108">For more information, see the [Programming Guide for DDS](/windows/desktop/direct3ddds/dx-graphics-dds-pguide) for details.</span></span>

## <a name="block-compression-formats-supported-in-direct3d-11"></a><span data-ttu-id="68bb5-109">Direct3D 11 支援的區塊壓縮格式</span><span class="sxs-lookup"><span data-stu-id="68bb5-109">Block Compression Formats Supported in Direct3D 11</span></span>



| <span data-ttu-id="68bb5-110">來源資料</span><span class="sxs-lookup"><span data-stu-id="68bb5-110">Source data</span></span>                                  | <span data-ttu-id="68bb5-111">資料壓縮解析度的最低需求</span><span class="sxs-lookup"><span data-stu-id="68bb5-111">Minimum required data compression resolution</span></span>                              | <span data-ttu-id="68bb5-112">建議格式</span><span class="sxs-lookup"><span data-stu-id="68bb5-112">Recommended format</span></span> | <span data-ttu-id="68bb5-113">最低支援的功能層級</span><span class="sxs-lookup"><span data-stu-id="68bb5-113">Minimum supported feature level</span></span> |
|----------------------------------------------|---------------------------------------------------------------------------|--------------------|---------------------------------|
| <span data-ttu-id="68bb5-114">帶有 Alpha 色板的三通道色彩</span><span class="sxs-lookup"><span data-stu-id="68bb5-114">Three-channel color with alpha channel</span></span>       | <span data-ttu-id="68bb5-115">帶有 0 或 1 個位元 Alpha 的三色彩通道 (5 個位元：6 個位元：5 個位元)</span><span class="sxs-lookup"><span data-stu-id="68bb5-115">Three color channels (5 bits:6 bits:5 bits), with 0 or 1 bit(s) of alpha</span></span>  | <span data-ttu-id="68bb5-116">BC1</span><span class="sxs-lookup"><span data-stu-id="68bb5-116">BC1</span></span>                | <span data-ttu-id="68bb5-117">Direct3D 9.1</span><span class="sxs-lookup"><span data-stu-id="68bb5-117">Direct3D 9.1</span></span>                    |
| <span data-ttu-id="68bb5-118">帶有 Alpha 色板的三通道色彩</span><span class="sxs-lookup"><span data-stu-id="68bb5-118">Three-channel color with alpha channel</span></span>       | <span data-ttu-id="68bb5-119">帶有 4 個位元 Alpha 的三色彩通道 (5 個位元：6 個位元：5 個位元)</span><span class="sxs-lookup"><span data-stu-id="68bb5-119">Three color channels (5 bits:6 bits:5 bits), with 4 bits of alpha</span></span>         | <span data-ttu-id="68bb5-120">BC2</span><span class="sxs-lookup"><span data-stu-id="68bb5-120">BC2</span></span>                | <span data-ttu-id="68bb5-121">Direct3D 9.1</span><span class="sxs-lookup"><span data-stu-id="68bb5-121">Direct3D 9.1</span></span>                    |
| <span data-ttu-id="68bb5-122">帶有 Alpha 色板的三通道色彩</span><span class="sxs-lookup"><span data-stu-id="68bb5-122">Three-channel color with alpha channel</span></span>       | <span data-ttu-id="68bb5-123">帶有 8 個位元 Alpha 的三色彩通道 (5 個位元：6 個位元：5 個位元)</span><span class="sxs-lookup"><span data-stu-id="68bb5-123">Three color channels (5 bits:6 bits:5 bits) with 8 bits of alpha</span></span>          | <span data-ttu-id="68bb5-124">BC3</span><span class="sxs-lookup"><span data-stu-id="68bb5-124">BC3</span></span>                | <span data-ttu-id="68bb5-125">Direct3D 9.1</span><span class="sxs-lookup"><span data-stu-id="68bb5-125">Direct3D 9.1</span></span>                    |
| <span data-ttu-id="68bb5-126">單一通道色彩</span><span class="sxs-lookup"><span data-stu-id="68bb5-126">One-channel color</span></span>                            | <span data-ttu-id="68bb5-127">單一色彩通道 (8 個位元)</span><span class="sxs-lookup"><span data-stu-id="68bb5-127">One color channel (8 bits)</span></span>                                                | <span data-ttu-id="68bb5-128">BC4</span><span class="sxs-lookup"><span data-stu-id="68bb5-128">BC4</span></span>                | <span data-ttu-id="68bb5-129">Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="68bb5-129">Direct3D 10</span></span>                     |
| <span data-ttu-id="68bb5-130">雙通道色彩</span><span class="sxs-lookup"><span data-stu-id="68bb5-130">Two-channel color</span></span>                            | <span data-ttu-id="68bb5-131">兩個色彩通道 (8 個位元：8 個位元)</span><span class="sxs-lookup"><span data-stu-id="68bb5-131">Two color channels (8 bits:8 bits)</span></span>                                        | <span data-ttu-id="68bb5-132">BC5</span><span class="sxs-lookup"><span data-stu-id="68bb5-132">BC5</span></span>                | <span data-ttu-id="68bb5-133">Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="68bb5-133">Direct3D 10</span></span>                     |
| <span data-ttu-id="68bb5-134">三通道高動態範圍 (HDR) 色彩</span><span class="sxs-lookup"><span data-stu-id="68bb5-134">Three-channel high dynamic range (HDR) color</span></span> | <span data-ttu-id="68bb5-135">三色通道 (16 位：16位：16位) "半" 浮點數\*</span><span class="sxs-lookup"><span data-stu-id="68bb5-135">Three color channels (16 bits:16 bits:16 bits) in "half" floating point\*</span></span> | <span data-ttu-id="68bb5-136">BC6H</span><span class="sxs-lookup"><span data-stu-id="68bb5-136">BC6H</span></span>               | <span data-ttu-id="68bb5-137">Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="68bb5-137">Direct3D 11</span></span>                     |
| <span data-ttu-id="68bb5-138">三通道色彩，及選擇性的 Alpha 色板</span><span class="sxs-lookup"><span data-stu-id="68bb5-138">Three-channel color, alpha channel optional</span></span>  | <span data-ttu-id="68bb5-139">帶有 0 到 8 個位元 Alpha 的三色彩通道 (每個通道 4 到 7 個位元)</span><span class="sxs-lookup"><span data-stu-id="68bb5-139">Three color channels (4 to 7 bits per channel) with 0 to 8 bits of alpha</span></span>  | <span data-ttu-id="68bb5-140">BC7</span><span class="sxs-lookup"><span data-stu-id="68bb5-140">BC7</span></span>                | <span data-ttu-id="68bb5-141">Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="68bb5-141">Direct3D 11</span></span>                     |



 

<span data-ttu-id="68bb5-142">\*「半」浮點數是16位值，其中包含選擇性的正負號位、5位偏差指數，以及10或11位尾數。</span><span class="sxs-lookup"><span data-stu-id="68bb5-142">\*"Half" floating point is a 16 bit value that consists of an optional sign bit, a 5 bit biased exponent, and a 10 or 11 bit mantissa.</span></span>

## <a name="bc1-bc2-and-b3-formats"></a><span data-ttu-id="68bb5-143">BC1、BC2，以及 B3 格式</span><span class="sxs-lookup"><span data-stu-id="68bb5-143">BC1, BC2, and B3 Formats</span></span>

<span data-ttu-id="68bb5-144">BC1、BC2，以及 BC3 格式對等於 Direct3D 9 DXTn 紋理壓縮格式，並且各自對應到 Direct3D 10 BC1、BC2，及 BC3 格式。</span><span class="sxs-lookup"><span data-stu-id="68bb5-144">The BC1, BC2, and BC3 formats are equivalent to the Direct3D 9 DXTn texture compression formats, and are the same as the corresponding Direct3D 10 BC1, BC2, and BC3 formats.</span></span> <span data-ttu-id="68bb5-145">所有功能層級都需要這三種格式的支援 (D3D \_ 功能 \_ 等級 \_ 9 \_ 1、d3d \_ 功能 \_ 層級 \_ 9 \_ 2、d3d \_ 功能 \_ 層級 \_ 9 \_ 3、d3d \_ 功能 \_ 等級 \_ 10 \_ 0、d3d \_ 功能 \_ 層級 \_ 10 \_ 1，以及 d3d \_ 功能 \_ 等級 \_ 11 \_ 0) 。</span><span class="sxs-lookup"><span data-stu-id="68bb5-145">Support for these three formats is required by all feature levels (D3D\_FEATURE\_LEVEL\_9\_1, D3D\_FEATURE\_LEVEL\_9\_2, D3D\_FEATURE\_LEVEL\_9\_3, D3D\_FEATURE\_LEVEL\_10\_0, D3D\_FEATURE\_LEVEL\_10\_1, and D3D\_FEATURE\_LEVEL\_11\_0).</span></span>



| <span data-ttu-id="68bb5-146">區塊壓縮格式</span><span class="sxs-lookup"><span data-stu-id="68bb5-146">Block compression format</span></span> | <span data-ttu-id="68bb5-147">DXGI 格式</span><span class="sxs-lookup"><span data-stu-id="68bb5-147">DXGI format</span></span>                                                                           | <span data-ttu-id="68bb5-148">Direct3D 9 對等格式</span><span class="sxs-lookup"><span data-stu-id="68bb5-148">Direct3D 9 equivalent format</span></span>                               | <span data-ttu-id="68bb5-149">每個 4 x 4 像素區塊的位元組</span><span class="sxs-lookup"><span data-stu-id="68bb5-149">Bytes per 4x4 pixel block</span></span> |
|--------------------------|---------------------------------------------------------------------------------------|------------------------------------------------------------|---------------------------|
| <span data-ttu-id="68bb5-150">BC1</span><span class="sxs-lookup"><span data-stu-id="68bb5-150">BC1</span></span>                      | <span data-ttu-id="68bb5-151">DXGI \_ 格式 \_ BC1 \_ UNORM、dxgi \_ 格式 \_ BC1 \_ UNORM \_ SRGB、dxgi \_ 格式 \_ BC1 無格式 \_</span><span class="sxs-lookup"><span data-stu-id="68bb5-151">DXGI\_FORMAT\_BC1\_UNORM, DXGI\_FORMAT\_BC1\_UNORM\_SRGB, DXGI\_FORMAT\_BC1\_TYPELESS</span></span> | <span data-ttu-id="68bb5-152">D3DFMT \_ DXT1，FourCC = "DXT1"</span><span class="sxs-lookup"><span data-stu-id="68bb5-152">D3DFMT\_DXT1, FourCC="DXT1"</span></span>                                | <span data-ttu-id="68bb5-153">8</span><span class="sxs-lookup"><span data-stu-id="68bb5-153">8</span></span>                         |
| <span data-ttu-id="68bb5-154">BC2</span><span class="sxs-lookup"><span data-stu-id="68bb5-154">BC2</span></span>                      | <span data-ttu-id="68bb5-155">DXGI \_ 格式 \_ BC2 \_ UNORM、dxgi \_ 格式 \_ BC2 \_ UNORM \_ SRGB、dxgi \_ 格式 \_ BC2 無格式 \_</span><span class="sxs-lookup"><span data-stu-id="68bb5-155">DXGI\_FORMAT\_BC2\_UNORM, DXGI\_FORMAT\_BC2\_UNORM\_SRGB, DXGI\_FORMAT\_BC2\_TYPELESS</span></span> | <span data-ttu-id="68bb5-156">D3DFMT \_ DXT2 \* 、FourCC = "DXT2"、D3DFMT \_ DXT3、FOURCC = "DXT3"</span><span class="sxs-lookup"><span data-stu-id="68bb5-156">D3DFMT\_DXT2\*, FourCC="DXT2", D3DFMT\_DXT3, FourCC="DXT3"</span></span> | <span data-ttu-id="68bb5-157">16</span><span class="sxs-lookup"><span data-stu-id="68bb5-157">16</span></span>                        |
| <span data-ttu-id="68bb5-158">BC3</span><span class="sxs-lookup"><span data-stu-id="68bb5-158">BC3</span></span>                      | <span data-ttu-id="68bb5-159">DXGI \_ 格式 \_ BC3 \_ UNORM、dxgi \_ 格式 \_ BC3 \_ UNORM \_ SRGB、dxgi \_ 格式 \_ BC3 無格式 \_</span><span class="sxs-lookup"><span data-stu-id="68bb5-159">DXGI\_FORMAT\_BC3\_UNORM, DXGI\_FORMAT\_BC3\_UNORM\_SRGB, DXGI\_FORMAT\_BC3\_TYPELESS</span></span> | <span data-ttu-id="68bb5-160">D3DFMT \_ DXT4 \* 、FourCC = "DXT4"、D3DFMT \_ DXT5、FOURCC = "DXT5"</span><span class="sxs-lookup"><span data-stu-id="68bb5-160">D3DFMT\_DXT4\*, FourCC="DXT4", D3DFMT\_DXT5, FourCC="DXT5"</span></span> | <span data-ttu-id="68bb5-161">16</span><span class="sxs-lookup"><span data-stu-id="68bb5-161">16</span></span>                        |



 

<span data-ttu-id="68bb5-162">\*這些壓縮配置 (DXT2 和 DXT4) 不區分 Direct3D 9 預乘的 Alpha 格式與標準的 Alpha 格式。</span><span class="sxs-lookup"><span data-stu-id="68bb5-162">\*These compression schemes (DXT2 and DXT4) make no distinction between the Direct3D 9 pre-multiplied alpha formats and the standard alpha formats.</span></span> <span data-ttu-id="68bb5-163">此區別必須透過可程式化著色器於轉譯時間中進行處理。</span><span class="sxs-lookup"><span data-stu-id="68bb5-163">This distinction must be handled by the programmable shaders at render time.</span></span>

## <a name="bc4-and-bc5-formats"></a><span data-ttu-id="68bb5-164">BC4 及 BC5 格式</span><span class="sxs-lookup"><span data-stu-id="68bb5-164">BC4 and BC5 Formats</span></span>



| <span data-ttu-id="68bb5-165">區塊壓縮格式</span><span class="sxs-lookup"><span data-stu-id="68bb5-165">Block compression format</span></span> | <span data-ttu-id="68bb5-166">DXGI 格式</span><span class="sxs-lookup"><span data-stu-id="68bb5-166">DXGI format</span></span>                                                                     | <span data-ttu-id="68bb5-167">Direct3D 9 對等格式</span><span class="sxs-lookup"><span data-stu-id="68bb5-167">Direct3D 9 equivalent format</span></span> | <span data-ttu-id="68bb5-168">每個 4 x 4 像素區塊的位元組</span><span class="sxs-lookup"><span data-stu-id="68bb5-168">Bytes per 4x4 pixel block</span></span> |
|--------------------------|---------------------------------------------------------------------------------|------------------------------|---------------------------|
| <span data-ttu-id="68bb5-169">BC4</span><span class="sxs-lookup"><span data-stu-id="68bb5-169">BC4</span></span>                      | <span data-ttu-id="68bb5-170">DXGI \_ 格式 \_ BC4 \_ UNORM、dxgi \_ 格式 \_ BC4 \_ SNORM、dxgi \_ 格式 \_ BC4 無格式 \_</span><span class="sxs-lookup"><span data-stu-id="68bb5-170">DXGI\_FORMAT\_BC4\_UNORM, DXGI\_FORMAT\_BC4\_SNORM, DXGI\_FORMAT\_BC4\_TYPELESS</span></span> | <span data-ttu-id="68bb5-171">FourCC="ATI1"</span><span class="sxs-lookup"><span data-stu-id="68bb5-171">FourCC="ATI1"</span></span>                | <span data-ttu-id="68bb5-172">8</span><span class="sxs-lookup"><span data-stu-id="68bb5-172">8</span></span>                         |
| <span data-ttu-id="68bb5-173">BC5</span><span class="sxs-lookup"><span data-stu-id="68bb5-173">BC5</span></span>                      | <span data-ttu-id="68bb5-174">DXGI \_ 格式 \_ BC5 \_ UNORM、dxgi \_ 格式 \_ BC5 \_ SNORM、dxgi \_ 格式 \_ BC5 無格式 \_</span><span class="sxs-lookup"><span data-stu-id="68bb5-174">DXGI\_FORMAT\_BC5\_UNORM, DXGI\_FORMAT\_BC5\_SNORM, DXGI\_FORMAT\_BC5\_TYPELESS</span></span> | <span data-ttu-id="68bb5-175">FourCC="ATI2"</span><span class="sxs-lookup"><span data-stu-id="68bb5-175">FourCC="ATI2"</span></span>                | <span data-ttu-id="68bb5-176">16</span><span class="sxs-lookup"><span data-stu-id="68bb5-176">16</span></span>                        |



 

## <a name="bc6h-format"></a><span data-ttu-id="68bb5-177">BC6H 格式</span><span class="sxs-lookup"><span data-stu-id="68bb5-177">BC6H Format</span></span>

<span data-ttu-id="68bb5-178">如需關於此格式的詳細資訊，請參閱[BC6H 格式](bc6h-format.md)文件。</span><span class="sxs-lookup"><span data-stu-id="68bb5-178">For more detailed information about this format, see the [BC6H Format](bc6h-format.md) documentation.</span></span>



| <span data-ttu-id="68bb5-179">區塊壓縮格式</span><span class="sxs-lookup"><span data-stu-id="68bb5-179">Block compression format</span></span> | <span data-ttu-id="68bb5-180">DXGI 格式</span><span class="sxs-lookup"><span data-stu-id="68bb5-180">DXGI format</span></span>                                                                      | <span data-ttu-id="68bb5-181">Direct3D 9 對等格式</span><span class="sxs-lookup"><span data-stu-id="68bb5-181">Direct3D 9 equivalent format</span></span> | <span data-ttu-id="68bb5-182">每個 4 x 4 像素區塊的位元組</span><span class="sxs-lookup"><span data-stu-id="68bb5-182">Bytes per 4x4 pixel block</span></span> |
|--------------------------|----------------------------------------------------------------------------------|------------------------------|---------------------------|
| <span data-ttu-id="68bb5-183">BC6H</span><span class="sxs-lookup"><span data-stu-id="68bb5-183">BC6H</span></span>                     | <span data-ttu-id="68bb5-184">DXGI \_ 格式 \_ BC6H \_ UF16、dxgi \_ 格式 \_ BC6H \_ SF16、dxgi \_ 格式 \_ BC6H 無格式 \_</span><span class="sxs-lookup"><span data-stu-id="68bb5-184">DXGI\_FORMAT\_BC6H\_UF16, DXGI\_FORMAT\_BC6H\_SF16, DXGI\_FORMAT\_BC6H\_TYPELESS</span></span> | <span data-ttu-id="68bb5-185">N/A</span><span class="sxs-lookup"><span data-stu-id="68bb5-185">N/A</span></span>                          | <span data-ttu-id="68bb5-186">16</span><span class="sxs-lookup"><span data-stu-id="68bb5-186">16</span></span>                        |



 

<span data-ttu-id="68bb5-187">BC6H 格式針對每個 4 x 4 的像素區塊可以選擇不同的編碼模式。</span><span class="sxs-lookup"><span data-stu-id="68bb5-187">The BC6H format can select different encoding modes for each 4x4 pixel block.</span></span> <span data-ttu-id="68bb5-188">共計有 14 個不同的編碼模式可以使用，每一種模式對於顯示紋理的最終視覺品質都有些許不同的取捨。</span><span class="sxs-lookup"><span data-stu-id="68bb5-188">A total of 14 different encoding modes are available, each with slightly different trade-offs in the resulting visual quality of the displayed texture.</span></span> <span data-ttu-id="68bb5-189">根據來源內容選擇或配合的品質等級，模式的選擇可允許硬體進行更快速的解碼，然而這也會大幅增加搜尋空間的複雜度。</span><span class="sxs-lookup"><span data-stu-id="68bb5-189">The choice of modes allows for fast decoding by the hardware with the quality level selected or adapted according to the source content, but it also greatly increases the complexity of the search space.</span></span>

## <a name="bc7-format"></a><span data-ttu-id="68bb5-190">BC7 格式</span><span class="sxs-lookup"><span data-stu-id="68bb5-190">BC7 Format</span></span>

<span data-ttu-id="68bb5-191">如需關於此格式的詳細資訊，請參閱[BC7 格式](bc7-format.md)文件。</span><span class="sxs-lookup"><span data-stu-id="68bb5-191">For more detailed information about this format, see the [BC7 Format](bc7-format.md) documentation.</span></span>



| <span data-ttu-id="68bb5-192">區塊壓縮格式</span><span class="sxs-lookup"><span data-stu-id="68bb5-192">Block compression format</span></span> | <span data-ttu-id="68bb5-193">DXGI 格式</span><span class="sxs-lookup"><span data-stu-id="68bb5-193">DXGI format</span></span>                                                                           | <span data-ttu-id="68bb5-194">Direct3D 9 對等格式</span><span class="sxs-lookup"><span data-stu-id="68bb5-194">Direct3D 9 equivalent format</span></span> | <span data-ttu-id="68bb5-195">每個 4 x 4 像素區塊的位元組</span><span class="sxs-lookup"><span data-stu-id="68bb5-195">Bytes per 4x4 pixel block</span></span> |
|--------------------------|---------------------------------------------------------------------------------------|------------------------------|---------------------------|
| <span data-ttu-id="68bb5-196">BC7</span><span class="sxs-lookup"><span data-stu-id="68bb5-196">BC7</span></span>                      | <span data-ttu-id="68bb5-197">DXGI \_ 格式 \_ BC7 \_ UNORM、dxgi \_ 格式 \_ BC7 \_ UNORM \_ SRGB、dxgi \_ 格式 \_ BC7 無格式 \_</span><span class="sxs-lookup"><span data-stu-id="68bb5-197">DXGI\_FORMAT\_BC7\_UNORM, DXGI\_FORMAT\_BC7\_UNORM\_SRGB, DXGI\_FORMAT\_BC7\_TYPELESS</span></span> | <span data-ttu-id="68bb5-198">N/A</span><span class="sxs-lookup"><span data-stu-id="68bb5-198">N/A</span></span>                          | <span data-ttu-id="68bb5-199">16</span><span class="sxs-lookup"><span data-stu-id="68bb5-199">16</span></span>                        |



 

<span data-ttu-id="68bb5-200">BC7 格式針對每個 4 x 4 的像素區塊可以選擇不同的編碼模式。</span><span class="sxs-lookup"><span data-stu-id="68bb5-200">The BC7 format can select different encoding modes for each 4x4 pixel block.</span></span> <span data-ttu-id="68bb5-201">共計有 8 個不同的編碼模式可以使用，每一種模式對於顯示紋理的最終視覺品質都有些許不同的取捨。</span><span class="sxs-lookup"><span data-stu-id="68bb5-201">A total of 8 different encoding modes are available, each with slightly different trade-offs in the resulting visual quality of the displayed texture.</span></span> <span data-ttu-id="68bb5-202">根據來源內容選擇或配合的品質等級，模式的選擇可允許硬體進行更快速的解碼，然而這也會大幅增加搜尋空間的複雜度。</span><span class="sxs-lookup"><span data-stu-id="68bb5-202">The choice of modes allows for fast decoding by the hardware with the quality level selected or adapted according to the source content, but it also greatly increases the complexity of the search space.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="68bb5-203">本節內容</span><span class="sxs-lookup"><span data-stu-id="68bb5-203">In this section</span></span>



| <span data-ttu-id="68bb5-204">主題</span><span class="sxs-lookup"><span data-stu-id="68bb5-204">Topic</span></span>                                                                 | <span data-ttu-id="68bb5-205">描述</span><span class="sxs-lookup"><span data-stu-id="68bb5-205">Description</span></span>                                                                                                                          |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="68bb5-206">BC6H 格式</span><span class="sxs-lookup"><span data-stu-id="68bb5-206">BC6H Format</span></span>](bc6h-format.md)<br/>                             | <span data-ttu-id="68bb5-207">BC6H 格式為一種設計用來支援來源資料中高動態範圍 (HDR) 色彩空間的紋理壓縮格式。</span><span class="sxs-lookup"><span data-stu-id="68bb5-207">The BC6H format is a texture compression format designed to support high-dynamic range (HDR) color spaces in source data.</span></span><br/> |
| [<span data-ttu-id="68bb5-208">BC7 格式</span><span class="sxs-lookup"><span data-stu-id="68bb5-208">BC7 Format</span></span>](bc7-format.md)<br/>                               | <span data-ttu-id="68bb5-209">BC7 格式是用於高品質 RGB 和 RGBA 資料壓縮的紋理壓縮格式。</span><span class="sxs-lookup"><span data-stu-id="68bb5-209">The BC7 format is a texture compression format used for high-quality compression of RGB and RGBA data.</span></span><br/>                    |
| [<span data-ttu-id="68bb5-210">BC7 格式模式參考</span><span class="sxs-lookup"><span data-stu-id="68bb5-210">BC7 Format Mode Reference</span></span>](bc7-format-mode-reference.md)<br/> | <span data-ttu-id="68bb5-211">本檔包含 BC7 材質壓縮格式區塊的8區塊模式和位配置清單。</span><span class="sxs-lookup"><span data-stu-id="68bb5-211">This documentation contains a list of the 8 block modes and bit allocations for BC7 texture compression format blocks.</span></span><br/>    |



 

## <a name="related-topics"></a><span data-ttu-id="68bb5-212">相關主題</span><span class="sxs-lookup"><span data-stu-id="68bb5-212">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68bb5-213"> (Direct3D 10) 封鎖壓縮 </span><span class="sxs-lookup"><span data-stu-id="68bb5-213">Block Compression (Direct3D 10)</span></span>](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression)
</dt> <dt>

[<span data-ttu-id="68bb5-214">紋理</span><span class="sxs-lookup"><span data-stu-id="68bb5-214">Textures</span></span>](overviews-direct3d-11-resources-textures.md)
</dt> </dl>

 

