---
title: 2D 仿射轉換效果
description: 2D 仿射轉換效果會使用 Direct2D 矩陣轉換和六個插補模式的任一個，根據3X2 矩陣將空間轉換套用至影像。
ms.assetid: E8973EBE-764C-4220-BB1E-3BFD4853582D
keywords:
- 2D 仿射轉換效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3017992d34cd98095f01192ea948684a6b52e53
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106565"
---
# <a name="2d-affine-transform-effect"></a><span data-ttu-id="9bf07-104">2D 仿射轉換效果</span><span class="sxs-lookup"><span data-stu-id="9bf07-104">2D affine transform effect</span></span>

<span data-ttu-id="9bf07-105">2D 仿射轉換效果會使用 Direct2D 矩陣 [轉換](direct2d-transforms-overview.md) 和六個插補模式的任一個，根據3X2 矩陣將空間轉換套用至影像。</span><span class="sxs-lookup"><span data-stu-id="9bf07-105">The 2D affine transform effect applies a spatial transform to a image based on a 3X2 matrix using the Direct2D matrix [transform](direct2d-transforms-overview.md) and any of six interpolation modes.</span></span> <span data-ttu-id="9bf07-106">您可以使用此效果來旋轉、縮放、扭曲或轉譯影像。</span><span class="sxs-lookup"><span data-stu-id="9bf07-106">You can use this effect to rotate, scale, skew, or translate an image.</span></span> <span data-ttu-id="9bf07-107">或者，您可以結合這些作業。</span><span class="sxs-lookup"><span data-stu-id="9bf07-107">Or, you can combine these operations.</span></span> <span data-ttu-id="9bf07-108">仿射傳輸會保留平行線，以及影像中任何三個點之間的距離比例。</span><span class="sxs-lookup"><span data-stu-id="9bf07-108">Affine transfers preserve parallel lines and the ratio of distances between any three points in an image.</span></span>

<span data-ttu-id="9bf07-109">這項效果的 CLSID 是 CLSID \_ D2D12DAffineTransform。</span><span class="sxs-lookup"><span data-stu-id="9bf07-109">The CLSID for this effect is CLSID\_D2D12DAffineTransform.</span></span>

-   [<span data-ttu-id="9bf07-110">範例影像</span><span class="sxs-lookup"><span data-stu-id="9bf07-110">Example image</span></span>](#example-image)
-   [<span data-ttu-id="9bf07-111">效果屬性</span><span class="sxs-lookup"><span data-stu-id="9bf07-111">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="9bf07-112">框線模式</span><span class="sxs-lookup"><span data-stu-id="9bf07-112">Border modes</span></span>](#border-modes)
-   [<span data-ttu-id="9bf07-113">插補模式</span><span class="sxs-lookup"><span data-stu-id="9bf07-113">Interpolation modes</span></span>](#interpolation-modes)
-   [<span data-ttu-id="9bf07-114">輸出點陣圖</span><span class="sxs-lookup"><span data-stu-id="9bf07-114">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="9bf07-115">需求</span><span class="sxs-lookup"><span data-stu-id="9bf07-115">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="9bf07-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="9bf07-116">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="9bf07-117">範例影像</span><span class="sxs-lookup"><span data-stu-id="9bf07-117">Example image</span></span>



| <span data-ttu-id="9bf07-118">之前</span><span class="sxs-lookup"><span data-stu-id="9bf07-118">Before</span></span>                                                             |
|--------------------------------------------------------------------|
| ![效果之前的影像。](images/default-before.jpg)         |
| <span data-ttu-id="9bf07-120">After</span><span class="sxs-lookup"><span data-stu-id="9bf07-120">After</span></span>                                                              |
| ![轉換後的影像。](images/21-2daffinetransform.png) |



 


```C++
ComPtr<ID2D1Effect> affineTransformEffect;
m_d2dContext->CreateEffect(CLSID_D2D12DAffineTransform, &affineTransformEffect);

affineTransformEffect->SetInput(0, bitmap);

D2D1_MATRIX_3X2_F matrix = D2D1::Matrix3x2F(0.9f, -0.1f,   0.1f, 0.9f,   8.0f, 45.0f);

affineTransformEffect->SetValue(D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX, matrix);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(affineTransformEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="9bf07-122">此效果會執行此矩陣作業：</span><span class="sxs-lookup"><span data-stu-id="9bf07-122">This effect performs this matrix operation:</span></span>

![仿射矩陣運算](images/affine-matrix-calculation.png)

<span data-ttu-id="9bf07-124">雖然輸入矩陣定義為3x2 矩陣，但最後一個資料行會以0、0和1填補，以產生正方形矩陣。</span><span class="sxs-lookup"><span data-stu-id="9bf07-124">Although the input matrix is defined as a 3x2 matrix, the last column is padded with 0, 0 and 1 to produce a square matrix.</span></span> <span data-ttu-id="9bf07-125">這可允許矩陣相乘，以便將轉換串連成單一矩陣。</span><span class="sxs-lookup"><span data-stu-id="9bf07-125">This allows for matrix multiplication, so that transforms can be concatenated into a single matrix.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="9bf07-126">效果屬性</span><span class="sxs-lookup"><span data-stu-id="9bf07-126">Effect properties</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9bf07-127">顯示名稱和索引列舉</span><span class="sxs-lookup"><span data-stu-id="9bf07-127">Display name and index enumeration</span></span></th>
<th><span data-ttu-id="9bf07-128">Description</span><span class="sxs-lookup"><span data-stu-id="9bf07-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9bf07-129">InterpolationMode</span><span class="sxs-lookup"><span data-stu-id="9bf07-129">InterpolationMode</span></span><br/> <span data-ttu-id="9bf07-130">D2D1_2DAFFINETRANSFORM_PROP_INTERPOLATION_MODE</span><span class="sxs-lookup"><span data-stu-id="9bf07-130">D2D1_2DAFFINETRANSFORM_PROP_INTERPOLATION_MODE</span></span><br/></td>
<td><span data-ttu-id="9bf07-131">用來調整影像的插補模式。</span><span class="sxs-lookup"><span data-stu-id="9bf07-131">The interpolation mode used to scale the image.</span></span> <span data-ttu-id="9bf07-132">有6個調整模式的品質和速度範圍。</span><span class="sxs-lookup"><span data-stu-id="9bf07-132">There are 6 scale modes that range in quality and speed.</span></span><br/> <span data-ttu-id="9bf07-133">類型為 D2D1_2DAFFINETRANSFORM_INTERPOLATION_MODE。</span><span class="sxs-lookup"><span data-stu-id="9bf07-133">Type is D2D1_2DAFFINETRANSFORM_INTERPOLATION_MODE.</span></span><br/> <span data-ttu-id="9bf07-134">預設值為 D2D1_2DAFFINETRANSFORM_INTERPOLATION_MODE_LINEAR。</span><span class="sxs-lookup"><span data-stu-id="9bf07-134">Default value is D2D1_2DAFFINETRANSFORM_INTERPOLATION_MODE_LINEAR.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9bf07-135">BorderMode</span><span class="sxs-lookup"><span data-stu-id="9bf07-135">BorderMode</span></span><br/> <span data-ttu-id="9bf07-136">D2D1_2DAFFINETRANSFORM_PROP_BORDER_MODE</span><span class="sxs-lookup"><span data-stu-id="9bf07-136">D2D1_2DAFFINETRANSFORM_PROP_BORDER_MODE</span></span><br/></td>
<td><span data-ttu-id="9bf07-137">用來計算影像（軟或硬）框線的模式。</span><span class="sxs-lookup"><span data-stu-id="9bf07-137">The mode used to calculate the border of the image, soft or hard.</span></span> <span data-ttu-id="9bf07-138">如需詳細資訊，請參閱 <a href="https://www.bing.com/search?q=Border+modes">框線模式</a> 。</span><span class="sxs-lookup"><span data-stu-id="9bf07-138">See <a href="https://www.bing.com/search?q=Border+modes">Border modes</a> for more info.</span></span> <br/> <span data-ttu-id="9bf07-139">類型為 D2D1_BORDER_MODE。</span><span class="sxs-lookup"><span data-stu-id="9bf07-139">Type is D2D1_BORDER_MODE.</span></span><br/> <span data-ttu-id="9bf07-140">預設值為 D2D1_BORDER_MODE_SOFT。</span><span class="sxs-lookup"><span data-stu-id="9bf07-140">Default value is D2D1_BORDER_MODE_SOFT.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9bf07-141">TransformMatrix</span><span class="sxs-lookup"><span data-stu-id="9bf07-141">TransformMatrix</span></span><br/> <span data-ttu-id="9bf07-142">D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX</span><span class="sxs-lookup"><span data-stu-id="9bf07-142">D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX</span></span><br/></td>
<td><span data-ttu-id="9bf07-143">使用 Direct2D 矩陣 <a href="direct2d-transforms-overview.md">轉換</a>來轉換影像的3x2 矩陣。</span><span class="sxs-lookup"><span data-stu-id="9bf07-143">The 3x2 matrix to transform the image using the Direct2D matrix <a href="direct2d-transforms-overview.md">transform</a>.</span></span> <br/> <span data-ttu-id="9bf07-144">類型為 D2D1_MATRIX_3X2_F。</span><span class="sxs-lookup"><span data-stu-id="9bf07-144">Type is D2D1_MATRIX_3X2_F.</span></span><br/> <span data-ttu-id="9bf07-145">預設值為 Matrix3x2F：： Identity () 。</span><span class="sxs-lookup"><span data-stu-id="9bf07-145">Default value is Matrix3x2F::Identity().</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9bf07-146">清晰度</span><span class="sxs-lookup"><span data-stu-id="9bf07-146">Sharpness</span></span><br/> <span data-ttu-id="9bf07-147">D2D1_2DAFFINETRANSFORM_PROP_SHARPNESS</span><span class="sxs-lookup"><span data-stu-id="9bf07-147">D2D1_2DAFFINETRANSFORM_PROP_SHARPNESS</span></span><br/></td>
<td><span data-ttu-id="9bf07-148">在高品質的三重插補點模式中，調整篩選的清晰度層級是介於0和1之間的浮點數。</span><span class="sxs-lookup"><span data-stu-id="9bf07-148">In the high quality cubic interpolation mode, the sharpness level of the scaling filter as a float between 0 and 1.</span></span> <span data-ttu-id="9bf07-149">這些值沒有用。</span><span class="sxs-lookup"><span data-stu-id="9bf07-149">The values are unitless.</span></span> <span data-ttu-id="9bf07-150">您可以使用清晰度來調整影像縮放時的影像品質。</span><span class="sxs-lookup"><span data-stu-id="9bf07-150">You can use sharpness to adjust the quality of an image when you scale the image.</span></span><br/> <span data-ttu-id="9bf07-151">清晰度因素會影響核心的圖形。</span><span class="sxs-lookup"><span data-stu-id="9bf07-151">The sharpness factor affects the shape of the kernel.</span></span> <span data-ttu-id="9bf07-152">最高的清晰度因數越小，核心就越小。</span><span class="sxs-lookup"><span data-stu-id="9bf07-152">The higher the sharpness factor, the smaller the kernel.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="9bf07-153">這個屬性只會影響高品質的三次插補模式。</span><span class="sxs-lookup"><span data-stu-id="9bf07-153">This property affects only the high quality cubic interpolation mode.</span></span>
</blockquote>
<br/> <span data-ttu-id="9bf07-154">類型為 FLOAT。</span><span class="sxs-lookup"><span data-stu-id="9bf07-154">Type is FLOAT.</span></span><br/> <span data-ttu-id="9bf07-155">預設值為 1.0 f。</span><span class="sxs-lookup"><span data-stu-id="9bf07-155">Default value is 1.0f.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="border-modes"></a><span data-ttu-id="9bf07-156">框線模式</span><span class="sxs-lookup"><span data-stu-id="9bf07-156">Border modes</span></span>



| <span data-ttu-id="9bf07-157">Name</span><span class="sxs-lookup"><span data-stu-id="9bf07-157">Name</span></span>                     | <span data-ttu-id="9bf07-158">描述</span><span class="sxs-lookup"><span data-stu-id="9bf07-158">Description</span></span>                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bf07-159">D2D1 \_ 框線 \_ 模式 \_ 軟</span><span class="sxs-lookup"><span data-stu-id="9bf07-159">D2D1\_BORDER\_MODE\_SOFT</span></span> | <span data-ttu-id="9bf07-160">效果會在插補時以透明黑色圖元來填補影像，進而產生軟邊緣。</span><span class="sxs-lookup"><span data-stu-id="9bf07-160">The effect pads the image with transparent black pixels as it interpolates, resulting in a soft edge.</span></span><br/> |
| <span data-ttu-id="9bf07-161">D2D1 \_ 框線 \_ 模式 \_ 硬性</span><span class="sxs-lookup"><span data-stu-id="9bf07-161">D2D1\_BORDER\_MODE\_HARD</span></span> | <span data-ttu-id="9bf07-162">效果會將輸出個至輸入影像的大小。</span><span class="sxs-lookup"><span data-stu-id="9bf07-162">The effect clamps the output to the size of the input image.</span></span> <br/>                                         |



 

## <a name="interpolation-modes"></a><span data-ttu-id="9bf07-163">插補模式</span><span class="sxs-lookup"><span data-stu-id="9bf07-163">Interpolation modes</span></span>



| <span data-ttu-id="9bf07-164">列舉型別</span><span class="sxs-lookup"><span data-stu-id="9bf07-164">Enumeration</span></span>                                                         | <span data-ttu-id="9bf07-165">描述</span><span class="sxs-lookup"><span data-stu-id="9bf07-165">Description</span></span>                                                                                                                                                                                          |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bf07-166">\_ \_ \_ \_ 最接近 \_ 鄰近的 D2D1 2DAFFINETRANSFORM 插補模式</span><span class="sxs-lookup"><span data-stu-id="9bf07-166">D2D1\_2DAFFINETRANSFORM\_INTERPOLATION\_MODE\_NEAREST\_NEIGHBOR</span></span>     | <span data-ttu-id="9bf07-167">範例最接近的單一點，並使用該點。</span><span class="sxs-lookup"><span data-stu-id="9bf07-167">Samples the nearest single point and uses that.</span></span> <span data-ttu-id="9bf07-168">這個模式會使用較少的處理時間，但會輸出最低品質的影像。</span><span class="sxs-lookup"><span data-stu-id="9bf07-168">This mode uses less processing time, but outputs the lowest quality image.</span></span>                                                                           |
| <span data-ttu-id="9bf07-169">D2D1 \_ 2DAFFINETRANSFORM \_ 插補 \_ 模式 \_ 線性</span><span class="sxs-lookup"><span data-stu-id="9bf07-169">D2D1\_2DAFFINETRANSFORM\_INTERPOLATION\_MODE\_LINEAR</span></span>                | <span data-ttu-id="9bf07-170">使用四個點取樣和線性插補。</span><span class="sxs-lookup"><span data-stu-id="9bf07-170">Uses a four point sample and linear interpolation.</span></span> <span data-ttu-id="9bf07-171">這個模式所使用的處理時間比最近的鄰近模式更多，但會輸出較高品質的影像。</span><span class="sxs-lookup"><span data-stu-id="9bf07-171">This mode uses more processing time than the nearest neighbor mode, but outputs a higher quality image.</span></span>                                           |
| <span data-ttu-id="9bf07-172">D2D1 \_ 2DAFFINETRANSFORM \_ 插補 \_ 模式 \_ 立方</span><span class="sxs-lookup"><span data-stu-id="9bf07-172">D2D1\_2DAFFINETRANSFORM\_INTERPOLATION\_MODE\_CUBIC</span></span>                 | <span data-ttu-id="9bf07-173">使用16個範例三核心來進行插補。</span><span class="sxs-lookup"><span data-stu-id="9bf07-173">Uses a 16 sample cubic kernel for interpolation.</span></span> <span data-ttu-id="9bf07-174">這個模式會使用大部分的處理時間，但會輸出較高品質的影像。</span><span class="sxs-lookup"><span data-stu-id="9bf07-174">This mode uses the most processing time, but outputs a higher quality image.</span></span>                                                                        |
| <span data-ttu-id="9bf07-175">D2D1 \_ 2DAFFINETRANSFORM \_ 插補 \_ 模式 \_ 多 \_ 樣本 \_ 線性</span><span class="sxs-lookup"><span data-stu-id="9bf07-175">D2D1\_2DAFFINETRANSFORM\_INTERPOLATION\_MODE\_MULTI\_SAMPLE\_LINEAR</span></span> | <span data-ttu-id="9bf07-176">使用單一圖元內的4個線性樣本來取得良好的邊緣消除鋸齒。</span><span class="sxs-lookup"><span data-stu-id="9bf07-176">Uses 4 linear samples within a single pixel for good edge anti-aliasing.</span></span> <span data-ttu-id="9bf07-177">這種模式適合用來在具有少量圖元的影像上相應減少量。</span><span class="sxs-lookup"><span data-stu-id="9bf07-177">This mode is good for scaling down by small amounts on images with few pixels.</span></span>                                              |
| <span data-ttu-id="9bf07-178">D2D1 \_ 2DAFFINETRANSFORM \_ 插補 \_ 模式 \_ 各向異性</span><span class="sxs-lookup"><span data-stu-id="9bf07-178">D2D1\_2DAFFINETRANSFORM\_INTERPOLATION\_MODE\_ANISOTROPIC</span></span>           | <span data-ttu-id="9bf07-179">根據點陣圖的轉換圖形，使用非等向篩選來取樣模式。</span><span class="sxs-lookup"><span data-stu-id="9bf07-179">Uses anisotropic filtering to sample a pattern according to the transformed shape of the bitmap.</span></span>                                                                                                     |
| <span data-ttu-id="9bf07-180">D2D1 \_ 2DAFFINETRANSFORM \_ 插補 \_ 模式 \_ 高 \_ 品質 \_ 三次</span><span class="sxs-lookup"><span data-stu-id="9bf07-180">D2D1\_2DAFFINETRANSFORM\_INTERPOLATION\_MODE\_HIGH\_QUALITY\_CUBIC</span></span>  | <span data-ttu-id="9bf07-181">如果 downscaling 與轉換矩陣有關，則使用可變大小的高品質三核心來執行預先縮小的影像。</span><span class="sxs-lookup"><span data-stu-id="9bf07-181">Uses a variable size high quality cubic kernel to perform a pre-downscale the image if downscaling is involved in the transform matrix.</span></span> <span data-ttu-id="9bf07-182">然後使用三次插補模式來進行最終輸出。</span><span class="sxs-lookup"><span data-stu-id="9bf07-182">Then uses the cubic interpolation mode for the final output.</span></span> |



 

> [!Note]  
> <span data-ttu-id="9bf07-183">如果您未選取模式，效果會預設為 D2D1 \_ 2DAFFINETRANSFORM \_ 插補 \_ 模式 \_ 線性。</span><span class="sxs-lookup"><span data-stu-id="9bf07-183">If you don't select a mode, the effect defaults to D2D1\_2DAFFINETRANSFORM\_INTERPOLATION\_MODE\_LINEAR.</span></span>

 

> [!Note]  
> <span data-ttu-id="9bf07-184">當調整時，非等向模式會產生 mipmap，不過，如果您在輸入至此效果的效果上將快取 **的屬性設** 為 true，則每次都不會針對足夠的小型影像產生 mipmap。</span><span class="sxs-lookup"><span data-stu-id="9bf07-184">Anisotropic mode generates mipmaps when scaling, however, if you set the **Cached** property to true on the effects that are input to this effect, the mipmaps won't be generated every time for sufficiently small images.</span></span>

 

## <a name="output-bitmap"></a><span data-ttu-id="9bf07-185">輸出點陣圖</span><span class="sxs-lookup"><span data-stu-id="9bf07-185">Output bitmap</span></span>

<span data-ttu-id="9bf07-186">輸出點陣圖的大小取決於套用至影像的轉換矩陣。</span><span class="sxs-lookup"><span data-stu-id="9bf07-186">The size of the output bitmap depends on the transform matrix that is applied to the image.</span></span>

<span data-ttu-id="9bf07-187">效果會執行轉換作業，然後在結果周圍套用周框方塊。</span><span class="sxs-lookup"><span data-stu-id="9bf07-187">The effect performs the transform operation and then applies a bounding box around the result.</span></span> <span data-ttu-id="9bf07-188">輸出點陣圖是周框方塊的大小。</span><span class="sxs-lookup"><span data-stu-id="9bf07-188">The output bitmap is the size of the bounding box.</span></span>

## <a name="requirements"></a><span data-ttu-id="9bf07-189">規格需求</span><span class="sxs-lookup"><span data-stu-id="9bf07-189">Requirements</span></span>



| <span data-ttu-id="9bf07-190">需求</span><span class="sxs-lookup"><span data-stu-id="9bf07-190">Requirement</span></span> | <span data-ttu-id="9bf07-191">值</span><span class="sxs-lookup"><span data-stu-id="9bf07-191">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9bf07-192">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9bf07-192">Minimum supported client</span></span> | <span data-ttu-id="9bf07-193">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9bf07-193">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="9bf07-194">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9bf07-194">Minimum supported server</span></span> | <span data-ttu-id="9bf07-195">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9bf07-195">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="9bf07-196">標頭</span><span class="sxs-lookup"><span data-stu-id="9bf07-196">Header</span></span>                   | <span data-ttu-id="9bf07-197">d2d1effects。h</span><span class="sxs-lookup"><span data-stu-id="9bf07-197">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="9bf07-198">程式庫</span><span class="sxs-lookup"><span data-stu-id="9bf07-198">Library</span></span>                  | <span data-ttu-id="9bf07-199">d2d1 .lib，dxguid .lib</span><span class="sxs-lookup"><span data-stu-id="9bf07-199">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="9bf07-200">相關主題</span><span class="sxs-lookup"><span data-stu-id="9bf07-200">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9bf07-201">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="9bf07-201">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

