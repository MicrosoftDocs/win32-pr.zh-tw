---
title: 如何建立線性漸層筆刷
description: 顯示如何使用 Direct2D 建立線性漸層筆刷。
ms.assetid: 3cf5acc6-2f17-49d4-aca5-a84a846d1749
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 3a50a6e3ab421e2275644051ed647d5c4501f8e0
ms.sourcegitcommit: 015fb35e736a235d3c9becff1f6832a0965b4303
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "103843024"
---
# <a name="how-to-create-a-linear-gradient-brush"></a>如何建立線性漸層筆刷

若要建立線性漸層筆刷，請使用 [**CreateLinearGradientBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) 方法，並指定線性漸層筆刷屬性和漸層停駐點集合。 某些多載可讓您指定筆刷屬性。 下列程式碼示範如何建立線性漸層筆刷來填滿正方形，以及建立實心黑色筆刷來繪製正方形的外框。

程式碼會產生下圖中顯示的輸出。

![以線性漸層筆刷填滿的正方形圖例](images/brushes-ovw-lineargradient.png)

1.  宣告 [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)型別的變數。
    ```C++
        ID2D1LinearGradientBrush *m_pLinearGradientBrush;
    ```

    

2.  您可以使用 [**ID2D1RenderTarget：： CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_id2d1gradientstopcollection))方法，利用 [**D2D1 \_ 梯度 \_ 停**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop)用結構的宣告陣列來建立 [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection)集合，如下列程式碼所示。
    > [!Note]  
    > 從 Windows 8 開始，您可以改用 [**ID2D1DeviceCoNtext：： CreateGradientStopCollection**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-creategradientstopcollection) 方法來建立 [**ID2D1GradientStopCollection1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1gradientstopcollection1) 集合。 此介面會以直線或 prmultiplied 色彩新增高彩漸層和漸層的插補。 如需詳細資訊，請參閱 **ID2DDeviceCoNtext：： CreateGradientStopCollection** 頁面。

     

    ```C++
    // Create an array of gradient stops to put in the gradient stop
    // collection that will be used in the gradient brush.
    ID2D1GradientStopCollection *pGradientStops = NULL;

    D2D1_GRADIENT_STOP gradientStops[2];
    gradientStops[0].color = D2D1::ColorF(D2D1::ColorF::Yellow, 1);
    gradientStops[0].position = 0.0f;
    gradientStops[1].color = D2D1::ColorF(D2D1::ColorF::ForestGreen, 1);
    gradientStops[1].position = 1.0f;
    // Create the ID2D1GradientStopCollection from a previously
    // declared array of D2D1_GRADIENT_STOP structs.
    hr = m_pRenderTarget->CreateGradientStopCollection(
        gradientStops,
        2,
        D2D1_GAMMA_2_2,
        D2D1_EXTEND_MODE_CLAMP,
        &pGradientStops
        );
    ```

    

3.  使用 [**ID2D1RenderTarget：： CreateLinearGradientBrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) 建立線性漸層筆刷、填滿筆刷的正方形，然後以黑色色彩筆刷繪製正方形。
    ```C++
    // The line that determines the direction of the gradient starts at
    // the upper-left corner of the square and ends at the lower-right corner.

    if (SUCCEEDED(hr))
    {
        hr = m_pRenderTarget->CreateLinearGradientBrush(
            D2D1::LinearGradientBrushProperties(
                D2D1::Point2F(0, 0),
                D2D1::Point2F(150, 150)),
            pGradientStops,
            &m_pLinearGradientBrush
            );
    }
    ```

    

    ```C++
    m_pRenderTarget->FillRectangle(&rcBrushRect, m_pLinearGradientBrush);
    m_pRenderTarget->DrawRectangle(&rcBrushRect, m_pBlackBrush, 1, NULL);
    ```

    

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct2D 參考](reference.md)
</dt> </dl>

 

 
