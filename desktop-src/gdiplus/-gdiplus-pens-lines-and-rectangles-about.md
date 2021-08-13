---
description: 若要使用 Windows 繪製線條 GDI+ 您需要建立繪圖物件和 Pen 物件。
ms.assetid: d91562ab-41e6-4bca-a320-74f490a4f88f
title: 畫筆、線條和矩形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb8ac54d1e98a617492aa6f5f1194767fc56a34ffcaaee71ba71753dda08f8bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119359588"
---
# <a name="pens-lines-and-rectangles"></a>畫筆、線條和矩形

若要使用 Windows 繪製線條 GDI+ 您需要建立 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)物件和 [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen)物件。 **Graphics** 物件提供實際繪製繪圖的方法，而 **Pen** 物件會儲存線條的屬性，例如色彩、寬度和樣式。 繪製線條只是呼叫 **Graphics** 物件的 [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint))方法。 **畫筆** 物件的位址會做為 DrawLine 方法的其中一個引數傳遞。 下列範例會繪製從點 (4，2) 到 (12，6) 點的直線。


```
myGraphics.DrawLine(&myPen, 4, 2, 12, 6);
```



[DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inconstpoint__inconstpoint_)) 是 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 類別的多載方法，因此您可以透過數種方式提供引數給它。 例如，您可以建立兩個 [**point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) 物件，並將 **point** 物件的參考傳遞為 DrawLine 方法的引數。


```
Point myStartPoint(4, 2);
Point myEndPoint(12, 6);
myGraphics.DrawLine(&myPen, myStartPoint, myEndPoint);
```



當您建立 [**畫筆**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) 物件時，可以指定某些屬性。 例如，一個 [畫筆](/windows/win32/api/gdipluspen/nf-gdipluspen-pen-pen(constpen_)) 的函式可讓您指定色彩和寬度。 下列範例會從 (0、0) 到 (60 30) ，繪製一條寬度2的藍色線。


```
Pen myPen(Color(255, 0, 0, 255), 2);
myGraphics.DrawLine(&myPen, 0, 0, 60, 30);
```



[**畫筆**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen)物件也有屬性（例如虛線樣式），您可以用來指定線條的功能。 例如，下列範例會繪製從 (100，50) 到 (300，80) 的虛線。


```
myPen.SetDashStyle(DashStyleDash);
myGraphics.DrawLine(&myPen, 100, 50, 300, 80);
```



您可以使用 [ [**畫筆**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) ] 物件的各種方法來設定該線條的許多屬性。 [**Pen：： SetStartCap**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setstartcap)和 [**Pen：： SetEndCap**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setendcap)方法會指定線條結尾的外觀;結尾可以是平面、正方形、圓角、三角形或自訂形狀。 [**Pen：： SetLineJoin**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin)方法可讓您指定連接線是否為斜接 (聯結) 、斜面、圓角或裁剪的尖角。 下圖顯示具有各種端點和聯結樣式的行。

![這兩行的圖解，示範圓角和圓形結束、圓角和斜接角，以及兩個箭號樣式](images/aboutgdip02-art04.png)

使用 GDI+ 繪製矩形類似于繪製線條。 若要繪製矩形，您需要 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件和 [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) 物件。 **Graphics** 物件提供 [graphicswindow.drawrectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint))方法，而 **Pen** 物件會儲存屬性，例如線條寬度和色彩。 **畫筆** 物件的位址會做為 graphicswindow.drawrectangle 方法的其中一個引數傳遞。 下列範例會在 (100、50) 、寬度為80且高度為40的情況下，繪製一個矩形，其左上角。


```
myGraphics.DrawRectangle(&myPen, 100, 50, 80, 40);
```



[Graphicswindow.drawrectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) 是 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 類別的多載方法，因此您可以透過數種方式提供引數給它。 例如，您可以建立 [**rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) 物件，並將 **rect** 物件的參考傳遞為 graphicswindow.drawrectangle 方法的引數。


```
Rect myRect(100, 50, 80, 40);
myGraphics.DrawRectangle(&myPen, myRect);
```



[**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect)物件有方法可操作和收集矩形的相關資訊。 例如，擴充和[位移](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-offset(inconstpoint_))方法會變更矩形的[大小和位置](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-inflate(inint_inint))。 [**Rect：： IntersectsWith**](/windows/win32/api/Gdiplustypes/nf-gdiplustypes-rect-intersectswith)方法會告訴您矩形是否與另一個指定的矩形相交，而 [Contains](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-contains(inint_inint))方法會告訴您指定的點是否在矩形內。

 

 
