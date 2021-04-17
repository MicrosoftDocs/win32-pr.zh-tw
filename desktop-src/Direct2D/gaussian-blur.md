---
title: 高斯模糊效果
description: 使用高斯模糊效果，根據整個輸入影像上的高斯函數來建立模糊。
ms.assetid: 6B8C9A0A-81D6-4CC2-B30B-995D4C2E59FC
keywords:
- 高斯模糊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfbe8b309a498315e389be45d382eca3ee1b98ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104563738"
---
# <a name="gaussian-blur-effect"></a><span data-ttu-id="93f8a-104">高斯模糊效果</span><span class="sxs-lookup"><span data-stu-id="93f8a-104">Gaussian blur effect</span></span>

<span data-ttu-id="93f8a-105">使用高斯模糊效果，根據整個輸入影像上的高斯函數來建立模糊。</span><span class="sxs-lookup"><span data-stu-id="93f8a-105">Use the Gaussian blur effect to create a blur based on the Gaussian function over the entire input image.</span></span>

<span data-ttu-id="93f8a-106">您可以使用此效果來建立發光和陰影，並使用 [複合](composite.md) 效果將結果套用至原始影像。</span><span class="sxs-lookup"><span data-stu-id="93f8a-106">You can use this effect to create glows and drop shadows and use the [composite](composite.md) effect to apply the result to the original image.</span></span> <span data-ttu-id="93f8a-107">它在相片處理時很有用，例如反白顯示和陰影等篩選。</span><span class="sxs-lookup"><span data-stu-id="93f8a-107">It is useful in photo processing for filters like highlights and shadows.</span></span> <span data-ttu-id="93f8a-108">您可以使用此效果的輸出來輸入光源效果，例如 [反射光源](specular-lighting.md) 或 [擴散光源](diffuse-lighting.md) 效果，因為 Alpha 色板的亮度很模糊，而光源則使用 Alpha 色板來判斷 surface 幾何是否為高度地圖。</span><span class="sxs-lookup"><span data-stu-id="93f8a-108">You can use the output of this effect for input into lighting effects, like the [Specular Lighting](specular-lighting.md) or [Diffuse Lighting](diffuse-lighting.md) effects, because the alpha channel is blurred, too and lighting effects use the alpha channel to determine surface geometry as a height map.</span></span>

<span data-ttu-id="93f8a-109">內建 [陰影](drop-shadow.md) 效果會使用此效果。</span><span class="sxs-lookup"><span data-stu-id="93f8a-109">This effect is used by the built-in [Shadow](drop-shadow.md) effect.</span></span>

<span data-ttu-id="93f8a-110">這項效果的 CLSID 是 CLSID \_ D2D1GaussianBlur。</span><span class="sxs-lookup"><span data-stu-id="93f8a-110">The CLSID for this effect is CLSID\_D2D1GaussianBlur.</span></span>

-   [<span data-ttu-id="93f8a-111">範例影像</span><span class="sxs-lookup"><span data-stu-id="93f8a-111">Example image</span></span>](#example-image)
-   [<span data-ttu-id="93f8a-112">效果屬性</span><span class="sxs-lookup"><span data-stu-id="93f8a-112">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="93f8a-113">優化模式</span><span class="sxs-lookup"><span data-stu-id="93f8a-113">Optimization modes</span></span>](#optimization-modes)
-   [<span data-ttu-id="93f8a-114">框線模式</span><span class="sxs-lookup"><span data-stu-id="93f8a-114">Border modes</span></span>](#border-modes)
-   [<span data-ttu-id="93f8a-115">輸出點陣圖</span><span class="sxs-lookup"><span data-stu-id="93f8a-115">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="93f8a-116">需求</span><span class="sxs-lookup"><span data-stu-id="93f8a-116">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="93f8a-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="93f8a-117">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="93f8a-118">範例影像</span><span class="sxs-lookup"><span data-stu-id="93f8a-118">Example image</span></span>



| <span data-ttu-id="93f8a-119">之前</span><span class="sxs-lookup"><span data-stu-id="93f8a-119">Before</span></span>                                                       |
|--------------------------------------------------------------|
| ![效果之前的影像。](images/default-before.jpg)   |
| <span data-ttu-id="93f8a-121">After</span><span class="sxs-lookup"><span data-stu-id="93f8a-121">After</span></span>                                                        |
| ![轉換後的影像。](images/1-gaussianblur.png) |



 


```C++
ComPtr<ID2D1Effect> gaussianBlurEffect;
m_d2dContext->CreateEffect(CLSID_D2D1GaussianBlur, &gaussianBlurEffect);

gaussianBlurEffect->SetInput(0, bitmap);
gaussianBlurEffect->SetValue(D2D1_GAUSSIANBLUR_PROP_STANDARD_DEVIATION, 3.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(gaussianBlurEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="93f8a-123">效果屬性</span><span class="sxs-lookup"><span data-stu-id="93f8a-123">Effect properties</span></span>



| <span data-ttu-id="93f8a-124">顯示名稱和索引列舉</span><span class="sxs-lookup"><span data-stu-id="93f8a-124">Display name and index enumeration</span></span>                                                    | <span data-ttu-id="93f8a-125">Description</span><span class="sxs-lookup"><span data-stu-id="93f8a-125">Description</span></span>                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93f8a-126">StandardDeviation</span><span class="sxs-lookup"><span data-stu-id="93f8a-126">StandardDeviation</span></span><br/> <span data-ttu-id="93f8a-127">D2D1 \_ GAUSSIANBLUR \_ 的 \_ 標準 \_ 偏差</span><span class="sxs-lookup"><span data-stu-id="93f8a-127">D2D1\_GAUSSIANBLUR\_PROP\_STANDARD\_DEVIATION</span></span><br/> | <span data-ttu-id="93f8a-128">要套用到影像的模糊量。</span><span class="sxs-lookup"><span data-stu-id="93f8a-128">The amount of blur to be applied to the image.</span></span> <span data-ttu-id="93f8a-129">您可以藉由將標準差乘以3來計算核心的模糊半徑。</span><span class="sxs-lookup"><span data-stu-id="93f8a-129">You can compute the blur radius of the kernel by multiplying the standard deviation by 3.</span></span> <span data-ttu-id="93f8a-130">標準差和模糊半徑的單位為 Dip。</span><span class="sxs-lookup"><span data-stu-id="93f8a-130">The units of both the standard deviation and blur radius are DIPs.</span></span> <span data-ttu-id="93f8a-131">如果值為零，則會完全停用此效果。</span><span class="sxs-lookup"><span data-stu-id="93f8a-131">A value of zero DIPs disables this effect entirely.</span></span> <span data-ttu-id="93f8a-132">此類型為 FLOAT。</span><span class="sxs-lookup"><span data-stu-id="93f8a-132">The type is FLOAT.</span></span><br/> <span data-ttu-id="93f8a-133">預設值為 3.0 f。</span><span class="sxs-lookup"><span data-stu-id="93f8a-133">The default value is 3.0f.</span></span><br/> |
| <span data-ttu-id="93f8a-134">Optimization</span><span class="sxs-lookup"><span data-stu-id="93f8a-134">Optimization</span></span><br/> <span data-ttu-id="93f8a-135">D2D1 \_ GAUSSIANBLUR \_ 的 \_ 優化</span><span class="sxs-lookup"><span data-stu-id="93f8a-135">D2D1\_GAUSSIANBLUR\_PROP\_OPTIMIZATION</span></span><br/>             | <span data-ttu-id="93f8a-136">優化模式。</span><span class="sxs-lookup"><span data-stu-id="93f8a-136">The optimization mode.</span></span> <span data-ttu-id="93f8a-137">如需詳細資訊，請參閱 [優化模式](#optimization-modes) 。</span><span class="sxs-lookup"><span data-stu-id="93f8a-137">See [Optimization modes](#optimization-modes) for more info.</span></span> <span data-ttu-id="93f8a-138">此類型為 D2D1 \_ GAUSSIANBLUR \_ 優化。</span><span class="sxs-lookup"><span data-stu-id="93f8a-138">The type is D2D1\_GAUSSIANBLUR\_OPTIMIZATION.</span></span><br/> <span data-ttu-id="93f8a-139">預設值為 D2D1 \_ GAUSSIANBLUR \_ 優化 \_ 平衡。</span><span class="sxs-lookup"><span data-stu-id="93f8a-139">The default value is D2D1\_GAUSSIANBLUR\_OPTIMIZATION\_BALANCED.</span></span><br/>                                                                                                            |
| <span data-ttu-id="93f8a-140">BorderMode</span><span class="sxs-lookup"><span data-stu-id="93f8a-140">BorderMode</span></span><br/> <span data-ttu-id="93f8a-141">D2D1 \_ GAUSSIANBLUR \_ 的 \_ 樣式框線 \_ 模式</span><span class="sxs-lookup"><span data-stu-id="93f8a-141">D2D1\_GAUSSIANBLUR\_PROP\_BORDER\_MODE</span></span><br/>               | <span data-ttu-id="93f8a-142">用來計算影像（軟或硬）框線的模式。</span><span class="sxs-lookup"><span data-stu-id="93f8a-142">The mode used to calculate the border of the image, soft or hard.</span></span> <span data-ttu-id="93f8a-143">如需詳細資訊，請參閱 [框線模式](#border-modes) 。</span><span class="sxs-lookup"><span data-stu-id="93f8a-143">See [Border modes](#border-modes) for more info.</span></span> <br/> <span data-ttu-id="93f8a-144">此類型為 D2D1 \_ GAUSSIANBLUR \_ BORDER \_ 模式。</span><span class="sxs-lookup"><span data-stu-id="93f8a-144">The type is D2D1\_GAUSSIANBLUR\_BORDER\_MODE.</span></span><br/> <span data-ttu-id="93f8a-145">預設值為 [D2D1 \_ 框線 \_ 模式] \_ 。</span><span class="sxs-lookup"><span data-stu-id="93f8a-145">The default value is D2D1\_BORDER\_MODE\_SOFT.</span></span><br/>                                                                                   |



 

## <a name="optimization-modes"></a><span data-ttu-id="93f8a-146">優化模式</span><span class="sxs-lookup"><span data-stu-id="93f8a-146">Optimization modes</span></span>



| <span data-ttu-id="93f8a-147">Name</span><span class="sxs-lookup"><span data-stu-id="93f8a-147">Name</span></span>                                          | <span data-ttu-id="93f8a-148">描述</span><span class="sxs-lookup"><span data-stu-id="93f8a-148">Description</span></span>                                                                                                                           |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93f8a-149">D2D1 \_ DIRECTIONALBLUR \_ 優化 \_ 速度</span><span class="sxs-lookup"><span data-stu-id="93f8a-149">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_SPEED</span></span>    | <span data-ttu-id="93f8a-150">套用內部優化，例如在相對較小半徑上進行預先調整。</span><span class="sxs-lookup"><span data-stu-id="93f8a-150">Applies internal optimizations such as pre-scaling at relatively small radii.</span></span> <span data-ttu-id="93f8a-151">使用線性篩選。</span><span class="sxs-lookup"><span data-stu-id="93f8a-151">Uses linear filtering.</span></span>                                  |
| <span data-ttu-id="93f8a-152">D2D1 \_ DIRECTIONALBLUR \_ 優化 \_ 平衡</span><span class="sxs-lookup"><span data-stu-id="93f8a-152">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_BALANCED</span></span> | <span data-ttu-id="93f8a-153">使用與速度模式相同的優化臨界值，但使用三線性篩選。</span><span class="sxs-lookup"><span data-stu-id="93f8a-153">Uses the same optimization thresholds as Speed mode, but uses trilinear filtering.</span></span>                                                    |
| <span data-ttu-id="93f8a-154">D2D1 \_ DIRECTIONALBLUR \_ 優化 \_ 品質</span><span class="sxs-lookup"><span data-stu-id="93f8a-154">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_QUALITY</span></span>  | <span data-ttu-id="93f8a-155">只會使用具有大型模糊半徑的內部優化，其中近似值較不可能可見。</span><span class="sxs-lookup"><span data-stu-id="93f8a-155">Only uses internal optimizations with large blur radii, where approximations are less likely to be visible.</span></span> <span data-ttu-id="93f8a-156">使用三線性篩選。</span><span class="sxs-lookup"><span data-stu-id="93f8a-156">Uses trilinear filtering.</span></span> |



 

## <a name="border-modes"></a><span data-ttu-id="93f8a-157">框線模式</span><span class="sxs-lookup"><span data-stu-id="93f8a-157">Border modes</span></span>



| <span data-ttu-id="93f8a-158">Name</span><span class="sxs-lookup"><span data-stu-id="93f8a-158">Name</span></span>                     | <span data-ttu-id="93f8a-159">描述</span><span class="sxs-lookup"><span data-stu-id="93f8a-159">Description</span></span>                                                                                                                                                                                                              |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93f8a-160">D2D1 \_ 框線 \_ 模式 \_ 軟</span><span class="sxs-lookup"><span data-stu-id="93f8a-160">D2D1\_BORDER\_MODE\_SOFT</span></span> | <span data-ttu-id="93f8a-161">效果會對影像進行透明黑色圖元，因為它會套用模糊核心，以產生軟邊緣。</span><span class="sxs-lookup"><span data-stu-id="93f8a-161">The effect pads the image with transparent black pixels as it applies the blur kernel, resulting in a soft edge.</span></span> <br/>                                                                                             |
| <span data-ttu-id="93f8a-162">D2D1 \_ 框線 \_ 模式 \_ 硬性</span><span class="sxs-lookup"><span data-stu-id="93f8a-162">D2D1\_BORDER\_MODE\_HARD</span></span> | <span data-ttu-id="93f8a-163">效果會將輸出個至輸入影像的大小。</span><span class="sxs-lookup"><span data-stu-id="93f8a-163">The effect clamps the output to the size of the input image.</span></span> <span data-ttu-id="93f8a-164">當效果套用模糊核心時，它會針對輸入界限外的樣本，以鏡像類型的框線轉換來擴充輸入影像。</span><span class="sxs-lookup"><span data-stu-id="93f8a-164">When the effect applies the blur kernel, it extends the input image with a mirror-type border transform for samples outside of the input bounds.</span></span><br/> |



 

## <a name="output-bitmap"></a><span data-ttu-id="93f8a-165">輸出點陣圖</span><span class="sxs-lookup"><span data-stu-id="93f8a-165">Output bitmap</span></span>

<span data-ttu-id="93f8a-166">此效果的輸出可能會比輸入點陣圖（以模糊半徑和框線模式為基礎）大。</span><span class="sxs-lookup"><span data-stu-id="93f8a-166">The output of this effect can be larger than the input bitmap based on the blur radius and the border mode.</span></span> <span data-ttu-id="93f8a-167">如果框線模式設定為 D2D1 \_ 框線模式， \_ 則 \_ 輸出點陣圖的 s 大小會隨著模糊核心的大小增加（以圖元表示）。</span><span class="sxs-lookup"><span data-stu-id="93f8a-167">If the border mode is set to D2D1\_BORDER\_MODE\_SOFT the s ize of the output bitmap increases by the size of the blur kernel, represented in pixels.</span></span> <span data-ttu-id="93f8a-168">下表提供您可以用來計算輸出點陣圖的方程式。</span><span class="sxs-lookup"><span data-stu-id="93f8a-168">This table provides an equation that you can use to compute the output bitmap.</span></span>

`Output bitmap growth (X and Y) = StandardDeviation  (DIPs)*6*((User DPI)/96)`

<span data-ttu-id="93f8a-169">因此，如果影像大小在每個方向增加10個圖元，則影像的左上角將會位於 (-5、-5) ，而右下角會是 (105，105) 。</span><span class="sxs-lookup"><span data-stu-id="93f8a-169">So, if the image size increases by 10 pixels in each direction the upper left corner of the image will be located at (-5, -5) while the lower right will be at (105, 105).</span></span>

## <a name="requirements"></a><span data-ttu-id="93f8a-170">規格需求</span><span class="sxs-lookup"><span data-stu-id="93f8a-170">Requirements</span></span>



| <span data-ttu-id="93f8a-171">需求</span><span class="sxs-lookup"><span data-stu-id="93f8a-171">Requirement</span></span> | <span data-ttu-id="93f8a-172">值</span><span class="sxs-lookup"><span data-stu-id="93f8a-172">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="93f8a-173">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="93f8a-173">Minimum supported client</span></span> | <span data-ttu-id="93f8a-174">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="93f8a-174">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="93f8a-175">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="93f8a-175">Minimum supported server</span></span> | <span data-ttu-id="93f8a-176">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="93f8a-176">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="93f8a-177">標頭</span><span class="sxs-lookup"><span data-stu-id="93f8a-177">Header</span></span>                   | <span data-ttu-id="93f8a-178">d2d1effects。h</span><span class="sxs-lookup"><span data-stu-id="93f8a-178">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="93f8a-179">程式庫</span><span class="sxs-lookup"><span data-stu-id="93f8a-179">Library</span></span>                  | <span data-ttu-id="93f8a-180">d2d1 .lib，dxguid .lib</span><span class="sxs-lookup"><span data-stu-id="93f8a-180">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="93f8a-181">相關主題</span><span class="sxs-lookup"><span data-stu-id="93f8a-181">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93f8a-182">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="93f8a-182">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

