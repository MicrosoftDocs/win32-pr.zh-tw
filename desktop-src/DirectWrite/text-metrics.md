---
title: 文字度量
description: 為了協助您的版面配置、自訂字型選取，以及其他需要大量計量的作業，從 Windows 8 開始，DirectWrite 有許多新的 Api，可表達您開發 rich text 應用程式時可能需要的字型相關資訊。
ms.assetid: 9df8c675-6f4d-4de7-916e-7dc51f5f04aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73647ae4521b23afb399a4c66c8b25cdc46ba1b5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106996566"
---
# <a name="text-metrics"></a>文字度量

為了協助您的版面配置、自訂字型選取，以及其他需要大量計量的作業，從 Windows 8 開始， [DirectWrite](direct-write-portal.md) 有許多新的 api，可表達您開發 rich text 應用程式時可能需要的字型相關資訊。

## <a name="panose"></a>PANOSE

PANOSE 是用來識別字體的視覺化分類系統。 PANOSE 分類包含系列、serif 樣式、權數、比例、對比、筆劃、arm 樣式、X 高度等等的資訊。此資訊描述字型的視覺化樣式。 這項資訊很重要，因為具有類似 PANOSE 值的字型看起來類似。 當字型無法使用，而且應用程式必須切換回可用的字型時，這非常有用。 比較字型的 PANOSE 值，可讓您選擇視覺效果與原始字型類似的字型。

為了存取字型的 PANOSE 資訊，請在 [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1)和 [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1)介面上使用 [**GetPanose**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefont1-getpanose)方法。 這個方法會傳回 [**DWRITE \_ PANOSE**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_panose) 列舉，其中包含該字型的所有 PANOSE 資訊。

## <a name="additional-metrics"></a>其他計量

從 Windows 8 開始， [DirectWrite](direct-write-portal.md) API 也支援一些新的計量，以向您的應用程式表達字型的有用資訊。 這些新計量包含這項資訊。

-   左、右、頂端和底部的字元周框方塊度量。
-   上標和下標元素的 X 和 Y 位置。
-   上標和下標元素的 X 和 Y 縮放比例資訊。
-   字型是否有印刷樣式計量。

您可以透過 [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1)和 [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1)介面上的新 [**GetMetrics**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefont1-getmetrics)方法，取得這項資訊。 這個方法會傳回包含所有資訊的 [**DWRITE \_ font-family \_ METRICS1**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_font_metrics1) 結構。

## <a name="caret-metrics"></a>插入號計量

若要建立文字編輯應用程式，您需要存取有關如何繪製可流覽文字之插入點的資訊。 從 Windows 8 開始， [DirectWrite](direct-write-portal.md)會在此案例的 [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1)和 [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1)介面上提供 [**GetCaretMetrics**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefontface1-getcaretmetrics)方法。 **GetCaretMetrics** 會傳回 [**DWRITE \_ 插入號 \_ 計量**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_caret_metrics) 列舉，其中包含有關基準上插入號的斜率和位移的資訊。

如果您想要能夠以斜體文字適當地使用其插入號斜率，此資訊特別有用。

## <a name="monospaced-discoverability"></a>等寬字型可探索性

讓使用者撰寫電腦程式代碼的應用程式，通常會使用等寬字型字型來取代更傳統的字型。 因此，您可以對開發相關應用程式中的字型選取進行更多的控制， [DirectWrite](direct-write-portal.md) 表示是否透過 API 等寬字型字型。 [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1)介面上的 [**IsMonospacedFont**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefont1-ismonospacedfont)方法會傳回布林值，指出字型是否為等寬字型。

## <a name="font-name-matching"></a>符合的字型名稱

PDF 讀取器等 Rich text 應用程式必須能夠將其內容中的字型與系統上的字型進行比對，因此需要存取多種格式的字型完整名稱。 因此，您可以更有效地比對字型， [DirectWrite](direct-write-portal.md) 包含的列舉會以許多格式表達字型的完整命名資訊。

您可以使用 [**DWRITE \_ 資訊 \_ 字串 \_ 識別碼**](/windows/win32/api/dwrite/ne-dwrite-dwrite_informational_string_id) 列舉來取得系統上任何字型的完整名稱、postscript 名稱和 postscript CID 名稱。 當您需要將應用程式中的字型與本機系統上的適當字型進行比對時，此資訊非常重要。

## <a name="glyph-advances"></a>字元前進

[**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1)和 [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1)介面上的 **GetGlyphAdvances** 方法會接受您需要前進資訊的圖像計數和索引，然後傳回有問題之圖像的前進。

## <a name="unicode-ranges"></a>Unicode 範圍

想要處理自己字型選取的應用程式，需要存取字型支援的 Unicode 範圍。 如此一來，如果字型不支援 Unicode 表示點，應用程式可以選擇包含該圖像的適當字型。 如果沒有此資訊，應用程式可能會使用不包含顯示資訊所需之所有字元的字型。

[**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1)和 [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1)介面上的 [**GetUnicodeRanges**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefont1-getunicoderanges)方法會接受從用戶端傳入的最大範圍數目，並傳回字型所支援的實際範圍。

## <a name="eudc-font-collection"></a>EUDC 字型集合

在 [**IDWriteFactory1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1)介面上使用 [**GetEudcFontCollection**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefactory1-geteudcfontcollection)方法，存取 EUDC 字型集合。 這個方法的運作方式與 [**GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection)相同，但會傳回 EUDC 字型集合的指標。

 

 