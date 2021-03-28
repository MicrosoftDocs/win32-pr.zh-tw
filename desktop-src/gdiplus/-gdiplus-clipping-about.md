---
description: 裁剪牽涉到將繪圖限制在特定區域。 下圖顯示字串 &\# 0034;Hello&\# 0034; 裁剪為心形的區域。
ms.assetid: 58cc052d-31af-4410-81b9-defbad08a1dc
title: '剪切 (GDI +) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 156ae2209a3b7135cde2804103531eaf7b519d73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026599"
---
# <a name="clipping-gdi"></a>剪切 (GDI +) 

裁剪牽涉到將繪圖限制在特定區域。 下圖顯示已裁剪至心形區域的字串 "Hello"。

![顯示紅紅中字串 "hello" 部分的圖例](images/aboutgdip02-art30.png)

您可以從路徑來建立區域，路徑可以包含字串的外框，因此您可以使用外框文字進行裁剪。 下圖顯示一組會裁剪成文字字串內部的同心圓。

![圖例顯示以同心圓模式填滿的字串 "hello"](images/aboutgdip02-art31.png)

若要使用裁剪繪製，請建立 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件、呼叫其 [SetClip](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode)) 方法，然後呼叫相同 **圖形** 物件的繪圖方法。 下列範例會繪製一條裁剪成矩形區域的線條。


```
Region myRegion(Rect(20, 30, 100, 50));
myGraphics.DrawRectangle(&myPen, 20, 30, 100, 50);  
myGraphics.SetClip(&myRegion, CombineModeReplace);
myGraphics.DrawLine(&myPen, 0, 0, 200, 200);
```



下圖顯示矩形區域以及裁剪的線條。

![圖例顯示具有從上到下對角線的矩形](images/aboutgdip02-art31a.png)

 

 



