---
description: 橢圓形是由其周框所指定。 下圖顯示一個橢圓形以及它的周框。
ms.assetid: 45e80501-4d64-480b-a7c7-3af52c00a0aa
title: 橢圓形和弧形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fadd0a34107681d2d155ead5d4f80b7208b8926603f21fa4541d502886edaf73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036746"
---
# <a name="ellipses-and-arcs"></a>橢圓形和弧形

橢圓形是由其周框所指定。 下圖顯示一個橢圓形以及它的周框。

![包含周框矩形內的橢圓形圖例](images/aboutgdip02-art05.png)

若要繪製橢圓形，您需要 [**圖形**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件和 [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) 物件。 **Graphics** 物件提供 [DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_))方法，而 **Pen** 物件會儲存橢圓形的屬性，例如線條寬度和色彩。 **畫筆** 物件的位址會做為 DrawEllipse 方法的其中一個引數傳遞。 傳遞至 DrawEllipse 方法的其餘引數會指定橢圓形的周框。 下列範例會繪製一個橢圓形;周框的寬度為160、高度80，以及 (100，50) 的左上角。


```
myGraphics.DrawEllipse(&myPen, 100, 50, 160, 80);
```



[DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) 是 [**圖形**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 類別的多載方法，因此您可以透過數種方式提供引數給它。 例如，您可以建立 [**rect**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect) 物件，並將 **rect** 物件的參考傳遞為 DrawEllipse 方法的引數。


```
Rect myRect(100, 50, 160, 80);
myGraphics.DrawEllipse(&myPen, myRect);
```



弧形是橢圓形的一部分。 若要繪製弧線，請呼叫 [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)類別的 [DrawArc](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inint_inint_inint_inint_inreal_inreal))方法。 DrawArc 方法的參數與 [DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) 方法的參數相同，不同之處在于 DrawArc 需要起始角度和掃除角度。 下列範例會繪製一條弧線，其開始角度為30度，而將角度為180度。


```
myGraphics.DrawArc(&myPen, 100, 50, 160, 80, 30, 180);
```



下圖顯示弧線、橢圓形和周框。

![周框矩形內的橢圓形圖例;橢圓形的左下半部以紅色繪製](images/aboutgdip02-art06.png)

 

 



