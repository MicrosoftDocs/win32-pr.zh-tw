---
title: DDS Cube 對應範例
description: 針對三種環境對應，cube 的一或多個臉部會使用未壓縮或壓縮的格式寫入檔案，而且所有臉部都必須是相同的大小。
ms.assetid: a77234f6-ba10-40dd-902f-33e600384aa5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 235749bc0cf95a2e2120f66f3bcfb8a46e158628
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507296"
---
# <a name="dds-cube-map-example"></a><span data-ttu-id="54b34-103">DDS Cube 對應範例</span><span class="sxs-lookup"><span data-stu-id="54b34-103">DDS Cube Map Example</span></span>

<span data-ttu-id="54b34-104">針對三種環境對應，cube 的一或多個臉部會使用未壓縮或壓縮的格式寫入檔案，而且所有臉部都必須是相同的大小。</span><span class="sxs-lookup"><span data-stu-id="54b34-104">For cubic environment maps, one or more faces of a cube are written to the file, using either uncompressed or compressed formats, and all faces must be the same size.</span></span> <span data-ttu-id="54b34-105">每個臉部都可以定義 mipmap，不過所有臉部都必須有相同數目的 mipmap 層級。</span><span class="sxs-lookup"><span data-stu-id="54b34-105">Each face can have mipmaps defined, although all faces must have the same number of mipmap levels.</span></span> <span data-ttu-id="54b34-106">如果檔案包含 cube 對應， \_ 就必須設定 DDSCAPS COMPLEX、DDSCAPS2 \_ 立方體貼圖，以及一或多個 DSCAPS2 \_ 立方體貼圖 \_ POSITIVEX/y/z 及/或 DDSCAPS2 立方體貼圖 \_ \_ NEGATIVEX/y/z。</span><span class="sxs-lookup"><span data-stu-id="54b34-106">If a file contains a cube map, DDSCAPS\_COMPLEX, DDSCAPS2\_CUBEMAP, and one or more of DSCAPS2\_CUBEMAP\_POSITIVEX/Y/Z and/or DDSCAPS2\_CUBEMAP\_NEGATIVEX/Y/Z should be set.</span></span> <span data-ttu-id="54b34-107">臉部的寫入順序如下：正面 x、負 x、正 y、負 y、正 z、負 z，並省略任何遺漏的臉部。</span><span class="sxs-lookup"><span data-stu-id="54b34-107">The faces are written in the order: positive x, negative x, positive y, negative y, positive z, negative z, with any missing faces omitted.</span></span> <span data-ttu-id="54b34-108">每個臉部都會以其主要影像來寫入，後面接著任何 mipmap 層級。</span><span class="sxs-lookup"><span data-stu-id="54b34-108">Each face is written with its main image, followed by any mipmap levels.</span></span>

<span data-ttu-id="54b34-109">例如，具有正 x、負 y 和正 z 面的 256 256 cube 地圖、DXT1 的像素格式，以及所有 mipmap 層級都會包含下列各項：</span><span class="sxs-lookup"><span data-stu-id="54b34-109">For example, a 256-by-256 cube map with positive x, negative y, and positive z faces, a pixel format of DXT1, and all mipmap levels would contain the following:</span></span>



| <span data-ttu-id="54b34-110">DDS 元件</span><span class="sxs-lookup"><span data-stu-id="54b34-110">DDS Components</span></span>                                      | <span data-ttu-id="54b34-111">\# 位元組</span><span class="sxs-lookup"><span data-stu-id="54b34-111">\# Bytes</span></span> |
|-----------------------------------------------------|----------|
| <span data-ttu-id="54b34-112">header</span><span class="sxs-lookup"><span data-stu-id="54b34-112">header</span></span>                                              | <span data-ttu-id="54b34-113">128</span><span class="sxs-lookup"><span data-stu-id="54b34-113">128</span></span>      |
| <span data-ttu-id="54b34-114">256-256 正 x 主要影像</span><span class="sxs-lookup"><span data-stu-id="54b34-114">256-by-256 positive x main image</span></span>                    | <span data-ttu-id="54b34-115">32768</span><span class="sxs-lookup"><span data-stu-id="54b34-115">32768</span></span>    |
| <span data-ttu-id="54b34-116">128-128 正 x mipmap 影像</span><span class="sxs-lookup"><span data-stu-id="54b34-116">128-by-128 positive x mipmap image</span></span>                  | <span data-ttu-id="54b34-117">8192</span><span class="sxs-lookup"><span data-stu-id="54b34-117">8192</span></span>     |
| <span data-ttu-id="54b34-118">64-64 正 x mipmap 影像</span><span class="sxs-lookup"><span data-stu-id="54b34-118">64-by-64 positive x mipmap image</span></span>                    | <span data-ttu-id="54b34-119">2048</span><span class="sxs-lookup"><span data-stu-id="54b34-119">2048</span></span>     |
| <span data-ttu-id="54b34-120">32-32 正 x mipmap 影像</span><span class="sxs-lookup"><span data-stu-id="54b34-120">32-by-32 positive x mipmap image</span></span>                    | <span data-ttu-id="54b34-121">512</span><span class="sxs-lookup"><span data-stu-id="54b34-121">512</span></span>      |
| <span data-ttu-id="54b34-122">16×16正 x mipmap 影像</span><span class="sxs-lookup"><span data-stu-id="54b34-122">16-by-16 positive x mipmap image</span></span>                    | <span data-ttu-id="54b34-123">128</span><span class="sxs-lookup"><span data-stu-id="54b34-123">128</span></span>      |
| <span data-ttu-id="54b34-124">8 x 8 的正 x mipmap 影像</span><span class="sxs-lookup"><span data-stu-id="54b34-124">8-by-8 positive x mipmap image</span></span>                      | <span data-ttu-id="54b34-125">32</span><span class="sxs-lookup"><span data-stu-id="54b34-125">32</span></span>       |
| <span data-ttu-id="54b34-126">4 x 4 的正 x mipmap 影像</span><span class="sxs-lookup"><span data-stu-id="54b34-126">4-by-4 positive x mipmap image</span></span>                      | <span data-ttu-id="54b34-127">8</span><span class="sxs-lookup"><span data-stu-id="54b34-127">8</span></span>        |
| <span data-ttu-id="54b34-128">2×2的正 x mipmap 影像</span><span class="sxs-lookup"><span data-stu-id="54b34-128">2-by-2 positive x mipmap image</span></span>                      | <span data-ttu-id="54b34-129">8</span><span class="sxs-lookup"><span data-stu-id="54b34-129">8</span></span>        |
| <span data-ttu-id="54b34-130">1-1 個正 x mipmap 影像</span><span class="sxs-lookup"><span data-stu-id="54b34-130">1-by-1 positive x mipmap image</span></span>                      | <span data-ttu-id="54b34-131">8</span><span class="sxs-lookup"><span data-stu-id="54b34-131">8</span></span>        |
| <span data-ttu-id="54b34-132">針對 y mipmap 影像重複先前的9層</span><span class="sxs-lookup"><span data-stu-id="54b34-132">repeat the previous 9 layers for the y mipmap image</span></span> | <span data-ttu-id="54b34-133">43704</span><span class="sxs-lookup"><span data-stu-id="54b34-133">43704</span></span>    |
| <span data-ttu-id="54b34-134">針對 z mipmap 影像重複前9層</span><span class="sxs-lookup"><span data-stu-id="54b34-134">repeat the previous 9 layers for the z mipmap image</span></span> | <span data-ttu-id="54b34-135">43704</span><span class="sxs-lookup"><span data-stu-id="54b34-135">43704</span></span>    |



 

<span data-ttu-id="54b34-136">從 DirectX 8 開始，會儲存 cube 對應和所有定義的臉部。</span><span class="sxs-lookup"><span data-stu-id="54b34-136">Starting with DirectX 8, a cube map is stored with all faces defined.</span></span>

## <a name="dxgi-cube-maps"></a><span data-ttu-id="54b34-137">DXGI Cube 對應</span><span class="sxs-lookup"><span data-stu-id="54b34-137">DXGI Cube Maps</span></span>

<span data-ttu-id="54b34-138">Direct3D 10. x 和 Direct3D 11 中的三層環境對應相當於具有6個影像的2D 材質陣列，而且可以像這樣儲存在 DDS 檔案中。</span><span class="sxs-lookup"><span data-stu-id="54b34-138">Cubic environment maps in Direct3D 10.x and Direct3D 11 are equivalent to a 2D texture array with 6 images, and can be stored in DDS files as such.</span></span> <span data-ttu-id="54b34-139">使用 Direct3D 10.1 和 Direct3D 11 時，硬體也可以支援 cubemaps 陣列，也就是具有6個影像的倍數的2D 材質陣列 (6、12、18、24等 ) 。</span><span class="sxs-lookup"><span data-stu-id="54b34-139">With Direct3D 10.1 and Direct3D 11, the hardware can also support arrays of cubemaps which are themselves 2D texture arrays with a multiple of 6 images (6, 12, 18, 24, etc.).</span></span>

<span data-ttu-id="54b34-140">例如，以下是以 BC6H 格式儲存 mipmap 層級的256到256立方體貼圖，作為2D 材質陣列：</span><span class="sxs-lookup"><span data-stu-id="54b34-140">For example, here is a 256-by-256 cubemap with mipmap levels stored in a BC6H format as a 2D texture array:</span></span>



| <span data-ttu-id="54b34-141">DDS 元件</span><span class="sxs-lookup"><span data-stu-id="54b34-141">DDS Components</span></span>                                                                                                                                                                                                  | <span data-ttu-id="54b34-142">\# 位元組</span><span class="sxs-lookup"><span data-stu-id="54b34-142">\# Bytes</span></span> |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------|
| <span data-ttu-id="54b34-143">"DX10" 的標頭 (FourCC ) </span><span class="sxs-lookup"><span data-stu-id="54b34-143">header (FourCC of "DX10")</span></span>                                                                                                                                                                                       | <span data-ttu-id="54b34-144">128</span><span class="sxs-lookup"><span data-stu-id="54b34-144">128</span></span>      |
| <span data-ttu-id="54b34-145">延伸標頭 (DXGI 格式設定為 95 \[ dxgi \_ 格式 \_ BC6H \_ UF16 \] ，維度值為 3 \[ D3Dxx \_ 資源 \_ 維度 \_ TEXTURE2D \] ，陣列大小為6，其他旗標為 0x4 \[ D3Dxx \_ 資源 \_ 其他 \_ TEXTURECUBE \]) </span><span class="sxs-lookup"><span data-stu-id="54b34-145">extended header (DXGI format set to 95 \[DXGI\_FORMAT\_BC6H\_UF16\], dimension value of 3 \[D3Dxx\_RESOURCE\_DIMENSION\_TEXTURE2D\], array size of 6, misc flags of 0x4 \[D3Dxx\_RESOURCE\_MISC\_TEXTURECUBE\])</span></span> | <span data-ttu-id="54b34-146">20</span><span class="sxs-lookup"><span data-stu-id="54b34-146">20</span></span>       |
| <span data-ttu-id="54b34-147">256-256 陣列專案 0 (正 x) 主要影像</span><span class="sxs-lookup"><span data-stu-id="54b34-147">256-by-256 array entry 0 (positive x) main image</span></span>                                                                                                                                                                | <span data-ttu-id="54b34-148">65536</span><span class="sxs-lookup"><span data-stu-id="54b34-148">65536</span></span>    |
| <span data-ttu-id="54b34-149">128-128 陣列專案 0 (正 x) mipmap 影像</span><span class="sxs-lookup"><span data-stu-id="54b34-149">128-by-128 array entry 0 (positive x) mipmap image</span></span>                                                                                                                                                              | <span data-ttu-id="54b34-150">16384</span><span class="sxs-lookup"><span data-stu-id="54b34-150">16384</span></span>    |
| <span data-ttu-id="54b34-151">64-64 陣列專案 0 (正 x) mipmap 影像</span><span class="sxs-lookup"><span data-stu-id="54b34-151">64-by-64 array entry 0 (positive x) mipmap image</span></span>                                                                                                                                                                | <span data-ttu-id="54b34-152">4096</span><span class="sxs-lookup"><span data-stu-id="54b34-152">4096</span></span>     |
| <span data-ttu-id="54b34-153">32-32 陣列專案 0 (正 x) mipmap 影像</span><span class="sxs-lookup"><span data-stu-id="54b34-153">32-by-32 array entry 0 (positive x) mipmap image</span></span>                                                                                                                                                                | <span data-ttu-id="54b34-154">1024</span><span class="sxs-lookup"><span data-stu-id="54b34-154">1024</span></span>     |
| <span data-ttu-id="54b34-155">16×16個數組專案 0 (正 x) mipmap 影像</span><span class="sxs-lookup"><span data-stu-id="54b34-155">16-by-16 array entry 0 (positive x) mipmap image</span></span>                                                                                                                                                                | <span data-ttu-id="54b34-156">256</span><span class="sxs-lookup"><span data-stu-id="54b34-156">256</span></span>      |
| <span data-ttu-id="54b34-157">8 x 8 的陣列專案 0 (正 x) mipmap 影像</span><span class="sxs-lookup"><span data-stu-id="54b34-157">8-by-8 array entry 0 (positive x) mipmap image</span></span>                                                                                                                                                                  | <span data-ttu-id="54b34-158">64</span><span class="sxs-lookup"><span data-stu-id="54b34-158">64</span></span>       |
| <span data-ttu-id="54b34-159">4 x 4 陣列專案 0 (正 x) mipmap 影像</span><span class="sxs-lookup"><span data-stu-id="54b34-159">4-by-4 array entry 0 (positive x) mipmap image</span></span>                                                                                                                                                                  | <span data-ttu-id="54b34-160">16</span><span class="sxs-lookup"><span data-stu-id="54b34-160">16</span></span>       |
| <span data-ttu-id="54b34-161">2到2個數組專案 0 (正 x) mipmap 影像</span><span class="sxs-lookup"><span data-stu-id="54b34-161">2-by-2 array entry 0 (positive x) mipmap image</span></span>                                                                                                                                                                  | <span data-ttu-id="54b34-162">16</span><span class="sxs-lookup"><span data-stu-id="54b34-162">16</span></span>       |
| <span data-ttu-id="54b34-163">1-1 個數組專案 0 (正 x) mipmap 影像</span><span class="sxs-lookup"><span data-stu-id="54b34-163">1-by-1 array entry 0 (positive x) mipmap image</span></span>                                                                                                                                                                  | <span data-ttu-id="54b34-164">16</span><span class="sxs-lookup"><span data-stu-id="54b34-164">16</span></span>       |
| <span data-ttu-id="54b34-165">針對陣列專案1重複前9層 (負 x) mipmap 影像</span><span class="sxs-lookup"><span data-stu-id="54b34-165">repeat the previous 9 layers for array entry 1 (negative x) mipmap image</span></span>                                                                                                                                        | <span data-ttu-id="54b34-166">87408</span><span class="sxs-lookup"><span data-stu-id="54b34-166">87408</span></span>    |
| <span data-ttu-id="54b34-167">針對陣列專案2，重複前9個圖層 (正 y) mipmap 影像</span><span class="sxs-lookup"><span data-stu-id="54b34-167">repeat the previous 9 layers for array entry 2 (positive y) mipmap image</span></span>                                                                                                                                        | <span data-ttu-id="54b34-168">87408</span><span class="sxs-lookup"><span data-stu-id="54b34-168">87408</span></span>    |
| <span data-ttu-id="54b34-169">針對陣列專案 3 (負 y) mipmap 影像重複前9個圖層</span><span class="sxs-lookup"><span data-stu-id="54b34-169">repeat the previous 9 layers for array entry 3 (negative y) mipmap image</span></span>                                                                                                                                        | <span data-ttu-id="54b34-170">87408</span><span class="sxs-lookup"><span data-stu-id="54b34-170">87408</span></span>    |
| <span data-ttu-id="54b34-171">針對陣列專案4，重複前9個圖層 (正 z) mipmap 影像</span><span class="sxs-lookup"><span data-stu-id="54b34-171">repeat the previous 9 layers for array entry 4 (positive z) mipmap image</span></span>                                                                                                                                        | <span data-ttu-id="54b34-172">87408</span><span class="sxs-lookup"><span data-stu-id="54b34-172">87408</span></span>    |
| <span data-ttu-id="54b34-173">針對陣列專案5重複前9層 (負 z) mipmap 影像</span><span class="sxs-lookup"><span data-stu-id="54b34-173">repeat the previous 9 layers for array entry 5 (negative z) mipmap image</span></span>                                                                                                                                        | <span data-ttu-id="54b34-174">87408</span><span class="sxs-lookup"><span data-stu-id="54b34-174">87408</span></span>    |



 

## <a name="related-topics"></a><span data-ttu-id="54b34-175">相關主題</span><span class="sxs-lookup"><span data-stu-id="54b34-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54b34-176">DDS 程式設計指南</span><span class="sxs-lookup"><span data-stu-id="54b34-176">Programming Guide for DDS</span></span>](dx-graphics-dds-pguide.md)
</dt> </dl>

 

 




