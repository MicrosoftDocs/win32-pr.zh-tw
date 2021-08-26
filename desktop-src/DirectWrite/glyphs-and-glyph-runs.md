---
title: 字元和圖像執行
description: 字元和圖像執行可在 DirectWrite API 的最底層功能（圖像呈現層）上取得。
ms.assetid: e670cb65-1fcb-46fd-ac0b-02eaaaa51996
keywords:
- DirectWrite，字型
- DirectWrite，圖像執行
- 圖像執行
- 圖像
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b39d1ca47249adf11f4e1e2072620f24553f7e299e0690c1cc147c4f74a4939f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902914"
---
# <a name="glyphs-and-glyph-runs"></a>字元和圖像執行

字元和圖像執行可在[DirectWrite](direct-write-portal.md) API 的最底層功能（圖像呈現層）上取得。

## <a name="glyphs"></a>字符

圖像是指定字型中字元的實體標記法。 字元可能有許多字元，而系統上的每個字型可能會為該字元定義不同的圖像。

有兩個或多個字元也可以合併成單一圖像，這個程式稱為「圖像撰寫」。 這也可以在相反的方向進行，也就是將單一圖像分割成多個字元，稱為「圖像分解」。

### <a name="alternate-glyphs"></a>替代字元

字型可提供字元的替代字元，例如 Pericles OpenType 字型的樣式替代圖像，如下列螢幕擷取畫面所示。 ' A '、' E ' 和 ' O ' 字元會以樣式替代字元轉譯。

!["古綠神話" 的螢幕擷取畫面，其中包含使用替代字元的 "a"、"e" 和 "o"](images/opentypealternateglyphs.png)

替代符號的另一個範例是花飾字字元。 下列螢幕擷取畫面顯示 Pescadero 字型的標準和花飾字型。

![標準和花飾字字元中字母 "a" 到 "n" 的螢幕擷取畫面](images/opentypeswashstandard.png)

您可以透過 [OpenType](../intl/opentype-font-format.md)使用花飾字元和其他印刷樣式功能，包括更詳盡的替代字元。 您可以使用 [**IDWriteTextLayout：： SetTypography**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-settypography) ，並傳遞與所需功能相關聯的 [**DWRITE \_ 字型 \_ 功能 \_ 標記**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_feature_tag) 列舉常數，將 OpenType 印刷樣式功能套用至文字範圍。

## <a name="glyph-runs"></a>圖像執行

圖像執行代表一組連續的圖像，這些字型全都具有相同的字型和大小，以及相同的用戶端繪製效果（如果有的話）。 底線和刪除線不是套用至文字範圍之圖像執行的一部分，而且會在稍後繪製。 内嵌物件（例如影像）也會分開繪製，因為它們不是字型的一部分。

### <a name="the-idwritefontface-interface"></a>IDWriteFontFace 介面

[DirectWrite](direct-write-portal.md)使用與 Windows Pesentation Foundation (WPF) 相同的字型分類系統，因此每個字型系列都可以有多個實體字型。 字型，例如 DirectWrite 中的 [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)介面，代表具有特定權數、斜面和延展的實體字型。 其中包含字型類型、適當的檔案參考、臉部辨識資料和各種字型資料，例如度量、名稱和圖像外框。

[**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)可以直接從字型名稱建立，或從字型集合中取得。

### <a name="glyph-metrics"></a>字符度量

個別的字元具有與其相關聯的度量。 您可以使用 [**IDWriteFontFace：： GetDesignGlyphMetrics**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getdesignglyphmetrics) 方法，取得圖像執行中所有字元的度量。 這會傳回 DWRITE 圖像指標結構，此結構具有預先的寬度、左右側邊、頂端和底部的關聯、高度和垂直基準原點。 [**\_ \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics)

下圖顯示兩個不同字元字元的各種計量。

![兩個不同字元的度量圖表](images/twoglyphs.png)

## <a name="drawing-a-glyph-run"></a>繪製圖像執行

在執行自訂文字轉譯器時，圖像的轉譯是由 [**IDWriteTextRenderer：:D rawglyphrun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun)處理，這是您實作為衍生自 [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer)之類別一部分的回呼方法。 傳遞至 [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun)的 [**DWRITE 圖像 \_ \_ 執行**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run)結構包含名為 *fontFace* 的 [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)物件，代表整個圖像執行的字型。

[**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)物件也會提供 [**GetGlyphRunOutline**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphrunoutline)方法，其會使用指定的幾何接收回呼（例如使用 [Direct2D](../direct2d/direct2d-portal.md)轉譯時的 [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) ）來計算圖像大綱。

如需詳細資訊，請參閱 [如何執行自訂文字](how-to-implement-a-custom-text-renderer.md) 轉譯器主題。

 

 