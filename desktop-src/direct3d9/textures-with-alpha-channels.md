---
description: 有兩種方式可以對呈現較複雜透明度的材質貼圖進行編碼。
ms.assetid: cae788f6-60f1-4987-8f06-bf4256bccd9b
title: '具有 Alpha 通道的材質 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c361b0335ef4f36b4efc9c90c71270e855f5db
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104555008"
---
# <a name="textures-with-alpha-channels-direct3d-9"></a><span data-ttu-id="45c50-103">具有 Alpha 通道的材質 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="45c50-103">Textures with Alpha Channels (Direct3D 9)</span></span>

<span data-ttu-id="45c50-104">有兩種方式可以對呈現較複雜透明度的材質貼圖進行編碼。</span><span class="sxs-lookup"><span data-stu-id="45c50-104">There are two ways to encode texture maps that exhibit more complex transparency.</span></span> <span data-ttu-id="45c50-105">在每個例子中，描述透明度的區塊都會優先於之前已描述完成的 64 位元區塊。</span><span class="sxs-lookup"><span data-stu-id="45c50-105">In each case, a block that describes the transparency precedes the 64-bit block already described.</span></span> <span data-ttu-id="45c50-106">透明度通常不是透過每像素 4 個位元 (明確編碼) 的 4 x 4 點陣圖呈現，就是透過較少位元並且類比於色彩編碼的線性插補呈現。</span><span class="sxs-lookup"><span data-stu-id="45c50-106">The transparency is either represented as a 4x4 bitmap with 4 bits per pixel (explicit encoding), or with fewer bits and linear interpolation that is analogous to what is used for color encoding.</span></span>

<span data-ttu-id="45c50-107">透明度區塊及色彩區塊會如下表所示進行排列。</span><span class="sxs-lookup"><span data-stu-id="45c50-107">The transparency block and the color block are arranged as shown in the following table.</span></span>



| <span data-ttu-id="45c50-108">單字位址</span><span class="sxs-lookup"><span data-stu-id="45c50-108">Word address</span></span> | <span data-ttu-id="45c50-109">64 位元區塊</span><span class="sxs-lookup"><span data-stu-id="45c50-109">64-bit block</span></span>                      |
|--------------|-----------------------------------|
| <span data-ttu-id="45c50-110">3:0</span><span class="sxs-lookup"><span data-stu-id="45c50-110">3:0</span></span>          | <span data-ttu-id="45c50-111">透明度區塊</span><span class="sxs-lookup"><span data-stu-id="45c50-111">Transparency block</span></span>                |
| <span data-ttu-id="45c50-112">7:4</span><span class="sxs-lookup"><span data-stu-id="45c50-112">7:4</span></span>          | <span data-ttu-id="45c50-113">之前已描述完成的 64 位元區塊</span><span class="sxs-lookup"><span data-stu-id="45c50-113">Previously described 64-bit block</span></span> |



 

## <a name="explicit-texture-encoding"></a><span data-ttu-id="45c50-114">明確材質編碼</span><span class="sxs-lookup"><span data-stu-id="45c50-114">Explicit Texture Encoding</span></span>

<span data-ttu-id="45c50-115">針對 (DXT2 和 DXT3 格式的明確材質編碼) ，描述透明度之材質的 Alpha 元件會編碼為每個材質4個位的4x4 點陣圖。</span><span class="sxs-lookup"><span data-stu-id="45c50-115">For explicit texture encoding (DXT2 and DXT3 formats), the alpha components of the texels that describe transparency are encoded in a 4x4 bitmap with 4 bits per texel.</span></span> <span data-ttu-id="45c50-116">這四個位元可透過不同的方式達成，例如：遞色，或是使用 Alpha 資料中最高有效的四個位元。</span><span class="sxs-lookup"><span data-stu-id="45c50-116">These four bits can be achieved through a variety of means such as dithering or by using the four most significant bits of the alpha data.</span></span> <span data-ttu-id="45c50-117">無論其產生方式為何，其會直接使用於程式之中，而不會有任何型式的插補。</span><span class="sxs-lookup"><span data-stu-id="45c50-117">However they are produced, they are used just as they are, without any form of interpolation.</span></span>

<span data-ttu-id="45c50-118">下列簡圖呈現了一個 64 位元的透明度區塊。</span><span class="sxs-lookup"><span data-stu-id="45c50-118">The following diagram shows a 64-bit transparency block.</span></span>

![64 位元透明度區塊的簡圖](images/colors4.png)

> [!Note]  
> <span data-ttu-id="45c50-120">Direct3D 的壓縮方法會使用四個最重要的位。</span><span class="sxs-lookup"><span data-stu-id="45c50-120">The compression method of Direct3D uses the four most significant bits.</span></span>

 

<span data-ttu-id="45c50-121">下表描述了如何在記憶體中，針對每個 16 位元文字配置 Alpha 資訊。</span><span class="sxs-lookup"><span data-stu-id="45c50-121">The following tables illustrate how the alpha information is laid out in memory, for each 16-bit word.</span></span>

<span data-ttu-id="45c50-122">此資料表包含 word 0 的版面配置。</span><span class="sxs-lookup"><span data-stu-id="45c50-122">This table contains the layout for word 0.</span></span>



| <span data-ttu-id="45c50-123">Bits</span><span class="sxs-lookup"><span data-stu-id="45c50-123">Bits</span></span>          | <span data-ttu-id="45c50-124">Alpha</span><span class="sxs-lookup"><span data-stu-id="45c50-124">Alpha</span></span>      |
|---------------|------------|
| <span data-ttu-id="45c50-125">3:0 (LSB \*) </span><span class="sxs-lookup"><span data-stu-id="45c50-125">3:0 (LSB\*)</span></span>   | <span data-ttu-id="45c50-126">\[0 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="45c50-126">\[0\]\[0\]</span></span> |
| <span data-ttu-id="45c50-127">7:4</span><span class="sxs-lookup"><span data-stu-id="45c50-127">7:4</span></span>           | <span data-ttu-id="45c50-128">\[0 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="45c50-128">\[0\]\[1\]</span></span> |
| <span data-ttu-id="45c50-129">11:8</span><span class="sxs-lookup"><span data-stu-id="45c50-129">11:8</span></span>          | <span data-ttu-id="45c50-130">\[0 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="45c50-130">\[0\]\[2\]</span></span> |
| <span data-ttu-id="45c50-131">15:12 (MSB \*) </span><span class="sxs-lookup"><span data-stu-id="45c50-131">15:12 (MSB\*)</span></span> | <span data-ttu-id="45c50-132">\[0 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="45c50-132">\[0\]\[3\]</span></span> |



 

<span data-ttu-id="45c50-133">\*最重要的 bit、最重要的位 (MSB) </span><span class="sxs-lookup"><span data-stu-id="45c50-133">\*least-significant bit, most significant bit (MSB)</span></span>

<span data-ttu-id="45c50-134">此資料表包含 word 1 的版面配置。</span><span class="sxs-lookup"><span data-stu-id="45c50-134">This table contains the layout for word 1.</span></span>



| <span data-ttu-id="45c50-135">Bits</span><span class="sxs-lookup"><span data-stu-id="45c50-135">Bits</span></span>        | <span data-ttu-id="45c50-136">Alpha</span><span class="sxs-lookup"><span data-stu-id="45c50-136">Alpha</span></span>      |
|-------------|------------|
| <span data-ttu-id="45c50-137">3:0 (LSB)</span><span class="sxs-lookup"><span data-stu-id="45c50-137">3:0 (LSB)</span></span>   | <span data-ttu-id="45c50-138">\[1 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="45c50-138">\[1\]\[0\]</span></span> |
| <span data-ttu-id="45c50-139">7:4</span><span class="sxs-lookup"><span data-stu-id="45c50-139">7:4</span></span>         | <span data-ttu-id="45c50-140">\[1 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="45c50-140">\[1\]\[1\]</span></span> |
| <span data-ttu-id="45c50-141">11:8</span><span class="sxs-lookup"><span data-stu-id="45c50-141">11:8</span></span>        | <span data-ttu-id="45c50-142">\[1 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="45c50-142">\[1\]\[2\]</span></span> |
| <span data-ttu-id="45c50-143">15:12 (MSB)</span><span class="sxs-lookup"><span data-stu-id="45c50-143">15:12 (MSB)</span></span> | <span data-ttu-id="45c50-144">\[1 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="45c50-144">\[1\]\[3\]</span></span> |



 

<span data-ttu-id="45c50-145">此資料表包含 word 2 的版面配置。</span><span class="sxs-lookup"><span data-stu-id="45c50-145">This table contains the layout for word 2.</span></span>



| <span data-ttu-id="45c50-146">Bits</span><span class="sxs-lookup"><span data-stu-id="45c50-146">Bits</span></span>        | <span data-ttu-id="45c50-147">Alpha</span><span class="sxs-lookup"><span data-stu-id="45c50-147">Alpha</span></span>      |
|-------------|------------|
| <span data-ttu-id="45c50-148">3:0 (LSB)</span><span class="sxs-lookup"><span data-stu-id="45c50-148">3:0 (LSB)</span></span>   | <span data-ttu-id="45c50-149">\[2 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="45c50-149">\[2\]\[0\]</span></span> |
| <span data-ttu-id="45c50-150">7:4</span><span class="sxs-lookup"><span data-stu-id="45c50-150">7:4</span></span>         | <span data-ttu-id="45c50-151">\[2 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="45c50-151">\[2\]\[1\]</span></span> |
| <span data-ttu-id="45c50-152">11:8</span><span class="sxs-lookup"><span data-stu-id="45c50-152">11:8</span></span>        | <span data-ttu-id="45c50-153">\[2 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="45c50-153">\[2\]\[2\]</span></span> |
| <span data-ttu-id="45c50-154">15:12 (MSB)</span><span class="sxs-lookup"><span data-stu-id="45c50-154">15:12 (MSB)</span></span> | <span data-ttu-id="45c50-155">\[2 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="45c50-155">\[2\]\[3\]</span></span> |



 

<span data-ttu-id="45c50-156">此資料表包含 word 3 的版面配置。</span><span class="sxs-lookup"><span data-stu-id="45c50-156">This table contains the layout for word 3.</span></span>



| <span data-ttu-id="45c50-157">Bits</span><span class="sxs-lookup"><span data-stu-id="45c50-157">Bits</span></span>        | <span data-ttu-id="45c50-158">Alpha</span><span class="sxs-lookup"><span data-stu-id="45c50-158">Alpha</span></span>      |
|-------------|------------|
| <span data-ttu-id="45c50-159">3:0 (LSB)</span><span class="sxs-lookup"><span data-stu-id="45c50-159">3:0 (LSB)</span></span>   | <span data-ttu-id="45c50-160">\[3 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="45c50-160">\[3\]\[0\]</span></span> |
| <span data-ttu-id="45c50-161">7:4</span><span class="sxs-lookup"><span data-stu-id="45c50-161">7:4</span></span>         | <span data-ttu-id="45c50-162">\[3 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="45c50-162">\[3\]\[1\]</span></span> |
| <span data-ttu-id="45c50-163">11:8</span><span class="sxs-lookup"><span data-stu-id="45c50-163">11:8</span></span>        | <span data-ttu-id="45c50-164">\[3 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="45c50-164">\[3\]\[2\]</span></span> |
| <span data-ttu-id="45c50-165">15:12 (MSB)</span><span class="sxs-lookup"><span data-stu-id="45c50-165">15:12 (MSB)</span></span> | <span data-ttu-id="45c50-166">\[3 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="45c50-166">\[3\]\[3\]</span></span> |



 

<span data-ttu-id="45c50-167">DXT2 和 DXT3 之間的差異在於，使用 DXT2 格式時，會假設色彩資料已由 Alpha 預乘。</span><span class="sxs-lookup"><span data-stu-id="45c50-167">The difference between DXT2 and DXT3 are that, in the DXT2 format, it is assumed that the color data has been premultiplied by alpha.</span></span> <span data-ttu-id="45c50-168">使用 DXT3 格式時，會假設色彩不會以 Alpha 預乘。</span><span class="sxs-lookup"><span data-stu-id="45c50-168">In the DXT3 format, it is assumed that the color is not premultiplied by alpha.</span></span> <span data-ttu-id="45c50-169">這兩種格式是需要的，因為在大部分情況下，使用材質時，檢查資料是否不足以判斷色彩值是否已乘以 Alpha。</span><span class="sxs-lookup"><span data-stu-id="45c50-169">These two formats are needed because, in most cases, by the time a texture is used, just examining the data is not sufficient to determine if the color values have been multiplied by alpha.</span></span> <span data-ttu-id="45c50-170">因為在執行時間需要這項資訊，所以會使用兩個 FOURCC 碼來區分這些情況。</span><span class="sxs-lookup"><span data-stu-id="45c50-170">Because this information is needed at run time, the two FOURCC codes are used to differentiate these cases.</span></span> <span data-ttu-id="45c50-171">不過，這兩種格式所使用的資料和插補方法相同。</span><span class="sxs-lookup"><span data-stu-id="45c50-171">However, the data and interpolation method used for these two formats is identical.</span></span>

<span data-ttu-id="45c50-172">DXT1 中使用的色彩比較，可判斷材質是否為透明的，不會使用此格式。</span><span class="sxs-lookup"><span data-stu-id="45c50-172">The color compare used in DXT1 to determine if the texel is transparent is not used in this format.</span></span> <span data-ttu-id="45c50-173">若不使用色彩比較，色彩資料預設會以 4 色模式進行處理。</span><span class="sxs-lookup"><span data-stu-id="45c50-173">It is assumed that without the color compare the color data is always treated as if in 4-color mode.</span></span> <span data-ttu-id="45c50-174">換句話說，DXT1 程式碼頂端的 if 語句應如下所示：</span><span class="sxs-lookup"><span data-stu-id="45c50-174">In other words, the if statement at the top of the DXT1 code should be the following:</span></span>


```
if ((color_0 > color_1) OR !DXT1) {
```



## <a name="three-bit-linear-alpha-interpolation"></a><span data-ttu-id="45c50-175">Three-Bit 線性 Alpha 插補</span><span class="sxs-lookup"><span data-stu-id="45c50-175">Three-Bit Linear Alpha Interpolation</span></span>

<span data-ttu-id="45c50-176">DXT4 和 DXT5 格式的透明度編碼是以類似于色彩使用的線性編碼的概念為基礎。</span><span class="sxs-lookup"><span data-stu-id="45c50-176">The encoding of transparency for the DXT4 and DXT5 formats is based on a concept similar to the linear encoding used for color.</span></span> <span data-ttu-id="45c50-177">兩個 8 位元 Alpha 值和一個每個像素中有三個位元的 4 x 4 點陣圖，會儲存於區塊中前八個位元組。</span><span class="sxs-lookup"><span data-stu-id="45c50-177">Two 8-bit alpha values and a 4x4 bitmap with three bits per pixel are stored in the first eight bytes of the block.</span></span> <span data-ttu-id="45c50-178">代表 Alpha 值會作為插補中繼 Alpha 值之用途使用。</span><span class="sxs-lookup"><span data-stu-id="45c50-178">The representative alpha values are used to interpolate intermediate alpha values.</span></span> <span data-ttu-id="45c50-179">其他資訊會以兩個 Alpha 值儲存的方式供作使用。</span><span class="sxs-lookup"><span data-stu-id="45c50-179">Additional information is available in the way the two alpha values are stored.</span></span> <span data-ttu-id="45c50-180">如果 Alpha \_ 0 大於 Alpha \_ 1，則插補會建立六個中間 Alpha 值。</span><span class="sxs-lookup"><span data-stu-id="45c50-180">If alpha\_0 is greater than alpha\_1, then six intermediate alpha values are created by the interpolation.</span></span> <span data-ttu-id="45c50-181">若為小於，則四個中繼 Alpha 值會插補於指定的 Alpha 極端值之間。</span><span class="sxs-lookup"><span data-stu-id="45c50-181">Otherwise, four intermediate alpha values are interpolated between the specified alpha extremes.</span></span> <span data-ttu-id="45c50-182">另外兩個額外隱含 Alpha 值則為 0 (完全透明) 及 255 (完全不透明)。</span><span class="sxs-lookup"><span data-stu-id="45c50-182">The two additional implicit alpha values are 0 (fully transparent) and 255 (fully opaque).</span></span>

<span data-ttu-id="45c50-183">下列程式碼示範了這個演算法。</span><span class="sxs-lookup"><span data-stu-id="45c50-183">The following code example illustrates this algorithm.</span></span>


```
// 8-alpha or 6-alpha block?    
if (alpha_0 > alpha_1) {    
    // 8-alpha block:  derive the other six alphas.    
    // Bit code 000 = alpha_0, 001 = alpha_1, others are interpolated.
    alpha_2 = (6 * alpha_0 + 1 * alpha_1 + 3) / 7;    // bit code 010
    alpha_3 = (5 * alpha_0 + 2 * alpha_1 + 3) / 7;    // bit code 011
    alpha_4 = (4 * alpha_0 + 3 * alpha_1 + 3) / 7;    // bit code 100
    alpha_5 = (3 * alpha_0 + 4 * alpha_1 + 3) / 7;    // bit code 101
    alpha_6 = (2 * alpha_0 + 5 * alpha_1 + 3) / 7;    // bit code 110
    alpha_7 = (1 * alpha_0 + 6 * alpha_1 + 3) / 7;    // bit code 111  
}    
else {  
    // 6-alpha block.    
    // Bit code 000 = alpha_0, 001 = alpha_1, others are interpolated.
    alpha_2 = (4 * alpha_0 + 1 * alpha_1 + 2) / 5;    // Bit code 010
    alpha_3 = (3 * alpha_0 + 2 * alpha_1 + 2) / 5;    // Bit code 011
    alpha_4 = (2 * alpha_0 + 3 * alpha_1 + 2) / 5;    // Bit code 100
    alpha_5 = (1 * alpha_0 + 4 * alpha_1 + 2) / 5;    // Bit code 101
    alpha_6 = 0;                                      // Bit code 110
    alpha_7 = 255;                                    // Bit code 111
}
```



<span data-ttu-id="45c50-184">Alpha 區塊的記憶體配置如下︰</span><span class="sxs-lookup"><span data-stu-id="45c50-184">The memory layout of the alpha block is as follows:</span></span>



| <span data-ttu-id="45c50-185">Byte</span><span class="sxs-lookup"><span data-stu-id="45c50-185">Byte</span></span> | <span data-ttu-id="45c50-186">Alpha</span><span class="sxs-lookup"><span data-stu-id="45c50-186">Alpha</span></span>                                                          |
|------|----------------------------------------------------------------|
| <span data-ttu-id="45c50-187">0</span><span class="sxs-lookup"><span data-stu-id="45c50-187">0</span></span>    | <span data-ttu-id="45c50-188">Alpha \_ 0</span><span class="sxs-lookup"><span data-stu-id="45c50-188">Alpha\_0</span></span>                                                       |
| <span data-ttu-id="45c50-189">1</span><span class="sxs-lookup"><span data-stu-id="45c50-189">1</span></span>    | <span data-ttu-id="45c50-190">Alpha \_ 1</span><span class="sxs-lookup"><span data-stu-id="45c50-190">Alpha\_1</span></span>                                                       |
| <span data-ttu-id="45c50-191">2</span><span class="sxs-lookup"><span data-stu-id="45c50-191">2</span></span>    | <span data-ttu-id="45c50-192">\[0 \] \[ 2 \] (2 MSBs) ， \[ 0 \] \[ 1 \] ， \[ 0 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="45c50-192">\[0\]\[2\] (2 MSBs), \[0\]\[1\], \[0\]\[0\]</span></span>                    |
| <span data-ttu-id="45c50-193">3</span><span class="sxs-lookup"><span data-stu-id="45c50-193">3</span></span>    | <span data-ttu-id="45c50-194">\[1 \] \[ 1 \] (1 MSB) 、 \[ 1 \] \[ 0 \] 、 \[ 0 \] \[ 3 \] 、 \[ 0 \] \[ 2 \] (1 LSB) </span><span class="sxs-lookup"><span data-stu-id="45c50-194">\[1\]\[1\] (1 MSB), \[1\]\[0\], \[0\]\[3\], \[0\]\[2\] (1 LSB)</span></span> |
| <span data-ttu-id="45c50-195">4</span><span class="sxs-lookup"><span data-stu-id="45c50-195">4</span></span>    | <span data-ttu-id="45c50-196">\[1 \] \[ 3 \] ， \[ 1 \] \[ 2 \] ， \[ 1 \] \[ 1 \] (2 LSBs) </span><span class="sxs-lookup"><span data-stu-id="45c50-196">\[1\]\[3\], \[1\]\[2\], \[1\]\[1\] (2 LSBs)</span></span>                    |
| <span data-ttu-id="45c50-197">5</span><span class="sxs-lookup"><span data-stu-id="45c50-197">5</span></span>    | <span data-ttu-id="45c50-198">\[2 \] \[ 2 \] (2 MSBs) ， \[ 2 \] \[ 1 \] ， \[ 2 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="45c50-198">\[2\]\[2\] (2 MSBs), \[2\]\[1\], \[2\]\[0\]</span></span>                    |
| <span data-ttu-id="45c50-199">6</span><span class="sxs-lookup"><span data-stu-id="45c50-199">6</span></span>    | <span data-ttu-id="45c50-200">\[3 \] \[ 1 \] (1 MSB) 、 \[ 3 \] \[ 0 \] 、 \[ 2 \] \[ 3 \] 、 \[ 2 \] \[ 2 \] (1 LSB) </span><span class="sxs-lookup"><span data-stu-id="45c50-200">\[3\]\[1\] (1 MSB), \[3\]\[0\], \[2\]\[3\], \[2\]\[2\] (1 LSB)</span></span> |
| <span data-ttu-id="45c50-201">7</span><span class="sxs-lookup"><span data-stu-id="45c50-201">7</span></span>    | <span data-ttu-id="45c50-202">\[3 \] \[ 3 \] ， \[ 3 \] \[ 2 \] ， \[ 3 \] \[ 1 \] (2 LSBs) </span><span class="sxs-lookup"><span data-stu-id="45c50-202">\[3\]\[3\], \[3\]\[2\], \[3\]\[1\] (2 LSBs)</span></span>                    |



 

<span data-ttu-id="45c50-203">DXT4 和 DXT5 之間的差異在於，在 DXT4 格式中，假設色彩資料已由 Alpha 預乘。</span><span class="sxs-lookup"><span data-stu-id="45c50-203">The difference between DXT4 and DXT5 is that in the DXT4 format it is assumed that the color data has been premultiplied by alpha.</span></span> <span data-ttu-id="45c50-204">使用 DXT5 格式時，會假設色彩未以 Alpha 預乘。</span><span class="sxs-lookup"><span data-stu-id="45c50-204">In the DXT5 format, it is assumed the color is not premultiplied by alpha.</span></span> <span data-ttu-id="45c50-205">這兩種格式是需要的，因為在大部分情況下，使用材質時，檢查資料是否不足以判斷色彩值是否已乘以 Alpha。</span><span class="sxs-lookup"><span data-stu-id="45c50-205">These two formats are needed because, in most cases, by the time a texture is used, just examining the data is not sufficient to determine if the color values have been multiplied by alpha.</span></span> <span data-ttu-id="45c50-206">因為在執行時間需要這項資訊，所以會使用兩個 FOURCC 碼來區分這些情況。</span><span class="sxs-lookup"><span data-stu-id="45c50-206">Because this information is needed at run time, the two FOURCC codes are used to differentiate these cases.</span></span> <span data-ttu-id="45c50-207">不過，這兩種格式所使用的資料和插補方法相同。</span><span class="sxs-lookup"><span data-stu-id="45c50-207">However, the data and interpolation method used for these two formats is identical.</span></span>

<span data-ttu-id="45c50-208">DXT1 中使用的色彩比較，可判斷材質是否為透明，而不會搭配這些格式使用。</span><span class="sxs-lookup"><span data-stu-id="45c50-208">The color compare used in DXT1 to determine if the texel is transparent is not used with these formats.</span></span> <span data-ttu-id="45c50-209">若不使用色彩比較，色彩資料預設會以 4 色模式進行處理。</span><span class="sxs-lookup"><span data-stu-id="45c50-209">It is assumed that without the color compare the color data is always treated as if in 4-color mode.</span></span> <span data-ttu-id="45c50-210">換句話說，DXT1 程式碼頂端的 if 語句應該是：</span><span class="sxs-lookup"><span data-stu-id="45c50-210">In other words, the if statement at the top of the DXT1 code should be:</span></span>


```
if ((color_0 > color_1) OR !DXT1) {
```



## <a name="related-topics"></a><span data-ttu-id="45c50-211">相關主題</span><span class="sxs-lookup"><span data-stu-id="45c50-211">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45c50-212">壓縮的材質資源</span><span class="sxs-lookup"><span data-stu-id="45c50-212">Compressed Texture Resources</span></span>](compressed-texture-resources.md)
</dt> </dl>

 

 



