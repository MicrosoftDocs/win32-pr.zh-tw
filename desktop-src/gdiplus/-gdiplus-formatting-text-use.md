---
description: 若要將特殊格式套用至文字，請將 StringFormat 物件初始化，並將該物件的位址傳遞至 Graphics 類別的 DrawString 方法。
ms.assetid: 4014a602-88f6-4fac-b4b2-3dafdcff8f33
title: 格式化文字 (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e6b2cc6109e7b946e9b4e98645c9445b8268bb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104570729"
---
# <a name="formatting-text-gdi"></a>格式化文字 (GDI+)

若要將特殊格式套用至文字，請將 [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat)物件初始化，並將該物件的位址傳遞至 [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)類別的 [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush))方法。

若要在矩形中繪製格式化的文字，您需要 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)、 [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily)、 [**字型**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font)、 [**RectF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rectf)、 [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat)和 [**筆刷**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) 物件。

-   [對齊文字](#aligning-text)
-   [設定制表位](#setting-tab-stops)
-   [繪製垂直文字](#drawing-vertical-text)

## <a name="aligning-text"></a>對齊文字

下列範例會在矩形中繪製文字。 每一行文字都是以 (的側邊) 為中心，而整個文字區塊則會在矩形中 (從上到下) 。


```
WCHAR string[] = 
   L"Use StringFormat and RectF objects to center text in a rectangle.";
                       
FontFamily   fontFamily(L"Arial");
Font         font(&fontFamily, 12, FontStyleBold, UnitPoint);
RectF        rectF(30.0f, 10.0f, 120.0f, 140.0f);
StringFormat stringFormat;
SolidBrush   solidBrush(Color(255, 0, 0, 255));

// Center-justify each line of text.
stringFormat.SetAlignment(StringAlignmentCenter);

// Center the block of text (top to bottom) in the rectangle.
stringFormat.SetLineAlignment(StringAlignmentCenter);

graphics.DrawString(string, -1, &font, rectF, &stringFormat, &solidBrush);

Pen pen(Color(255, 0, 0, 0));
graphics.DrawRectangle(&pen, rectF);
            
```



下圖顯示矩形和中央文字。

![視窗的螢幕擷取畫面，包含包含六行文字的矩形，水準置中](images/fontstext3.png)

上述程式碼會呼叫 [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) 物件的兩個方法： [**StringFormat：： SetAlignment**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setalignment) 和 [**StringFormat：： SetLineAlignment**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setlinealignment)。 **StringFormat：： SetAlignment** 的呼叫會指定每一行文字都在傳遞給 [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush))方法的第三個引數所指定的矩形中置中。 **StringFormat：： SetLineAlignment** 的呼叫會指定文字區塊的中心 (在矩形中的上到下) 。

值 [* * * * StringAlignmentCenter *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringalignment) * * 是 **StringAlignment** 列舉的元素，它是在 Gdiplusenums 中宣告的。

## <a name="setting-tab-stops"></a>設定制表位

您可以藉由呼叫 [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat)物件的 [**StringFormat：： SetTabStops**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-settabstops)方法，然後將該 **StringFormat** 物件的位址傳遞至 [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)類別的 [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush))方法，來設定文字的定位停駐點。

下列範例會在150、250和350設定制表位。 然後，程式碼會顯示名稱和測試分數的索引標籤式清單。


```
WCHAR string[150] = 
   L"Name\tTest 1\tTest 2\tTest 3\n";

StringCchCatW(string, 150, L"Joe\t95\t88\t91\n");
StringCchCatW(string, 150, L"Mary\t98\t84\t90\n");
StringCchCatW(string, 150, L"Sam\t42\t76\t98\n");
StringCchCatW(string, 150, L"Jane\t65\t73\t92\n");
                       
FontFamily   fontFamily(L"Courier New");
Font         font(&fontFamily, 12, FontStyleRegular, UnitPoint);
RectF        rectF(10.0f, 10.0f, 450.0f, 100.0f);
StringFormat stringFormat;
SolidBrush   solidBrush(Color(255, 0, 0, 255));
REAL         tabs[] = {150.0f, 100.0f, 100.0f};

stringFormat.SetTabStops(0.0f, 3, tabs);

graphics.DrawString(string, -1, &font, rectF, &stringFormat, &solidBrush);

Pen pen(Color(255, 0, 0, 0));
graphics.DrawRectangle(&pen, rectF);
            
```



下圖顯示索引標籤式的文字。

![包含四個文字資料行的矩形圖例;每個資料行都保持支援](images/fontstext4.png)

上述程式碼會將三個引數傳遞給 [**StringFormat：： SetTabStops**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-settabstops) 方法。 第三個引數是包含定位字元位移的陣列位址。 第二個引數表示該陣列中有三個位移。 傳遞至 **StringFormat：： SetTabStops** 的第一個引數為0，表示陣列中的第一個位移是從位置0（周框矩形的左邊緣）測量的。

## <a name="drawing-vertical-text"></a>繪製垂直文字

您可以使用 [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) 物件來指定以垂直方式（而非水準）繪製文字。

下列範例會將值 [* * * * StringFormatFlagsDirectionVertical *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringformatflags) * * 傳遞給 [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat)物件的 [**StringFormat：： SetFormatFlags**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setformatflags)方法。 將 **StringFormat** 物件的位址傳遞至 [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)類別的 [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush))方法。 值 [* * * * StringFormatFlagsDirectionVertical *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringformatflags) * * 是 **system.drawing.stringformatflags>** 列舉的元素，它是在 Gdiplusenums 中宣告的。


```
WCHAR string[] = L"Vertical text";
                     
FontFamily   fontFamily(L"Lucida Console");
Font         font(&fontFamily, 14, FontStyleRegular, UnitPoint);
PointF       pointF(40.0f, 10.0f);
StringFormat stringFormat;
SolidBrush   solidBrush(Color(255, 0, 0, 255));

stringFormat.SetFormatFlags(StringFormatFlagsDirectionVertical);

graphics.DrawString(string, -1, &font, pointF, &stringFormat, &solidBrush);
            
```



下圖顯示垂直文字。

![顯示包含順時針旋轉90度之文字的視窗的圖例](images/fontstext5.png)

 

 



