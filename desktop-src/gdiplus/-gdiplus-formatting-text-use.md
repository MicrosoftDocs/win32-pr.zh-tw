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
# <a name="formatting-text-gdi"></a><span data-ttu-id="16fc5-103">格式化文字 (GDI+)</span><span class="sxs-lookup"><span data-stu-id="16fc5-103">Formatting Text (GDI+)</span></span>

<span data-ttu-id="16fc5-104">若要將特殊格式套用至文字，請將 [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat)物件初始化，並將該物件的位址傳遞至 [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)類別的 [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush))方法。</span><span class="sxs-lookup"><span data-stu-id="16fc5-104">To apply special formatting to text, initialize a [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) object and pass the address of that object to the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span>

<span data-ttu-id="16fc5-105">若要在矩形中繪製格式化的文字，您需要 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)、 [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily)、 [**字型**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font)、 [**RectF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rectf)、 [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat)和 [**筆刷**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) 物件。</span><span class="sxs-lookup"><span data-stu-id="16fc5-105">To draw formatted text in a rectangle, you need [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics), [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font), [**RectF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rectf), [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat), and [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) objects.</span></span>

-   [<span data-ttu-id="16fc5-106">對齊文字</span><span class="sxs-lookup"><span data-stu-id="16fc5-106">Aligning Text</span></span>](#aligning-text)
-   [<span data-ttu-id="16fc5-107">設定制表位</span><span class="sxs-lookup"><span data-stu-id="16fc5-107">Setting Tab Stops</span></span>](#setting-tab-stops)
-   [<span data-ttu-id="16fc5-108">繪製垂直文字</span><span class="sxs-lookup"><span data-stu-id="16fc5-108">Drawing Vertical Text</span></span>](#drawing-vertical-text)

## <a name="aligning-text"></a><span data-ttu-id="16fc5-109">對齊文字</span><span class="sxs-lookup"><span data-stu-id="16fc5-109">Aligning Text</span></span>

<span data-ttu-id="16fc5-110">下列範例會在矩形中繪製文字。</span><span class="sxs-lookup"><span data-stu-id="16fc5-110">The following example draws text in a rectangle.</span></span> <span data-ttu-id="16fc5-111">每一行文字都是以 (的側邊) 為中心，而整個文字區塊則會在矩形中 (從上到下) 。</span><span class="sxs-lookup"><span data-stu-id="16fc5-111">Each line of text is centered (side to side), and the entire block of text is centered (top to bottom) in the rectangle.</span></span>


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



<span data-ttu-id="16fc5-112">下圖顯示矩形和中央文字。</span><span class="sxs-lookup"><span data-stu-id="16fc5-112">The following illustration shows the rectangle and the centered text.</span></span>

![視窗的螢幕擷取畫面，包含包含六行文字的矩形，水準置中](images/fontstext3.png)

<span data-ttu-id="16fc5-114">上述程式碼會呼叫 [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) 物件的兩個方法： [**StringFormat：： SetAlignment**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setalignment) 和 [**StringFormat：： SetLineAlignment**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setlinealignment)。</span><span class="sxs-lookup"><span data-stu-id="16fc5-114">The preceding code calls two methods of the [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) object: [**StringFormat::SetAlignment**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setalignment) and [**StringFormat::SetLineAlignment**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setlinealignment).</span></span> <span data-ttu-id="16fc5-115">**StringFormat：： SetAlignment** 的呼叫會指定每一行文字都在傳遞給 [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush))方法的第三個引數所指定的矩形中置中。</span><span class="sxs-lookup"><span data-stu-id="16fc5-115">The call to **StringFormat::SetAlignment** specifies that each line of text is centered in the rectangle given by the third argument passed to the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) method.</span></span> <span data-ttu-id="16fc5-116">**StringFormat：： SetLineAlignment** 的呼叫會指定文字區塊的中心 (在矩形中的上到下) 。</span><span class="sxs-lookup"><span data-stu-id="16fc5-116">The call to **StringFormat::SetLineAlignment** specifies that the block of text is centered (top to bottom) in the rectangle.</span></span>

<span data-ttu-id="16fc5-117">值 [\* \* \* \* StringAlignmentCenter \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringalignment) \* \* 是 **StringAlignment** 列舉的元素，它是在 Gdiplusenums 中宣告的。</span><span class="sxs-lookup"><span data-stu-id="16fc5-117">The value [\*\*\*\*StringAlignmentCenter\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringalignment) is an element of the **StringAlignment** enumeration, which is declared in Gdiplusenums.h.</span></span>

## <a name="setting-tab-stops"></a><span data-ttu-id="16fc5-118">設定制表位</span><span class="sxs-lookup"><span data-stu-id="16fc5-118">Setting Tab Stops</span></span>

<span data-ttu-id="16fc5-119">您可以藉由呼叫 [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat)物件的 [**StringFormat：： SetTabStops**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-settabstops)方法，然後將該 **StringFormat** 物件的位址傳遞至 [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)類別的 [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush))方法，來設定文字的定位停駐點。</span><span class="sxs-lookup"><span data-stu-id="16fc5-119">You can set tab stops for text by calling the [**StringFormat::SetTabStops**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-settabstops) method of a [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) object and then passing the address of that **StringFormat** object to the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span>

<span data-ttu-id="16fc5-120">下列範例會在150、250和350設定制表位。</span><span class="sxs-lookup"><span data-stu-id="16fc5-120">The following example sets tab stops at 150, 250, and 350.</span></span> <span data-ttu-id="16fc5-121">然後，程式碼會顯示名稱和測試分數的索引標籤式清單。</span><span class="sxs-lookup"><span data-stu-id="16fc5-121">Then the code displays a tabbed list of names and test scores.</span></span>


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



<span data-ttu-id="16fc5-122">下圖顯示索引標籤式的文字。</span><span class="sxs-lookup"><span data-stu-id="16fc5-122">The following illustration shows the tabbed text.</span></span>

![包含四個文字資料行的矩形圖例;每個資料行都保持支援](images/fontstext4.png)

<span data-ttu-id="16fc5-124">上述程式碼會將三個引數傳遞給 [**StringFormat：： SetTabStops**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-settabstops) 方法。</span><span class="sxs-lookup"><span data-stu-id="16fc5-124">The preceding code passes three arguments to the [**StringFormat::SetTabStops**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-settabstops) method.</span></span> <span data-ttu-id="16fc5-125">第三個引數是包含定位字元位移的陣列位址。</span><span class="sxs-lookup"><span data-stu-id="16fc5-125">The third argument is the address of an array containing the tab offsets.</span></span> <span data-ttu-id="16fc5-126">第二個引數表示該陣列中有三個位移。</span><span class="sxs-lookup"><span data-stu-id="16fc5-126">The second argument indicates that there are three offsets in that array.</span></span> <span data-ttu-id="16fc5-127">傳遞至 **StringFormat：： SetTabStops** 的第一個引數為0，表示陣列中的第一個位移是從位置0（周框矩形的左邊緣）測量的。</span><span class="sxs-lookup"><span data-stu-id="16fc5-127">The first argument passed to **StringFormat::SetTabStops** is 0, which indicates that the first offset in the array is measured from position 0, the left edge of the bounding rectangle.</span></span>

## <a name="drawing-vertical-text"></a><span data-ttu-id="16fc5-128">繪製垂直文字</span><span class="sxs-lookup"><span data-stu-id="16fc5-128">Drawing Vertical Text</span></span>

<span data-ttu-id="16fc5-129">您可以使用 [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) 物件來指定以垂直方式（而非水準）繪製文字。</span><span class="sxs-lookup"><span data-stu-id="16fc5-129">You can use a [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) object to specify that text be drawn vertically rather than horizontally.</span></span>

<span data-ttu-id="16fc5-130">下列範例會將值 [\* \* \* \* StringFormatFlagsDirectionVertical \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringformatflags) \* \* 傳遞給 [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat)物件的 [**StringFormat：： SetFormatFlags**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setformatflags)方法。</span><span class="sxs-lookup"><span data-stu-id="16fc5-130">The following example passes the value [\*\*\*\*StringFormatFlagsDirectionVertical\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringformatflags) to the [**StringFormat::SetFormatFlags**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setformatflags) method of a [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) object.</span></span> <span data-ttu-id="16fc5-131">將 **StringFormat** 物件的位址傳遞至 [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)類別的 [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush))方法。</span><span class="sxs-lookup"><span data-stu-id="16fc5-131">The address of that **StringFormat** object is passed to the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="16fc5-132">值 [\* \* \* \* StringFormatFlagsDirectionVertical \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringformatflags) \* \* 是 **system.drawing.stringformatflags>** 列舉的元素，它是在 Gdiplusenums 中宣告的。</span><span class="sxs-lookup"><span data-stu-id="16fc5-132">The value [\*\*\*\*StringFormatFlagsDirectionVertical\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringformatflags) is an element of the **StringFormatFlags** enumeration, which is declared in Gdiplusenums.h.</span></span>


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



<span data-ttu-id="16fc5-133">下圖顯示垂直文字。</span><span class="sxs-lookup"><span data-stu-id="16fc5-133">The following illustration shows the vertical text.</span></span>

![顯示包含順時針旋轉90度之文字的視窗的圖例](images/fontstext5.png)

 

 



