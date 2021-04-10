---
title: 使用 Direct2D 轉譯
description: Direct2D 提供的方法，可讓您以只有 IDWriteTextFormat 或 IDWriteTextLayout 所描述的格式，將文字轉譯成 Direct2D 介面。
ms.assetid: 4acd1aee-98bf-4ca3-b4dc-b73c96c6ca63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58af17e15bcb9bd52461a2da3110982fb04e4c0a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104024017"
---
# <a name="render-using-direct2d"></a><span data-ttu-id="5c67a-103">使用 Direct2D 轉譯</span><span class="sxs-lookup"><span data-stu-id="5c67a-103">Render Using Direct2D</span></span>

<span data-ttu-id="5c67a-104">Direct2D 提供的方法，可讓您以只有 [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) 或 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 所描述的格式，將文字轉譯成 Direct2D 介面。</span><span class="sxs-lookup"><span data-stu-id="5c67a-104">Direct2D provides methods for rendering either text with formatting described by only an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) or an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) to a Direct2D surface.</span></span>

## <a name="rendering-text-described-by-idwritetextformat"></a><span data-ttu-id="5c67a-105">IDWriteTextFormat 所描述的轉譯文字</span><span class="sxs-lookup"><span data-stu-id="5c67a-105">Rendering Text Described by IDWriteTextFormat</span></span>

<span data-ttu-id="5c67a-106">若要使用 [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)物件轉譯字串，以描述整個字串的格式，請使用 [Direct2D](../direct2d/direct2d-portal.md)所提供的 [**ID2D1RenderTarget：:D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))方法。</span><span class="sxs-lookup"><span data-stu-id="5c67a-106">To render a string using an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object to describe the formatting for the entire string, use the [**ID2D1RenderTarget::DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) method provided by [Direct2D](../direct2d/direct2d-portal.md).</span></span>

1.  <span data-ttu-id="5c67a-107">藉由取出轉譯區域的維度來定義文字版面配置的區域，並建立具有相同維度的 [Direct2D](../direct2d/direct2d-portal.md) 矩形。</span><span class="sxs-lookup"><span data-stu-id="5c67a-107">Define the area for the text layout by retrieving the dimensions of the rendering area, and create a [Direct2D](../direct2d/direct2d-portal.md) rectangle that has the same dimensions.</span></span>
    ```C++
    D2D1_RECT_F layoutRect = D2D1::RectF(
        static_cast<FLOAT>(rc.left) / dpiScaleX_,
        static_cast<FLOAT>(rc.top) / dpiScaleY_,
        static_cast<FLOAT>(rc.right - rc.left) / dpiScaleX_,
        static_cast<FLOAT>(rc.bottom - rc.top) / dpiScaleY_
        );
    
    ```

    

2.  <span data-ttu-id="5c67a-108">使用 [**ID2D1RenderTarget：:D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) 方法和 [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) 物件將文字轉譯至螢幕。</span><span class="sxs-lookup"><span data-stu-id="5c67a-108">Use the [**ID2D1RenderTarget::DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) method and the [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object to render text to the screen.</span></span> <span data-ttu-id="5c67a-109">**ID2D1RenderTarget：:D rawtext** 方法會採用下列參數：</span><span class="sxs-lookup"><span data-stu-id="5c67a-109">The **ID2D1RenderTarget::DrawText** method takes the following parameters:</span></span>
    -   <span data-ttu-id="5c67a-110">要轉譯的字串。</span><span class="sxs-lookup"><span data-stu-id="5c67a-110">A string to render.</span></span>
    -   <span data-ttu-id="5c67a-111">[**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="5c67a-111">A pointer to an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface.</span></span>
    -   <span data-ttu-id="5c67a-112">[Direct2D](../direct2d/direct2d-portal.md)版面配置矩形。</span><span class="sxs-lookup"><span data-stu-id="5c67a-112">A [Direct2D](../direct2d/direct2d-portal.md) layout rectangle.</span></span>
    -   <span data-ttu-id="5c67a-113">公開 [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush)之介面的指標。</span><span class="sxs-lookup"><span data-stu-id="5c67a-113">A pointer to an interface that exposes [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush).</span></span>

    ```C++
    pRT_->DrawText(
        wszText_,        // The string to render.
        cTextLength_,    // The string's length.
        pTextFormat_,    // The text format.
        layoutRect,       // The region of the window where the text will be rendered.
        pBlackBrush_     // The brush used to draw the text.
        );
    
    ```

    

## <a name="rendering-a-idwritetext-layout-object"></a><span data-ttu-id="5c67a-114">轉譯 IDWriteText 版面設定物件</span><span class="sxs-lookup"><span data-stu-id="5c67a-114">Rendering a IDWriteText Layout Object</span></span>

<span data-ttu-id="5c67a-115">若要使用 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 物件所指定的文字版面配置設定來繪製文字，請將 MultiformattedText：:D rawtext 方法中的程式碼變更為使用 [**IDWriteTextLayout：:D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)。</span><span class="sxs-lookup"><span data-stu-id="5c67a-115">To draw the text with the text layout settings specified by the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object, change the code in the MultiformattedText::DrawText method to use [**IDWriteTextLayout::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout).</span></span>

1.  <span data-ttu-id="5c67a-116">Delcare [**D2D1 \_ 點的 \_ 2f**](../direct2d/d2d1-point-2f.md) 變數，並將它設定為視窗的左上角。</span><span class="sxs-lookup"><span data-stu-id="5c67a-116">Delcare a [**D2D1\_POINT\_2F**](../direct2d/d2d1-point-2f.md) variable and set it to the upper-left point of the window.</span></span>
    ```C++
    D2D1_POINT_2F origin = D2D1::Point2F(
        static_cast<FLOAT>(rc.left / dpiScaleX_),
        static_cast<FLOAT>(rc.top / dpiScaleY_)
        );
    
    ```

    

2.  <span data-ttu-id="5c67a-117">藉由呼叫 [Direct2D](../direct2d/direct2d-portal.md)轉譯目標的 [**ID2D1RenderTarget：:D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)方法並傳遞 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)指標，將文字繪製到螢幕。</span><span class="sxs-lookup"><span data-stu-id="5c67a-117">Draw the text to the screen by calling the [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) method of the [Direct2D](../direct2d/direct2d-portal.md) render target and passing the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) pointer.</span></span>
    ```C++
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    
    ```

    

 

 