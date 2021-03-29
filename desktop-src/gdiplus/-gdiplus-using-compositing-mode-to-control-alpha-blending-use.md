---
description: 有時候您可能會想要建立具有下列特性的非螢幕點陣圖：
ms.assetid: 2a7590ce-daf4-4892-a838-603e3f89b1bb
title: 使用複合模式控制 Alpha 混色
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db54c71ac9687a1ddf28db09b922b7799d0ebaa3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972828"
---
# <a name="using-compositing-mode-to-control-alpha-blending"></a>使用複合模式控制 Alpha 混色

有時候您可能會想要建立具有下列特性的非螢幕點陣圖：

-   色彩的 Alpha 值小於255。
-   當您建立點陣圖時，色彩不會加上 Alpha 的混合。
-   當您顯示完成的點陣圖時，點陣圖中的色彩會與顯示裝置上的背景色彩混合使用 Alpha。

若要建立這類點陣圖，請建立一個空白 [**點陣圖**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) 物件，然後根據該點陣圖來建立 [**圖形**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件。 將 **圖形** 物件的合成模式設定為 CompositingModeSourceCopy。

下列範例會根據 [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap)物件建立 [**圖形**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)物件。 程式碼會使用 **Graphics** 物件，以及兩個半透明筆刷 (Alpha = 160) 在點陣圖上繪製。 程式碼會使用半透明筆刷來填滿紅色橢圓形和綠色橢圓形。 綠色橢圓形與紅色橢圓形重迭，但綠色不會與紅色混合，因為 **Graphics** 物件的合成模式設定為 CompositingModeSourceCopy。

接下來，程式碼會呼叫 [BeginPaint](/windows/win32/api/winuser/nf-winuser-beginpaint) ，並根據裝置內容建立 [**圖形**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件，以準備在螢幕上繪製。 程式碼會在螢幕上繪製點陣圖兩次：一次在白色背景上，一次在彩色背景上。 點陣圖中屬於兩個省略號的圖元具有 Alpha 元件160，因此省略號會與螢幕上的背景色彩混合。


```
// Create a blank bitmap.
Bitmap bitmap(180, 100);
// Create a Graphics object that can be used to draw on the bitmap.
Graphics bitmapGraphics(&bitmap);
// Create a red brush and a green brush, each with an alpha value of 160.
SolidBrush redBrush(Color(210, 255, 0, 0));
SolidBrush greenBrush(Color(210, 0, 255, 0));
// Set the compositing mode so that when overlapping ellipses are drawn,
// the colors of the ellipses are not blended.
bitmapGraphics.SetCompositingMode(CompositingModeSourceCopy);
// Fill an ellipse using a red brush that has an alpha value of 160.
bitmapGraphics.FillEllipse(&redBrush, 0, 0, 150, 70);
// Fill a second ellipse using green brush that has an alpha value of 160. 
// The green ellipse overlaps the red ellipse, but the green is not 
// blended with the red.
bitmapGraphics.FillEllipse(&greenBrush, 30, 30, 150, 70);
// Prepare to draw on the screen.
hdc = BeginPaint(hWnd, &ps);
Graphics* pGraphics = new Graphics(hdc);
pGraphics->SetCompositingQuality(CompositingQualityGammaCorrected);
// Draw a multicolored background.
SolidBrush brush(Color((ARGB)Color::Aqua));
pGraphics->FillRectangle(&brush, 200, 0, 60, 100);
brush.SetColor(Color((ARGB)Color::Yellow));
pGraphics->FillRectangle(&brush, 260, 0, 60, 100);
brush.SetColor(Color((ARGB)Color::Fuchsia));
pGraphics->FillRectangle(&brush, 320, 0, 60, 100);
   
// Display the bitmap on a white background.
pGraphics->DrawImage(&bitmap, 0, 0);
// Display the bitmap on a multicolored background.
pGraphics->DrawImage(&bitmap, 200, 0);
delete pGraphics;
EndPaint(hWnd, &ps);
```



下圖顯示上述程式碼的輸出。 請注意，省略號會與背景混合，但是它們不會互相混合。

![顯示兩個不同色彩橢圓形的圖例，其中每個橢圓形都會與彩色色彩混合](images/sourcecopy.png)

上述程式碼範例具有下列語句：


```
bitmapGraphics.SetCompositingMode(CompositingModeSourceCopy);
```



如果您想要讓省略號彼此混合以及背景，請將該語句變更為下列內容：


```
bitmapGraphics.SetCompositingMode(CompositingModeSourceOver);
```



下圖顯示修改過的程式碼的輸出。

![使用複合模式控制 Alpha 混色圖](images/sourceover.png)

 

 



