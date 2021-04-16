---
title: 如何繪製和填滿基本圖形
description: 本主題說明如何繪製基本圖形。
ms.assetid: 8a68fc3f-118c-447b-856c-05417ae4ef29
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 6b6b5a6fb08ac962475c2f0aa2812b4c3ae5da03
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104551899"
---
# <a name="how-to-draw-and-fill-a-basic-shape"></a>如何繪製和填滿基本圖形

本主題說明如何繪製基本圖形。 [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)介面提供了用來大綱和填滿省略號、矩形和線條的方法。 下列範例示範如何建立和繪製橢圓形。

本主題包含下列幾節：

-   [以實心筆觸繪製橢圓形的外框](#draw-the-outline-of-an-ellipse-with-a-solid-stroke)
-   [使用虛線筆觸繪製橢圓形](#draw-an-ellipse-with-a-dashed-stroke)
-   [繪製和填滿橢圓形](#draw-and-fill-an-ellipse)
-   [繪製更複雜的圖形](#drawing-more-complex-shapes)
-   [相關主題](#related-topics)

## <a name="draw-the-outline-of-an-ellipse-with-a-solid-stroke"></a>以實心筆觸繪製橢圓形的外框

若要繪製橢圓形的輪廓，您可以定義筆刷 (例如 [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) 或 [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)) 來繪製外框，並使用 [**D2D1 \_ 橢圓形**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse) 來描述橢圓形的位置和維度，然後將這些物件傳遞給 [**ID2D1RenderTarget：:D rawellipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) 方法。 下列範例會建立黑色純色筆刷，並將其儲存在 m \_ spBlackBrush 類別成員中。


```C++
hr = m_pRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF::Black),
    &m_pBlackBrush
    );
```



下一個範例會定義 [**D2D1 \_ 橢圓形**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse) ，並使用它與前一個範例中定義的筆刷來繪製橢圓形的輪廓。 此範例會產生下圖所示的輸出。

![具有實心筆觸的橢圓形圖例](images/drawandfillellipseexample-1.png)


```C++
D2D1_ELLIPSE ellipse = D2D1::Ellipse(
    D2D1::Point2F(100.f, 100.f),
    75.f,
    50.f
    );

m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f);
```



## <a name="draw-an-ellipse-with-a-dashed-stroke"></a>使用虛線筆觸繪製橢圓形

上述範例使用了純筆劃。 您可以藉由建立 [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle)，以數種方式修改筆劃的外觀。 **ID2D1StrokeStyle** 可讓您在筆劃的開頭和結尾指定圖形（不論是否有虛線模式），依此類推。 下列範例會建立描述虛線筆劃的 **ID2D1StrokeStyle** 。 這個範例會使用預先定義的虛線模式 [**D2D1 \_ 虛線 \_ 樣式 \_ 虛線 \_ 點 \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_dash_style)，但是您也可以指定自己的虛線樣式。


```C++
D2D1_STROKE_STYLE_PROPERTIES strokeStyleProperties = D2D1::StrokeStyleProperties(
    D2D1_CAP_STYLE_FLAT,  // The start cap.
    D2D1_CAP_STYLE_FLAT,  // The end cap.
    D2D1_CAP_STYLE_TRIANGLE, // The dash cap.
    D2D1_LINE_JOIN_MITER, // The line join.
    10.0f, // The miter limit.
    D2D1_DASH_STYLE_DASH_DOT_DOT, // The dash style.
    0.0f // The dash offset.
    );

hr = m_pDirect2dFactory->CreateStrokeStyle(strokeStyleProperties, NULL, 0, &m_pStrokeStyle);

```



下一個範例會使用筆觸樣式搭配 [**DrawEllipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) 方法。 此範例會產生下圖所示的輸出。

![具有虛線筆觸的橢圓形圖例](images/drawandfillellipseexample-2.png)


```C++
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f, m_pStrokeStyle);
```



## <a name="draw-and-fill-an-ellipse"></a>繪製和填滿橢圓形

若要繪製橢圓形的內部，請使用 [**FillEllipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) 方法。 下列範例會使用 [**DrawEllipse**]/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse (constd2d1_ellipse__id2d1brush_float_id2d1strokestyle) ) 方法來勾勒出橢圓形，然後使用 **FillEllipse** 方法來繪製其內部。 此範例會產生下圖所示的輸出。

![橢圓形的圖例，其中含有虛線筆觸，然後以純灰色色彩填滿](images/drawandfillellipseexample-3.png)


```C++
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f, m_pStrokeStyle);
m_pRenderTarget->FillEllipse(ellipse, m_pSilverBrush);
```



下一個範例會先填滿橢圓形，然後繪製其輪廓。 此範例會產生下圖所示的輸出。

![以純色筆觸填滿的橢圓形圖例，然後以虛線筆觸表示](images/drawandfillellipseexample-4.png)


```C++
m_pRenderTarget->FillEllipse(ellipse, m_pSilverBrush);
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f, m_pStrokeStyle);
```



這些範例中已省略程式碼。

## <a name="drawing-more-complex-shapes"></a>繪製更複雜的圖形

若要繪製更複雜的圖形，您可以定義 ID2D1Geometry 物件，並使用這些物件搭配 [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) 和 [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) 方法。 如需詳細資訊，請參閱 [幾何總覽](direct2d-geometries-overview.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[幾何概觀](direct2d-geometries-overview.md)
</dt> <dt>

[筆刷概觀](direct2d-brushes-overview.md)
</dt> </dl>

 

 