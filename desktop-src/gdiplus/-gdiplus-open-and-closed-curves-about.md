---
description: 下圖顯示兩個曲線：一個開啟，另一個已關閉。
ms.assetid: e0fb8ba1-1783-4b36-93d8-f1242425d8bd
title: 開啟與關閉的曲線
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 383f7c68909a73291c00c6e760d1cc6554b061d5749b33e6e90ba3a986c71906
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117885123"
---
# <a name="open-and-closed-curves"></a>開啟與關閉的曲線

下圖顯示兩個曲線：一個開啟，另一個已關閉。

![開啟曲線 (曲線) 和封閉曲線 (圖形大綱的圖例) ](images/aboutgdip02-art24.png)

封閉曲線有內部，因此可以使用筆刷填滿。 Windows GDI+ 中的 [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)類別提供下列方法來填寫封閉的圖形和曲線： [graphicswindow.fillrectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(constbrush_constrect_))、 [FillEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(constbrush_constrect_))、 [FillPie](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpie(inconstbrush_inreal_inreal_inreal_inreal_inreal_inreal))、 [FillPolygon](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpolygon(inconstbrush_inconstpoint_inint))、 [FillClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpoint_inint))、 [**graphics：： FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath)和 [**graphics：： FillRegion**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillregion)。 每當您呼叫其中一個方法時，您必須將其中一個特定筆刷型別的位址傳遞 ([**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush)、 [**HatchBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush)、 [**TextureBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-texturebrush)、 [**LinearGradientBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush)或 [**PathGradientBrush**](/windows/win32/api/gdipluspath/nl-gdipluspath-pathgradientbrush)) 做為引數。

[FillPie](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpie(inconstbrush_inreal_inreal_inreal_inreal_inreal_inreal))方法是[DrawArc](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inint_inint_inint_inint_inreal_inreal))方法的隨附。 如同 DrawArc 方法繪製橢圓形外框的一部分，FillPie 方法會填滿橢圓形內部的部分。 下列範例會繪製弧形並填滿橢圓內部的對應部分。


```
myGraphics.FillPie(&mySolidBrush, 0, 0, 140, 70, 0, 120);
myGraphics.DrawArc(&myPen, 0, 0, 140, 70, 0, 120);
```



下圖顯示弧線和填滿的圓形圖。

![顯示填滿橢圓形區段的圖例](images/aboutgdip02-art25.png)

[FillClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpoint_inint))方法是[DrawClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawclosedcurve(inconstpen_inconstpoint_inint))方法的隨附。 這兩種方法都會藉由將結束點連接到起點，來自動關閉曲線。 下列範例繪製的曲線會通過 (0、0) 、 (60、20) 和 (40、50) 。 然後，會將 (40、50) 連接至起點 (0、0) ，然後將內部填滿純色，以自動關閉曲線。


```
Point myPointArray[] =
   {Point(10, 10), Point(60, 20),Point(40, 50)};
myGraphics.DrawClosedCurve(&myPen, myPointArray, 3);
myGraphics.FillClosedCurve(&mySolidBrush, myPointArray, 3, FillModeAlternate)
```



路徑可以包含數個圖形 (子路徑) 。 [**Graphics：： FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath)方法會填滿每個圖形的內部。 如果未關閉圖表， **Graphics：： FillPath** 方法會填滿在圖形關閉時所要括住的區域。 下列範例會繪製和填滿由弧線、基線曲線、字串和圓形圖組成的路徑。


```
myGraphics.FillPath(&mySolidBrush, &myGraphicsPath);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



下圖顯示以純色筆刷填滿之前和之後的路徑。 請注意，字串中的文字是由 [**圖形：:D rawpath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) 方法所組成，但是未填滿。 它是繪製字串中字元內部的 [**Graphics：： FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) 方法。

![圖例：兩次顯示文字和開啟和封閉曲線;這些是第一次是空的，而且會填滿第二次](images/aboutgdip02-art26.png)

 

 



