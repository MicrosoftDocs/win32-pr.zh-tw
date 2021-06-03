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
# <a name="how-to-draw-text"></a><span data-ttu-id="1b0b0-103">如何繪製文字</span><span class="sxs-lookup"><span data-stu-id="1b0b0-103">How to Draw Text</span></span>

<span data-ttu-id="1b0b0-104">若要使用 Direct2D 繪製文字，請針對具有單一格式的文字使用 [**ID2D1RenderTarget：:D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) 方法。</span><span class="sxs-lookup"><span data-stu-id="1b0b0-104">To draw text with Direct2D, use the [**ID2D1RenderTarget::DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) method for text that has a single format.</span></span> <span data-ttu-id="1b0b0-105">或者，將 [**ID2D1RenderTarget：:D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) 方法用於多種格式、先進的 OpenType 功能或點擊測試。</span><span class="sxs-lookup"><span data-stu-id="1b0b0-105">Or, use the [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) method for multiple formats, advanced OpenType features, or hit testing.</span></span> <span data-ttu-id="1b0b0-106">這些方法會使用 DirectWrite API 來提供高品質的文字顯示。</span><span class="sxs-lookup"><span data-stu-id="1b0b0-106">These methods use the DirectWrite API to provide high-quality text display.</span></span>

## <a name="the-drawtext-method"></a><span data-ttu-id="1b0b0-107">DrawText 方法</span><span class="sxs-lookup"><span data-stu-id="1b0b0-107">The DrawText Method</span></span>

<span data-ttu-id="1b0b0-108">若要繪製具有單一格式的文字，請使用 [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) 方法。</span><span class="sxs-lookup"><span data-stu-id="1b0b0-108">To draw text that has a single format, use the [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) method.</span></span> <span data-ttu-id="1b0b0-109">若要使用此方法，請先使用 [**IDWriteFactory**](/windows/desktop/api/dwrite/nn-dwrite-idwritefactory) 來建立 [**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) 實例。</span><span class="sxs-lookup"><span data-stu-id="1b0b0-109">To use this method, first use an [**IDWriteFactory**](/windows/desktop/api/dwrite/nn-dwrite-idwritefactory) to create an [**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) instance.</span></span>

<span data-ttu-id="1b0b0-110">下列程式碼會建立 [**IDWriteTextFormat**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) 物件，並將它儲存在 *m \_ pTextFormat* 變數中。</span><span class="sxs-lookup"><span data-stu-id="1b0b0-110">The following code creates an [**IDWriteTextFormat**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) object and stores it in the *m\_pTextFormat* variable.</span></span>


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



<span data-ttu-id="1b0b0-111">因為 [**IDWriteFactory**](/windows/desktop/api/dwrite/nn-dwrite-idwritefactory) 和 [**IDWriteTextFormat**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) 物件是與 [裝置無關的資源](resources-and-resource-domains.md)，所以您可以只建立一次來改善應用程式的效能，而不是每次轉譯框架時都重新建立它們。</span><span class="sxs-lookup"><span data-stu-id="1b0b0-111">Because [**IDWriteFactory**](/windows/desktop/api/dwrite/nn-dwrite-idwritefactory) and [**IDWriteTextFormat**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) objects are [device-independent resources](resources-and-resource-domains.md), you can improve an application's performance by creating them only one time, instead of re-creating them every time that a frame is rendered.</span></span>

<span data-ttu-id="1b0b0-112">建立文字格式物件之後，您可以將它用於轉譯目標。</span><span class="sxs-lookup"><span data-stu-id="1b0b0-112">After you create the text format object, you can use it with a render target.</span></span> <span data-ttu-id="1b0b0-113">下列程式碼會使用轉譯目標的 [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) 方法， (*m \_ pRenderTarget* 變數) 來繪製文字。</span><span class="sxs-lookup"><span data-stu-id="1b0b0-113">The following code draws the text by using the [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) method of the render target (the *m\_pRenderTarget* variable).</span></span>


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



## <a name="the-drawtextlayout-method"></a><span data-ttu-id="1b0b0-114">DrawTextLayout 方法</span><span class="sxs-lookup"><span data-stu-id="1b0b0-114">The DrawTextLayout Method</span></span>

<span data-ttu-id="1b0b0-115">[**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)方法會呈現 [**IDWriteTextLayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout)物件。</span><span class="sxs-lookup"><span data-stu-id="1b0b0-115">The [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) method renders an [**IDWriteTextLayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span> <span data-ttu-id="1b0b0-116">使用這個方法可將多個格式套用至文字區塊 (例如，將文字的一部分加上底線) 、使用 advanced OpenType 功能，或執行點擊測試支援。</span><span class="sxs-lookup"><span data-stu-id="1b0b0-116">Use this method to apply multiple formats to a block of text (such as underlining a part of text), to use advanced OpenType features, or to perform hit testing support.</span></span>

<span data-ttu-id="1b0b0-117">[**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)方法也提供重複繪製相同文字的效能優勢。</span><span class="sxs-lookup"><span data-stu-id="1b0b0-117">The [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) method also provides performance benefits for drawing the same text repeatedly.</span></span> <span data-ttu-id="1b0b0-118">當您建立時， [**IDWriteTextLayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) 物件會測量並配置其文字。</span><span class="sxs-lookup"><span data-stu-id="1b0b0-118">The [**IDWriteTextLayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) object measures and lays out its text when you create it.</span></span> <span data-ttu-id="1b0b0-119">如果您只建立一個 **IDWriteTextLayout** 物件，並在每次需要重新繪製文字時重複使用它，效能就會提升，因為系統不需要再次測量及配置文字。</span><span class="sxs-lookup"><span data-stu-id="1b0b0-119">If you create an **IDWriteTextLayout** object only one time and reuse it every time that you have to redraw the text, the performance improves because the system does not have to measure and lay out the text again.</span></span>

<span data-ttu-id="1b0b0-120">在您可以使用 [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) 方法之前，必須先使用 [**IDWriteFactory**](/windows/desktop/api/dwrite/nn-dwrite-idwritefactory) 來建立 [**IDWriteTextFormat**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) 和 [**IDWriteTextLayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) 物件。</span><span class="sxs-lookup"><span data-stu-id="1b0b0-120">Before you can use the [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) method, you must use an [**IDWriteFactory**](/windows/desktop/api/dwrite/nn-dwrite-idwritefactory) to create [**IDWriteTextFormat**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) and [**IDWriteTextLayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) objects.</span></span> <span data-ttu-id="1b0b0-121">建立這些物件之後，請呼叫 **DrawTextLayout** 方法。</span><span class="sxs-lookup"><span data-stu-id="1b0b0-121">After these objects are created, call the **DrawTextLayout** method.</span></span>

<span data-ttu-id="1b0b0-122">如需詳細資訊和範例，請參閱 [文字格式設定和版面](/windows/desktop/DirectWrite/text-formatting-and-layout) 配置總覽。</span><span class="sxs-lookup"><span data-stu-id="1b0b0-122">For more information and examples, see the [Text Formatting and Layout](/windows/desktop/DirectWrite/text-formatting-and-layout) overview.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1b0b0-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="1b0b0-123">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="1b0b0-124">[**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))</span><span class="sxs-lookup"><span data-stu-id="1b0b0-124">[**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))</span></span>
</dt> <dt>

[<span data-ttu-id="1b0b0-125">**DrawTextLayout**</span><span class="sxs-lookup"><span data-stu-id="1b0b0-125">**DrawTextLayout**</span></span>](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)
</dt> <dt>

[<span data-ttu-id="1b0b0-126">**IDWriteTextFormat**</span><span class="sxs-lookup"><span data-stu-id="1b0b0-126">**IDWriteTextFormat**</span></span>](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat)
</dt> <dt>

[<span data-ttu-id="1b0b0-127">**IDWriteTextLayout**</span><span class="sxs-lookup"><span data-stu-id="1b0b0-127">**IDWriteTextLayout**</span></span>](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> <dt>

[<span data-ttu-id="1b0b0-128">文字格式設定和版面配置</span><span class="sxs-lookup"><span data-stu-id="1b0b0-128">Text Formatting and Layout</span></span>](/windows/desktop/DirectWrite/text-formatting-and-layout)
</dt> </dl>

 

 
