---
description: 多邊形是具有三個或更多直邊的封閉圖。
ms.assetid: f1155341-83f3-4805-8d42-a1910515db31
title: 多邊形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe67ec2d062579df0510c100a80d06715be4199e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690336"
---
# <a name="polygons"></a>多邊形

多邊形是具有三個或更多直邊的封閉圖。 例如，三角形是三邊的多邊形，矩形是具有四邊的多邊形，而五邊是具有五邊的多邊形。 下圖顯示數個多邊形。

![圖例顯示不同圖形、大小和色彩的五個多邊形](images/aboutgdip02-art07.png)

若要繪製多邊形，您需要 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件、 [**畫筆**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) 物件和 [**點**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) 陣列 (或 [**PointF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pointf)) 物件。 **Graphics** 物件提供 [DrawPolygon](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpolygon(inconstpen_inconstpoint_inint))方法。 **Pen** 物件會儲存多邊形的屬性，例如線條寬度和色彩，而 **Point** 物件的陣列則會儲存以直線連接的點。 **Pen** 物件的位址和 **Point** 物件的陣列會以引數的形式傳遞至 DrawPolygon 方法。 下列範例會繪製三側多邊形。 請注意， **myPointArray** 中只有三個點： (0、0) 、 (50、30) 和 (30 60) 。 DrawPolygon 方法會藉由繪製從 (30，60) 回到起點 (0，0) ; 的直線，來自動關閉多邊形。


```
Point myPointArray[] =
   {Point(0, 0), Point(50, 30), Point(30, 60)};
myGraphics.DrawPolygon(&myPen, myPointArray, 3);
```



下圖顯示多邊形。

![針對座標軸顯示三角形的圖例](images/aboutgdip02-art08.png)

 

 



