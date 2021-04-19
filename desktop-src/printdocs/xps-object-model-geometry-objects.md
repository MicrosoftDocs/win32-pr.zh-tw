---
description: 本主題提供在 XPS OM 中使用 geometry 相關介面的範例。
ms.assetid: 2663c6fc-301e-4765-b37c-b5e29a714ce8
title: XPS OM 幾何物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cca767de311d2f2d49b0b194c372c0e69eaa637c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106996667"
---
# <a name="xps-om-geometry-objects"></a>XPS OM 幾何物件

本主題提供在 XPS OM 中使用 geometry 相關介面的範例。

## <a name="create-a-rectangular-geometry"></a>建立矩形幾何

下列程式碼範例會建立描述封閉矩形圖形的 geometry 物件。


```C++
    HRESULT                         hr = S_OK;
    IXpsOMVisualCollection          *canvasVisuals = NULL;
    IXpsOMPath                      *pathSidebar = NULL;
    IXpsOMGeometry                  *xpsGeometry = NULL;
    IXpsOMGeometryFigure            *xpsFigure = NULL;
    IXpsOMGeometryFigureCollection  *xpsFigureCollection = NULL;
    IXpsOMSolidColorBrush           *sidebarBrush = NULL;

    XPS_POINT      startPoint;
    XPS_RECT       shape;

    // define the rectangle
    shape.x = 10.0f;
    shape.y = 10.0f;
    shape.height = 100.0f;
    shape.width = 200.0f;

    // set the start point
    startPoint.x = shape.x;
    startPoint.y = shape.y;

    // define the segment types to be straight lines
    XPS_SEGMENT_TYPE sidebarSegmentTypes[3] = {
        XPS_SEGMENT_TYPE_LINE, 
        XPS_SEGMENT_TYPE_LINE, 
        XPS_SEGMENT_TYPE_LINE
    };

    // define the points of the rectangular shape
    // other than the start point
    FLOAT sidebarSegmentData[6] = {
        shape.x,               shape.y + shape.height,
        shape.x + shape.width, shape.y + shape.height,
        shape.x + shape.width, shape.y
    };

    // set the lines to be solid (not stroked)
    BOOL sidebarSegmentStrokes[3] = {
        FALSE, FALSE, FALSE
    };

    // create the geometry figure interface
    hr = xpsFactory->CreateGeometryFigure( &startPoint, &xpsFigure );

    // close the figure so that the last segment point is
    // connected to the start point
    hr = xpsFigure->SetIsClosed( TRUE );

    // set the shape to be filled by the fill brush
    hr = xpsFigure->SetIsFilled( TRUE );

    // set the segments using the information defined above
    hr = xpsFigure->SetSegments(
        3, 
        6, 
        sidebarSegmentTypes,
        sidebarSegmentData, 
        sidebarSegmentStrokes);

    // create a geometry using the figure just created
    hr = xpsFactory->CreateGeometry(&xpsGeometry);

    // get a pointer to the figure collection
    hr = xpsGeometry->GetFigures(&xpsFigureCollection);

    // and add the figure of the rectangle to the geometry
    hr = xpsFigureCollection->Append(xpsFigure);
```



如需將區段新增至幾何圖的詳細資訊，請參閱 [**IXpsOMGeometryFigure：： GetSegmentData 方法**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgeometryfigure-getsegmentdata) 和 [**IXpsOMGeometryFigure：： SetSegments 方法**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgeometryfigure-setsegments) 參考主題中的程式碼範例。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IXpsOMGeometry 介面**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry)
</dt> <dt>

[**IXpsOMGeometryFigure 介面**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure)
</dt> <dt>

[**IXpsOMGeometryFigure：： GetSegmentData 方法**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgeometryfigure-getsegmentdata)
</dt> <dt>

[**IXpsOMGeometryFigure：： SetSegments 方法**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgeometryfigure-setsegments)
</dt> <dt>

[**IXpsOMGeometryFigureCollection 介面**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigurecollection)
</dt> </dl>

 

 



