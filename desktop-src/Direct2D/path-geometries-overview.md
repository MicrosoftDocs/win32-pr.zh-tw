---
title: 路徑幾何總覽
description: 描述如何使用路徑幾何來定義複雜的圖形。
ms.assetid: 38a290be-b915-4317-b9b1-0e49e40dc8ec
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 0189c46f50e2ccc9ecc4523a4bb6f34006e59139
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/28/2021
ms.locfileid: "104568766"
---
# <a name="path-geometries-overview"></a>路徑幾何總覽

本主題說明如何使用 Direct2D 路徑幾何來建立複雜的繪圖。 包含以下幾節。

-   [先決條件](#prerequisites)
-   [Direct2D 中的路徑幾何](#path-geometries-in-direct2d)
-   [使用 ID2D1GeometrySink 來填入路徑幾何](#using-an-id2d1geometrysink-to-populate-a-path-geometry)
-   [範例：建立複雜的繪圖](#example-create-a-complex-drawing)
    -   [建立左方山地的路徑幾何](#create-a-path-geometry-for-the-left-mountain)
    -   [建立適用于右山地的路徑幾何](#create-a-path-geometry-for-the-right-mountain)
    -   [建立 Sun 的路徑幾何](#create-a-path-geometry-for-the-sun)
    -   [建立河的路徑幾何](#create-a-path-geometry-for-the-river)
    -   [將路徑幾何轉譯至顯示](#render-the-path-geometries-onto-the-display)
-   [相關主題](#related-topics)

## <a name="prerequisites"></a>必要條件

本總覽假設您已經熟悉如何建立基本的 Direct2D 應用程式，如 [建立簡單的 Direct2D 應用程式](direct2d-quickstart.md)中所述。 它也假設您已熟悉 Direct2D 幾何的基本功能，如 [幾何總覽](direct2d-geometries-overview.md)中所述。

## <a name="path-geometries-in-direct2d"></a>Direct2D 中的路徑幾何

路徑幾何會以 [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) 介面表示。 若要具現化路徑幾何，請呼叫 [**ID2D1Factory：： CreatePathGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) 方法。 這些物件可用來描述由弧線、曲線和線條等線段組成的複雜幾何圖形。 若要在路徑幾何中填入圖表和區段，請呼叫 [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) 方法來取出 [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) ，並使用 geometry 接收器的方法將圖形和區段加入至路徑幾何。

## <a name="using-an-id2d1geometrysink-to-populate-a-path-geometry"></a>使用 ID2D1GeometrySink 來填入路徑幾何

[**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) 描述的幾何路徑可以包含線條、弧線、三次方貝茲曲線，以及二次方貝茲曲線。

幾何接收器是由一或多個圖表所組成。 每個圖表都是由一或多個線條、曲線或弧線區段所組成。 若要建立圖表，請呼叫 [**BeginFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure) 方法，並傳入圖表的起點，然後使用其 add 方法 (例如 [**AddLine**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometrysink-addline) 和 [**AddBezier**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) 來加入區段。 當您完成加入區段時，請呼叫 [**EndFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-endfigure) 方法。 您可以重複此順序來建立其他圖形。 當您完成建立圖表時，請呼叫 [**Close**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-close) 方法。

## <a name="example-create-a-complex-drawing"></a>範例：建立複雜的繪圖

下圖顯示具有線條、弧形和貝茲曲線的複雜繪圖。 接下來的程式碼範例會示範如何使用四個路徑幾何物件（一個用於左方的山區）來建立繪圖、將一個用於右山地、一個用於一張，以及一個適用于 sun 的光暈。

![使用路徑幾何的河、山脈和 sun 圖例](images/path-geo-mnts.png)

### <a name="create-a-path-geometry-for-the-left-mountain"></a>建立左方山地的路徑幾何

此範例會先建立左方山地的路徑幾何，如下圖所示。

![顯示表示山地的多邊形複雜繪圖。](images/path-geo-leftmnt.png)

為了建立左方的山，此範例會呼叫 [**ID2D1Factory：： CreatePathGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) 方法來建立 [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry)。


```C++
hr = m_pD2DFactory->CreatePathGeometry(&m_pLeftMountainGeometry);
```



然後，此範例會使用 [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) 方法從 [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) 取得幾何接收器，並將其儲存在 *pSink* 變數中。


```C++
ID2D1GeometrySink *pSink = NULL;
hr = m_pLeftMountainGeometry->Open(&pSink);
```



然後，此範例會呼叫 [**BeginFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure)，並在 [**D2D1 \_ 圖中 \_ \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_figure_begin) 傳入，指出此圖表已填滿，然後呼叫 [**AddLines**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-addlines)，傳入 [**D2D1 \_ 點 \_**](d2d1-point-2f.md) 的陣列、 (267、177) 、 (236、192) 、 (212、160) 、 (156、255) 和 (346、255) 。

下列程式碼示範如何執行這項操作。


```C++
pSink->SetFillMode(D2D1_FILL_MODE_WINDING);

pSink->BeginFigure(
    D2D1::Point2F(346,255),
    D2D1_FIGURE_BEGIN_FILLED
    );
D2D1_POINT_2F points[5] = {
   D2D1::Point2F(267, 177),
   D2D1::Point2F(236, 192),
   D2D1::Point2F(212, 160),
   D2D1::Point2F(156, 255),
   D2D1::Point2F(346, 255), 
   };
pSink->AddLines(points, ARRAYSIZE(points));
pSink->EndFigure(D2D1_FIGURE_END_CLOSED);
```



### <a name="create-a-path-geometry-for-the-right-mountain"></a>建立適用于右山地的路徑幾何

接著，此範例會為右山建立另一個路徑幾何，其點為 (481、146) 、 (449、181) 、 (433、159) 、 (401、214) 、 (381、199) 、 (323、263) 和 (575、263) 。 下圖顯示如何顯示右邊的山地。

![顯示山地的多邊形圖例](images/path-geo-rightmnt.png)

下列程式碼示範如何執行這項操作。


```C++
        hr = m_pD2DFactory->CreatePathGeometry(&m_pRightMountainGeometry);
        if(SUCCEEDED(hr))
        {
            ID2D1GeometrySink *pSink = NULL;

            hr = m_pRightMountainGeometry->Open(&pSink);
            if (SUCCEEDED(hr))
            {
                pSink->SetFillMode(D2D1_FILL_MODE_WINDING);

                pSink->BeginFigure(
                    D2D1::Point2F(575,263),
                    D2D1_FIGURE_BEGIN_FILLED
                    );
                D2D1_POINT_2F points[] = {
                   D2D1::Point2F(481, 146),
                   D2D1::Point2F(449, 181),
                   D2D1::Point2F(433, 159),
                   D2D1::Point2F(401, 214),
                   D2D1::Point2F(381, 199), 
                   D2D1::Point2F(323, 263), 
                   D2D1::Point2F(575, 263)
                   };
                pSink->AddLines(points, ARRAYSIZE(points));
                pSink->EndFigure(D2D1_FIGURE_END_CLOSED);
            }
            hr = pSink->Close();

            SafeRelease(&pSink);
       }
```



### <a name="create-a-path-geometry-for-the-sun"></a>建立 Sun 的路徑幾何

然後，此範例會將另一個路徑幾何填入至太陽，如下圖所示。

![顯示太陽的弧形和貝茲曲線圖例](images/path-geo-sun.png)

若要這樣做，路徑幾何會建立一個接收，然後將每個光暈的曲線和一個圖表加入至接收器。 藉由重複 [**BeginFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure)順序，其 Add (例如 [**AddBezier**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget))) 方法和 [**EndFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-endfigure)，會將多個資料新增至接收器。

下列程式碼示範如何執行這項操作。


```C++
        hr = m_pD2DFactory->CreatePathGeometry(&m_pSunGeometry);
        if(SUCCEEDED(hr))
        {
            ID2D1GeometrySink *pSink = NULL;

            hr = m_pSunGeometry->Open(&pSink);
            if (SUCCEEDED(hr))
            {
                pSink->SetFillMode(D2D1_FILL_MODE_WINDING);
            
                pSink->BeginFigure(
                    D2D1::Point2F(270, 255),
                    D2D1_FIGURE_BEGIN_FILLED
                    );
                pSink->AddArc(
                    D2D1::ArcSegment(
                        D2D1::Point2F(440, 255), // end point
                        D2D1::SizeF(85, 85),
                        0.0f, // rotation angle
                        D2D1_SWEEP_DIRECTION_CLOCKWISE,
                        D2D1_ARC_SIZE_SMALL
                        ));            
                pSink->EndFigure(D2D1_FIGURE_END_CLOSED);

                pSink->BeginFigure(
                    D2D1::Point2F(299, 182),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(299, 182),
                       D2D1::Point2F(294, 176),
                       D2D1::Point2F(285, 178)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(276, 179),
                       D2D1::Point2F(272, 173),
                       D2D1::Point2F(272, 173)
                       ));
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);

                pSink->BeginFigure(
                    D2D1::Point2F(354, 156),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(354, 156),
                       D2D1::Point2F(358, 149),
                       D2D1::Point2F(354, 142)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(349, 134),
                       D2D1::Point2F(354, 127),
                       D2D1::Point2F(354, 127)
                       ));
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);

                pSink->BeginFigure(
                    D2D1::Point2F(322,164),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(322, 164),
                       D2D1::Point2F(322, 156),
                       D2D1::Point2F(314, 152)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(306, 149),
                       D2D1::Point2F(305, 141),
                       D2D1::Point2F(305, 141)
                       ));              
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);

                pSink->BeginFigure(
                    D2D1::Point2F(385, 164),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(385,164),
                       D2D1::Point2F(392,161),
                       D2D1::Point2F(394,152)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(395,144),
                       D2D1::Point2F(402,141),
                       D2D1::Point2F(402,142)
                       ));                
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);

                pSink->BeginFigure(
                    D2D1::Point2F(408,182),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(408,182),
                       D2D1::Point2F(416,184),
                       D2D1::Point2F(422,178)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(428,171),
                       D2D1::Point2F(435,173),
                       D2D1::Point2F(435,173)
                       ));
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);
            }
            hr = pSink->Close();

            SafeRelease(&pSink);
       }
```



### <a name="create-a-path-geometry-for-the-river"></a>建立河的路徑幾何

然後，此範例會為包含貝茲曲線的河建立另一個幾何路徑。 下圖顯示的是如何顯示中的。

![顯示河的貝茲曲線圖例](images/path-geo-river.png)

下列程式碼示範如何執行這項操作。


```C++
        hr = m_pD2DFactory->CreatePathGeometry(&m_pRiverGeometry);
    
        if(SUCCEEDED(hr))
        {
            ID2D1GeometrySink *pSink = NULL;

            hr = m_pRiverGeometry->Open(&pSink);
            if (SUCCEEDED(hr))
            {
                pSink->SetFillMode(D2D1_FILL_MODE_WINDING);
                pSink->BeginFigure(
                    D2D1::Point2F(183, 392),
                    D2D1_FIGURE_BEGIN_FILLED
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(238, 284),
                       D2D1::Point2F(472, 345),
                       D2D1::Point2F(356, 303)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(237, 261),
                       D2D1::Point2F(333, 256),
                       D2D1::Point2F(333, 256)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(335, 257),
                       D2D1::Point2F(241, 261),
                       D2D1::Point2F(411, 306)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(574, 350),
                       D2D1::Point2F(288, 324),
                       D2D1::Point2F(296, 392)
                       ));
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);
            }
```



### <a name="render-the-path-geometries-onto-the-display"></a>將路徑幾何轉譯至顯示

下列程式碼示範如何在顯示上呈現已填入的路徑幾何。 它會先繪製和繪製 sun 幾何、左方的山地幾何、下出的幾何，最後是右邊的山地幾何。


```C++
 m_pRenderTarget->BeginDraw();

 m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

 m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

 D2D1_SIZE_F rtSize = m_pRenderTarget->GetSize();
 m_pRenderTarget->FillRectangle(
     D2D1::RectF(0, 0, rtSize.width, rtSize.height),
     m_pGridPatternBitmapBrush
     );

 m_pRenderTarget->FillGeometry(m_pSunGeometry, m_pRadialGradientBrush);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::Black, 1.f));
 m_pRenderTarget->DrawGeometry(m_pSunGeometry, m_pSceneBrush, 1.f);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::OliveDrab, 1.f));
 m_pRenderTarget->FillGeometry(m_pLeftMountainGeometry, m_pSceneBrush);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::Black, 1.f));
 m_pRenderTarget->DrawGeometry(m_pLeftMountainGeometry, m_pSceneBrush, 1.f);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::LightSkyBlue, 1.f));
 m_pRenderTarget->FillGeometry(m_pRiverGeometry, m_pSceneBrush);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::Black, 1.f));
 m_pRenderTarget->DrawGeometry(m_pRiverGeometry, m_pSceneBrush, 1.f);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::YellowGreen, 1.f));
 m_pRenderTarget->FillGeometry(m_pRightMountainGeometry, m_pSceneBrush);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::Black, 1.f));
 m_pRenderTarget->DrawGeometry(m_pRightMountainGeometry, m_pSceneBrush, 1.f);


 hr = m_pRenderTarget->EndDraw();
```



完整的範例會輸出下圖。

![使用路徑幾何的河、山脈和 sun 圖例](images/path-geo-mnts.png)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立簡單的 Direct2D 應用程式](direct2d-quickstart.md)
</dt> <dt>

[幾何概觀](direct2d-geometries-overview.md)
</dt> </dl>

 

 