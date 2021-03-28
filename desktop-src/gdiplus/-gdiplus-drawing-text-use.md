---
description: 您可以使用 Graphics 類別的 DrawString 方法，在指定的位置或指定的矩形內繪製文字。
ms.assetid: a873c132-f232-4144-bcc3-ca200055074c
title: 繪製文字 (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e16ed49a5ab92380b42ed3316346ac547f95be9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115232"
---
# <a name="drawing-text-gdi"></a><span data-ttu-id="2d4e4-103">繪製文字 (GDI+)</span><span class="sxs-lookup"><span data-stu-id="2d4e4-103">Drawing Text (GDI+)</span></span>

<span data-ttu-id="2d4e4-104">您可以使用 [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)類別的 [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush))方法，在指定的位置或指定的矩形內繪製文字。</span><span class="sxs-lookup"><span data-stu-id="2d4e4-104">You can use the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) method of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class to draw text at a specified location or within a specified rectangle.</span></span>

-   [<span data-ttu-id="2d4e4-105">在指定的位置繪製文字</span><span class="sxs-lookup"><span data-stu-id="2d4e4-105">Drawing Text at a Specified Location</span></span>](#drawing-text-at-a-specified-location)
-   [<span data-ttu-id="2d4e4-106">在矩形中繪製文字</span><span class="sxs-lookup"><span data-stu-id="2d4e4-106">Drawing Text in a Rectangle</span></span>](#drawing-text-in-a-rectangle)

## <a name="drawing-text-at-a-specified-location"></a><span data-ttu-id="2d4e4-107">在指定的位置繪製文字</span><span class="sxs-lookup"><span data-stu-id="2d4e4-107">Drawing Text at a Specified Location</span></span>

<span data-ttu-id="2d4e4-108">若要在指定的位置繪製文字，您需要 [**圖形**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)、 [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily)、 [**字型**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font)、 [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf)和 [**筆刷**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) 物件。</span><span class="sxs-lookup"><span data-stu-id="2d4e4-108">To draw text at a specified location, you need [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics), [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font), [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf), and [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) objects.</span></span>

<span data-ttu-id="2d4e4-109">下列範例會將 "Hello" 字串繪製在位置 (30，10) 。</span><span class="sxs-lookup"><span data-stu-id="2d4e4-109">The following example draws the string "Hello" at location (30, 10).</span></span> <span data-ttu-id="2d4e4-110">字型家族的時間是新的羅馬。</span><span class="sxs-lookup"><span data-stu-id="2d4e4-110">The font family is Times New Roman.</span></span> <span data-ttu-id="2d4e4-111">字型是字型家族的個別成員，是新的羅馬、大小為24圖元、一般樣式。</span><span class="sxs-lookup"><span data-stu-id="2d4e4-111">The font, which is an individual member of the font family, is Times New Roman, size 24 pixels, regular style.</span></span> <span data-ttu-id="2d4e4-112">假設 **圖形** 是現有的 [**圖形**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件。</span><span class="sxs-lookup"><span data-stu-id="2d4e4-112">Assume that **graphics** is an existing [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span>

```
FontFamily  fontFamily(L"Times New Roman");
Font        font(&fontFamily, 24, FontStyleRegular, UnitPixel);
PointF      pointF(30.0f, 10.0f);
SolidBrush  solidBrush(Color(255, 0, 0, 255));

graphics.DrawString(L"Hello", -1, &font, pointF, &solidBrush);

```

<span data-ttu-id="2d4e4-113">下圖顯示上述程式碼的輸出。</span><span class="sxs-lookup"><span data-stu-id="2d4e4-113">The following illustration shows the output of the preceding code.</span></span>

![小視窗的螢幕擷取畫面，其中包含文字 "hello"](images/fontstext1.png)

<span data-ttu-id="2d4e4-115">在上述範例中， [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) 的函式會收到可識別字型家族的字串。</span><span class="sxs-lookup"><span data-stu-id="2d4e4-115">In the preceding example, the [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) constructor receives a string that identifies the font family.</span></span> <span data-ttu-id="2d4e4-116">**FontFamily** 物件的位址會以第一個引數的形式傳遞至 [**字型**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font)的函式。</span><span class="sxs-lookup"><span data-stu-id="2d4e4-116">The address of the **FontFamily** object is passed as the first argument to the [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) constructor.</span></span> <span data-ttu-id="2d4e4-117">傳遞至 **字型** 引數的第二個引數會指定以第四個引數所提供的單位來測量的字型大小。</span><span class="sxs-lookup"><span data-stu-id="2d4e4-117">The second argument passed to the **Font** constructor specifies the size of the font measured in units given by the fourth argument.</span></span> <span data-ttu-id="2d4e4-118">第三個引數會指定字型 (一般、粗體、斜體等) 。</span><span class="sxs-lookup"><span data-stu-id="2d4e4-118">The third argument specifies the style (regular, bold, italic, and so on) of the font.</span></span>

<span data-ttu-id="2d4e4-119">[DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush))方法會接收五個引數。</span><span class="sxs-lookup"><span data-stu-id="2d4e4-119">The [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) method receives five arguments.</span></span> <span data-ttu-id="2d4e4-120">第一個引數是要繪製的字串，而第二個引數是 (的長度（以字元為單位），而不是該字串的位元組) 。</span><span class="sxs-lookup"><span data-stu-id="2d4e4-120">The first argument is the string to be drawn, and the second argument is the length (in characters, not bytes) of that string.</span></span> <span data-ttu-id="2d4e4-121">如果字串以 null 結束，您可以傳遞-1 作為長度。</span><span class="sxs-lookup"><span data-stu-id="2d4e4-121">If the string is null-terminated, you can pass –1 for the length.</span></span> <span data-ttu-id="2d4e4-122">第三個引數是先前所建立之 [**字型**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) 物件的位址。</span><span class="sxs-lookup"><span data-stu-id="2d4e4-122">The third argument is the address of the [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) object that was constructed previously.</span></span> <span data-ttu-id="2d4e4-123">第四個引數是 [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf) 物件，其中包含字串左上角的座標。</span><span class="sxs-lookup"><span data-stu-id="2d4e4-123">The fourth argument is a [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf) object that contains the coordinates of the upper-left corner of the string.</span></span> <span data-ttu-id="2d4e4-124">第五個引數是將用來填滿字串字元的 [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) 物件位址。</span><span class="sxs-lookup"><span data-stu-id="2d4e4-124">The fifth argument is the address of a [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) object that will be used to fill the characters of the string.</span></span>

## <a name="drawing-text-in-a-rectangle"></a><span data-ttu-id="2d4e4-125">在矩形中繪製文字</span><span class="sxs-lookup"><span data-stu-id="2d4e4-125">Drawing Text in a Rectangle</span></span>

<span data-ttu-id="2d4e4-126">[**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)類別的其中一個 [**DrawString**](https://www.bing.com/search?q=**DrawString**)方法有 *RectF* 參數。</span><span class="sxs-lookup"><span data-stu-id="2d4e4-126">One of the [**DrawString**](https://www.bing.com/search?q=**DrawString**) methods of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class has a *RectF* parameter.</span></span> <span data-ttu-id="2d4e4-127">藉由呼叫該 **DrawString** 方法，您可以繪製文字，以在指定的矩形中換行。</span><span class="sxs-lookup"><span data-stu-id="2d4e4-127">By calling that **DrawString** method, you can draw text that wraps in a specified rectangle.</span></span> <span data-ttu-id="2d4e4-128">若要在矩形中繪製文字，您需要 **圖形**、 [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily)、 [**字型**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font)、 [**RectF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf)和 [**筆刷**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) 物件。</span><span class="sxs-lookup"><span data-stu-id="2d4e4-128">To draw text in a rectangle, you need **Graphics**, [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font), [**RectF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf), and [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) objects.</span></span>

<span data-ttu-id="2d4e4-129">下列範例會建立左上角的矩形 (30、10) 、寬度100和高度122。</span><span class="sxs-lookup"><span data-stu-id="2d4e4-129">The following example creates a rectangle with upper-left corner (30, 10), width 100, and height 122.</span></span> <span data-ttu-id="2d4e4-130">然後，程式碼會在該矩形內繪製一個字串。</span><span class="sxs-lookup"><span data-stu-id="2d4e4-130">Then the code draws a string inside that rectangle.</span></span> <span data-ttu-id="2d4e4-131">字串會限制為矩形，並換成個別單字不會中斷的方式。</span><span class="sxs-lookup"><span data-stu-id="2d4e4-131">The string is restricted to the rectangle and wraps in such a way that individual words are not broken.</span></span>

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

<span data-ttu-id="2d4e4-132">下圖顯示在矩形中繪製的文字。</span><span class="sxs-lookup"><span data-stu-id="2d4e4-132">The following illustration shows the text drawn in the rectangle.</span></span>

![小視窗的螢幕擷取畫面，其中包含 recangle，在其中會顯示句子的第一個部分](images/fontstext2.png)

<span data-ttu-id="2d4e4-134">在上述範例中，傳遞至 [**DrawString**](https://www.bing.com/search?q=**DrawString**) 方法的第四個引數是 [**RectF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf) 物件，可指定文字的周框。</span><span class="sxs-lookup"><span data-stu-id="2d4e4-134">In the preceding example, the fourth argument passed to the [**DrawString**](https://www.bing.com/search?q=**DrawString**) method is a [**RectF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf) object that specifies the bounding rectangle for the text.</span></span> <span data-ttu-id="2d4e4-135">第五個參數的類型為 [**StringFormat**](/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat)，引數為 **Null** ，因為不需要特殊字元串格式。</span><span class="sxs-lookup"><span data-stu-id="2d4e4-135">The fifth parameter is of type [**StringFormat**](/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat)— the argument is **NULL** because no special string formatting is required.</span></span>
