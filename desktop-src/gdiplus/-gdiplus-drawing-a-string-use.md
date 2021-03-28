---
description: 繪製一條線的主題說明如何撰寫 Windows 應用程式，以使用 Windows GDI + 繪製線條。
ms.assetid: fcf45b19-456c-4551-8901-d587a73a5638
title: 繪製字串
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a88e76fd38dd640a402edf202dc6cdbd3008a76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192333"
---
# <a name="drawing-a-string"></a>繪製字串

[繪製一條線](-gdiplus-drawing-a-line-use.md)的主題說明如何撰寫 windows 應用程式，以使用 windows gdi + 繪製線條。 若要繪製字串，請使用下列 **onpaint** 函數來取代該主題中顯示的 **onpaint** 函式：


```
VOID OnPaint(HDC hdc)
{
   Graphics    graphics(hdc);
   SolidBrush  brush(Color(255, 0, 0, 255));
   FontFamily  fontFamily(L"Times New Roman");
   Font        font(&fontFamily, 24, FontStyleRegular, UnitPixel);
   PointF      pointF(10.0f, 20.0f);
   
   graphics.DrawString(L"Hello World!", -1, &font, pointF, &brush);
}
```



先前的程式碼會建立數個 GDI + 物件。 [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)物件提供 [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush))方法，此方法會執行實際的繪圖。 [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush)物件指定字串的色彩。

[**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily)的函式會接收單一的字串引數，以識別字型家族。 **FontFamily** 物件的位址是傳遞至 [**字型**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font)函式的第一個引數。 傳遞至 [字型](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(constfont_)) 函式的第二個引數會指定字型大小，而第三個引數會指定樣式。 **FontStyleRegular** 值是 [**FontStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-fontstyle)列舉的成員，它是在 Gdiplusenums 中宣告的。 **字型** 引數的最後一個引數會指出在此案例中，) 以圖元為單位來測量字型 (24 的大小。 **UnitPixel** 值是 [**單位**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-unit)列舉的成員。

傳遞至 [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) 方法的第一個引數是寬字元字串的位址。 第二個引數（-1）指定字串是以 null 結束。  (如果字串不是以 null 結束，則第二個引數應該指定字串中的寬字元數目。 ) 第三個引數是 [**字型**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) 物件的位址。 第四個引數是 [**PointF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pointf) 物件的參考，該物件會指定要繪製字串的位置。 最後一個引數是 [**筆刷**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) 物件的位址，可指定字串的色彩。

 

 
