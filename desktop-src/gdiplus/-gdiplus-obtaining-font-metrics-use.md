---
description: FontFamily 類別提供下列方法，以取得特定系列/樣式組合的各種計量：
ms.assetid: 3be485d0-9e0d-43e0-813e-668102ebc010
title: 取得字型計量
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 800fcee7dd1729a6fd5e59bb5dd636af89670776
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026201"
---
# <a name="obtaining-font-metrics"></a>取得字型計量

[**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily)類別提供下列方法，以取得特定系列/樣式組合的各種計量：

-   [**FontFamily：： GetEmHeight**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getemheight) (FontStyle) 
-   [**FontFamily：： GetCellAscent**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getcellascent) (FontStyle) 
-   [**FontFamily：： GetCellDescent**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getcelldescent) (FontStyle) 
-   [**FontFamily：： GetLineSpacing**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getlinespacing) (FontStyle) 

這些方法所傳回的數位是字型設計單位，因此它們與特定 [**字型**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) 物件的大小和單位無關。

下圖顯示上升、下降和行距。

![相鄰線上兩個字元的圖表，顯示資料格上升、資料格下降和行間距](images/fontstext7a.png)

下列範例會顯示 Arial 字型家族的一般樣式的度量。 程式碼也會根據具有16圖元大小的 Arial 系列) 來建立 ([**字型**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) 物件，並以圖元為) 單位顯示該特定 **字型** 物件的度量 (。


```
#define INFO_STRING_SIZE 100  // one line of output including null terminator
WCHAR infoString[INFO_STRING_SIZE] = L"";
UINT  ascent;                 // font family ascent in design units
REAL  ascentPixel;            // ascent converted to pixels
UINT  descent;                // font family descent in design units
REAL  descentPixel;           // descent converted to pixels
UINT  lineSpacing;            // font family line spacing in design units
REAL  lineSpacingPixel;       // line spacing converted to pixels
                       
FontFamily   fontFamily(L"Arial");
Font         font(&fontFamily, 16, FontStyleRegular, UnitPixel);
PointF       pointF(10.0f, 10.0f);
SolidBrush   solidBrush(Color(255, 0, 0, 0));

// Display the font size in pixels.
StringCchPrintf(
   infoString, 
   INFO_STRING_SIZE, 
   L"font.GetSize() returns %f.", font.GetSize());

graphics.DrawString(
   infoString, -1, &font, pointF, &solidBrush);

// Move down one line.
pointF.Y += font.GetHeight(0.0);

// Display the font family em height in design units.
StringCchPrintf(
   infoString, 
   INFO_STRING_SIZE, 
   L"fontFamily.GetEmHeight() returns %d.", 
   fontFamily.GetEmHeight(FontStyleRegular));

graphics.DrawString(infoString, -1, &font, pointF, &solidBrush);

// Move down two lines.
pointF.Y += 2.0f * font.GetHeight(0.0f);

// Display the ascent in design units and pixels.
ascent = fontFamily.GetCellAscent(FontStyleRegular);

// 14.484375 = 16.0 * 1854 / 2048
ascentPixel = 
   font.GetSize() * ascent / fontFamily.GetEmHeight(FontStyleRegular);

StringCchPrintf(
   infoString,
   INFO_STRING_SIZE,
   L"The ascent is %d design units, %f pixels.",
   ascent, 
   ascentPixel);

graphics.DrawString(infoString, -1, &font, pointF, &solidBrush);

// Move down one line.
pointF.Y += font.GetHeight(0.0f);

// Display the descent in design units and pixels.
descent = fontFamily.GetCellDescent(FontStyleRegular);

// 3.390625 = 16.0 * 434 / 2048
descentPixel = 
   font.GetSize() * descent / fontFamily.GetEmHeight(FontStyleRegular);

StringCchPrintf(
   infoString, 
   INFO_STRING_SIZE,
   L"The descent is %d design units, %f pixels.",
   descent, 
   descentPixel);

graphics.DrawString(infoString, -1, &font, pointF, &solidBrush);

// Move down one line.
pointF.Y += font.GetHeight(0.0f);

// Display the line spacing in design units and pixels.
lineSpacing = fontFamily.GetLineSpacing(FontStyleRegular);

// 18.398438 = 16.0 * 2355 / 2048
lineSpacingPixel = 
   font.GetSize() * lineSpacing / fontFamily.GetEmHeight(FontStyleRegular);

StringCchPrintf(
   infoString, 
   INFO_STRING_SIZE,
   L"The line spacing is %d design units, %f pixels.",
   lineSpacing, 
   lineSpacingPixel);

graphics.DrawString(infoString, -1, &font, pointF, &solidBrush);
            
```



下圖顯示上述程式碼的輸出。

![視窗的螢幕擷取畫面，其中包含字型大小和高度的文字，以及上移、下降和行距](images/fontstext8.png)

請注意上圖中前兩行的輸出。 [**字型**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font)物件傳回的大小為16，而 [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily)物件傳回的 em 高度為2048。 這兩個數字 (16 和 2048) 是在字型設計單位和單位之間轉換的關鍵， (在此案例中為 **字型** 物件的圖元) 。

例如，您可以將從設計單位轉換成圖元，如下所示：

![將1854設計單位乘以16圖元除以2048設計單位的方程式，必須為14.484375 圖元](images/fontstext9.png)

上述程式碼會設定 [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf)物件的 *y* 資料成員，以垂直方式放置文字。 `font.GetHeight(0.0f)`每一行新的文字都會增加 y 座標。 [**字型**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font)物件的 [**Font-size：： GetHeight**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-getheight(inreal))方法會傳回該特定 **字型** 物件的行間距， (以圖元為單位的) 。 在此範例中， **字型：： GetHeight** 傳回的數位為18.398438。 請注意，這與將行間距度量轉換成圖元所取得的數位相同。

 

 
