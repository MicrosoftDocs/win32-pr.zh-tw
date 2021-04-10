---
title: 字元和圖像執行
description: 圖像和圖像執行可在 DirectWrite API 的最底層功能（圖像呈現層）上取得。
ms.assetid: e670cb65-1fcb-46fd-ac0b-02eaaaa51996
keywords:
- DirectWrite，字型
- DirectWrite，圖像執行
- 圖像執行
- 圖像
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32c5c6b30c9a44cde4704e6afd231cebbc91d2be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092840"
---
# <a name="glyphs-and-glyph-runs"></a><span data-ttu-id="24d26-107">字元和圖像執行</span><span class="sxs-lookup"><span data-stu-id="24d26-107">Glyphs and Glyph Runs</span></span>

<span data-ttu-id="24d26-108">圖像和圖像執行可在 [DirectWrite](direct-write-portal.md) API 的最底層功能（圖像呈現層）上取得。</span><span class="sxs-lookup"><span data-stu-id="24d26-108">Glyphs and glyph runs are available at the lowest layer of functionality of the [DirectWrite](direct-write-portal.md) API, the glyph-rendering layer.</span></span>

## <a name="glyphs"></a><span data-ttu-id="24d26-109">字符</span><span class="sxs-lookup"><span data-stu-id="24d26-109">Glyphs</span></span>

<span data-ttu-id="24d26-110">圖像是指定字型中字元的實體標記法。</span><span class="sxs-lookup"><span data-stu-id="24d26-110">A glyph is a physical representation of a character in a given font.</span></span> <span data-ttu-id="24d26-111">字元可能有許多字元，而系統上的每個字型可能會為該字元定義不同的圖像。</span><span class="sxs-lookup"><span data-stu-id="24d26-111">Characters might have many glyphs, with each font on a system potentially defining a different glyph for that character.</span></span>

<span data-ttu-id="24d26-112">有兩個或多個字元也可以合併成單一圖像，這個程式稱為「圖像撰寫」。</span><span class="sxs-lookup"><span data-stu-id="24d26-112">Two or more glyphs can also be combined into a single glyph, this process is called glyph composition.</span></span> <span data-ttu-id="24d26-113">這也可以在相反的方向進行，也就是將單一圖像分割成多個字元，稱為「圖像分解」。</span><span class="sxs-lookup"><span data-stu-id="24d26-113">This can also be done in the opposite direction, a single glyph being split into multiple glyphs, known as glyph decomposition.</span></span>

### <a name="alternate-glyphs"></a><span data-ttu-id="24d26-114">替代字元</span><span class="sxs-lookup"><span data-stu-id="24d26-114">Alternate Glyphs</span></span>

<span data-ttu-id="24d26-115">字型可提供字元的替代字元，例如 Pericles OpenType 字型的樣式替代圖像，如下列螢幕擷取畫面所示。</span><span class="sxs-lookup"><span data-stu-id="24d26-115">Fonts may provide alternate glyphs for characters, such as the stylistic alternate glyphs for the Pericles OpenType font, as shown in the following screen shot.</span></span> <span data-ttu-id="24d26-116">' A '、' E ' 和 ' O ' 字元會以樣式替代字元轉譯。</span><span class="sxs-lookup"><span data-stu-id="24d26-116">The 'A', 'E', and 'O' characters are rendered with stylistic alternate glyphs.</span></span>

!["古綠神話" 的螢幕擷取畫面，其中包含使用替代字元的 "a"、"e" 和 "o"](images/opentypealternateglyphs.png)

<span data-ttu-id="24d26-118">替代符號的另一個範例是花飾字字元。</span><span class="sxs-lookup"><span data-stu-id="24d26-118">Another example of alternate glyphs are swash glyphs.</span></span> <span data-ttu-id="24d26-119">下列螢幕擷取畫面顯示 Pescadero 字型的標準和花飾字型。</span><span class="sxs-lookup"><span data-stu-id="24d26-119">The following screen shot shows standard and swash glyphs for the Pescadero font.</span></span>

![標準和花飾字字元中字母 "a" 到 "n" 的螢幕擷取畫面](images/opentypeswashstandard.png)

<span data-ttu-id="24d26-121">您可以透過 [OpenType](../intl/opentype-font-format.md)使用花飾字元和其他印刷樣式功能，包括更詳盡的替代字元。</span><span class="sxs-lookup"><span data-stu-id="24d26-121">Swashes and other typographic features, including more elaborate alternate glyphs, are available through [OpenType](../intl/opentype-font-format.md).</span></span> <span data-ttu-id="24d26-122">您可以使用 [**IDWriteTextLayout：： SetTypography**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-settypography) ，並傳遞與所需功能相關聯的 [**DWRITE \_ 字型 \_ 功能 \_ 標記**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_feature_tag) 列舉常數，將 OpenType 印刷樣式功能套用至文字範圍。</span><span class="sxs-lookup"><span data-stu-id="24d26-122">OpenType typographic features can be applied to a text range by using the [**IDWriteTextLayout::SetTypography**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-settypography) and passing the [**DWRITE\_FONT\_FEATURE\_TAG**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_feature_tag) enumeration constant associated with the desired feature.</span></span>

## <a name="glyph-runs"></a><span data-ttu-id="24d26-123">圖像執行</span><span class="sxs-lookup"><span data-stu-id="24d26-123">Glyph Runs</span></span>

<span data-ttu-id="24d26-124">圖像執行代表一組連續的圖像，這些字型全都具有相同的字型和大小，以及相同的用戶端繪製效果（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="24d26-124">A glyph run represents a contiguous set of glyphs that all have the same font face and size, as well as the same client drawing effect, if any.</span></span> <span data-ttu-id="24d26-125">底線和刪除線不是套用至文字範圍之圖像執行的一部分，而且會在稍後繪製。</span><span class="sxs-lookup"><span data-stu-id="24d26-125">Underline and strikethrough are not part of the glyph run for the text range they are applied to, and are drawn later.</span></span> <span data-ttu-id="24d26-126">内嵌物件（例如影像）也會分開繪製，因為它們不是字型的一部分。</span><span class="sxs-lookup"><span data-stu-id="24d26-126">Inline objects, such as images, are also drawn separately, as they are not part of a font.</span></span>

### <a name="the-idwritefontface-interface"></a><span data-ttu-id="24d26-127">IDWriteFontFace 介面</span><span class="sxs-lookup"><span data-stu-id="24d26-127">The IDWriteFontFace Interface</span></span>

<span data-ttu-id="24d26-128">[DirectWrite](direct-write-portal.md) 使用與 Windows Pesentation FOUNDATION (WPF) 相同的字型分類系統，因此每個字型系列可能會有多個實體字型。</span><span class="sxs-lookup"><span data-stu-id="24d26-128">[DirectWrite](direct-write-portal.md) uses the same system for font classification as Windows Pesentation Foundation (WPF), so there can be multiple physical fonts per each font family.</span></span> <span data-ttu-id="24d26-129">字型，例如 DirectWrite 中的 [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) 介面，代表具有特定權數、斜面和延展的實體字型。</span><span class="sxs-lookup"><span data-stu-id="24d26-129">A font face, such as the [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) interface in DirectWrite, represents a physical font, with a specific weight, slant, and stretch.</span></span> <span data-ttu-id="24d26-130">其中包含字型類型、適當的檔案參考、臉部辨識資料和各種字型資料，例如度量、名稱和圖像外框。</span><span class="sxs-lookup"><span data-stu-id="24d26-130">It contains the font face type, appropriate file references, face identification data and various font data such as metrics, names and glyph outlines.</span></span>

<span data-ttu-id="24d26-131">[**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)可以直接從字型名稱建立，或從字型集合中取得。</span><span class="sxs-lookup"><span data-stu-id="24d26-131">The [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) can be created directly from a font name or obtained from a font collection.</span></span>

### <a name="glyph-metrics"></a><span data-ttu-id="24d26-132">字符度量</span><span class="sxs-lookup"><span data-stu-id="24d26-132">Glyph Metrics</span></span>

<span data-ttu-id="24d26-133">個別的字元具有與其相關聯的度量。</span><span class="sxs-lookup"><span data-stu-id="24d26-133">Individual glyphs have metrics associated with them.</span></span> <span data-ttu-id="24d26-134">您可以使用 [**IDWriteFontFace：： GetDesignGlyphMetrics**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getdesignglyphmetrics) 方法，取得圖像執行中所有字元的度量。</span><span class="sxs-lookup"><span data-stu-id="24d26-134">You can obtain the metrics for all of the glyphs in a glyph run by using the [**IDWriteFontFace::GetDesignGlyphMetrics**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getdesignglyphmetrics) method.</span></span> <span data-ttu-id="24d26-135">這會傳回 DWRITE 圖像指標結構，此結構具有預先的寬度、左右側邊、頂端和底部的關聯、高度和垂直基準原點。 [**\_ \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics)</span><span class="sxs-lookup"><span data-stu-id="24d26-135">This returns a [**DWRITE\_GLYPH\_METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics) structure that has the advance width, the left and right side bearing, the top and bottom side bearing, the height and the vertical baseline origin.</span></span>

<span data-ttu-id="24d26-136">下圖顯示兩個不同字元字元的各種計量。</span><span class="sxs-lookup"><span data-stu-id="24d26-136">The following diagram shows various metrics of two different glyph characters.</span></span>

![兩個不同字元的度量圖表](images/twoglyphs.png)

## <a name="drawing-a-glyph-run"></a><span data-ttu-id="24d26-138">繪製圖像執行</span><span class="sxs-lookup"><span data-stu-id="24d26-138">Drawing a Glyph Run</span></span>

<span data-ttu-id="24d26-139">在執行自訂文字轉譯器時，圖像的轉譯是由 [**IDWriteTextRenderer：:D rawglyphrun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun)處理，這是您實作為衍生自 [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer)之類別一部分的回呼方法。</span><span class="sxs-lookup"><span data-stu-id="24d26-139">When implementing a custom text renderer, the rendering of glyphs is handled by the [**IDWriteTextRenderer::DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), a callback method that you implement as part of a class derived from [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer).</span></span> <span data-ttu-id="24d26-140">傳遞至 [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun)的 [**DWRITE 圖像 \_ \_ 執行**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run)結構包含名為 *fontFace* 的 [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)物件，代表整個圖像執行的字型。</span><span class="sxs-lookup"><span data-stu-id="24d26-140">The [**DWRITE\_GLYPH\_RUN**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) structure that is passed to [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) contains a [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) object, named *fontFace*, that represents the font face for the entire glyph run.</span></span>

<span data-ttu-id="24d26-141">[**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)物件也會提供 [**GetGlyphRunOutline**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphrunoutline)方法，其會使用指定的幾何接收回呼（例如使用 [Direct2D](../direct2d/direct2d-portal.md)轉譯時的 [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) ）來計算圖像大綱。</span><span class="sxs-lookup"><span data-stu-id="24d26-141">The [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) object also provides the [**GetGlyphRunOutline**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphrunoutline) method, which computes the glyph outlines by using a specified geometry sink callback, such as [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) when rendering with [Direct2D](../direct2d/direct2d-portal.md).</span></span>

<span data-ttu-id="24d26-142">如需詳細資訊，請參閱 [如何執行自訂文字](how-to-implement-a-custom-text-renderer.md) 轉譯器主題。</span><span class="sxs-lookup"><span data-stu-id="24d26-142">For more information, see the [How to Implement a Custom Text Renderer](how-to-implement-a-custom-text-renderer.md) topic.</span></span>

 

 