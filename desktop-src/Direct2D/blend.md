---
title: 混合效果
description: 使用 blend 效果來合併2個影像。 此效果有26種 blend 模式。
ms.assetid: 39D8BAA3-8FF3-4F10-99A0-B26FCA3018AE
keywords:
- blend 效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e248d1f7f41721d173510b8d10feac9be2e08f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844243"
---
# <a name="blend-effect"></a><span data-ttu-id="cb268-105">混合效果</span><span class="sxs-lookup"><span data-stu-id="cb268-105">Blend effect</span></span>

<span data-ttu-id="cb268-106">使用 blend 效果來合併2個影像。</span><span class="sxs-lookup"><span data-stu-id="cb268-106">Use the blend effect to combine 2 images.</span></span> <span data-ttu-id="cb268-107">此效果有26種 blend 模式。</span><span class="sxs-lookup"><span data-stu-id="cb268-107">This effect has 26 blend modes.</span></span>

<span data-ttu-id="cb268-108">這項效果的 CLSID 是 CLSID \_ D2D1Blend。</span><span class="sxs-lookup"><span data-stu-id="cb268-108">The CLSID for this effect is CLSID\_D2D1Blend.</span></span>

-   [<span data-ttu-id="cb268-109">混合範例</span><span class="sxs-lookup"><span data-stu-id="cb268-109">Blending examples</span></span>](#blending-examples)
-   [<span data-ttu-id="cb268-110">效果屬性</span><span class="sxs-lookup"><span data-stu-id="cb268-110">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="cb268-111">Blend 模式</span><span class="sxs-lookup"><span data-stu-id="cb268-111">Blend modes</span></span>](#blend-modes)
-   [<span data-ttu-id="cb268-112">HSL 色彩空間轉換</span><span class="sxs-lookup"><span data-stu-id="cb268-112">HSL color space conversions</span></span>](#hsl-color-space-conversions)
    -   [<span data-ttu-id="cb268-113">從 RGB 轉換成 HSL</span><span class="sxs-lookup"><span data-stu-id="cb268-113">Converting from RGB to HSL</span></span>](#converting-from-rgb-to-hsl)
    -   [<span data-ttu-id="cb268-114">從 HSL 轉換成 RGB</span><span class="sxs-lookup"><span data-stu-id="cb268-114">Converting from HSL to RGB</span></span>](#converting-from-hsl-to-rgb)
-   [<span data-ttu-id="cb268-115">輸出點陣圖</span><span class="sxs-lookup"><span data-stu-id="cb268-115">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="cb268-116">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="cb268-116">Sample code</span></span>](#sample-code)
-   [<span data-ttu-id="cb268-117">需求</span><span class="sxs-lookup"><span data-stu-id="cb268-117">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="cb268-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="cb268-118">Related topics</span></span>](#related-topics)

## <a name="blending-examples"></a><span data-ttu-id="cb268-119">混合範例</span><span class="sxs-lookup"><span data-stu-id="cb268-119">Blending examples</span></span>

<span data-ttu-id="cb268-120">以下是 blend 效果的每個 blend 模式的範例影像。</span><span class="sxs-lookup"><span data-stu-id="cb268-120">Here is an example image of every blend mode of the blend effect.</span></span> <span data-ttu-id="cb268-121">下一節將列出 blend 模式和對應模式屬性的完整清單</span><span class="sxs-lookup"><span data-stu-id="cb268-121">A full list of the blend modes and the corresponding mode properties are in the next section</span></span>

![所有可用 blend 模式的效果範例螢幕擷取畫面。](images/blend-modes.png)

<span data-ttu-id="cb268-123">以下是使用排除模式的另一個範例。</span><span class="sxs-lookup"><span data-stu-id="cb268-123">Here is another example using the exclusion mode.</span></span>



| <span data-ttu-id="cb268-124">影像1之前</span><span class="sxs-lookup"><span data-stu-id="cb268-124">Before image 1</span></span>                                                             |
|----------------------------------------------------------------------------|
| ![效果前的第一個來源影像。](images/default-before.jpg)    |
| <span data-ttu-id="cb268-126">影像2之前</span><span class="sxs-lookup"><span data-stu-id="cb268-126">Before image 2</span></span>                                                             |
| ![效果之前的第二個影像。](images/4-arthimetic-composite2.jpg) |
| <span data-ttu-id="cb268-128">After</span><span class="sxs-lookup"><span data-stu-id="cb268-128">After</span></span>                                                                      |
| ![轉換後的影像。](images/5-blend.png)                      |



 


```C++
ComPtr<ID2D1Effect> blendEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Blend, &blendEffect);

blendEffect->SetInput(0, bitmap);
blendEffect->SetInput(1, bitmapTwo);
blendEffect->SetValue(D2D1_BLEND_PROP_MODE, D2D1_BLEND_MODE_EXCLUSION);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(blendEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="cb268-130">效果屬性</span><span class="sxs-lookup"><span data-stu-id="cb268-130">Effect properties</span></span>



| <span data-ttu-id="cb268-131">顯示名稱和索引列舉</span><span class="sxs-lookup"><span data-stu-id="cb268-131">Display name and index enumeration</span></span>                 | <span data-ttu-id="cb268-132">描述</span><span class="sxs-lookup"><span data-stu-id="cb268-132">Description</span></span>                                                                                                                                                                               |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb268-133">[模式]</span><span class="sxs-lookup"><span data-stu-id="cb268-133">Mode</span></span><br/> <span data-ttu-id="cb268-134">D2D1 \_ BLEND \_ \_ 模式</span><span class="sxs-lookup"><span data-stu-id="cb268-134">D2D1\_BLEND\_PROP\_MODE</span></span><br/> | <span data-ttu-id="cb268-135">用於效果的 blend 模式。</span><span class="sxs-lookup"><span data-stu-id="cb268-135">The blend mode used for the effect.</span></span> <span data-ttu-id="cb268-136">如需詳細資訊，請參閱 [Blend 模式](#blend-modes) 。</span><span class="sxs-lookup"><span data-stu-id="cb268-136">See [Blend modes](#blend-modes) for more info.</span></span> <span data-ttu-id="cb268-137">此類型為 D2D1 \_ BLEND \_ 模式。</span><span class="sxs-lookup"><span data-stu-id="cb268-137">The type is D2D1\_BLEND\_MODE.</span></span><br/> <span data-ttu-id="cb268-138">預設值為 D2D1 \_ BLEND \_ 模式 \_ 乘。</span><span class="sxs-lookup"><span data-stu-id="cb268-138">The default value is D2D1\_BLEND\_MODE\_MULTIPLY.</span></span><br/> |



 

## <a name="blend-modes"></a><span data-ttu-id="cb268-139">Blend 模式</span><span class="sxs-lookup"><span data-stu-id="cb268-139">Blend modes</span></span>

<span data-ttu-id="cb268-140">此處的表格顯示此效果的所有 blend 模式。</span><span class="sxs-lookup"><span data-stu-id="cb268-140">The table here shows all the blend modes of this effect.</span></span> <span data-ttu-id="cb268-141">計算效果輸出所需的 helper 函式是在下一節中。</span><span class="sxs-lookup"><span data-stu-id="cb268-141">The helper functions necessary to compute the output of the effect are in the next section.</span></span>

<span data-ttu-id="cb268-142">Color： O <sub>PRGB</sub>  =  *f* (f <sub>rgb</sub>，B <sub>rgb</sub>) \* f <sub>a</sub> \* B <sub>a</sub> + f <sub>RGB</sub> \* f <sub>a</sub> \* (1-B <sub>a</sub>) + B <sub>RGB</sub> \* B <sub>a</sub> \* (1-f <sub>a</sub>) </span><span class="sxs-lookup"><span data-stu-id="cb268-142">Color: O <sub>PRGB</sub> = *f*(F<sub>RGB</sub>, B<sub>RGB</sub>) \* F<sub>A</sub> \* B<sub>A</sub> + F<sub>RGB</sub> \* F<sub>A</sub> \* (1 - B<sub>A</sub>) + B<sub>RGB</sub> \* B<sub>A</sub> \* (1 - F<sub>A</sub>)</span></span>

<span data-ttu-id="cb268-143">Alpha： O<sub>a</sub> = F<sub>a</sub> \* (1-B<sub>a</sub>) + B<sub>a</sub></span><span class="sxs-lookup"><span data-stu-id="cb268-143">Alpha: O<sub>A</sub> = F<sub>A</sub> \* (1 - B<sub>A</sub>) + B<sub>A</sub></span></span>

<span data-ttu-id="cb268-144">其中：</span><span class="sxs-lookup"><span data-stu-id="cb268-144">Where:</span></span>

-   <span data-ttu-id="cb268-145">O<sub>PRGB</sub> 是前置乘輸出色彩</span><span class="sxs-lookup"><span data-stu-id="cb268-145">O<sub>PRGB</sub> is the pre-multiplied output color</span></span>
-   <span data-ttu-id="cb268-146">O<sub>A</sub> 是輸出 Alpha</span><span class="sxs-lookup"><span data-stu-id="cb268-146">O<sub>A</sub> is Output Alpha</span></span>
-   <span data-ttu-id="cb268-147">B<sub>RGB</sub> 是取消前置的目的地色彩</span><span class="sxs-lookup"><span data-stu-id="cb268-147">B<sub>RGB</sub> is the un-pre-multiplied destination color</span></span>
-   <span data-ttu-id="cb268-148">B<sub>A</sub> 是目的地 Alpha</span><span class="sxs-lookup"><span data-stu-id="cb268-148">B<sub>A</sub> is destination alpha</span></span>
-   <span data-ttu-id="cb268-149">F<sub>RGB</sub> 是取消前置的來源色彩</span><span class="sxs-lookup"><span data-stu-id="cb268-149">F<sub>RGB</sub> is the un-pre-multiplied source color</span></span>
-   <span data-ttu-id="cb268-150">F<sub>A</sub> 是來源 Alpha</span><span class="sxs-lookup"><span data-stu-id="cb268-150">F<sub>A</sub> is source alpha</span></span>
-   <span data-ttu-id="cb268-151">*f* (S <sub>Rgb</sub>，D <sub>rgb</sub>) 是一種會因 blend 模式而異的 blend 函數</span><span class="sxs-lookup"><span data-stu-id="cb268-151">*f*(S<sub>RGB</sub>, D<sub>RGB</sub>) is a blend function that varies per-blend-mode</span></span>

<span data-ttu-id="cb268-152">某些 blend 模式需要從色調、飽和度、亮度 (HSL) 色彩空間轉換成 RGB。</span><span class="sxs-lookup"><span data-stu-id="cb268-152">Some of the blend modes require conversion to and from the hue, saturation, luminosity (HSL) color space to RGB.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cb268-153">列舉型別</span><span class="sxs-lookup"><span data-stu-id="cb268-153">Enumeration</span></span></th>
<th><span data-ttu-id="cb268-154">方程</span><span class="sxs-lookup"><span data-stu-id="cb268-154">Equation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cb268-155">D2D1_BLEND_MODE_DARKEN</span><span class="sxs-lookup"><span data-stu-id="cb268-155">D2D1_BLEND_MODE_DARKEN</span></span></td>
<td><span data-ttu-id="cb268-156">僅適用于 Alpha 的基本 blend 公式。</span><span class="sxs-lookup"><span data-stu-id="cb268-156">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-darken-1.png" alt="mathematical formula for a darken effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb268-157">D2D1_BLEND_MODE_MULTIPLY</span><span class="sxs-lookup"><span data-stu-id="cb268-157">D2D1_BLEND_MODE_MULTIPLY</span></span></td>
<td><span data-ttu-id="cb268-158">僅適用于 Alpha 的基本 blend 公式。</span><span class="sxs-lookup"><span data-stu-id="cb268-158">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-multiply-1.png" alt="Mathematical formula for a mutiply effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb268-159">D2D1_BLEND_MODE_COLOR_BURN</span><span class="sxs-lookup"><span data-stu-id="cb268-159">D2D1_BLEND_MODE_COLOR_BURN</span></span></td>
<td><span data-ttu-id="cb268-160">使用 <em>f</em> (f<sub>Rgb</sub>、B<sub>rgb</sub>) = 的基本 blend 公式</span><span class="sxs-lookup"><span data-stu-id="cb268-160">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-colorburn-1.png" alt="Mathematical formula for a coor burn effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb268-161">D2D1_BLEND_MODE_LINEAR_BURN</span><span class="sxs-lookup"><span data-stu-id="cb268-161">D2D1_BLEND_MODE_LINEAR_BURN</span></span></td>
<td><span data-ttu-id="cb268-162">使用 <em>f</em> (f<sub>Rgb</sub>、B<sub>rgb</sub>) = 的基本 blend 公式</span><span class="sxs-lookup"><span data-stu-id="cb268-162">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-linearburn-1.png" alt="Mathematical formula for a linear burn effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb268-163">D2D1_BLEND_MODE_DARKER_COLOR</span><span class="sxs-lookup"><span data-stu-id="cb268-163">D2D1_BLEND_MODE_DARKER_COLOR</span></span></td>
<td><span data-ttu-id="cb268-164">僅適用于 Alpha 的基本 blend 公式。</span><span class="sxs-lookup"><span data-stu-id="cb268-164">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-darkencolor-1.png" alt="Mathematical formla for a darken color effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb268-165">D2D1_BLEND_MODE_LIGHTEN</span><span class="sxs-lookup"><span data-stu-id="cb268-165">D2D1_BLEND_MODE_LIGHTEN</span></span></td>
<td><span data-ttu-id="cb268-166">僅適用于 Alpha 的基本 blend 公式。</span><span class="sxs-lookup"><span data-stu-id="cb268-166">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-lighten-1.png" alt="Mathematical formula for a lighten effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb268-167">D2D1_BLEND_MODE_SCREEN</span><span class="sxs-lookup"><span data-stu-id="cb268-167">D2D1_BLEND_MODE_SCREEN</span></span></td>
<td><span data-ttu-id="cb268-168">僅適用于 Alpha 的基本 blend 公式。</span><span class="sxs-lookup"><span data-stu-id="cb268-168">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-screen-1.png" alt="Mathematical formula for a screen effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb268-169">D2D1_BLEND_MODE_COLOR_DODGE</span><span class="sxs-lookup"><span data-stu-id="cb268-169">D2D1_BLEND_MODE_COLOR_DODGE</span></span></td>
<td><span data-ttu-id="cb268-170">使用 <em>f</em> (f<sub>Rgb</sub>、B<sub>rgb</sub>) = 的基本 blend 公式</span><span class="sxs-lookup"><span data-stu-id="cb268-170">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-colordodge-1.png" alt="Mathematical formula for a color dodge effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb268-171">D2D1_BLEND_MODE_LINEAR_DODGE</span><span class="sxs-lookup"><span data-stu-id="cb268-171">D2D1_BLEND_MODE_LINEAR_DODGE</span></span></td>
<td><span data-ttu-id="cb268-172">使用 <em>f</em> (f<sub>Rgb</sub>、B<sub>rgb</sub>) = 的基本 blend 公式</span><span class="sxs-lookup"><span data-stu-id="cb268-172">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-lineardodge-1.png" alt="Mathematical formula for a linear dodge effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb268-173">D2D1_BLEND_MODE_LIGHTER_COLOR</span><span class="sxs-lookup"><span data-stu-id="cb268-173">D2D1_BLEND_MODE_LIGHTER_COLOR</span></span></td>
<td><span data-ttu-id="cb268-174">僅適用于 Alpha 的基本 blend 公式。</span><span class="sxs-lookup"><span data-stu-id="cb268-174">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-lightercolor-1.png" alt="Mathematical formula for a lighter color effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb268-175">D2D1_BLEND_MODE_OVERLAY</span><span class="sxs-lookup"><span data-stu-id="cb268-175">D2D1_BLEND_MODE_OVERLAY</span></span></td>
<td><span data-ttu-id="cb268-176">使用 <em>f</em> (f<sub>Rgb</sub>、B<sub>rgb</sub>) = 的基本 blend 公式</span><span class="sxs-lookup"><span data-stu-id="cb268-176">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-overlay-1.png" alt="Mathematical formula for an overlay effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb268-177">D2D1_BLEND_MODE_SOFT_LIGHT</span><span class="sxs-lookup"><span data-stu-id="cb268-177">D2D1_BLEND_MODE_SOFT_LIGHT</span></span></td>
<td><span data-ttu-id="cb268-178">使用 <em>f</em> (f<sub>Rgb</sub>、B<sub>rgb</sub>) = 的基本 blend 公式</span><span class="sxs-lookup"><span data-stu-id="cb268-178">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-softlight-1.png" alt="Mathematical formula for a soft light effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb268-179">D2D1_BLEND_MODE_HARD_LIGHT</span><span class="sxs-lookup"><span data-stu-id="cb268-179">D2D1_BLEND_MODE_HARD_LIGHT</span></span></td>
<td><span data-ttu-id="cb268-180">使用 <em>f</em> (f<sub>Rgb</sub>、B<sub>rgb</sub>) = 的基本 blend 公式</span><span class="sxs-lookup"><span data-stu-id="cb268-180">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-hardlight-1.png" alt="Mathematical formula for a hard light effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb268-181">D2D1_BLEND_MODE_VIVID_LIGHT</span><span class="sxs-lookup"><span data-stu-id="cb268-181">D2D1_BLEND_MODE_VIVID_LIGHT</span></span></td>
<td><span data-ttu-id="cb268-182">使用 <em>f</em> (f<sub>Rgb</sub>、B<sub>rgb</sub>) = 的基本 blend 公式</span><span class="sxs-lookup"><span data-stu-id="cb268-182">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-vividlight-1.png" alt="Mathematical formula for a vivid light effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb268-183">D2D1_BLEND_MODE_LINEAR_LIGHT</span><span class="sxs-lookup"><span data-stu-id="cb268-183">D2D1_BLEND_MODE_LINEAR_LIGHT</span></span></td>
<td><span data-ttu-id="cb268-184">使用 <em>f</em> (f<sub>Rgb</sub>、B<sub>rgb</sub>) = 的基本 blend 公式</span><span class="sxs-lookup"><span data-stu-id="cb268-184">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-linearlight-1.png" alt="Mathematical formula for a linear light effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb268-185">D2D1_BLEND_MODE_PIN_LIGHT</span><span class="sxs-lookup"><span data-stu-id="cb268-185">D2D1_BLEND_MODE_PIN_LIGHT</span></span></td>
<td><span data-ttu-id="cb268-186">使用 <em>f</em> (f<sub>Rgb</sub>、B<sub>rgb</sub>) = 的基本 blend 公式</span><span class="sxs-lookup"><span data-stu-id="cb268-186">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-pinlight-1.png" alt="Mathematical formula for a pin light effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb268-187">D2D1_BLEND_MODE_HARD_MIX</span><span class="sxs-lookup"><span data-stu-id="cb268-187">D2D1_BLEND_MODE_HARD_MIX</span></span></td>
<td><span data-ttu-id="cb268-188">使用 <em>f</em> (f<sub>Rgb</sub>、B<sub>rgb</sub>) = 的基本 blend 公式</span><span class="sxs-lookup"><span data-stu-id="cb268-188">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-hardmix-1.png" alt="Mathematical formula for a hard mix effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb268-189">D2D1_BLEND_MODE_DIFFERENCE</span><span class="sxs-lookup"><span data-stu-id="cb268-189">D2D1_BLEND_MODE_DIFFERENCE</span></span></td>
<td><span data-ttu-id="cb268-190">使用 <em>f</em> 的基本 blend 公式 (f<sub>Rgb</sub>、B<sub>RGB</sub>) = abs (f<sub>rgb</sub> - B<sub>rgb</sub>) </span><span class="sxs-lookup"><span data-stu-id="cb268-190">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) = abs(F<sub>RGB</sub> - B<sub>RGB</sub>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb268-191">D2D1_BLEND_MODE_EXCLUSION</span><span class="sxs-lookup"><span data-stu-id="cb268-191">D2D1_BLEND_MODE_EXCLUSION</span></span></td>
<td><span data-ttu-id="cb268-192">使用<em>f</em> (f<sub>Rgb</sub>、B<sub>rgb</sub>) = F<sub>rgb</sub> + b<sub>rgb</sub> 2 \* f<sub>rgb</sub> \* b<sub>rgb</sub>的基本 blend 公式</span><span class="sxs-lookup"><span data-stu-id="cb268-192">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) = F<sub>RGB</sub> + B<sub>RGB</sub>   2 \* F<sub>RGB</sub> \* B<sub>RGB</sub></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb268-193">D2D1_BLEND_MODE_HUE</span><span class="sxs-lookup"><span data-stu-id="cb268-193">D2D1_BLEND_MODE_HUE</span></span></td>
<td><span data-ttu-id="cb268-194">僅適用于 Alpha 的基本 blend 公式。</span><span class="sxs-lookup"><span data-stu-id="cb268-194">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-hue-1.png" alt="Mathematical formula for a hue blend effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb268-195">D2D1_BLEND_MODE_SATURATION</span><span class="sxs-lookup"><span data-stu-id="cb268-195">D2D1_BLEND_MODE_SATURATION</span></span></td>
<td><span data-ttu-id="cb268-196">僅適用于 Alpha 的基本 blend 公式。</span><span class="sxs-lookup"><span data-stu-id="cb268-196">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-saturation-1.png" alt="Mathematical formula for a sturation blend effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb268-197">D2D1_BLEND_MODE_COLOR</span><span class="sxs-lookup"><span data-stu-id="cb268-197">D2D1_BLEND_MODE_COLOR</span></span></td>
<td><span data-ttu-id="cb268-198">僅適用于 Alpha 的基本 blend 公式。</span><span class="sxs-lookup"><span data-stu-id="cb268-198">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-color-1.png" alt="Mathematical formula for a color blend effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb268-199">D2D1_BLEND_MODE_LUMINOSITY</span><span class="sxs-lookup"><span data-stu-id="cb268-199">D2D1_BLEND_MODE_LUMINOSITY</span></span></td>
<td><span data-ttu-id="cb268-200">僅適用于 Alpha 的基本 blend 公式。</span><span class="sxs-lookup"><span data-stu-id="cb268-200">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-luminosity-1.png" alt="Mathematical formula for a luminosity blend effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb268-201">D2D1_BLEND_MODE_DISSOLVE</span><span class="sxs-lookup"><span data-stu-id="cb268-201">D2D1_BLEND_MODE_DISSOLVE</span></span></td>
<td><span data-ttu-id="cb268-202">假設︰</span><span class="sxs-lookup"><span data-stu-id="cb268-202">Given:</span></span>
<ul>
<li><span data-ttu-id="cb268-203">目前圖元的場景座標 XY</span><span class="sxs-lookup"><span data-stu-id="cb268-203">A scene coordinate XY for the current pixel</span></span></li>
<li><span data-ttu-id="cb268-204">具決定性的虛擬亂數產生器 rand (XY) 以種子座標 XY 為基礎，具有 [0，1] 值的非偏誤分佈</span><span class="sxs-lookup"><span data-stu-id="cb268-204">A deterministic pseudo-random number generator rand(XY) based on seed coordinate XY, with unbiased distribution of values from [0, 1]</span></span></li>
</ul>
<br/> <img src="images/blend-mode-dissolve-1.png" alt="Mathematical formula for a dissolve blend effect." /><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb268-205">D2D1_BLEND_MODE_SUBTRACT</span><span class="sxs-lookup"><span data-stu-id="cb268-205">D2D1_BLEND_MODE_SUBTRACT</span></span></td>
<td><span data-ttu-id="cb268-206">僅適用于 Alpha 的基本 blend 公式。</span><span class="sxs-lookup"><span data-stu-id="cb268-206">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-subtract-1.png" alt="Mathematical formula for a subtract blend effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb268-207">D2D1_BLEND_MODE_DIVISION</span><span class="sxs-lookup"><span data-stu-id="cb268-207">D2D1_BLEND_MODE_DIVISION</span></span></td>
<td><span data-ttu-id="cb268-208">僅適用于 Alpha 的基本 blend 公式。</span><span class="sxs-lookup"><span data-stu-id="cb268-208">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-division-1.png" alt="Mathematical formula for a division blend effect." /></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="cb268-209">針對所有 Blend 模式，輸出值會預乘並壓制至範圍 \[ 0，1 \] 。</span><span class="sxs-lookup"><span data-stu-id="cb268-209">For all Blend modes, the output value is premultiplied and clamped to the range \[0, 1\].</span></span>

 

## <a name="hsl-color-space-conversions"></a><span data-ttu-id="cb268-210">HSL 色彩空間轉換</span><span class="sxs-lookup"><span data-stu-id="cb268-210">HSL color space conversions</span></span>

<span data-ttu-id="cb268-211">亮度元件是使用 RGB 加權來計算：</span><span class="sxs-lookup"><span data-stu-id="cb268-211">The luminosity component is computed using the RGB weights here:</span></span>

-   <span data-ttu-id="cb268-212">*k*<sub>R</sub> = 0.30</span><span class="sxs-lookup"><span data-stu-id="cb268-212">*k*<sub>R</sub> = 0.30</span></span>
-   <span data-ttu-id="cb268-213">*k*<sub>G</sub> = 0.59</span><span class="sxs-lookup"><span data-stu-id="cb268-213">*k*<sub>G</sub> = 0.59</span></span>
-   <span data-ttu-id="cb268-214">*k*<sub>B</sub> = 0.11</span><span class="sxs-lookup"><span data-stu-id="cb268-214">*k*<sub>B</sub> = 0.11</span></span>

### <a name="converting-from-rgb-to-hsl"></a><span data-ttu-id="cb268-215">從 RGB 轉換成 HSL</span><span class="sxs-lookup"><span data-stu-id="cb268-215">Converting from RGB to HSL</span></span>

![描述從 rgb 色彩轉換成 hsl 色彩的數學公式。](images/blend-rgb-to-hsl-1.png)

<span data-ttu-id="cb268-217">這會將 *S* 和 *L* 置於範圍 \[ \] -1.0，5.0 的0.0、1.0 和 *H* 範圍中 \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="cb268-217">This places *S* and *L* in the range \[0.0, 1.0\] and *H* in the range \[-1.0, 5.0\].</span></span>

### <a name="converting-from-hsl-to-rgb"></a><span data-ttu-id="cb268-218">從 HSL 轉換成 RGB</span><span class="sxs-lookup"><span data-stu-id="cb268-218">Converting from HSL to RGB</span></span>

<span data-ttu-id="cb268-219">若要轉換成另一種方式，我們使用先前計算的反向。</span><span class="sxs-lookup"><span data-stu-id="cb268-219">To convert the other way we use the inverse of the previous calculations.</span></span>

<span data-ttu-id="cb268-220">If *S* = 0 then *R*  =  *G*  =  *B*  =  *L*</span><span class="sxs-lookup"><span data-stu-id="cb268-220">If *S* = 0 then *R* = *G* = *B* = *L*</span></span>

<span data-ttu-id="cb268-221">否則會有六個與色調相關的案例：</span><span class="sxs-lookup"><span data-stu-id="cb268-221">Otherwise there are six hue-dependant cases:</span></span>

<span data-ttu-id="cb268-222">如果 *H* 大於0，則值位於紅色/洋紅磁區中， *R*  >  *B*  >  *G*。</span><span class="sxs-lookup"><span data-stu-id="cb268-222">If *H* is greater than 0, the values are in the red/magenta sector where *R* > *B* > *G*.</span></span>

![數學 equaiton 將 hsl 色彩轉換成 rgb 的六個步驟之一。](images/blend-hsl-to-rgb-1rm.png)

<span data-ttu-id="cb268-224">如果 *H* 大於或等於0且小於1，則這些值會在 *R*  >  *G*  >  *B* 的紅色/黃色磁區中。</span><span class="sxs-lookup"><span data-stu-id="cb268-224">If *H* is greater than or equal to 0 and less than 1, the values are in the red/yellow sector where *R* > *G* > *B*.</span></span>

![數學 equaiton 將 hsl 色彩轉換成 rgb 的六個步驟。](images/blend-hsl-to-rgb-1ry.png)

<span data-ttu-id="cb268-226">如果 *H* 大於或等於1且小於2，這些值會在黃色/綠色磁區中， *G*  >  *R*  >  *B*。</span><span class="sxs-lookup"><span data-stu-id="cb268-226">If *H* is greater than or equal to 1 and less than 2, the values are in the yellow/green sector where *G* > *R* > *B*.</span></span>

![數學 equaiton 將 hsl 色彩轉換成 rgb 的六個步驟三。](images/blend-hsl-to-rgb-1yg.png)

<span data-ttu-id="cb268-228">如果 *H* 大於或等於2且小於3，則值會在 *G*  >  *B*  >  *R* 的綠色/青色磁區中。</span><span class="sxs-lookup"><span data-stu-id="cb268-228">If *H* is greater than or equal to 2 and less than 3, the values are in the green/cyan sector where *G* > *B* > *R*.</span></span>

![數學 equaiton 將 hsl 色彩轉換成 rgb 的六個步驟四。](images/blend-hsl-to-rgb-1gc.png)

<span data-ttu-id="cb268-230">如果 *H* 大於或等於3且小於4，則值會在青色/藍色磁區中，其中 *B*  >  *G*  >  *R*。</span><span class="sxs-lookup"><span data-stu-id="cb268-230">If *H* is greater than or equal to 3 and less than 4, the values are in the cyan/blue sector where *B* > *G* > *R*.</span></span>

![數學 equaiton 將 hsl 色彩轉換為 rgb 的五個步驟五。](images/blend-hsl-to-rgb-1cb.png)

<span data-ttu-id="cb268-232">如果 *H* 大於或等於4，則值會在藍色/洋紅磁區中（ *B*  >  *R*  >  *G*）。</span><span class="sxs-lookup"><span data-stu-id="cb268-232">If *H* is greater than or equal to 4, the values are in the blue/magenta sector where *B* > *R* > *G*.</span></span>

![數學 equaiton 將 hsl 色彩轉換為 rgb 的步驟六。](images/blend-hsl-to-rgb-1bm.png)

<span data-ttu-id="cb268-234">由於混合模式會從兩個不同的色彩建立任意的 HSL 元件組合，因此轉換的 RGB 值通常不會超出範圍，也就是一或多個通道元件可能超出 \[ 0.0、1.0 的法律範圍 \] 。</span><span class="sxs-lookup"><span data-stu-id="cb268-234">Because the blending modes make arbitrary combinations of HSL components from two different colors, it is common for the converted RGB value to be out-of-gamut, that is, one or more channel components may be outside the legal range of \[0.0, 1.0\].</span></span> <span data-ttu-id="cb268-235">這些色彩會透過降低飽和度的最小程度來帶回範圍，同時保留色調和亮度：</span><span class="sxs-lookup"><span data-stu-id="cb268-235">These colors are brought back into gamut by minimally reducing the saturation, while preserving both hue and luminosity:</span></span>

![數學公式，描述超出範圍實例所需的更正。](images/blend-gamut-correction.png)

## <a name="output-bitmap"></a><span data-ttu-id="cb268-237">輸出點陣圖</span><span class="sxs-lookup"><span data-stu-id="cb268-237">Output bitmap</span></span>

<span data-ttu-id="cb268-238">這個效果的輸出點陣圖一律是兩個輸入影像的聯集大小。</span><span class="sxs-lookup"><span data-stu-id="cb268-238">The output bitmap for this effect is always the size of the union of the two input images.</span></span>

## <a name="sample-code"></a><span data-ttu-id="cb268-239">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="cb268-239">Sample code</span></span>

<span data-ttu-id="cb268-240">如需此效果的範例，請下載 [Direct2D 複合效果模式範例](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample)。</span><span class="sxs-lookup"><span data-stu-id="cb268-240">For an example of this effect, download the [Direct2D composite effect modes sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample).</span></span>

## <a name="requirements"></a><span data-ttu-id="cb268-241">規格需求</span><span class="sxs-lookup"><span data-stu-id="cb268-241">Requirements</span></span>



| <span data-ttu-id="cb268-242">需求</span><span class="sxs-lookup"><span data-stu-id="cb268-242">Requirement</span></span> | <span data-ttu-id="cb268-243">值</span><span class="sxs-lookup"><span data-stu-id="cb268-243">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cb268-244">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cb268-244">Minimum supported client</span></span> | <span data-ttu-id="cb268-245">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cb268-245">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="cb268-246">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cb268-246">Minimum supported server</span></span> | <span data-ttu-id="cb268-247">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cb268-247">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="cb268-248">標頭</span><span class="sxs-lookup"><span data-stu-id="cb268-248">Header</span></span>                   | <span data-ttu-id="cb268-249">d2d1effects。h</span><span class="sxs-lookup"><span data-stu-id="cb268-249">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="cb268-250">程式庫</span><span class="sxs-lookup"><span data-stu-id="cb268-250">Library</span></span>                  | <span data-ttu-id="cb268-251">d2d1 .lib，dxguid .lib</span><span class="sxs-lookup"><span data-stu-id="cb268-251">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="cb268-252">相關主題</span><span class="sxs-lookup"><span data-stu-id="cb268-252">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb268-253">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="cb268-253">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

