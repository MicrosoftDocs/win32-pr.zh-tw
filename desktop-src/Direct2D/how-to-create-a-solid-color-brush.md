---
title: 如何建立純色筆刷
description: 顯示如何使用 Direct2D 建立純色筆刷。
ms.assetid: 70700b82-2294-46be-b1c0-fc89def441e2
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: bc6fbf5df42386f5e0e5a843a1906d36d4fc8c71
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933321"
---
# <a name="how-to-create-a-solid-color-brush"></a><span data-ttu-id="84257-103">如何建立純色筆刷</span><span class="sxs-lookup"><span data-stu-id="84257-103">How to Create a Solid Color Brush</span></span>

<span data-ttu-id="84257-104">若要建立單色筆刷，請使用 [**ID2DRenderTarget：： CreateSolidColorBrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) 方法，並指定您想要繪製的色彩。</span><span class="sxs-lookup"><span data-stu-id="84257-104">To create a solid color brush, use the [**ID2DRenderTarget::CreateSolidColorBrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) method and specify the color with which you want to paint.</span></span> <span data-ttu-id="84257-105">某些 **CreateSolidColorBrush** 多載也可讓您指定筆刷的不透明度。</span><span class="sxs-lookup"><span data-stu-id="84257-105">Some of the **CreateSolidColorBrush** overloads also enable you to specify the opacity of the brush.</span></span>

<span data-ttu-id="84257-106">下列程式碼會示範如何建立實心黃色-綠色筆刷來填滿正方形，以及建立實心黑色筆刷來繪製正方形的外框。</span><span class="sxs-lookup"><span data-stu-id="84257-106">The following code shows how to create a solid yellow-green brush to fill a square, and a solid black brush to draw the outline of the square.</span></span> <span data-ttu-id="84257-107">程式碼會產生下圖中顯示的輸出。</span><span class="sxs-lookup"><span data-stu-id="84257-107">The code produces the output shown in the following illustration.</span></span>

![以黃色黃色綠色色彩填滿的矩形圖例](images/brushes-ovw-solidcolor.png)

1.  <span data-ttu-id="84257-109">宣告兩個 [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) 指標：一個用來繪製黑色，另一個用於繪製黃色綠色。</span><span class="sxs-lookup"><span data-stu-id="84257-109">Declare two [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) pointers: one for painting black and one for painting yellow green.</span></span>
    ```C++
        ID2D1SolidColorBrush *m_pBlackBrush;
        ID2D1SolidColorBrush *m_pYellowGreenBrush;
    ```

    

2.  <span data-ttu-id="84257-110">呼叫 [**CreateSolidColorBrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) 方法來建立筆刷：</span><span class="sxs-lookup"><span data-stu-id="84257-110">Call the [**CreateSolidColorBrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) method to create the brushes:</span></span>
    ```C++
    if (SUCCEEDED(hr))
    {
        hr = m_pRenderTarget->CreateSolidColorBrush(
            D2D1::ColorF(D2D1::ColorF::Black, 1.0f),
            &m_pBlackBrush
            );
    }

    // Create a solid color brush with its rgb value 0x9ACD32.
    if (SUCCEEDED(hr))
    {
        hr = m_pRenderTarget->CreateSolidColorBrush(
            D2D1::ColorF(D2D1::ColorF(0x9ACD32, 1.0f)),  
            &m_pYellowGreenBrush
            );
    }
    ```

    

3.  <span data-ttu-id="84257-111">呼叫 [**graphicswindow.fillrectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f__id2d1brush)) 方法，利用黃色的綠色筆刷和 [**graphicswindow.drawrectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) 方法來繪製矩形的內部，以黑色筆刷繪製矩形的外框：</span><span class="sxs-lookup"><span data-stu-id="84257-111">Call the [**FillRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f__id2d1brush)) method to paint the interior of the rectangle with the yellow green brush and the [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) method to paint the outline of the rectangle with the black brush:</span></span>
    ```C++
    m_pRenderTarget->FillRectangle(&rcBrushRect, m_pYellowGreenBrush);
    m_pRenderTarget->DrawRectangle(&rcBrushRect, m_pBlackBrush, 1, NULL);
    ```

    

## <a name="related-topics"></a><span data-ttu-id="84257-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="84257-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84257-113">Direct2D 參考</span><span class="sxs-lookup"><span data-stu-id="84257-113">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 