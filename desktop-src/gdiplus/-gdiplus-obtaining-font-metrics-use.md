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
# <a name="obtaining-font-metrics"></a><span data-ttu-id="d1731-103">取得字型計量</span><span class="sxs-lookup"><span data-stu-id="d1731-103">Obtaining Font Metrics</span></span>

<span data-ttu-id="d1731-104">[**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily)類別提供下列方法，以取得特定系列/樣式組合的各種計量：</span><span class="sxs-lookup"><span data-stu-id="d1731-104">The [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) class provides the following methods that retrieve various metrics for a particular family/style combination:</span></span>

-   <span data-ttu-id="d1731-105">[**FontFamily：： GetEmHeight**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getemheight) (FontStyle) </span><span class="sxs-lookup"><span data-stu-id="d1731-105">[**FontFamily::GetEmHeight**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getemheight)(FontStyle)</span></span>
-   <span data-ttu-id="d1731-106">[**FontFamily：： GetCellAscent**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getcellascent) (FontStyle) </span><span class="sxs-lookup"><span data-stu-id="d1731-106">[**FontFamily::GetCellAscent**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getcellascent)(FontStyle)</span></span>
-   <span data-ttu-id="d1731-107">[**FontFamily：： GetCellDescent**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getcelldescent) (FontStyle) </span><span class="sxs-lookup"><span data-stu-id="d1731-107">[**FontFamily::GetCellDescent**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getcelldescent)(FontStyle)</span></span>
-   <span data-ttu-id="d1731-108">[**FontFamily：： GetLineSpacing**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getlinespacing) (FontStyle) </span><span class="sxs-lookup"><span data-stu-id="d1731-108">[**FontFamily::GetLineSpacing**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getlinespacing)(FontStyle)</span></span>

<span data-ttu-id="d1731-109">這些方法所傳回的數位是字型設計單位，因此它們與特定 [**字型**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) 物件的大小和單位無關。</span><span class="sxs-lookup"><span data-stu-id="d1731-109">The numbers returned by these methods are in font design units, so they are independent of the size and units of a particular [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) object.</span></span>

<span data-ttu-id="d1731-110">下圖顯示上升、下降和行距。</span><span class="sxs-lookup"><span data-stu-id="d1731-110">The following illustration shows ascent, descent, and line spacing.</span></span>

![相鄰線上兩個字元的圖表，顯示資料格上升、資料格下降和行間距](images/fontstext7a.png)

<span data-ttu-id="d1731-112">下列範例會顯示 Arial 字型家族的一般樣式的度量。</span><span class="sxs-lookup"><span data-stu-id="d1731-112">The following example displays the metrics for the regular style of the Arial font family.</span></span> <span data-ttu-id="d1731-113">程式碼也會根據具有16圖元大小的 Arial 系列) 來建立 ([**字型**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) 物件，並以圖元為) 單位顯示該特定 **字型** 物件的度量 (。</span><span class="sxs-lookup"><span data-stu-id="d1731-113">The code also creates a [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) object (based on the Arial family) with size 16 pixels and displays the metrics (in pixels) for that particular **Font** object.</span></span>


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



<span data-ttu-id="d1731-114">下圖顯示上述程式碼的輸出。</span><span class="sxs-lookup"><span data-stu-id="d1731-114">The following illustration shows the output of the preceding code.</span></span>

![視窗的螢幕擷取畫面，其中包含字型大小和高度的文字，以及上移、下降和行距](images/fontstext8.png)

<span data-ttu-id="d1731-116">請注意上圖中前兩行的輸出。</span><span class="sxs-lookup"><span data-stu-id="d1731-116">Note the first two lines of output in the preceding illustration.</span></span> <span data-ttu-id="d1731-117">[**字型**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font)物件傳回的大小為16，而 [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily)物件傳回的 em 高度為2048。</span><span class="sxs-lookup"><span data-stu-id="d1731-117">The [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) object returns a size of 16, and the [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) object returns an em height of 2,048.</span></span> <span data-ttu-id="d1731-118">這兩個數字 (16 和 2048) 是在字型設計單位和單位之間轉換的關鍵， (在此案例中為 **字型** 物件的圖元) 。</span><span class="sxs-lookup"><span data-stu-id="d1731-118">These two numbers (16 and 2,048) are the key to converting between font design units and the units (in this case pixels) of the **Font** object.</span></span>

<span data-ttu-id="d1731-119">例如，您可以將從設計單位轉換成圖元，如下所示：</span><span class="sxs-lookup"><span data-stu-id="d1731-119">For example, you can convert the ascent from design units to pixels as follows:</span></span>

![將1854設計單位乘以16圖元除以2048設計單位的方程式，必須為14.484375 圖元](images/fontstext9.png)

<span data-ttu-id="d1731-121">上述程式碼會設定 [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf)物件的 *y* 資料成員，以垂直方式放置文字。</span><span class="sxs-lookup"><span data-stu-id="d1731-121">The preceding code positions text vertically by setting the *y* data member of a [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf) object.</span></span> <span data-ttu-id="d1731-122">`font.GetHeight(0.0f)`每一行新的文字都會增加 y 座標。</span><span class="sxs-lookup"><span data-stu-id="d1731-122">The y-coordinate is increased by `font.GetHeight(0.0f)` for each new line of text.</span></span> <span data-ttu-id="d1731-123">[**字型**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font)物件的 [**Font-size：： GetHeight**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-getheight(inreal))方法會傳回該特定 **字型** 物件的行間距， (以圖元為單位的) 。</span><span class="sxs-lookup"><span data-stu-id="d1731-123">The [**Font::GetHeight**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-getheight(inreal)) method of a [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) object returns the line spacing (in pixels) for that particular **Font** object.</span></span> <span data-ttu-id="d1731-124">在此範例中， **字型：： GetHeight** 傳回的數位為18.398438。</span><span class="sxs-lookup"><span data-stu-id="d1731-124">In this example, the number returned by **Font::GetHeight** is 18.398438.</span></span> <span data-ttu-id="d1731-125">請注意，這與將行間距度量轉換成圖元所取得的數位相同。</span><span class="sxs-lookup"><span data-stu-id="d1731-125">Note that this is the same as the number obtained by converting the line spacing metric to pixels.</span></span>

 

 
