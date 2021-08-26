---
title: 使用 Direct2D 轉譯
description: Direct2D 提供的方法，可讓您以只有 IDWriteTextFormat 或 IDWriteTextLayout 所描述的格式，將文字轉譯成 Direct2D 介面。
ms.assetid: 4acd1aee-98bf-4ca3-b4dc-b73c96c6ca63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ad297a8fdf2078c966989baf5e81c69cf515427340f8de8d073035fcf98f434
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048478"
---
# <a name="render-using-direct2d"></a>使用 Direct2D 轉譯

Direct2D 提供的方法，可讓您以只有 [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) 或 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 所描述的格式，將文字轉譯成 Direct2D 介面。

## <a name="rendering-text-described-by-idwritetextformat"></a>IDWriteTextFormat 所描述的轉譯文字

若要使用 [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)物件轉譯字串，以描述整個字串的格式，請使用 [Direct2D](../direct2d/direct2d-portal.md)所提供的 [**ID2D1RenderTarget：:D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))方法。

1.  藉由取出轉譯區域的維度來定義文字版面配置的區域，並建立具有相同維度的 [Direct2D](../direct2d/direct2d-portal.md) 矩形。
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

    

## <a name="rendering-a-idwritetext-layout-object"></a>轉譯 IDWriteText 版面設定物件

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

    

 

 