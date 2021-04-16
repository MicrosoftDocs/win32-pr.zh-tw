---
description: 本節說明如何在 XPS OM 中使用 XPS 檔 API 的路徑相關介面。
ms.assetid: 4e76355a-ad53-4177-b8c7-3e768a1d4e3f
title: 使用 XPS OM 路徑介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca66b65c6f20dc3b585de706e223df1f76d518a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513564"
---
# <a name="working-with-xps-om-path-interfaces"></a>使用 XPS OM 路徑介面

本節說明如何在 XPS OM 中使用 XPS 檔 API 的路徑相關介面。



| 介面名稱                                                            | 概念子系                                                                                                                                                                                                                                                                                                                                                                                                                                         | Description                                                                                                                                                                                       |
|---------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)<br/>                               | 無<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | 描述圖形路徑元素。<br/>                                                                                                                                                    |
| [**IXpsOMBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush)<br/>                             | [**IXpsOMSolidColorBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush)<br/> [**IXpsOMTileBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomtilebrush)<br/> [**IXpsOMVisualBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush)<br/> [**IXpsOMImageBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush)<br/> [**IXpsOMGradientBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientbrush)<br/> [**IXpsOMLinearGradientBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomlineargradientbrush)<br/> [**IXpsOMRadialGradientBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomradialgradientbrush)<br/> | 筆刷用來填滿區域或線條。<br/>                                                                                                                                             |
| [**IXpsOMSolidColorBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush)<br/>         | 無<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | 提供純色填滿或筆觸。 <br/>                                                                                                                                                |
| [**IXpsOMVisualBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush)<br/>                 | 無<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | 提供視覺物件，例如路徑、圖像或畫布，或用來作為並排顯示或筆觸的部分視覺效果。 <br/>                                                                  |
| [**IXpsOMImageBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush)<br/>                   | 無<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | 提供影像 (或部分影像) 用來作為並排填填滿或筆觸。 <br/>                                                                                                           |
| [**IXpsOMLinearGradientBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomlineargradientbrush)<br/> | 無<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | 提供用來作為填滿或筆觸的線性漸層。 <br/>                                                                                                                            |
| [**IXpsOMRadialGradientBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomradialgradientbrush)<br/> | 無<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | 提供用來作為填滿或筆觸的放射漸層。 <br/>                                                                                                                            |
| [**IXpsOMGradientStop**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientstop)<br/>               | 無<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | 定義線性或放射漸層內的單一色彩值變化點。 <br/>                                                                                                     |
| [**IXpsOMGeometry**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry)<br/>                       | [**IXpsOMGeometryFigure**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure)<br/>                                                                                                                                                                                                                                                                                                                                                                                             | 提供要當做裁剪區域或路徑定義使用之向量區域的定義。 包含一或多個 [**IXpsOMGeometryFigure**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure) 介面。 <br/> |
| [**IXpsOMGeometryFigure**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure)<br/>           | 無<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | 區域定義的一部分，由 [**IXpsOMGeometry**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry) 介面參考，且包含一或多個區段。 <br/>                                    |
| [**IXpsOMMatrixTransform**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform)<br/>         | 無<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | 指定在呈現期間要套用至物件的仿射矩陣轉換。 <br/>                                                                                              |



 

## <a name="contents"></a>目錄

-   [XPS OM 筆刷](xps-object-model-brushes.md)
-   [XPS OM 漸層](xps-object-model-gradients.md)
-   [XPS OM 幾何物件](xps-object-model-geometry-objects.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IXpsOMPath 介面**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)
</dt> <dt>

[**IXpsOMDashCollection 介面**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdashcollection)
</dt> <dt>

[**IXpsOMMatrixTransform 介面**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform)
</dt> </dl>

 

 




