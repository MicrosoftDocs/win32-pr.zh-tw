---
title: DDS 紋理範例
description: 若是未壓縮的材質，請使用 DDSD \_ 音調和 DDPF \_ RGB 旗標; 若為壓縮的材質，請使用 DDSD \_ LINEARSIZE 和 DDPF \_ FOURCC 旗標。
ms.assetid: 5bf54e8d-1dc5-4782-96c1-132d258fb560
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbaa6f86dddc7e60d7f41fc34d7c9fe994d50e4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968640"
---
# <a name="dds-texture-example"></a><span data-ttu-id="892be-103">DDS 紋理範例</span><span class="sxs-lookup"><span data-stu-id="892be-103">DDS Texture Example</span></span>

<span data-ttu-id="892be-104">若是未壓縮的材質，請使用 DDSD \_ 音調和 DDPF \_ RGB 旗標; 若為壓縮的材質，請使用 DDSD \_ LINEARSIZE 和 DDPF \_ FOURCC 旗標。</span><span class="sxs-lookup"><span data-stu-id="892be-104">For an uncompressed texture, use the DDSD\_PITCH and DDPF\_RGB flags; for a compressed texture, use the DDSD\_LINEARSIZE and DDPF\_FOURCC flags.</span></span> <span data-ttu-id="892be-105">針對 mipmapped 材質，請使用 DDSD \_ MIPMAPCOUNT、DDSCAPS \_ MIPMAP 和 DDSCAPS \_ 複雜旗標以及 MIPMAP count 成員。</span><span class="sxs-lookup"><span data-stu-id="892be-105">For a mipmapped texture, use the DDSD\_MIPMAPCOUNT, DDSCAPS\_MIPMAP, and DDSCAPS\_COMPLEX flags also as well as the mipmap count member.</span></span> <span data-ttu-id="892be-106">如果產生 mipmap，通常會寫入所有層級，直到1到1為止。</span><span class="sxs-lookup"><span data-stu-id="892be-106">If mipmaps are generated, all levels down to 1-by-1 are usually written.</span></span>

<span data-ttu-id="892be-107">針對壓縮的材質，每個 mipmap 層級影像的大小通常是先前大小的一四，最少為 8 (DXT1) 或 16 (DXT2-5) 位元組 (用於正方形紋理) 。</span><span class="sxs-lookup"><span data-stu-id="892be-107">For a compressed texture, the size of each mipmap level image is typically one-fourth the size of the previous, with a minimum of 8 (DXT1) or 16 (DXT2-5) bytes (for square textures).</span></span> <span data-ttu-id="892be-108">您可以使用下列公式來計算非正方形材質的每個層級大小：</span><span class="sxs-lookup"><span data-stu-id="892be-108">Use the following formula to calculate the size of each level for a non-square texture:</span></span>


```
max(1, ( (width + 3) / 4 ) ) x max(1, ( (height + 3) / 4 ) ) x 8(DXT1) or 16(DXT2-5)
```



<span data-ttu-id="892be-109">下表列出每個圖層針對 256 256 R8G8B8 材質所佔用的空間量，而不使用壓縮。</span><span class="sxs-lookup"><span data-stu-id="892be-109">This table lists the amount of space taken up by each layer for a 256-by-256 R8G8B8 texture, without using compression.</span></span>



| <span data-ttu-id="892be-110">DDS 元件</span><span class="sxs-lookup"><span data-stu-id="892be-110">DDS Components</span></span>          | <span data-ttu-id="892be-111">\# 位元組</span><span class="sxs-lookup"><span data-stu-id="892be-111">\# Bytes</span></span> |
|-------------------------|----------|
| <span data-ttu-id="892be-112">header</span><span class="sxs-lookup"><span data-stu-id="892be-112">header</span></span>                  | <span data-ttu-id="892be-113">128</span><span class="sxs-lookup"><span data-stu-id="892be-113">128</span></span>      |
| <span data-ttu-id="892be-114">256-256 的主要影像</span><span class="sxs-lookup"><span data-stu-id="892be-114">256-by-256 main image</span></span>   | <span data-ttu-id="892be-115">196608</span><span class="sxs-lookup"><span data-stu-id="892be-115">196608</span></span>   |
| <span data-ttu-id="892be-116">128-128 mipmap 影像</span><span class="sxs-lookup"><span data-stu-id="892be-116">128-by-128 mipmap image</span></span> | <span data-ttu-id="892be-117">49152</span><span class="sxs-lookup"><span data-stu-id="892be-117">49152</span></span>    |
| <span data-ttu-id="892be-118">64-64 mipmap 影像</span><span class="sxs-lookup"><span data-stu-id="892be-118">64-by-64 mipmap image</span></span>   | <span data-ttu-id="892be-119">12288</span><span class="sxs-lookup"><span data-stu-id="892be-119">12288</span></span>    |
| <span data-ttu-id="892be-120">32-32 mipmap 影像</span><span class="sxs-lookup"><span data-stu-id="892be-120">32-by-32 mipmap image</span></span>   | <span data-ttu-id="892be-121">3072</span><span class="sxs-lookup"><span data-stu-id="892be-121">3072</span></span>     |
| <span data-ttu-id="892be-122">16 x 16 mipmap 影像</span><span class="sxs-lookup"><span data-stu-id="892be-122">16-by-16 mipmap image</span></span>   | <span data-ttu-id="892be-123">768</span><span class="sxs-lookup"><span data-stu-id="892be-123">768</span></span>      |
| <span data-ttu-id="892be-124">8 x 8 mipmap 影像</span><span class="sxs-lookup"><span data-stu-id="892be-124">8-by-8 mipmap image</span></span>     | <span data-ttu-id="892be-125">192</span><span class="sxs-lookup"><span data-stu-id="892be-125">192</span></span>      |
| <span data-ttu-id="892be-126">四 mipmap 影像</span><span class="sxs-lookup"><span data-stu-id="892be-126">4-by-4 mipmap image</span></span>     | <span data-ttu-id="892be-127">48</span><span class="sxs-lookup"><span data-stu-id="892be-127">48</span></span>       |
| <span data-ttu-id="892be-128">2 mipmap 影像</span><span class="sxs-lookup"><span data-stu-id="892be-128">2-by-2 mipmap image</span></span>     | <span data-ttu-id="892be-129">12</span><span class="sxs-lookup"><span data-stu-id="892be-129">12</span></span>       |
| <span data-ttu-id="892be-130">1對 1 mipmap 影像</span><span class="sxs-lookup"><span data-stu-id="892be-130">1-by-1 mipmap image</span></span>     | <span data-ttu-id="892be-131">3</span><span class="sxs-lookup"><span data-stu-id="892be-131">3</span></span>        |



 

<span data-ttu-id="892be-132">下表列出使用壓縮 (DXT1) 的相同材質，各圖層所佔用的空間量。</span><span class="sxs-lookup"><span data-stu-id="892be-132">This table lists the amount of space taken up by each layer for the same texture using compression (DXT1).</span></span>



| <span data-ttu-id="892be-133">DDS 元件</span><span class="sxs-lookup"><span data-stu-id="892be-133">DDS Components</span></span>         | <span data-ttu-id="892be-134">\# 位元組</span><span class="sxs-lookup"><span data-stu-id="892be-134">\# Bytes</span></span> |
|------------------------|----------|
| <span data-ttu-id="892be-135">header</span><span class="sxs-lookup"><span data-stu-id="892be-135">header</span></span>                 | <span data-ttu-id="892be-136">128</span><span class="sxs-lookup"><span data-stu-id="892be-136">128</span></span>      |
| <span data-ttu-id="892be-137">256-64 的主要影像</span><span class="sxs-lookup"><span data-stu-id="892be-137">256-by-64 main image</span></span>   | <span data-ttu-id="892be-138">8192</span><span class="sxs-lookup"><span data-stu-id="892be-138">8192</span></span>     |
| <span data-ttu-id="892be-139">128-32 mipmap 影像</span><span class="sxs-lookup"><span data-stu-id="892be-139">128-by-32 mipmap image</span></span> | <span data-ttu-id="892be-140">2048</span><span class="sxs-lookup"><span data-stu-id="892be-140">2048</span></span>     |
| <span data-ttu-id="892be-141">64-16 mipmap 影像</span><span class="sxs-lookup"><span data-stu-id="892be-141">64-by-16 mipmap image</span></span>  | <span data-ttu-id="892be-142">512</span><span class="sxs-lookup"><span data-stu-id="892be-142">512</span></span>      |
| <span data-ttu-id="892be-143">32-8 mipmap 影像</span><span class="sxs-lookup"><span data-stu-id="892be-143">32-by-8 mipmap image</span></span>   | <span data-ttu-id="892be-144">128</span><span class="sxs-lookup"><span data-stu-id="892be-144">128</span></span>      |
| <span data-ttu-id="892be-145">16-4 mipmap 影像</span><span class="sxs-lookup"><span data-stu-id="892be-145">16-by-4 mipmap image</span></span>   | <span data-ttu-id="892be-146">32</span><span class="sxs-lookup"><span data-stu-id="892be-146">32</span></span>       |
| <span data-ttu-id="892be-147">每2個 mipmap 影像</span><span class="sxs-lookup"><span data-stu-id="892be-147">8-by-2 mipmap image</span></span>    | <span data-ttu-id="892be-148">16</span><span class="sxs-lookup"><span data-stu-id="892be-148">16</span></span>       |
| <span data-ttu-id="892be-149">mipmap 影像的 4 x 1</span><span class="sxs-lookup"><span data-stu-id="892be-149">4-by-1 mipmap image</span></span>    | <span data-ttu-id="892be-150">8</span><span class="sxs-lookup"><span data-stu-id="892be-150">8</span></span>        |
| <span data-ttu-id="892be-151">mipmap 影像</span><span class="sxs-lookup"><span data-stu-id="892be-151">2-by-1 mipmap image</span></span>    | <span data-ttu-id="892be-152">8</span><span class="sxs-lookup"><span data-stu-id="892be-152">8</span></span>        |
| <span data-ttu-id="892be-153">1對 1 mipmap 影像</span><span class="sxs-lookup"><span data-stu-id="892be-153">1-by-1 mipmap image</span></span>    | <span data-ttu-id="892be-154">8</span><span class="sxs-lookup"><span data-stu-id="892be-154">8</span></span>        |



 

<span data-ttu-id="892be-155">下表列出使用 DXGI 壓縮格式之相同材質的每個圖層所佔用的空間量 (在此案例中為 BC3 \_ UNORM) ，因此需要延伸標頭：</span><span class="sxs-lookup"><span data-stu-id="892be-155">This table lists the amount of space taken up by each layer for the same texture using a DXGI compression format (in this case BC3\_UNORM) that therefore requires the extended header:</span></span>



| <span data-ttu-id="892be-156">DDS 元件</span><span class="sxs-lookup"><span data-stu-id="892be-156">DDS Components</span></span>                                                | <span data-ttu-id="892be-157">\# 位元組</span><span class="sxs-lookup"><span data-stu-id="892be-157">\# Bytes</span></span> |
|---------------------------------------------------------------|----------|
| <span data-ttu-id="892be-158">標頭 (FourCC 設為 "DX10" ) </span><span class="sxs-lookup"><span data-stu-id="892be-158">header (FourCC set to "DX10")</span></span>                                 | <span data-ttu-id="892be-159">128</span><span class="sxs-lookup"><span data-stu-id="892be-159">128</span></span>      |
| <span data-ttu-id="892be-160">延伸標頭 (DXGI 格式設定為 DXGI \_ 格式 \_ BC3 \_ UNORM) </span><span class="sxs-lookup"><span data-stu-id="892be-160">extended header (DXGI format set to DXGI\_FORMAT\_BC3\_UNORM)</span></span> | <span data-ttu-id="892be-161">20</span><span class="sxs-lookup"><span data-stu-id="892be-161">20</span></span>       |
| <span data-ttu-id="892be-162">256-64 的主要影像</span><span class="sxs-lookup"><span data-stu-id="892be-162">256-by-64 main image</span></span>                                          | <span data-ttu-id="892be-163">16384</span><span class="sxs-lookup"><span data-stu-id="892be-163">16384</span></span>    |
| <span data-ttu-id="892be-164">128-32 mipmap 影像</span><span class="sxs-lookup"><span data-stu-id="892be-164">128-by-32 mipmap image</span></span>                                        | <span data-ttu-id="892be-165">4096</span><span class="sxs-lookup"><span data-stu-id="892be-165">4096</span></span>     |
| <span data-ttu-id="892be-166">64-16 mipmap 影像</span><span class="sxs-lookup"><span data-stu-id="892be-166">64-by-16 mipmap image</span></span>                                         | <span data-ttu-id="892be-167">1024</span><span class="sxs-lookup"><span data-stu-id="892be-167">1024</span></span>     |
| <span data-ttu-id="892be-168">32-8 mipmap 影像</span><span class="sxs-lookup"><span data-stu-id="892be-168">32-by-8 mipmap image</span></span>                                          | <span data-ttu-id="892be-169">256</span><span class="sxs-lookup"><span data-stu-id="892be-169">256</span></span>      |
| <span data-ttu-id="892be-170">16-4 mipmap 影像</span><span class="sxs-lookup"><span data-stu-id="892be-170">16-by-4 mipmap image</span></span>                                          | <span data-ttu-id="892be-171">64</span><span class="sxs-lookup"><span data-stu-id="892be-171">64</span></span>       |
| <span data-ttu-id="892be-172">每2個 mipmap 影像</span><span class="sxs-lookup"><span data-stu-id="892be-172">8-by-2 mipmap image</span></span>                                           | <span data-ttu-id="892be-173">32</span><span class="sxs-lookup"><span data-stu-id="892be-173">32</span></span>       |
| <span data-ttu-id="892be-174">mipmap 影像的 4 x 1</span><span class="sxs-lookup"><span data-stu-id="892be-174">4-by-1 mipmap image</span></span>                                           | <span data-ttu-id="892be-175">16</span><span class="sxs-lookup"><span data-stu-id="892be-175">16</span></span>       |
| <span data-ttu-id="892be-176">mipmap 影像</span><span class="sxs-lookup"><span data-stu-id="892be-176">2-by-1 mipmap image</span></span>                                           | <span data-ttu-id="892be-177">16</span><span class="sxs-lookup"><span data-stu-id="892be-177">16</span></span>       |
| <span data-ttu-id="892be-178">1對 1 mipmap 影像</span><span class="sxs-lookup"><span data-stu-id="892be-178">1-by-1 mipmap image</span></span>                                           | <span data-ttu-id="892be-179">16</span><span class="sxs-lookup"><span data-stu-id="892be-179">16</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="892be-180">相關主題</span><span class="sxs-lookup"><span data-stu-id="892be-180">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="892be-181">DDS 程式設計指南</span><span class="sxs-lookup"><span data-stu-id="892be-181">Programming Guide for DDS</span></span>](dx-graphics-dds-pguide.md)
</dt> </dl>

 

 




