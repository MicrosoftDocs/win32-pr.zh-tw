---
description: 您可以使用 Graphics 類別的 DrawString 方法，在指定的位置或指定的矩形內繪製文字。
ms.assetid: a873c132-f232-4144-bcc3-ca200055074c
title: 繪製文字 (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31591d62198bc6ff72cdd7cce0d8ab515dc0e96011457b5bccd601a59ee0293f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120115038"
---
# <a name="drawing-text-gdi"></a>繪製文字 (GDI+)

您可以使用 [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)類別的 [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush))方法，在指定的位置或指定的矩形內繪製文字。

-   [在指定的位置繪製文字](#drawing-text-at-a-specified-location)
-   [在矩形中繪製文字](#drawing-text-in-a-rectangle)

## <a name="drawing-text-at-a-specified-location"></a>在指定的位置繪製文字

若要在指定的位置繪製文字，您需要 [**圖形**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)、 [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily)、 [**字型**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font)、 [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf)和 [**筆刷**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) 物件。

下列範例會將 "Hello" 字串繪製在位置 (30，10) 。 字型家族的時間是新的羅馬。 字型是字型家族的個別成員，是新的羅馬、大小為24圖元、一般樣式。 假設 **圖形** 是現有的 [**圖形**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件。

```
FontFamily  fontFamily(L"Times New Roman");
Font        font(&fontFamily, 24, FontStyleRegular, UnitPixel);
PointF      pointF(30.0f, 10.0f);
SolidBrush  solidBrush(Color(255, 0, 0, 255));

graphics.DrawString(L"Hello", -1, &font, pointF, &solidBrush);

```

下圖顯示上述程式碼的輸出。

![小視窗的螢幕擷取畫面，其中包含文字 "hello"](images/fontstext1.png)

在上述範例中， [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) 的函式會收到可識別字型家族的字串。 **FontFamily** 物件的位址會以第一個引數的形式傳遞至 [**字型**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font)的函式。 傳遞至 **字型** 引數的第二個引數會指定以第四個引數所提供的單位來測量的字型大小。 第三個引數會指定字型 (一般、粗體、斜體等) 。

[DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush))方法會接收五個引數。 第一個引數是要繪製的字串，而第二個引數是 (的長度（以字元為單位），而不是該字串的位元組) 。 如果字串以 null 結束，您可以傳遞-1 作為長度。 第三個引數是先前所建立之 [**字型**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) 物件的位址。 第四個引數是 [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf) 物件，其中包含字串左上角的座標。 第五個引數是將用來填滿字串字元的 [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) 物件位址。

## <a name="drawing-text-in-a-rectangle"></a>在矩形中繪製文字

[**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)類別的其中一個 [**DrawString**](https://www.bing.com/search?q=**DrawString**)方法有 *RectF* 參數。 藉由呼叫該 **DrawString** 方法，您可以繪製文字，以在指定的矩形中換行。 若要在矩形中繪製文字，您需要 **圖形**、 [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily)、 [**字型**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font)、 [**RectF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf)和 [**筆刷**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) 物件。

下列範例會建立左上角的矩形 (30、10) 、寬度100和高度122。 然後，程式碼會在該矩形內繪製一個字串。 字串會限制為矩形，並換成個別單字不會中斷的方式。

```
WCHAR string[] = 
   L"Draw text in a rectangle by passing a RectF to the DrawString method.";

FontFamily   fontFamily(L"Arial");
Font         font(&fontFamily, 12, FontStyleBold, UnitPoint);
RectF        rectF(30.0f, 10.0f, 100.0f, 122.0f);
SolidBrush   solidBrush(Color(255, 0, 0, 255));

graphics.DrawString(string, -1, &font, rectF, NULL, &solidBrush);

Pen pen(Color(255, 0, 0, 0));
graphics.DrawRectangle(&pen, rectF);
```

下圖顯示在矩形中繪製的文字。

![小視窗的螢幕擷取畫面，其中包含 recangle，在其中會顯示句子的第一個部分](images/fontstext2.png)

在上述範例中，傳遞至 [**DrawString**](https://www.bing.com/search?q=**DrawString**) 方法的第四個引數是 [**RectF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf) 物件，可指定文字的周框。 第五個參數的類型為 [**StringFormat**](/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat)，引數為 **Null** ，因為不需要特殊字元串格式。
