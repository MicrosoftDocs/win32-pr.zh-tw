---
title: 色彩字型
description: 本主題說明色彩字型、其在 DirectWrite 和 Direct2D 中的支援，以及如何在您的應用程式中使用它們。
ms.assetid: 74e096c4-9d1c-8854-e9ee-f8b11ac1c71a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5c0154e528ab8471d40f4771db5479ca9233320177386adbbd849162dbcd598
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119329520"
---
# <a name="color-fonts"></a>色彩字型

本主題說明色彩字型、其在 DirectWrite 和 Direct2D 中的支援，以及如何在您的應用程式中使用它們。

本檔包含下列部分：

-   [什麼是色彩字型？](#what-are-color-fonts)
-   [為何要使用色彩字型？](#why-use-color-fonts)
-   [Windows 支援何種色彩字型？](#what-kinds-of-color-fonts-does-windows-support)
-   [使用色彩字型](#using-color-fonts)
    -   [在 XAML 應用程式中使用色彩字型](#using-color-fonts-in-a-xaml-app)
    -   [在 Microsoft Edge 中使用色彩字型](#using-color-fonts-in-microsoft-edge)
    -   [使用色彩字型搭配 DirectWrite 和 Direct2D](#using-color-fonts-with-directwrite-and-direct2d)
    -   [使用色彩字型搭配 Win2D](#using-color-fonts-with-win2d)
-   [相關主題](#related-topics)

## <a name="what-are-color-fonts"></a>什麼是色彩字型？

色彩字型（也稱為彩色字型或彩色字型）是一種字型技術，可讓字型設計工具在每個圖像中使用多種色彩。 色彩字型可讓應用程式和網站中的彩色文字案例具有較少的程式碼和更健全的作業系統支援，而不是在文字轉譯系統之上執行的臨機操作技術。

您可能最熟悉的字型不是色彩字型。 這些字型只會定義其所包含之字元的形狀，包括向量大綱或單色點陣圖。 在繪圖時，文字轉譯器會使用單一色彩來填滿圖像圖形， (要轉譯的應用程式或檔所指定的字型色彩 ) 。 另一方面，色彩字型除了圖形資訊之外，還包含色彩資訊。 某些方法可讓字型設計工具提供多個色彩調色板，以提供色彩字型藝術彈性。

下列範例會顯示 Segoe UI 表情色彩字型的圖像。 圖像會在左邊以單色轉譯，右邊以色彩呈現。

![顯示並排顯示的字元（以單色呈現的左圖像，在 Segoe U I 表情色彩字型中）。](images/color-font-cat.png)

色彩字型通常包含不支援色彩字型的平臺或已停用色彩功能之案例的回溯資訊。 在這些平臺上，色彩字型會轉譯為一般的單色字型。

## <a name="why-use-color-fonts"></a>為何要使用色彩字型？

在過去，設計人員和開發人員已使用各種不同的技術來取得彩色文字。 例如，網站通常會使用點陣影像而非文字，以顯示豐富的標頭。 這種方法可提供藝術彈性，但點陣圖形不會適當地調整成所有顯示大小，也不會提供與實際文字相同的協助工具功能。 另一種常見的技術是以不同的字型色彩覆迭多個單色字型，但這通常需要額外的版面配置程式碼來管理。

色彩字型提供一種方式，可讓您使用一般字型的所有簡潔和功能來達成這些視覺效果。 以色彩字型轉譯的文字與其他文字相同：可以複製和貼上、協助工具工具可以剖析它，依此類推。

## <a name="what-kinds-of-color-fonts-does-windows-support"></a>Windows 支援何種色彩字型？

[OpenType 規格](https://www.microsoft.com/Typography/OpenTypeSpecification.aspx)定義了數種在字型中內嵌色彩資訊的方式。 從 Windows 10 周年更新開始，DirectWrite 和 Direct2D (及其內建的 Windows 架構) 支援這些方法。 下表摘要說明這些摘要：



| 技巧                                                                                                                        | 描述                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [COLR](/typography/opentype/spec/colr) /[CPAL](/typography/opentype/spec/cpal)資料表 | 使用彩色向量的圖層，其形狀的定義方式與單一色彩圖像外框外。 **注意：** 從 Windows 8.1 開始支援。 <br/>                                                                                                                                                 |
| [SVG](/typography/opentype/spec/svg) 資料表                                                                 | 使用以可擴充向量圖形格式撰寫的向量影像。 **注意：** 從 Windows 10 周年更新，DirectWrite 支援完整 SVG 規格的子集。並非所有 SVG 內容都能以 OpenType SVG 字型呈現。 如需詳細資料，請參閱 [SVG 支援](../direct2d/svg-support.md) 。 <br/> |
| [CBDT](/typography/opentype/spec/cbdt) /[CBLC](/typography/opentype/spec/cblc)資料表 | 使用內嵌的色彩點陣圖影像。                                                                                                                                                                                                                                                                                |
| [sbix](/typography/opentype/spec/sbix) 資料表                                                               | 使用內嵌的色彩點陣圖影像。                                                                                                                                                                                                                                                                                |



 

## <a name="using-color-fonts"></a>使用色彩字型

從使用者的觀點來看，色彩字型只是字型。 例如，通常可以透過與單色字型相同的方式，從系統安裝和卸載它們，而且它們會轉譯為一般、可選取的文字。

從開發人員的觀點來看，色彩字型的使用方式通常與單色字型相同。 在 XAML 和 Microsoft Edge framework 中，您可以使用色彩字型來將文字樣式的樣式與一般字型相同，而且根據預設，您的文字將會以色彩呈現。 不過，如果您的應用程式直接呼叫 Direct2D Api (或 Win2D Api) 轉譯文字，則必須明確要求色彩字型轉譯。

### <a name="using-color-fonts-in-a-xaml-app"></a>在 XAML 應用程式中使用色彩字型

XAML 平臺的 text 元素 (例如[TextBlock](/uwp/api/windows.ui.xaml.controls.textblock)、 [TextBox](/uwp/api/windows.ui.xaml.controls.textbox)、 [RichEditBox](/uwp/api/windows.ui.xaml.controls.richeditbox)、圖像和[FontIcon](/uwp/api/windows.ui.xaml.controls.fonticon)) 預設支援色彩[字型](/uwp/api/windows.ui.xaml.documents.glyphs?f=255&MSPPError=-2147217396)。 只要使用色彩字型來為您的文字加上樣式，就會以色彩轉譯任何色彩字型。 下列程式碼範例示範使用以應用程式封裝的色彩字型來為 TextBlock 建立樣式的一種方式。 相同的技巧也適用于一般字型。


```XML
<TextBlock FontFamily="Assets/TMyColorFont.otf#MyFontFamilyName">Here is some text.</TextBlock>
```



如果您不想要讓 XAML 文字元素轉譯彩色文字，請將其 [IsColorFontEnabledProperty](/uwp/api/windows.ui.xaml.controls.textblock.iscolorfontenabledproperty) 屬性設定為 false。

### <a name="using-color-fonts-in-microsoft-edge"></a>在 Microsoft Edge 中使用色彩字型

色彩字型預設會在 Microsoft Edge 上執行的網站和 web 應用程式中轉譯，包括 XAML [web](/uwp/api/windows.ui.xaml.controls.webview)程式控制項。 只要使用 HTML 和 CSS 來為您的文字建立色彩字型的樣式，就會以色彩轉譯任何色彩圖像。

### <a name="using-color-fonts-with-directwrite-and-direct2d"></a>使用色彩字型搭配 DirectWrite 和 Direct2D

您的應用程式可以使用 Direct2D 的較高層級文字繪圖方法 ([**DrawText**](../direct2d/id2d1devicecontext4-drawtext-overload.md) 和) [**DrawTextLayout**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawtextlayout) ，也可以使用較低層級的技術來直接繪製圖像執行。 無論是哪一種情況，您的應用程式都需要變更程式碼，才能正確處理色彩圖像。 如果您的應用程式使用 Direct2D s **DrawText** 和 **DrawTextLayout** api，請注意，這些預設不會轉譯色彩字型。 這是為了避免在色彩字型支援之前設計的文字轉譯應用程式中發生非預期的行為變更。

若要加入宣告色彩字元轉譯，請將 [**D2D1 \_ DRAW \_ TEXT \_ 選項 \_ 啟用 \_ 色彩 \_ 字型**](/windows/win32/api/d2d1/ne-d2d1-d2d1_draw_text_options) 選項旗標傳遞至繪圖方法。 下列程式碼範例示範如何呼叫 Direct2D s DrawText 方法，以色彩字型呈現字串：


```C++
// If m_textFormat points to a font with color glyphs, then the following  
// call will render m_string using the color glyphs available in that font. 
// Any monochromatic glyphs will be rendered with m_defaultFillBrush. 
m_deviceContext->DrawText( 
    m_string->Data(), 
    m_string->Length(), 
    m_textFormat.Get(), 
    m_layoutRect, 
    m_defaultFillBrush.Get(), 
    D2D1_DRAW_TEXT_OPTIONS_ENABLE_COLOR_FONT 
    );  
    
```



如果您的應用程式使用較低層級的 Api 來直接處理圖像執行，則它會在色彩字型存在時繼續運作，但無法在沒有其他邏輯的情況下繪製色彩圖像。

若要正確處理色彩字型，您的應用程式應該：

1.  將圖像執行資訊傳遞給 [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun)，以及 [**DWRITE 影像處理 \_ \_ \_ 格式**](/windows/win32/api/dcommon/ne-dcommon-dwrite_glyph_image_formats) 參數，指出應用程式準備處理的色彩圖像)  (的類型。 如果有任何色彩圖像 (根據字型和要求的 **DWRITE \_ \_ 圖像影像 \_ 格式**) ，則 DirectWrite 會將主要圖像執行分割成個別的色彩圖像執行，您可以透過步驟4中傳回的 [**IDWriteColorGlyphRunEnumerator**](idwritecolorglyphrunenumerator.md)物件來存取這些文字。
2.  檢查 [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) 傳回的 HRESULT，以判斷是否偵測到任何色彩字元執行。 **DWRITE \_ E \_ NOCOLOR** 的 **HRESULT** 指出沒有適用的色彩圖像執行。
3.  如果 [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) 藉由傳回 **DWRITE \_ E \_ NOCOLOR**) 來 (未回報色彩字元執行，則會將整個圖像執行視為單色，而您的應用程式應該將它繪製為所需的 (例如，使用 [**ID2D1DeviceCoNtext：:D rawglyphrun**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawglyphrun)) 。
4.  如果 [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) 回報色彩圖像執行的存在，則您的應用程式應該忽略主要圖像執行，並改為使用 TranslateColorGlyphRun 所傳回的色彩字元執行 (s) 。 若要這樣做，請逐一查看傳回的 [**IDWriteColorGlyphRunEnumerator1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritecolorglyphrunenumerator1) 物件，並依適當的圖像影像格式來繪製每個色彩圖像 (例如，您可以使用 [**DrawColorBitmapGlyphRun**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawcolorbitmapglyphrun) 和 [**DrawSvgGlyphRun**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawsvgglyphrun) 來) 分別繪製色彩點陣圖字元和 SVG 圖像。

下列程式碼範例顯示此程式的一般結構：


```C++
// An example code snippet demonstrating how to use TranslateColorGlyphRun 
// to handle different kinds of color glyphs. This code does not make any 
// actual drawing calls. 
HRESULT DrawGlyphRun( 
    FLOAT baselineOriginX, 
    FLOAT baselineOriginY, 
    DWRITE_MEASURING_MODE measuringMode, 
    _In_ DWRITE_GLYPH_RUN const* glyphRun, 
    _In_ DWRITE_GLYPH_RUN_DESCRIPTION const* glyphRunDescription, 
) 
{ 
    // Specify the color glyph formats your app supports. In this example, 
    // the app requests only glyphs defined with PNG or SVG. 
    DWRITE_GLYPH_IMAGE_FORMATS requestedFormats = 
        DWRITE_GLYPH_IMAGE_FORMATS_PNG | DWRITE_GLYPH_IMAGE_FORMATS_SVG; 

    ComPtr<IDWriteColorGlyphRunEnumerator1> glyphRunEnumerator; 
    HRESULT hr = m_dwriteFactory->TranslateColorGlyphRun( 
        D2D1::Point2F(baselineOriginX, baselineOriginY), 
        glyphRun, 
        glyphRunDescription, 
        requestedFormats, // the glyph formats supported by this renderer 
        measuringMode, 
        nullptr, 
        0, 
        &glyphRunEnumerator // on return, may contain color glyph runs 
        ); 

    if (hr == DWRITE_E_NOCOLOR) 
    { 
        // The glyph run has no color glyphs. Draw it as a monochrome glyph 
        // run, for example using the DrawGlyphRun method on a Direct2D 
        // device context. 
    } 
    else 
    { 
        // The glyph run has one or more color glyphs. 
        DX::ThrowIfFailed(hr); 

        // Iterate through the color glyph runs and draw them. 
        for (;;) 
        { 
            BOOL haveRun; 
            DX::ThrowIfFailed(glyphRunEnumerator->MoveNext(&haveRun)); 
            if (!haveRun) 
            { 
                break; 
            } 

            // Retrieve the color glyph run. 
            DWRITE_COLOR_GLYPH_RUN1 const* colorRun; 
            DX::ThrowIfFailed(glyphRunEnumerator->GetCurrentRun(&colorRun)); 

            // Draw the color glyph run depending on its format. 
            switch (colorRun->glyphImageFormat) 
            { 
            case DWRITE_GLYPH_IMAGE_FORMATS_PNG: 
                // Draw the PNG glyph, for example with 
                // ID2D1DeviceContext4::DrawColorBitmapGlyphRun. 
                break; 

            case DWRITE_GLYPH_IMAGE_FORMATS_SVG: 
                // Draw the SVG glyph, for example with 
                // ID2D1DeviceContext4::DrawSvgGlyphRun. 
                break; 

                // ...etc. 
            } 
        } 
    } 

    return hr; 
} 
```



### <a name="using-color-fonts-with-win2d"></a>使用色彩字型搭配 Win2D

類似于 Direct2D，Win2D s 文字繪製 Api 預設不會轉譯色彩字型。 若要加入宣告色彩字元轉譯，請在您的應用程式傳遞給文字繪圖方法的文字格式物件中設定 [EnableColorFont](https://microsoft.github.io/Win2D/html/T_Microsoft_Graphics_Canvas_Text_CanvasDrawTextOptions.htm) 選項旗標。 下列程式碼範例示範如何使用 Win2D，以色彩字型呈現字串：


```C++
// The text format that will be used to draw the text. (Declared elsewhere 
// and initialized elsewhere by the app to point to a color font.) 
CanvasTextFormat m_textFormat; 

// Set the EnableColorFont option. 
m_textFormat.Options = CanvasDrawTextOptions.EnableColorFont; 

// If m_textFormat points to a font with color glyphs, then the following  
// call will render m_string using the color glyphs available in that font. 
// Any monochromatic glyphs will be rendered with m_color. 
args.DrawingSession.DrawText( 
    m_string, 
    m_point, 
    m_color, 
    m_textFormat 
    ); 
```

## <a name="related-topics"></a>相關主題

[DirectWrite 彩色圖像範例](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteColorGlyph)


[**IDWriteFontFace4 介面**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface4)


[**IDWriteFactory4：： TranslateColorGlyphRun 方法**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun)


[**ID2D1DeviceCoNtext4：:D rawText 方法**](../direct2d/id2d1devicecontext4-drawtext-overload.md)


 

