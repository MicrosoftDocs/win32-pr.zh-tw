---
description: 路徑是藉由結合線條、矩形和簡單曲線來形成。 回想一下向量圖形，下列基本組建區塊已證明是最適合用來繪製圖片的概念。
ms.assetid: 88fea2ec-7b53-44bb-841d-486c5c879c68
title: 路徑 (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f54dae290138314cac3dae8d259591939490764d371e9a2caf9423801e985ec2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117695474"
---
# <a name="paths-gdi"></a>路徑 (GDI+)

路徑是藉由結合線條、矩形和簡單曲線來形成。 回想一下 [向量圖形](-gdiplus-overview-of-vector-graphics-about.md) ，下列基本組建區塊已證明是最適合用來繪製圖片的概念。

-   線條
-   矩形
-   橢圓形
-   弧
-   多邊形
-   基本曲線
-   貝茲曲線

在 Windows GDI+ 中， [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath)物件可讓您將這些建築物區塊的一連串收集到單一單位。 然後，您可以使用圖形類別 [**:D rawpath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) [**方法，繪製**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 線條、矩形、多邊形和曲線的整個序列。 下圖顯示藉由結合直線、弧線、貝茲曲線和基線曲線所建立的路徑。

![結合線條、弧線、貝茲曲線和基線曲線的路徑圖例](images/aboutgdip02-art14.png)

[**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath)類別提供下列方法來建立要繪製的專案序列： [AddLine](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addline(inint_inint_inint_inint))、 [AddRectangle](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addrectangle(inconstrectf_))、 [shapes.addellipse](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addellipse(inint_inint_inint_inint))、 [AddArc](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addarc(inint_inint_inint_inint_inreal_inreal))、 [AddPolygon](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addpolygon(inconstpointf_inint))、 [AddCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)) (用於基本曲線) 和 [AddBezier](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addbezier(inint_inint_inint_inint_inint_inint_inint_inint))。 這些方法都是多載的：也就是說，每個方法都有數個不同的參數清單變化。 例如，AddLine 方法的一種變化會接收四個整數，而 AddLine 方法的另一種變化則會接收兩個 [**點**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) 物件。

將線條、矩形和貝茲曲線新增至路徑的方法具有複數附屬方法，可在單一呼叫中將數個專案新增至路徑： [AddLines](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addlines(inconstpoint_inint))、 [AddRectangles](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addrectangles(inconstrectf_inint))和 [AddBeziers](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addbeziers(inconstpointf_inint))。 此外， [AddCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)) 方法也有附屬方法 [AddClosedCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addclosedcurve(inconstpointf_inint))，它會將封閉曲線新增至路徑。

若要繪製路徑，您需要 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件、 [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) 物件和 [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) 物件。 **Graphics** 物件提供 [**圖形：:D rawpath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath)方法，而 **Pen** 物件會儲存路徑的屬性，例如線條寬度和色彩。 **GraphicsPath** 物件會儲存組成路徑的線條、矩形和曲線序列。 **Pen** 物件和 **GraphicsPath** 物件的位址會做為引數傳遞給 **圖形：:D rawpath** 方法。 下列範例會繪製包含線條、橢圓形和貝茲曲線的路徑。


```
myGraphicsPath.AddLine(0, 0, 30, 20);
myGraphicsPath.AddEllipse(20, 20, 20, 40);
myGraphicsPath.AddBezier(30, 60, 70, 60, 50, 30, 100, 10);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



下圖顯示路徑。

![以線條、橢圓形和貝茲曲線組成的路徑圖例](images/aboutgdip02-art15.png)

除了將線條、矩形和曲線新增至路徑，您還可以將路徑新增至路徑。 這可讓您結合現有的路徑來形成大型、複雜的路徑。 下列程式碼會將 **graphicsPath1** 和 **GraphicsPath2** 新增至 **myGraphicsPath**。 [**GraphicsPath：： AddPath**](/windows/win32/api/Gdipluspath/nf-gdipluspath-graphicspath-addpath)方法的第二個參數會指定加入的路徑是否連接至現有的路徑。


```
myGraphicsPath.AddPath(&graphicsPath1, FALSE);
myGraphicsPath.AddPath(&graphicsPath2, TRUE);
```



您可以新增其他兩個專案至路徑：字串和圓形圖。 圓形圖是橢圓形內部的一部分。 下列範例會建立從弧線、基線曲線、字串和圓形圖的路徑。


```
myGraphicsPath.AddArc(0, 0, 30, 20, -90, 180);
myGraphicsPath.AddCurve(myPointArray, 3);
myGraphicsPath.AddString(L"a string in a path", 18, &myFontFamily, 
   0, 24, myPointF, &myStringFormat);
myGraphicsPath.AddPie(230, 10, 40, 40, 40, 110);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



下圖顯示路徑。 請注意，不需要連接路徑;弧線、基線曲線、字串和圓形圖會分開。

![由中斷連接線組成的路徑圖例：弧形、基線曲線、字串和圓形圖](images/aboutgdip02-art16.png)

 

 



