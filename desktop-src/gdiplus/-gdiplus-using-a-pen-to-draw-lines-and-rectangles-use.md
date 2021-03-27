---
description: 若要繪製線條和矩形，您需要繪圖物件和 Pen 物件。 Graphics 物件提供 DrawLine 方法，而 Pen 物件會儲存線條的功能，例如色彩和寬度。
ms.assetid: f2e4144f-f2f1-49db-bfdf-ffce3023b4cb
title: 使用畫筆繪製線條和矩形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b335caf7e2ecbad6bc49965ff757809c3b1179c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943940"
---
# <a name="using-a-pen-to-draw-lines-and-rectangles"></a>使用畫筆繪製線條和矩形

若要繪製線條和矩形，您需要 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件和 [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) 物件。 **Graphics** 物件提供 [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint))方法，而 **Pen** 物件會儲存線條的功能，例如色彩和寬度。

下列範例會繪製從 (20，10) 到 (300，100) 的行。 假設 **圖形** 是現有的 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件。


```
Pen pen(Color(255, 0, 0, 0));
graphics.DrawLine(&pen, 20, 10, 300, 100);
```



第一個程式碼語句會使用 [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) 類別的函式來建立黑色畫筆。 傳遞給 **畫筆** 參數的一個引數是 [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) 物件。 用來建立 **色彩** 物件的值（ (255、0、0、0) ）會對應至色彩的 Alpha、紅色、綠色和藍色元件。 這些值會定義不透明的黑色畫筆。

下列範例會繪製一個矩形，其左上角位於 (10，10) 。 矩形的寬度為100，高度為50。 傳遞給 [**畫筆**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) 表示函式的第二個引數表示畫筆寬度為5圖元。


```
Pen blackPen(Color(255, 0, 0, 0), 5);
stat = graphics.DrawRectangle(&blackPen, 10, 10, 100, 50);
```



繪製矩形時，畫筆會以矩形的界限為中心。 因為畫筆寬度為5，所以矩形的側邊繪製的寬度為5圖元，因此會在界限本身繪製1圖元、在內部繪製2圖元，並在外部繪製2個圖元。 如需畫筆對齊的詳細資訊，請參閱 [設定畫筆寬度和對齊方式](-gdiplus-setting-pen-width-and-alignment-use.md)。

下圖顯示產生的矩形。 如果畫筆寬度為一個圖元，則虛線會顯示繪製矩形的位置。 矩形左上角的放大視圖會顯示黑色黑色線條會置於這些虛線的中央。

![以黑色黑色線條繪製的矩形圖例，該線條周圍會圍住細灰色的虛線](images/pens1.png)

 

 



