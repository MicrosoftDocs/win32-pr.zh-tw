---
title: 複合效果
description: 使用複合效果結合2個或多個影像。 此效果有13個不同的複合模式。
ms.assetid: 60b878e9-1bc6-40d4-ade3-4bbd5c822c55
keywords:
- 複合效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9872a66d031e8307f911ec7270af81397a80276
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934524"
---
# <a name="composite-effect"></a><span data-ttu-id="7be08-105">複合效果</span><span class="sxs-lookup"><span data-stu-id="7be08-105">Composite effect</span></span>

<span data-ttu-id="7be08-106">使用複合效果結合2個或多個影像。</span><span class="sxs-lookup"><span data-stu-id="7be08-106">Use the composite effect to combine 2 or more images.</span></span> <span data-ttu-id="7be08-107">此效果有13個不同的複合模式。</span><span class="sxs-lookup"><span data-stu-id="7be08-107">This effect has 13 different composite modes.</span></span> <span data-ttu-id="7be08-108">T</span><span class="sxs-lookup"><span data-stu-id="7be08-108">T</span></span>

<span data-ttu-id="7be08-109">複合效果接受2個以上的輸入。</span><span class="sxs-lookup"><span data-stu-id="7be08-109">The composite effect accepts 2 or more inputs.</span></span> <span data-ttu-id="7be08-110">當您指定2個影像時，目的地是第一個輸入 (索引 0) ，而來源是第二個輸入 (索引 1) 。</span><span class="sxs-lookup"><span data-stu-id="7be08-110">When you specify 2 images, destination is the first input (index 0) and the source is the second input (index 1).</span></span> <span data-ttu-id="7be08-111">如果您指定2個以上的輸入，則影像會從第一個輸入開始，而第二個則是從第一個輸入開始，依此類推。</span><span class="sxs-lookup"><span data-stu-id="7be08-111">If you specify more than 2 inputs the images are composited starting with the first input and the second and so on.</span></span>

<span data-ttu-id="7be08-112">此效果會使用圖形處理器 (GPU) 的混合單位來執行所有模式。</span><span class="sxs-lookup"><span data-stu-id="7be08-112">This effect implements all of the modes using the blending unit of the graphics processing unit (GPU).</span></span>

<span data-ttu-id="7be08-113">這項效果的 CLSID 是 CLSID \_ D2D1Composite。</span><span class="sxs-lookup"><span data-stu-id="7be08-113">The CLSID for this effect is CLSID\_D2D1Composite.</span></span>

-   [<span data-ttu-id="7be08-114">範例影像</span><span class="sxs-lookup"><span data-stu-id="7be08-114">Example image</span></span>](#example-image)
-   [<span data-ttu-id="7be08-115">效果屬性</span><span class="sxs-lookup"><span data-stu-id="7be08-115">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="7be08-116">模式類型</span><span class="sxs-lookup"><span data-stu-id="7be08-116">Mode types</span></span>](#mode-types)
-   [<span data-ttu-id="7be08-117">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="7be08-117">Sample code</span></span>](#sample-code)
-   [<span data-ttu-id="7be08-118">需求</span><span class="sxs-lookup"><span data-stu-id="7be08-118">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="7be08-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="7be08-119">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="7be08-120">範例影像</span><span class="sxs-lookup"><span data-stu-id="7be08-120">Example image</span></span>

<span data-ttu-id="7be08-121">此處的影像顯示兩個相同大小重迭的圓角矩形。</span><span class="sxs-lookup"><span data-stu-id="7be08-121">The image here shows 2 rounded rectangles of the same size that overlap.</span></span> <span data-ttu-id="7be08-122">藍色矩形是來源，紅色矩形是目的地。</span><span class="sxs-lookup"><span data-stu-id="7be08-122">The blue rectangle is the source and the red rectangle is the destination.</span></span> <span data-ttu-id="7be08-123">這些映射是由來源 Over 模式所撰寫。</span><span class="sxs-lookup"><span data-stu-id="7be08-123">The images were composited with the Source Over mode.</span></span>

![範例影像，顯示使用來源 over 模式重迭的兩個相同大小的圓角矩形。](images/composite-over.png)

<span data-ttu-id="7be08-125">以下是使用預設模式的另一個範例。</span><span class="sxs-lookup"><span data-stu-id="7be08-125">Here's another example using the default mode.</span></span>



| <span data-ttu-id="7be08-126">影像1之前</span><span class="sxs-lookup"><span data-stu-id="7be08-126">Before image 1</span></span>                                                          |
|-------------------------------------------------------------------------|
| ![效果前的第一個來源影像。](images/default-before.jpg) |
| <span data-ttu-id="7be08-128">影像2之前</span><span class="sxs-lookup"><span data-stu-id="7be08-128">Before image 2</span></span>                                                          |
| ![效果之前的第二個影像。](images/3-composite(2of2).png)    |
| <span data-ttu-id="7be08-130">After</span><span class="sxs-lookup"><span data-stu-id="7be08-130">After</span></span>                                                                   |
| ![轉換後的影像。](images/3-composite.png)               |



 


```C++
ComPtr<ID2D1Effect> compositeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect);

compositeEffect->SetInput(0, bitmap);
compositeEffect->SetInput(1, bitmapTwo);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="7be08-132">效果屬性</span><span class="sxs-lookup"><span data-stu-id="7be08-132">Effect properties</span></span>



| <span data-ttu-id="7be08-133">顯示名稱和索引列舉</span><span class="sxs-lookup"><span data-stu-id="7be08-133">Display name and index enumeration</span></span>                     | <span data-ttu-id="7be08-134">類型和預設值</span><span class="sxs-lookup"><span data-stu-id="7be08-134">Type and default value</span></span>                                                          | <span data-ttu-id="7be08-135">描述</span><span class="sxs-lookup"><span data-stu-id="7be08-135">Description</span></span>                   |
|--------------------------------------------------------|---------------------------------------------------------------------------------|-------------------------------|
| <span data-ttu-id="7be08-136">[模式]</span><span class="sxs-lookup"><span data-stu-id="7be08-136">Mode</span></span><br/> <span data-ttu-id="7be08-137">D2D1 \_ 複合 \_ \_ 模型模式</span><span class="sxs-lookup"><span data-stu-id="7be08-137">D2D1\_COMPOSITE\_PROP\_MODE</span></span><br/> | <span data-ttu-id="7be08-138">D2D1 \_ 複合 \_ 模式</span><span class="sxs-lookup"><span data-stu-id="7be08-138">D2D1\_COMPOSITE\_MODE</span></span><br/> <span data-ttu-id="7be08-139">D2D1 \_ 複合 \_ 模式 \_ 來源 \_</span><span class="sxs-lookup"><span data-stu-id="7be08-139">D2D1\_COMPOSITE\_MODE\_SOURCE\_OVER</span></span><br/> | <span data-ttu-id="7be08-140">效果所使用的模式。</span><span class="sxs-lookup"><span data-stu-id="7be08-140">The mode used for the effect.</span></span> |



 

## <a name="mode-types"></a><span data-ttu-id="7be08-141">模式類型</span><span class="sxs-lookup"><span data-stu-id="7be08-141">Mode types</span></span>

<span data-ttu-id="7be08-142">此處的表格顯示此效果的模式。</span><span class="sxs-lookup"><span data-stu-id="7be08-142">The table here shows the modes of this effect.</span></span> <span data-ttu-id="7be08-143">表格中所列的方能使用下列元素：</span><span class="sxs-lookup"><span data-stu-id="7be08-143">The equations listed in the table use these elements:</span></span>

-   <span data-ttu-id="7be08-144">O = 輸出</span><span class="sxs-lookup"><span data-stu-id="7be08-144">O = Output</span></span>
-   <span data-ttu-id="7be08-145">S = 來源</span><span class="sxs-lookup"><span data-stu-id="7be08-145">S = Source</span></span>
-   <span data-ttu-id="7be08-146">SA = 來源 Alpha</span><span class="sxs-lookup"><span data-stu-id="7be08-146">SA = Source Alpha</span></span>
-   <span data-ttu-id="7be08-147">D = 目的地</span><span class="sxs-lookup"><span data-stu-id="7be08-147">D = Destination</span></span>
-   <span data-ttu-id="7be08-148">DA = 目的地 Alpha</span><span class="sxs-lookup"><span data-stu-id="7be08-148">DA = Destination Alpha</span></span>



| <span data-ttu-id="7be08-149">列舉型別</span><span class="sxs-lookup"><span data-stu-id="7be08-149">Enumeration</span></span>                                  | <span data-ttu-id="7be08-150">方程</span><span class="sxs-lookup"><span data-stu-id="7be08-150">Equation</span></span>                          | <span data-ttu-id="7be08-151">輸出點陣圖大小</span><span class="sxs-lookup"><span data-stu-id="7be08-151">Output Bitmap Size</span></span>                                                                                      |
|----------------------------------------------|-----------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7be08-152">D2D1 \_ 複合 \_ 模式 \_ 來源 \_</span><span class="sxs-lookup"><span data-stu-id="7be08-152">D2D1\_COMPOSITE\_MODE\_SOURCE\_OVER</span></span>          | <span data-ttu-id="7be08-153">O = S + (1 SA) \* D</span><span class="sxs-lookup"><span data-stu-id="7be08-153">O = S + (1   SA) \* D</span></span>             | <span data-ttu-id="7be08-154">來源和目的地點陣圖的聯集</span><span class="sxs-lookup"><span data-stu-id="7be08-154">Union of source and destination bitmaps</span></span>                                                                 |
| <span data-ttu-id="7be08-155">D2D1 \_ 複合 \_ 模式 \_ 目的地 \_</span><span class="sxs-lookup"><span data-stu-id="7be08-155">D2D1\_COMPOSITE\_MODE\_DESTINATION\_OVER</span></span>     | <span data-ttu-id="7be08-156">O = (1 DA) \* S + D</span><span class="sxs-lookup"><span data-stu-id="7be08-156">O = (1   DA) \* S + D</span></span>             | <span data-ttu-id="7be08-157">來源和目的地點陣圖的聯集</span><span class="sxs-lookup"><span data-stu-id="7be08-157">Union of source and destination bitmaps</span></span>                                                                 |
| <span data-ttu-id="7be08-158">D2D1 \_ 複合 \_ 模式 \_ 來源 \_</span><span class="sxs-lookup"><span data-stu-id="7be08-158">D2D1\_COMPOSITE\_MODE\_SOURCE\_IN</span></span>            | <span data-ttu-id="7be08-159">O = DA \* S</span><span class="sxs-lookup"><span data-stu-id="7be08-159">O = DA \* S</span></span>                       | <span data-ttu-id="7be08-160">來源和目的地點陣圖的交集</span><span class="sxs-lookup"><span data-stu-id="7be08-160">Intersection of source and destination bitmaps</span></span>                                                          |
| <span data-ttu-id="7be08-161">D2D1 \_ 複合 \_ 模式 \_ 目的地 \_</span><span class="sxs-lookup"><span data-stu-id="7be08-161">D2D1\_COMPOSITE\_MODE\_DESTINATION\_IN</span></span>       | <span data-ttu-id="7be08-162">O = SA \* D</span><span class="sxs-lookup"><span data-stu-id="7be08-162">O = SA \* D</span></span>                       | <span data-ttu-id="7be08-163">來源和目的地點陣圖的交集</span><span class="sxs-lookup"><span data-stu-id="7be08-163">Intersection of source and destination bitmaps</span></span>                                                          |
| <span data-ttu-id="7be08-164">D2D1 \_ 複合 \_ 模式 \_ 來源 \_ 輸出</span><span class="sxs-lookup"><span data-stu-id="7be08-164">D2D1\_COMPOSITE\_MODE\_SOURCE\_OUT</span></span>           | <span data-ttu-id="7be08-165">O = (1-DA) \* S</span><span class="sxs-lookup"><span data-stu-id="7be08-165">O = (1 - DA) \* S</span></span>                 | <span data-ttu-id="7be08-166">來源點陣圖的區域</span><span class="sxs-lookup"><span data-stu-id="7be08-166">Region of the source bitmap</span></span>                                                                             |
| <span data-ttu-id="7be08-167">D2D1 \_ 複合 \_ 模式 \_ 目的地 \_ 輸出</span><span class="sxs-lookup"><span data-stu-id="7be08-167">D2D1\_COMPOSITE\_MODE\_DESTINATION\_OUT</span></span>      | <span data-ttu-id="7be08-168">O = (1-SA) \* D</span><span class="sxs-lookup"><span data-stu-id="7be08-168">O = (1 - SA) \* D</span></span>                 | <span data-ttu-id="7be08-169">目的地點陣圖的區域</span><span class="sxs-lookup"><span data-stu-id="7be08-169">Region of the destination bitmap</span></span>                                                                        |
| <span data-ttu-id="7be08-170">D2D1 \_ 複合 \_ 模式 \_ 來源 \_</span><span class="sxs-lookup"><span data-stu-id="7be08-170">D2D1\_COMPOSITE\_MODE\_SOURCE\_ATOP</span></span>          | <span data-ttu-id="7be08-171">O = DA \* S + (1-SA) \* D</span><span class="sxs-lookup"><span data-stu-id="7be08-171">O = DA \* S + (1 - SA) \* D</span></span>       | <span data-ttu-id="7be08-172">目的地點陣圖的區域</span><span class="sxs-lookup"><span data-stu-id="7be08-172">Region of the destination bitmap</span></span>                                                                        |
| <span data-ttu-id="7be08-173">D2D1 \_ 複合 \_ 模式 \_ 目的地 \_</span><span class="sxs-lookup"><span data-stu-id="7be08-173">D2D1\_COMPOSITE\_MODE\_DESTINATION\_ATOP</span></span>     | <span data-ttu-id="7be08-174">O = (1-DA) \* S + SA \* D</span><span class="sxs-lookup"><span data-stu-id="7be08-174">O = (1 - DA) \* S + SA \* D</span></span>       | <span data-ttu-id="7be08-175">來源點陣圖的區域</span><span class="sxs-lookup"><span data-stu-id="7be08-175">Region of the source bitmap</span></span>                                                                             |
| <span data-ttu-id="7be08-176">D2D1 \_ 複合 \_ 模式 \_ XOR</span><span class="sxs-lookup"><span data-stu-id="7be08-176">D2D1\_COMPOSITE\_MODE\_XOR</span></span>                   | <span data-ttu-id="7be08-177">O = (1-DA) \* S + (1-SA) \* D</span><span class="sxs-lookup"><span data-stu-id="7be08-177">O = (1 - DA) \* S + (1 - SA) \* D</span></span> | <span data-ttu-id="7be08-178">來源和目的地點陣圖的聯集</span><span class="sxs-lookup"><span data-stu-id="7be08-178">Union of source and destination bitmaps</span></span>                                                                 |
| <span data-ttu-id="7be08-179">D2D1 \_ 複合 \_ 模式 \_ 加號</span><span class="sxs-lookup"><span data-stu-id="7be08-179">D2D1\_COMPOSITE\_MODE\_PLUS</span></span>                  | <span data-ttu-id="7be08-180">O = S + D</span><span class="sxs-lookup"><span data-stu-id="7be08-180">O = S + D</span></span>                         | <span data-ttu-id="7be08-181">來源和目的地點陣圖的聯集</span><span class="sxs-lookup"><span data-stu-id="7be08-181">Union of source and destination bitmaps</span></span>                                                                 |
| <span data-ttu-id="7be08-182">D2D1 \_ 複合 \_ 模式 \_ 來源 \_ 複製</span><span class="sxs-lookup"><span data-stu-id="7be08-182">D2D1\_COMPOSITE\_MODE\_SOURCE\_COPY</span></span>          | <span data-ttu-id="7be08-183">O = S</span><span class="sxs-lookup"><span data-stu-id="7be08-183">O = S</span></span>                             | <span data-ttu-id="7be08-184">來源點陣圖的區域</span><span class="sxs-lookup"><span data-stu-id="7be08-184">Region of the source bitmap</span></span>                                                                             |
| <span data-ttu-id="7be08-185">D2D1 \_ 複合 \_ 模式系結 \_ \_ 來源 \_ 複製</span><span class="sxs-lookup"><span data-stu-id="7be08-185">D2D1\_COMPOSITE\_MODE\_BOUNDED\_SOURCE\_COPY</span></span> | <span data-ttu-id="7be08-186">O = S (只有在來源存在時) </span><span class="sxs-lookup"><span data-stu-id="7be08-186">O = S (only where source exists)</span></span>  | <span data-ttu-id="7be08-187">來源和目的點陣圖的聯集。</span><span class="sxs-lookup"><span data-stu-id="7be08-187">Union of source and destination bitmaps.</span></span> <span data-ttu-id="7be08-188">來源不存在時，不會覆寫目的地。</span><span class="sxs-lookup"><span data-stu-id="7be08-188">Destination is not overwritten where the source doesn't exist.</span></span> |
| <span data-ttu-id="7be08-189">D2D1 \_ 複合 \_ 模式 \_ 遮罩 \_ 倒轉</span><span class="sxs-lookup"><span data-stu-id="7be08-189">D2D1\_COMPOSITE\_MODE\_MASK\_INVERT</span></span>          | <span data-ttu-id="7be08-190">O = (1 D) \* S + (1 SA) \* D</span><span class="sxs-lookup"><span data-stu-id="7be08-190">O = (1   D) \* S + (1   SA) \* D</span></span>  | <span data-ttu-id="7be08-191">來源和目的點陣圖的聯集。Alpha 值是不變的。</span><span class="sxs-lookup"><span data-stu-id="7be08-191">Union of source and destination bitmaps.The alpha values are unchanged.</span></span>                                 |



 

<span data-ttu-id="7be08-192">下圖顯示每個模式的範例，其中包含不透明度為1.0 或0.5 的影像。</span><span class="sxs-lookup"><span data-stu-id="7be08-192">The figure here shows an example of each of the modes with images that have an opacity of 1.0 or 0.5.</span></span>

![每個模式的範例影像，其不透明度設定為1.0 或0.5。](images/composite-types.png)

## <a name="sample-code"></a><span data-ttu-id="7be08-194">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="7be08-194">Sample code</span></span>

<span data-ttu-id="7be08-195">如需此效果的範例，請下載 [Direct2D 複合效果模式範例](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample)。</span><span class="sxs-lookup"><span data-stu-id="7be08-195">For an example of this effect, download the [Direct2D composite effect modes sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample).</span></span>

## <a name="requirements"></a><span data-ttu-id="7be08-196">規格需求</span><span class="sxs-lookup"><span data-stu-id="7be08-196">Requirements</span></span>



| <span data-ttu-id="7be08-197">需求</span><span class="sxs-lookup"><span data-stu-id="7be08-197">Requirement</span></span> | <span data-ttu-id="7be08-198">值</span><span class="sxs-lookup"><span data-stu-id="7be08-198">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7be08-199">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7be08-199">Minimum supported client</span></span> | <span data-ttu-id="7be08-200">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7be08-200">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="7be08-201">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7be08-201">Minimum supported server</span></span> | <span data-ttu-id="7be08-202">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7be08-202">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="7be08-203">標頭</span><span class="sxs-lookup"><span data-stu-id="7be08-203">Header</span></span>                   | <span data-ttu-id="7be08-204">d2d1effects。h</span><span class="sxs-lookup"><span data-stu-id="7be08-204">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="7be08-205">程式庫</span><span class="sxs-lookup"><span data-stu-id="7be08-205">Library</span></span>                  | <span data-ttu-id="7be08-206">d2d1 .lib，dxguid .lib</span><span class="sxs-lookup"><span data-stu-id="7be08-206">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="7be08-207">相關主題</span><span class="sxs-lookup"><span data-stu-id="7be08-207">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7be08-208">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="7be08-208">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

