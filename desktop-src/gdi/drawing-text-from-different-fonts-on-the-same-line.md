---
description: 字型家族內的不同類型樣式可以有不同的寬度。
ms.assetid: d21613ef-1ba4-40bb-b922-afe287556441
title: 在同一行上繪製不同字型的文字
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2eae2a7a332bd929b9a965462ce802734679f9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191949"
---
# <a name="drawing-text-from-different-fonts-on-the-same-line"></a><span data-ttu-id="4f7c5-103">在同一行上繪製不同字型的文字</span><span class="sxs-lookup"><span data-stu-id="4f7c5-103">Drawing Text from Different Fonts on the Same Line</span></span>

<span data-ttu-id="4f7c5-104">字型家族內的不同類型樣式可以有不同的寬度。</span><span class="sxs-lookup"><span data-stu-id="4f7c5-104">Different type styles within a font family can have different widths.</span></span> <span data-ttu-id="4f7c5-105">例如，系列的粗體和斜體樣式一律會比指定的點大小的羅馬樣式更寬。</span><span class="sxs-lookup"><span data-stu-id="4f7c5-105">For example, bold and italic styles of a family are always wider than the roman style for a specified point size.</span></span> <span data-ttu-id="4f7c5-106">當您在同一行上顯示或列印數種類型的樣式時，您必須追蹤線的寬度，以避免在彼此上方顯示或列印字元。</span><span class="sxs-lookup"><span data-stu-id="4f7c5-106">When you display or print several type styles on a single line, you must keep track of the width of the line to avoid having characters displayed or printed on top of one another.</span></span>

<span data-ttu-id="4f7c5-107">您可以使用兩個函式，以目前的字型來取得文字 (或範圍) 的寬度。</span><span class="sxs-lookup"><span data-stu-id="4f7c5-107">You can use two functions to retrieve the width (or extent) of text in the current font.</span></span> <span data-ttu-id="4f7c5-108">[GetTabbedTextExtent](/windows/desktop/api/Winuser/nf-winuser-gettabbedtextextenta)函數會計算字元字串的寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="4f7c5-108">The [GetTabbedTextExtent](/windows/desktop/api/Winuser/nf-winuser-gettabbedtextextenta) function computes the width and height of a character string.</span></span> <span data-ttu-id="4f7c5-109">如果字串包含一或多個定位字元，則字串的寬度會以指定的定位點-停用位置陣列為基礎。</span><span class="sxs-lookup"><span data-stu-id="4f7c5-109">If the string contains one or more tab characters, the width of the string is based upon a specified array of tab-stop positions.</span></span> <span data-ttu-id="4f7c5-110">[GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a)函式會計算文字行的寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="4f7c5-110">The [GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a) function computes the width and height of a line of text.</span></span>

<span data-ttu-id="4f7c5-111">必要時，系統會變更字元點陣圖以會合成字型。</span><span class="sxs-lookup"><span data-stu-id="4f7c5-111">When necessary, the system synthesizes a font by changing the character bitmaps.</span></span> <span data-ttu-id="4f7c5-112">若要合成粗體字的字元，系統會繪製字元兩次：在起始點，然後再繪製一個圖元到起點的右邊。</span><span class="sxs-lookup"><span data-stu-id="4f7c5-112">To synthesize a character in a bold font, the system draws the character twice: at the starting point, and again one pixel to the right of the starting point.</span></span> <span data-ttu-id="4f7c5-113">若要以斜體字型合成字元，系統會在字元資料格的底部繪製兩個數據列，將起點向右移動一個圖元、繪製接下來的兩個數據列，然後繼續直到繪製該字元為止。</span><span class="sxs-lookup"><span data-stu-id="4f7c5-113">To synthesize a character in an italic font, the system draws two rows of pixels at the bottom of the character cell, moves the starting point one pixel to the right, draws the next two rows, and continues until the character has been drawn.</span></span> <span data-ttu-id="4f7c5-114">藉由移動圖元，每個字元會顯示為向右切變。</span><span class="sxs-lookup"><span data-stu-id="4f7c5-114">By shifting pixels, each character appears to be sheared to the right.</span></span> <span data-ttu-id="4f7c5-115">切變數是字元高度的函式。</span><span class="sxs-lookup"><span data-stu-id="4f7c5-115">The amount of shear is a function of the height of the character.</span></span>

<span data-ttu-id="4f7c5-116">撰寫包含多個字型之文字行的其中一種方式，是在每次呼叫 [TextOut](/windows/desktop/api/Wingdi/nf-wingdi-textouta)之後使用 [**GetTextExtentPoint32**](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a)函式，並將長度新增至目前的位置。</span><span class="sxs-lookup"><span data-stu-id="4f7c5-116">One way to write a line of text that contains multiple fonts is to use the [**GetTextExtentPoint32**](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a) function after each call to [TextOut](/windows/desktop/api/Wingdi/nf-wingdi-textouta) and add the length to a current position.</span></span> <span data-ttu-id="4f7c5-117">下列範例會寫入「這是範例字串」這一行。</span><span class="sxs-lookup"><span data-stu-id="4f7c5-117">The following example writes the line "This is a sample string."</span></span> <span data-ttu-id="4f7c5-118">針對 "This a" 使用粗體字元，為 "sample" 切換為斜體字元，然後針對 "string" 傳回粗體字字元。</span><span class="sxs-lookup"><span data-stu-id="4f7c5-118">using bold characters for "This is a", switches to italic characters for "sample", then returns to bold characters for "string."</span></span> <span data-ttu-id="4f7c5-119">列印所有字串之後，它會還原系統預設字元。</span><span class="sxs-lookup"><span data-stu-id="4f7c5-119">After printing all the strings, it restores the system default characters.</span></span>


```C++
int XIncrement; 
int YStart; 
TEXTMETRIC tm; 
HFONT hfntDefault, hfntItalic, hfntBold; 
SIZE sz; 
LPSTR lpszString1 = "This is a "; 
LPSTR lpszString2 = "sample "; 
LPSTR lpszString3 = "string."; 
HRESULT hr;
size_t * pcch;
 
// Create a bold and an italic logical font.  
 
hfntItalic = MyCreateFont(); 
hfntBold = MyCreateFont(); 
 
 
// Select the bold font and draw the first string  
// beginning at the specified point (XIncrement, YStart).  
 
XIncrement = 10; 
YStart = 50; 
hfntDefault = SelectObject(hdc, hfntBold); 
hr = StringCchLength(lpszString1, 11, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        }
TextOut(hdc, XIncrement, YStart, lpszString1, *pcch); 
 
// Compute the length of the first string and add  
// this value to the x-increment that is used for the  
// text-output operation.  

hr = StringCchLength(lpszString1, 11, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        } 
GetTextExtentPoint32(hdc, lpszString1, *pcch, &sz); 
XIncrement += sz.cx; 
 
// Retrieve the overhang value from the TEXTMETRIC  
// structure and subtract it from the x-increment.  
// (This is only necessary for non-TrueType raster  
// fonts.)  
 
GetTextMetrics(hdc, &tm); 
XIncrement -= tm.tmOverhang; 
 
// Select an italic font and draw the second string  
// beginning at the point (XIncrement, YStart).  
 
hfntBold = SelectObject(hdc, hfntItalic); 
GetTextMetrics(hdc, &tm); 
XIncrement -= tm.tmOverhang;
hr = StringCchLength(lpszString2, 8, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        } 
TextOut(hdc, XIncrement, YStart, lpszString2, *pcch); 
 
// Compute the length of the second string and add  
// this value to the x-increment that is used for the  
// text-output operation.  

hr = StringCchLength(lpszString2, 8, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        }  
GetTextExtentPoint32(hdc, lpszString2, *pcch, &sz); 
XIncrement += sz.cx; 
 
// Reselect the bold font and draw the third string  
// beginning at the point (XIncrement, YStart).  
 
SelectObject(hdc, hfntBold);
hr = StringCchLength(lpszString3, 8, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        }  
TextOut(hdc, XIncrement - tm.tmOverhang, YStart, lpszString3, 
            *pcch); 
 
// Reselect the original font.  
 
SelectObject(hdc, hfntDefault); 
 
// Delete the bold and italic fonts.  
 
DeleteObject(hfntItalic); 
DeleteObject(hfntBold); 
```



<span data-ttu-id="4f7c5-120">在此範例中， [GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a) 函式會使用指定字串的長度和高度，初始化 [大小](/previous-versions//dd145106(v=vs.85)) 結構的成員。</span><span class="sxs-lookup"><span data-stu-id="4f7c5-120">In this example, the [GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a) function initializes the members of a [SIZE](/previous-versions//dd145106(v=vs.85)) structure with the length and height of the specified string.</span></span> <span data-ttu-id="4f7c5-121">[GetTextMetrics](/windows/desktop/api/Wingdi/nf-wingdi-gettextmetrics)函式會捕獲目前字型的懸垂。</span><span class="sxs-lookup"><span data-stu-id="4f7c5-121">The [GetTextMetrics](/windows/desktop/api/Wingdi/nf-wingdi-gettextmetrics) function retrieves the overhang for the current font.</span></span> <span data-ttu-id="4f7c5-122">因為如果字型是 TrueType 字型，所以懸垂為零，而懸垂值不會變更字串位置。</span><span class="sxs-lookup"><span data-stu-id="4f7c5-122">Because the overhang is zero if the font is a TrueType font, the overhang value does not change the string placement.</span></span> <span data-ttu-id="4f7c5-123">但是對於點陣字型而言，使用懸垂值是很重要的。</span><span class="sxs-lookup"><span data-stu-id="4f7c5-123">For raster fonts, however, it is important to use the overhang value.</span></span>

<span data-ttu-id="4f7c5-124">懸垂會從粗體字串減去一次，如果字型是點陣字型，則會將後續字元放在接近字串結尾的字元。</span><span class="sxs-lookup"><span data-stu-id="4f7c5-124">The overhang is subtracted from the bold string once, to bring subsequent characters closer to the end of the string if the font is a raster font.</span></span> <span data-ttu-id="4f7c5-125">因為懸垂會影響點陣字型中的斜體字串開頭和結尾，所以字元會從指定位置的右邊開始，並在最後一個字元資料格的端點左邊結束。</span><span class="sxs-lookup"><span data-stu-id="4f7c5-125">Because overhang affects both the beginning and end of the italic string in a raster font, the glyphs start at the right of the specified location and end at the left of the endpoint of the last character cell.</span></span> <span data-ttu-id="4f7c5-126"> ([**GetTextExtentPoint32**](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a) 函式會抓取字元資料格的範圍，而不是字元的範圍。 ) 若要考慮點陣斜體字串中的懸垂，範例會先減去懸垂再放置字串，然後再將它重新減去，然後再放置後續字元。</span><span class="sxs-lookup"><span data-stu-id="4f7c5-126">(The [**GetTextExtentPoint32**](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a) function retrieves the extent of the character cells, not the extent of the glyphs.) To account for the overhang in the raster italic string, the example subtracts the overhang before placing the string and subtracts it again before placing subsequent characters.</span></span>

<span data-ttu-id="4f7c5-127">[SetTextJustification](/windows/desktop/api/Wingdi/nf-wingdi-settextjustification)函式會在文字行中將額外的空格新增至分行符號。</span><span class="sxs-lookup"><span data-stu-id="4f7c5-127">The [SetTextJustification](/windows/desktop/api/Wingdi/nf-wingdi-settextjustification) function adds extra space to the break characters in a line of text.</span></span> <span data-ttu-id="4f7c5-128">您可以使用 [GetTextExtentPoint](/windows/desktop/api/WinGdi/nf-wingdi-gettextextentpointa) 函式來判斷字串的範圍，然後從該行應該佔用的總空間量減去該範圍，並使用 [**SetTextJustification**](/windows/win32/api/wingdi/nf-wingdi-settextjustification) 函式將額外的空間分配給字串中的分隔字元。</span><span class="sxs-lookup"><span data-stu-id="4f7c5-128">You can use the [GetTextExtentPoint](/windows/desktop/api/WinGdi/nf-wingdi-gettextextentpointa) function to determine the extent of a string, then subtract that extent from the total amount of space the line should occupy, and use the [**SetTextJustification**](/windows/win32/api/wingdi/nf-wingdi-settextjustification) function to distribute the extra space among the break characters in the string.</span></span> <span data-ttu-id="4f7c5-129">[SetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-settextcharacterextra)函式會在所選字型中的每個字元資料格加上額外的空間，包括 break 字元。</span><span class="sxs-lookup"><span data-stu-id="4f7c5-129">The [SetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-settextcharacterextra) function adds extra space to every character cell in the selected font, including the break character.</span></span> <span data-ttu-id="4f7c5-130"> (您可以使用 [GetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharacterextra) 函式來判斷目前新增至字元資料格的額外空間量;預設設定為零。 ) </span><span class="sxs-lookup"><span data-stu-id="4f7c5-130">(You can use the [GetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharacterextra) function to determine the current amount of extra space being added to the character cells; the default setting is zero.)</span></span>

<span data-ttu-id="4f7c5-131">您可以使用 [GetCharWidth32](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidth32a) 或 [GetCharABCWidths](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsa) 函式來取得字型中的個別字元寬度，以較大的精確度來放置字元。</span><span class="sxs-lookup"><span data-stu-id="4f7c5-131">You can place characters with greater precision by using the [GetCharWidth32](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidth32a) or [GetCharABCWidths](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsa) function to retrieve the widths of individual characters in a font.</span></span> <span data-ttu-id="4f7c5-132">[**GetCharABCWidths**](/windows/win32/api/wingdi/nf-wingdi-getcharabcwidthsa)函式比 [**GetCharWidth32**](/windows/win32/api/wingdi/nf-wingdi-getcharwidth32a)函數更為精確，但只能搭配 TrueType 字型使用。</span><span class="sxs-lookup"><span data-stu-id="4f7c5-132">The [**GetCharABCWidths**](/windows/win32/api/wingdi/nf-wingdi-getcharabcwidthsa) function is more accurate than the [**GetCharWidth32**](/windows/win32/api/wingdi/nf-wingdi-getcharwidth32a) function, but it can only be used with TrueType fonts.</span></span>

<span data-ttu-id="4f7c5-133">ABC 間距也可讓應用程式執行非常精確的文字對齊。</span><span class="sxs-lookup"><span data-stu-id="4f7c5-133">ABC spacing also allows an application to perform very accurate text alignment.</span></span> <span data-ttu-id="4f7c5-134">例如，當應用程式靠右對齊點陣羅馬字型但未使用 ABC 間距時，會將前進寬度計算為字元寬度。</span><span class="sxs-lookup"><span data-stu-id="4f7c5-134">For example, when the application right aligns a raster roman font without using ABC spacing, the advance width is calculated as the character width.</span></span> <span data-ttu-id="4f7c5-135">這表示點陣圖中圖像右邊的空白字元會對齊，而非圖像本身。</span><span class="sxs-lookup"><span data-stu-id="4f7c5-135">This means the white space to the right of the glyph in the bitmap is aligned, not the glyph itself.</span></span> <span data-ttu-id="4f7c5-136">藉由使用 ABC 寬度，當對齊文字時，應用程式的放置和移除空白字元會有更大的彈性，因為它們具有可讓它們精確控制 intercharacter 間距的資訊。</span><span class="sxs-lookup"><span data-stu-id="4f7c5-136">By using ABC widths, applications have more flexibility in the placement and removal of white space when aligning text, because they have information that allows them to finely control intercharacter spacing.</span></span>

 

 
