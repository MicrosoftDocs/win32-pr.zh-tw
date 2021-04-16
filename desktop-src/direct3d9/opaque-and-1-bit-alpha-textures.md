---
description: 材質格式 DXT1 適用于不透明或具有單一透明色彩的材質。
ms.assetid: a890ed0a-1f68-45b8-93cb-b621d1908d9f
title: " (Direct3D 9) 的不透明和1位 Alpha 紋理"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f629eff594d28d9a807021c0b9df0bd05ea66c3
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/04/2021
ms.locfileid: "104550557"
---
# <a name="opaque-and-1-bit-alpha-textures-direct3d-9"></a><span data-ttu-id="35471-103"> (Direct3D 9) 的不透明和1位 Alpha 紋理</span><span class="sxs-lookup"><span data-stu-id="35471-103">Opaque and 1-Bit Alpha Textures (Direct3D 9)</span></span>

<span data-ttu-id="35471-104">材質格式 DXT1 適用于不透明或具有單一透明色彩的材質。</span><span class="sxs-lookup"><span data-stu-id="35471-104">Texture format DXT1 is for textures that are opaque or have a single transparent color.</span></span>

<span data-ttu-id="35471-105">針對每個不透明或 1 位元 alpha 區塊，儲存兩個 16 位元值 (RGB 5:6:5 格式)，以及每像素 2 位元的 4x4 點陣圖。</span><span class="sxs-lookup"><span data-stu-id="35471-105">For each opaque or 1-bit alpha block, two 16-bit values (RGB 5:6:5 format) and a 4x4 bitmap with 2 bits per pixel are stored.</span></span> <span data-ttu-id="35471-106">這總計 16 紋素 64 位元，或每紋素四個位元。</span><span class="sxs-lookup"><span data-stu-id="35471-106">This totals 64 bits for 16 texels, or four bits per texel.</span></span> <span data-ttu-id="35471-107">在區塊點陣圖中，每紋素有 2 位元可在四個色彩之間選取，其中兩個會儲存在編碼資料中。</span><span class="sxs-lookup"><span data-stu-id="35471-107">In the block bitmap, there are 2 bits per texel to select between the four colors, two of which are stored in the encoded data.</span></span> <span data-ttu-id="35471-108">線性插補會將另外兩種色彩從這些儲存的色彩中衍生。</span><span class="sxs-lookup"><span data-stu-id="35471-108">The other two colors are derived from these stored colors by linear interpolation.</span></span> <span data-ttu-id="35471-109">此配置顯示在下圖。</span><span class="sxs-lookup"><span data-stu-id="35471-109">This layout is shown in the following diagram.</span></span>

![點陣圖配置的圖表](images/colors1.png)

<span data-ttu-id="35471-111">透過比較儲存在區塊中的兩個 16 位元色彩值可區別 1 位元的 alpha 格式和不透明格式。</span><span class="sxs-lookup"><span data-stu-id="35471-111">The 1-bit alpha format is distinguished from the opaque format by comparing the two 16-bit color values stored in the block.</span></span> <span data-ttu-id="35471-112">它們會被視為不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="35471-112">They are treated as unsigned integers.</span></span> <span data-ttu-id="35471-113">如果第一個色彩大於第二個，就表示只定義不透明的紋素。</span><span class="sxs-lookup"><span data-stu-id="35471-113">If the first color is greater than the second, it implies that only opaque texels are defined.</span></span> <span data-ttu-id="35471-114">這表示使用四個色彩代表紋素。</span><span class="sxs-lookup"><span data-stu-id="35471-114">This means four colors are used to represent the texels.</span></span> <span data-ttu-id="35471-115">在四色編碼中，有兩種衍生的色彩，所有四個色彩平均散佈在 RGB 色彩空間。</span><span class="sxs-lookup"><span data-stu-id="35471-115">In four-color encoding, there are two derived colors and all four colors are equally distributed in RGB color space.</span></span> <span data-ttu-id="35471-116">這個格式類似 RGB 5:6:5 格式。</span><span class="sxs-lookup"><span data-stu-id="35471-116">This format is analogous to RGB 5:6:5 format.</span></span> <span data-ttu-id="35471-117">否則，對於 1 位元透明度，使用三個色彩，保留第四個來代表透明紋素。</span><span class="sxs-lookup"><span data-stu-id="35471-117">Otherwise, for 1-bit alpha transparency, three colors are used and the fourth is reserved to represent transparent texels.</span></span>

<span data-ttu-id="35471-118">在三色編碼中，有一個衍生的色彩，並保留第四個 2 位元程式碼指出透明紋素 (alpha 資訊)。</span><span class="sxs-lookup"><span data-stu-id="35471-118">In three-color encoding, there is one derived color and the fourth 2-bit code is reserved to indicate a transparent texel (alpha information).</span></span> <span data-ttu-id="35471-119">這個格式類似 RGBA 5:5:5:1，其中最後一位元用於編碼 alpha 遮罩。</span><span class="sxs-lookup"><span data-stu-id="35471-119">This format is analogous to RGBA 5:5:5:1, where the final bit is used for encoding the alpha mask.</span></span>

<span data-ttu-id="35471-120">下列程式碼示範的演算法用於決定是否選取三或四個色彩編碼︰</span><span class="sxs-lookup"><span data-stu-id="35471-120">The following code example illustrates the algorithm for deciding whether three- or four-color encoding is selected:</span></span>


```
if (color_0 > color_1) 
{
    // Four-color block: derive the other two colors.    
    // 00 = color_0, 01 = color_1, 10 = color_2, 11 = color_3
    // These 2-bit codes correspond to the 2-bit fields 
    // stored in the 64-bit block.
    color_2 = (2 * color_0 + color_1 + 1) / 3;
    color_3 = (color_0 + 2 * color_1 + 1) / 3;
}    
else
{ 
    // Three-color block: derive the other color.
    // 00 = color_0,  01 = color_1,  10 = color_2,  
    // 11 = transparent.
    // These 2-bit codes correspond to the 2-bit fields 
    // stored in the 64-bit block. 
    color_2 = (color_0 + color_1) / 2;    
    color_3 = transparent;    

}
```



<span data-ttu-id="35471-121">建議您在混合之前將透明度像素的 RGBA 元件設為零。</span><span class="sxs-lookup"><span data-stu-id="35471-121">It is recommended that you set the RGBA components of the transparency pixel to zero before blending.</span></span>

<span data-ttu-id="35471-122">下表顯示 8 位元組區塊的記憶體配置。</span><span class="sxs-lookup"><span data-stu-id="35471-122">The following tables show the memory layout for the 8-byte block.</span></span> <span data-ttu-id="35471-123">它假設第一個索引對應 y 座標，第二個對應 x 座標。</span><span class="sxs-lookup"><span data-stu-id="35471-123">It is assumed that the first index corresponds to the y-coordinate and the second corresponds to the x-coordinate.</span></span> <span data-ttu-id="35471-124">例如，材質 \[ 1 \] \[ 2 \] 指的是 (x，y) = (2，1) 的材質地圖圖元。</span><span class="sxs-lookup"><span data-stu-id="35471-124">For example, Texel\[1\]\[2\] refers to the texture map pixel at (x,y) = (2,1).</span></span>

<span data-ttu-id="35471-125">此資料表包含8位元組 (64 位) 區塊的記憶體配置。</span><span class="sxs-lookup"><span data-stu-id="35471-125">This table contains the memory layout for the 8-byte (64-bit) block.</span></span>



| <span data-ttu-id="35471-126">單字位址</span><span class="sxs-lookup"><span data-stu-id="35471-126">Word address</span></span> | <span data-ttu-id="35471-127">16 位元單字</span><span class="sxs-lookup"><span data-stu-id="35471-127">16-bit word</span></span>    |
|--------------|----------------|
| <span data-ttu-id="35471-128">0</span><span class="sxs-lookup"><span data-stu-id="35471-128">0</span></span>            | <span data-ttu-id="35471-129">色彩 \_ 0</span><span class="sxs-lookup"><span data-stu-id="35471-129">Color\_0</span></span>       |
| <span data-ttu-id="35471-130">1</span><span class="sxs-lookup"><span data-stu-id="35471-130">1</span></span>            | <span data-ttu-id="35471-131">色彩 \_ 1</span><span class="sxs-lookup"><span data-stu-id="35471-131">Color\_1</span></span>       |
| <span data-ttu-id="35471-132">2</span><span class="sxs-lookup"><span data-stu-id="35471-132">2</span></span>            | <span data-ttu-id="35471-133">點陣圖字 \_ 0</span><span class="sxs-lookup"><span data-stu-id="35471-133">Bitmap Word\_0</span></span> |
| <span data-ttu-id="35471-134">3</span><span class="sxs-lookup"><span data-stu-id="35471-134">3</span></span>            | <span data-ttu-id="35471-135">點陣圖文字 \_ 1</span><span class="sxs-lookup"><span data-stu-id="35471-135">Bitmap Word\_1</span></span> |



 

<span data-ttu-id="35471-136">色彩 \_ 0 和色彩 \_ 1 （兩個極端的色彩）如下所示：</span><span class="sxs-lookup"><span data-stu-id="35471-136">Color\_0 and Color\_1, the colors at the two extremes, are laid out as follows:</span></span>



| <span data-ttu-id="35471-137">Bits</span><span class="sxs-lookup"><span data-stu-id="35471-137">Bits</span></span>        | <span data-ttu-id="35471-138">Color</span><span class="sxs-lookup"><span data-stu-id="35471-138">Color</span></span>                 |
|-------------|-----------------------|
| <span data-ttu-id="35471-139">4:0 (LSB \*) </span><span class="sxs-lookup"><span data-stu-id="35471-139">4:0 (LSB\*)</span></span> | <span data-ttu-id="35471-140">藍色元件</span><span class="sxs-lookup"><span data-stu-id="35471-140">Blue color component</span></span>  |
| <span data-ttu-id="35471-141">10:5</span><span class="sxs-lookup"><span data-stu-id="35471-141">10:5</span></span>        | <span data-ttu-id="35471-142">綠色元件</span><span class="sxs-lookup"><span data-stu-id="35471-142">Green color component</span></span> |
| <span data-ttu-id="35471-143">15:11</span><span class="sxs-lookup"><span data-stu-id="35471-143">15:11</span></span>       | <span data-ttu-id="35471-144">紅色元件</span><span class="sxs-lookup"><span data-stu-id="35471-144">Red color component</span></span>   |



 

<span data-ttu-id="35471-145">\*最不重要的位</span><span class="sxs-lookup"><span data-stu-id="35471-145">\*least-significant bit</span></span>

<span data-ttu-id="35471-146">點陣圖字 \_ 0 的配置如下：</span><span class="sxs-lookup"><span data-stu-id="35471-146">Bitmap Word\_0 is laid out as follows:</span></span>



| <span data-ttu-id="35471-147">Bits</span><span class="sxs-lookup"><span data-stu-id="35471-147">Bits</span></span>          | <span data-ttu-id="35471-148">紋素</span><span class="sxs-lookup"><span data-stu-id="35471-148">Texel</span></span>           |
|---------------|-----------------|
| <span data-ttu-id="35471-149">1:0 (LSB)</span><span class="sxs-lookup"><span data-stu-id="35471-149">1:0 (LSB)</span></span>     | <span data-ttu-id="35471-150">材質 \[ 0 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="35471-150">Texel\[0\]\[0\]</span></span> |
| <span data-ttu-id="35471-151">3:2</span><span class="sxs-lookup"><span data-stu-id="35471-151">3:2</span></span>           | <span data-ttu-id="35471-152">材質 \[ 0 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="35471-152">Texel\[0\]\[1\]</span></span> |
| <span data-ttu-id="35471-153">5:4</span><span class="sxs-lookup"><span data-stu-id="35471-153">5:4</span></span>           | <span data-ttu-id="35471-154">材質 \[ 0 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="35471-154">Texel\[0\]\[2\]</span></span> |
| <span data-ttu-id="35471-155">7:6</span><span class="sxs-lookup"><span data-stu-id="35471-155">7:6</span></span>           | <span data-ttu-id="35471-156">材質 \[ 0 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="35471-156">Texel\[0\]\[3\]</span></span> |
| <span data-ttu-id="35471-157">9:8</span><span class="sxs-lookup"><span data-stu-id="35471-157">9:8</span></span>           | <span data-ttu-id="35471-158">材質 \[ 1 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="35471-158">Texel\[1\]\[0\]</span></span> |
| <span data-ttu-id="35471-159">11:10</span><span class="sxs-lookup"><span data-stu-id="35471-159">11:10</span></span>         | <span data-ttu-id="35471-160">材質 \[ 1 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="35471-160">Texel\[1\]\[1\]</span></span> |
| <span data-ttu-id="35471-161">13:12</span><span class="sxs-lookup"><span data-stu-id="35471-161">13:12</span></span>         | <span data-ttu-id="35471-162">材質 \[ 1 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="35471-162">Texel\[1\]\[2\]</span></span> |
| <span data-ttu-id="35471-163">15:14 (MSB \*) </span><span class="sxs-lookup"><span data-stu-id="35471-163">15:14 (MSB\*)</span></span> | <span data-ttu-id="35471-164">材質 \[ 1 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="35471-164">Texel\[1\]\[3\]</span></span> |



 

<span data-ttu-id="35471-165">\*最重要的一點 (MSB) </span><span class="sxs-lookup"><span data-stu-id="35471-165">\*most significant bit (MSB)</span></span>

<span data-ttu-id="35471-166">點陣圖 Word \_ 1 的配置如下：</span><span class="sxs-lookup"><span data-stu-id="35471-166">Bitmap Word\_1 is laid out as follows:</span></span>



| <span data-ttu-id="35471-167">Bits</span><span class="sxs-lookup"><span data-stu-id="35471-167">Bits</span></span>        | <span data-ttu-id="35471-168">紋素</span><span class="sxs-lookup"><span data-stu-id="35471-168">Texel</span></span>           |
|-------------|-----------------|
| <span data-ttu-id="35471-169">1:0 (LSB)</span><span class="sxs-lookup"><span data-stu-id="35471-169">1:0 (LSB)</span></span>   | <span data-ttu-id="35471-170">材質 \[ 2 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="35471-170">Texel\[2\]\[0\]</span></span> |
| <span data-ttu-id="35471-171">3:2</span><span class="sxs-lookup"><span data-stu-id="35471-171">3:2</span></span>         | <span data-ttu-id="35471-172">材質 \[ 2 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="35471-172">Texel\[2\]\[1\]</span></span> |
| <span data-ttu-id="35471-173">5:4</span><span class="sxs-lookup"><span data-stu-id="35471-173">5:4</span></span>         | <span data-ttu-id="35471-174">材質 \[ 2 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="35471-174">Texel\[2\]\[2\]</span></span> |
| <span data-ttu-id="35471-175">7:6</span><span class="sxs-lookup"><span data-stu-id="35471-175">7:6</span></span>         | <span data-ttu-id="35471-176">材質 \[ 2 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="35471-176">Texel\[2\]\[3\]</span></span> |
| <span data-ttu-id="35471-177">9:8</span><span class="sxs-lookup"><span data-stu-id="35471-177">9:8</span></span>         | <span data-ttu-id="35471-178">材質 \[ 3 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="35471-178">Texel\[3\]\[0\]</span></span> |
| <span data-ttu-id="35471-179">11:10</span><span class="sxs-lookup"><span data-stu-id="35471-179">11:10</span></span>       | <span data-ttu-id="35471-180">材質 \[ 3 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="35471-180">Texel\[3\]\[1\]</span></span> |
| <span data-ttu-id="35471-181">13:12</span><span class="sxs-lookup"><span data-stu-id="35471-181">13:12</span></span>       | <span data-ttu-id="35471-182">材質 \[ 3 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="35471-182">Texel\[3\]\[2\]</span></span> |
| <span data-ttu-id="35471-183">15:14 (MSB)</span><span class="sxs-lookup"><span data-stu-id="35471-183">15:14 (MSB)</span></span> | <span data-ttu-id="35471-184">材質 \[ 3 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="35471-184">Texel\[3\]\[3\]</span></span> |



 

## <a name="example-of-opaque-color-encoding"></a><span data-ttu-id="35471-185">不透明色彩編碼的範例</span><span class="sxs-lookup"><span data-stu-id="35471-185">Example of Opaque Color Encoding</span></span>

<span data-ttu-id="35471-186">以不透明編碼為例，假設色彩紅色和黑色位於極端。</span><span class="sxs-lookup"><span data-stu-id="35471-186">As an example of opaque encoding, assume that the colors red and black are at the extremes.</span></span> <span data-ttu-id="35471-187">紅色為色彩 \_ 0，黑色為色彩 \_ 1。</span><span class="sxs-lookup"><span data-stu-id="35471-187">Red is color\_0, and black is color\_1.</span></span> <span data-ttu-id="35471-188">有四個以內插值取代的色彩之之間平均漸層分散。</span><span class="sxs-lookup"><span data-stu-id="35471-188">There are four interpolated colors that form the uniformly distributed gradient between them.</span></span> <span data-ttu-id="35471-189">若要判斷 4x4 點陣圖值，請使用下列的計算︰</span><span class="sxs-lookup"><span data-stu-id="35471-189">To determine the values for the 4x4 bitmap, the following calculations are used:</span></span>


```
00 ? color_0
01 ? color_1
10 ? 2/3 color_0 + 1/3 color_1
11 ? 1/3 color_0 + 2/3 color_1
```



<span data-ttu-id="35471-190">然後點陣圖看起來如下列圖表。</span><span class="sxs-lookup"><span data-stu-id="35471-190">The bitmap then looks like the following diagram.</span></span>

![顯示展開點陣圖版面配置的圖表。](images/colors2.png)

<span data-ttu-id="35471-192">這看起來像下列圖解系列色彩。</span><span class="sxs-lookup"><span data-stu-id="35471-192">This looks like the following illustrated series of colors.</span></span>

> [!Note]  
> <span data-ttu-id="35471-193">在影像中，圖元 (0，0) 出現在左上方。</span><span class="sxs-lookup"><span data-stu-id="35471-193">In an image, pixel (0,0) appears on the top left.</span></span>

 

![不透明編碼漸層圖例](images/redsquares.png)

## <a name="example-of-1-bit-alpha-encoding"></a><span data-ttu-id="35471-195">1位 Alpha 編碼範例</span><span class="sxs-lookup"><span data-stu-id="35471-195">Example of 1-Bit Alpha Encoding</span></span>

<span data-ttu-id="35471-196">當不帶正負號的16位整數（色彩0） \_ 小於不帶正負號的16位整數（色彩1）時，就會選取此格式 \_ 。</span><span class="sxs-lookup"><span data-stu-id="35471-196">This format is selected when the unsigned 16-bit integer, color\_0, is less than the unsigned 16-bit integer, color\_1.</span></span> <span data-ttu-id="35471-197">可以使用此格式的範例是樹上樹葉，與藍天對映。</span><span class="sxs-lookup"><span data-stu-id="35471-197">An example of where this format can be used is leaves on a tree, shown against a blue sky.</span></span> <span data-ttu-id="35471-198">有些紋素可標示成透明，同時有三種綠色系列仍可供樹葉運用。</span><span class="sxs-lookup"><span data-stu-id="35471-198">Some texels can be marked as transparent while three shades of green are still available for the leaves.</span></span> <span data-ttu-id="35471-199">兩個色彩修正極端，而且第三個插補色彩。</span><span class="sxs-lookup"><span data-stu-id="35471-199">Two colors fix the extremes, and the third is an interpolated color.</span></span>

<span data-ttu-id="35471-200">以下是這類圖片的範例圖。</span><span class="sxs-lookup"><span data-stu-id="35471-200">The following illustration is an example of such a picture.</span></span>

![1 位元 alpha 編碼的圖例](images/greenthing.png)

<span data-ttu-id="35471-202">請注意，影像會顯示為白色，而材質會編碼為透明。</span><span class="sxs-lookup"><span data-stu-id="35471-202">Note that where the image is shown as white, the texel would be encoded as transparent.</span></span> <span data-ttu-id="35471-203">另請注意，在混合之前，透明材質的 RGBA 元件應該設定為零。</span><span class="sxs-lookup"><span data-stu-id="35471-203">Also note that the RGBA components of the transparent texels should be set to zero before blending.</span></span>

<span data-ttu-id="35471-204">適用於色彩和透明度的點陣圖編碼，會使用下列的計算來判定。</span><span class="sxs-lookup"><span data-stu-id="35471-204">The bitmap encoding for the colors and the transparency is determined using the following calculations.</span></span>


```
00 ? color_0
01 ? color_1
10 ? 1/2 color_0 + 1/2 color_1
11   ?   Transparent
```



<span data-ttu-id="35471-205">然後點陣圖看起來如下列圖表。</span><span class="sxs-lookup"><span data-stu-id="35471-205">The bitmap then looks like the following diagram.</span></span>

![展開的點陣圖配置的圖表](images/colors3.png)

## <a name="related-topics"></a><span data-ttu-id="35471-207">相關主題</span><span class="sxs-lookup"><span data-stu-id="35471-207">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35471-208">壓縮的材質資源</span><span class="sxs-lookup"><span data-stu-id="35471-208">Compressed Texture Resources</span></span>](compressed-texture-resources.md)
</dt> </dl>

 

 



