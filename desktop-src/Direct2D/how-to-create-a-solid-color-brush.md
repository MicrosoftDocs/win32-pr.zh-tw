---
title: 如何建立純色筆刷
description: 顯示如何使用 Direct2D 建立純色筆刷。
ms.assetid: 70700b82-2294-46be-b1c0-fc89def441e2
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 395652a33f8541a825bab9f2ababcceb4b31d7c8d46458a08148e63c85b2afff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119259450"
---
# <a name="how-to-create-a-solid-color-brush"></a>如何建立純色筆刷

若要建立單色筆刷，請使用 [**ID2DRenderTarget：： CreateSolidColorBrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) 方法，並指定您想要繪製的色彩。 某些 **CreateSolidColorBrush** 多載也可讓您指定筆刷的不透明度。

下列程式碼會示範如何建立實心黃色-綠色筆刷來填滿正方形，以及建立實心黑色筆刷來繪製正方形的外框。 程式碼會產生下圖中顯示的輸出。

![以黃色黃色綠色色彩填滿的矩形圖例](images/brushes-ovw-solidcolor.png)

1.  宣告兩個 [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) 指標：一個用來繪製黑色，另一個用於繪製黃色綠色。
    ```C++
        ID2D1SolidColorBrush *m_pBlackBrush;
        ID2D1SolidColorBrush *m_pYellowGreenBrush;
    ```

    

2.  呼叫 [**CreateSolidColorBrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) 方法來建立筆刷：
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

    

3.  呼叫 [**graphicswindow.fillrectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f__id2d1brush)) 方法，利用黃色的綠色筆刷和 [**graphicswindow.drawrectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) 方法來繪製矩形的內部，以黑色筆刷繪製矩形的外框：
    ```C++
    m_pRenderTarget->FillRectangle(&rcBrushRect, m_pYellowGreenBrush);
    m_pRenderTarget->DrawRectangle(&rcBrushRect, m_pBlackBrush, 1, NULL);
    ```

    

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct2D 參考](reference.md)
</dt> </dl>

 

 