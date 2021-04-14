---
title: 調整效果
description: 使用此效果可將影像向上或向下調整。 效果具有最接近鄰近、線性、三次、多取樣線性、非線性和高品質的三種調整模式。
ms.assetid: 99DFA8DB-384B-4F64-90A2-0D3D7E1ACF27
keywords:
- 調整效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad3af77bc24db387fff0854e0432c270fa2ce6d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384494"
---
# <a name="scale-effect"></a><span data-ttu-id="0e45e-105">調整效果</span><span class="sxs-lookup"><span data-stu-id="0e45e-105">Scale effect</span></span>

<span data-ttu-id="0e45e-106">使用此效果可將影像向上或向下調整。</span><span class="sxs-lookup"><span data-stu-id="0e45e-106">Use this effect to scale an image up or down.</span></span> <span data-ttu-id="0e45e-107">效果具有六個調整模式：最接近的鄰近、線性、三、多取樣線性、非等向和高品質的三層。</span><span class="sxs-lookup"><span data-stu-id="0e45e-107">The effect has six scaling modes: nearest neighbor, linear, cubic, multi-sample linear, anisotropic, and high quality cubic.</span></span>

<span data-ttu-id="0e45e-108">這項效果的 CLSID 是 CLSID \_ D2D1Scale。</span><span class="sxs-lookup"><span data-stu-id="0e45e-108">The CLSID for this effect is CLSID\_D2D1Scale.</span></span>

-   [<span data-ttu-id="0e45e-109">範例影像</span><span class="sxs-lookup"><span data-stu-id="0e45e-109">Example image</span></span>](#example-image)
-   [<span data-ttu-id="0e45e-110">效果屬性</span><span class="sxs-lookup"><span data-stu-id="0e45e-110">Effect properties</span></span>](#effect-properties)
    -   [<span data-ttu-id="0e45e-111">框線模式</span><span class="sxs-lookup"><span data-stu-id="0e45e-111">Border modes</span></span>](#border-modes)
-   [<span data-ttu-id="0e45e-112">插補模式</span><span class="sxs-lookup"><span data-stu-id="0e45e-112">Interpolation modes</span></span>](#interpolation-modes)
-   [<span data-ttu-id="0e45e-113">輸出點陣圖</span><span class="sxs-lookup"><span data-stu-id="0e45e-113">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="0e45e-114">需求</span><span class="sxs-lookup"><span data-stu-id="0e45e-114">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="0e45e-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="0e45e-115">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="0e45e-116">範例影像</span><span class="sxs-lookup"><span data-stu-id="0e45e-116">Example image</span></span>

<span data-ttu-id="0e45e-117">此範例會顯示縮放效果，縮放比例為輸入和裁剪至原始大小的2倍。</span><span class="sxs-lookup"><span data-stu-id="0e45e-117">This example shows the scale effect zooming in 2 times the input and cropping to the original size.</span></span>



| <span data-ttu-id="0e45e-118">之前</span><span class="sxs-lookup"><span data-stu-id="0e45e-118">Before</span></span>                                                     |
|------------------------------------------------------------|
| ![效果之前的影像。](images/default-before.jpg) |
| <span data-ttu-id="0e45e-120">After</span><span class="sxs-lookup"><span data-stu-id="0e45e-120">After</span></span>                                                      |
| ![轉換後的影像。](images/22-scale.png)     |



 


```C++
ComPtr<ID2D1Effect> scaleEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Scale, &scaleEffect);

scaleEffect->SetInput(0, bitmap);

scaleEffect->SetValue(D2D1_SCALE_PROP_CENTER_POINT, D2D1::Vector2F(256.0f, 192.0f));
scaleEffect->SetValue(D2D1_SCALE_PROP_SCALE, D2D1::Vector2F(2.0f, 2.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(scaleEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="0e45e-122">效果屬性</span><span class="sxs-lookup"><span data-stu-id="0e45e-122">Effect properties</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0e45e-123">顯示名稱和索引列舉</span><span class="sxs-lookup"><span data-stu-id="0e45e-123">Display name and index enumeration</span></span></th>
<th><span data-ttu-id="0e45e-124">Description</span><span class="sxs-lookup"><span data-stu-id="0e45e-124">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0e45e-125">調整</span><span class="sxs-lookup"><span data-stu-id="0e45e-125">Scale</span></span><br/> <span data-ttu-id="0e45e-126">D2D1_SCALE_PROP_SCALE</span><span class="sxs-lookup"><span data-stu-id="0e45e-126">D2D1_SCALE_PROP_SCALE</span></span><br/></td>
<td><span data-ttu-id="0e45e-127">以 X 和 Y 方向的比例量，作為輸出大小與輸入大小的比率。</span><span class="sxs-lookup"><span data-stu-id="0e45e-127">The scale amount in the X and Y direction as a ratio of the output size to the input size.</span></span> <span data-ttu-id="0e45e-128">這個屬性會 D2D1_VECTOR_2Fdefined 為： (X 刻度、Y 刻度) 。</span><span class="sxs-lookup"><span data-stu-id="0e45e-128">This property a D2D1_VECTOR_2Fdefined as: (X scale, Y scale).</span></span> <span data-ttu-id="0e45e-129">尺規數量為 FLOAT、無量，且必須為正數或0。</span><span class="sxs-lookup"><span data-stu-id="0e45e-129">The scale amounts are FLOAT, unitless, and must be positive or 0.</span></span><br/> <span data-ttu-id="0e45e-130">此類型為 D2D1_VECTOR_2F。</span><span class="sxs-lookup"><span data-stu-id="0e45e-130">The type is D2D1_VECTOR_2F.</span></span><br/> <span data-ttu-id="0e45e-131">預設值為 {1.0 f、1.0 f}。</span><span class="sxs-lookup"><span data-stu-id="0e45e-131">The default value is {1.0f, 1.0f}.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0e45e-132">CenterPoint</span><span class="sxs-lookup"><span data-stu-id="0e45e-132">CenterPoint</span></span><br/> <span data-ttu-id="0e45e-133">D2D1_SCALE_PROP_CENTER_POINT</span><span class="sxs-lookup"><span data-stu-id="0e45e-133">D2D1_SCALE_PROP_CENTER_POINT</span></span><br/></td>
<td><span data-ttu-id="0e45e-134">影像縮放中心點。</span><span class="sxs-lookup"><span data-stu-id="0e45e-134">The image scaling center point.</span></span> <span data-ttu-id="0e45e-135">這個屬性是定義為： (點 X、點 Y) 的 D2D1_VECTOR_2F。</span><span class="sxs-lookup"><span data-stu-id="0e45e-135">This property is a D2D1_VECTOR_2F defined as: (point X, point Y).</span></span> <span data-ttu-id="0e45e-136">單位為 Dip。</span><span class="sxs-lookup"><span data-stu-id="0e45e-136">The units are in DIPs.</span></span><br/> <span data-ttu-id="0e45e-137">使用中央點屬性來圍繞左上角的某個點進行縮放。</span><span class="sxs-lookup"><span data-stu-id="0e45e-137">Use the center point property to scale around a point other than the upper-left corner.</span></span><br/> <span data-ttu-id="0e45e-138">此類型為 D2D1_VECTOR_2F。</span><span class="sxs-lookup"><span data-stu-id="0e45e-138">The type is D2D1_VECTOR_2F.</span></span><br/> <span data-ttu-id="0e45e-139">預設值為 {0.0 f，0.0 f}。</span><span class="sxs-lookup"><span data-stu-id="0e45e-139">The default value is {0.0f, 0.0f}.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0e45e-140">BorderMode</span><span class="sxs-lookup"><span data-stu-id="0e45e-140">BorderMode</span></span><br/> <span data-ttu-id="0e45e-141">D2D1_SCALE_PROP_BORDER_MODE</span><span class="sxs-lookup"><span data-stu-id="0e45e-141">D2D1_SCALE_PROP_BORDER_MODE</span></span><br/></td>
<td><span data-ttu-id="0e45e-142">用來計算影像（軟或硬）框線的模式。</span><span class="sxs-lookup"><span data-stu-id="0e45e-142">The mode used to calculate the border of the image, soft or hard.</span></span> <span data-ttu-id="0e45e-143">如需詳細資訊，請參閱 <a href="#border-modes">框線模式</a> 。</span><span class="sxs-lookup"><span data-stu-id="0e45e-143">See <a href="#border-modes">Border modes</a> for more info.</span></span> <br/> <span data-ttu-id="0e45e-144">此類型為 D2D1_BORDER_MODE。</span><span class="sxs-lookup"><span data-stu-id="0e45e-144">The type is D2D1_BORDER_MODE.</span></span><br/> <span data-ttu-id="0e45e-145">預設值為 D2D1_BORDER_MODE_SOFT。</span><span class="sxs-lookup"><span data-stu-id="0e45e-145">The default value is D2D1_BORDER_MODE_SOFT.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0e45e-146">清晰度</span><span class="sxs-lookup"><span data-stu-id="0e45e-146">Sharpness</span></span><br/> <span data-ttu-id="0e45e-147">D2D1_SCALE_PROP_SHARPNESS</span><span class="sxs-lookup"><span data-stu-id="0e45e-147">D2D1_SCALE_PROP_SHARPNESS</span></span><br/></td>
<td><span data-ttu-id="0e45e-148">在高品質的三重插補點模式中，調整篩選的清晰度層級是介於0和1之間的浮點數。</span><span class="sxs-lookup"><span data-stu-id="0e45e-148">In the high quality cubic interpolation mode, the sharpness level of the scaling filter as a float between 0 and 1.</span></span> <span data-ttu-id="0e45e-149">這些值沒有用。</span><span class="sxs-lookup"><span data-stu-id="0e45e-149">The values are unitless.</span></span> <span data-ttu-id="0e45e-150">您可以使用「清晰度」來調整影像向下調整時的影像品質。</span><span class="sxs-lookup"><span data-stu-id="0e45e-150">You can use sharpness to adjust the quality of an image when you scale the image down.</span></span><br/> <span data-ttu-id="0e45e-151">清晰度因素會影響核心的圖形。</span><span class="sxs-lookup"><span data-stu-id="0e45e-151">The sharpness factor affects the shape of the kernel.</span></span> <span data-ttu-id="0e45e-152">最高的清晰度因數越小，核心就越小。</span><span class="sxs-lookup"><span data-stu-id="0e45e-152">The higher the sharpness factor, the smaller the kernel.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="0e45e-153">這個屬性只會影響高品質的三次插補模式。</span><span class="sxs-lookup"><span data-stu-id="0e45e-153">This property affects only the high quality cubic interpolation mode.</span></span>
</blockquote>
<br/> <span data-ttu-id="0e45e-154">此類型為 FLOAT。</span><span class="sxs-lookup"><span data-stu-id="0e45e-154">The type is FLOAT.</span></span><br/> <span data-ttu-id="0e45e-155">預設值為 0.0 f。</span><span class="sxs-lookup"><span data-stu-id="0e45e-155">The default value is 0.0f.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0e45e-156">InterpolationMode</span><span class="sxs-lookup"><span data-stu-id="0e45e-156">InterpolationMode</span></span><br/> <span data-ttu-id="0e45e-157">D2D1_SCALE_PROP_INTERPOLATION_MODE</span><span class="sxs-lookup"><span data-stu-id="0e45e-157">D2D1_SCALE_PROP_INTERPOLATION_MODE</span></span><br/></td>
<td><span data-ttu-id="0e45e-158">效果用來調整影像的插補模式。</span><span class="sxs-lookup"><span data-stu-id="0e45e-158">The interpolation mode the effect uses to scale the image.</span></span> <span data-ttu-id="0e45e-159">有6個調整模式的品質和速度範圍。</span><span class="sxs-lookup"><span data-stu-id="0e45e-159">There are 6 scale modes that range in quality and speed.</span></span> <span data-ttu-id="0e45e-160">如需詳細資訊，請參閱 <a href="#interpolation-modes">插補模式</a> 。</span><span class="sxs-lookup"><span data-stu-id="0e45e-160">See <a href="#interpolation-modes">Interpolation modes</a> for more info.</span></span> <br/> <span data-ttu-id="0e45e-161">此類型為 D2D1_SCALE_INTERPOLATION_MODE。</span><span class="sxs-lookup"><span data-stu-id="0e45e-161">The type is D2D1_SCALE_INTERPOLATION_MODE.</span></span><br/> <span data-ttu-id="0e45e-162">預設值為 D2D1_SCALE_INTERPOLATION_MODE_LINEAR。</span><span class="sxs-lookup"><span data-stu-id="0e45e-162">The default value is D2D1_SCALE_INTERPOLATION_MODE_LINEAR.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="border-modes"></a><span data-ttu-id="0e45e-163">框線模式</span><span class="sxs-lookup"><span data-stu-id="0e45e-163">Border modes</span></span>



| <span data-ttu-id="0e45e-164">Name</span><span class="sxs-lookup"><span data-stu-id="0e45e-164">Name</span></span>                     | <span data-ttu-id="0e45e-165">描述</span><span class="sxs-lookup"><span data-stu-id="0e45e-165">Description</span></span>                                                                                                                                                                                                                                                              |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e45e-166">D2D1 \_ 框線 \_ 模式 \_ 軟</span><span class="sxs-lookup"><span data-stu-id="0e45e-166">D2D1\_BORDER\_MODE\_SOFT</span></span> | <span data-ttu-id="0e45e-167">此效果會在輸入影像套用卷積核心時，以透明的黑色圖元為單位，以透明的方式在輸入界限之外取得樣本。</span><span class="sxs-lookup"><span data-stu-id="0e45e-167">The effect pads the input image with transparent black pixels for samples outside of the input bounds when it applies the convolution kernel.</span></span> <span data-ttu-id="0e45e-168">這會建立影像的軟邊緣，並且在進程中依核心的大小展開輸出點陣圖。</span><span class="sxs-lookup"><span data-stu-id="0e45e-168">This creates a soft edge for the image, and in the process expands the output bitmap by the size of the kernel.</span></span><br/> |
| <span data-ttu-id="0e45e-169">D2D1 \_ 框線 \_ 模式 \_ 硬性</span><span class="sxs-lookup"><span data-stu-id="0e45e-169">D2D1\_BORDER\_MODE\_HARD</span></span> | <span data-ttu-id="0e45e-170">效果會使用鏡像類型的框線轉換來擴充輸入界限之外樣本的輸入影像。</span><span class="sxs-lookup"><span data-stu-id="0e45e-170">The effect extends the input image with a mirror-type border transform for samples outside of the input bounds.</span></span> <span data-ttu-id="0e45e-171">輸出點陣圖的大小等於輸入點陣圖的大小。</span><span class="sxs-lookup"><span data-stu-id="0e45e-171">The size of the output bitmap is equal to the size of the input bitmap.</span></span><br/>                                                                       |



 

\`

## <a name="interpolation-modes"></a><span data-ttu-id="0e45e-172">插補模式</span><span class="sxs-lookup"><span data-stu-id="0e45e-172">Interpolation modes</span></span>



| <span data-ttu-id="0e45e-173">列舉型別</span><span class="sxs-lookup"><span data-stu-id="0e45e-173">Enumeration</span></span>                                             | <span data-ttu-id="0e45e-174">描述</span><span class="sxs-lookup"><span data-stu-id="0e45e-174">Description</span></span>                                                                                                                                                                                          |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e45e-175">D2D1 \_ 縮放 \_ 插補 \_ 模式 \_ 最接近 \_ 鄰近</span><span class="sxs-lookup"><span data-stu-id="0e45e-175">D2D1\_SCALE\_INTERPOLATION\_MODE\_NEAREST\_NEIGHBOR</span></span>     | <span data-ttu-id="0e45e-176">範例最接近的單一點，並使用該點。</span><span class="sxs-lookup"><span data-stu-id="0e45e-176">Samples the nearest single point and uses that.</span></span> <span data-ttu-id="0e45e-177">這個模式會使用較少的處理時間，但會輸出最低品質的影像。</span><span class="sxs-lookup"><span data-stu-id="0e45e-177">This mode uses less processing time, but outputs the lowest quality image.</span></span>                                                                           |
| <span data-ttu-id="0e45e-178">D2D1 \_ SCALE \_ 插補 \_ 模式 \_ 線性</span><span class="sxs-lookup"><span data-stu-id="0e45e-178">D2D1\_SCALE\_INTERPOLATION\_MODE\_LINEAR</span></span>                | <span data-ttu-id="0e45e-179">使用四個點取樣和線性插補。</span><span class="sxs-lookup"><span data-stu-id="0e45e-179">Uses a four point sample and linear interpolation.</span></span> <span data-ttu-id="0e45e-180">這個模式所使用的處理時間比最近的鄰近模式更多，但會輸出較高品質的影像。</span><span class="sxs-lookup"><span data-stu-id="0e45e-180">This mode uses more processing time than the nearest neighbor mode, but outputs a higher quality image.</span></span>                                           |
| <span data-ttu-id="0e45e-181">D2D1 \_ SCALE \_ 插補 \_ 模式 \_ 立方</span><span class="sxs-lookup"><span data-stu-id="0e45e-181">D2D1\_SCALE\_INTERPOLATION\_MODE\_CUBIC</span></span>                 | <span data-ttu-id="0e45e-182">使用16個範例三核心來進行插補。</span><span class="sxs-lookup"><span data-stu-id="0e45e-182">Uses a 16 sample cubic kernel for interpolation.</span></span> <span data-ttu-id="0e45e-183">這個模式會使用大部分的處理時間，但會輸出較高品質的影像。</span><span class="sxs-lookup"><span data-stu-id="0e45e-183">This mode uses the most processing time, but outputs a higher quality image.</span></span>                                                                        |
| <span data-ttu-id="0e45e-184">D2D1 \_ SCALE \_ 內插補點 \_ 模式 \_ 多 \_ 樣本 \_ 線性</span><span class="sxs-lookup"><span data-stu-id="0e45e-184">D2D1\_SCALE\_INTERPOLATION\_MODE\_MULTI\_SAMPLE\_LINEAR</span></span> | <span data-ttu-id="0e45e-185">使用單一圖元內的4個線性樣本來取得良好的邊緣消除鋸齒。</span><span class="sxs-lookup"><span data-stu-id="0e45e-185">Uses 4 linear samples within a single pixel for good edge anti-aliasing.</span></span> <span data-ttu-id="0e45e-186">這種模式適合用來在具有少量圖元的影像上相應減少量。</span><span class="sxs-lookup"><span data-stu-id="0e45e-186">This mode is good for scaling down by small amounts on images with few pixels.</span></span>                                              |
| <span data-ttu-id="0e45e-187">D2D1 \_ 調整 \_ 內插補點 \_ 模式 \_</span><span class="sxs-lookup"><span data-stu-id="0e45e-187">D2D1\_SCALE\_INTERPOLATION\_MODE\_ANISOTROPIC</span></span>           | <span data-ttu-id="0e45e-188">根據點陣圖的轉換圖形，使用非等向篩選來取樣模式。</span><span class="sxs-lookup"><span data-stu-id="0e45e-188">Uses anisotropic filtering to sample a pattern according to the transformed shape of the bitmap.</span></span>                                                                                                     |
| <span data-ttu-id="0e45e-189">D2D1 \_ 調整 \_ 插補 \_ 模式 \_ 高品質的 \_ \_ 三階</span><span class="sxs-lookup"><span data-stu-id="0e45e-189">D2D1\_SCALE\_INTERPOLATION\_MODE\_HIGH\_QUALITY\_CUBIC</span></span>  | <span data-ttu-id="0e45e-190">如果 downscaling 與轉換矩陣有關，則使用可變大小的高品質三核心來執行預先縮小的影像。</span><span class="sxs-lookup"><span data-stu-id="0e45e-190">Uses a variable size high quality cubic kernel to perform a pre-downscale the image if downscaling is involved in the transform matrix.</span></span> <span data-ttu-id="0e45e-191">然後使用三次插補模式來進行最終輸出。</span><span class="sxs-lookup"><span data-stu-id="0e45e-191">Then uses the cubic interpolation mode for the final output.</span></span> |



 

> [!Note]  
> <span data-ttu-id="0e45e-192">如果您未選取模式，效果會預設為 D2D1 \_ 縮放 \_ 插補 \_ 模式 \_ 線性。</span><span class="sxs-lookup"><span data-stu-id="0e45e-192">If you don't select a mode, the effect defaults to D2D1\_SCALE\_INTERPOLATION\_MODE\_LINEAR.</span></span>

 

> [!Note]  
> <span data-ttu-id="0e45e-193">當調整時，非等向模式會產生 mipmap，不過，如果您在輸入至此效果的效果上將快取 **的屬性設** 為 true，則每次都不會針對足夠的小型影像產生 mipmap。</span><span class="sxs-lookup"><span data-stu-id="0e45e-193">Anisotropic mode generates mipmaps when scaling, however, if you set the **Cached** property to true on the effects that are input to this effect, the mipmaps won't be generated every time for sufficiently small images.</span></span>

 

## <a name="output-bitmap"></a><span data-ttu-id="0e45e-194">輸出點陣圖</span><span class="sxs-lookup"><span data-stu-id="0e45e-194">Output bitmap</span></span>

<span data-ttu-id="0e45e-195">輸出點陣圖的位置和大小取決於指定的縮放比例和中心點。</span><span class="sxs-lookup"><span data-stu-id="0e45e-195">The location and size of the output bitmap depends on the specified scale factor and the center point.</span></span>

<span data-ttu-id="0e45e-196">您可以使用此方程式來計算輸出點陣圖的大小：</span><span class="sxs-lookup"><span data-stu-id="0e45e-196">You can calculate the size of the output bitmap using this equation:</span></span><dl> <span data-ttu-id="0e45e-197">BitmapSize？ (圖元) = 調整？ \*原始點陣圖大小？</span><span class="sxs-lookup"><span data-stu-id="0e45e-197">BitmapSize?(Pixels)=Scale?\*Original Bitmap Size?</span></span> <span data-ttu-id="0e45e-198"> (Dip) \* (UserDPI/96) </span><span class="sxs-lookup"><span data-stu-id="0e45e-198">(DIPs)\*(UserDPI/96)</span></span>  
<span data-ttu-id="0e45e-199">BitmapSize<sub>y</sub> (圖元) = 縮放<sub>y</sub> \* 原始點陣圖大小<sub>y</sub> (dip) \* (UserDPI/96) </span><span class="sxs-lookup"><span data-stu-id="0e45e-199">BitmapSize<sub>y</sub>(Pixels)=Scale<sub>y</sub>\*Original Bitmap Size<sub>y</sub> (DIPs)\*(UserDPI/96)</span></span>  
</dl>

<span data-ttu-id="0e45e-200">效果會將圖元的分數四捨五入到最接近的整個圖元。</span><span class="sxs-lookup"><span data-stu-id="0e45e-200">The effect rounds fractions of pixels up to the nearest whole pixel.</span></span>

<span data-ttu-id="0e45e-201">點陣圖的位置是 (0、0) 或中心點屬性的值。</span><span class="sxs-lookup"><span data-stu-id="0e45e-201">The location of the bitmap is (0, 0) or the value of the center point property.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e45e-202">規格需求</span><span class="sxs-lookup"><span data-stu-id="0e45e-202">Requirements</span></span>



| <span data-ttu-id="0e45e-203">需求</span><span class="sxs-lookup"><span data-stu-id="0e45e-203">Requirement</span></span> | <span data-ttu-id="0e45e-204">值</span><span class="sxs-lookup"><span data-stu-id="0e45e-204">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0e45e-205">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0e45e-205">Minimum supported client</span></span> | <span data-ttu-id="0e45e-206">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0e45e-206">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="0e45e-207">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0e45e-207">Minimum supported server</span></span> | <span data-ttu-id="0e45e-208">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0e45e-208">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="0e45e-209">標頭</span><span class="sxs-lookup"><span data-stu-id="0e45e-209">Header</span></span>                   | <span data-ttu-id="0e45e-210">d2d1effects。h</span><span class="sxs-lookup"><span data-stu-id="0e45e-210">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="0e45e-211">程式庫</span><span class="sxs-lookup"><span data-stu-id="0e45e-211">Library</span></span>                  | <span data-ttu-id="0e45e-212">d2d1 .lib，dxguid .lib</span><span class="sxs-lookup"><span data-stu-id="0e45e-212">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="0e45e-213">相關主題</span><span class="sxs-lookup"><span data-stu-id="0e45e-213">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e45e-214">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="0e45e-214">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

