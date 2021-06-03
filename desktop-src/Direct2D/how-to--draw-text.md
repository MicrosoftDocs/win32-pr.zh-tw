---
title: 如何繪製文字
description: 示範如何使用 Direct2D 呈現文字。
ms.assetid: 914dd9d0-78c8-44a3-8504-837faf3201d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd841f3b07edbde5e3fc6ed70f679cd58b3725f4
ms.sourcegitcommit: d5f16b9d3d5d2e2080ba7b6837eb37250fa67a30
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/02/2021
ms.locfileid: "111349967"
---
# <a name="how-to-draw-text"></a>如何繪製文字

若要使用 Direct2D 繪製文字，請針對具有單一格式的文字使用 [**ID2D1RenderTarget：:D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) 方法。 或者，將 [**ID2D1RenderTarget：:D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) 方法用於多種格式、先進的 OpenType 功能或點擊測試。 這些方法會使用 DirectWrite API 來提供高品質的文字顯示。

## <a name="the-drawtext-method"></a>DrawText 方法

若要繪製具有單一格式的文字，請使用 [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) 方法。 若要使用此方法，請先使用 [**IDWriteFactory**](/windows/desktop/api/dwrite/nn-dwrite-idwritefactory) 來建立 [**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) 實例。

下列程式碼會建立 [**IDWriteTextFormat**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) 物件，並將它儲存在 *m \_ pTextFormat* 變數中。


```C++
// Create resources which are not bound
// to any device. Their lifetime effectively extends for the
// duration of the app. These resources include the Direct2D and
// DirectWrite factories,  and a DirectWrite Text Format object
// (used for identifying particular font characteristics).
//
HRESULT DemoApp::CreateDeviceIndependentResources()
{
    static const WCHAR msc_fontName[] = L"Verdana";
    static const FLOAT msc_fontSize = 50;
    HRESULT hr;

    // Create a Direct2D factory.
    hr = D2D1CreateFactory(D2D1_FACTORY_TYPE_SINGLE_THREADED, &m_pD2DFactory);

    if (SUCCEEDED(hr))
    {        
        // Create a DirectWrite factory.
        hr = DWriteCreateFactory(
            DWRITE_FACTORY_TYPE_SHARED,
            __uuidof(m_pDWriteFactory),
            reinterpret_cast<IUnknown **>(&m_pDWriteFactory)
            );
    }
    if (SUCCEEDED(hr))
    {
        // Create a DirectWrite text format object.
        hr = m_pDWriteFactory->CreateTextFormat(
            msc_fontName,
            NULL,
            DWRITE_FONT_WEIGHT_NORMAL,
            DWRITE_FONT_STYLE_NORMAL,
            DWRITE_FONT_STRETCH_NORMAL,
            msc_fontSize,
            L"", //locale
            &m_pTextFormat
            );
    }
    if (SUCCEEDED(hr))
    {
        // Center the text horizontally and vertically.
        m_pTextFormat->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER);
        
        m_pTextFormat->SetParagraphAlignment(DWRITE_PARAGRAPH_ALIGNMENT_CENTER);
    }

    return hr;
}
```



因為 [**IDWriteFactory**](/windows/desktop/api/dwrite/nn-dwrite-idwritefactory) 和 [**IDWriteTextFormat**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) 物件是與 [裝置無關的資源](resources-and-resource-domains.md)，所以您可以只建立一次來改善應用程式的效能，而不是每次轉譯框架時都重新建立它們。

建立文字格式物件之後，您可以將它用於轉譯目標。 下列程式碼會使用轉譯目標的 [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) 方法， (*m \_ pRenderTarget* 變數) 來繪製文字。


```C++
//  Called whenever the application needs to display the client
//  window. This method writes "Hello, World"
//
//  Note that this function will automatically discard device-specific
//  resources if the Direct3D device disappears during function
//  invocation, and will recreate the resources the next time it's
//  invoked.
//
HRESULT DemoApp::OnRender()
{
    HRESULT hr;

    hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        static const WCHAR sc_helloWorld[] = L"Hello, World!";

        // Retrieve the size of the render target.
        D2D1_SIZE_F renderTargetSize = m_pRenderTarget->GetSize();

        m_pRenderTarget->BeginDraw();

        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

        m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

        m_pRenderTarget->DrawText(
            sc_helloWorld,
            ARRAYSIZE(sc_helloWorld) - 1,
            m_pTextFormat,
            D2D1::RectF(0, 0, renderTargetSize.width, renderTargetSize.height),
            m_pBlackBrush
            );

        hr = m_pRenderTarget->EndDraw();

        if (hr == D2DERR_RECREATE_TARGET)
        {
            hr = S_OK;
            DiscardDeviceResources();
        }
    }

    return hr;
}
```



## <a name="the-drawtextlayout-method"></a>DrawTextLayout 方法

[**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)方法會呈現 [**IDWriteTextLayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout)物件。 使用這個方法可將多個格式套用至文字區塊 (例如，將文字的一部分加上底線) 、使用 advanced OpenType 功能，或執行點擊測試支援。

[**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)方法也提供重複繪製相同文字的效能優勢。 當您建立時， [**IDWriteTextLayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) 物件會測量並配置其文字。 如果您只建立一個 **IDWriteTextLayout** 物件，並在每次需要重新繪製文字時重複使用它，效能就會提升，因為系統不需要再次測量及配置文字。

在您可以使用 [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) 方法之前，必須先使用 [**IDWriteFactory**](/windows/desktop/api/dwrite/nn-dwrite-idwritefactory) 來建立 [**IDWriteTextFormat**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) 和 [**IDWriteTextLayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) 物件。 建立這些物件之後，請呼叫 **DrawTextLayout** 方法。

如需詳細資訊和範例，請參閱 [文字格式設定和版面](/windows/desktop/DirectWrite/text-formatting-and-layout) 配置總覽。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))
</dt> <dt>

[**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)
</dt> <dt>

[**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat)
</dt> <dt>

[**IDWriteTextLayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> <dt>

[文字格式設定和版面配置](/windows/desktop/DirectWrite/text-formatting-and-layout)
</dt> </dl>

 

 
