---
title: 陰影效果
description: 使用陰影效果，從影像的 Alpha 通道產生陰影。
ms.assetid: 53525584-10CF-46C2-9400-C4FB225D4693
keywords:
- 陰影效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c42fd8755078dd79f2b01b623b1839785beb3c3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317140"
---
# <a name="shadow-effect"></a><span data-ttu-id="1aefe-104">陰影效果</span><span class="sxs-lookup"><span data-stu-id="1aefe-104">Shadow effect</span></span>

<span data-ttu-id="1aefe-105">使用陰影效果，從影像的 Alpha 通道產生陰影。</span><span class="sxs-lookup"><span data-stu-id="1aefe-105">Use the shadow effect to generate a shadow from the alpha channel of an image.</span></span> <span data-ttu-id="1aefe-106">針對較高的 Alpha 值，陰影較不透明，較低的 Alpha 值則更透明。</span><span class="sxs-lookup"><span data-stu-id="1aefe-106">The shadow is more opaque for higher alpha values and more transparent for lower alpha values.</span></span> <span data-ttu-id="1aefe-107">您可以設定模糊的數量和陰影的色彩。</span><span class="sxs-lookup"><span data-stu-id="1aefe-107">You can set the amount of blur and the color of the shadow.</span></span>

-   [<span data-ttu-id="1aefe-108">範例影像</span><span class="sxs-lookup"><span data-stu-id="1aefe-108">Example image</span></span>](#example-image)
-   [<span data-ttu-id="1aefe-109">效果屬性</span><span class="sxs-lookup"><span data-stu-id="1aefe-109">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="1aefe-110">優化模式</span><span class="sxs-lookup"><span data-stu-id="1aefe-110">Optimization modes</span></span>](#optimization-modes)
-   [<span data-ttu-id="1aefe-111">輸出點陣圖</span><span class="sxs-lookup"><span data-stu-id="1aefe-111">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="1aefe-112">需求</span><span class="sxs-lookup"><span data-stu-id="1aefe-112">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="1aefe-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="1aefe-113">Related topics</span></span>](#related-topics)

<span data-ttu-id="1aefe-114">這項效果的 CLSID 是 CLSID \_ D2D1Shadow。</span><span class="sxs-lookup"><span data-stu-id="1aefe-114">The CLSID for this effect is CLSID\_D2D1Shadow.</span></span>

## <a name="example-image"></a><span data-ttu-id="1aefe-115">範例影像</span><span class="sxs-lookup"><span data-stu-id="1aefe-115">Example image</span></span>

<span data-ttu-id="1aefe-116">此處的範例會顯示陰影效果的輸出，其在原始位置中是由其組成的來源影像。</span><span class="sxs-lookup"><span data-stu-id="1aefe-116">The example here shows the output of the shadow effect translated down and right with the source image composited over it in the original location.</span></span> <span data-ttu-id="1aefe-117">陰影效果只會輸出陰影。</span><span class="sxs-lookup"><span data-stu-id="1aefe-117">The shadow effect only outputs the shadow.</span></span>



| <span data-ttu-id="1aefe-118">之前</span><span class="sxs-lookup"><span data-stu-id="1aefe-118">Before</span></span>                                                  |
|---------------------------------------------------------|
| ![效果之前的影像。](images/8-crop.png)      |
| <span data-ttu-id="1aefe-120">After</span><span class="sxs-lookup"><span data-stu-id="1aefe-120">After</span></span>                                                   |
| ![轉換後的影像。](images/25-shadow.png) |



 


```C++
ComPtr<ID2D1Effect> shadowEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Shadow, &shadowEffect);

shadowEffect->SetInput(0, bitmap);

// Shadow is composited on top of a white surface to show opacity.
ComPtr<ID2D1Effect> floodEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Flood, &floodEffect);

floodEffect->SetValue(D2D1_FLOOD_PROP_COLOR, D2D1::Vector4F(1.0f, 1.0f, 1.0f, 1.0f));

ComPtr<ID2D1Effect> affineTransformEffect;
m_d2dContext->CreateEffect(CLSID_D2D12DAffineTransform, &affineTransformEffect);

affineTransformEffect->SetInputEffect(0, shadowEffect.Get());

D2D1_MATRIX_3X2_F matrix = D2D1::Matrix3x2F::Translation(20, 20));

affineTransformEffect->SetValue(D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX, matrix);

ComPtr<ID2D1Effect> compositeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect);

compositeEffect->SetInputEffect(0, floodEffect.Get());
compositeEffect->SetInputEffect(1, affineTransformEffect.Get());
compositeEffect->SetInput(2, bitmap);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="1aefe-122">效果屬性</span><span class="sxs-lookup"><span data-stu-id="1aefe-122">Effect properties</span></span>



| <span data-ttu-id="1aefe-123">顯示名稱和索引列舉</span><span class="sxs-lookup"><span data-stu-id="1aefe-123">Display name and index enumeration</span></span>                                                        | <span data-ttu-id="1aefe-124">Description</span><span class="sxs-lookup"><span data-stu-id="1aefe-124">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1aefe-125">BlurStandardDeviation</span><span class="sxs-lookup"><span data-stu-id="1aefe-125">BlurStandardDeviation</span></span><br/> <span data-ttu-id="1aefe-126">D2D1 \_ 陰影 \_ 樣式 \_ 模糊 \_ 標準 \_ 偏差</span><span class="sxs-lookup"><span data-stu-id="1aefe-126">D2D1\_SHADOW\_PROP\_BLUR\_STANDARD\_DEVIATION</span></span><br/> | <span data-ttu-id="1aefe-127">要套用至影像之 Alpha 通道的模糊數量。</span><span class="sxs-lookup"><span data-stu-id="1aefe-127">The amount of blur to be applied to the alpha channel of the image.</span></span> <span data-ttu-id="1aefe-128">您可以藉由將標準差乘以3來計算核心的模糊半徑。</span><span class="sxs-lookup"><span data-stu-id="1aefe-128">You can compute the blur radius of the kernel by multiplying the standard deviation by 3.</span></span> <span data-ttu-id="1aefe-129">標準差和模糊半徑的單位為 Dip。</span><span class="sxs-lookup"><span data-stu-id="1aefe-129">The units of both the standard deviation and blur radius are DIPs.</span></span><br/> <span data-ttu-id="1aefe-130">這個屬性與 [高斯模糊](gaussian-blur.md) 的標準差屬性相同。</span><span class="sxs-lookup"><span data-stu-id="1aefe-130">This property is the same as the [Gaussian Blur](gaussian-blur.md) standard deviation property.</span></span> <br/> <span data-ttu-id="1aefe-131">此類型為 FLOAT。</span><span class="sxs-lookup"><span data-stu-id="1aefe-131">The type is FLOAT.</span></span><br/> <span data-ttu-id="1aefe-132">預設值為 3.0 f。</span><span class="sxs-lookup"><span data-stu-id="1aefe-132">The default value is 3.0f.</span></span><br/> |
| <span data-ttu-id="1aefe-133">Color</span><span class="sxs-lookup"><span data-stu-id="1aefe-133">Color</span></span><br/> <span data-ttu-id="1aefe-134">D2D1 \_ 陰影 \_ 樣式 \_ 色彩</span><span class="sxs-lookup"><span data-stu-id="1aefe-134">D2D1\_SHADOW\_PROP\_COLOR</span></span><br/>                                     | <span data-ttu-id="1aefe-135">延伸陰影的色彩。</span><span class="sxs-lookup"><span data-stu-id="1aefe-135">The color of the drop shadow.</span></span> <span data-ttu-id="1aefe-136">這個屬性是 D2D1 \_ 向量 \_ 4F，定義為： (R、G、B、) 。</span><span class="sxs-lookup"><span data-stu-id="1aefe-136">This property is a D2D1\_VECTOR\_4F defined as: (R, G, B, A).</span></span> <span data-ttu-id="1aefe-137">您必須以純 Alpha 指定此色彩。</span><span class="sxs-lookup"><span data-stu-id="1aefe-137">You must specify this color in straight alpha.</span></span><br/> <span data-ttu-id="1aefe-138">此類型為 D2D1 \_ VECTOR \_ 4F。</span><span class="sxs-lookup"><span data-stu-id="1aefe-138">The type is D2D1\_VECTOR\_4F.</span></span><br/> <span data-ttu-id="1aefe-139">預設值為 {0.0 f、0.0 f、0.0 f、1.0 f}。</span><span class="sxs-lookup"><span data-stu-id="1aefe-139">The default value is {0.0f, 0.0f, 0.0f, 1.0f}.</span></span><br/>                                                                                                                                                                     |
| <span data-ttu-id="1aefe-140">Optimization</span><span class="sxs-lookup"><span data-stu-id="1aefe-140">Optimization</span></span><br/> <span data-ttu-id="1aefe-141">D2D1 \_ 陰影 \_ 樣式 \_ 優化</span><span class="sxs-lookup"><span data-stu-id="1aefe-141">D2D1\_SHADOW\_PROP\_OPTIMIZATION</span></span><br/>                       | <span data-ttu-id="1aefe-142">效能優化的層級。</span><span class="sxs-lookup"><span data-stu-id="1aefe-142">The level of performance optimization.</span></span><br/> <span data-ttu-id="1aefe-143">此類型為 D2D1 \_ 陰影 \_ 優化。</span><span class="sxs-lookup"><span data-stu-id="1aefe-143">The type is D2D1\_SHADOW\_OPTIMIZATION.</span></span><br/> <span data-ttu-id="1aefe-144">預設值為 D2D1 \_ 陰影 \_ 優化 \_ 平衡。</span><span class="sxs-lookup"><span data-stu-id="1aefe-144">The default value is D2D1\_SHADOW\_OPTIMIZATION\_BALANCED.</span></span><br/>                                                                                                                                                                                                                                                   |



 

## <a name="optimization-modes"></a><span data-ttu-id="1aefe-145">優化模式</span><span class="sxs-lookup"><span data-stu-id="1aefe-145">Optimization modes</span></span>



| <span data-ttu-id="1aefe-146">Name</span><span class="sxs-lookup"><span data-stu-id="1aefe-146">Name</span></span>                                          | <span data-ttu-id="1aefe-147">描述</span><span class="sxs-lookup"><span data-stu-id="1aefe-147">Description</span></span>                                                                                                                           |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1aefe-148">D2D1 \_ DIRECTIONALBLUR \_ 優化 \_ 速度</span><span class="sxs-lookup"><span data-stu-id="1aefe-148">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_SPEED</span></span>    | <span data-ttu-id="1aefe-149">套用內部優化，例如在相對較小半徑上進行預先調整。</span><span class="sxs-lookup"><span data-stu-id="1aefe-149">Applies internal optimizations such as pre-scaling at relatively small radii.</span></span> <span data-ttu-id="1aefe-150">使用線性篩選。</span><span class="sxs-lookup"><span data-stu-id="1aefe-150">Uses linear filtering.</span></span>                                  |
| <span data-ttu-id="1aefe-151">D2D1 \_ DIRECTIONALBLUR \_ 優化 \_ 平衡</span><span class="sxs-lookup"><span data-stu-id="1aefe-151">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_BALANCED</span></span> | <span data-ttu-id="1aefe-152">使用與速度模式相同的優化臨界值，但使用三線性篩選。</span><span class="sxs-lookup"><span data-stu-id="1aefe-152">Uses the same optimization thresholds as Speed mode, but uses trilinear filtering.</span></span>                                                    |
| <span data-ttu-id="1aefe-153">D2D1 \_ DIRECTIONALBLUR \_ 優化 \_ 品質</span><span class="sxs-lookup"><span data-stu-id="1aefe-153">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_QUALITY</span></span>  | <span data-ttu-id="1aefe-154">只會使用具有大型模糊半徑的內部優化，其中近似值較不可能可見。</span><span class="sxs-lookup"><span data-stu-id="1aefe-154">Only uses internal optimizations with large blur radii, where approximations are less likely to be visible.</span></span> <span data-ttu-id="1aefe-155">使用三線性篩選。</span><span class="sxs-lookup"><span data-stu-id="1aefe-155">Uses trilinear filtering.</span></span> |



 

## <a name="output-bitmap"></a><span data-ttu-id="1aefe-156">輸出點陣圖</span><span class="sxs-lookup"><span data-stu-id="1aefe-156">Output bitmap</span></span>

<span data-ttu-id="1aefe-157">輸出點陣圖的大小是模糊輸出的大小。</span><span class="sxs-lookup"><span data-stu-id="1aefe-157">The size of the output bitmap is the size of the blur output.</span></span> <span data-ttu-id="1aefe-158">相對於原始點陣圖的輸出點陣圖成長量，可以使用下列方程式來計算：</span><span class="sxs-lookup"><span data-stu-id="1aefe-158">The amount the output bitmap growth relative to the original bitmap can be calculated using the following equation:</span></span>

<span data-ttu-id="1aefe-159">輸出點陣圖成長 (X 和 Y) = BlurStandardDeviation (與裝置無關的圖元 (Dip) ) \* 6 \* (使用者 DPI) /96</span><span class="sxs-lookup"><span data-stu-id="1aefe-159">Output Bitmap Growth (X and Y) = BlurStandardDeviation (device-independent pixels (DIPs))\*6\*(User DPI)/96</span></span>

<span data-ttu-id="1aefe-160">輸出會在所有方向平均增加，因此，如果大小在每個方向增加10個圖元，點陣圖的左上角就會位於 (-5，-5) ，而右下角會是 (105，105) ，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="1aefe-160">The output increases equally in all direction, so for example if the size increases by 10 pixels in each direction, the upper left corner of the bitmap is located at (-5, -5) and the lower right will be at (105, 105) as shown in the diagram here.</span></span>

![陰影效果輸出大小成長圖表。](images/drop-shadow-output-growth.png)

## <a name="requirements"></a><span data-ttu-id="1aefe-162">規格需求</span><span class="sxs-lookup"><span data-stu-id="1aefe-162">Requirements</span></span>



| <span data-ttu-id="1aefe-163">需求</span><span class="sxs-lookup"><span data-stu-id="1aefe-163">Requirement</span></span> | <span data-ttu-id="1aefe-164">值</span><span class="sxs-lookup"><span data-stu-id="1aefe-164">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1aefe-165">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1aefe-165">Minimum supported client</span></span> | <span data-ttu-id="1aefe-166">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1aefe-166">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="1aefe-167">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1aefe-167">Minimum supported server</span></span> | <span data-ttu-id="1aefe-168">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1aefe-168">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="1aefe-169">標頭</span><span class="sxs-lookup"><span data-stu-id="1aefe-169">Header</span></span>                   | <span data-ttu-id="1aefe-170">d2d1effects。h</span><span class="sxs-lookup"><span data-stu-id="1aefe-170">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="1aefe-171">程式庫</span><span class="sxs-lookup"><span data-stu-id="1aefe-171">Library</span></span>                  | <span data-ttu-id="1aefe-172">d2d1 .lib，dxguid .lib</span><span class="sxs-lookup"><span data-stu-id="1aefe-172">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="1aefe-173">相關主題</span><span class="sxs-lookup"><span data-stu-id="1aefe-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1aefe-174">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="1aefe-174">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

