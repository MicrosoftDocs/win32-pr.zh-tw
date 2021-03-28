---
description: Windows GDI + 會在座標系統上繪製線條、矩形和其他圖形。
ms.assetid: a43bcb27-473b-4ca2-a937-2b54384ab86b
title: 向量圖形的概觀
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e9bfe98585ef8e073cf1c563c237436b7c982bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104569086"
---
# <a name="overview-of-vector-graphics"></a>向量圖形的概觀

Windows GDI + 會在座標系統上繪製線條、矩形和其他圖形。 您可以從各種不同的座標系統中進行選擇，但預設的座標系統在左上角有原點，X 軸指向右邊，y 軸則指向向下。 預設座標系統中的測量單位是圖元。

![以 X 軸向右展開，y 軸向下擴充的座標系統圖例](images/aboutgdip02-art01.png)

電腦監視器會以矩形陣列的點（稱為圖片元素或圖元）建立其顯示。 畫面上顯示的圖元數目會因某個監視器而異，而顯示在個別監視器上的圖元數目通常可以設定為使用者的某個範圍。

![矩形方格的圖例，該方格中有三個數據格，其座標標示](images/aboutgdip02-art02.png)

當您使用 GDI + 繪製線條、矩形或曲線時，您會提供有關要繪製之專案的特定索引鍵資訊。 例如，您可以藉由提供兩個點來指定線條，也可以藉由提供點、高度和寬度來指定矩形。 GDI + 會與顯示驅動程式軟體一起運作，以判斷哪些圖元必須開啟才能顯示線條、矩形或曲線。 下圖顯示已開啟的圖元，可顯示從點 (4，2) 到 (12，8) 點的線。

![圖例顯示矩形格線，其中儲存格已填滿，以指出兩個端點之間的線條](images/aboutgdip02-art03.png)

經過一段時間後，某些基本構成要素已證明是最適合用來建立二維圖片的部分。 下列清單提供所有由 GDI + 支援的組建區塊：

-   線條
-   矩形
-   橢圓形
-   弧
-   多邊形
-   基本曲線
-   貝茲曲線

GDI + 中的 [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 類別提供下列方法來繪製上一份清單中的專案： [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint))、 [graphicswindow.drawrectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint))、 [DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrectf_))、 [DrawPolygon](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpolygon(inconstpen_inconstpointf_inint))、 [DrawArc](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inconstrectf__inreal_inreal))、 [DrawCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcurve(inconstpen_inconstpoint_inint)) (用於基本曲線) 和 [DrawBezier](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbezier(inconstpen_inconstpoint__inconstpoint__inconstpoint__inconstpoint_))。 這些方法都是多載的：也就是說，每個方法都有數個不同的參數清單變化。 例如，DrawLine 方法的一個變化會接收 [**pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) 物件的位址和四個整數，而 DrawLine 方法的另一種變化則會接收 **pen** 物件的位址和兩個 [**點**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) 物件參考。

繪製線條、矩形和貝茲曲線的方法具有複數附屬方法，可在單一呼叫中繪製數個專案： [DrawLines](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawlines(inconstpen_inconstpointf_inint))、 [DrawRectangles](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangles(inconstpen_inconstrect_inint))和 [DrawBeziers](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbeziers(inconstpen_inconstpoint_inint))。 此外， [DrawCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcurve(inconstpen_inconstpoint_inint)) 方法也有附屬方法 [DrawClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawclosedcurve(inconstpen_inconstpoint_inint))，它會將曲線的結束點連接到起點來關閉曲線。

[**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)類別的所有繪圖方法都可以搭配 [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen)物件一起使用。 因此，為了繪製任何內容，您必須建立至少兩個物件： **圖形** 物件和 **畫筆** 物件。 **Pen** 物件會儲存要繪製之專案的屬性，例如線條寬度和色彩。 **畫筆** 物件的位址會做為繪圖方法的其中一個引數傳遞。 例如， [graphicswindow.drawrectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) 方法的其中一個變化會接收 **畫筆** 物件的位址和四個整數（如下列程式碼所示），其會繪製寬度為100的矩形、50的高度和 (20、10) 的左上角。


```
myGraphics.DrawRectangle(&myPen, 20, 10, 100, 50);
```



 

 



