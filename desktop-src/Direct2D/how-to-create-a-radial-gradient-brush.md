---
title: 如何建立放射狀漸層筆刷
description: 顯示如何使用 Direct2D 建立放射狀漸層筆刷。
ms.assetid: 663743c9-16e9-4e3a-90b2-883ef0b8d5cf
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: fe3509a80f80132f4a5e5d65f62476be1cac61d1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104186014"
---
# <a name="how-to-create-a-radial-gradient-brush"></a>如何建立放射狀漸層筆刷

若要建立放射狀漸層筆刷，請使用 [**ID2DRenderTarget：： CreateRadialGradientBrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush)) 方法，並指定星形漸層筆刷屬性和漸層停駐點集合。 某些多載可讓您指定筆刷屬性。 下列程式碼示範如何建立放射狀漸層筆刷來填滿圓形，以及建立實心黑色筆刷來繪製圓形的外框。

程式碼會產生下圖中顯示的輸出。

![填滿放射狀漸層筆刷的圓形圖例](images/brushes-ovw-radials.png)

1.  宣告 [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)型別的變數。
    ```C++
        ID2D1RadialGradientBrush *m_pRadialGradientBrush;
    ```

    

2.  建立 [**D2D1 \_ 梯度 \_ 停**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop) 用結構的陣列，以放入漸層停駐點集合。 **D2D1 \_ 梯度停駐 \_ 點** 結構包含漸層停駐點的位置和色彩。 位置表示筆刷中漸層停駐點的相對位置。 值的範圍為 \[ 0.0 f、1.0 f \] ，如下列程式碼所示。

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

    

3.  您可以使用 [**ID2D1RenderTarget：： CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection))方法，從先前宣告的 [**D2D1 \_ 梯度 \_ 停**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop)用結構陣列建立 [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection)集合。 然後，使用 [**CreateRadialGradientBrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush)) 建立放射狀漸層筆刷。

    > [!Note]  
    > 從 Windows 8 開始，您可以使用 [**ID2D1DeviceCoNtext：： CreateGradientStopCollection**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-creategradientstopcollection) 方法來建立 [**ID2D1GradientStopCollection1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1gradientstopcollection1) 集合，而不是 [**ID2D1RenderTarget：： CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) 方法。 此介面會以直線或 prmultiplied 色彩新增高彩漸層和漸層的插補。 如需詳細資訊，請參閱 **ID2DDeviceCoNtext：： CreateGradientStopCollection** 頁面。

     

    ```C++
    // The center of the gradient is in the center of the box.
    // The gradient origin offset was set to zero(0, 0) or center in this case.
    if (SUCCEEDED(hr))
    {
        hr = m_pRenderTarget->CreateRadialGradientBrush(
            D2D1::RadialGradientBrushProperties(
                D2D1::Point2F(75, 75),
                D2D1::Point2F(0, 0),
                75,
                75),
            pGradientStops,
            &m_pRadialGradientBrush
            );
    }
    ```

    

    ```C++
    m_pRenderTarget->FillEllipse(ellipse, m_pRadialGradientBrush);
    m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 1, NULL);
    ```

    

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct2D 參考](reference.md)
</dt> </dl>

 

 