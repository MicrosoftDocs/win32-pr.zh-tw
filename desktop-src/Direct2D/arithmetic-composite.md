---
title: 算術複合效果
description: 使用算術複合效果，以使用輸入影像中圖元的加權總和來合併2個影像。
ms.assetid: 6EC8CD61-5B51-4A8E-8A61-B291ABB5C5E0
keywords:
- 算術複合效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04c235ecb024c6b9e7adbce31c9f0cd65bc36cdf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934846"
---
# <a name="arithmetic-composite-effect"></a><span data-ttu-id="89241-104">算術複合效果</span><span class="sxs-lookup"><span data-stu-id="89241-104">Arithmetic composite effect</span></span>

<span data-ttu-id="89241-105">使用算術複合效果，以使用輸入影像中圖元的加權總和來合併2個影像。</span><span class="sxs-lookup"><span data-stu-id="89241-105">Use the arithmetic composite effect to combine 2 images using a weighted sum of pixels from the input images.</span></span>

<span data-ttu-id="89241-106">這項效果的 CLSID 是 CLSID \_ D2D1ArithmeticComposite。</span><span class="sxs-lookup"><span data-stu-id="89241-106">The CLSID for this effect is CLSID\_D2D1ArithmeticComposite.</span></span>

-   [<span data-ttu-id="89241-107">Formula</span><span class="sxs-lookup"><span data-stu-id="89241-107">Formula</span></span>](#formula)
-   [<span data-ttu-id="89241-108">範例影像</span><span class="sxs-lookup"><span data-stu-id="89241-108">Example image</span></span>](#example-image)
-   [<span data-ttu-id="89241-109">效果屬性</span><span class="sxs-lookup"><span data-stu-id="89241-109">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="89241-110">輸出點陣圖</span><span class="sxs-lookup"><span data-stu-id="89241-110">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="89241-111">需求</span><span class="sxs-lookup"><span data-stu-id="89241-111">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="89241-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="89241-112">Related topics</span></span>](#related-topics)

## <a name="formula"></a><span data-ttu-id="89241-113">Formula</span><span class="sxs-lookup"><span data-stu-id="89241-113">Formula</span></span>

<span data-ttu-id="89241-114">這裡的公式可用來計算此效果。</span><span class="sxs-lookup"><span data-stu-id="89241-114">The formula here is used to compute this effect.</span></span>

<span data-ttu-id="89241-115">輸出<sub>rgba</sub> = C1 \* 來源<sub>rgba</sub> \* 目的地<sub>rgba</sub> + c2 \* 來源<sub>rgba</sub> + c3 \* 目的地<sub>rgba</sub> + c4</span><span class="sxs-lookup"><span data-stu-id="89241-115">Output<sub>rgba</sub> = C1 \* Source<sub>rgba</sub> \* Destination<sub>rgba</sub> + C2 \* Source<sub>rgba</sub> + C3 \* Destination<sub>rgba</sub> + C4</span></span>

<span data-ttu-id="89241-116">其中 C1、C2、C3、C4 是您所設定的係數。</span><span class="sxs-lookup"><span data-stu-id="89241-116">Where C1, C2, C3, C4 are coefficients that you set.</span></span>

<span data-ttu-id="89241-117">係數會對應至 D2D1 向量中的值 \_ \_ 4F (x、y、z、w) ：</span><span class="sxs-lookup"><span data-stu-id="89241-117">The coefficients map to the values in a D2D1\_VECTOR\_4F (x, y, z, w):</span></span>

-   <span data-ttu-id="89241-118">x = C1</span><span class="sxs-lookup"><span data-stu-id="89241-118">x = C1</span></span>
-   <span data-ttu-id="89241-119">y = C2</span><span class="sxs-lookup"><span data-stu-id="89241-119">y = C2</span></span>
-   <span data-ttu-id="89241-120">z = C3</span><span class="sxs-lookup"><span data-stu-id="89241-120">z = C3</span></span>
-   <span data-ttu-id="89241-121">w = C4</span><span class="sxs-lookup"><span data-stu-id="89241-121">w = C4</span></span>

## <a name="example-image"></a><span data-ttu-id="89241-122">範例影像</span><span class="sxs-lookup"><span data-stu-id="89241-122">Example image</span></span>

<span data-ttu-id="89241-123">簡單的範例是加入來源和目的地圖元。</span><span class="sxs-lookup"><span data-stu-id="89241-123">A simple example is to add the source and destination pixels.</span></span> <span data-ttu-id="89241-124">在此範例中，會將兩個圓角的矩形組合在一起。</span><span class="sxs-lookup"><span data-stu-id="89241-124">In the example, 2 rounded rectangles are composited together.</span></span> <span data-ttu-id="89241-125">來源矩形為藍色，目的地為紅色。</span><span class="sxs-lookup"><span data-stu-id="89241-125">The source rectangle is blue and the destination is red.</span></span>

<span data-ttu-id="89241-126">此處的影像是算術複合效果的輸出，其方程式的係數設定為此處的值。</span><span class="sxs-lookup"><span data-stu-id="89241-126">The image here is the output of the Arithmetic Composite effect with the coefficients of the equation set to the values here.</span></span>

-   <span data-ttu-id="89241-127">C1 = 0</span><span class="sxs-lookup"><span data-stu-id="89241-127">C1 = 0</span></span>
-   <span data-ttu-id="89241-128">C2 = 1</span><span class="sxs-lookup"><span data-stu-id="89241-128">C2 = 1</span></span>
-   <span data-ttu-id="89241-129">C3 = 1</span><span class="sxs-lookup"><span data-stu-id="89241-129">C3 = 1</span></span>
-   <span data-ttu-id="89241-130">C4 = 0</span><span class="sxs-lookup"><span data-stu-id="89241-130">C4 = 0</span></span>

![範例影像，顯示使用算術複合效果重迭的兩個相同大小的圓角矩形。](images/arithmetic-50-percent.png)

<span data-ttu-id="89241-132">結果是會加入來源和目的地的圖元值。</span><span class="sxs-lookup"><span data-stu-id="89241-132">The result is that the pixel values for the source and destination are added.</span></span> <span data-ttu-id="89241-133">矩形不會與 RGBA 值重迭的區域全部都是0。</span><span class="sxs-lookup"><span data-stu-id="89241-133">The regions where the rectangles don't overlap the RGBA values are all 0.</span></span> <span data-ttu-id="89241-134">因為 R 和 B 值都是最大值，所以矩形會重迭色彩為洋紅。</span><span class="sxs-lookup"><span data-stu-id="89241-134">Where the rectangles overlap the color is magenta because the R and B values are both at maximum.</span></span>

<span data-ttu-id="89241-135">以下是另一個包含程式碼的範例影像。</span><span class="sxs-lookup"><span data-stu-id="89241-135">Here's another example image with code.</span></span>



| <span data-ttu-id="89241-136">影像1之前</span><span class="sxs-lookup"><span data-stu-id="89241-136">Before image 1</span></span>                                                             |
|----------------------------------------------------------------------------|
| ![效果前的第一個來源影像。](images/default-before.jpg)    |
| <span data-ttu-id="89241-138">影像2之前</span><span class="sxs-lookup"><span data-stu-id="89241-138">Before image 2</span></span>                                                             |
| ![效果之前的第二個影像。](images/4-arthimetic-composite2.jpg) |
| <span data-ttu-id="89241-140">After</span><span class="sxs-lookup"><span data-stu-id="89241-140">After</span></span>                                                                      |
| ![轉換後的影像。](images/4-arithmeticcomposite.png)        |



 


```C++
ComPtr<ID2D1Effect> arithmeticCompositeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1ArithmeticComposite, &arithmeticCompositeEffect);

arithmeticCompositeEffect->SetInput(0, bitmap);
arithmeticCompositeEffect->SetInput(1, bitmapTwo);
arithmeticCompositeEffect->SetValue(D2D1_ARITHMETICCOMPOSITE_PROP_COEFFICIENTS, D2D1::Vector4F(0.0f, 0.5f, 0.5f, 0.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(arithmeticCompositeEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="89241-142">效果屬性</span><span class="sxs-lookup"><span data-stu-id="89241-142">Effect properties</span></span>



| <span data-ttu-id="89241-143">顯示名稱和索引列舉</span><span class="sxs-lookup"><span data-stu-id="89241-143">Display name and index enumeration</span></span>                                               | <span data-ttu-id="89241-144">Description</span><span class="sxs-lookup"><span data-stu-id="89241-144">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89241-145">係數</span><span class="sxs-lookup"><span data-stu-id="89241-145">Coefficients</span></span><br/> <span data-ttu-id="89241-146">D2D1 ARITHMETICCOMPOSITE 的各種 \_ \_ \_ 係數</span><span class="sxs-lookup"><span data-stu-id="89241-146">D2D1\_ARITHMETICCOMPOSITE\_PROP\_COEFFICIENTS</span></span><br/> | <span data-ttu-id="89241-147">用來組合兩個輸入影像的方程式係數。</span><span class="sxs-lookup"><span data-stu-id="89241-147">The coefficients for the equation used to composite the two input images.</span></span> <span data-ttu-id="89241-148">係數沒有單位或未系結。</span><span class="sxs-lookup"><span data-stu-id="89241-148">The coefficients are unitless and unbounded.</span></span> <span data-ttu-id="89241-149">類型為 D2D1 \_ VECTOR \_ 4F。</span><span class="sxs-lookup"><span data-stu-id="89241-149">Type is D2D1\_VECTOR\_4F.</span></span><br/> <span data-ttu-id="89241-150">預設值為 {1.0 f、0.0 f、0.0 f、0.0 f}。</span><span class="sxs-lookup"><span data-stu-id="89241-150">Default value is {1.0f, 0.0f, 0.0f, 0.0f}.</span></span><br/>                                                                                                                                                                                                                                 |
| <span data-ttu-id="89241-151">ClampOutput</span><span class="sxs-lookup"><span data-stu-id="89241-151">ClampOutput</span></span><br/> <span data-ttu-id="89241-152">D2D1 ARITHMETICCOMPOSITE 的一種 \_ \_ \_ 夾具 \_ 輸出</span><span class="sxs-lookup"><span data-stu-id="89241-152">D2D1\_ARITHMETICCOMPOSITE\_PROP\_CLAMP\_OUTPUT</span></span><br/> | <span data-ttu-id="89241-153">效果會個色彩值在0和1之間，效果會將值傳遞給圖形中的下一個效果。</span><span class="sxs-lookup"><span data-stu-id="89241-153">The effect clamps color values to between 0 and 1 before the effect passes the values to the next effect in the graph.</span></span> <br/> <span data-ttu-id="89241-154">如果您將此設定為 TRUE，效果會將值設為夾具。</span><span class="sxs-lookup"><span data-stu-id="89241-154">If you set this to TRUE the effect will clamp the values.</span></span> <span data-ttu-id="89241-155">如果您將此值設定為 FALSE，效果將不會顯示色彩值，但其他效果和輸出介面可能會在這些值的精確度不夠高時，將這些值設定為夾具。</span><span class="sxs-lookup"><span data-stu-id="89241-155">If you set this to FALSE, the effect will not clamp the color values, but other effects and the output surface may clamp the values if they are not of high enough precision.</span></span><br/> <span data-ttu-id="89241-156">類型為 BOOL。</span><span class="sxs-lookup"><span data-stu-id="89241-156">Type is BOOL.</span></span><br/> <span data-ttu-id="89241-157">預設值為 FALSE。</span><span class="sxs-lookup"><span data-stu-id="89241-157">Default value is FALSE.</span></span><br/> |



 

## <a name="output-bitmap"></a><span data-ttu-id="89241-158">輸出點陣圖</span><span class="sxs-lookup"><span data-stu-id="89241-158">Output bitmap</span></span>

<span data-ttu-id="89241-159">輸出點陣圖取決於係數值。</span><span class="sxs-lookup"><span data-stu-id="89241-159">The output bitmap depends on the coefficient values.</span></span> <span data-ttu-id="89241-160">這些是可能的輸出點陣圖大小。</span><span class="sxs-lookup"><span data-stu-id="89241-160">These are the possible output bitmap sizes.</span></span>

-   <span data-ttu-id="89241-161">如果 C1 是唯一的非零係數，則輸出大小是輸入矩形的交集。</span><span class="sxs-lookup"><span data-stu-id="89241-161">If C1 is the only non-zero coefficient, the output size is the intersection of the input rectangles.</span></span>
-   <span data-ttu-id="89241-162">如果 C2 是唯一的非零係數，輸出大小就是來源矩形的大小。</span><span class="sxs-lookup"><span data-stu-id="89241-162">If C2 is the only non-zero coefficient, the output size is the size of the Source rectangle.</span></span>
-   <span data-ttu-id="89241-163">如果 C3 是唯一的非零係數，輸出大小就是目的地矩形的大小。</span><span class="sxs-lookup"><span data-stu-id="89241-163">If C3 is the only non-zero coefficient, the output size is the size of the Destination rectangle..</span></span>
-   <span data-ttu-id="89241-164">如果所有係數都是零，則輸出大小為空的矩形。</span><span class="sxs-lookup"><span data-stu-id="89241-164">If all coefficients are zero, the output size is an empty rectangle.</span></span>
-   <span data-ttu-id="89241-165">針對所有其他係數值，輸出大小為輸入矩形的聯集。</span><span class="sxs-lookup"><span data-stu-id="89241-165">For all other coefficient values, the output size is the union of the input rectangles.</span></span>

## <a name="requirements"></a><span data-ttu-id="89241-166">規格需求</span><span class="sxs-lookup"><span data-stu-id="89241-166">Requirements</span></span>



| <span data-ttu-id="89241-167">需求</span><span class="sxs-lookup"><span data-stu-id="89241-167">Requirement</span></span> | <span data-ttu-id="89241-168">值</span><span class="sxs-lookup"><span data-stu-id="89241-168">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="89241-169">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="89241-169">Minimum supported client</span></span> | <span data-ttu-id="89241-170">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="89241-170">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="89241-171">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="89241-171">Minimum supported server</span></span> | <span data-ttu-id="89241-172">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="89241-172">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="89241-173">標頭</span><span class="sxs-lookup"><span data-stu-id="89241-173">Header</span></span>                   | <span data-ttu-id="89241-174">d2d1effects。h</span><span class="sxs-lookup"><span data-stu-id="89241-174">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="89241-175">程式庫</span><span class="sxs-lookup"><span data-stu-id="89241-175">Library</span></span>                  | <span data-ttu-id="89241-176">d2d1 .lib，dxguid .lib</span><span class="sxs-lookup"><span data-stu-id="89241-176">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="89241-177">相關主題</span><span class="sxs-lookup"><span data-stu-id="89241-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89241-178">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="89241-178">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

