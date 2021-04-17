---
title: Turbulence 效果
description: 您可以使用 turbulence 效果，根據 Perlin 雜訊函式來產生點陣圖。
ms.assetid: 86C1990E-958C-46D7-840A-E4A17F1D1740
keywords:
- turbulence 效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f67f615ec5b68ca285a048b68bc7bc8eab6e24
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/04/2021
ms.locfileid: "104551134"
---
# <a name="turbulence-effect"></a><span data-ttu-id="9bec6-104">Turbulence 效果</span><span class="sxs-lookup"><span data-stu-id="9bec6-104">Turbulence effect</span></span>

<span data-ttu-id="9bec6-105">您可以使用 turbulence 效果，根據 Perlin 雜訊函式來產生點陣圖。</span><span class="sxs-lookup"><span data-stu-id="9bec6-105">Use the turbulence effect to generate a bitmap based on the Perlin noise function.</span></span>

<span data-ttu-id="9bec6-106">Turbulence 效果沒有輸入影像。</span><span class="sxs-lookup"><span data-stu-id="9bec6-106">The turbulence effect has no input image.</span></span>

<span data-ttu-id="9bec6-107">這項效果的 CLSID 是 CLSID \_ D2D1Turbulence。</span><span class="sxs-lookup"><span data-stu-id="9bec6-107">The CLSID for this effect is CLSID\_D2D1Turbulence.</span></span>

-   [<span data-ttu-id="9bec6-108">範例影像</span><span class="sxs-lookup"><span data-stu-id="9bec6-108">Example image</span></span>](#example-image)
-   [<span data-ttu-id="9bec6-109">效果屬性</span><span class="sxs-lookup"><span data-stu-id="9bec6-109">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="9bec6-110">雜訊模式</span><span class="sxs-lookup"><span data-stu-id="9bec6-110">Noise modes</span></span>](#noise-modes)
-   [<span data-ttu-id="9bec6-111">輸出點陣圖</span><span class="sxs-lookup"><span data-stu-id="9bec6-111">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="9bec6-112">需求</span><span class="sxs-lookup"><span data-stu-id="9bec6-112">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="9bec6-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="9bec6-113">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="9bec6-114">範例影像</span><span class="sxs-lookup"><span data-stu-id="9bec6-114">Example image</span></span>

![顯示 turbulence 效果輸出的效果範例螢幕擷取畫面。](images/32-turbulence.png)

<span data-ttu-id="9bec6-116">Turbulence 效果會計算一或多個 Perlin 雜訊函數 octaves 的總和。</span><span class="sxs-lookup"><span data-stu-id="9bec6-116">The Turbulence effect computes the sum of one or more octaves of the Perlin noise function.</span></span> <span data-ttu-id="9bec6-117">Perlin 雜訊是虛擬隨機函數，其值取決於頻率、位置和種子值。</span><span class="sxs-lookup"><span data-stu-id="9bec6-117">Perlin noise is a pseudo-random function whose value depends on the frequency, position, and seed value.</span></span> <span data-ttu-id="9bec6-118">效果會使用其中一個方程式來產生 RGBA 值。</span><span class="sxs-lookup"><span data-stu-id="9bec6-118">The effect generates the RGBA values using one of these equations.</span></span>

<span data-ttu-id="9bec6-119">如果您選取 D2D1 \_ TURBULENCE \_ 雜訊碎形 \_ 加 \_ 總雜訊模式，效果會使用這個方程式。</span><span class="sxs-lookup"><span data-stu-id="9bec6-119">If you select the D2D1\_TURBULENCE\_NOISE\_FRACTAL\_SUM noise mode the effect uses this equation.</span></span>

![顯示用來產生點陣圖之 turbulence 函數的螢幕擷取畫面。](images/turbulence-equation1.png)

<span data-ttu-id="9bec6-121">如果您選取 D2D1 \_ TURBULENCE \_ 雜訊 \_ TURBULENCE 雜訊模式，效果就會使用此方程式。</span><span class="sxs-lookup"><span data-stu-id="9bec6-121">If you select the D2D1\_TURBULENCE\_NOISE\_TURBULENCE noise mode the effect uses this equation.</span></span>

![用來產生點陣圖的 turbulence 函數。](images/turbulence-equation2.png)

> [!Note]  
> <span data-ttu-id="9bec6-123">`PerlinNoise`函數的範圍為 \[ -1、1 \] 。</span><span class="sxs-lookup"><span data-stu-id="9bec6-123">The `PerlinNoise` function has a range of \[-1, 1\].</span></span>

 

<span data-ttu-id="9bec6-124">此效果會輸出預乘 Alpha 的圖元值。</span><span class="sxs-lookup"><span data-stu-id="9bec6-124">This effect outputs pixel values in premultiplied alpha.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="9bec6-125">效果屬性</span><span class="sxs-lookup"><span data-stu-id="9bec6-125">Effect properties</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9bec6-126">顯示名稱和索引列舉</span><span class="sxs-lookup"><span data-stu-id="9bec6-126">Display name and index enumeration</span></span></th>
<th><span data-ttu-id="9bec6-127">Description</span><span class="sxs-lookup"><span data-stu-id="9bec6-127">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9bec6-128">Offset</span><span class="sxs-lookup"><span data-stu-id="9bec6-128">Offset</span></span><br/> <span data-ttu-id="9bec6-129">D2D1_TURBULENCE_PROP_OFFSET</span><span class="sxs-lookup"><span data-stu-id="9bec6-129">D2D1_TURBULENCE_PROP_OFFSET</span></span><br/></td>
<td><span data-ttu-id="9bec6-130">產生 turbulence 輸出的座標。</span><span class="sxs-lookup"><span data-stu-id="9bec6-130">The coordinates where the turbulence output is generated.</span></span><br/> <span data-ttu-id="9bec6-131">用來產生 Perlin 雜訊的演算法與位置相依，因此不同的位移會導致不同的輸出。</span><span class="sxs-lookup"><span data-stu-id="9bec6-131">The algorithm used to generate the Perlin noise is position dependent, so a different offset results in a different output.</span></span> <span data-ttu-id="9bec6-132">這個屬性未系結，而且單位是在 Dip 中指定</span><span class="sxs-lookup"><span data-stu-id="9bec6-132">This property is not bounded and the units are specified in DIPs</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="9bec6-133">位移與轉譯沒有相同的效果，因為雜訊函式輸出是無限的，且函式會在磚周圍換行。</span><span class="sxs-lookup"><span data-stu-id="9bec6-133">The offset does not have the same effect as a translation because the noise function output is infinite and the function will wrap around the tile.</span></span>
</blockquote>
<br/> <span data-ttu-id="9bec6-134">此類型為 D2D1_VECTOR_2F。</span><span class="sxs-lookup"><span data-stu-id="9bec6-134">The type is D2D1_VECTOR_2F.</span></span><br/> <span data-ttu-id="9bec6-135">預設值為 {0.0 f，0.0 f}。</span><span class="sxs-lookup"><span data-stu-id="9bec6-135">The default value is {0.0f, 0.0f}.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9bec6-136">大小</span><span class="sxs-lookup"><span data-stu-id="9bec6-136">Size</span></span><br/> <span data-ttu-id="9bec6-137">D2D1_TURBULENCE_PROP_SIZE</span><span class="sxs-lookup"><span data-stu-id="9bec6-137">D2D1_TURBULENCE_PROP_SIZE</span></span><br/></td>
<td><span data-ttu-id="9bec6-138">Turbulence 輸出的大小。</span><span class="sxs-lookup"><span data-stu-id="9bec6-138">The size of the turbulence output.</span></span><br/> <span data-ttu-id="9bec6-139">這個屬性未系結，而且單位是在 Dip 中指定</span><span class="sxs-lookup"><span data-stu-id="9bec6-139">This property is not bounded and the units are specified in DIPs</span></span> <br/>
<br/> <span data-ttu-id="9bec6-140">此類型為 D2D1_VECTOR_2F。</span><span class="sxs-lookup"><span data-stu-id="9bec6-140">The type is D2D1_VECTOR_2F.</span></span><br/> <span data-ttu-id="9bec6-141">預設值為 {0.0 f，0.0 f}。</span><span class="sxs-lookup"><span data-stu-id="9bec6-141">The default value is {0.0f, 0.0f}.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9bec6-142">BaseFrequency</span><span class="sxs-lookup"><span data-stu-id="9bec6-142">BaseFrequency</span></span><br/> <span data-ttu-id="9bec6-143">D2D1_TURBULENCE_PROP_BASE_FREQUENCY</span><span class="sxs-lookup"><span data-stu-id="9bec6-143">D2D1_TURBULENCE_PROP_BASE_FREQUENCY</span></span><br/></td>
<td><span data-ttu-id="9bec6-144">X 和 Y 方向的基底頻率。</span><span class="sxs-lookup"><span data-stu-id="9bec6-144">The base frequencies in the X and Y direction.</span></span> <span data-ttu-id="9bec6-145">這個屬性是浮點數，而且必須大於0。</span><span class="sxs-lookup"><span data-stu-id="9bec6-145">This property is a float and must be greater than 0.</span></span> <span data-ttu-id="9bec6-146">單位會以 1/下降來指定。</span><span class="sxs-lookup"><span data-stu-id="9bec6-146">The units are specified in 1/DIPs.</span></span> <br/> <span data-ttu-id="9bec6-147">針對基底頻率，1 (1/Dip) 的值會導致 Perlin 雜訊完成兩個圖元之間的整個迴圈。</span><span class="sxs-lookup"><span data-stu-id="9bec6-147">A value of 1 (1/DIPs) for the base frequency results in the Perlin noise completing an entire cycle between two pixels.</span></span> <span data-ttu-id="9bec6-148">這些圖元的簡化插補會產生完全隨機的圖元，因為圖元之間沒有相互關聯。</span><span class="sxs-lookup"><span data-stu-id="9bec6-148">The ease interpolation for these pixels results in completely random pixels, since there is no correlation between the pixels.</span></span><br/> <span data-ttu-id="9bec6-149">針對基底頻率，值為 0.1 (1/Dip) ，Perlin 雜訊函式每10次都會重複一次。</span><span class="sxs-lookup"><span data-stu-id="9bec6-149">A value of 0.1(1/DIPs) for the base frequency, the Perlin noise function repeats every 10 DIPs.</span></span> <span data-ttu-id="9bec6-150">這會導致圖元之間的相互關聯，而且可以看見一般的 turbulence 效果。</span><span class="sxs-lookup"><span data-stu-id="9bec6-150">This results in correlation between pixels and the typical turbulence effect is visible.</span></span><br/> <span data-ttu-id="9bec6-151">此類型為 D2D1_VECTOR_2F。</span><span class="sxs-lookup"><span data-stu-id="9bec6-151">The type is D2D1_VECTOR_2F.</span></span><br/> <span data-ttu-id="9bec6-152">預設值為 {0.01 f，0.01 f}。</span><span class="sxs-lookup"><span data-stu-id="9bec6-152">The default value is {0.01f, 0.01f}.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9bec6-153">NumOctaves</span><span class="sxs-lookup"><span data-stu-id="9bec6-153">NumOctaves</span></span><br/> <span data-ttu-id="9bec6-154">D2D1_TURBULENCE_PROP_NUM_OCTAVES</span><span class="sxs-lookup"><span data-stu-id="9bec6-154">D2D1_TURBULENCE_PROP_NUM_OCTAVES</span></span><br/></td>
<td><span data-ttu-id="9bec6-155">雜訊函數的 octaves 數目。</span><span class="sxs-lookup"><span data-stu-id="9bec6-155">The number of octaves for the noise function.</span></span> <span data-ttu-id="9bec6-156">這個屬性是 UINT32，而且必須大於0。</span><span class="sxs-lookup"><span data-stu-id="9bec6-156">This property is a UINT32 and must be greater than 0.</span></span><br/> <span data-ttu-id="9bec6-157">此類型為 UINT32。</span><span class="sxs-lookup"><span data-stu-id="9bec6-157">The type is UINT32.</span></span><br/> <span data-ttu-id="9bec6-158">預設值為 1。</span><span class="sxs-lookup"><span data-stu-id="9bec6-158">The default value is 1.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9bec6-159">Seed</span><span class="sxs-lookup"><span data-stu-id="9bec6-159">Seed</span></span><br/> <span data-ttu-id="9bec6-160">D2D1_TURBULENCE_PROP_SEED</span><span class="sxs-lookup"><span data-stu-id="9bec6-160">D2D1_TURBULENCE_PROP_SEED</span></span><br/></td>
<td><span data-ttu-id="9bec6-161">虛擬隨機產生器的種子。</span><span class="sxs-lookup"><span data-stu-id="9bec6-161">The seed for the pseudo random generator.</span></span> <span data-ttu-id="9bec6-162">這個屬性未系結。</span><span class="sxs-lookup"><span data-stu-id="9bec6-162">This property is unbounded.</span></span><br/> <span data-ttu-id="9bec6-163">此類型為 UINT32。</span><span class="sxs-lookup"><span data-stu-id="9bec6-163">The type is UINT32.</span></span><br/> <span data-ttu-id="9bec6-164">預設值為 0。</span><span class="sxs-lookup"><span data-stu-id="9bec6-164">The default value is 0.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9bec6-165">雜訊</span><span class="sxs-lookup"><span data-stu-id="9bec6-165">Noise</span></span><br/> <span data-ttu-id="9bec6-166">D2D1_TURBULENCE_PROP_NOISE</span><span class="sxs-lookup"><span data-stu-id="9bec6-166">D2D1_TURBULENCE_PROP_NOISE</span></span><br/></td>
<td><span data-ttu-id="9bec6-167">Turbulence 雜訊模式。</span><span class="sxs-lookup"><span data-stu-id="9bec6-167">The turbulence noise mode.</span></span> <span data-ttu-id="9bec6-168">這個屬性可以是 <em>碎形 sum</em> 或 <em>turbulence</em>。</span><span class="sxs-lookup"><span data-stu-id="9bec6-168">This property can be either <em>fractal sum</em> or <em>turbulence</em>.</span></span> <span data-ttu-id="9bec6-169">指出是否要根據碎形雜訊或 Turbulence 函數來產生點陣圖。</span><span class="sxs-lookup"><span data-stu-id="9bec6-169">Indicates whether to generate a bitmap based on Fractal Noise or the Turbulence function.</span></span> <span data-ttu-id="9bec6-170">如需詳細資訊，請參閱 <a href="#noise-modes">雜訊模式</a> 。</span><span class="sxs-lookup"><span data-stu-id="9bec6-170">See <a href="#noise-modes">Noise modes</a> for more info.</span></span> <br/> <span data-ttu-id="9bec6-171">此類型為 D2D1_TURBULENCE_NOISE。</span><span class="sxs-lookup"><span data-stu-id="9bec6-171">The type is D2D1_TURBULENCE_NOISE.</span></span><br/> <span data-ttu-id="9bec6-172">預設值為 D2D1_TURBULENCE_NOISE_FRACTAL_SUM。</span><span class="sxs-lookup"><span data-stu-id="9bec6-172">The default value is D2D1_TURBULENCE_NOISE_FRACTAL_SUM.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9bec6-173">Stitchable</span><span class="sxs-lookup"><span data-stu-id="9bec6-173">Stitchable</span></span><br/> <span data-ttu-id="9bec6-174">D2D1_TURBULENCE_PROP_STITCHABLE</span><span class="sxs-lookup"><span data-stu-id="9bec6-174">D2D1_TURBULENCE_PROP_STITCHABLE</span></span><br/></td>
<td><span data-ttu-id="9bec6-175">開啟或關閉裝訂。</span><span class="sxs-lookup"><span data-stu-id="9bec6-175">Turns stitching on or off.</span></span> <span data-ttu-id="9bec6-176">基礎頻率會經過調整，以便拼接輸出點陣圖。</span><span class="sxs-lookup"><span data-stu-id="9bec6-176">The base frequency is adjusted so that output bitmap can be stitched.</span></span> <span data-ttu-id="9bec6-177">如果您想要並排顯示 turbulence 效果輸出的多個複本，這會很有用。</span><span class="sxs-lookup"><span data-stu-id="9bec6-177">This is useful if you want to tile multiple copies of the turbulence effect output.</span></span>
<ul>
<li><span data-ttu-id="9bec6-178">您可以使用圖格效果) 來將輸出點陣圖 (並排顯示，而不會顯示接縫的外觀。</span><span class="sxs-lookup"><span data-stu-id="9bec6-178">True   The output bitmap can be tiled (using the tile effect) without the appearance of seams.</span></span> <span data-ttu-id="9bec6-179">基礎頻率會經過調整，以便拼接輸出點陣圖。</span><span class="sxs-lookup"><span data-stu-id="9bec6-179">The base frequency is adjusted so that output bitmap can be stitched.</span></span></li>
<li><span data-ttu-id="9bec6-180">False：基底頻率未調整，所以如果點陣圖已並排顯示，則圖格之間可能會出現接縫。</span><span class="sxs-lookup"><span data-stu-id="9bec6-180">False   The base frequency is not adjusted, so seams may appear between tiles if the bitmap is tiled.</span></span></li>
</ul>
<br/> <span data-ttu-id="9bec6-181">此類型為 BOOL。</span><span class="sxs-lookup"><span data-stu-id="9bec6-181">The type is BOOL.</span></span><br/> <span data-ttu-id="9bec6-182">預設值為 FALSE。</span><span class="sxs-lookup"><span data-stu-id="9bec6-182">The default value is FALSE.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="noise-modes"></a><span data-ttu-id="9bec6-183">雜訊模式</span><span class="sxs-lookup"><span data-stu-id="9bec6-183">Noise modes</span></span>



| <span data-ttu-id="9bec6-184">列舉型別</span><span class="sxs-lookup"><span data-stu-id="9bec6-184">Enumeration</span></span>                           | <span data-ttu-id="9bec6-185">描述</span><span class="sxs-lookup"><span data-stu-id="9bec6-185">Description</span></span>                                                                           |
|---------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9bec6-186">D2D1 \_ TURBULENCE \_ 雜訊 \_ 碎形 \_ 總和</span><span class="sxs-lookup"><span data-stu-id="9bec6-186">D2D1\_TURBULENCE\_NOISE\_FRACTAL\_SUM</span></span> | <span data-ttu-id="9bec6-187">計算 octaves 的總和，將輸出範圍從 \[ -1，1 \] ，移至 \[ 0，1 \] 。</span><span class="sxs-lookup"><span data-stu-id="9bec6-187">Computes a sum of the octaves, shifting the output range from \[-1, 1\], to \[0, 1\].</span></span> |
| <span data-ttu-id="9bec6-188">D2D1 \_ TURBULENCE \_ 雜訊 \_ TURBULENCE</span><span class="sxs-lookup"><span data-stu-id="9bec6-188">D2D1\_TURBULENCE\_NOISE\_TURBULENCE</span></span>   | <span data-ttu-id="9bec6-189">計算每個 octave 之絕對值的總和。</span><span class="sxs-lookup"><span data-stu-id="9bec6-189">Computes a sum of the absolute value of each octave.</span></span>                                  |



 

> [!Note]  
> <span data-ttu-id="9bec6-190">這兩種模式都不包含輸出值的明確夾具。</span><span class="sxs-lookup"><span data-stu-id="9bec6-190">Neither mode contains an explicit clamp of the output values.</span></span>

 

## <a name="output-bitmap"></a><span data-ttu-id="9bec6-191">輸出點陣圖</span><span class="sxs-lookup"><span data-stu-id="9bec6-191">Output bitmap</span></span>

<span data-ttu-id="9bec6-192">此效果會產生邏輯上無限大小的點陣圖。</span><span class="sxs-lookup"><span data-stu-id="9bec6-192">This effect generates a logically infinite sized bitmap.</span></span>

## <a name="requirements"></a><span data-ttu-id="9bec6-193">規格需求</span><span class="sxs-lookup"><span data-stu-id="9bec6-193">Requirements</span></span>



| <span data-ttu-id="9bec6-194">需求</span><span class="sxs-lookup"><span data-stu-id="9bec6-194">Requirement</span></span> | <span data-ttu-id="9bec6-195">值</span><span class="sxs-lookup"><span data-stu-id="9bec6-195">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9bec6-196">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9bec6-196">Minimum supported client</span></span> | <span data-ttu-id="9bec6-197">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9bec6-197">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="9bec6-198">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9bec6-198">Minimum supported server</span></span> | <span data-ttu-id="9bec6-199">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9bec6-199">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="9bec6-200">標頭</span><span class="sxs-lookup"><span data-stu-id="9bec6-200">Header</span></span>                   | <span data-ttu-id="9bec6-201">d2d1effects。h</span><span class="sxs-lookup"><span data-stu-id="9bec6-201">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="9bec6-202">程式庫</span><span class="sxs-lookup"><span data-stu-id="9bec6-202">Library</span></span>                  | <span data-ttu-id="9bec6-203">d2d1 .lib，dxguid .lib</span><span class="sxs-lookup"><span data-stu-id="9bec6-203">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="9bec6-204">相關主題</span><span class="sxs-lookup"><span data-stu-id="9bec6-204">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9bec6-205">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="9bec6-205">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

