---
title: 使用 DirectWrite 開始使用教學課程
description: 本檔將說明如何使用 DirectWrite 和 Direct2D 來建立包含單一格式的簡單文字，以及包含多個格式的文字。
ms.assetid: cc2758d7-3f47-452a-8d81-3f777fe490ec
keywords:
- DirectWrite，教學課程
- DirectWrite，快速入門教學課程
- DirectWrite、Direct2D
- Direct2D
- DirectWrite，IDWriteTextLayout 介面
- IDWriteTextLayout 介面
- DirectWrite，IDWriteTypography 介面
- IDWriteTypography 介面
- DirectWrite，IDWriteTextFormat 介面
- IDWriteTextFormat 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48fb385ff78650a16599a32d76d7c51ba575de47
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315862"
---
# <a name="tutorial-getting-started-with-directwrite"></a>教學課程：使用 DirectWrite 開始使用

本檔將說明如何使用 [DirectWrite](direct-write-portal.md) 和 [Direct2D](rendering-by-using-direct2d.md) 來建立包含單一格式的簡單文字，以及包含多個格式的文字。

本教學課程包含下列部分：

-   [原始程式碼](#source-code)
-   [繪製簡單文字](#drawing-simple-text)
    -   [第1部分：宣告 DirectWrite 和 Direct2D 資源。](#part-1-declare-directwrite-and-direct2d-resources)
    -   [第2部分：建立與裝置無關的資源。](#part-2-create-device-independent-resources)
    -   [第3部分：建立 Device-Dependent 資源。](#part-3-create-device-dependent-resources)
    -   [第4部分：使用 Direct2D DrawText 方法繪製文字。](#part-4-draw-text-by-using-the-direct2d-drawtext-method)
    -   [第5部分：使用 Direct2D 轉譯視窗內容](#part-5-render-the-window-contents-using-direct2d)
-   [繪製具有多種格式的文字。](#drawing-text-with-multiple-formats)
    -   [第1部分：建立 IDWriteTextLayout 介面。](#part-1-create-an-idwritetextlayout-interface)
    -   [第2部分：使用 IDWriteTextLayout 套用格式。](#part-2-applying-formatting-with-idwritetextlayout)
    -   [第3部分：使用 IDWriteTypography 新增印刷樣式功能。](#part-3-adding-typographic-features-with-idwritetypography)
    -   [第4部分：使用 Direct2D DrawTextLayout 方法繪製文字。](#part-4-draw-text-using-the-direct2d-drawtextlayout-method)

## <a name="source-code"></a>原始程式碼

本總覽所顯示的原始程式碼取自 [DirectWrite Hello World 範例](/samples/browse/?redirectedfrom=MSDN-samples)。 每個部分都是在不同的類別中執行 (SimpleText 和 MultiformattedText) ，而且會顯示在另一個子視窗中。 每個類別都代表一個 Microsoft Win32 視窗。 除了 *WndProc* 方法，每個類別都包含下列方法：



| 函式                              | 描述                                                                                         |
|---------------------------------------|-----------------------------------------------------------------------------------------------------|
| **CreateDeviceIndependentResources**  | 建立與裝置無關的資源，讓它們可以在任何地方重複使用。                      |
| **DiscardDeviceIndependentResources** | 不再需要與裝置無關的資源時，會加以釋放。                          |
| **CreateDeviceResources**             | 建立與特定裝置系結的資源，例如筆刷和轉譯目標。        |
| **DiscardDeviceResources**            | 不再需要裝置相依的資源之後，再加以釋放。                            |
| **DrawD2DContent**                    | 使用 [Direct2D](../direct2d/direct2d-portal.md) 來呈現至螢幕。                              |
| **DrawText**                          | 使用 [Direct2D](../direct2d/direct2d-portal.md)繪製文字字串。                            |
| **OnResize**                          | 當視窗大小變更時，調整 [Direct2D](../direct2d/direct2d-portal.md) 轉譯目標的大小。 |



 

您可以使用所提供的範例，或使用下列指示，將 [DirectWrite](direct-write-portal.md) 和 [Direct2D](rendering-by-using-direct2d.md) 新增至您自己的 Win32 應用程式。 如需範例和相關聯專案檔案的詳細資訊，請參閱 [DirectWriteHelloWorld 範例](/samples/browse/?redirectedfrom=MSDN-samples)。

## <a name="drawing-simple-text"></a>繪製簡單文字

本節說明如何使用 [DirectWrite](direct-write-portal.md) 和 [Direct2D](../direct2d/direct2d-portal.md) 轉譯具有單一格式的簡單文字，如下列螢幕擷取畫面所示。

!["hello world using directwrite！" 的螢幕擷取畫面 以單一格式](images/simplecropped.png)

在螢幕上繪製簡單的文字需要四個元件：

-   要呈現的字元字串。
-   [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)的實例。
-   要包含文字的區域維度。
-   可以呈現文字的物件。 在本教學課程中。 您可以使用 [Direct2D](../direct2d/direct2d-portal.md) 轉譯目標。

[**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)介面描述用來格式化文字的字型系列名稱、大小、粗細、樣式和延展，並描述地區設定資訊。 **IDWriteTextFormat** 也會定義用來設定和取得下列屬性的方法：

-   行距。
-   相對於版面配置方塊左邊緣與右邊緣的文字對齊方式。
-   相對於版面配置方塊頂端和底部的段落對齊。
-   讀取方向。
-   溢出配置方塊之文字的文字修剪細微性。
-   遞增定位停駐點。
-   段落流程方向。

使用本檔中所述的兩個程式的文字來繪製文字時，必須要有 [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) 介面。

您必須要有 [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory)實例，才能建立 [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)物件或任何其他 [DirectWrite](direct-write-portal.md)物件。 您可以使用 **IDWriteFactory** 來建立 **IDWriteTextFormat** 實例和其他 DirectWrite 物件。 若要取得 factory 實例，請使用 [**DWriteCreateFactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) 函數。

### <a name="part-1-declare-directwrite-and-direct2d-resources"></a>第1部分：宣告 DirectWrite 和 Direct2D 資源。

在這個部分中，您會宣告稍後將用來建立和顯示文字的物件，做為您類別的私用資料成員。 [DirectWrite](direct-write-portal.md)的所有介面、函式和資料類型都是在 *dwrite .h* 標頭檔中宣告，而 [Direct2D](../direct2d/direct2d-portal.md)的所有介面、函數和資料類型都是在 *d2d1* 中宣告;如果您尚未這麼做，請在您的專案中包含這些標頭。

1.  在您的類別標頭檔中 (SimpleText) ，將 [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) 和 [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) 介面的指標宣告為私用成員。
    ```C++
    IDWriteFactory* pDWriteFactory_;
    IDWriteTextFormat* pTextFormat_;
    
    ```

    

2.  宣告成員以保存要呈現的文字字串和字串的長度。
    ```C++
    const wchar_t* wszText_;
    UINT32 cTextLength_;
    
    ```

    

3.  宣告 [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)、 [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget)和 [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) 介面的指標，以使用 [Direct2D](../direct2d/direct2d-portal.md)來呈現文字。
    ```C++
    ID2D1Factory* pD2DFactory_;
    ID2D1HwndRenderTarget* pRT_;
    ID2D1SolidColorBrush* pBlackBrush_;
    
    ```

    

### <a name="part-2-create-device-independent-resources"></a>第2部分：建立與裝置無關的資源。

[Direct2D](rendering-by-using-direct2d.md) 提供兩種類型的資源：與裝置相關的資源，以及與裝置無關的資源。 與裝置相關的資源會與轉譯裝置相關聯，且如果移除該裝置，將無法再運作。 另一方面，與裝置無關的資源可以是應用程式範圍的最後一個。

[DirectWrite](direct-write-portal.md) 資源與裝置無關。

在本節中，您會建立應用程式所使用的裝置獨立資源。 這些資源必須透過呼叫介面的 **發行** 方法來釋放。

某些使用的資源必須只建立一次，且不會系結至裝置。 這些資源的初始化會放在 *SimpleText：： CreateDeviceIndependentResources* 方法中，此方法會在初始化類別時呼叫。

1.  在類別實 (中的 *SimpleText：： CreateDeviceIndependentResources* 方法內，在 SimpleText .cpp) 中，呼叫 [**D2D1CreateFactory**](/windows/win32/api/d2d1/nf-d2d1-d2d1createfactory) 函式來建立 [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) 介面，這是所有 [Direct2D](../direct2d/direct2d-portal.md) 物件的根 factory 介面。 您可以使用相同的 factory 來具現化其他 Direct2D 資源。
    ```C++
    hr = D2D1CreateFactory(
        D2D1_FACTORY_TYPE_SINGLE_THREADED,
        &pD2DFactory_
        );
    
    ```

    

2.  呼叫 [**DWriteCreateFactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) 函式來建立 [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) 介面，這是所有 [DirectWrite](direct-write-portal.md) 物件的根 factory 介面。 您可以使用相同的 factory 來具現化其他 DirectWrite 資源。
    ```C++
    if (SUCCEEDED(hr))
    {
        hr = DWriteCreateFactory(
            DWRITE_FACTORY_TYPE_SHARED,
            __uuidof(IDWriteFactory),
            reinterpret_cast<IUnknown**>(&pDWriteFactory_)
            );
    }
    
    ```

    

3.  初始化文字字串並儲存其長度。

    ```C++
    wszText_ = L"Hello World using  DirectWrite!";
    cTextLength_ = (UINT32) wcslen(wszText_);
    
    ```

    

4.  使用 [**IDWriteFactory：： CreateTextFormat**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextformat)方法建立 [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)介面物件。 **IDWriteTextFormat** 指定將用來轉譯文字字串的字型、粗細、延展、樣式和地區設定。
    ```C++
    if (SUCCEEDED(hr))
    {
        hr = pDWriteFactory_->CreateTextFormat(
            L"Gabriola",                // Font family name.
            NULL,                       // Font collection (NULL sets it to use the system font collection).
            DWRITE_FONT_WEIGHT_REGULAR,
            DWRITE_FONT_STYLE_NORMAL,
            DWRITE_FONT_STRETCH_NORMAL,
            72.0f,
            L"en-us",
            &pTextFormat_
            );
    }
    
    ```

    

5.  藉由呼叫 [**IDWriteTextFormat：： SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) 和 [**IDWriteTextFormat：： SetParagraphAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setparagraphalignment) 方法，以水準和垂直方式將文字置中。
    ```C++
    // Center align (horizontally) the text.
    if (SUCCEEDED(hr))
    {
        hr = pTextFormat_->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER);
    }

    if (SUCCEEDED(hr))
    {
        hr = pTextFormat_->SetParagraphAlignment(DWRITE_PARAGRAPH_ALIGNMENT_CENTER);
    }
    
    ```

    

在此部分中，您已將應用程式所使用的裝置獨立資源初始化。 在下一個部分中，您會初始化裝置相依的資源。

### <a name="part-3-create-device-dependent-resources"></a>第3部分：建立 Device-Dependent 資源。

在此部分中，您會建立 [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) 和 [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) 來呈現您的文字。

轉譯目標是一種 Direct2D 物件，它會建立繪圖資源，並將繪製命令轉譯成轉譯裝置。 [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget)是呈現至 **HWND** 的轉譯目標。

轉譯目標可以建立的繪圖資源之一，是繪製大綱、填滿和文字的筆刷。 [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)會以純色繪製。

[**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget)和 [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)介面都是在建立時系結至轉譯裝置，而且必須在裝置變成無效時予以釋放和重新建立。

1.  在 SimpleText：： CreateDeviceResources 方法中，檢查呈現目標指標是否為 **Null**。 如果是，請取出轉譯區域的大小，然後建立該大小的 [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) 。 使用 **ID2D1HwndRenderTarget** 來建立 [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)。
    ```C++
    RECT rc;
    GetClientRect(hwnd_, &rc);

    D2D1_SIZE_U size = D2D1::SizeU(rc.right - rc.left, rc.bottom - rc.top);

    if (!pRT_)
    {
        // Create a Direct2D render target.
        hr = pD2DFactory_->CreateHwndRenderTarget(
                D2D1::RenderTargetProperties(),
                D2D1::HwndRenderTargetProperties(
                    hwnd_,
                    size
                    ),
                &pRT_
                );

        // Create a black brush.
        if (SUCCEEDED(hr))
        {
            hr = pRT_->CreateSolidColorBrush(
                D2D1::ColorF(D2D1::ColorF::Black),
                &pBlackBrush_
                );
        }
    }
    
    ```

    

2.  在 SimpleText：:D iscardDeviceResources 方法中，釋放筆刷和轉譯目標。
    ```C++
    SafeRelease(&pRT_);
    SafeRelease(&pBlackBrush_);
    
    ```

    

現在您已建立轉譯目標和筆刷，接下來您可以使用它們來呈現文字。

### <a name="part-4-draw-text-by-using-the-direct2d-drawtext-method"></a>第4部分：使用 Direct2D DrawText 方法繪製文字。

1.  在您類別的 SimpleText：:D rawText 方法中，藉由取出轉譯區域的維度來定義文字版面配置的區域，並建立具有相同維度的 [Direct2D](../direct2d/direct2d-portal.md) 矩形。
    ```C++
    D2D1_RECT_F layoutRect = D2D1::RectF(
        static_cast<FLOAT>(rc.left) / dpiScaleX_,
        static_cast<FLOAT>(rc.top) / dpiScaleY_,
        static_cast<FLOAT>(rc.right - rc.left) / dpiScaleX_,
        static_cast<FLOAT>(rc.bottom - rc.top) / dpiScaleY_
        );
    
    ```

    

2.  使用 [**ID2D1RenderTarget：:D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) 方法和 [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) 物件將文字轉譯至螢幕。 **ID2D1RenderTarget：:D rawtext** 方法會採用下列參數：
    -   要轉譯的字串。
    -   [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)介面的指標。
    -   [Direct2D](../direct2d/direct2d-portal.md)版面配置矩形。
    -   公開 [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush)之介面的指標。

    ```C++
    pRT_->DrawText(
        wszText_,        // The string to render.
        cTextLength_,    // The string's length.
        pTextFormat_,    // The text format.
        layoutRect,       // The region of the window where the text will be rendered.
        pBlackBrush_     // The brush used to draw the text.
        );
    
    ```

    

### <a name="part-5-render-the-window-contents-using-direct2d"></a>第5部分：使用 Direct2D 轉譯視窗內容

若要在收到繪製訊息時使用 [Direct2D](../direct2d/direct2d-portal.md) 來呈現視窗的內容，請執行下列動作：

1.  藉由呼叫第3部分中所實行的 SimpleText：： CreateDeviceResources 方法，來建立裝置相依的資源。
2.  呼叫呈現目標的 [**ID2D1HwndRenderTarget：： BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) 方法。
3.  藉由呼叫 [**ID2D1HwndRenderTarget：： clear**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-clear(constd2d1_color_f)) 方法來清除呈現目標。
4.  呼叫 SimpleText：:D rawText 方法，在第4部分中執行。
5.  呼叫呈現目標的 [**ID2D1HwndRenderTarget：： EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) 方法。
6.  如有必要，請捨棄裝置相依的資源，讓它們可以在重繪視窗時重新建立。


```C++
hr = CreateDeviceResources();

if (SUCCEEDED(hr))
{
    pRT_->BeginDraw();

    pRT_->SetTransform(D2D1::IdentityMatrix());

    pRT_->Clear(D2D1::ColorF(D2D1::ColorF::White));

    // Call the DrawText method of this class.
    hr = DrawText();

    if (SUCCEEDED(hr))
    {
        hr = pRT_->EndDraw(
            );
    }
}

if (FAILED(hr))
{
    DiscardDeviceResources();
}

```



SimpleText 類別是在 SimpleText 和 SimpleText 中執行。

## <a name="drawing-text-with-multiple-formats"></a>繪製具有多種格式的文字。

本節說明如何使用 [DirectWrite](direct-write-portal.md) 和 [Direct2D](../direct2d/direct2d-portal.md) 轉譯具有多種格式的文字，如下列螢幕擷取畫面所示。

!["hello world using directwrite！" 的螢幕擷取畫面，其中有一些不同樣式、大小和格式的部分](images/multiformattedcropped.png)

本節的程式碼會實作為 [DWriteHelloWorld 範例](/samples/browse/?redirectedfrom=MSDN-samples)中的 MultiformattedText 類別。 它是根據上一節中的步驟。

若要建立多格式的文字，您可以使用 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 介面，以及上一節所介紹的 [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) 介面。 **IDWriteTextLayout** 介面會描述文字區塊的格式設定和版面配置。 除了 **IDWriteTextFormat** 物件所指定的預設格式之外，也可以使用 **IDWriteTextLayout** 來變更特定範圍的文字格式。 這包括字型系列名稱、大小、粗細、樣式、延展、刪除線和底線。

[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 也提供點擊測試方法。 這些方法所傳回的點擊測試度量，會相對於使用 [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory)介面的 [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout)方法建立 **IDWriteTextLayout** 介面物件時所指定的版面配置方塊。

[**IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography)介面是用來將選擇性的 [OpenType](../intl/opentype-font-format.md)印刷樣式功能新增至文字配置，例如花飾字和替代的樣式文字集。 您可以藉由呼叫 **IDWriteTypography** 介面的 [**AddFontFeature**](/windows/win32/api/dwrite/nf-dwrite-idwritetypography-addfontfeature)方法，將印刷樣式功能加入至文字配置內的特定文字範圍。 這個方法會接收 [**DWRITE \_ 字型 \_ 功能**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_feature_tag) 結構作為參數，其中包含 **DWRITE \_ 字型 \_ 功能 \_ 標記** 列舉常數和 **UINT32** 執行參數。 您可以在 microsoft.com 上的 [Opentype 版面配置標記](https://www.microsoft.com/typography/otspec/features_ae.htm) 登錄中找到已註冊的 opentype 功能清單。 如需對等的 DirectWrite 列舉常數，請參閱 **DWRITE \_ 字型 \_ 功能 \_ 標記**。

### <a name="part-1-create-an-idwritetextlayout-interface"></a>第1部分：建立 IDWriteTextLayout 介面。

1.  宣告 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 介面的指標，作為 MultiformattedText 類別的成員。
    ```C++
    IDWriteTextLayout* pTextLayout_;
    
    ```

    

2.  在 MultiformattedText：： CreateDeviceIndependentResources 方法的結尾，藉由呼叫 [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout)方法來建立 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)介面物件。 **IDWriteTextLayout** 介面提供額外的格式設定功能，例如將不同格式套用至選取的文字部分的能力。
    ```C++
    // Create a text layout using the text format.
    if (SUCCEEDED(hr))
    {
        RECT rect;
        GetClientRect(hwnd_, &rect); 
        float width  = rect.right  / dpiScaleX_;
        float height = rect.bottom / dpiScaleY_;

        hr = pDWriteFactory_->CreateTextLayout(
            wszText_,      // The string to be laid out and formatted.
            cTextLength_,  // The length of the string.
            pTextFormat_,  // The text format to apply to the string (contains font information, etc).
            width,         // The width of the layout box.
            height,        // The height of the layout box.
            &pTextLayout_  // The IDWriteTextLayout interface pointer.
            );
    }
    
    ```

    

### <a name="part-2-applying-formatting-with-idwritetextlayout"></a>第2部分：使用 IDWriteTextLayout 套用格式。

您可以使用 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 介面，將格式化（例如字型大小、粗細和底線）套用至要顯示之文字的子字串。

1.  藉由宣告 [**DWRITE \_ 文字 \_ 範圍**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) 和呼叫 [**IDWriteTextLayout：： SetFontSize**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setfontsize) 方法，將 "DirectWrite" 的子字串 "Di" 設定為100的字型大小。
    ```C++
    // Format the "DirectWrite" substring to be of font size 100.
    if (SUCCEEDED(hr))
    {
        DWRITE_TEXT_RANGE textRange = {20,        // Start index where "DirectWrite" appears.
                                        6 };      // Length of the substring "Direct" in "DirectWrite".
        hr = pTextLayout_->SetFontSize(100.0f, textRange);
    }
    ```

    

2.  藉由呼叫 [**IDWriteTextLayout：： SetUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setunderline) 方法，對子字串 "DirectWrite" 加上底線。
    ```C++
    // Format the word "DWrite" to be underlined.
    if (SUCCEEDED(hr))
    {
        
        DWRITE_TEXT_RANGE textRange = {20,      // Start index where "DirectWrite" appears.
                                       11 };    // Length of the substring "DirectWrite".
        hr = pTextLayout_->SetUnderline(TRUE, textRange);
    }
    ```

    

3.  藉由呼叫 [**IDWriteTextLayout：： SetFontWeight**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setfontweight) 方法，將子字串 "DirectWrite" 的字型粗細設定為粗體。
    ```C++
    if (SUCCEEDED(hr))
    {
        // Format the word "DWrite" to be bold.
        DWRITE_TEXT_RANGE textRange = {20,
                                       11 };
        hr = pTextLayout_->SetFontWeight(DWRITE_FONT_WEIGHT_BOLD, textRange);
    }
    ```

    

### <a name="part-3-adding-typographic-features-with-idwritetypography"></a>第3部分：使用 IDWriteTypography 新增印刷樣式功能。

1.  藉由呼叫 [**IDWriteFactory：： CreateTypography**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtypography)方法，宣告並建立 [**IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography)介面物件。
    ```C++
    // Declare a typography pointer.
    IDWriteTypography* pTypography = NULL;

    // Create a typography interface object.
    if (SUCCEEDED(hr))
    {
        hr = pDWriteFactory_->CreateTypography(&pTypography);
    }
    
    ```

    

2.  藉由宣告已指定樣式設定7的 [**DWRITE \_ 字型 \_ 功能**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_feature) 物件，並呼叫 [**IDWriteTypography：： AddFontFeature**](/windows/win32/api/dwrite/nf-dwrite-idwritetypography-addfontfeature) 方法，來加入字型功能。
    ```C++
    // Set the stylistic set.
    DWRITE_FONT_FEATURE fontFeature = {DWRITE_FONT_FEATURE_TAG_STYLISTIC_SET_7,
                                       1};
    if (SUCCEEDED(hr))
    {
        hr = pTypography->AddFontFeature(fontFeature);
    }
    
    ```

    

3.  藉由宣告 [**DWRITE \_ 文字 \_ 範圍**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) 變數，並呼叫 [**IDWriteTextLayout：： SetTypography**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-settypography) 方法並傳入文字範圍，設定文字配置以使用整個字串的印刷樣式。
    ```C++
    if (SUCCEEDED(hr))
    {
        // Set the typography for the entire string.
        DWRITE_TEXT_RANGE textRange = {0,
                                       cTextLength_};
        hr = pTextLayout_->SetTypography(pTypography, textRange);
    }
    
    ```

    

4.  在 MultiformattedText：： OnResize 方法中設定 text layout 物件的新寬度和高度。
    ```C++
    if (pTextLayout_)
    {
        pTextLayout_->SetMaxWidth(static_cast<FLOAT>(width / dpiScaleX_));
        pTextLayout_->SetMaxHeight(static_cast<FLOAT>(height / dpiScaleY_));
    }
    ```

    

### <a name="part-4-draw-text-using-the-direct2d-drawtextlayout-method"></a>第4部分：使用 Direct2D DrawTextLayout 方法繪製文字。

若要使用 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 物件所指定的文字版面配置設定來繪製文字，請將 MultiformattedText：:D rawtext 方法中的程式碼變更為使用 [**IDWriteTextLayout：:D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)。

1.  Delcare [**D2D1 \_ 點的 \_ 2f**](../direct2d/d2d1-point-2f.md) 變數，並將它設定為視窗的左上角。
    ```C++
    D2D1_POINT_2F origin = D2D1::Point2F(
        static_cast<FLOAT>(rc.left / dpiScaleX_),
        static_cast<FLOAT>(rc.top / dpiScaleY_)
        );
    
    ```

    

2.  藉由呼叫 [Direct2D](../direct2d/direct2d-portal.md)轉譯目標的 [**ID2D1RenderTarget：:D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)方法並傳遞 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)指標，將文字繪製到螢幕。
    ```C++
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    
    ```

    

MultiformattedText 類別是在 MultiformattedText 和 MultiformattedText 中執行。

 

 