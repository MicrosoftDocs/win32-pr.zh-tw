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
# <a name="drawing-a-string"></a><span data-ttu-id="4daae-103">繪製字串</span><span class="sxs-lookup"><span data-stu-id="4daae-103">Drawing a String</span></span>

<span data-ttu-id="4daae-104">[繪製一條線](-gdiplus-drawing-a-line-use.md)的主題說明如何撰寫 windows 應用程式，以使用 windows gdi + 繪製線條。</span><span class="sxs-lookup"><span data-stu-id="4daae-104">The topic [Drawing a Line](-gdiplus-drawing-a-line-use.md) shows how to write a Windows application that uses Windows GDI+ to draw a line.</span></span> <span data-ttu-id="4daae-105">若要繪製字串，請使用下列 **onpaint** 函數來取代該主題中顯示的 **onpaint** 函式：</span><span class="sxs-lookup"><span data-stu-id="4daae-105">To draw a string, replace the **OnPaint** function shown in that topic with the following **OnPaint** function:</span></span>


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



<span data-ttu-id="4daae-106">先前的程式碼會建立數個 GDI + 物件。</span><span class="sxs-lookup"><span data-stu-id="4daae-106">The previous code creates several GDI+ objects.</span></span> <span data-ttu-id="4daae-107">[**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)物件提供 [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush))方法，此方法會執行實際的繪圖。</span><span class="sxs-lookup"><span data-stu-id="4daae-107">The [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object provides the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) method, which does the actual drawing.</span></span> <span data-ttu-id="4daae-108">[**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush)物件指定字串的色彩。</span><span class="sxs-lookup"><span data-stu-id="4daae-108">The [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) object specifies the color of the string.</span></span>

<span data-ttu-id="4daae-109">[**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily)的函式會接收單一的字串引數，以識別字型家族。</span><span class="sxs-lookup"><span data-stu-id="4daae-109">The [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) constructor receives a single, string argument that identifies the font family.</span></span> <span data-ttu-id="4daae-110">**FontFamily** 物件的位址是傳遞至 [**字型**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font)函式的第一個引數。</span><span class="sxs-lookup"><span data-stu-id="4daae-110">The address of the **FontFamily** object is the first argument passed to the [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) constructor.</span></span> <span data-ttu-id="4daae-111">傳遞至 [字型](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(constfont_)) 函式的第二個引數會指定字型大小，而第三個引數會指定樣式。</span><span class="sxs-lookup"><span data-stu-id="4daae-111">The second argument passed to the [Font](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(constfont_)) constructor specifies the font size, and the third argument specifies the style.</span></span> <span data-ttu-id="4daae-112">**FontStyleRegular** 值是 [**FontStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-fontstyle)列舉的成員，它是在 Gdiplusenums 中宣告的。</span><span class="sxs-lookup"><span data-stu-id="4daae-112">The value **FontStyleRegular** is a member of the [**FontStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-fontstyle) enumeration, which is declared in Gdiplusenums.h.</span></span> <span data-ttu-id="4daae-113">**字型** 引數的最後一個引數會指出在此案例中，) 以圖元為單位來測量字型 (24 的大小。</span><span class="sxs-lookup"><span data-stu-id="4daae-113">The last argument to the **Font** constructor indicates that the size of the font (24 in this case) is measured in pixels.</span></span> <span data-ttu-id="4daae-114">**UnitPixel** 值是 [**單位**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-unit)列舉的成員。</span><span class="sxs-lookup"><span data-stu-id="4daae-114">The value **UnitPixel** is a member of the [**Unit**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-unit) enumeration.</span></span>

<span data-ttu-id="4daae-115">傳遞至 [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) 方法的第一個引數是寬字元字串的位址。</span><span class="sxs-lookup"><span data-stu-id="4daae-115">The first argument passed to the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) method is the address of a wide-character string.</span></span> <span data-ttu-id="4daae-116">第二個引數（-1）指定字串是以 null 結束。</span><span class="sxs-lookup"><span data-stu-id="4daae-116">The second argument, –1, specifies that the string is null terminated.</span></span> <span data-ttu-id="4daae-117"> (如果字串不是以 null 結束，則第二個引數應該指定字串中的寬字元數目。 ) 第三個引數是 [**字型**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) 物件的位址。</span><span class="sxs-lookup"><span data-stu-id="4daae-117">(If the string is not null terminated, the second argument should specify the number of wide characters in the string.) The third argument is the address of the [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) object.</span></span> <span data-ttu-id="4daae-118">第四個引數是 [**PointF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pointf) 物件的參考，該物件會指定要繪製字串的位置。</span><span class="sxs-lookup"><span data-stu-id="4daae-118">The fourth argument is a reference to a [**PointF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pointf) object that specifies the location where the string will be drawn.</span></span> <span data-ttu-id="4daae-119">最後一個引數是 [**筆刷**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) 物件的位址，可指定字串的色彩。</span><span class="sxs-lookup"><span data-stu-id="4daae-119">The last argument is the address of the [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) object, which specifies the color of the string.</span></span>

 

 
