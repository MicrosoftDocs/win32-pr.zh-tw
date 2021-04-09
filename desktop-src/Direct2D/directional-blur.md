---
title: 方向模糊效果
description: 方向模糊效果與高斯模糊類似，不同之處在于您可以在特定方向扭曲模糊。
ms.assetid: 59328FA4-5C27-4A81-AAB2-C5B25B3615C6
keywords:
- 方向模糊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0e1c098d17929563cf69f4e61416fa0d93a88dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685496"
---
# <a name="directional-blur-effect"></a><span data-ttu-id="0fa27-104">方向模糊效果</span><span class="sxs-lookup"><span data-stu-id="0fa27-104">Directional blur effect</span></span>

<span data-ttu-id="0fa27-105">方向模糊效果與 [高斯模糊](gaussian-blur.md)類似，不同之處在于您可以在特定方向扭曲模糊。</span><span class="sxs-lookup"><span data-stu-id="0fa27-105">The directional blur effect is similar to [Gaussian blur](gaussian-blur.md), except you can skew the blur in a particular direction.</span></span> <span data-ttu-id="0fa27-106">您可以使用此效果，讓影像看起來像是移動中或強調動畫影像。</span><span class="sxs-lookup"><span data-stu-id="0fa27-106">You can use this effect to make an image look as if it is in motion or to emphasize an animated image.</span></span>

<span data-ttu-id="0fa27-107">這項效果的 CLSID 是 CLSID \_ D2D1DirectionalBlur。</span><span class="sxs-lookup"><span data-stu-id="0fa27-107">The CLSID for this effect is CLSID\_D2D1DirectionalBlur.</span></span>

-   [<span data-ttu-id="0fa27-108">範例影像</span><span class="sxs-lookup"><span data-stu-id="0fa27-108">Example image</span></span>](#example-image)
-   [<span data-ttu-id="0fa27-109">效果屬性</span><span class="sxs-lookup"><span data-stu-id="0fa27-109">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="0fa27-110">優化模式</span><span class="sxs-lookup"><span data-stu-id="0fa27-110">Optimization modes</span></span>](#optimization-modes)
-   [<span data-ttu-id="0fa27-111">框線模式</span><span class="sxs-lookup"><span data-stu-id="0fa27-111">Border modes</span></span>](#border-modes)
-   [<span data-ttu-id="0fa27-112">輸出點陣圖</span><span class="sxs-lookup"><span data-stu-id="0fa27-112">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="0fa27-113">需求</span><span class="sxs-lookup"><span data-stu-id="0fa27-113">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="0fa27-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="0fa27-114">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="0fa27-115">範例影像</span><span class="sxs-lookup"><span data-stu-id="0fa27-115">Example image</span></span>



| <span data-ttu-id="0fa27-116">之前</span><span class="sxs-lookup"><span data-stu-id="0fa27-116">Before</span></span>                                                          |
|-----------------------------------------------------------------|
| ![效果之前的影像。](images/default-before.jpg)      |
| <span data-ttu-id="0fa27-118">After</span><span class="sxs-lookup"><span data-stu-id="0fa27-118">After</span></span>                                                           |
| ![轉換後的影像。](images/2-directionalblur.png) |



 


```C++
ComPtr<ID2D1Effect> directionalBlurEffect;
m_d2dContext->CreateEffect(CLSID_D2D1DirectionalBlur, &directionalBlurEffect);

directionalBlurEffect->SetInput(0, bitmap);
directionalBlurEffect->SetValue(D2D1_DIRECTIONALBLUR_PROP_STANDARD_DEVIATION, 7.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(directionalBlurEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="0fa27-120">效果屬性</span><span class="sxs-lookup"><span data-stu-id="0fa27-120">Effect properties</span></span>



| <span data-ttu-id="0fa27-121">顯示名稱和索引列舉</span><span class="sxs-lookup"><span data-stu-id="0fa27-121">Display name and index enumeration</span></span>                                                       | <span data-ttu-id="0fa27-122">Description</span><span class="sxs-lookup"><span data-stu-id="0fa27-122">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fa27-123">StandardDeviation</span><span class="sxs-lookup"><span data-stu-id="0fa27-123">StandardDeviation</span></span><br/> <span data-ttu-id="0fa27-124">D2D1 \_ DIRECTIONALBLUR \_ 的 \_ 標準 \_ 偏差</span><span class="sxs-lookup"><span data-stu-id="0fa27-124">D2D1\_DIRECTIONALBLUR\_PROP\_STANDARD\_DEVIATION</span></span><br/> | <span data-ttu-id="0fa27-125">要套用到影像的模糊量。</span><span class="sxs-lookup"><span data-stu-id="0fa27-125">The amount of blur to be applied to the image.</span></span> <span data-ttu-id="0fa27-126">您可以藉由將標準差乘以3來計算核心的模糊半徑。</span><span class="sxs-lookup"><span data-stu-id="0fa27-126">You can compute the blur radius of the kernel by multiplying the standard deviation by 3.</span></span> <span data-ttu-id="0fa27-127">標準差和模糊半徑的單位為 Dip。</span><span class="sxs-lookup"><span data-stu-id="0fa27-127">The units of both the standard deviation and blur radius are DIPs.</span></span> <span data-ttu-id="0fa27-128">值為 0 Dip 會停用此效果。</span><span class="sxs-lookup"><span data-stu-id="0fa27-128">A value of 0 DIPs disables this effect.</span></span> <span data-ttu-id="0fa27-129">此類型為 FLOAT。</span><span class="sxs-lookup"><span data-stu-id="0fa27-129">The type is FLOAT.</span></span><br/> <span data-ttu-id="0fa27-130">預設值為 3.0 f。</span><span class="sxs-lookup"><span data-stu-id="0fa27-130">The default value is 3.0f.</span></span><br/>                                                                            |
| <span data-ttu-id="0fa27-131">角度</span><span class="sxs-lookup"><span data-stu-id="0fa27-131">Angle</span></span><br/> <span data-ttu-id="0fa27-132">D2D1 \_ DIRECTIONALBLUR \_ 的 \_ 角度</span><span class="sxs-lookup"><span data-stu-id="0fa27-132">D2D1\_DIRECTIONALBLUR\_PROP\_ANGLE</span></span><br/>                           | <span data-ttu-id="0fa27-133">相對於 X 軸之模糊的角度（以逆時針方向）。</span><span class="sxs-lookup"><span data-stu-id="0fa27-133">The angle of the blur relative to the x-axis, in the counterclockwise direction.</span></span> <span data-ttu-id="0fa27-134">單位是以度為單位來指定。</span><span class="sxs-lookup"><span data-stu-id="0fa27-134">The units are specified in degrees.</span></span><br/> <span data-ttu-id="0fa27-135">模糊核心會先使用與 [高斯模糊](gaussian-blur.md) 效果相同的進程產生。</span><span class="sxs-lookup"><span data-stu-id="0fa27-135">The blur kernel is first generated using the same process as for the [Gaussian blur](gaussian-blur.md) effect.</span></span> <span data-ttu-id="0fa27-136">核心值接著會根據模糊角度進行轉換。</span><span class="sxs-lookup"><span data-stu-id="0fa27-136">The kernel values are then transformed according to the blur angle.</span></span><br/> <span data-ttu-id="0fa27-137">此類型為 FLOAT。</span><span class="sxs-lookup"><span data-stu-id="0fa27-137">The type is FLOAT.</span></span><br/> <span data-ttu-id="0fa27-138">預設值為 0.0 f。</span><span class="sxs-lookup"><span data-stu-id="0fa27-138">The default value is 0.0f.</span></span><br/> |
| <span data-ttu-id="0fa27-139">Optimization</span><span class="sxs-lookup"><span data-stu-id="0fa27-139">Optimization</span></span><br/> <span data-ttu-id="0fa27-140">D2D1 \_ DIRECTIONALBLUR \_ 的 \_ 優化</span><span class="sxs-lookup"><span data-stu-id="0fa27-140">D2D1\_DIRECTIONALBLUR\_PROP\_OPTIMIZATION</span></span><br/>             | <span data-ttu-id="0fa27-141">優化模式。</span><span class="sxs-lookup"><span data-stu-id="0fa27-141">The optimization mode.</span></span> <span data-ttu-id="0fa27-142">如需詳細資訊，請參閱 [優化模式](#optimization-modes) 。</span><span class="sxs-lookup"><span data-stu-id="0fa27-142">See [Optimization modes](#optimization-modes) for more info.</span></span><br/> <span data-ttu-id="0fa27-143">此類型為 D2D1 \_ DIRECTIONALBLUR \_ 優化。</span><span class="sxs-lookup"><span data-stu-id="0fa27-143">The type is D2D1\_DIRECTIONALBLUR\_OPTIMIZATION.</span></span><br/> <span data-ttu-id="0fa27-144">預設值為 D2D1 \_ DIRECTIONALBLUR \_ 優化 \_ 平衡。</span><span class="sxs-lookup"><span data-stu-id="0fa27-144">The default value is D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_BALANCED.</span></span> <br/>                                                                                                                                                         |
| <span data-ttu-id="0fa27-145">BorderMode</span><span class="sxs-lookup"><span data-stu-id="0fa27-145">BorderMode</span></span><br/> <span data-ttu-id="0fa27-146">D2D1 \_ DIRECTIONALBLUR \_ 的 \_ 樣式框線 \_ 模式</span><span class="sxs-lookup"><span data-stu-id="0fa27-146">D2D1\_DIRECTIONALBLUR\_PROP\_BORDER\_MODE</span></span><br/>               | <span data-ttu-id="0fa27-147">用來計算影像（軟或硬）框線的模式。</span><span class="sxs-lookup"><span data-stu-id="0fa27-147">The mode used to calculate the border of the image, soft or hard.</span></span> <span data-ttu-id="0fa27-148">如需詳細資訊，請參閱 [框線模式](#border-modes) 。</span><span class="sxs-lookup"><span data-stu-id="0fa27-148">See [Border modes](#border-modes) for more info.</span></span><br/> <span data-ttu-id="0fa27-149">此類型為 D2D1 \_ 框線 \_ 模式。</span><span class="sxs-lookup"><span data-stu-id="0fa27-149">The type is D2D1\_BORDER\_MODE.</span></span><br/> <span data-ttu-id="0fa27-150">預設值為 [D2D1 \_ 框線 \_ 模式] \_ 。</span><span class="sxs-lookup"><span data-stu-id="0fa27-150">The default value is D2D1\_BORDER\_MODE\_SOFT.</span></span><br/>                                                                                                                                                                 |



 

## <a name="optimization-modes"></a><span data-ttu-id="0fa27-151">優化模式</span><span class="sxs-lookup"><span data-stu-id="0fa27-151">Optimization modes</span></span>



| <span data-ttu-id="0fa27-152">Name</span><span class="sxs-lookup"><span data-stu-id="0fa27-152">Name</span></span>                                          | <span data-ttu-id="0fa27-153">描述</span><span class="sxs-lookup"><span data-stu-id="0fa27-153">Description</span></span>                                                                                                                           |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fa27-154">D2D1 \_ DIRECTIONALBLUR \_ 優化 \_ 速度</span><span class="sxs-lookup"><span data-stu-id="0fa27-154">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_SPEED</span></span>    | <span data-ttu-id="0fa27-155">套用內部優化，例如在相對較小半徑上進行預先調整。</span><span class="sxs-lookup"><span data-stu-id="0fa27-155">Applies internal optimizations such as pre-scaling at relatively small radii.</span></span> <span data-ttu-id="0fa27-156">使用線性篩選。</span><span class="sxs-lookup"><span data-stu-id="0fa27-156">Uses linear filtering.</span></span>                                  |
| <span data-ttu-id="0fa27-157">D2D1 \_ DIRECTIONALBLUR \_ 優化 \_ 平衡</span><span class="sxs-lookup"><span data-stu-id="0fa27-157">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_BALANCED</span></span> | <span data-ttu-id="0fa27-158">使用與速度模式相同的優化臨界值，但使用三線性篩選。</span><span class="sxs-lookup"><span data-stu-id="0fa27-158">Uses the same optimization thresholds as Speed mode, but uses trilinear filtering.</span></span>                                                    |
| <span data-ttu-id="0fa27-159">D2D1 \_ DIRECTIONALBLUR \_ 優化 \_ 品質</span><span class="sxs-lookup"><span data-stu-id="0fa27-159">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_QUALITY</span></span>  | <span data-ttu-id="0fa27-160">只會使用具有大型模糊半徑的內部優化，其中近似值較不可能可見。</span><span class="sxs-lookup"><span data-stu-id="0fa27-160">Only uses internal optimizations with large blur radii, where approximations are less likely to be visible.</span></span> <span data-ttu-id="0fa27-161">使用三線性篩選。</span><span class="sxs-lookup"><span data-stu-id="0fa27-161">Uses trilinear filtering.</span></span> |



 

## <a name="border-modes"></a><span data-ttu-id="0fa27-162">框線模式</span><span class="sxs-lookup"><span data-stu-id="0fa27-162">Border modes</span></span>



| <span data-ttu-id="0fa27-163">Name</span><span class="sxs-lookup"><span data-stu-id="0fa27-163">Name</span></span>                     | <span data-ttu-id="0fa27-164">描述</span><span class="sxs-lookup"><span data-stu-id="0fa27-164">Description</span></span>                                                                                                                                                                                                              |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fa27-165">D2D1 \_ 框線 \_ 模式 \_ 軟</span><span class="sxs-lookup"><span data-stu-id="0fa27-165">D2D1\_BORDER\_MODE\_SOFT</span></span> | <span data-ttu-id="0fa27-166">效果會對影像進行透明黑色圖元，因為它會套用模糊核心，以產生軟邊緣。</span><span class="sxs-lookup"><span data-stu-id="0fa27-166">The effect pads the image with transparent black pixels as it applies the blur kernel, resulting in a soft edge.</span></span> <br/>                                                                                             |
| <span data-ttu-id="0fa27-167">D2D1 \_ 框線 \_ 模式 \_ 硬性</span><span class="sxs-lookup"><span data-stu-id="0fa27-167">D2D1\_BORDER\_MODE\_HARD</span></span> | <span data-ttu-id="0fa27-168">效果會將輸出個至輸入影像的大小。</span><span class="sxs-lookup"><span data-stu-id="0fa27-168">The effect clamps the output to the size of the input image.</span></span> <span data-ttu-id="0fa27-169">當效果套用模糊核心時，它會針對輸入界限外的樣本，以鏡像類型的框線轉換來擴充輸入影像。</span><span class="sxs-lookup"><span data-stu-id="0fa27-169">When the effect applies the blur kernel, it extends the input image with a mirror-type border transform for samples outside of the input bounds.</span></span><br/> |



 

## <a name="output-bitmap"></a><span data-ttu-id="0fa27-170">輸出點陣圖</span><span class="sxs-lookup"><span data-stu-id="0fa27-170">Output bitmap</span></span>

<span data-ttu-id="0fa27-171">輸出點陣圖的大小會根據標準差、效果的角度和框線模式而增加。</span><span class="sxs-lookup"><span data-stu-id="0fa27-171">The size of the output bitmap increases based on the standard deviation, the angle of the effect, and the border mode.</span></span> <span data-ttu-id="0fa27-172">如果框線模式設定為 D2D1 \_ 框線 \_ 模式，則 \_ 輸出點陣圖的大小會隨著模糊核心的大小增加（以圖元表示）。</span><span class="sxs-lookup"><span data-stu-id="0fa27-172">If the border mode is set to D2D1\_BORDER\_MODE\_SOFT the size of the output bitmap increases by the size of the blur kernel, represented in pixels.</span></span> <span data-ttu-id="0fa27-173">您可以使用這些方程式來計算輸出點陣圖的大小。</span><span class="sxs-lookup"><span data-stu-id="0fa27-173">These equations can be used to calculate the size of the output bitmap.</span></span>



| <span data-ttu-id="0fa27-174">需求</span><span class="sxs-lookup"><span data-stu-id="0fa27-174">Requirement</span></span> | <span data-ttu-id="0fa27-175">值</span><span class="sxs-lookup"><span data-stu-id="0fa27-175">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="0fa27-176">輸出點陣圖成長 X</span><span class="sxs-lookup"><span data-stu-id="0fa27-176">Output Bitmap Growth X</span></span> | <span data-ttu-id="0fa27-177">List.standarddeviation (Dip) \* 6 \* ( (使用者 DPI) /96) \* cos (角度) ) </span><span class="sxs-lookup"><span data-stu-id="0fa27-177">StandardDeviation (DIPs) \* 6 \* ((User DPI) / 96) \* cos(Angle))</span></span> |
| <span data-ttu-id="0fa27-178">輸出點陣圖成長 Y</span><span class="sxs-lookup"><span data-stu-id="0fa27-178">Output Bitmap Growth Y</span></span> | <span data-ttu-id="0fa27-179">List.standarddeviation (Dip) \* 6 \* ( (使用者 DPI) /96) \* Angle (角度) ) </span><span class="sxs-lookup"><span data-stu-id="0fa27-179">StandardDeviation (DIPs) \* 6 \* ((User DPI) / 96) \* sin(Angle))</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="0fa27-180">規格需求</span><span class="sxs-lookup"><span data-stu-id="0fa27-180">Requirements</span></span>



| <span data-ttu-id="0fa27-181">需求</span><span class="sxs-lookup"><span data-stu-id="0fa27-181">Requirement</span></span> | <span data-ttu-id="0fa27-182">值</span><span class="sxs-lookup"><span data-stu-id="0fa27-182">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0fa27-183">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0fa27-183">Minimum supported client</span></span> | <span data-ttu-id="0fa27-184">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0fa27-184">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="0fa27-185">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0fa27-185">Minimum supported server</span></span> | <span data-ttu-id="0fa27-186">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0fa27-186">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="0fa27-187">標頭</span><span class="sxs-lookup"><span data-stu-id="0fa27-187">Header</span></span>                   | <span data-ttu-id="0fa27-188">d2d1effects。h</span><span class="sxs-lookup"><span data-stu-id="0fa27-188">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="0fa27-189">程式庫</span><span class="sxs-lookup"><span data-stu-id="0fa27-189">Library</span></span>                  | <span data-ttu-id="0fa27-190">d2d1 .lib，dxguid .lib</span><span class="sxs-lookup"><span data-stu-id="0fa27-190">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="0fa27-191">相關主題</span><span class="sxs-lookup"><span data-stu-id="0fa27-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0fa27-192">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="0fa27-192">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

