---
title: 自訂功能區色彩
description: Windows 功能區架構會公開一組色彩屬性，讓應用程式在執行時間自訂各種功能區 UI 元素的外觀。
ms.assetid: e070aaca-d350-4336-8e5d-d5d9c8167287
keywords:
- Windows 功能區，自訂色彩
- 功能區、自訂色彩
- 自訂 Windows 功能區色彩
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55ff6527dc67ee18df4723fc33e4b764e20127e8
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "103681489"
---
# <a name="customizing-ribbon-colors"></a><span data-ttu-id="781c4-106">自訂功能區色彩</span><span class="sxs-lookup"><span data-stu-id="781c4-106">Customizing Ribbon Colors</span></span>

<span data-ttu-id="781c4-107">Windows 功能區架構會公開一組色彩屬性，讓應用程式在執行時間自訂各種功能區 UI 元素的外觀。</span><span class="sxs-lookup"><span data-stu-id="781c4-107">The Windows Ribbon framework exposes a set of color properties that allow an application to customize the appearance of various Ribbon UI elements at run time.</span></span>

-   [<span data-ttu-id="781c4-108">簡介</span><span class="sxs-lookup"><span data-stu-id="781c4-108">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="781c4-109">指定功能區色彩</span><span class="sxs-lookup"><span data-stu-id="781c4-109">Specify Ribbon Colors</span></span>](#specify-ribbon-colors)
-   [<span data-ttu-id="781c4-110">將 RGB 轉換成 HSB</span><span class="sxs-lookup"><span data-stu-id="781c4-110">Convert RGB to HSB</span></span>](#convert-rgb-to-hsb)
-   [<span data-ttu-id="781c4-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="781c4-111">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="781c4-112">簡介</span><span class="sxs-lookup"><span data-stu-id="781c4-112">Introduction</span></span>

<span data-ttu-id="781c4-113">下表所列的 [framework 屬性索引鍵](windowsribbon-reference-properties-framework.md) 可用來設定功能區應用程式中各種 UI 元素的色彩。</span><span class="sxs-lookup"><span data-stu-id="781c4-113">The [framework property keys](windowsribbon-reference-properties-framework.md) listed in the following table are used to set the color of various UI elements in a Ribbon application.</span></span> <span data-ttu-id="781c4-114">這些屬性可讓功能區架構支援跨應用程式的個人化、身分識別需求和商標規格。</span><span class="sxs-lookup"><span data-stu-id="781c4-114">These properties allow the Ribbon framework to support personalization, identity requirements, and branding specifications across applications.</span></span>

| <span data-ttu-id="781c4-115">功能區色彩</span><span class="sxs-lookup"><span data-stu-id="781c4-115">Ribbon Color</span></span>                     | <span data-ttu-id="781c4-116">Framework 屬性索引鍵</span><span class="sxs-lookup"><span data-stu-id="781c4-116">Framework Property Key</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="781c4-117">背景色彩</span><span class="sxs-lookup"><span data-stu-id="781c4-117">Background color</span></span>                 | [<span data-ttu-id="781c4-118">UI \_ PKEY \_ GlobalBackgroundColor</span><span class="sxs-lookup"><span data-stu-id="781c4-118">UI\_PKEY\_GlobalBackgroundColor</span></span>](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md)                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="781c4-119">僅將色彩醒目提示 (Windows 7) </span><span class="sxs-lookup"><span data-stu-id="781c4-119">Highlight color (Windows 7 only)</span></span> | <span data-ttu-id="781c4-120">[UI \_Windows 8 \_ ](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md)\* \*： \* \* [ui \_ PKEY \_ GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) 中引進的 PKEY GlobalHighlightColor \* \* \* 無法獨立于 [ui \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md)之外進行設定。</span><span class="sxs-lookup"><span data-stu-id="781c4-120">[UI\_PKEY\_GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md)\*\*\*\*Introduced in Windows 8\*\*:  \*\* [UI\_PKEY\_GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) cannot be set independently of [UI\_PKEY\_GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md).</span></span><br/> <br/>                                                              |
| <span data-ttu-id="781c4-121">文字色彩</span><span class="sxs-lookup"><span data-stu-id="781c4-121">Text color</span></span>                       | <span data-ttu-id="781c4-122">[UI \_PKEY \_ GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md)\* \* \* \* 在 Windows 8 引進 **：** Windows 8 中 [ui \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md) 的預設值變更，可能需要在針對 Windows 7 設計的功能區應用程式中調整 [ui \_ PKEY \_ GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md) 。</span><span class="sxs-lookup"><span data-stu-id="781c4-122">[UI\_PKEY\_GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md)\*\*\*\*Introduced in Windows 8 **:** Changes to the default value of [UI\_PKEY\_GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md) in Windows 8 might require an adjustment to [UI\_PKEY\_GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md) in Ribbon apps designed for Windows 7.</span></span><br/> <br/> |



 

## <a name="specify-ribbon-colors"></a><span data-ttu-id="781c4-123">指定功能區色彩</span><span class="sxs-lookup"><span data-stu-id="781c4-123">Specify Ribbon Colors</span></span>

<span data-ttu-id="781c4-124">功能區架構會使用色調、飽和度、亮度 (HSB) 色彩模型，其不同于較常見的色調、飽和度、亮度 (HSL) 或色調、飽和度、值 (HSV) 色彩空間。</span><span class="sxs-lookup"><span data-stu-id="781c4-124">The Ribbon framework uses a Hue, Saturation, Brightness (HSB) color model, which differs from the more common hue, saturation, luminosity (HSL) or hue, saturation, value (HSV) color spaces.</span></span> <span data-ttu-id="781c4-125">尤其是 B 代表整體的亮度或亮度層級，而不是特定色彩的亮度。</span><span class="sxs-lookup"><span data-stu-id="781c4-125">In particular, B represents an overall brightness or luminosity level rather than the lightness of a particular color.</span></span>

<span data-ttu-id="781c4-126">若要在功能區架構中指定 UI 元素的色彩，應用程式會將 HSB 值指派給每個全域色彩屬性。</span><span class="sxs-lookup"><span data-stu-id="781c4-126">To specify the color of UI elements in the Ribbon framework, an application assigns HSB values to each of the global color properties.</span></span> <span data-ttu-id="781c4-127">然後，這些值會在功能區應用程式所需的所有功能區專案中通用套用 (架構不支援將 HSB 值指派給個別元素和控制項) 。</span><span class="sxs-lookup"><span data-stu-id="781c4-127">These values are then applied universally across all Ribbon elements as required by the Ribbon application (the framework does not support assigning HSB values to individual elements and controls).</span></span>

<span data-ttu-id="781c4-128">在 Windows 8 \* \*： \* \*[ui \_ PKEY \_ GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) 中引進，指派的值與 [ui \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md)相同。</span><span class="sxs-lookup"><span data-stu-id="781c4-128">\*\*\*\*Introduced in Windows 8\*\*:  \*\*[UI\_PKEY\_GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) is assigned the same value as [UI\_PKEY\_GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md).</span></span>

<span data-ttu-id="781c4-129">下表描述功能區架構 HSB 參數。</span><span class="sxs-lookup"><span data-stu-id="781c4-129">The following table describes the Ribbon framework HSB parameters.</span></span>



<span data-ttu-id="781c4-130">元件</span><span class="sxs-lookup"><span data-stu-id="781c4-130">Component</span></span>

<span data-ttu-id="781c4-131">描述</span><span class="sxs-lookup"><span data-stu-id="781c4-131">Description</span></span>

<span data-ttu-id="781c4-132">調整的值\*</span><span class="sxs-lookup"><span data-stu-id="781c4-132">Adjusted Values\*</span></span>

<span data-ttu-id="781c4-133">色調 (H) </span><span class="sxs-lookup"><span data-stu-id="781c4-133">Hue (H)</span></span>

<span data-ttu-id="781c4-134">Pigment （或實際的色彩）通常會識別為介於0到359度的 circlular 範圍內的值。</span><span class="sxs-lookup"><span data-stu-id="781c4-134">The pigment, or actual, color is typically identified as a value from a circlular range of 0 to 359 degrees.</span></span>

<span data-ttu-id="781c4-135">0 (紅色) 至 255 (紅色) </span><span class="sxs-lookup"><span data-stu-id="781c4-135">0 (red) to 255 (red)</span></span>

<span data-ttu-id="781c4-136">飽和度 (S) </span><span class="sxs-lookup"><span data-stu-id="781c4-136">Saturation (S)</span></span>

<span data-ttu-id="781c4-137">以百分比表示的色彩的純度或飽和度，從0到100%。</span><span class="sxs-lookup"><span data-stu-id="781c4-137">The purity, or saturation, of the color measured as a percentage from 0 to 100%.</span></span>

<span data-ttu-id="781c4-138">0 (灰色) 255 (完全飽和) </span><span class="sxs-lookup"><span data-stu-id="781c4-138">0 (grey) to 255 (fully saturated)</span></span>

<span data-ttu-id="781c4-139">亮度 (B) </span><span class="sxs-lookup"><span data-stu-id="781c4-139">Brightness (B)</span></span>

<span data-ttu-id="781c4-140">色彩的整體亮度或暗度，以從0到100% 的百分比表示。</span><span class="sxs-lookup"><span data-stu-id="781c4-140">The overall brightness or darkness of the color measured as a percentage from 0 to 100%.</span></span>

<span data-ttu-id="781c4-141">0 (深色) 至 255 (light) </span><span class="sxs-lookup"><span data-stu-id="781c4-141">0 (dark) to 255 (light)</span></span>

<span data-ttu-id="781c4-142">\* 針對架構，每個參數值的原始範圍會轉譯為0到255的範圍。</span><span class="sxs-lookup"><span data-stu-id="781c4-142">\* The original range for each parameter value is translated into a range of 0 to 255 for the framework.</span></span>



 

<span data-ttu-id="781c4-143">HSB 值不會識別特定的色彩。</span><span class="sxs-lookup"><span data-stu-id="781c4-143">HSB values do not identify specific colors.</span></span> <span data-ttu-id="781c4-144">相反地，HSB 屬性值的組合會影響整個 UI 中色彩漸層的色彩漸層相對於彼此的調整方式。</span><span class="sxs-lookup"><span data-stu-id="781c4-144">Instead, the combination of HSB property values influences how color gradients throughout the UI are adjusted relative to each other.</span></span>

<span data-ttu-id="781c4-145">將自訂 HSB 值指派給 [UI \_ PKEY \_ GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md) 和 [ui \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md)時，建議將這些值設為夠高的對比，以確保可讀性。</span><span class="sxs-lookup"><span data-stu-id="781c4-145">When assigning custom HSB values to [UI\_PKEY\_GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md) and [UI\_PKEY\_GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md), it is recommended that these values be of high enough contrast to ensure readability.</span></span> <span data-ttu-id="781c4-146">具體而言，文字色彩應該比功能區 UI 的最亮陰影更深色。</span><span class="sxs-lookup"><span data-stu-id="781c4-146">Specifically, the text color should be darker than the lightest shade of the ribbon UI.</span></span> <span data-ttu-id="781c4-147">在必要時，架構會自動調整 UI \_ PKEY \_ GlobalTextColor HSB 值，以提供與任何衍生自 UI PKEY GlobalBackgroundColor 之背景陰影或漸層的足夠對比 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="781c4-147">Where necessary, the framework automatically adjusts the UI\_PKEY\_GlobalTextColor HSB value to provide sufficient contrast against any background shade or gradient derived from UI\_PKEY\_GlobalBackgroundColor.</span></span>

> [!Note]  
> <span data-ttu-id="781c4-148">在 Windows 7 中， [ui \_ PKEY \_ GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) 可以獨立于 [ui \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md)之外進行設定。</span><span class="sxs-lookup"><span data-stu-id="781c4-148">In Windows 7, [UI\_PKEY\_GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) can be set independently of [UI\_PKEY\_GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md).</span></span>

 

<span data-ttu-id="781c4-149">下列範例示範如何為 [ui \_ PKEY \_ GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md)、 [ui \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md)和 [ui \_ PKEY \_ GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) 屬性指定自訂色彩。</span><span class="sxs-lookup"><span data-stu-id="781c4-149">The following example demonstrates how to specify a custom color for the [UI\_PKEY\_GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md), [UI\_PKEY\_GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md), and [UI\_PKEY\_GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) properties.</span></span>


```C++
CComPtr<IPropertyStore> spPropertyStore;

// _spFramework is a pointer to the IUIFramework interface that is assigned 
// when the Ribbon is initialized.
if (SUCCEEDED(_spFramework->QueryInterface(&spPropertyStore)))
{
  PROPVARIANT propvarBackground;
  PROPVARIANT propvarHighlight;
  PROPVARIANT propvarText;
 
  // UI_HSBCOLOR is a type defined in UIRibbon.h that is composed of 
  // three component values: hue, saturation and brightness, respectively.
  UI_HSBCOLOR BackgroundColor = UI_HSB(0x14, 0x38, 0x54);
  UI_HSBCOLOR HighlightColor = UI_HSB(0x00, 0x36, 0x87);
  UI_HSBCOLOR TextColor = UI_HSB(0x2B, 0xD6, 0x00);

  InitPropVariantFromUInt32(BackgroundColor, &propvarBackground);
  InitPropVariantFromUInt32(HighlightColor, &propvarHighlight);
  InitPropVariantFromUInt32(TextColor, &propvarText);
 
  spPropertyStore->SetValue(UI_PKEY_GlobalBackgroundColor, propvarBackground);
  spPropertyStore->SetValue(UI_PKEY_GlobalTextColor, propvarText);
 
  spPropertyStore->Commit();
}
```



## <a name="convert-rgb-to-hsb"></a><span data-ttu-id="781c4-150">將 RGB 轉換成 HSB</span><span class="sxs-lookup"><span data-stu-id="781c4-150">Convert RGB to HSB</span></span>

<span data-ttu-id="781c4-151">本節說明將功能區架構 HSB 值（在此範例中為 [UI \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md) ）動態比對在執行時間的特定 RGB 色彩所需的公式。</span><span class="sxs-lookup"><span data-stu-id="781c4-151">This section describes the formula that is required for dynamically matching a Ribbon framework HSB value, the [UI\_PKEY\_GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md) in this example, to a specific RGB color at run time.</span></span>

<span data-ttu-id="781c4-152">索引標籤資料列背景會當做參考點使用，因為它會轉譯為平面色彩介面，相較于功能區背景的亮度漸層。</span><span class="sxs-lookup"><span data-stu-id="781c4-152">The tab row background is used as a reference point because it is rendered as a flat color surface compared to the brightness gradient of the ribbon background.</span></span>

<span data-ttu-id="781c4-153">需要初步轉換才能取得中繼 HSL 值。</span><span class="sxs-lookup"><span data-stu-id="781c4-153">A preliminary conversion is necessary to obtain an intermediate HSL value.</span></span> <span data-ttu-id="781c4-154">這個 HSL 值接著可以轉換成 HSB 值。</span><span class="sxs-lookup"><span data-stu-id="781c4-154">This HSL value can then be converted to an HSB value.</span></span>

> [!Note]  
> <span data-ttu-id="781c4-155">使用大部分的相片編輯軟體，可輕鬆地完成從 RGB 到 HSL 的轉換。</span><span class="sxs-lookup"><span data-stu-id="781c4-155">The conversion from RGB to HSL is easily accomplished with most photo editing software.</span></span>

 

<span data-ttu-id="781c4-156">從0.0 到 1.0) 範圍中的每個元件轉換 HSL (，到功能區 HSB 設定都是透過下列公式完成：</span><span class="sxs-lookup"><span data-stu-id="781c4-156">Conversion of HSL (with each component in the range of 0.0 to 1.0) to a Ribbon HSB setting is accomplished through the following formulas:</span></span>

-   <span data-ttu-id="781c4-157">H<sub>background</sub> = Round (255.0 H) </span><span class="sxs-lookup"><span data-stu-id="781c4-157">H<sub>background</sub> = Round(255.0 H)</span></span>
-   <span data-ttu-id="781c4-158">S<sub>背景</sub> = 四捨五入 (255.0 S) </span><span class="sxs-lookup"><span data-stu-id="781c4-158">S<sub>background</sub> = Round(255.0 S)</span></span>
-   <span data-ttu-id="781c4-159">B<sub>背景</sub> = 四捨五入 (257.7 + 149.9 Ln (L) ) if 0.1793 <= L <= 0.9821</span><span class="sxs-lookup"><span data-stu-id="781c4-159">B<sub>background</sub> = Round(257.7 + 149.9 ln(L)) if 0.1793 <= L <= 0.9821</span></span>

## <a name="related-topics"></a><span data-ttu-id="781c4-160">相關主題</span><span class="sxs-lookup"><span data-stu-id="781c4-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="781c4-161">色彩指導方針</span><span class="sxs-lookup"><span data-stu-id="781c4-161">Color Guidelines</span></span>](https://msdn.microsoft.com/library/aa511283.aspx)
</dt> <dt>

[<span data-ttu-id="781c4-162">架構屬性</span><span class="sxs-lookup"><span data-stu-id="781c4-162">Framework Properties</span></span>](windowsribbon-reference-properties-framework.md)
</dt> </dl>

 

 





